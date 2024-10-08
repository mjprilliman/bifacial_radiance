.. _whatsnew_0440:

v0.4.4 (XX / XX / 2024)
------------------------
Bugfix Release  ...


API Changes
~~~~~~~~~~~~
* New input parameter to :py:class:`~bifacial_radiance.ModuleObj and :py:class:`~bifacial_radiance.RadianceObj.makeModule`:  `glassEdge`.  If :py:class:`~bifacial_radiance.RadianceObj.makeModule` `glass` = True, then this extends the glass past the absorber edge by this total amount (half in each x and y direction). Default 10mm.
* Module glass thickness can be changed. In :py:class:`~bifacial_radiance.RadianceObj.makeModule`, if `glass` = True, then setting the `z` parameter will indicate the total (front + back) glass thickness with the 1mm absorber in the middle.  The default is z = 10mm.

Enhancements
~~~~~~~~~~~~
* Conduct an automated check for proper radiance RAYPATH setting (:issue:`525`)(:pull:`537`)


Bug fixes
~~~~~~~~~
* Fixed a major error with indexing the irradiance conditions with :py:func:`~bifacial_radiance.RadianceObj.gendaylit1axis`. This could result in the trackerdict entry being mismatched from the metdata resource. (:issue:`441`)
* versioning with setuptools_scm- set fallback_version to bifirad v0.4.3 to prevent crashes if git is not present (:issue:`535`)(:pull:`539`)

Documentation
~~~~~~~~~~~~~~
* No longer provide a warning message when both `hub_height` and `clearance_height` are passed to :py:class:`~bifacial_radiance.AnalysisObj.moduleAnalysis`  (:pull:`540`)
* More useful __repr__ output in :py:class:`~bifacial_radiance.AnalysisObj and :py:class:`~bifacial_radiance.MetObj   (:issue:`471`)

Contributors
~~~~~~~~~~~~
* Silvana Ayala (:ghuser:`shirubana`)
* Chris Deline (:ghuser:`cdeline`)
