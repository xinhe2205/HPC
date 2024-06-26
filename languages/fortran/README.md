1.  [HPC User Wiki](index.html)
2.  [NREL HPC User Community
    Wiki](NREL-HPC-User-Community-Wiki_15171667.html)
3.  [Tips and Tricks](Tips-and-Tricks_18593769.html)
4.  [Fortran 90](Fortran90/f90.md)

 HPC User Wiki : Fortran Programs
=================================

Created by Southerland, Jennifer, last modified on 2018-01-23

Compiling and Running Fortran Programs on the Eagle System
==============================================================

Follow these instructions to compile and run your Fortran program on
Eagle.

Create Program
--------------

Using a text editor such as nano, vi or emacs, create a file called
hello.F90.

If you don't already know how to use a text editor, we suggest you learn
to use nano. To create the file named hello.F90, enter the following
command on the login node on Eagle:

    $ nano hello.F90

This will start the nano program, which will allow you to type text into
the file. Commands to tell nano what to do are located at the bottom of
your screen. The ^ symbol means to hold the Control key while you type
the letter, so ^o (pronounced "control-o") is entered by holding the
control key and the o key at the same time.

Enter the following text, being careful to include the spaces and
symbols as shown:

    program hello
    write(6,*)'hello, world'
    stop
    end program hello

Save this file by entering ^o. Exit nano by entering ^x.

Compile Program
---------------

To convert your program from a human-readable language like Fortran
(which is used in the example above) to the language used inside the
computer, a program called a "compiler" is used. Eagle has several
different compilers for each commonly used language. For this example,
we will use the compilers that are developed by Intel. The command used
to run the Intel Fortran compiler is "ifort". To run it on the file you
just created, type

    $ ifort -o hello hello.F90

The -o hello part of the command tells the compiler to store its output
in a file called hello. This file contains the program that will execute
on the computer.

Execute this program with the following command:

    $ ./hello

Document generated by Confluence on 2019-04-03 10:15

[Atlassian](http://www.atlassian.com/)
