#Fuzzy Inference System (FIS) to Model DEM Error Repository

This repository has been created to function as a database for FIS that model DEM error. The FIS in this repository are shipped with the Geomorphic Change Detection (GCD) Software Version 6.X. To auto load the repository to your FIS Library in your GCD projects make sure that the **_Autoload ET-AL provided FIS library_** is checked. This option is accesed through the _Customize_ drop-down menu on the tool bar, and clicking the _Options_ button to bring up the _Options_ form. For further information about the _Options_ menu [click here.](http://gcd6help.joewheaton.org/gcd-command-reference/customize-menu/options) Once the **_Autoload ET-AL provided FIS library_** option is turned on, everytime the user is creating a FIS error surface they will be able to utilize the FIS to model DEM error. 

##Naming Convention of FIS Repository

Each FIS has 2 main components to how it is named the first is an abbreviation of the surveying method that was used to collect the data to create the DEM. A list of the surveying methods refered to in the repository are listed below:

* **TS** - Total Station
* **TLS** - Terrestrial Laser Scanner
* **GPS** - Global Positioning System Survey
* **ALS** - Airborne Laser Scanner
* **GreenALS** - Green Airborne Laser Scanner
* **MBES** - Multibeam Echo Sounder

The survey type represented by the abbreviations above is separated from the second component of the naming mechanism by an underscore _. The other component to the naming mechanism is the input variables that are used in the FIS. Each input variable is then seperated by an underscore. A list of the input variables influencing DEM error that are refered to in the repository are listed below:

**It seems that some of the FIS have Zerror between the survey type and input variables but some don't, should I add this to all of them?**

* **PD** - Point Density
* **SA** - ? Slope Analysis - This is used in the most recent FIS created for CHaMP **I propose this is changed to SL for slope that is appended by deg or pct for degrees or percent** as it is in the other FIS
* **3DQ** - 3D Point Quality
* **PQ** - Point Quality
* **SR** - Surface Roughness
* **IntErr** - Interpolation Error
* **Veg** - Vegetation
* **WD** - ?

For example the FIS in the repository that is named **TS_PD_SLdeg** is an FIS used to model uncertainty in a DEM created from data collected by a total station that uses point density and slope degrees as its inputs.

**Unless specified with a final trailing underscore and different linear unit, like _Feet. Then the FIS is in meters.**