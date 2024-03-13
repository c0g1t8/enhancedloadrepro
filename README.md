# enhancedloadrepro

Repro of enhancedload Issue

```powerhsell
md server-hosted
pushd
cd server-hosted
dotnet new blazor -int None -o None
dotnet new blazor -int Server -o Server
dotnet new blazor -int WebAssembly -o WebAssembly
dotnet new blazor -int Auto -o Auto
popd

md wasm
pushd
cd wasm
dotnet new blazorwasm
popd

md maui-blazor
pushd
cd maui-blazor
dotnet new maui-blazor
popd
```

```powershell
dotnet new solution
dotnet sln add .\server-hosted\None\
dotnet sln add .\server-hosted\Server\
dotnet sln add .\server-hosted\WebAssembly\WebAssembly\
dotnet sln add .\server-hosted\WebAssembly\WebAssembly.Client\
dotnet sln add .\server-hosted\Auto\Auto\
dotnet sln add .\server-hosted\Auto\Auto.Client\
dotnet sln add .\wasm\
dotnet sln add .\maui-blazor\
```
