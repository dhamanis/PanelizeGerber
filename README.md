PanelizeGerber
==============

For panelizing gerber files from CadsoftEagle6 (and possibly others)

This software depends on gerbmerge. gerbmerge is a painful to configure software that excels a panelizing large arrays of different dimensions of boards. Due to the random placement algorithm, it struggles to make regular arrays of one design. That is what PanelizeGerber was written to do; it handles all the configuration things to force gerbmerge to do exactly what you want. A copy of gerbmerge1.8 is in a subdirectory of this source (and is referenced accordingly).

Requirements:
	python
	SimpleParse (module for python)

Tested on mac. Should run on linux. Edits will be necessary for windows use.

Use:
--Export appropriate gerbers from Eagle or elsewhere
	--Included is the necessary CAM file for eagle
	--Run prepareCAM.sh to create prepareCAM.cam. This file merely has paths set to put gerbers in the folder with panelize.py
	--for using other software, create these files:

		n.oln (outline)
		n.txt (drills)
		n.gbs (mask, bottom)
		n.gts (mask, top)
		b.gbo (silk, bottom)
		n.gto (silk, top)
		n.gbl (copper, bottom)
		b.gtl (copper, top)

		Currently panelize gerbers only supposed 2 layers, with this specific naming

--Run panelize.py. The command line prompt will lead you through the rest.
--Outputted gerbers are in the output folder.


 
(c) Alexander Dewing (sephamorr) 2013. Released under GPL. Please keep this copyright notice.