Maven-Webapp-Google-Closure
===========================

A maven webapp that compiles JS and CSS into the webapp war using google closure ant scripts.

This is a starter maven webapp that will run on port 9000.
It uses maven profiles to:

  - localhost: Compile CSS and JS locally within the webapp for rapid testing
  - dev: Compile CSS and JS into an exploded webapp folder where it packages resources into a jar.

The dev profile is used in a maven overlay situation, where you may have mutliple overlay folders containing more CSS and JS files.
That said, it also works fine without utilizing maven overlays.

----

This project references the basic GSS build script I have posted here:
https://github.com/scarrillo/GSS-Build

As well as:

Closure Compiler jar and GSS examples from: http://code.google.com/p/closure-stylesheets/
