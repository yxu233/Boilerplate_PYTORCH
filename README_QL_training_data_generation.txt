Files to open:
(1) Open .tif image in ImageJ
(2) Drag the ImageJ macro "save_ROI for QL.ijm" into ImageJ to open it


Tracing:
(2) Use the "circle" tool to circle the DAPI nucleus in the image *** always do this FIRST, before tracing any sheaths
(3) Press "t" to save ROI in ROI manager
(3) Right click on the "straight line" tool and select "segmented line"
(4) Draw segmented line over where you think the sheaths are located
	- repeat until all are traced
(5) Then go to the ImageJ macro you opened before and click "run" (bottom left corner), that will save the current cell you traced in the folder you indicated in the macro
	- repeat all of these tracing steps for all the cells in the image you want to segment
	***you don't have to do every cell
	***check to make sure it saved properly!!! Each new ROI file should have a unique numerical identifier __001, 002 ect... so make sure you're not overwriting files. If so, let me know.


Tips:
- if you lose track of which cells you have done already, go to the folder where your ROI are being saved, and you can drag all of the ROI into ImageJ to see where you left off
	***just remember to clear the ROI manager manually so you don't accidentally save ROI of past ROIs

- try to offer as much variety in your tracing as possible, don't just go for the easiest cells to trace

- ***send me a few sample ROIs at the beginning so I can make sure it is working okay. Also send me the raw data to go with the ROIs

- ***always keep track of all the raw data you've traced. Best is to make a copy in a new folder, so we can come back to it easily instead of having to dig through a bunch of files.