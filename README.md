###Extendable source control plugin for InterSystems Caché Studio

By default export *.CLS, *.MAC, *.INT, *.INC, *.DFI into working directory as *.CLS.xml, ..., etc. in XML format 

Testing in Caché v2016, v2012.2

**Installation**:

* Import: **sc.plugin.PRJ.xml**
* Execute: d ##class(sc.plugin).install()
* (Optional) Setup working directory: w ##class(sc.options).workdir( "c:\YourWorkingDirectory\" )
* (Optional) Export classes: d ##class(sc.classes).exportAll()
* (Optional) Export routines: d ##class(sc.routines).exportAll()
* (Optional) Export DFI documents - **not working yet**: d ##class(sc.dfi).exportAll()
* Start Studio

**Extend**:

* Import **sc.plugin.ud.PRJ.xml**
* Explore classes in **sc.ud** package
* Create your own subclass of sc.classes, sc.routines, sc.dfi and override necessary methods
* Change settings: d ##class(sc.options).handler("CLS","MyOwn.ClassesHandler")




