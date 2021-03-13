Scripts for processing IGETS data: **igetsDataTools**
=====================================================
This repository contains **Matlab/Octave** scripts and functions related to loading/writing/processing of gravimeter data stored in **International Geodynamics and
Earth Tide Service** ([IGETS](http://u.720life.cn/g/5f0235e00a14ad5b79d0dd2fece3543a91fb7558449b20c26808568d647b005ddd16ab4c3484373ccdb1f1a093e2f764)  database.  
### Dependency
* To run any script, download the [hydroGravityLib](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cb87c1f19afe2d991ca90fb50da5f73ae22784e2faefcb4229ca1062d0c41b8a)  (Matlab/Octave HydroGravity Library) and adjust the paths in the script accordingly
* All scripts should work with both, Matlab and Octave, although the loading of one second monthly data in Octave takes lot of time :-(  
* Scripts tested using iGrav006 gravimeter data

### Scripts and Functions
* `igets_set_and_run.m`: **main script** containing all settings. Run this script to call other processing functions
* `igets_raw_to_ggp.m`: conversion of 1 second iGrav [TSoft](http://u.720life.cn/g/5b6237a02cceec628dd91e2925b181fd072d24102cf5a01183d7c75635241b3f8680a91f54451fc932940f8f7c560d62)  files to ggp/igets data format/database, i.e., convert daily data to monthly files  
* `igets_sec_to_min.m`: filter and re-sample/decimate the created or downloaded monthly ggp/igets data to 1 minute data
* `igets_min_to_hour_res.m`: filter and re-sample the 1 minute data to hourly gravity residuals
* `igets_export_data.m`: load + stack one second/minute/hour data and save the whole time series into one file (ggp/tsf/mat format)  
* `igets_import_data.m`: import data stored in other formats (e.g. tsf or mat) to IGETS database. For example: use to convert precipitation data

### Auxiliary files
Besides the IGETS data, some auxiliary files are needed. The `data` folder contains examples of such files:
* modified filter files: `g1s1md.gwr` (1 second to 1 minute) and `g1m1h.nlf` (1 minute to 1 hour). Always use (modified) filters recommended by IGETS!
* `tides_file_example.tsf`: tides time series used when computing gravity residuals
* `correction_file_example.txt`: correction file used in to remove anomalous time intervals (set to NaN), gaps (linear interpolation) and to remove steps



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)