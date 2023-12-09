# Myapp
It is sample ASP.NET core web app project with default template is created. Later the appsettings.json and Index.cshtml were  updated to reference the key vault secret.

appsettings.json was updated with the bewlow entry.

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*",
  "FromMessage":  "from appsettings.json file"
}
```
Index.cshtml was updated with the following code.

```cshtml
@page
@model IndexModel
@{
    ViewData["Title"] = "Home page";
}


@using Microsoft.Extensions.Configuration
@inject IConfiguration Configuration


<div class="text-center">
    <h1 class="display-4">Welcome @Configuration["FromMessage"]</h1>
    <p>Learn about <a href="https://docs.microsoft.com/aspnet/core">building Web apps with ASP.NET Core</a>.</p>
</div>
```


