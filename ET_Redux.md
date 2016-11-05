##ET_Redux Documentation Overview

ET_Redux is a stand-alone desktop application, produced by CIRDLES.org as the successor to U-Pb_Redux in January, 2015, with the initials "ET" referring to its sponsor [EARTHTIME](http://www.earth-time.org). ET_Redux is cyber infrastructure for geochronologists that automates workflows from sample collection to publicly archiving of results into the NSF-sponsored [Geochron](http://www.geochron.org) community database. ET_Redux exports analysis results as an [aliquot](https://raw.githubusercontent.com/EARTHTIME/Schema/master/AliquotXMLSchema.xsd) XML file, which can be exported to Geochron or stored and shared as desired.  ET_Redux currently serves the ID-TIMS and LAICP-MS U-Pb geochronology communities and is funded 2014 - 2017 by NSF to extend to U-series analyses.

##Information for use of Documentation
The documentation below is essentially a set of step by step instructions on how to operate the software. For auditory and visual learners, youtube video tutorials will be included among the written instructions.

##Concept of operations
ET_Redux provides sophisticated graphical and statistical tools to assist with data ingestion and organization, data reduction, uncertainty propagation, visualizations, publication-ready vectorized tables and plots, and one-click archiving. These include interactive data tables, concordia and weighted mean plots, dynamic decomposition of uncertainties into contributions from individual sources, and algorithms for propagation of systematic uncertainties in tracer calibration and decay constants. 

##Policies that affect the system
ET_Redux is sponsored by EARTHTIME and funded in part by the National Science Foundation under Grant Numbers 0930223 and 1443037. Any opinions, findings and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the National Science Foundation (NSF).

##Starting ET_Redux and starting data reduction

##Procedures
(-Youtube videos)

###New Project from Raw Data
1. Open ET_Redux - note that this will generate two html files, ChangeLog.html and Credits.html
1. To start, click Project in the top left corner.
1. Then click New Project from Raw Data.
1. Click LA-ICP-MS.  Note that IDTIMS raw data is currently processed by our software [Tripoli](http://cirdles.org/projects/tripoli/).
1. Now you will see the Project Manager interface where you specify your project. Start by entering your Project Name and then choosing the appropriate:
  * File Handling Protocol
  * Raw data template
  * Analysis purpose
1. Finally, press "Prepare to load/Process Raw Data." Then, depending on your file handling protocol you will be able to select your data file or data folder and then click Open to show the parameters manager. If you use folders, be sure that all necessary files are present.
1. Confirm that all parameters are correct - the defaults are shown initially.
1. Full Uncertainty propagation is the default - use the fast option to explore datasets only.
1. Seolect your Primary Reference Material.  Note the default is set in the Lab Settings Manager.
1. Now you are ready to start the reduction process. You can either start a live session while the mass spectrometer is producing data or proceed to reduce an already-collected dataset as explained below.

###Live Data Reduction Processing (to be revised):
1. Press, Save and Monitor/Process Raw Data
1. Once launched you will have to wait for at least 3-4 analysis to be reduced before seeing any data.
1. To remove unwanted analysis, right click on the selected grain in your report table located below concordia, it will now be sent to the rejected fractions tab but will still be reduced
	4. To look at individual groups of grains (Standards or Unknowns), click on the sample name in the left hand column, a drop down menu will appear with all available groups to view on Concordia and on the PDF.
	5. To set different filters, adjust them under the PDF. To apply them to the Concordia plot, select apply filters under the Concordia.
	6. To change what ages are shown on the PDF, select one of the three ages (6/8, 6/7, or best age). We suggest the best age option.
	7. Best age filter can be changed while you are looking at unknowns in Concordia space
	8. When a grain is removed be patient, it will take until the next FC grain to update the session.
	9. If you need to refresh, hit Refresh Views
	10. Wait until the run has completed and proceed to Project Raw Data Manager section.

###Project Raw Data Manager (to be revised)
	1. To make your view easier:
		a. Y-axis Scaling set to Independent
		b. Also press Show All Local Y-axis
	2. Proceed to look through all your reference materials to make sure your ratios are within the acceptable rages. It will be very clear when an analysis is bad. You will either see a very large scatter in data points or the fit line will be far off the data points.
	3. Once you have looked over your data points proceed to click on the Show Session button
	4. You will now be directed to the Fractionation Plots. Here is where we will remove any poorly behaved reference material analysis and hopefully achieve an MSWD of 1.0.
	5. To remove a data point, hover over an errant black spot and right click. You will be asked to “exclude this fraction, click on it and the black dot will change to red indicating it has been removed.
	6. Once you have removed all unwanted data points you MUST hit refit, so that the changes you have made update the plot and MSWD. You can play with which fit function you like, but generally we utilize the line.
	7. When you are happy with your fits, to complete your reduction hit update report table. Once you click the update report table button it will be grayed out which indicates that it is working. Wait until it finishes indicated by the greyed returning to white.
	8. Press Save in the bottom left hand corner and then close the window.
	
###New Sample Analysis for ID-TIMS
	1. Go to Sample and click New Sample Analysis for ID-TIMS.
	2. ID-TIMS Workflow Manager for ANALYSIS MODE of a Sample
	3. Choose the Local Sample Name and fill in that field.
	4. Choose between Sesar and GeochronID for the Registry and fill in the Sample ID IGSN.
	5. Select Analysis Purpose and choose the Set Phsyical Constants Model.
	6. Under Aliquot name, click Add Name and the information for the new Aliquot will be displayed in the blue box. The information that will be displayed includes, Fraction ID, Tracer, Tracer Mass, Fraction Mass, Pb Blank, Initial Pb model, Est. Date, and the Pb Blank Mass.
	7. The user has the option to remove the selected Aliquot or save it as a sample.

##Glossary
####Sample-A single collection of a geologic material (usually rock or mineral) from one location. A sample has a lab specific name and a unique identifier such as the IGSN provided by SESAR.
####Project- collection of samples
####Sample-composed of aliquots or physical pieces of the sample. It is a single collection of geologic material from one place.
####Aliquot- phsyical pieces of a sample whose dates you wish to interpret seperately.
####Fraction- a paired U+Pb analysis
####Live Workflow- establishes a direct link between Tripoli (another CIRDLES software product) and ET_Redux.
