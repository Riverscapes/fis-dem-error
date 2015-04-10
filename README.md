#Fuzzy Inference System (FIS) to Model DEM Error Repository

This repository has been created to function as a database for FIS that model DEM error. The FIS in this repository are shipped with the Geomorphic Change Detection (GCD) Software Version 6.X. To auto load the repository to your FIS Library in your GCD projects make sure that the **_Autoload ET-AL provided FIS library_** is checked. This option is accesed through the _Customize_ drop-down menu on the tool bar, and clicking the _Options_ button to bring up the _Options_ form. For further information about the _Options_ menu [click here.](http://gcd6help.joewheaton.org/gcd-command-reference/customize-menu/options) Once the **_Autoload ET-AL provided FIS library_** option is turned on, everytime the user is creating a FIS error surface they will be able to utilize the FIS to model DEM error. 

##Naming Convention of FIS Repository

The naming convention for each FIS has 3 main components. The first is an abbreviation of the surveying method that was used to collect the data to create the DEM, the second is the output the FIS is modeling (currently all FIS in repository are modeling DEM Error aka Z error), and the input variables used in each FIS. In addition their are 3 optional components, organization FIS was developed for, linear units the FIS is developed in, and year FIS was developed. Each component of the naming mechanism is separated by an underscore _ . 

A list of the surveying methods refered to in the repository and the abbreviations used to refer to them in the naming convention are listed below:

* **TS** - Total Station
* **TLS** - Terrestrial Laser Scanner
* **GPS** - Global Positioning System Survey
* **ALS** - Airborne Laser Scanner
* **GreenALS** - Green Airborne Laser Scanner
* **MBES** - Multibeam Echo Sounder

The second component is the output the FIS is modeling. A list of the outputs referred to in the repository and the abbreviations used to refer to them in the naming convention is listed below:

* **ZError** - DEM error

The third component to the naming mechanism is the input variables that are used in the FIS. Each input variable is then seperated by an underscore. A list of the input variables influencing DEM error that are refered to in the repository are listed below:

* **PD** - Point Density
* **3DQ** - 3D Point Quality
* **PQ** - Point Quality
* **SR** - Surface Roughness
* **SLP** - Slope
--* deg for slope in degrees
--* pct for slope in percent rise
* **IntErr** - Interpolation Error
* **Veg** - Vegetation
* **WD** - Wet Dry

The optional component of organization FIS was developed for precedes the FIS. A list of the organizations referred to in the repository and the abbreviations used to refer to them in the naming convention is listed below:

* **CHaMP** - Columbia River Habitat Monitoring Program

The optional component of linear unit and year developed trail the other naming components. **Unless specified with a final trailing underscore and different linear unit, like _Feet. Then the FIS is in meters.**

For example the FIS named **TS_ZError_PD_SLdeg** is an FIS used to model DEM error in a DEM created from data collected by a total station the inputs to the FIS are point density and slope degrees.

The FIS named **CHaMP_TS_ZError_PD_SLPdeg_SR_3DQ_IntErr** was created for the Columbia River Habitat Monitoring Program used to model DEM error in a DEM created from data collected by a total station the inputs to the FIS are point density, slope degrees, surface roughness, 3D point quality, and interpolation error.

##Creating Error Surface Using FIS

For more a tutorial for how to utilize an FIS to create an error surface within GCD, [follow this link].(http://gcd6help.joewheaton.org/tutorials--how-to/vii-fuzzy-inference-systems-in-gcd)

##Building FIS and Contributing to Repo

If you are interested in building your own FIS their is a [tutorial here](http://gcd6help.joewheaton.org/tutorials--how-to/viii-building-your-own-fis) for how to use Matlab's Fuzzy Logic Toolbox as well as helpful links, literature, and other information. If you would like to contribute a FIS to this repository please contact James Hensleigh (James.Hensleigh@usu.edu).
