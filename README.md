# CytoSPADE Cytoscape Plugin for SPADE

The CytoSPADE Cytoscape plugin provides a GUI for setting-up and interactively visualizing the results of SPADE analyses. It is designed to work with the SPADE R-package. Please see the documentation for that project on how to use the plugin (and SPADE in general). This README and related documentation are primarily targeted at developers working on the plugin itself.

## Prerequisites
1. [Netbeans and the Java 1.6 SDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
1. [git](http://git-scm.com)
1. Latest version of [Cytoscape](http://www.cytoscape.org/download.html)

## Setup and Build Process
The CytoSPADE repository is itself a Netbeans project and can be opened directly with *Open a Project*. Note that you will likely get complaints about unresolved library paths. You can resolve these paths by setting the path to your Cytoscape installation via an "IDE Variable", specificallly via *Tools -> Variables* add a variable `CYTOSCAPE_PATH` that points to your top level Cytoscape installation directory. The project library dependencies are set relative to this variable and should be resolved at this point.

After you build the project (the hammer in the toolbar), there will be two jars created in the `dist/` directory, `CytoSPADE.jar` and `CytoSPADE.dist.jsr`. The latter has all the non-Cytoscape dependencies compiled in, and is the file you should copy to the CytoScape plugins folder as `CytoSPADE.jar`.

## Tips and Resources
* [Cytoscape plugin developer's cookbook](http://cytoscape.wodaklab.org/wiki/plugin_developer_tutorial)
* [Cytoscape 2.8.1 API](http://chianti.ucsd.edu/Cyto-2_8_1/javadoc/overview-summary.html)
