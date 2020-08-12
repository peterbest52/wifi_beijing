# SSTM Codes #

## Downloads ##
The codes can be accessed from [here](https://github.com/xic19022/wifi_beijing/tree/codes).

## Instructions ##
The python codes *SSTM.py* has been developed to generate the SSTM. Specifically, it derives the visit frequency of the track points based on each user’s media access control (MAC) address.

**Inputs**: Input data for running the *SSTM.py* include the raw Wi-Fi data (filename: *Wifi.csv* in the zipped file *wifi.zip*), weekend dates during the study period (filename: *weekend_date_dict.xlsx*), time periods in a day (filename: *time_period_dict.xlsx*), and the major activity type near each Wi-Fi detector (filename: *activity_type_dict.xlsx*).

Please change the reading and writing file paths to your local directory before running the codes. It may take a few hours to run the codes.

**Outputs**: The output of running the *SSTM.py* is a csv file (*output_SSTM.csv* in the zipped file *output_SSTM.zip*) including ID, user_MAC, and two SSTMs (weekday and weekend, 4×4 for each). In the *output_SSTM.csv*, the kmeans_cluster column is the kmeans++ clustering result of the SSTMs, and this column is derived by the MATLAB codes *kmeans_SSTM.m*.

**Abbreviations** (in the *output_SSTM.csv*):

Day type: W1: weekday, W2: weekend;

Time period: TP1: 0:00–9:00, TP2: 9:00-20:00, TP3: 20:00–22:00, TP4: 22:00–24:00;

Major activity type: AT1: tourist, AT2: residential, AT3: commercial, AT4: mixed;

kmeans_cluster: 1: Local resident, 2: Nearby resident, 3: Passing commuter, 4: Frequent visitor, 5: Weekday visitor, 6: Weekend visitor.