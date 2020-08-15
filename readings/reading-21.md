# Layouts

## What is a Layout
Layouts are part of a page that stays the same allowing the user to have a consistent experience in different areas of a website. For example, regardless of what page a user is on, they should see the same nav bar. In razor pages, these are usually held in a `Shared` directory within `Pages`. The naming convention with layouts is to use an underscore to indicate its shared nature. In an MVC framework with a `Views` folder, the same files would be kept with the same naming conventions. Layouts can also reference sections in a page. These sections can be required, but if it isn't found, then this will cause an exception to be thrown. Any code that needs to be run before any full view (not including layouts), needs to be placed in a `ViewStart.cshtml` file in the `Pages` directory.

## Tag Helpers
Tag helpers allow for server-side code to help with and be a part of rendering views, specifically in razor pages. To enable tag helpers to be available for a view, a `_ViewImports.cshtml` file has to be created with the line `@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers`. This file is inherited by all files in the Views or Pages directory by default. Tag helpers only modify the HTML element that they are directly attached to. They are commonly used in forms and anchors tags. They allows for a concise way of referencing the controller, action, and method all in one spot.<br>
- `asp-controller`:	The name of the controller.
- `asp-action`:	The name of the action method.
- `asp-area`:	The name of the area.
- `asp-page`:	The name of the Razor page.
- `asp-page-handler`:	The name of the Razor page handler.
- `asp-route`:	The name of the route.
- `asp-route-{value}`:	A single URL route value. For example, asp-route-id="1234".
- `asp-all-route-data`:	All route values.
- `asp-fragment`:	The URL fragment.



[Table of Contents](../README.md)
