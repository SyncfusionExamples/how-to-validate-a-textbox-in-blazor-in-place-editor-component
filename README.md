# How to Validate a Textbox in the Syncfusion Blazor In-Place Editor Component

## Overview

This sample demonstrates how to validate user input within the Syncfusion [Blazor In-Place Editor](https://www.syncfusion.com/blazor-components/blazor-in-place-editor) while editing text content directly on a page. The application shows how validation can be applied to inline editing scenarios to ensure that users enter acceptable values before data is saved.

The sample focuses on textbox validation in an In-Place Editor control and includes examples of applying validation rules, displaying validation messages, adding custom error text, and restricting input length. The project is implemented as a hosted Blazor WebAssembly solution with separate Client, Server, and Shared projects.

## Key Features

- Uses the Syncfusion Blazor In-Place Editor component (`SfInPlaceEditor`) for inline text editing.
- Two-way binds the editor value using the `@bind-Value` directive.
- Embeds a Blazor `EditForm` inside the `EditorComponent` template to enable form validation during editing.
- Uses `DataAnnotationsValidator` to apply model-based validation rules.
- Uses the Syncfusion Blazor TextBox component (`SfTextBox`) as the editor input control.
- Displays validation errors using the Blazor `ValidationMessage` component.
- Demonstrates validation through a strongly-typed `ValidationModel` class.
- Applies the `[Required]` data annotation to prevent empty values.
- Uses the `[StringLength(10)]` data annotation to restrict input length to a maximum of 10 characters.
- Displays a custom validation message ("Name is too long") when the character limit is exceeded.
- Initializes the editor with a default value (`Andrew`) through the model.
- Includes a hosted Blazor WebAssembly application with client, server, and shared projects.
- Contains a sample weather forecast page demonstrating data retrieval from the hosted ASP.NET Core backend.
- Uses `HttpClient.GetFromJsonAsync<WeatherForecast[]>()` to request data from the server API.
- Implements an ASP.NET Core Web API controller (`WeatherForecastController`) that returns sample forecast data for client-side consumption.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the `ValidateTextBox.sln` solution file.
3. Restore all NuGet packages.
4. Build the solution.
5. Run the application using **Ctrl+F5**.

**Visual Studio Code**

1. Clone or download this repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the project directory.

```bash
dotnet restore
dotnet run
```

5. Open the local application URL displayed in the terminal after the application starts.

## Project Structure

- `Client/Pages/Index.razor` — Primary sample page demonstrating textbox validation within the Syncfusion SfInPlaceEditor component.
- `Client/Pages/FetchData.razor` — Weather forecast page that consumes data from the server using HttpClient.
- `Server/Controllers/WeatherForecastController.cs` — ASP.NET Core API controller that generates and returns weather forecast data.
- `Shared/WeatherForecast.cs` — Shared forecast model used by both the client and server projects.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Refer to the Syncfusion In-Place Editor documentation: https://blazor.syncfusion.com/documentation/in-place-editor/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.