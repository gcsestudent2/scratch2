# .NET Core 2.0 - Hello, World  App

Requires Docker (Linux containers)

## Build Container

```bash
$ docker build -t hello-world-dotnet .
```

## Run Container

```bash
$ docker run hello-world-dotnet
```

This will return

```text
Hello World!
```

    Starting point for this repo is :
    git clone https://github.com/richardjortega/hello-world-dotnet-docker
    Then change various references to .NET2 to .NET9.0
    Delete cloned .git folder (rm -rf .git) and move everything up a level because debugging seems to need it.
    
    Install vscode extension C# Dev Kit; (which also brings in C#; .NET Core Tools)
    Can then run and use debugger breakpoints.
    Next step is to see if the debugger works with VB.NET too (fingers crossed).
    Would also like to understand how to run debugger in a container (like in following example, which sadly isn't working). 
    MarcelDempers - Debugging .NET Core in Docker with VSCode - https://www.youtube.com/watch?v=ds2bud0ZYTY
    
    Docker commands also work after following modifications to Dockerfile :
    microsoft/dotnet:2.1-sdk -> mcr.microsoft.com/dotnet/sdk:9.0
    microsoft/dotnet:2.1-runtime -> mcr.microsoft.com/dotnet/runtime:2.0
    A few useful docker commands :
    docker ps -a
    docker image ls 
    docker container rm <interesting_easley> (change this to a different name !)
    docker image rm hello-world-dotnet
