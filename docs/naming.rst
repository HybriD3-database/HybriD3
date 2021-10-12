========================
Compound names
========================

There are several ways in which one can define the name of a given material and/or chemical compound. In the HybriD\ :sup:`3` database, our objective is to support as many searchable alternative names as possible for a given compound, mapping (where possible) community conventions.

-----------------
Naming a compound
-----------------

The HybriD\ :sup:`3` database supports multiple names for the same compound, reflecting the fact that there are multiple naming conventions in the chemical and materials science literature. Some of them overlap, others may not even be unique between different compounds. Our core objectives are to provide names that are, at least in their combination, unique, but even more importantly to make a given compound findable by users who are potentially using different conventions.

The present version of the database (June 2021 and previously) uses short compound names that are inspired by chemical formulae but that essentially reflect abbreviations commonly used in the perovskite literature.

For instance, the 3D hybrid perovskite methylammonium lead iodide appears first under the name of "MAPbI3", using the frequent abbreviation "MA" for the methylammonium cation.

In a separate field, alternate names for the same compound are provided, e.g., "MAPI" (short form used in the community), "(MA)PbI3", "CH3NH3PbI3" or, indeed, "Methylammonium lead iodide". These are not the only possible names for methylammonium lead iodide, but will give a user a reasonable chance to identify the compound in question with specificity.

We are, of course, aware of more formal naming conventions, most importantly the IUPAC convention that covers organic substances. In detail, however, this convention can deviate from practical conventions used uniformly through our community. For example, methylammonium becomes methanaminium; but additionally, the -NH3 group will also be named "azanium" in other contexts.

However, the "MAPbI3" convention for the "main" compound name quickly becomes ambiguous for more complex compounds. Going forward (post June 2021) and for the time being, we therefore will adopt the following strategy for naming compounds and for providing alternate names:

------------------
Main compound name
------------------

A commonly accepted but chemically sensible verbal name for a compound, such as "Methylammonium lead iodide". This name does not express the full stoichiometry of the compound (for example, this particular compound is a triiodide) but it provides sufficient name recognition in the community to identify the compound in question.

----------
IUPAC name
----------

A field that adds a IUPAC conforming name especially for complex organic cations to the best of our present abilities. For complex molecules, detailed IUPAC names are not simple and, as we understand them, also not always unique. We welcome feedback on particular name choices, should they seem ambiguous or need correction. Thank you!

A particularly relevant question in the `IUPAC Blue Book`_ at the time of writing pertains to the naming of the ionic side chain NH3\ :sup:`+`, commonly named ammonium. In short (Blue Book rules P-73.1.1.1, P-73.1.1.2, P-73.1.2), ammonium is allowed but the preferred name is either azanium or aminium. As mentioned above, for the overall compound names, we prefer ammonium, which is more widely used in the hybrid organic-inorganic semiconductor community in our experience. For the IUPAC naming conventions, we use aminium, but azanium could be used as well. Examples include:

.. list-table::
   :widths: 100 100 100 
   :header-rows: 1

   * - (CH3)4N\ :sup:`+`
     - CH3NH3\ :sup:`+` 
     - C16H24N2\ :sup:`+`
   * - tetramethylammonium
     - methylammonium 
     - phenethylammonium
   * - tetramethylazanium 
     - methylazanium
     - phenylethanazanium
   * - N,N,N-trimethylmethanaminium (PIN) 
     - methanaminium (PIN)
     - 2-phenylethane-1-aminium (PIN)
   
---------------
Alternate Names
---------------

This is an entry that lists as many alternate compound names for a given compound as possible, aiming to make the material in question findable by a search while avoiding to include ambiguous names that would appear in too many unrelated searches. In practice, the web-based search functionality in our data base simply uses sub-strings of names and alternate names as search expressions.

-----------------
Chemical Formula
-----------------

A field that in practice this is the concatenation of the organic and inorganic subcomponents of a material with the appropriate multiplicity for the organic component. The organic component is expressed in standard Hill Notation i.e. C\ :sub:`n`\H\ :sub:`m`\ABC... which is by design not unique. We aim to uniquely identify materials with IUPAC and compound names and instead use the Formula and organic fields as an easily standardizable for quick and broad searches of groups of compounds.

-----------------
Organic Component
-----------------

The organic cation of a given material in standard Hill Notation (see Chemical Formula above) but ignoring multiplicity of these cations for example: Bis(methylammonium) copper bromide would have a Formula of C2H12N2CuBr4 but an organic component of CH6N. This makes the organic component search useful for identifying materials containing a specific cation. If a material has two or more different cations this field is a list of each cation for the same search capabilities.

.. _IUPAC Blue Book: https://www.qmul.ac.uk/sbcs/iupac/BlueBook/index.html
