# [Sonalysis.net](http://www.sonalysis.net/) Music Recommender

## Team Members:
- Andrew Cho
- Holland Delany
- Meredith Latasa
- William Whitehead

<br />

## 1. Description of functionality
This app serves as an interactive resource for finding information about music and discovering new music.Users are able to search a subset of Spotify's catalogue and find song recommendations based on dynamic custom algorithm that takes into account user preferences on a number of musical attributes.

#### Browse page: 
- Presents an abbreviated set of genres and song traits, which when selected, populate groupings of top albums based on Album of the Year data.

![Browse](readme/explore.gif)


#### Search page:
- Returns results for keywords that represent either a song name, an album name, or an artist name. Exact matches, LIKE matches, and fuzzy matches are given back to the user in order of relevancy.

![Search](readme/search.gif)


#### Recommendations page:
- Available to the users after an item is accessed from Search results. Users are able to manipulate the attributes that are submitted to the recommendation algorithm based on their preferences. They can also choose which attributes the algorithm should include or disregard. 

![Recommendation](readme/recommendation.gif)


#### Modals:
- Can be accessed across the application and offer information about songs, albums, and artists. They allow the user to play song snippets, view album art, and see relevant attributes & statistics. 

<br />

## 2. Instructions for building it locally 


#### To run the server:

- Create a server.json file in server/config modeled on server-template.json file.  Request the database password from an administrator.

- From the server directory, run 'npm install' to install dependencies.

- To run the server, use the command 'npm run watch'.


#### To run the client:

- Create a client.json file in client/config modeled on client-template.json file.  Replace any psswords necessary.

- From the client directory, run 'npm install' to install dependencies.

- To start the client, use the command 'npm start'.

- In the browser, navigate to http://localhost:8080/

- Hot reloading is enabled


<br />

## 3. Architecture

####  Client:
-  ReactJS application utilizing the Material-UI library for the user interface design.

####  Server:
-  Express Node.js application (deployed to AWS Lambda and API Gateway in production).

####  Database:
- MySQL database hosted by AWS RDS server. The seed datasets created in Python Jupyter notebook were uploaded to AWS RDS via MySQL Workbench. 

####  Artist & Album Artwork Service:
-  A Python script that integrates with the Spotify API and deployed to an AWS Lambda and API Gateway.
