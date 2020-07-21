# CustomAnalyzer

Project template for custom FxCop and StyleCop rulesets distributed as a NuGet package. Installs [Microsoft.CodeAnalysis.FxCopAnalyzers](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers) and [StyleCop.Analyzers](https://www.nuget.org/packages/StyleCop.Analyzers) as dependencies.

## Step 1: cherry-pick the rules

Copy the contents of this repository and edit the [`.ruleset` files](Rulesets/) enabling the desired rules:

```xml
<!-- change "None" for either "Warning" or "Error" on the desired rule -->
<Rule Id="CA1000" Action="None" />
```

## Step 2: choose a cool name

Rename `CustomAnalyzer.csproj` with a cool name like `YourCoolCompany.Analyzer.csproj`. Modify the package description and version if needed.

## Step 3: pack it up

Run `dotnet pack` and there you have it, your own pre-configured analyzer as a `.nupkg`. `dotnet add package` wherever you like, no further configuration needed.
