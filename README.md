# affected-reference-problem


## Inspect included files in Problem.Api

`dotnet msbuild -target:DebugAppStuff .\backend\domains\test\lib\Problem.ApiClient\Problem.ApiClient.csproj`

## Test with tool locally

1. Clone this repo
1. dotnet tool restore
1. Hit an enter in OpenApi/subdir/Proj1.json and save.
1. dotnet affected --dry-run

Expected result: The project `backend/domains/test/lib/Problem.ApiClient/Problem.ApiClient.csproj` is detected as changed.

## Debug affected

1. Hit an enter in OpenApi/subdir/Proj1.json and save.
1. Start your clone of dotnet-affected
1. Open launchSettings.json and edit the section "affected" to point to your clone of this repo.
   `"commandLineArgs": "-v -p #path_to_repo# --output-dir C:\\Temp --output-name changed"`

Start the command "affected" in debug.

Expected result: The project `backend/domains/test/lib/Problem.ApiClient/Problem.ApiClient.csproj` is detected as changed.
