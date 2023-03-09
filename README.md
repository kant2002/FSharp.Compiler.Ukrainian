Nuget пакет для Ф# компілятора 
======================

Цей репозіторій містить інфраструктуру для створення Nuget пакету із компілятором [Ф#](https://github.com/kant2002/fsharp).

Щоб використати мову Ф# вам треба лише додати пакет FSharp.Compiler.Ukrainian
```
mkdir sample
cd sample
dotnet new console -lang F# -o .
dotnet add package FSharp.Compiler.Ukrainian
```

## Створення Nuget пакету

Спочатку треба скомпілювати сам компілятор Ф#
```
cd c:\d\
git clone https://github.com/kant2002/fsharp
cd fsharp
./build.cmd -c Release
```

а потім виконати цю команду у папці цього репозіторія.
```
dotnet pack -c Release /p:FSharpRoot=c:\d\fsharp
```