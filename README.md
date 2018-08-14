File Manager (Storage)
======================

A simple Android File Manager (Storage) to create, read, delete, append, encrypt files and more, on internal or external storage spaces.

### Options
* [Easy define Internal or External storage](#initialize)
* [Create directory](#create-directory)
* [Create file](#create-file)
* [Read file content](#read-file)
* [Append content to file](#append-content-to-file)
* [Copy](#copy)
* [Move](#move)
* [Delete directory](#delete-directory)
* [Delete file](#delete-file)
* [Get files](#get-files)
* [More options](#more)
* [Encrypt the file content](#security-configuration)


### Check Directory of File ...

* Is directory exists
	``` java
	boolean dirExists = storage.isDirectoryExists(path);
	```

* Is file exists
	``` java
	boolean fileExists = storage.isFileExist(path);
	```


### Security configuration
You can write and read files while the content is **encrypted**. It means, that no one can read the data of your files from external or internal storage.

You will continue using the same api as before. The only thing you need to do is to configure the Simple Storage library before the you want to create/read encrypted data.

### Security on Java
// set encryption
String IVX = "abcdefghijklmnop"; // 16 lenght - not secret
String SECRET_KEY = "secret1234567890"; // 16 lenght - secret
byte[] SALT = "0000111100001111".getBytes(); // random 16 bytes array

