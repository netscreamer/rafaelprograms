# rafaelprograms
Wt C++ Setup Files To Use With Komodo Edit

These are the setup files for using the Wt C++ library for developing web and console applications.

My version of Wt is 3.3.5 and uses boost 1.57. All binaries are included with this setup. You will need to download Komodo Edit to use the compiler and CMake in this setup. Here is what else you will need:

CMake
MinGW-w64

Once you have CMake, MinGW, and Komodo Edit, you will have to make some changes to make this work. I have included the Komodo Edit command files and the batch files so that you can follow the YouTube videos.

I have included all the "Build" and "Projects" Komodo Edit command files but they will have to be modified to fit your setup. Here is what you will need to do:
In "Komodo\Komodo Commands\Build" you have to edit the "Clean_Project.komodotool" file. You have to change the "value" to whatever path you use for the batch files. For example: "C:\\Users\\<Your-Windows-Username-Or-Account>\\Komodo\\Tools\\CleanBuild.bat\" or wherever you decide to put the batch files. You would do the same thing for all these files:

Clean_Project.komodotool
Compile.komodotool
Debug.komodotool
Run.komodotool
Run_CMake.komodotool (this is different from the rest)
Witty_Server.komodotool
 
 Run_CMake.komodotool has a value of: "cmake .. -G \ "MinGW Makefiles\" -DCMAKE_BUILD_TYPE=Debug". You can change this value for CMake from -DCMAKE_BUILD_TYPE=DEBUG to "None", "Release", "RelWithDebInfo" or "MinSizeRel". 
 
 These point to folders in the Komodo folder in the repository. You will have to edit these. For example in "C++_Project.komodotool": "xcopy \"C:\\Users\\Developer\\My Projects\\Komodo\\CPP\" /e" or wherever you decide to put this folder. These are nothing more than batch commands.
 
 C++_Project.komodotool
 SOCI Project.komodotool
 Wt Data Project.komodotool
 Wt Project Project.komodotool
 
 The easiest thing for you to do is import the folders from Komodo Edit and then edit these values by right clicking on the commands by right-clicking on the command and editing the "Command:" path wherever the batch or folder resides in you setup.
 
Bugs can be reported here http://redmine.webtoolkit.eu/projects/wt/issues/new

Demos, examples

The homepage, itself a Wt application, contains also various examples.
