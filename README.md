[![Build Status](https://travis-ci.org/lasote/conan-jansson.svg)](https://travis-ci.org/lasote/conan-jansson)


# conan-jansson

[Conan.io](https://conan.io) package for lib jansson library: http://www.jansson.org/pub/png/jansson.html

The packages generated with this **conanfile** can be found in [conan.io](https://conan.io/source/jansson/2.7/lasote/stable).

## Build packages

Download conan client from [Conan.io](https://conan.io) and run:

    $ python build.py

## Upload packages to server

    $ conan upload jansson/2.7@lasote/stable --all
    
## Reuse the packages

### Basic setup

    $ conan install jansson/2.7@lasote/stable
    
### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*
    
    [requires]
    jansson/2.7@lasote/stable

    [options]
    jansson:shared=true # false
    
    [generators]
    txt
    cmake

Complete the installation of requirements for your project running:</small></span>

    conan install . 

Project setup installs the library (and all his dependencies) and generates the files *conanbuildinfo.txt* and *conanbuildinfo.cmake* with all the paths and variables that you need to link with your dependencies.

