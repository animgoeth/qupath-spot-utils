# qupath-spot-utils
Scripts for processing microarray spots in QuPath

### *extract_annotated_spots*

This script finds spots that intersect annotated regions within a slide and saves their positions + annotated labels in a CSV file.

**Input format:**

Spot coordinates file:
```
ACGCCTGACACGCGCT-1,0,0,0,947,1161
TACCGATCCAACACTT-1,0,1,1,1099,1248
...
ATACCCTGGCTCAAAT-1,0,1,13,1101,2295
GGGTTTCCGGCTTCCA-1,0,0,14,950,2383
```

Scale factor file:
```
{"spot_diameter_fullres": 113.41830135687084, "tissue_hires_scalef": 0.1370614, "fiducial_diameter_fullres": 183.2141791149452, "tissue_lowres_scalef": 0.04111842}
```

**Usage:**
1) Load an annotated tissue slide in QuPath
2) Click *Automate -> Show script editor* in QuPath's menu
3) In the Script Editor window, click *File -> Open...* and choose the *extract_annotated_spots.groovy* file
4) Navigate to the bottom of the file and fill in the proper file paths for SPOT_COORDINATES_FILE_PATH, SCALE_FACTOR_FILE_PATH and OUTPUT_FILE_PATH
5) Click *Run -> Run* in the Script Editor window
