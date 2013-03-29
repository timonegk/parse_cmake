parse\_cmake
===================

Python module for parsing CMake files.

Installing
----------

    python setup.py install

or

    sudo pip install parse_cmake

Usage
-----

The API can be used as follows:

    >>> import parse_cmake.parsing as cmp
    >>> cmakelists_contents = 'FIND_PACKAGE(ITK REQUIRED)  # Hello, CMake!'
    >>> cmp.parse(cmakelists_contents)
    File([Command([u'ITK', u'REQUIRED', u'# Hello, CMake!'])])

There is also a command line utility called cmake_pprint that pretty-prints
CMake files:

    $ cmake_pprint CMakeLists.txt
