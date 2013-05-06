kea5-maven
==========

Unofficial fork of Keyword Extraction Algorithm 5, adapted to the Maven standard directory layout.

See [official KEA website](http://www.nzdl.org/Kea/) and the original source so on the [Google code repository](http://code.google.com/p/kea-algorithm/).

Instructions
------------

Presumably you will be familiar with Maven usage if using this rather than the original distribution.

KEA has been split into two Maven modules:

 -  **kea-core** contains the core library
 -  **kea-demo** contains sample data and the **TestKea** demo class
 
*kea5-maven* has not yet been made available in a public Maven repository. To install for use in other Maven projects, run `mvn install` on the **kea-core** module (or the parent kea module). You may also wish to use some of the sample data from the **kea-demo** module to get KEA up and running in your project.

Demo
----

To run the demo class, **TestKea**, run `mvn test` on the **kea-demo** module. 

Alternatively, if you wish to specify arguments on the command line as described in section 2 of the [original KEA 5 Readme](Kea-5.0-Readme.txt), run 
`mvn exec:java -Dexec.mainClass=com.github.polarisation.kea.main.KEAModelBuilder -Dexec.args="[args]"`
where `[args]` should be replaced with command line arguments.

Notes
-----

This is based off the 5.0 distribution (not the 5.1 source). I did not want to use the 5.1 source because looking at a quick diff, I noticed 5.1 was slightly inferior in some ways (seems to be lacking some generics that are in 5.0). I may integrate the 5.1 changes later if I come across the bug it fixes.

Dependencies (Weka, Jena, and Snowball) have been updated to the latest versions (as of May 2013). This does not appear to cause any problems but should be reviewed if bugs do appear.

If you find any bugs and wish to contribute any fixes I will happy to add you as a collaborator.