### Promgram
- program.cs
 Add for fluentMigrator
``` 
// Add for fluentMigrator

builder.services.AddLogging(c => c.AddFluentMigratorConsole())

            .AddFluentMigratorCore()

            .ConfigureRunner(c => c.AddSqlServer2016()

            .WithGlobalConnectionString(Configuration.GetConnectionString("SqlConnection"))

            .ScanIn(Assembly.GetExecutingAssembly()).For.Migrations());
			
```		