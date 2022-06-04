====================================
Instructions for adding new datasets
====================================

The following is a tentative list of details that should be mentioned while entering data in the HybriD\ :sup:`3` database, along with the probable location in published literature where such information can be found. This document can be used as a general guideline for the purpose of adding new datasets.

-----------------------------------------------------
Atomic structure 
Dealing with crystallographic information files (CIFs)
-----------------------------------------------------

Crystallographic information files (CIFs) are a standardized file format, generated after collecting and solving diffraction data (generally, X-ray diffraction or neutron diffraction). Information on the atomic structure of a material, along with the measurement conditions, can be found in the CIFs. Also, one CIF can contain information on multiple structures. These files are usually submitted with manuscripts to journals and are expected to be peer-reviewed before publication. Prior to including any CIF in the HybriD3 database, it is critical to ensure that the copyright holder of each particular CIF has agreed that we are allowed to include the CIF. CIFs are not just bare data (i.e., they do not just state trivial numbers but rather contain a great deal of specific text) and they are clearly and legitimately subject to copyright. Including CIFs from other, external databases, for example, is usually not permitted and individual permission from the authors must be sought to include a format that is not the same CIF as stored in an existing database.
Where can you find the CIF?
There are three possible locations – 
1.	“Supporting/Supplementary Information (SI)” section of the paper. In this case, it is usually necessary to obtain permission from the author(s) to include the CIF file in HybriD\ :sup:`3`. Please be mindful of the authors' hard work to obtain their data in the first place. In HybriD\ :sup:`3`, we hope that disseminating such data with permission of the authors is helpful and broadens the visibility of their work, but the decision is clearly theirs.
2.	Rarely, some authors do put CIF as texts in the SI pdf. If no CIF is found in the paper, but the content suggests that there should be one(s), check the pdf of SI. As before, the permission of the authors is usually needed in order to be allowed to reproduce the CIF in the HybriD\ :sup:`3` database.
3.	Lastly, there are a few large online repositories. For example, the Cambridge Crystallographic Data Centre (CCDC; ccdc.cam.ac.uk/structures/), or the Crystallography Open Database (COD; crystallography.net/cod/search.html), let us search for structures with the paper’s DOI. As mentioned above, using these services always requires abiding by their copyright rules. We are not simply allowed to upload a database's CIF to the HybriD\ :sup:`3` Database unless the general copyright rules of that database unambiguously permit this. Usually, we do not have this permission. In such cases, the best path is still to write to the corresponding author of the paper for permission.
What to do with the CIF?
Once a CIF is available with permission, several next steps are needed for inclusion in HybriD\ :sup:`3`. First, open the file in any visualization software, such as JMol [http://jmol.sourceforge.net], VESTA [jp-minerals.org/vesta], or Mercury [ccdc.cam.ac.uk/solutions/csd-core/components/mercury/]. Each software offers many features, so going through the software documentation might be helpful. At this step, note the number of structures available in the CIF. 
Then, open the same file using a text editor (right-click – open with – any text editor of your choice). It’s better to use a text editor that lets you search (ctrl+f or cmd+f) for keywords. 
Note the following information* – 
1.	Crystal system (search for “system”) 
2.	Space group (search for “space group”) [If there is a suffix in the notation, type it in the first bracket. e.g., for Pnm2\ :sub:`1`, type it as -  Pnm2(1)]
3.	The color of the crystal (search for “colour” or “color”)
4.	The shape of the crystal (search for “description” or “shape”)
5.	Radiation type and wavelength (search for “wavelength”) 
6.	Measurement temperature (search for “temperature”) [be sure to note the error in measurement]
7.	Errors in lattice parameters [Errors can be inputted simply by typing them in the bracket with the parameters. E.g., typing “18.617(4)” in add data page will show up as 18.617(±0.004) when the dataset is published]

As always, please include the original reference to the authors' work (typically, a journal reference) in the HybriD\ :sup:`3` database along with the data for proper reproducibility, attribution, and further details.
* If there is more than one structure, be sure to correctly associate the noted information with the corresponding structure. Some of these details may also be available in the main paper or SI.
# Errors in lattice parameters are updated automatically when CIFs containing single structures are directly uploaded from the “ADD Data” page without any conversion.

--------------------
Synthesis method
--------------------

A “Synthesis method” section can usually be found in all experimental papers. Be sure to check the SI, if it is unavailable in the main paper. The followings are the section-wise guidelines for writing the methods in our database. Please do not simply copy text verbatim from a reference since that text will, in fact, be subject to copyright by the authors or publisher.
For “Starting materials,” 
<the full name of the chemical used> (<the abbreviation or formula>, <purity>, <make>).
E.g., lead iodide (PbI\ :sub:`2`, 99.99%, Sigma-Aldrich), methylammonium iodide (MAI, >99%, Alfa Aesar), etc.
For “Product,”
<color><shape><formula><sample type>
E.g., Orange plate-like (PEA)\ :sub:`2`PbI\:sub:`4` crystals
For powders and films, “shape” will be usually unavailable.
For films, <thickness> might be available.
For “Description,”
-	Use the formula or abbreviations of the reactants
-	Write the amount taken (in grams/ molar/ ml - whichever is available on the paper)
-	Write the temperature at which a particular step is performed
-	Write the time required for the completion of each step

---------------------
Experimental details
---------------------

Similar to the synthesis methods, in peer-reviewed papers, a section named “experimental details” is always available either in the main paper, or in the SI, though the location varies among journals and article types. In some cases (e.g., correspondence articles), the details do not appear as a separate section but are often buried inside the main text, or even as a reference at the end of the paper. 
For “method,”
Write the full name of the experiment: for example, “Single-crystal X-ray diffraction”, “Powder X-ray diffraction”, “Photoluminescence spectroscopy”, “Diffused-reflectance spectroscopy”, etc.
Note that “Photoluminescence spectroscopy” is a method, but “Photoluminescence spectrum” is not a method. Do not copy-paste the method name from the primary property card.
For “Description,”
Mention the name of the instrument. 
If the measurement is Single-crystal X-ray diffraction, mention the radiation source and the wavelength.
Additionally, use the “Fixed parameter - Physical Property” field – 
If the measurement is Photoluminescence spectroscopy - specify the excitation wavelength.
If the measurement is Photoluminescence excitation spectroscopy - specify the emission wavelength.
For all measurements - specify the temperature. For “room temperature,” use 298 K.
As before, please do not copy non-trivial segments of text literally from other sources but rather include just the bare data in the format consistent with other entries in the HybriD\ :sup:`3` database itself.

---------------------
Axis labels
---------------------

The axis label can be specified in the “primary (or secondary) property label” fields. Unless specified, the database uses the y-axis (x-axis) label same as the primary (secondary) property. For example, by default, a photoluminescence dataset will display “photoluminescence spectrum (arbitrary unit)” on the y-axis. However, “photoluminescence spectrum” is not a “property” of the system, “Photoluminescence intensity” is. This is why it is always better to specify the label and use it the same as the source.
The following are a few primary properties and the recommended corresponding y-axis labels that we can use:
Photoluminescence – Intensity
Absorbance – Normalized absorbance [Note: sometimes absorbance is reported in paper as absolute values. In such cases, the label should be “Absorbance”]
PXRD – Intensity
