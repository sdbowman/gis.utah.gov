---
status: publish
layout: page
tags:
  - dem
  - lidar
author:
  display_name: Rick Kelson
  email: rkelson@utah.gov
published: true
date: 2017-05-22 23:29:51
title: Monroe Mountain LiDAR Elevation Data (2016)
categories: []
---

<style type="text/css">
#logo {
  max-width: 400px;
  margin: 0 auto;
}
</style>
<div id="logo">
  <img src="{{ "/images/lidar_monroe.PNG" | prepend: site.baseurl }}" alt="Monroe Sample" />
</div>

[![Project area map]({{"/images/lidar_monroe_coverage_sm.png" | prepend:site.baseurl}} "click for map")]({{"/images/lidar_monroe_coverage.png" | prepend:site.baseurl}}){:.inline-text-right}

During the Summer of 2016 AGRC and the U.S. Forest Service acquired [292 square miles]({{ "/images/lidar_monroe_coverage.png/" | prepend: site.baseurl }}) of 8 points per meter Quality Level 1 LiDAR on Monroe Mountain in central Utah. The acquisition took place with leaf-on conditions to model the forest canopy in addition to ground elevations. The .5 meter resolution bare earth DEMs and first-return/highest-hit DSM in .tif format have a 10.0cm vertical RMSE accuracy and are available for download. The LAS classified point cloud are also available [by request](mailto:rkelson@utah.gov) and eventually from [Open Topography](http://www.opentopography.org/). This elevation data was collected between Aug. 27 and Sept. 11, 2016 and has a UTM NAD83 (2011) zone 12 north meter NAVD88(GEOID12) projection.

<ul class="dotless">
  <li>
    <strong>
      <i class="fa fa-download"></i> <a href="http://raster.utah.gov/?cat=.5%20Meter%20%7B2016%20LiDAR%7D" target="_blank">Retrieve 2016 Bare Earth DEMs and First Return DSMs via Interactive Map</a>
    </strong>
  </li>
  <li>
    <i class="fa fa-download"></i> Download project <a href="https://storage.googleapis.com/state-of-utah-sgid-downloads/lidar/monroe-mtn-2016/DEMs/MonroeMtn_2016_Report.zip" target="_blank">Reports</a> and
      <a href="https://storage.googleapis.com/state-of-utah-sgid-downloads/lidar/monroe-mtn-2016/DEMs/MonroeMtn_2016_Metadata.zip" target="_blank">Metadata</a>
  </li>
  <li>
    <i class="fa fa-download"></i> Download <a href="https://storage.googleapis.com/state-of-utah-sgid-downloads/lidar/monroe-mtn-2016/DEMs/MonroeMtn_2016_shp.zip" target="_blank">shapefiles</a> of project area, tile indices, and breaklines
  </li>
</ul>

The naming convention for the tiles are based off the [U.S. National Grid (USNG)]( http://www.fgdc.gov/usng/how-to-read-usng/index_html).

This elevation data has a UTM NAD83 (2011) zone 12 north meters NAVD88(GEOID12) projection

If you need assistance contact Rick Kelson at [rkelson@utah.gov](mailto:rkelson@utah.gov)

<div id="logo">
  <img src="{{ "/images/monroe_DEM.png" | prepend: site.baseurl }}" alt="Monroe Sample" />
</div>
<div id="logo">
  <img src="{{ "/images/monroe_DSM.png" | prepend: site.baseurl }}" alt="Monroe Sample" />
</div>
