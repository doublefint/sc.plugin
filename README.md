###Extendable source control plugin for InterSystems Caché Studio

By default export *.CLS, *.MAC, *.INT, *.INC, *.DFI into working directory as *.CLS.xml, *.MAC.xml, etc. in XML format 

Testing in Caché v2016, v2012.2

**Installation**:

* Import: [sc.plugin.PRJ.xml](https://github.com/doublefint/sc.plugin/blob/master/sc.plugin.PRJ.xml)
* Execute: `d ##class(sc.plugin).install()`
* _(Optional)_ Setup working directory: `w ##class(sc.options).workdir( "c:\YourWorkingDirectory\" )`
* _(Optional)_ Export classes: `d ##class(sc.classes).exportAll()`
* _(Optional)_ Export routines: `d ##class(sc.routines).exportAll()`
* _(Optional)_ Export DFI documents - **not working yet**: `d ##class(sc.dfi).exportAll()`
* Start Studio

**Extend**:

* Explore classes in [sc.ud](https://github.com/doublefint/sc.plugin/tree/master/sc/ud) package
* Create your own subclass of sc.classes, sc.routines, sc.dfi and override necessary methods
* Change settings: `d ##class(sc.options).handler("CLS","MyOwn.ClassesHandler")`
