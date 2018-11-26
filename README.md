# EF Core Mess-around (Database First)

## Create a project

```shell
dotnet new classlib
```

## Fix the csproj file

Make sure you have a runtime version in the Model CSPROJ file: -

```XML
<Project Sdk="Microsoft.NET.Sdk">  
    <PropertyGroup>
        <TargetFramework>netcoreapp2.1</TargetFramework>
        <RuntimeFrameworkVersion>2.1.6</RuntimeFrameworkVersion>
    </PropertyGroup>
 </Project>
 ```

## Add required NuGet packages

```shell
dotnet add package Microsoft.EntityFrameworkCore.Design
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
```

### Rebuild framework

```shell
dotnet ef dbcontext scaffold "Server=localhost;Database=EfDemo;User Id=SA;Password=P@55w0rd;" Microsoft.EntityFrameworkCore.SqlServer -o Models
```
