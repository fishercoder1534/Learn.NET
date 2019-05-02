This project was created following this tutorial: https://docs.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/razor-pages-start

1. run this command `dotnet new webapp -o RazorPagesMovie`
2. run `dotnet run`
3. run `dotnet add package Microsoft.EntityFrameworkCore.SQLite`
4. run `dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design`
5. run `dotnet add package Microsoft.EntityFrameworkCore.Design`
6. Scaffold the movie model
    a. install the scaffolding tool, `dotnet tool install --global dotnet-aspnet-codegenerator`
    b. run `dotnet aspnet-codegenerator razorpage -m Movie -dc RazorPagesMovieContext -udl -outDir Pages/Movies --referenceScriptLibraries`
    c. run `dotnet aspnet-codegenerator razorpage -h`
7. initial migration
    a. run `dotnet ef migrations add InitialCreate` which generates code to create the initial database schema. The schema is based on the model specified in the DbContext (In the RazorPagesMovieContext.cs file). 
    b. run `dotnet ef database update`
