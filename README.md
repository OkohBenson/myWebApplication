# myWebApplication

Dynamic website — ASP.NET Web Forms project (Visual Studio Web Application).

## Description
A small ASP.NET Web Forms website with sample pages (Home, About, Contact) and front-end assets (Bootstrap, jQuery). Built for .NET Framework 4.7.2 and intended to run under IIS Express from Visual Studio.

## Prerequisites
- Windows
- Visual Studio 2017/2019/2022 (with .NET desktop/web development workloads)
- .NET Framework 4.7.2
- NuGet CLI (optional) or allow Visual Studio to restore packages automatically

## Build & run (shortest path)
1. Clone the repository:

```bash
git clone https://github.com/OkohBenson/myWebApplication.git
cd myWebApplication
```

2. Restore NuGet packages (one of):

```bash
nuget restore myWebApplication.sln
# or let Visual Studio restore packages on first load
```

3. Build the solution (one of):

```bash
msbuild myWebApplication.sln /p:Configuration=Debug
# or open myWebApplication.sln in Visual Studio and Build
```

4. Run the project from Visual Studio (F5) — it is configured to use IIS Express at:

https://localhost:44366/

You can open that URL after starting the project (IIS Express will host the app locally).

## Notes
- The project target framework is .NET Framework 4.7.2 (see myWebApplication/myWebApplication.csproj).
- Front-end libraries included: jQuery 3.3.1, Bootstrap (CSS + JS). Bundling is configured in App_Start/BundleConfig.cs.
- If you prefer command-line hosting, you can publish the project and host under a full IIS or Azure App Service, but Visual Studio / IIS Express is the intended developer workflow.

## Files of interest
- myWebApplication/myWebApplication.csproj — project settings and IIS Express URL
- myWebApplication/Global.asax(.cs) — application start hooks
- myWebApplication/App_Start/BundleConfig.cs — bundling for CSS/JS
- myWebApplication/Default.aspx, About.aspx, Contact.aspx — example pages

