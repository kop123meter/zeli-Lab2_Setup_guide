# zeli-Lab2_Setup_guide
LAB 2A in Mac OS

1.Pre-Lab
In Mac OS, We first touch a hello.txt and then edit the hello.txt by vim.At last, we can see the document through cat.
![image](https://github.com/kop123meter/zeli-Lab2_Setup_guide/blob/main/Pre-lab2.png)

2.Setting Lab 2 A
First, Install Homebrew

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Second, Export Homebrew to environment path:

(1)cd ~(open ~directory)
(2)If we don’t have .zshrc document, we need to creat in 
(3)open or vim .zshrc to edit the file
(4)add two exports to the file
     export PATH=/opt/homebrew/bin:$PATH
     export PATH=/opt/homebrew/sbin:$PATH
(5)source .zhsrc
(6)brew -v to check.If the HomeBrew is successfully export to environment, we will look the version of HomeBrew.
![image]([https://github.com/kop123meter/zeli-Lab2_Setup_guide/blob/main/Pre-lab2.png](https://github.com/kop123meter/zeli-Lab2_Setup_guide/blob/main/homebrew_install.png))


Third, From the above figure, we need to install the wget by 
                                      brew install wget

Fourth, install the toolchain:


brew install cmake 
brew tap ArmMbed/homebrew-formulae 
brew install arm-none-eabi-gcc




Then, set environment in VsCode 
By following the guidence in document Getting start with Raspberry 9.1:

(1)After starting Visual Studio Code you then need to install the CMake Tools extension. Click on the Extensions icon in the left-hand toolbar (or type Cmd + Shift + X), and search for "CMake Tools" and click on the entry in the list, and then click
on the install button. 
(2)We now need to set the PICO_SDK_PATH environment variable. Navigate to the pico-examples directory and create a .vscode directory and add a file called settings.json to tell CMake Tools to location of the SDK. Additionally point Visual Studio at the CMake Tools extension.


{   "cmake.environment": 
{   "PICO_SDK_PATH":"../../pico-sdk"   }, 
}

(3)Then go to the File menu and click on "Add Folder to Workspace…" and navigate to pico-examples repo and click "Okay". The project will load and you’ll (probably) be prompted to choose a compiler, Select "GCC for arm-noneeabi" 


(4)clicke the bulid botton  we can see:



In the end, we need to Drag and drop hello_usb.uf2 onto the Mass Storage Device from the
pico-examples/build/hello_world/usb/

Then, open the terminal and link to the screen . 

we can see that




     
