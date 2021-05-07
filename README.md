# ConfSurface

#### Scratching the surface of configurable systems: 
 * understanding how compile-time options have effects on binary size and gadget (surface attack); 
 * build predictor models/configurators; 
 * automate the exploration with variability modeling and reproducible build environment
 
#### Subject systems:
 * x264 : https://github.com/ternava/x264/tree/x264-compileoptions
 * nginx : https://github.com/ternava/nginx/tree/branches/nginx-conf-options
 * curl : https://github.com/ternava/curl/tree/curl-compileoptions
 * sqlite : https://github.com/ternava/sqlite/tree/sqlite-compileoptions
 * xz : https://github.com/ternava/xz/tree/xz-compileoptions

In each project of the system there is a `measures` folder, which contains the used scripts and the obtained results on `binary size` and `number of gadgets`. 

 #### Feature models: 
 * [FM of x264](featuremodels/fm-x264.png)
 * [FM of nginx](featuremodels/fm-nginx.png)
 * [FM of curl](featuremodels/fm-curl.png)
 * [FM of sqlite](featuremodels/fm-sqlite.png)
 * [FM of xz](featuremodels/fm-xz.png)
