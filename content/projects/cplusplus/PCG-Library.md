+++
title = 'PCG Library'
date = 2024-09-01
draft = true
layout = "cplusplus"
repo = "https://github.com/SpeedyE1780/PCG-Tool"
demo = "https://www.youtube.com/embed/videoseries?si=Qc-ZjgTxP2TnKMe9&amp;list=PLdX38AkXi8wAdDMCTZNRRvFEx8e7FYPco"
tools = ["images/tools/cmake-original.svg", "images/tools/csharp-original.svg", "images/tools/python-original.svg", "images/tools/unity-original.svg", "images/tools/unrealengine-original.svg", "images/tools/playcanvas.png", "images/tools/nextjs-original.svg", "images/tools/asciidoc-og.png", "images/tools/doxygen.svg"]
summary = "Library that generates content procedurally it's implemented with multiple languages and engines. It also provides web services like a REST API and Web App"
+++

This was my major project for my postgraduate.

The PCG Library is made up of the C++ DLL library that can be used with C++ and other languages by using the C DLL.

This library can currently be used with C#, Unity, Unreal and Python.

A REST API is available to use the library with languages not yet implemented.

The library can be previewed using the web app.

Code documentation is generated with doxygen.

A manual is created using asciidoc.

## Wrappers

### C# Wrapper

Uses DLLImport to call native functions.
Redefines C++ classes and enums.

### Python Wrapper

Uses ctypes to call native function.
Redefines C++ classes and enums.

## Engine Implementations

### Unity Package

{{< youtube-demo demo="https://www.youtube.com/embed/w16gru7T23M?si=Qs9tzBNtra-c0CCF" >}}

A Unity package was developed that relies on the C# Wrapper.
The package adds editor windows to generate content during edit mode.
Content can also be generated during play mode using only the C# Wrapper if the editor windows are not needed.

### Unreal Plugin

{{< youtube-demo demo="https://www.youtube.com/embed/K3PAtEFqO30?si=sll0qLp_qvFR8oNK" >}}

An Unreal plugin was developed that adds the C++ library as a third party library and allows generating content during runtime.
A second plugin was developed that adds editor window to generate content during edit mode.

## Web Services

### Web API

{{< youtube-demo demo="https://www.youtube.com/embed/P_mNN8f9NCI?si=SWu3H1UM6HA9isSf" >}}

The PCG Web API is an ASP.NET Core REST API.
It takes the parameters in the request body and uses the C# Wrapper to generate content and returns the result as JSON in the response.

### Web APP

{{< youtube-demo demo="https://www.youtube.com/embed/EbdXR-TMIEI?si=OlEJ7uZW33DBd-o1" >}}

The PCG Web APP is a web application built with NextJS that previews the engine's functionality on the web.
It shows the result of combinations and sequences as text output.
It displays the result of level generation using the PlayCanvas engine and allows moving around in the scene to look at the result.
The generated JSON can be copied from the text area where it is displayed.
