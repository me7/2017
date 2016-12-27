## installation

will failed
mongod.exe - System Error
The program can't start because api-ms-win-crt-runtime-l1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem. 

see http://stackoverflow.com/questions/33265663/api-ms-win-crt-runtime-l1-1-0-dll-is-missing-when-opening-microsoft-office-file to download vc_redist
you cannot install version 3 unless you use windows 7 SP1
* install mongodb compass to working with database (need register mongodb-compass-1.5.0-win32-x64.exe) **work with version >=3.2**

use this file http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.0.0-rc5.zip (date 2015-01-15 02:10:01)
* download version 2 from https://www.mongodb.org/dl/win32/x86_64-2008plus-ssl
  * ~~the last version I can use with window 7 64bit is mongodb-win32-x86_64-2.7.8-signed.msi~~ not work with robomongo
  * use mongodb-win32-x86_64-2.4.13.zip
* install in d:\mongodb
* it's will default database at D:\data\db
* some usefull tools https://docs.mongodb.com/ecosystem/tools/administration-interfaces/
  * https://robomongo.org/
  * 


## mongo shell sample code
* https://docs.mongodb.com/manual/reference/mongo-shell/
* `show dbs`
* `use hana` will create hana database if not exist
* `db.products.insert({"prod":"104536-x-1","wo":"16KCE55006","rc":"2/10"})` create record in products collection, respond with WriteResult({ "nInserted" : 1 })
* `db.products.find()` will show all records