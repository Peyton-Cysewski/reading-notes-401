# View Components

## Intro to View Components
View Components are very similar to partials insofar as they can provide specific parts of a view that will make up a complete view. Components do not work with model binding but instead use the data that is passed into it when being called. To make a View Component, the associated class needs to either derive from `ViewComponent`, use the `[ViewComponent]` attribute, derive from a class like the prior two, or end with `ViewComponent` in its name (as a suffix). The logic associated within this class is housed in an `Invoke` method with its parameters coming from the invocation of the method, not model binding (as mentioned previously). These view components never handle requests directly.</br>
Calling a view component in a view looks like: `@await Component.InvokeAsync("Name of view component", {Anonymous Type Containing Parameters})`. It can also be done with the use of helper tags: example: `<vc:priority-list max-priority="2" is-done="false"></vc:priority-list>` but requires the component view's name to be registered with the help tag declaration inside of `_ViewImports.cshtml`: `@addTagHelper *, MyWebApp`. The actual view should be stored in the file directory: `/Views/Shared/Components/{View Component Name}/{View Name}` and the View Name should be `Default.cshtml`. 



[Table of Contents](README.md)