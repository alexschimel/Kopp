![](https://github.com/alexschimel/Kopp/blob/04f0991168e0554acd2d13a867316a1b93ed5730/Kopp_resources/icon_400.png)

# *Kopp* 

Tracking Multibeam raw data parameter changes.

[![](https://github.com/alexschimel/Kopp/blob/04f0991168e0554acd2d13a867316a1b93ed5730/Kopp_resources/download.png)](https://github.com/alexschimel/Kopp/releases/download/v1.0.0/Kopp_v100_setup.exe)

## Description

*Kopp* (Norwegian Bokmål for "cup") is a free and open-source app to list all changes in parameters in a list of raw data files acquired by multibeam echosounders. Its main purpose is to serve as a simple tool to check for intempestive settings changes that affect the quality of backscatter mosaics. *Kopp* uses the [CoFFee multibeam data processing toolbox](https://github.com/alexschimel/CoFFee) (hence the name). It is coded in [MATLAB](https://www.mathworks.com/products/matlab.html), but is also available as a standalone application that does not require a MATLAB licence (see the Dependencies and Installing sections).

*Kopp* is still at an early stage of development so it has fewer features and more bugs than you would want. Please be patient. For a starter, its main current limitations are that it only works with Kongsberg EM Series .all files for now. Contrary to other CoFFee-based apps, *Kopp* does not save converted data on the hard-drive, but converts on the fly, extract the information necessary, and delete the converted data, so there are no limitations in number of files loaded at a time.

## Getting Started

### Dependencies

* For the source code:
  * [MATLAB](https://www.mathworks.com/products/matlab.html). The code was developed with version R2020b, but it may work on earlier/later versions.
  * Some [MATLAB toolboxes](https://www.mathworks.com/products.html):
    * TO DO...
  * [The *CoFFee* toolbox](https://github.com/alexschimel/CoFFee)
* For the compiled executable: [MATLAB Runtime v9.9](https://www.mathworks.com/products/compiler/matlab-runtime.html).
  * Note: if you install the app using the binary installer, the setup wizard will automatically detect whether you have the correct version of MATLAB Runtime installed and, if not, allow you to download and install it then.

### Installing

* For the source code: 
  * Clone or download this repository, as well as the repository of [*CoFFee*](https://github.com/alexschimel/CoFFee), onto your machine.
* For the compiled executable: 
  * Preferably, [download the binary installer from the releases page](https://github.com/alexschimel/Kopp/releases), execute the installer, and follow the instructions of the setup wizard. The setup wizard will check if you have the appropriate version of MATLAB Runtime installed and, if not, let you download and install it. Note that the setup wizard requires an internet connection.
  * Alternatively, you can simply [download the binary executable and accompanying files from the releases page](https://github.com/alexschimel/Kopp/releases) and double-click the .exe file to run the application without installing it. Note that you still need to have the appropriate version of MATLAB Runtime installed.

### Executing program

* For the source code: Start MATLAB, navigate to the root directory of the *Kopp* code, and type `Kopp` in the Command Window.
  * Note: The first time you run *Kopp* from the source code, you will be prompted to provide the location of a folder containing the *CoFFee* toolbox. *Kopp* will check if the version of that toolbox is the one with which the app was built. If the version of *CoFFee* is not the one expected, you will receive a warning letting you know you might experience issues, and recommending you download (or check out) the appropriate version.
* For the compiled executable: Execute the installed program.
  * Note: The first time you run *Kopp* after installation, it might take a while for the app to appear. Be patient. It will be faster the next times.

Note: At start-up, *Kopp* creates a `Kopp` user folder (normally, C:\Users\USERNAME\Documents\Kopp). This folder contains a configuration file for the app, and is the default folder for any exports from the app. This folder or any of its contents can be deleted safely (although if you delete the configuration file, this will reset the app configuration).

## Help

*Kopp* is a tiny tool. here's all the help you need:
1. Click the 'Open' button. Select a folder with raw data files. 
2. *Kopp* will list all raw data files supported found in this folder and sub-folders, and for each in turn it will parse the file and extract the parameters in it.
3. The parameter changes are then sorted chronologically and printed on the accompanying console.
4. When you close the software, the contents of the console are saved as a log file to be found in the `Kopp` user folder (normally, C:\Users\USERNAME\Documents\Kopp).

If you want to receive notifications of future releases (recommended), you may create a github account, and on this repository click on 'Watch', then 'Custom', and choose 'Releases'. Verify in your GitHub settings that you are set to receive 'Watching' notifications.

For more information, contact the authors.

## Authors

* Alexandre Schimel([The Geological Survey of Norway](https://www.ngu.no), alexandre.schimel@ngu.no)
* Margaret Dolan, Shyam Shand, Terje Thorsnes, Lilja Rún Bjarnadóttir (The Geological Survey of Norway)

## Version History

[See the releases page](https://github.com/alexschimel/Kopp/releases)

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

## See Also

All apps based on CoFFee:
* *Grounds*: https://github.com/alexschimel/Grounds
* *Espresso* (private)
* *Iskaffe*: https://github.com/alexschimel/Iskaffe
* *Kopp*: https://github.com/alexschimel/Kopp

## Acknowledgments

None to date.

## References 

None to date.

## For developers

[See the section 'For Developers' on the *CoFFee* page](https://github.com/alexschimel/CoFFee)
