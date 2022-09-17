# style-guide
Style rules and guidelines for lightsource-nz software projects

This repository is a single location for all documents and references related to code style and project organization conventions for lightsource-nz software projects. The majority of C-language specific style rules derive from the ZeroMQ [21/CLASS Specification](https://rfc.zeromq.org/spec/21/), which provides a well thought-out and consistent set of conventions for organization and naming in software projects, as well as a good basis for implementing separation of concerns in large bodies of C source code.

C/C++ projects should use the most recent (finalized) version of their corresponding language specification- at time of writing C18 or C++17. This is one area where lightsource-nz code style differs from the 21/CLASS spec, which effectively mandates the use of C89 or C99. Existing projects should maintain the language level which was current at their time of creation, migrating projects to newer language specs may be done at the discretion of the project maintainer.

Projects written in C or C++ use CMake scripts for build and test automation, and for inter-project dependency management. This provides the ability to structure large, complex projects as hierarchies or aggregations of modules, with manageable and bounded build script complexity. Software library projects for desktop or server target platforms should be defined as CMake PUBLIC libs, while those targeting bare-metal embedded platforms should be CMake INTERFACE libs.
