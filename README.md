# ankitvijay-ParseCsProject
ParseCsProject is a command line utility to parse a collection of CS Projects (.csproj files) and change settings like FxCop, adding custom dictionary etc in one go.

How to Use
ParseCsProject accepts following agguments.
<<FilePath>> - This is a mandatory argument. You need to pass the absolute or relative path for text file where list of projects exists. E
    Example: namespace.txt
    The content of the file should be list of csproj file paths that need to be modified. Each line should contain one file path.
    
[/C] or [/Configuration] - Defines the comma separated values of configuraton for which the settings have to be modified.
    Example: /C=Debug,Release
    Default Value: Debug
    
[/P] or [/Platform] - Defines plaform for which settings have to be modified.
    Example: /P=AnyCPU
    Default Value: AnyCPU
    
[/Twe] or [/TreatWarningsAsErrors] - Set this value to true to treat warnigns as errors. False, otherwise
    Example: /Twe="true"
    Default Value: NA
    
[/Rca] or [/RunCodeAnalysis] - Set this value to true to enable code analysis on project build. False, otherwise
    Example: /rca="true"
    Default Value: NA
    
[/Fr] or [/FxCopRuleSet] - Set the code analyis ruleset. Provide the ruleset relative path.
    Example: /fr="..\..\myruleset.ruleset"
    Default Value: NA
    
[/Dl] or [/DefaultLanguague] - Defines the project default language.
    Example: /Dl="en-GB"
    Default Value: en-US
    
[/cd] or [/CustomDictionary] - Adds code analysis dictionary as link to the project. Provide the file relative path.
    Example: /cd="..\..\CustomDictionary.xml"
    Default Value: en-US

    
Full Example:

ParseCsProject "C:\ProjectFiles\namespace.txt" /c="Debug,Release" /p="AnyCPU" /twe="true" /rca="false" /fr="..\..\myruleset.ruleset" /dl="en-GB" /cd="..\..\CustomDictionary.xml"
