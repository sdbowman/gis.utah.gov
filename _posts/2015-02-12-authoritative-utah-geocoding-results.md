---
status: publish
layout: post
author:
  display_name: Steve Gourley
tags:
  - api
  - geocoding
  - mapserv
  - qaqc
  - quality assurance
  - roads
published: true
date: 2015-02-12 18:52:22 -0700
title: Authoritative Utah Geocoding Results
categories:
  - Developer
  - Featured
  - SGID Blog
---
<p><a href="{{ "/downloads/Screen-Shot-2015-02-12-at-6.49.06-PM.png" | prepend: site.baseurl }}"><img src="{{ "/images/Screen-Shot-2015-02-12-at-6.49.06-PM.png" | prepend: site.baseurl }}" alt="" title="Screen Shot 2015-02-12 at 6.49.06 PM" width="219" height="266" class="inline-text-left" /></a>
<h3>Geocoding Assurance <em>or</em> Why you should trust the results</h3>
<p>The AGRC <a href="http://api.mapserv.utah.gov">web api</a> is a great resource for deriving information from the <a href="{{ "/data" | prepend: site.baseurl }}">SGID</a>. Geocoding an address is one of the more popular and useful free services. But it is important that users have confidence in the match results returned from the geocoding api.</p>
<p>As you may know, the geocoding api uses <a href="http://api.mapserv.utah.gov/#geocoding">address points and road centerlines</a> to locate the best match when geocoding. Or, users may specify that the matches come only from centerline or address points. Each of the 29 Utah counties provide AGRC with a periodic update of their local road centerline and address point data. This schedule allows the geocoding api to use the most current data in order to provide the best match results.</p>
<p>Comprehensive updates, which are new roads, subdivisions, and road name and address range changes, are made to <strong>1 urban county</strong> <em>(Davis, Salt Lake, Utah, Washington, or Weber)</em> and <strong>2 rural counties</strong> on a <strong>monthly</strong> cadence. For a given month, the <strong>other four</strong> urban counties receive new road and subdivision updates only. The counties chosen for update are based on a <a href="https://docs.google.com/spreadsheet/ccc?key=0Aj18jufMWioidENRNDhPb3VtRTFGamJfYzlPal9TNmc&amp;usp=sharing">round robin schedule</a>. It is important to keep in mind that the these statewide layers would not be possible without the active partnership of, and excellent work performed by local government GIS staff over the years! </p>
<p>AGRC partners with many <strong>911 Call Centers</strong> (aka PSAPs) and the <strong>Blue Stakes of Utah Utility Notification 811 Center</strong> to receive <a href="{{site.baseurl}}{% post_url 2015-02-09-utah-sgid-statewide-roads-data-layer-updates-242015 %}">address improvement feedback</a>. This feedback is given to AGRC, <em>and the counties</em>, on a <strong>monthly</strong> basis. All of these updates are then pushed to the public <strong>roads</strong> dataset in the SGID on the <strong>first Wednesday</strong> of each month.</p>
<p>When these changes are detected by nightly automated tasks, python scripts download the data, update geocoding address locator indexes, and publish them as services for the web api to use. These automated tasks help the geocoding api give the most accurate and current matches.</p>
<p>Utah addresses are unique from other states because of a strong <a href="http://www.exploreutah.com/GettingAround/Navigating_Utahs_Streets.shtml">address grid system</a>. The address grid system enables us to make special assumptions and optimizations to address finding processes used by the geocoding api. For more information about some of these techniques, you can view <a href="http://steveoh.github.io/Presentations/2014/UGIC/#0">the slides</a> from a UGIC presentation or view a <a href="https://www.youtube.com/watch?v=BHhQxxXy6bo">video</a> of <a href="http://twitter.com/steveagrc">Steve Gourley</a> giving the presentation at an <a href="https://www.youtube.com/user/UtahDTS">EDG brown bag</a> event.</p>
<p>In an effort to keep the geocoding match results of a high quality, we created a <a href="https://github.com/agrc/AddressAssurance">sample dataset</a> of Utah addresses for testing, which you can <a href="https://github.com/agrc/AddressAssurance/blob/master/GCTestAddresses.gdb.zip?raw=true">download</a> for your own purposes. This random sampling of test addresses from across the state contains the X,Y location for where the address <em>actually</em> is. The <strong>~800</strong> address locations in the dataset were quality controlled and validated by AGRC staff. This dataset allows AGRC developers to test the web api geocoding match results against addresses of different types around the state. Using the expected locations and a little math, the developers can validate match results prior to every update to the geocoding api (including the api pre-logic, the behind the scenes locator engines, and the road and address data). The results are then compared to ensure that they are within an acceptable distance from where the actual address location is.</p>
<p>These tests give AGRC and it's developers the assurance to add new features and optimizations to increase the match rates without creating undesired side-effects. When a new feature or optimization idea is implemented, every address in the sample dataset must match within an acceptable distance or else it's back to the drawing board.</p>
<p>Our road centerline and address data updates sourced directly from local government together with the mature and quality assurance testing that is performed with new api releases are very important to the quality and consistency of geocoding results. We are happy to provide even more behind-the-scenes detail about the AGRC geocoding api service upon request. It is important that users have confidence in what we feel is <strong>the authoritative source</strong> for statewide address finding services that are used in many important Utah analyses and applications.</p>
 