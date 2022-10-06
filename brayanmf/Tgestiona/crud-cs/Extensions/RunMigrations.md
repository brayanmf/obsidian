#### RunMigrations.cs
Como ejecutamos las migraciones?. gracias a
FluentMigrator crear una extensión que ejecute nuestras migraciones justo antes de que se ejecute nuestra aplicación.

```
using System;

using Microsoft.Extensions.DependencyInjection;

using Microsoft.Extensions.Hosting;

using FluentMigrator.Runner;

  

namespace TodoAPI.Extensions

{

    public static class MigrationManager

    {

        public static IHost MigrateDatabase(this IHost host)

        {

            using (var scope = host.Services.CreateScope())

            {

                var migrationService = scope.ServiceProvider.GetRequiredService<IMigrationRunner>();

                try

                {

                    migrationService.ListMigrations();

                    migrationService.MigrateUp();

                }

                catch (Exception e)

                {

                    Console.WriteLine(e.Message);

                    throw;

                }

            }

            return host;

        }

    }

}
```