# Human Mobility Study using Wi-Fi Data #

## SSTM Method ##
SSTM represents the **Semantic Space-time Matrix** model. The SSTM model is developed to derive the semantic information of human movements. It is implemented through aggregating the temporalities and activity types of the track points derived from people's movement trajectories sensed by **Wi-Fi detectors**.

Please refer to the article for details.

## Study Area ##
The study area is the **Shichahai scenic area** of Beijing, China (Figure 1). This area is known for its unique hutong culture, a residential culture of grassroots Beijingers living in small alleys, which can be traced back to the Yuan Dynasty (1267–1368 AD). As a reminiscence of the history, the Shichahai scenic area has been gentrified for mixed urban functions, including cultural preservation, residential housing, and tourist development. Also, due to the large volume of daily visitors, human mobility patterns in the area are extremely complex. This complexity is further confounded by unorganized building footprints, where small alleys crisscross an open and geographically small area (i.e., 146.7 hectares or 0.56 square miles in total area).

![Study area](https://github.com/xic19022/wifi_bj/blob/img/Study_area.jpg)

<div align="center">Figure 1. Wi-Fi detectors installed in the study area</div>
<br />

## Introduction to Wi-Fi Data Collection ##

Wi-Fi sensing employs a Wi-Fi detector that tracks Wi-Fi probe requests within an effective detection range when a mobile device attempts to establish a wireless connection to the 802.11 wireless network, generally known as the Wi-Fi network (see Figure 2a). In the case study, we used the WIFIPIX WP-300 Wi-Fi detectors with a detection range of 25 meters (see Figure 2b). 

![Wifi_detector](https://github.com/xic19022/wifi_bj/blob/img/Wifi.jpg)

<div align="center">Figure 2. (a) Diagram of the Wi-Fi data collection; (b) the Wi-Fi detector used in the study</div>
<br />

When a probe request is received by the Wi-Fi detector, it will be decoded into readable attributes, including: 

* Wi-Fi detector ID
* MAC address of the mobile device
* Start stimestamp
* End timestamp
* Date

The information is then uploaded to a cloud server and can be exported into a tabular file (i.e., the comma-separated values [CSV] file) for analysis. The Wi-Fi connection records can then be geocoded based on the location of the Wi-Fi detector. Also, since the MAC address is unique for each mobile device, it can become the identifier of the movement trajectories completed by the same traveler.

## Wi-Fi Data ##
The Wi-Fi data for the study area were collected by the 29 Wi-Fi detectors installed in the study area from October 2 through October 14, 2018. They contained the Wi-Fi connection records derived from 463,874 individuals. Due to privacy concerns, the last four digits of the user's MAC address were masked out.

The Wi-Fi data can be downloaded from [here](https://github.com/xic19022/wifi_bj/blob/master/Wifi.zip).

## POI Data ##
The point-of-interest (POI) data were used for deriving the activity types for the SSTM modeling. The raw data was derived from AutoNavi (www.amap.com), one of the largest web map service providers in China.

The POI data can be downloaded from [here](https://github.com/xic19022/wifi_bj/blob/master/POI.xlsx).

## SSTM Codes ##
The Python codes for generating the SSTM can be downloaded from [here](https://github.com/xic19022/wifi_bj/blob/master/SSTM_codes.zip).

Instructions for using the codes can be accessed from [here](https://github.com/xic19022/wifi_bj/blob/master/SSTM_Instructions.md).
