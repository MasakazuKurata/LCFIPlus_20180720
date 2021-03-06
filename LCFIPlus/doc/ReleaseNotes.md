# v00-06-07


* 2017-06-16 Andre Sailer ([PR#23](https://github.com/lcfiplus/LCFIPlus/pull/23))
  - Fix crash when BeamspotContraint is false
  - Fix memory leak in VertexFinderSuehara

* 2017-11-14 Frank Gaede ([PR#32](https://github.com/lcfiplus/LCFIPlus/pull/32))
  - move release notes to ./doc/ReleaseNotes.md
  - add Licence (GPLv3)
  - update to v00-06-06 and add release notes for this
      - only documentation, release originally made on iLCSoft fork

* 2017-11-14 Frank Gaede ([PR#31](https://github.com/lcfiplus/LCFIPlus/pull/31))
  - replace Gear w/ DD4hep
       - only used for accessing the B-field
       - dependency on DD4hep only implicitly through MarlinUtil

* 2017-07-28 Dan Protopopescu ([PR#27](https://github.com/lcfiplus/LCFIPlus/pull/27))
  Removed redefinition of 'integ'

* 2017-05-27 Andre Sailer ([PR#21](https://github.com/lcfiplus/LCFIPlus/pull/21))
  - lcfiplus::Parameters: fix implementation of the copy constructor, fixes lcfiplus/LCFIPlus#19


# v00-06-06

* 2017-07-02 Andre Sailer ([PR#24](https://github.com/lcfiplus/LCFIPlus/pull/24))
  - Processor parameters are now a shared_ptr

# v00-06-05
- Deal with TMVA API changes in ROOT 6.08

# v00-06-04
- Cope with newer version of TMVA: need a patch commited to ROOT on 16 Sep 2016.
  Use ROOT version newer than above date.
- Suppress warnings with c++11.

# v00-06-03
- Bugfix in JetFinder (default behaviour changed at v00-06-01)
- Durham and Valencia jet algorithms with beam jets introduced

# v00-06-02
- Automatic creation of JointProbability histograms implemented
- Calculation of joint probability with histograms automatically created (jprob2)
  Use v03_p01 steering, vertex probability and weight files in ILDConfig
  for the new joint probability.

# v00-06-01?
- Added possibility to include beam jets in JetFinder (thanks to Philipp Roloff)

# v00-06-00a

**Development release: please use at your own risk **
- 6-category training (b,c,o,bb,bc,cc) implemented
- Extracting all variables used for the flavor tagging now available
- Added MC-related input variables (MCnb, MCnc etc.)
  in flavor tagging to be used for training
  (available only if MCParticle collection is supplied)
- Added more input variables for flavor tagging

# v00-05-02
- Fixed type conversion error in track hits
- Fixed MC vertex information
- Added option to choose track hit ordering
- Modifications to track selection criteria involving subdetector hits
- Vertex-jet reassociation no longer throws exception to cope with cases
  where tracks are dropped such as when running kt algorithm before LCFIPlus

# v00-05-01
- Improved steering options thanks to P.Roloff
  1) The magnetic field can be specified (default behavior is to read from GEAR).
	2) The beam constraint in the primary vertex fit can be switched off.
	3) The beam size can be adjusted.
	4) The cuts on the number of hits to calculate jointProbD0 and jointProbZ0,
	and to find the most significant track can now be adjusted.

# v00-05
- vertex-assisted jet clustering now adjustable with vertex pairing penalties
- flavor tagging input variables added
- can apply preselections to samples used in training

# v00-04
- lcfiplus processor should work with multiple instances
- single track pseudo-vertex added
- jet vertex refiner algorithm added
- improved v0 rejection
- new flavor tagging variables + various bug fixes
- updated steering files
