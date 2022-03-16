# Prototype Analysis for JIBE project

This Rmarkdown file provides an example multimodal analysis from origins to destinations to inform modelling in the JIBE project.

It uses r5r, an implementation of Conveyal's R5 routing engine for R.  The R5 software evolved from OpenTripPlanner v1, which was its prototype, and is [recommended](http://docs.opentripplanner.org/en/latest/Version-Comparison/) for use for analytical scenarios such as this one. The r5r library was also recommended as the fastest option in a recent paper, *Higgins, C., Palm, M., DeJohn, A., Xi, L., Vaughan, J., Farber, S., Widener, M., & Miller, E. (2022). Calculating place-based transit accessibility: Methods, tools and algorithmic dependence. Journal of Transport and Land Use, 15(1), 95–116. https://doi.org/10.5198/jtlu.2022.2012*.  The analysis drew upon the r5r [vignette](https://cran.r-project.org/web/packages/r5r/vignettes/intro_to_r5r.html).

# Prerequisites:
The installation of Java 11 and PostgreSQL is required, along with r5r and other packages used in the code example.

The analysis was run using R 4.1.3, within RStudio 1.4

The project directory should contain:
- an OSM excerpt for the region of interest, (http://download.openstreetmap.fr/extracts/oceania/australia/)
- a GTFS.zip file (https://transitfeeds.com/p/ptv/497/20190920/download), 
- and data containing origin and destination locations in EPSG:4326 CRS
