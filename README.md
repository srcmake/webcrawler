# Python Web Crawler Project

This Python project aims to find all valid webpages on a website given a starting url. 

Said another way, we'd like all webpages that can be found on a website if we start on the home page. This program will find all of those urls, and output them to a file.

# Code Logic

0. Create a hashmap for all visited urls. 
0. Create a queue for urls that we need to check.
0. Create a list of valid urls (to output later).
1. Receive input (of the first url).
2. Add that url to our check queue.

3. While our check queue is not empty...
	4. If the url was not visited already...
		5. Mark it as visited (by adding it to our hashmap).
		6. Download the html of the webpage.
		7. Parse the HTML for all urls (into a list).
		8. For each url in the list...
			9. Check that the url is valid. (Not from another site, or an invalid subdomain).
			10. If that url is valid then...
			11. Add it to the valid url list.
			12. Add it to the queue (if the url wasn't visited already).
			
13. Sort the list of valid urls.
14. Write that list to a file.

# Copyright

The copyright belongs to www.srcmake.com 2018. Feel free to use or modify the code. This is just a fun little project. 