
nutget or dotnet
1.install the packages 
- System.IdentityModel.Tokens.Jwt; // create token
- Microsft.IdentityModel.Tokens //install nuget for jwt generating key for jwt
- Microsft.AspNetCore.Authentication.JwtBearer //authorizacion for controller
2. update in startup.cs file
3. create the jwtService to generate Tokens in String Format
4. Send it whenever login is Successfull
5. receive this token in frontend and store it in Browser's Locals