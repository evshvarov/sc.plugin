###sc.plugin

Extendable s[ource] c[ontrol] plugin for InterSystems Caché Studio

Export/Import *.cls, *.mac, *.int, *.inc into filesystem

For example, `test.test.CLS` will be exported as `workdir\test\test.CLS.xml`

Testing in Ensemble v.2014.1, Caché v.2015.2 - 2016.1 on Windows 7x64

**Installation**:

* **Backup** first !!!
* Import: [sc.plugin.PRJ.xml](https://github.com/doublefint/sc.plugin/blob/master/sc.plugin.PRJ.xml)
* Execute: `d ##class(sc.plugin).install()`
* _(Optional)_ Setup working directory: `w ##class(sc.options).workdir( "c:\YourWorkingDirectory\" )`
* _(Optional)_ Export classes: `d ##class(sc.classes).exportAll()`
* _(Optional)_ Export routines: `d ##class(sc.routines).exportAll()`
* _(Optional)_ Export DFI documents : `d ##class(sc.dfi).exportAll()`
* Start Studio

**Extend**:

* See examples in [sc.ud](https://github.com/doublefint/sc.plugin/tree/master/sc/ud) or [sc.plain - (udl)](https://github.com/doublefint/sc.plugin/tree/master/sc/plain) packages
* Create your own subclass of sc.classes, sc.routines, sc.dfi and override necessary methods

###sc.plain.plugin

Export/Import code in *UDL* format ( plain - as you see in Studio ). Require Caché v.2014.1 or greater.
For example, `test.test.CLS` will be exported as `workdir\test\test.CLS`

* Import: [sc.plain.plugin.PRJ.xml](https://github.com/doublefint/sc.plugin/blob/master/sc.plain.plugin.PRJ.xml)
* Execute: `d ##class(sc.plain.plugin).install()`
* Reopen Studio

###sc.ud.plugin

Export/Import code into subfolders: 
```
 *.cls -> workdir\_CLS\*.xml
 *.mac -> WORKDIR\_RTN\*.xml
 *.int -> WORKDIR\_INT\*.xml
 *.inc -> WORKDIR\_INC\*.xml
```
* Import: [sc.ud.plugin.PRJ.xml](https://github.com/doublefint/sc.plugin/blob/master/sc.ud.plugin.PRJ.xml)
* Execute: `d ##class(sc.ud.plugin).install()`
* Reopen Studio
 
