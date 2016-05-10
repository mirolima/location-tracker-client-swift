# Location Tracker

The Location Tracker app is an iOS app developed in Swift to be used in conjunction with the [Location Tracker Server](https://github.com/ibm-cds-labs/location-tracker-server-nodejs).

## How it works

The Location Tracker app supports offline-first, Cloudant Sync, and is implemented on a database-per-user architecture. When a user registers, a specific database is created for that user and is used to track only that user's locations. In addition, the server configures continuous replication for each user-specific database into a consolidated database where all locations can be queried (location_tracker_all). See the architecture diagram below for more information.

### Architecture Diagram

![Architecture of Location Tracker](http://developer.ibm.com/clouddataservices/wp-content/uploads/sites/47/2016/05/locationTracker2ArchDiagram1Sm.png)

## Running with Xcode

Get the project and change into the project directory:

    $ git clone https://github.com/ibm-cds-labs/location-tracker-client-swift.git
    $ cd location-tracker-client-swift

1. Install the project's dependencies:

    $ pod install


2. Open the workspace in Xcode
3. Open AppConstants.swift
4. Change the baseUrl to point to your Location Tracker Server running on Bluemix

## License

Licensed under the [Apache License, Version 2.0](LICENSE.txt).
