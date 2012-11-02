Maven-Webapp-Google-Closure
===========================

A maven webapp that compiles JS and CSS into the webapp war using google closure ant scripts**.

This is a starter maven webapp that will run on port 9000.
It uses maven profiles to:

  - localhost: Compile CSS and JS locally within the webapp for rapid testing
  - dev: Compile CSS and JS into an exploded webapp folder where they will be packaged into the final webapp war.

The dev profile is mainly used in a maven overlay situation, where you may have mutliple overlay projects containing more CSS and JS files.
That said, it also works fine as a single project, without maven overlays.

** Ant scripts:

The JS compiler ant script is from:
  http://code.google.com/p/closure-compiler/wiki/BuildingWithAnt

The CSS compiler ant script is a variant of a build script I wrote and posted here:
  https://github.com/scarrillo/GSS-Build
  - This variant has a few added options for managing compilation and recompiling via:
    Sublime Text or command line with mvn antrun:run

Sublime Text Maven Build System
===========================
I've also included a variant of a maven build system I use at work.
Place this in Sublime's /Packages/User/ dirctory and then associate the project with the "mvn-run" build system.

You can then:
- cmd + b: Start Jetty (and compile)
- alt + j: Recompile CSS and JS (without restarting jetty)
- cmd + shift + b: Stop and restart Jetty

Notes: Windows users, this Sublime build script is not 100% yet.

----
Closure Compiler jar and GSS examples from: http://code.google.com/p/closure-stylesheets/
