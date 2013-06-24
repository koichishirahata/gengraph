#gengraph

[Koichi Shirahata](http://matsu-www.is.titech.ac.jp/~koichi-s/>) modified graph500(http://www.graph500.org/) reference implementation(Version 2.1.4, http://www.graph500.org/referencecode) for generating kronecker graphs into files, for measuring or debugging graph application with various graph sizes. Currently, graph500.c has been mogified for outputting an edge list of a kronecker graph into a text/binary file.

##Installation and Setup

    $ cd graph500-2.1.4  
    $ make

##Run the generator

To generate an edge list, just run one of below executables.

    -[seq|omp|...]-csr/{executable} [OPTION]

options:
    
    -o: output file name 
    -i: output binary file (in order of: src0 dst0 src1 dst1 ...)
        if not specified, output text file (default)

example:

    ./seq-csr/sec-csr -s 14 -o s14.edge

**NOTE: if you do not use "-o" option, do not output and exit.**

Now you can use the edge list (e.g. s14.edge) for your graph applications.

##Copyright
* Copyright (C) 2013 [Koichi Shirahata](http://matsu-www.is.titech.ac.jp/~koichi-s/>) All Rights Reserved.

