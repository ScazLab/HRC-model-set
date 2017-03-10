# HRC Model Set
_Model set for Human-Robot collaborative tasks_

## Introduction

The human-robot collaboration (HRC) model set is intended to ease the design of human-robot collaboration experiments.
It targets scenarios like the collaborative assembly of furniture, and consists of a combination of standard components and custom designs, that are:

 * A series of eight 3D printed brackets
 * Dowels
 * Plywood
 * Fasteners (Screws)

The model set aims at reducing the amount of work required to set up and reproduce HRC experiments.
It is designed to be modular, extendable, and easy to distribute. All the content of this repository is distributed under the [Creative Commons attribution-sharealike 4.0 international public license (CC-by-sa)](https://creativecommons.org/licenses/by-sa/4.0/legalcode).


## 3D Printed Brackets

The 3D Printed Brackets were designed with three main criteria in mind : re-use, replicability, and modularity.


The `.stl` files and the SolidWorks files can be found in the [`Bracket STL Files`](https://github.com/ScazLab/HRC-model-set/tree/master/Bracket%20STL%20Files) and [`Bracket SolidWorks Files`](https://github.com/ScazLab/HRC-model-set/tree/master/Bracket%20SolidWorks%20Files) sub-folders respectively.

## Hardware

Exclusive of the 3D printed brackets, all of the hardware of the HRC Model Set can be found online, at a hardware store, or craft supply. Below are the hardware components along with a link to where you can purchase them.

1. __Wooden Dowels__ In our experiments we used 1/2" (OD) dowels from [this]( https://www.amazon.com/gp/product/B00YDLVP9C/ref=oh_aui_search_detailpage?ie=UTF8&psc=1) assorted value pack. You can also purchase the dowels [here](https://www.amazon.com/Wooden-Dowel-Rods-12-Bag/dp/B00XQI3NJS/ref=sr_1_2?ie=UTF8&qid=1488559469&sr=8-2&keywords=1%2F2%22+craft+dowel) if you do not want an assortment of sizes.
2. __Plywood__ [These](https://www.amazon.com/gp/product/B00CQKYZPI/ref=oh_aui_search_detailpage?ie=UTF8&psc=1) 12" x 12" plywood sheets were then cut on a laser cutter to size. To build the console, larger sheets found [here](https://www.amazon.com/Baltic-Birch-Plywood-Scroll-Woodpeckers/dp/B01MQTWKBX/ref=sr_1_1_m?s=arts-crafts&ie=UTF8&qid=1488566139&sr=1-1&keywords=24%22x24%22%2Bcraft%2Bplywood&th=1) can be used.
3. __Screws__ #4 screws in 1/4" lengths can be found [here](https://www.amazon.com/gp/product/B01HAEX8C0/ref=oh_aui_search_detailpage?ie=UTF8&psc=1), and #4 screws in 1/2" lengths can be found [here](https://www.amazon.com/gp/product/B00OKIT234/ref=oh_aui_search_detailpage?ie=UTF8&psc=1). These screws are both Phillips head screws, however it is possible to find screws with different drive heads as well.

## Example designs

We present four prototypical objects built using different configurations of the hardware mentioned above.

Our designs range from the most simple, the Table configuration, to quite complex, the Console configuration.

Below are renderings of each design along with a bill of materials.

![Table](https://cloud.githubusercontent.com/assets/12373812/23683629/0b698e6c-0368-11e7-8cdd-c7b93e4e4a9a.jpg)

Hardware | Amount
-------- | --------
``Top``| 4
``Foot``| 4
``6" Dowel `` | 4
``6" x 8" Plywood`` | 1
`` #4 Screw .25"`` | 8
`` #4 Screw .50"`` | 8

![Chair](https://cloud.githubusercontent.com/assets/12373812/23683588/d4976b34-0367-11e7-8ffe-7fc8ab9b6dd6.jpg)

Hardware | Amount
-------- | --------
``Top``| 2
``Foot``| 4
``ChairL`` | 1
``ChairR`` | 1
``ChairBack``| 2
``6" Dowel `` | 6
``6.75" Dowel``| 1
``6" x 8" Plywood`` | 1
``6.75" x 2.5"`` | 1
`` #4 Screw .25"`` | 12
`` #4 Screw .50"`` | 14

![Shelf](https://cloud.githubusercontent.com/assets/12373812/23683615/f7b5769c-0367-11e7-9f4d-f1979abac6a7.jpg)

Hardware | Amount
-------- | --------
``Top``| 4
``Foot``| 4
``Shelf90`` | 4
``6" Dowel `` | 8
``6" x 8" Plywood`` | 2
`` #4 Screw .25"`` | 16
`` #4 Screw .50"`` | 16

![Console](https://cloud.githubusercontent.com/assets/12373812/23683601/e2a5c1bc-0367-11e7-9647-fbce437b5b30.jpg)

Hardware | Amount
-------- | --------
``Top``| 4
``Foot``| 8
``Shelf90`` | 12
``Shelf180`` | 4
``Top180`` | 4
``6" Dowel `` | 24
``6" x 8" Plywood`` | 6
``6" x 16" Plywood`` | 2
`` #4 Screw .25"`` | 48
`` #4 Screw .50"`` | 48


## CAD- 3D Modeling
With access to the SolidWorks files, making adjustments to fit plywood and dowels of various lengths or widths requires a few simple steps.

### Adding Plywood Thickness

![PlywoodThickness](https://cloud.githubusercontent.com/assets/12373812/23572174/50f8ab50-003b-11e7-9cb4-f687dbdad2df.PNG)

To change the width of the insert for a piece of plywood of a different size, the model has been separated with a plane to extrude from. In the image above “Plane 3” is referenced off the face of the inside wall of the insert. By modifying the extrude feature “Boss-Extrude3” with the dimension of your piece of plywood, you will now have an insert that is compatible with your experiment. The rest of the features will update accordingly.

### Changing Dowel Diameter

![DowelDiameter](https://cloud.githubusercontent.com/assets/12373812/23584150/2f4ee744-0126-11e7-896a-cab7d1c7ae53.PNG)

To account for a different diameter of dowel, find the _sketch_—in the above image it is “Sketch2” under “Boss-Extrude4”—that creates the cylindrical feature. Edit the sketch, and update the dimension of the diameter to the dowel size of your choice. While in this sketch, you can also determine the wall thickness of the feature by modifying the offset between the inner circle (your dowel) and the outer concentric curves (the walls). You can also modify the length of the two parallel flat sides to either create a larger or smaller surface for a robot with an electric gripper to hold onto.

### Changing Screw Size and Type

![ScrewSize](https://cloud.githubusercontent.com/assets/12373812/23584211/623c8ca4-0128-11e7-88cd-b997aac6dd68.PNG)

In order to change the screw size and type, you can modify the _CSK..._ feature. To create a screw hole from scratch, you add a feature to your family tree under the “Hole Wizard” tab where most of the standard features are found. Within the “Hole Wizard” dialogue box, you can change the screw to fit ANSI or metric types of standard screws. It is possible to dictate the type of countersink depending on what kind of screw you choose. The dialogue also allows you to determine exactly where the screws will be placed. This opens the possibilities of modifying an HRC experiment to account for different types of screw drivers.

### Inserting a Fiduciary Marker

![FiduciaryMarkers](https://cloud.githubusercontent.com/assets/4378663/23570411/0733191e-0032-11e7-8050-d8c79e5c967f.PNG)

Fiduciary markers can be a great asset to designing an HRC experiment because they can give a robot more agency by perception. To embed a fiduciary marker directly onto one of the brackets, you must first convert the fiduciary marker image into a `.dxf` or `.dwg` file. This can be achieved by pulling a marker image into a vector image software such as *Adobe Illustrator* and tracing the image to duplicate the outlines as a vector lines. You can then save the vector outlines as either of the accepted files.

To insert these files into your SolidWorks model, open your `.dwg` or `.dxf` file under `file > open`. You will be re-directed to the DWG/DXF wizard in which you can specify a series of import options like scale and origin of the image. You want to make sure to import the file as a 2D sketch in your part.

In order to create the embedded feature, you may have to re-trace your fiduciary marker sketch using the “Convert Entities” tool. Then, highlight the dark areas of the marker and use the “Extruded Cut” feature to cut into your bracket enough to be able to distinguish the marker, but not too far as to cut through the wall of the bracket.

### Cost Analysis

![CostAnalysis](https://cloud.githubusercontent.com/assets/12373812/23584326/40ebc246-012c-11e7-97c9-024668e0ac44.PNG)

To be able to estimate the cost of producing one of the brackets using other manufacturing methods or materials, you can use the “Costing” tool under the “Evaluate” tab. There, you can specify what material you will be manufacturing or fabricating the parts with, what process you will use, e.g. 3D printing or injection molding, how many brackets you plan to produce, and compare several methods.

## 3D Printing

Each bracket <!-- Add something about in the paper?--> was modeled in SolidWorks and then printed on a Dimension Elite FDM printer using ABS+ plastic. <!-- Insert settings -->

Below are some guidelines to use when printing out a file using some common 3D printers:

*Each print is of the “Top” bracket for comparison.*

### [MakerBot Replicator Gen. 5](https://www.makerbot.com/replicator/)

####10mm layer height
![10mm](https://cloud.githubusercontent.com/assets/12373812/23683332/701683da-0366-11e7-8ba1-3ac8efa29b85.PNG)

Using the above settings, the estimated print time is 2 hours and 12 minutes. The material usage is 15.11 grams.

Diameter specified in the SW File: .127 cm  
Diameter of actual printed bracket: .123 cm

Distance of plywood insert in the SW File: .318 cm 	
Distance of plywood insert of actual printed bracket: .302 cm

![10print](https://cloud.githubusercontent.com/assets/12373812/23770608/afaff860-04e1-11e7-89b4-5f637e37c9e0.JPG)

####20mm layer height
![20mm](https://cloud.githubusercontent.com/assets/12373812/23683341/7c1b8fb8-0366-11e7-82f6-870d0b399e3f.PNG)

Using the above settings, the estimated print time is 1hour and 13 minutes. The material usage is 13.6 grams.

Diameter specified in the SW File: .127 cm  
Diameter of actual printed bracket: .122 cm

Distance of plywood insert in the SW File: .318 cm 	
Distance of plywood insert of actual printed bracket: .309 cm

![20print](https://cloud.githubusercontent.com/assets/12373812/23770588/9837019c-04e1-11e7-904c-8a529ec3e6c5.JPG)

*In order to achieve a clean edge for the plywood to be inserted into the bracket, you may need to use pliers to get rid of the support material and use sandpaper to smooth down any remaining plastic.*  

![sanded](https://cloud.githubusercontent.com/assets/12373812/23770600/a79328a0-04e1-11e7-8bd3-d68dca7c0e5d.JPG)


### [Dimension Elite](http://www.stratasys.com/~/media/Main/Files/Machine_Spec_Sheets/PSS_FDM_DimElite.pdf?la=en)

![WithSupport](https://cloud.githubusercontent.com/assets/12373812/23810655/77331124-05a0-11e7-95b7-20e54b15aa75.JPG)

Layer Resolution: 0.0100  
Model Internal: Sparse- High Density  
Support Infill: SMART
STL Units: mm

Using the above settings, the estimated print time is 1 hour and 35 minutes. The materials usage is 0.80 in^3 of model material and 0.20 in^3 of support material.

Diameter specified in the SW File: .127 cm  
Diameter of actual printed bracket: .126 cm

Distance of plywood insert in the SW File: .318 cm 	
Distance of plywood insert of actual printed bracket: .315 cm



### [Objet 30Pro](http://www.stratasys.com/3d-printers/design-series/objet30?cid=70130000001stsN&utm_ad=Objet30&utm_source=google&utm_term=objet30&utm_campaign=Search+-+US+-+Brand&utm_medium=cpc&utm_content=sDBnZ7UQ1_dc%7Cpcrid%7C102344693641%7Cpkw%7Cobjet30%7Cpmt%7Cp%7C&gclid=CJ2l8qOBu9ICFZCFswodHTwPbg)

![WithSupport](https://cloud.githubusercontent.com/assets/12373812/23810630/5f09ac20-05a0-11e7-80ca-127fbf5938e9.JPG)

Unlike the previous 3D printers, the Objet30Pro does not have as many options to change the density of the part or the layer height. This model was printed without a glossy finish.

The estimated print time is 3 hours and 58 minutes. The materials usage is 27.0 grams of VeroGrey and 18.0 grams of support material.

Diameter specified in the SW File: .127 cm  
Diameter of actual printed bracket: .126 cm

Distance of plywood insert in the SW File: .318 cm 	
Distance of plywood insert of actual printed bracket: .316 cm
