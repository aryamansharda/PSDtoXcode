# Welcome to PSDtoXcode!

### Disclaimer

If you're a recruiter or another engineer looking at this code, cut me some slack. I wrote this program when I was 15. 


## File Overview
- PSDtoXcode.jsx
	> Source code for the project
- PSDtoXcode Demo.psd
	>An example of how the layers should be titled in your source Photoshop design 
- PSDtoXcode.jsxbin
	>Executable version of the script 

## Project Overview
Please read the Instructions.rtf file before proceeding. 

The implementation is fairly straightforward. The program will first ask you for the .storyboard file you want to add a new View Controller too. Once this is done, the program will search through the XML that defines the .storyboard file to find a good location to insert this new View Controller.

Then, the application will rasterize and ungroup all the layers in the Photoshop document. A necessary step in order to export the assets. 

Additionally, the program will reverse the order of the layers so that way when the elements are added to Xcode, they are presented with the same view hierarchy as you originally intended; the first Photoshop layer is the one at the top of the view hierarchy where as in Xcode the last element added is at the top of view hierarchy - reversing the order of the layer fixes this issue.

Then, the program will check if the resolution of the Photoshop design is high enough to export @3X resolution graphics. If it is, the program will include them, otherwise the program will skip straight to exporting @2x and @1x graphics. The program will iterate through every later in your project and will export the asset itself and will append to the .storyboard file the XML to recreate it in Xcode. 

At the end of the execution, you will be prompted to return to Xcode. All you need to do now is add the newly exported assets into your Xcode project and you'll have a pixel perfect recreation of your original design in seconds. 
