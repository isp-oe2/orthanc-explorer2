# Orthanc Explorer 2


## Build instructions
### Dependencies
* An instance of Orthanc ready to run
* cmake
* g++ and make or Visual Studio for Windows

### Installation

#### Building the shared library file
##### Mac OS X / Linux:


	mkdir build
	cd build
	cmake ..
	
##### Windows:

	mkdir build
	cd build
For a 32 bit version:


	cmake ..
For a 64 bit version:


	cmake -G "Visual Studio XX Win64" ..
	
Replace XX by your version of Visual Studio (e.g. : 15) 


##### Import the plugin
Specify the .so / .dylib / .dll shared library's path in the Orthanc's [configuration file](http://book.orthanc-server.com/users/configuration.html#configuration).

	{
  	"Name" : "MyOrthanc",
  	[...]
  	"Plugins" : [
    	"/home/user/OrthancDicomWeb/Build/libOrthancDicomWeb.so"
  	]
	}
		
### Running the web interface
Once the plugin is installed, you can restart Orthanc

You can access the web interface by going to the URL:

	http://localhost:8042/OE2
	
By default, you can connect as superuser with username *root* and passwoord *root*
