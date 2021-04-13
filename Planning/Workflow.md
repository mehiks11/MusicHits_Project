## **Data Lists:**
**Data needed:**
* Song name
* Artist
* Artist followers on spotify
* Artist monthly listeners
* Peak Ranking 
* Week of peak ranking (less important)
* Genre
* Length
* Key
* BPM
* Record Label

**Dataset will include:**
* Song name
* Artist
* Artist followers on spotify
* Artist monthly listeners
* Peak Ranking 
* Genre
* Length
* Key
* BPM
* Major Record Label or No?


**Fit on:**
* Artist followers on spotify
* Artist monthly listeners
* Peak Ranking 
* Genre
* Length
* Key
* BPM
* Major Record Label or No?

**Location of each metric online + Scraping Method:**

*Billboard:* [Beautifulsoup + Selenium]
* Song name 
* Artist
* Peak Ranking 

*Wikipedia:* [Beautifulsoup + Selenium]
* Genre
* Length
* Record Label

*Spotify:* [Spotify API]
* Artist followers on spotify
* Artist monthly listeners

*Notediscover:* [Beautifulsoup + Selenium]
* Key
* BPM



## **WorkFlow:**
### Obtaining the Data into a dataframe
1. Scrape ten? weeks of songs with a month of time in between from **billboard**. (~2500 data points)
    * Obtain: *Song name, Artist, Peak Ranking*
2. Create a data frame with Song name, Artist, Peak Ranking
3. Create a list of song names for iteration
4. Create a function that generically grabs *genre, length*, and *record label* from **wikipedia** and appends that dictionary with those values onto a list
5. Use selenium to search every song name from the song list on **wikipedia** with the author name, click the first link, and run the above function 
7. Create a function that generically grabs *key* and *BPM* from **notediscover**
8. Use selenium to search every song name from song list on google search + notediscover, click on first link, and run above function
9. Merge the above three lists with the values on song name for your dataset with song attributes
10. Figure out how to work Spotify API and add further instructions below
11. 


