# ApplyVersionToAssemblies
Look for a 0.0.0.0 pattern in the build number.  If found use it to version the assemblies. For example, if the 'Build number format' build process parameter 

``
$(BuildDefinitionName)_$(Year:yyyy).$(Month).$(DayOfMonth)$(Rev:.r) then your build numbers come out like this: "Build HelloWorld_2013.07.19.1" This script would then apply version 2013.07.19.1 to your assemblies.
``
# Other Files Supported for Versioning
- .sqlproj : SQL Server Project
- .nuspec : Semantic Version 1.0 and 2.0 

# Build and Release Support
Due to the different folder available the script checks if an Artifacts Directory is present
If using for Semantic Versioning a variable $(semanticVersion) is published so other tasks are able to consume the value
