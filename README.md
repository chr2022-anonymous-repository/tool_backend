# Guide to Backend

 - [front-end API specification](./API_v0.1.4.yml): Swagger API specification for the frontend written by ??? (upload at https://swagger.io/tools/swagger-editor/ for a nice view)
 - [server configuration files & instructions](./server_config.zip) used for setting up the development server (Ubuntu + NGINX)
 - [`v0_8.zip`](./v0_8.zip) version 8 of the backend which includes the Flask app, helper functionality and the bias scoring engines' definitions



## Installation of the Server 

Either follow the Server configuration instructions to setup a (Ubuntu+NGINX) server. Or, if you have a server set up, skip this step and directly set up the Flask app:

 0. (the Flask app requires a virtual enviroment to be installed in the folder it is served from (otherwise startup scripts will fail))

 1. the app needs to be 'assembled' from the parts in this repository:
   - copy the contents of the latest version of the backend (currently v0_4) into the folder you want to serve the Flask app from
   - copy the lastest version of the NMvW data set in /data (OMITTED) into {your_path}/NMvW_data/
 
 
 2. in app.py (inside v0_8), there are hard-coded references to directories:
  - data_dir: "/data/" (location of pre-cached and saved engines)  
    these references need to be changed to where the data is located
