# SAMMI-YouTube-Link-Handler
- Originally is an extension call "YouTube Video Duration" by Christina K.
- Specially modified/enhanced for the purpose of use by myself and/or Epi's LB2 gang
- Ported to ~~LB2~~ SAMMI

what this extension do ?  
Pass a youtube link to extension, and it will return 4 variable for you. 
1. Extract Youtube's VideoID from link
2. Return "Left Over" duration in milliseconds
   - if t= params not detect in url link, return full video duration.
   - if t= params is detected in url link,  return "Left Over" duration by using full video length minus starting second from t= params.
3. Check if Video is having some restriction by checking :
   - Is embeddable
   - Is require Age Verify (18+)
   - Is restricted on your country
   - Is a live stream
4. (Optional) Return YouTube video's title
   - select language code (HL) for capture other title language if available
   
enable Debug if extension is not function correctly for view more info

Briefing of the Extension Command field
```
String - Link : The YouTube URL Link that pass to extension.
Can be fixed URL link or from a variable

String - Country Code : Country code for check on video restriction. 
Example: MY for Malaysia. Check on transmitter for country code.

Variable - VideoID : Variable to store the unique YouTube ID that was returned.
Example if String - Link = https://www.youtube.com/watch?v=KaqC5FnvAEc , will return as KaqC5FnvAEc
Support link with timestamp like https://www.youtube.com/watch?v=KaqC5FnvAEc&t=12s , will return as KaqC5FnvAEc&t=12

Variable - Duration : Variable to store the left over video duration (in milliseconds) that was returned via the YouTube API.
Works with videos with ?t= on the URL.
Example if &t=12s and the total video duration is 60sec, will return as 48000.

Variable Restricted : Variable to store the value if the video has age/country/livestream/embedded on third party website's restrictions.
If return as 0 mean video is assumed safe to view on stream,
will return 1/2/3/4 depending on how many restrictions found.
```
v3.2 New Extension Commands
```
Enable - HL : Tick for make API return localized Video Title base on String - HL Code

String - HL Code : Language code, check it on Transmitter for language that YouTube supported.

Enable - Title : Tick for extension return Video Title as variable

Variable - Title : Variable to store the video's Title
```
----

Original Message by Christinna K: 

# LB-YouTube-Duration
 Retrieve duration of any YouTube video in milliseconds.

[![](https://github.com/christinna9031/LioranBoard-Files/blob/main/img/paypal.png?raw=true)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=3YWXYQE3HKWHQ)

DISCLAIMER: The extension is provided as is. The developer has no obligation to provide maintenance and support services or handle any bug reports.
Feel free to edit the extension for your own use. You may not distribute, sell or publish it without the author’s permission.
