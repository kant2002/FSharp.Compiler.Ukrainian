Nuget пакет для Ф# компілятора 
======================

Цей репозіторій містить інфраструктуру для створення Nuget пакету із компілятором Ф#.

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