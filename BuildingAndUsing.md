## Building ##

The current version of Molotov features no [Makefile](http://en.wikipedia.org/wiki/Make_(software)#Makefile_structure), existing entirely as a single C++ source file. Fortunately, the dependencies are sparse and supported on multiple platforms.

The dependencies for building the tool are GNU GCC, libstdc++, and the [Armadillo Linear Algebra library](http://arma.sourceforge.net/), of required versions not yet tested. When in doubt, use the latest versions of GCC, libstdc++, and Armadillo available for your platform. Since this step and all documentation that follows should be performed via the command line in a POSIX-compliant environment, Windows users may want to consider [MinGW](http://www.mingw.org/) or [Cygwin](http://www.cygwin.com/) for building and deployment.

Once your environment has these dependencies in place, building is as easy as issuing the command:
```
  g++ -o molotov ml-reimplementation.cpp
```

Once built, you should have a working executable named "molotov" in the directory used to invoke this command. This will be used for the instructions that follow.


## Executing ##

To invoke the tool, simply execute it according to the input parameters as defined above:
```
  molotov <sequence file> <background file> <threshold file> <matrix lib> [-quiet] [-filter] [-reverse]
```

### Additional Information ###
  * [Input parameters](Inputs.md)
  * [Understanding the output](Outputs.md)