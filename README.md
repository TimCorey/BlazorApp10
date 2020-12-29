# Blazor Server CSS Bug in .NET 5
This code reproduces an issue in Blazor Server (.NET 5) where switching the environment away from development causes the application to lose the BlazorApp10.style.css file.

## Steps To Test This Code
Run the code in Kestrel. It will work fine. Then, launch it in IIS Express. The styling will be missing, including the menu, because the BlazorApp10.style.css file is missing (404 error).

## About the Code
This is a stock Blazor Server (.NET 5) template with only one change - I set the IIS Express ASPNETCORE_ENVIRONMENT variable to "Production". No other changes were made to the template.
