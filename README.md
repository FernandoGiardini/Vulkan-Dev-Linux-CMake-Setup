<H1>Setting up a Vulkan developer enviroment using CMake in Linux [Ubuntu]!</H1>

<H3>Repository meant to help begginers set up the coding enviroment faster and with ease.</H3>

What we'll be using:

<li>Compiler that supports C++17 (GCC 7+ or Clang 5+)
<li>CMake 
  
```
sudo apt install cmake
```
<li>Vulkan packages

```
sudo apt install vulkan-tools
sudo apt install libvulkan-dev
sudo apt install vulkan-validationlayers-dev spirv-tools
```
>To check proper installation and hardware compatibility, run:

```
vulkaninfo > vulcaninfo.txt
vkcube
```

"vulakninfo > vuncalinfo.txt" will give all the information about the compatibility in a generated .txt file.
"vkcube" will generate a window with a spinning cube.

If this worked fine your machine is compatible with Vulkan!

Now for the multiplatform window creation and management, we'll use GLFW.

```
sudo apt install libglfw3-dev
```
And for helping with linear algebra operations later on we'll use GLM.

```
sudo apt install libglm-dev
```
<H3>Now for the shader compiler, we'll use glslc.</H3>

<li>Donwload the tgz file that is compatible with your C++ compiler in https://github.com/google/shaderc/blob/main/downloads.md ;
<li>Unzip the downloaded file and open the directory;
<li>Enter the 'bin' directory;
<li>Copy the 'glslc' file to your '/usr/local/bin' (Might have to sudo);

Now if you run:

```
glslc
```
you'll get an error message saying  'glslc: error: no input files'.
This indicates that glslc is installed.

Now all theres left is to use the already made CMakeLists.txt file.
(I'm assuming that you already cloned the repository)

Now for the final steps, create the build directory, move there, create the MakeFile using Cmake and you should see a black 'Vulkan Window' on your screen.

```
mkdir build
cd build
cmake ..
make
./vktest
```

<br> Congratulations, you are now oficcialy on the first step of the journey, Happy hacking! :p 🚀

