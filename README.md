# SpaceBot
Discord bot that uses the NASA public API to send pretty pictures of space

Currently sends a space picture to a channel named #photography at the following times in GMT: 03:00, 14:00 18:00

Basic documentation:
sb-daily yyyy-mm-dd

	Date format should be yyyy-mm-dd, eg: 2020-01-01
	Date will default to today if no argument is given

sb-earth
	
	Sends the most recent picture of the earth in HD
	No arguments required

sb-search -Title-Description
	
	Sends the most relevent image based on search terms.
	eg sb-search -Nebula-Purple
  Please not that this bot is not intened for searching, thus this function rarely gives what expected or works at all

sb-rover camera_date
	
	Sends a picture from the curiosity rover on Mars
	Possible arguments for camera: fhaz,rhaz,mast,chemcam,navcam,random
	Date format should be yyyy-mm-dd, eg: 2020-01-01
	Date will default to yesterday if no argument is given. This is to prevent any errors to do with no images
	This is now recursive to prevent issues with there being no image, and will create a random date until it finds a picture.

The difference between spaceLibs and spaceLibsOLD is that with spaceLibs,
it only returns the link to the pic of the day,
not the image path, making it faster when an embed will work just fine. It downloads the others still, because those are usually not too big
SpaceLibsOLD has a slightly different place where it saves images to the new one,
becasue linux wasn't happy about where the ".sh" file I was using to start the bots was.
