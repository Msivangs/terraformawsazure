# Selenium


Selenium Introduction

What is Selenium:
1. Selenium is open Source testing tool.
2. It is exclusively for web based applications.
3. Selenium supports multiple browsers - Chrome, Firefox, Internet Explorer, Safari
4. Selenium Works with multiple platforms - Windows, Mac, Linux.
5. Selenium Can be coded in multiple languages - Java, C#, Python, JavaScript, PHP, Ruby.
6. Differences between Selenium and WebDriver.

Selenium WebDriver:
If you want to create robust, browser-based regression automation suites and tests, scale and distribute scripts across many environments, then you want to use Selenium WebDriver, a collection of language specific bindings to drive a browser - the way it is meant to be driven.

WebDriver: 
	•	WebDriver is designed as a simple and more concise programming interface.
	•	WebDriver is a compact object-oriented API.
	•	It drives the browser effectively.

Selenium WebDriver Architecture: ￼

	•	After you trigger the test, complete selenium code(Client) which we have written will be converted to Json format.
	•	Generated Json is sent to browser driver (Server) through http protocol. 
	•	         Note: Each browser contains a separate browser driver.
	•	Browser drivers communicate with its respective browser and executes the commands by interpreting Json which it received on the browser.
	•	Browser Driver receives responses back from the browser and it sends Json response back to Client.


Complete Installation Guide for Java and Selenium Learning

1. Download Java from below link

http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html

2. Setting JAVA_HOME path in MAC OS X 

	•	Open Terminal and run the below commands to setup the path
	•	vim ~/.bash_profile
	•	export JAVA_HOME=$(/usr/libexec/java_home)
	•	Hit Esc and then :wq  and then ENTER
	•	source ~/.bash_profile
	•	echo $JAVA_HOME

3. Eclipse Installation:

Link for Selenium official Site : http://www.seleniumhq.org

SeleniumHistory:
Selenium came into existence in 2004 when  GUY named Jason Huggins was testing an internal application at ThoughtWorks.
Selenium is a set of different software tools each with a different approach to supporting test automation.
1.1 Selenium Components:
 Selenium IDE
Selenium Remote Control
Selenium WebDriver
 Selenium Grid
Lets have a look on each of these components:
 Selenium IDE
Selenium IDE is a complete integrated development environment (IDE) for Selenium tests. It is implemented as a Firefox extension, and allows recording, editing, and debugging tests. It was previously known as Selenium Recorder.
Scripts are recorded in Selenese, a special test scripting language for Selenium. Selenese provides commands for performing actions in a browser (click a link, select an option), and for retrieving data from the resulting pages.
It is not only just play back tool, It can records user actions as they are performed and then exports them as reusable script in one of many programming languages that can be later executed.

Drawbacks:
As it will come with only Firefox addin.What if you want to test your application which works only in Internet explorer or some any other browser?
Selenium IDE is not suitable when you want to built a robust frameworks.
Selenium IDE doesn’t provide iteration or conditional statements for test scripts.

Selenium Rc(Selenium 1.0)
Selenium RC was first component in the market which control a browser from a language of your choice. The underlying functionality of Selenium Remote Control is that it uses  Javascript library(Selenium core) that could drive interactions with the page, allows us to automatically rerun tests against multiple browsers.
Selenium RC Architecture
There is a selenium-RC server which acts as proxy between our Driver code and Application under Test
 The client/driver establishes a connection with the selenium-RC server. 2. Selenium RC server launches a browser (or reuses an old one) with a URL that injects Selenium-Core’s JavaScript into the browser-loaded web page. 3. The client-driver passes a Selenese command to the server. 4. The Server interprets the command and then triggers the corresponding JavaScript execution to execute that command within the browser. 5. Selenium-Core instructs the browser to act on that first instruction, typically opening a page of the AUT. 6. The browser receives the open request and asks for the website’s content from the Selenium RC server (set as the HTTP proxy for the browser to use). 7. Selenium RC server communicates with the Web server asking for the page and once it receives it, it sends the page to the browser masking the origin to look like the page comes from the same server as Selenium-Core (this allows Selenium-Core to comply with the Same Origin Policy). 8. The browser receives the web page and renders it in the frame/window reserved for it


drawbacks.
 As it is entirely use JavaScript to talk to browser, it leads to significant weakness. Every browser impose very strict security rules on the JavaScript being executed to protect the users from malicious scripts
There is no support for Android and IOS Platform
Server need to be started every time to run a program.
Lot of Limitations when a Application has Rich API with dynamic elements
Native keyboard and mouse events cannot be handled in efficient manner


Webdriver:(Selenium 2.0)
This brand new automation tool provides all sorts of features, including a more cohesive and object oriented API as well as an answer to the limitations of the old implementation.It supports the WebDriver API  underlying technology,along with the Selenium underlying technology,
The architecture of Selenium Webdriver is entirely different from RC.Unlike RC there is no proxy server betweenAUT and Code.
It makes direct calls to browser native API to get the things executed.Unlike RC it does not Use any proxy server to talk to browser. WebDriver uses the most appropriate way to access the browser API. If we look at Firefox, it uses JavaScript to access the API. If we look at Internet Explorer, it uses C++. That means that it sometimes needs direct help from browser development team,By this approach we can control browsers in the best possible way but has the downside that new browsers entering the market will not be supported straight away like we can with RC
As Webdriver directly talks with browser we can overcome the limitations of JavaScript security model which we have face with Selenium Core in RC
Selenium-WebDriver supports the following browsers along with the operating systems these browsers
are compatible with.
• Google Chrome 12.0.712.0+
• Internet Explorer 6, 7, 8, 9 - 32 and 64-bit where applicable
• Firefox 3.0, 3.5, 3.6, 4.0, 5.0, 6, 7
• Opera 11.5+
• HtmlUnit 2.9
• Android – 2.3+ for phones and tablets (devices & emulators)
• iOS 3+ for phones (devices & emulators) and 3.2+ for tablets (devices & emulators)
Languages on which Webdriver Supports:
Java,
 Javascript,
Ruby,
 PHP,
 Python,
 Perl 
 C#
You can use any of the above language to Automate application.There is nothing rule like as your website is built with C#,so you have to use only C# code in Webdriver to automate your application.The language you write your code is Application independent.
Why Webdriver??
In addition, Selenium 2 still runs Selenium 1’s Selenium RC interface for backwards compatibility
No server required to start.
No support for Android and Iphone platform in RC
Can Handle rich API 
Can handle Mouse movements
It directly talks to browser. unlike RC it does not use any proxy server
It supports all the Latest Versions of Firefox
All future enhancements can be done in Webdriver only.
 Selenium Grid
 Selenium Grid allows you to run your tests in parallel, that is,different tests can be run at the same time on different remote machines. s. Also, if you must run your test suite on multiple environments you can have different remote machines supporting and running your tests in them at the same time. In each case Selenium Grid greatly improves the time it takes to run your suite by making use of parallel processing

4. Selenium Project Creation:

	•	Project is nothing but a test suite, which can store collection of test cases.
	•	Under the test suite we need to define the test cases, which are nothing but each java class file is represented as one selenium test case.

	•	5. Selenium jars download:
	•	
	•	https://www.selenium.dev/downloads/ 
	•	
	•	
	•	6. Configure downloaded selenium jars in project build path.
	•	
	•	Right click on Project —> Select Properties—> Select Java build path —>Select add external jars —> Add all downloaded jars and jars from lib file also.
	•	
	•	7. Choose browsers to run and download version depends on your chrome, Firefox browsers version.
	•	
	•	https://www.selenium.dev/downloads/
	•	
	•	      webdriver.chrome.driver
	•	
	•	Similar way we can choose the Firefox browser by repeating the step7.
	•	
	•	      Web driver.gecko.driver
	•	
	•	The other important changes in Selenium 3.x are listed below:
	•	
	•	* Minimum java version is now 8+(Kindly use Java 8 lates and Selenium 3 to avoid this issue.)
	•	
	•	* The original RC APIs are only available via the leg-rc package.
	•	
	•	* To run exported IDE tests, ensure that the leg-rc package is on the classpath.
	•	
	•	* Support for Firefox is via Mozilla's geckodriver.
	•	* Support for Edge is provided by MS:
	•	* Official support for IE requires version 9 or above
	•	* New html-table runner backed by WebDriver.
	•	* Unused command line arguments are now no longer parsed.
	•	
	•	Geckodriver for firefox...
	•	*******************************
	•	When you are using Selenium 3 releases, you have to download geckodriver to run your test on firefox browser. Just like the other drivers(chromedriver/iedriver) available to Selenium, Mozilla has released geckodriver executable that will run alongside the firefox browser. Firefox version 48 & above will use geckodriver.
	•	
	•	If you want to work with Firefox you have to set the property now.  You can download geckodriver from Github and then you can extract and you will get .exe file. https://github.com/mozilla/geckodriver/releases/
	•	
	•	You can place it on C:\\ and use as below - 
	•	
	•	Sample Code:-
	•	System.setProperty("webdriver.gecko.driverî,îC:\\geckodriver.exe");
	•	WebDriver driver = new FirefoxDriver();
	•	driver.get("http://www.google.com");
	•	driver.quit();

WebDriver Java Concepts

	•	Interface:
	•	A Java interface defines a set of methods but does not implement them. A class that implements the interface agrees to implement all of the methods defined in the interface.
	•	Webdriver is the Interface
	•	All Known Implementing Classes:
	•	AndroidDriver, AndroidWebDriver, ChromeDriver, EventFiringWebDriver, FirefoxDriver, HtmlUnitDriver, InternetExplorerDriver,IPhoneDriver, IPhoneSimulatorDriver, RemoteWebDriver, SafariDriver
	•	Steps for Creating class object with reference to interface
	•	1.	Choose the Browse on which you want to perform 
	•	Automation and Select the respective class to implement Webdriver
	•	Ex: FirefoxDriver()
	•	2. Create an object for the Class and assign name to it
	•	Selenium=New FirefoxDriver();
	•	3.Then make Class object reference to the Webdriver 
	•	Interface which you want to implement
	•	Webdriver Selenium=New FirefoxDriver();
	•	Basis methods of Webdriver:
	•	Get();
	•	Load a new web page in the current browser window.
	•	getCurentURL();
	•	 Get a string representing the current URL that the browser is looking at.
	•	getTitle()
	•	 The title of the current page
	•	getPageSource()
	•	Get the source of the last loaded page.
	•	Quit();
	•	Quits this driver, closing every associated window.
	•	Close();
	•	Close the current window, quitting the browser if it's the last     window currently open.
                              Locator Techniques and Tools used identify objects
Tools for identifying elements :

Installing Firebug, Firepath       ñ Firefox
Chrome Inspector                   GoogleChrome
F 12                               Internet Explorer

Firebug Download Links
https://addons.mozilla.org/en-US/firefox/addon/firebug/
FirePath download
https://addons.mozilla.org/en-US/firefox/addon/firepath/