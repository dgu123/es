Installation
============

ES is built using [CMake](http://www.cmake.org/).  To keep the source tree
clean, it is a good idea to build it in a separate directory:

 *  mkdir build; cd build
 *  cmake ..
 *  make
 *  sudo make install

This will install it to /usr/local.  Changing this is easiest using `ccmake`,
or one of the graphical user interfaces for CMake.  To build project files
for IDEs, please refer to the CMake documentation.


Running the unit tests
----------------------

To run the unit tests, you need to have the
[Boost Unit Test framework](http://boost.org/) installed.

 * cmake .. -DBUILD_UNITTEST=1
 * make
 * cd unit_tests
 * ./unit_tests


Generating documentation
------------------------

Documentation can be autogenerated using [Doxygen](http://www.doxygen.org/).

 * cmake .. -DBUILD_DOCUMENTATION=1
 * make doc

The documentation ends up in the doc directory.

