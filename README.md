# LB2-YouTube-Link-Handler
- Originally is an extension call "YouTube Video Duration" by Christina K.
- Specially modified/enhanced for the purpose of use by myself and/or Epi's LB2 gang
- Ported to LB2

what this extension do ?  
Pass a youtube link to extension, and it will return 3 variable for you. 
1. Extract Youtube's VideoID from link
2. Return "Left Over" duration in milliseconds
   - if t= params not detect in url link, return full video duration.
   - if t= params is detected in url link,  return "Left Over" duration by using full video length minus starting second from t= params.
3. Check if Video is having some restriction by checking :
   - Is embeddable
   - Is require Age Verify (18+)
   - Is restricted on your country
   - Is a live stream
   
enable Debug if extension is not function correctly for view more info

----

Original Message by Christinna K: 

# LB-YouTube-Duration
 Retrieve duration of any YouTube video in milliseconds.

[![](https://github.com/christinna9031/LioranBoard-Files/blob/main/img/paypal.png?raw=true)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=3YWXYQE3HKWHQ)

DISCLAIMER: The extension is provided as is. The developer has no obligation to provide maintenance and support services or handle any bug reports.
Feel free to edit the extension for your own use. You may not distribute, sell or publish it without the author’s permission.