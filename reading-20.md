# Razor Pages

## Razor Pages vs MVC
#### MVC
- Typical path goes as follows: User requests home.index, ASP.NET routes request to controller action, the controller does its stuff, it goes to the ASP.NET view engine, the user sees the rendered view.
- The routing engine is responsible for connecting a route to a controller action.
- The logic for validating requests and callign services live in the controller.
- Views are housed in .cshtml file of the same as the controller that is within a `Views` directory.
- Views are usually associated with ViewModels that has properties for the data you wish to display.
#### Razor Pages
- Typical path goes as follows: User requests something, ASP.NET routes the request to razor page, Razor page performs an action, views engine renders a view, the user sees the rendered view.
- With razor pages, the request itself holds the name of the view that will be searched for. The razor page acts directly as the controller.
- To qualify as a razor page, the .cshtml file needs to be inside a `Pages` directory with `@page` inside it.
- Each razor page has an associated .cshtml.cs file of the same name that handles the application code.

## Razor Pages Setup
- Configuration starts in the `startup.cs` file: In `ConfigureServices` add `services.AddMvc()` and in `Configure` add `app.UseMvc()`.
- In any views files located in the `Pages` directory, `@page` must be the first directive on the page signifying its use as a razor page.
- Files the may have use in many or all views are typically named using an _underscore.
- The `wwwroot` folder contains static files such as HTML, Javascript, and CSS.
- `appSettings.JSON` contains configuration information such as connection strings.
- `Program.cs` is the entry point for the entire application.
- `Startup.cs` contains code that configures app behavior.



[Table of Contents](README.md)