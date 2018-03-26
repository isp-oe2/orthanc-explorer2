# Orthanc Explorer 2


## Build instructions
### Dependencies
* An instance of Orthanc ready to run
* npm
* cmake
* g++ and make for Linux/Mac OS X 
* Visual Studio 15 2017 for Windows

### Installation

#### Building the shared library file
##### Mac OS X:

	cd scripts
	chmod u+x
	./OSX_lib_generation.sh
	
##### Linux:

	cd scripts
	chmod u+x
	./LINUX_lib_generation.sh
	
##### Windows 64 bits:

	cd scripts
	Win64_lib_generation.cmd
	
If you do not have Visual Studio 15 2017, change the name of the version in the script Win64_lib_generation.cmd


#### Import the plugin
##### Check the library
The library should be  generated in the "binaries" folder

##### Link the plugin to Orthanc
Specify the .so / .dylib / .dll shared library's path in the Orthanc's [configuration file](http://book.orthanc-server.com/users/configuration.html#configuration).

	{
  	"Name" : "MyOrthanc",
  	[...]
  	"Plugins" : [
    	"/home/user/orthanc-explorer2/build/libOE2.so"
  	]
	}
		
### Running the web interface
Once the plugin is installed, you can restart Orthanc

You can access the web interface by going to the URL:

	http://localhost:8042/OE2
	
By default, you can connect as superuser with username *root* and passwoord *root*
