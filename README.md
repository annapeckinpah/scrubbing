# Forum Scrubbing
Performing scraping with Selenium Chromedriver

Script for scraping sub-forums on https://www.nissanclub.com/ using...
Homepage URL: https://www.nissanclub.com/
Tools: Selenium, ChromeDriver
Data Organizer: Pandas

Version: 2.1
Date Created: 01/30/2019
Last Modified: 02/26/2019
#####################################################################################

#####################################################################################

ABOUT V2:

1. Separated a) opening Chrome Driver and b) attempt to open URL
   into two sections to allow faster URL change.
2. Added column "Thread Title" to output, which is a string  
   containing the title of the thread the post belongs to.

ABOUT V2-1:

1. Added lines that will add a custom comment ID for each Reddit comment scraped
   for a project. It will be contained in the "My Comment ID" column of the
   Pandas data frame.

#####################################################################################

#####################################################################################

READ ME!!!

This script is able to scrape sub-forums on https://www.nissanclub.com/,
using Selenium and ChromeDriver to navigate through multiple pages on the sub-forum
and the Pandas package to organize the data to output a .csv file.

YOU NEED THESE INSTALLED:
1. Python ver. 3.x
2. Selenium
3. Chromedriver
4. Pandas (a Python package)

#####################################################################################

CODE OVERVIEW -- This script...

1. Sets up the ChromeDriver to open a new Chrome browser window.
2. Navigates to the given URL, which should be the 1st page of a sub-forum on
   https://www.nissanclub.com/
3. Obtains each post data on the 1st page and adds the data to a global list.
4. Clicks on an arrow to open a "Go to Page" pop-up box.
5. Inputs the next page number into the text box and hits ENTER as a key.
6. Loads the next page and obtains each post data on that page.
7. Steps 4-6 are repeated for all consequent pages.
8. Makes a data frame using Pandas with the obtained post data.
9. Outputs a .csv file containing the post data.

#####################################################################################

A FEW WARNINGS...

Once chromedriver starts, please put the window on another desktop monitor or
such that your mouse will NOT hover over the page. It is important to NOT let
your mouse hover over the page while the script is navigating to the other pages
on the sub-forum, as the "Go to Page" pop-up dialog box may disappear if you
hover over something else, interfering with page number input into the text box.
If your mouse DOES hover over the page and the next page does not load as
expected, please restart the script from the beginning to obtain accurate results.

This site contains many ads and may have trouble fully loading the page within
a considerable amount of time, thus, a timeout is in place to allow the code to
move on without waiting for the page to load all of its contents.
As a result, the terminal will print error messages regarding the timeout, but
please disregard them, as it is simply a sign that the code is moving on
in this script.

This script may not work as expected on every try due to Internet connectivity
and other loading errors, so it is vital that the user pays attention to the
chromedriver window and terminal outputs (print statements) as the code is running.

#####################################################################################


