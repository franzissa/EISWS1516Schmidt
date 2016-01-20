# MongoDB Example Server

## Installation
1. Install Homebrew. You can skip this step if you already have homebrew installed. This assumes that you have ruby available, which most OS X installs should. See http://brew.sh for more information.
4. Download the server app’s dependencies. From the server directory, `npm` will read the `package.json` file and download the dependency tree into `node_modules`.

    
## Run
1. In one terminal process, start Mongo. (assuming standard install):    
   
   
        /usr/local/mongodb/bin/mongod
    
2. Start the app from the server directory. This will start node and run `index.js`.

        node .
    
### The App
The interface is a map with Locations of Interest. To add a location, tap the + button. This will add a tag at the current location. 

The "folder" button allows you to filter the locations by categories.

## Configuration

To change the URL/port:

1. Set the port in `index.js` in the line `app.set('port', process.env.PORT || 3000);`
2. Then change the `kBaseURL` macro in `Locations.m` to point to the new location. 

To point to a non-default localhost mongo:

1. Change the `mongoHost` and `mongoPort` variables in `index.js`.


## Troubleshooting
Pointing a web browser at http://localhost:3000 to see an abbreviated list of saved tags 

## Sys Requirements
* Mac OS X 10.8+
* Xcode 5+
* iOS 7+
    
## Copyright 
Copyright 2013 Michael Katz. All rights reserved. 