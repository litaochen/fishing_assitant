Litao Chen
litao.chen@outlook.com
Aug.04.2017


Work through
Note: this app will use phone camera. You may need to test it on iphone instead of the simulator


+ On the launch
	- the app will try to restore the user's data from disk
	- if not available, will create new data object 
	- if available, later on operations will be based on the restored data


+ Home page
	- Mapview: shows the catch records on the map as annotations,
			   when tapping on the annotation it will show the species you catch there,
			   When you open the app, it will find you location and center the map accordingly
	- Got a fish!: 		a button allows you to add record to the database
	- Suggestions:		a button brings you to the suggestion page
	- Show my Catches:	a button brings you to the table view for all your catches

+ Got a fish page
	- when you come to this page, a default new item will be created for editting
	- the app will turn on the camera automatically to allow you to take a 
	  picture of the catch. 
	- You can cacel the camera. the picture will be the default fish shadow
	- After you take a picture, the app with make a thumbnail of the picture and save it to
	  the record, the picture will appear in the image view
	- you can then set the species, weight and bait
	- the app will perform simple validation on user's input, warning will be given when user
	  input invalid weight or no bait info was provided.

	- when you are doing the editting the first time the record was created, the app quietly 
	  goes to the network to grap the 
	  weather data from two APIs, one for weather, another one for tide
	- Commonly the weather data will be ready in 1 second. When both data are ready, the 
	  useful part of the data will be extracted and stored in the record
	- The app will process the weather data to get the segmented or abstracted conditions for 	future suggestions
	
	- when you cancel the editting, the new default item will be removed and no new record
	  was saved to the database
	- When you save the change, you will be lead to the main page, and the map annotation 
	  will be updated automatically

+ show muy catches page:
	- list all your records in table view in two sections, one for freshwater and one 
	  for saltwater
	- each record will show you the picture, the date, the weather summary, the weight and bait
	 - At the bottom you have three options:
	     -> sort by date
	     -> sort by weight
	     -> sort by species
	 - tap the bar item, the order of the records will be updated accordingly
	 - tapping the record will bring you to the detail editting page
	 - the detail editting page will show you the current value of the record, you can change it as you want
	 - any changes you saved will be reflected on the table list in real time
	 - left swipe will allow you to delete the record. The view will update in real time

+ suggestion page:
	- when you come to this page, the app will analyze all you stored record and find out the 
	  most frequent conditions accross your records, like the best temp rage, tide range and so
	  on.
	- the more data in the database, the more accurate the suggestions are.


