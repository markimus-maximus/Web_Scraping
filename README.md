# Web_Scraping

This file contains a class for web scraping. Within this class are functions for web scraping tasks with Selenium, such as scrolling web pages, logging into a website, diverting cookies, closing push notification message. Additionally, there is a function for creating a range of dates as strings with which to concatenate to a url as a permalink. This way, you can generate a list of urls relating to dates of your choosing. More spcific information is in the below function list. 


Function list:

`webdriver_init(self, url)`

This function takes url as a parameter and initialises `selenium` web driver, then requesting the url from chrome. After request, the sleep funtion waits for 2 seconds to avoid looking like a bot. This method streamlines the other methods below since most methods required these lines of code. This method should be called first. 


`cookies_bypass(self, XPath)`

This function takes an XPath as a parameter in order to specify which button to click to bypass cookies. In principle this function could be used to specify and button which precludes reaching the requested webpage. With the required button XPath, the find_elemnet and click functions of the driver class are used to find and click the button, respectively. 

`auto_login(self, email_address, password)`

This function takes email address and passowrd as parameters and iteratively requests user XPath inputs in order to designate which buttons to click to proceed through the log in process. The find_element, click functions and send_keys of the driver class are used to select button, click button and send username/password, repsectively. 

`scroll_page(self, x, y)`

This function takes x,y coordinates as parameters in order to scroll to a certain location on the page. To achive this, the execute_script function of the driver class is used. 



`maximise_window(self)`

This method maximised the window, which may allow .click method to access otherwise hidden buttons.

`bypass_initial_popup(self)`

Bypasses a popup which can appear before the website is accessed. This method uses ChromeOptions function of the webdriver class to specify to click not to allow notifications. 
