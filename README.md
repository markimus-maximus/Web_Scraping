# Web_Scraping

This file contains a class for web scraping. Within this class are functions for web scraping tasks with Selenium, such as scrolling web pages, logging into a website, diverting cookies, closing push notification message. Additionally, there is a function for creating a range of dates as strings with which to concatenate to a url as a permalink. This way, you can generate a list of urls relating to dates of your choosing. More spcific information is in the below function list. 

Function list:

webdriver_init: 

This function takes url as a parameter and initialises selenium web driver, then requesting the url from chrome. After request, the sleep funtion waits for 2 seconds to avoid looking like a bot. This method streamlines the other methods below since most methods required these lines of code. This method should be called first. 

daterange: 

This function  takes start and end dates and uses the datetime class to to generate iterative daily dates between the 2 given dates, in the format yyyy/mm/dd. The function then puts each of the dates into a list and returns this list as list_dates.

create_url_list_with_date_permalinks

This function takes a list of permalinks (for example a list of dates) and a url with which to concatenate the url and output as a list. This list of concatenated urls then provide the bases to iteratively request urls for scraping multiple pages. 

cookies_bypass

This function takes an XPath as a parameter in order to specify which button to click to bypass cookies. In principle this function could be used to specify and button which precludes reaching the requested webpage. With the required button XPath, the find_elemnet and click functions of the driver class are used to find and click the button, respectively. 

auto_login

This function takes email address and passowrd as parameters and iteratively requests user XPath inputs in order to designate which buttons to click to proceed through the log in process. The find_element, click functions and send_keys of the driver class are used to select button, click button and send username/password, repsectively. 

scroll_page

This function takes x,y coordinates as parameters in order to scroll to a certain location on the page. To achive this, the execute_script function of the driver class is used. 

click_notifications

This method uses ChromeOptions function of the webdriver class to specify to click not to allow notifications. 

There are methods which scrape coin market cap website. This website was chosen because there are vast and rich cryptocurrency data which can be used to characterise past market movements and analyse trends. There is a function 
