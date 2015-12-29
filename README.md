###Extendable source control plugin for InterSystems Caché Studio

By default export *.CLS, *.MAC, *.INT, *.INC, *.DFI into working directory as *.CLS.xml, *.MAC.xml, etc. in XML format 

Testing in Caché v2016, v2012.2

**Installation**:

* Import: [sc.plugin.PRJ.xml](https://github.com/doublefint/sc.plugin/blob/master/sc.plugin.PRJ.xml)
* Execute: `d ##class(sc.plugin).install()`
* _(Optional)_ Setup working directory: `w ##class(sc.options).workdir( "c:\YourWorkingDirectory\" )`
* _(Optional)_ Export classes: `d ##class(sc.classes).exportAll()`
* _(Optional)_ Export routines: `d ##class(sc.routines).exportAll()`
* _(Optional)_ Export DFI documents : `d ##class(sc.dfi).exportAll()`
* Start Studio

**Extend**:

* Explore classes in [sc.ud](https://github.com/doublefint/sc.plugin/tree/master/sc/ud) package
* Create your own subclass of sc.classes, sc.routines, sc.dfi and override necessary methods

**sc.plain.plugin**

Export/Import code in UDL format ( as you see in Studio ) 
* Import: [sc.plugin.ud.PRJ.xml](https://github.com/doublefint/sc.plugin/blob/master/sc.plugin.ud.PRJ.xml)
* Execute: `d ##class(sc.plain.plugin).install()`
* Reopen Studio

**sc.ud.plugin**

Export/Import code into subfolders: 

 .CLS -> WORKDIR\\_CLS\\*.xml
 
 .MAC -> WORKDIR\\_RTN\\*.xml
 
 .INT -> WORKDIR\\_INT\\*.xml
 
 .INC -> WORKDIR\\_INC\\*.xml
 
* Import: [sc.plugin.ud.PRJ.xml](https://github.com/doublefint/sc.plugin/blob/master/sc.plugin.ud.PRJ.xml)
* Execute: `d ##class(sc.ud.plugin).install()`
* Reopen Studio
 
