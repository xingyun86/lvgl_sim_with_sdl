# LVGL - PC Simulator using Visual Studio 2019

This is a pre-configured Visual Studio project to try LVGL on a Windows PC. The project uses the [SDL](https://www.libsdl.org/) library which is copied and linked to the project, so you can compile it without any extra dependencies. The 64 bit libraries are used so it will work out-of-the-box on 64-bit systems.

Instructions for cloning, building and running the application are found below.

**This project is not for Visual Studio Code, it is for Visual Studio 2019.**

## How to Clone

This repository contains other, necessary LVGL software repositories as [git sub-modules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).  Those sub-modules are not pulled in with the normal git clone command and they will be needed.  There are a couple of techniques to pull in the submodules.

### Everything at Once

This command will clone the lv_sim_visual_studio_sdl repository and all submodules in a single step.

```
git clone https://github.com/xingyun86/lvgl_sim_sdl.git
```

## How To Build & Run

Open the `lvgl_sim_sdl.sln` solution file in Visual Studio. Click on the _Local windows Debugger_ button in the top toolbar.  The included project will be built and run, launching from a cmd window.

## Trying Things Out

There are a list of possible test applications in the [main.c](lvgl_sim_sdl/main.c) file.  Each test or demo is launched via a single function call.  By default the `lv_demo_widgets` function is the one that runs, but you can comment that one out and choose any of the others to compile and run.

Use these examples to start building your own application test code inside the simulator.

## A Note About Versions

This repository has its sub-module references updated shortly after the release of new, major releases of LittlevGL's core [lvgl](https://github.com/lvgl/lvgl) project.  If you need to pull in bug fixes in the sub-modules in between major releases you will have to update the references on your own.  If source files are added or removed in the sub-modules then the visual studio project will likely need adjusting.  See the commit log for examples of sub-module updates and associated visual studio file changes.
