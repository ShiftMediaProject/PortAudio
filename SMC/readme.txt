
This is a small list of steps in order to build PortAudio into a msvc DLL and lib file.
Currently this project builds for 4 out of the 5 win32 APIs (DS/ASIO/WASAPI/WDMKS).

The project contains Release and Debug builds for static lib files (Debug/Release)
  as well as dynamic shared dll files (DebugDLL/ReleaseDLL).
Choose whichever project configuration meets your requirements.


*** Building without ASIO support ***

To build PortAudio without ASIO support ensure that you use the Visual Studio project configurations that are not suffixed with 'ASIO'.
These configurations will automatically build without ASIO support without any further input.


*** Building with ASIO support ***

To build PortAudio with ASIO support ensure that you use the Visual Studio project configurations that are suffixed with 'ASIO'.
In order to build with ASIO support you need to download the ASIO SDK from:
http://www.steinberg.net/en/company/developer.html

Once the SDK is downloaded extract the contents alongside the PortAudio folder.
Then rename the ASIO folder to 'ASIOSDK'.

The new project folder structure should look like:
PortAudio
   |--bindings
   |--build
   |--etc.
ASIOSDK
   |--asio
   |--common
   |--etc.

Once the ASIO SDK has been extracted then the project will build normally without any issue.


*** Building without ASIO support ***

To build PortAudio without ASIO support ensure that you use the Visual Studio project configurations that are suffixed with 'NoASIO'.
These configurations will automatically build without ASIO support without any further input.
