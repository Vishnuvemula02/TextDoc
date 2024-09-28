My new project 1 
Automation testing 
importent topices whichic i can praper for software testing interview
15_jun_2024

String Class Methods

	.toLowerCase()
	.toUpperCase()
	.length()
	.equals()
	.equalsIgnoreCase()
	.contains()
	.charAt()
	.subString()
	.compareTo()
---------------------------------------------------------------------------------------------------------- 
Converting a String to LowerCase and UpperCase
---------------------------------------------------------------------------------------------------------
		
		String course = "Java";
		
		System.out.println(course.toLowerCase());
		System.out.println(course.toUpperCase());
---------------------------------------------------------------------------------------------------------
Couting No. of chars in a String using : length()
---------------------------------------------------------------------------------------------------------
		
		String course = "Java";		
		
		int count = course.length();
		System.out.println(count);

-------------------------------------------------------------------------------------------------------
Capturing a character present at specified index using : charAt()
-------------------------------------------------------------------------------------------------------

		String course = "Java";		
		
		char x = course.charAt(0);
		System.out.println(x);
		
		char y = course.charAt(3);
		System.out.println(y);
--------------------------------------------------------------------------------------------------------
Capturing a part of a String using : subString()
--------------------------------------------------------------------------------------------------------
		
		String course = "Selenium Java";		
		String str = course.substring(9);
		System.out.println(str);

-----------------------------------------------------------------------------------------------------------
Capturing a part of a String using : subString()
-----------------------------------------------------------------------------------------------------------
		
		String course = "Selenium Java";		
		String str = course.substring(9, 11);
		System.out.println(str);
---------------------------------------------------------------------------------------------------------
Comparing Two Strings using : equals()
---------------------------------------------------------------------------------------------------------
		
		String pword = "QEdge";
		String cpword = "qedge";
		
		boolean res = pword.equals(cpword);
		System.out.println(res);

output : false
---------------------------------------------------------------------------------------------------------
Comparing Two String using : equalsIgnoreCase()
---------------------------------------------------------------------------------------------------------
		
		String exptitle = "google images";
		String acttitle = "Google Images";
		
		boolean res = exptitle.equalsIgnoreCase(acttitle);
		System.out.println(res);
-------------------------------------------------------------------------------------------------------
contains()
-------------------------------------------------------------------------------------------------------
		
		String pgtitle = "Welcome to Google Cloud";
				
		boolean res = pgtitle.contains("Google");
		System.out.println(res);

output : true
--------------------------------------------------------------------------------------------------------
cotains()
--------------------------------------------------------------------------------------------------------
		String pgtitle = "Welcome to Google Cloud";
				
		boolean res = pgtitle.toLowerCase().contains("google");
		System.out.println(res);
---------------------------------------------------------------------------------------------------------

18_jun_2024
---------------------------------------------------------------------------------------------------------

compareTo()
-------------------------------------------------------------------------------------
		
		String str1,str2;
		
		str1 = "A";
		str2 = "A";		
		System.out.println(str2.compareTo(str1));
		
		str1 = "A";
		str2 = "B";		
		System.out.println(str2.compareTo(str1));
		
		str1 = "B";
		str2 = "A";		
		System.out.println(str2.compareTo(str1));
------------------------------------------------------------------------------------
Declaring Arrays
------------------------------------------------------------------------------------

	datatype[] array_var = {val1,val2,...valn};
-------------------------------------------------------------------------------------
counting no of elements in a array using : length
-------------------------------------------------------------------------------------	
		int[] x = {10,20,30,40};	
		int count =x.length;
		System.out.println(count);
--------------------------------------------------------------------------------------
Accessing elements present in a array using: array[index]
------------------------------------------------------------------------------------
		int[] x = {10,20,30,40};	
		System.out.println(x[0]);
		System.out.println(x[1]);
		System.out.println(x[2]);
		System.out.println(x[3]);
-------------------------------------------------------------------------------------
Replacing an existing element using: array[index]=newvalue
------------------------------------------------------------------------------------
		int[] x = {10,20,30,40};		
		x[0]=50;
		System.out.println(x[0]);
-------------------------------------------------------------------------------------
19_jun_2024

Array:
-------------------------------------------------------------------------------------
		String[] cars = {"Car1","Car2","Car3","Car4"};
		
		int count = cars.length;
		System.out.println(count);
		System.out.println(cars[0]);
		System.out.println(cars[3]);
		
		cars[3]="New Car";
		System.out.println("After replacing");
		System.out.println(cars[3]);
-------------------------------------------------------------------------------------
		Object[] empdata = {"E001","Richads",25,'M',45000.99,true};
		
		System.out.println(empdata.length);
		System.out.println(empdata[0]);
		System.out.println(empdata[1]);
		System.out.println(empdata[2]);
		System.out.println(empdata[3]);
		System.out.println(empdata[4]);
		System.out.println(empdata[5]);
--------------------------------------------------------------------------------------
ArrayList: It is a resizable array can be use to store as many values as you needed.
	   arraylist accept only non-primitive datatypes.

Syntax of creating a ArrayList:

			ArrayList<ref_datatype> alist = new ArrayList<>();
			
Adding elements into ArrayList using: add()
syntax:

	alist.add(element);

Counting no of elements using: size()
syntax:
	alist.size();
	
Removing elements from arraylist using: remove()
syntax:
	alist.remove(index);		

Replacing an existing element using: set()
syntax:
	alist.set(index,element);
-------------------------------------------------------------------------------------
ArrayList:
-------------------------------------------------------------------------------------
		ArrayList<String> carlist = new ArrayList<String>();
		// Adding Elements
		carlist.add("AUDI");
		carlist.add("BMW");
		carlist.add("VOLVO");
		carlist.add("HONDA");
		
		// counting elements
		int count = carlist.size();
		System.out.println(count);
		
		//Accessing elements
		System.out.println(carlist.get(0));
		System.out.println(carlist.get(3));
		
		// removing elements
		carlist.remove(0);
		
		System.out.println(carlist.size());
		
		System.out.println(carlist.get(0));
		
		// replacing elements
		carlist.set(0,"BMW X1");
		System.out.println(carlist.get(0));
--------------------------------------------------------------------------------------	
22_jun_2024

nested if:
syntax:	
	if(condition_1)
		{
		statements;
		}else if(condition_2)
		{
		statements;
		}else if...
-----------------------------------------------------------------------------------
			int a,b;
			a=100;
			b=500;
			
			if(a!=b)
			{
				if(a>b)
				{
					System.out.println("a is big");
				}else
				{
					System.out.println("b is big");
				}
			}else
			{
				System.out.println("Both are equal");
			}


------------------------------------------------------------------------------------
			String ccode = "s";
			
			if(ccode.equalsIgnoreCase("j"))
			{
				System.out.println("JAVA");
			}else if(ccode.equalsIgnoreCase("p"))
			{
				System.out.println("PYTHON");
			}else if(ccode.equalsIgnoreCase("t"))
			{
				System.out.println("TESTING");
			}else
			{
				System.out.println("Course does not exist");
			}

		
-------------------------------------------------------------------------------------
switch case:
>It is use to check multiple possible conditions.We can check multiple conditions using
 nested if. To verify multiple conditions instead of writing a complex nested if 
 better to go with switch case.

syntax:

		switch(variable)
		{
		case 1:
		    statements;
		    break;
		case 2:
		    statements;
		    break;
		case n:
		    statements;
		    break;
		default:
		    statements;
		}

-------------------------------------------------------------------------------------
			String ccode = "t";
			
			switch(ccode.toLowerCase())
			{
			
			case "j":
				System.out.println("JAVA");
				break;
			case "p":
				System.out.println("PYHTON");
				break;
			case "t":
				System.out.println("TESTING");
				break;
			default:
				System.out.println("Course does not exist");
				
			}
-------------------------------------------------------------------------------------
Scanner:
>Java provided Scanner class to read the data from a file also to read the data from a
 console.
>This Scanner class provided 
*nextLine();
*nextInt();
*nextBoolean();
 methods to read the data from java console.
-------------------------------------------------------------------------------------
Reading String data from console:
-------------------------------------------------------------------------------------
			System.out.println("Enter your name:");
			Scanner sc = new Scanner(System.in);
			
		    	String name = sc.nextLine();
		    	System.out.println("Your name is :"+name);
-------------------------------------------------------------------------------------
Reading int data from console
-------------------------------------------------------------------------------------
			System.out.println("Enter your salary:");
			Scanner sc = new Scanner(System.in);
			
			int sal = sc.nextInt();
			
			System.out.println("Your salary is:"+sal);
-------------------------------------------------------------------------------------
Reading boolean data from console
-------------------------------------------------------------------------------------
			System.out.println("Enter your working status:");
			Scanner sc = new Scanner(System.in);
			
			boolean status = sc.nextBoolean();
	
			System.out.println("Status is:"+status);

----------------------------------------------------------------------------------------------
24_jun_2024

Java provided the following looping statements to run the same code repetatively
1)while loop
2)do while loop
3)for loop
4)for each loop
-------------------------------------------------------------------------------------
1)while loop
-------------------------------------------------------------------------------------

			int i =1;
			
			while(i<=10)
			{
				
				System.out.println(i);
				i++;
			}
			 System.out.println("End of the while loop");
-------------------------------------------------------------------------------------
2)do while loop
-------------------------------------------------------------------------------------
		int i =11;
		
		do
		{
			
			System.out.println(i);
			i++;
		}while(i<=10);
		
		 System.out.println("End of the while loop");
-------------------------------------------------------------------------------------
3)for loop
-------------------------------------------------------------------------------------
		for(int i=0;i<3;i++)
		{
		System.out.println(marks[i]);
		}
-------------------------------------------------------------------------------------
A program to print all elements present in array using for loop:
-------------------------------------------------------------------------------------
		int[] marks = {60,70,80,90,100};
		
		for(int i=0;i<marks.length;i++)
		{
			System.out.println(marks[i]);
		}
-------------------------------------------------------------------------------------
4)for each loop
-------------------------------------------------------------------------------------
		int[] marks = {60,70,80,90,100};
		
		for(int data : marks)
		{
			System.out.println(data);
		}

-------------------------------------------------------------------------------------
		List<String> carlist = new ArrayList<String>();
		
		carlist.add("car1");
		carlist.add("car2");
		carlist.add("car3");
		carlist.add("car4");
 		
		for(String car : carlist)
		{
			System.out.println(car);
		}
--------------------------------------------------------------------------------------

25_jun_2024

Selenium browser plugins:
>chromedriver.exe is a plugin for selenium to work with chrome browser.
>geckodriver.exe is a plugin for selenium to work with firefox browser.
>similarly for all the remaining browsers selenium provided corresponding browser 
 plugins.
-------------------------------------------------------------------------------------
script to open chrome browser:
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
-------------------------------------------------------------------------------------
script to open firefox browser:
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.gecko.driver","geckodriver.exe");
		WebDriver driver = new FirefoxDriver();
-------------------------------------------------------------------------------------

26_jun_2024

Deleting browser cookies:
-------------------------------------------------------------------------------------
	driver.manage().deleteAllCookies(); will delete browser history only for the
 current browser session not permanently.
-------------------------------------------------------------------------------------
Accessing Web URL:
-------------------------------------------------------------------------------------
>Selenium webdriver provided get() method to access web application URL.

	driver.get("http://appurl");

		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.get("https://facebook.com");

>We must supply http based url otherwise selenium thows invalid argument exception.
-------------------------------------------------------------------------------------
Accessing web App present in local system:
-------------------------------------------------------------------------------------
	driver.get("file:///filepath");

	driver.get("file:///C:/Users/MAXHUB/Desktop/Sample.html");
-------------------------------------------------------------------------------------
Maximizing the browser window:
-------------------------------------------------------------------------------------
	driver.manage().window().maximize();
-------------------------------------------------------------------------------------
Automating browser navigation:
>Selenium webdriver provided Navigation class this class provided
  navigate().to()
  navigate().back()
  navigate().forward()
  navigate().refresh()  to automate browser navigation.
-------------------------------------------------------------------------------------
Capturing title of a page using : getTitle()
-------------------------------------------------------------------------------------
		driver.get("https://google.com");
		driver.findElement(By.linkText("Sign in")).click();
		String pagetitle= driver.getTitle();
		System.out.println(pagetitle);
-------------------------------------------------------------------------------------

27_jun_2024
Capturing current url of the window using: getCurrentUrl()
-------------------------------------------------------------------------------------
		driver.get("https://google.com");
		driver.findElement(By.linkText("Gmail")).click();
		String pageurl = driver.getCurrentUrl();
		System.out.println(pageurl);
-------------------------------------------------------------------------------------
Closing current browser window using: close()
-------------------------------------------------------------------------------------
		driver.get("https://gmail.com");
		driver.findElement(By.linkText("Help")).click();
		driver.close();
-------------------------------------------------------------------------------------
Closing all browser windows using: quit()
-------------------------------------------------------------------------------------
		driver.get("https://gmail.com");
		driver.findElement(By.linkText("Help")).click();
		driver.quit();
-------------------------------------------------------------------------------------
How selenium identify element or elements present in a webpage:
-------------------------------------------------------------------------------------
>Selenium webdriver provided
			1)findElement()                        
			2)findElements() 
methods to identify elements present in a webpage.

findElement():
>It returns the first webelement matching the given properties. it's returntype is
 WebElement.
-------------------------------------------------------------------------------------
		driver.get("https://amazon.in");
		WebElement element = driver.findElement(By.linkText("Mobiles"));
		element.click();
-------------------------------------------------------------------------------------
		driver.get("https://amazon.in");
		driver.findElement(By.linkText("See more")).click();
-------------------------------------------------------------------------------------
Note:
>If no element matching the given properties selenium throws 
 	"NoSuchElementException".
-------------------------------------------------------------------------------------
findElements():
>It returns a List<WebElement> matching the given properties.

	driver.get("https://amazon.in");
	List<WebElement> links = driver.findElements(By.linkText("See more")); 
	System.out.println(links.size());
-------------------------------------------------------------------------------------
		driver.get("https://google.com");
		List<WebElement> links = driver.findElements(By.tagName("a"));
		System.out.println(links.size());
		links.get(0).click();
_____________________________________________________

1st July 2024


Script for Facebook Login
-------------------------------------------------------------------------------------

		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		
		driver.get("https://facebook.com");
		driver.findElement(By.id("email")).sendKeys("your username");
		driver.findElement(By.id("pass")).sendKeys("your password");
		driver.findElement(By.name("login")).click();
------------------------------------------------------------------------------------
Script for OrangeHRM Login
------------------------------------------------------------------------------------

		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("Qedge123!@#");
		driver.findElement(By.name("Submit")).click();	
		
		driver.findElement(By.partialLinkText("Welcome")).click();		
		driver.findElement(By.linkText("Logout")).click();
		driver.close();

------------------------------------------------------------------------------------------

2_july_2024

Using any property of the element in XPath : Flights Application Login Script
------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		
		driver.get("http://flights.qedgetech.com");
		
		driver.findElement(By.name("email")).sendKeys("sureshbabu.qedge@gmail.com");
		driver.findElement(By.name("password")).sendKeys("demo");
		driver.findElement(By.xpath("//button[@type='submit']")).click();
--------------------------------------------------------------------------------------
Using any property of the element in XPath :
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		
		driver.get("http://google.com");
		driver.findElement(By.xpath("//*[@aria-label='Google apps']")).click();
---------------------------------------------------------------------------------------
Using multiple properties in XPath
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com");
		driver.findElement(By.name("email")).sendKeys("sureshbabu.qedge@gmail.com");
		driver.findElement(By.name("password")).sendKeys("demo");
		driver.findElement(By.xpath("//button[@type='submit']")).click();
		driver.findElement(By.xpath("//input[@name='price_class' and @value='Business']")).click();

-------------------------------------------------------------------------------------------------------------

3_july_2024

XPath : starts-with()
--------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://facebook.com");
		driver.findElement(By.id("email")).sendKeys("demo.qedge@gmail.com");
		driver.findElement(By.id("pass")).sendKeys("Qedge123");
		driver.findElement(By.xpath("//button[starts-with(@id,'u_0_5')]")).click();
---------------------------------------------------------------------------------------
XPath : starts-with()
-------------------------------------------------------------------------------------
System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("Qedge123!@#");
		driver.findElement(By.name("Submit")).click();
		
		driver.findElement(By.linkText("PIM")).click();
		driver.findElement(By.linkText("Employee List")).click();
		
		List<WebElement> chklist = driver.findElements(By.xpath("//input[starts-with(@id,'ohrmList_chkSelectRecord')]"));
		
		for(WebElement element : chklist)
		{
			element.click();
		}
------------------------------------------------------------------------------------
contains()
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");
		
		driver.findElement(By.xpath("//input[contains(@placeholder,'phone')]")).sendKeys("demo");	
------------------------------------------------------------------------------------------
Absolute XPath
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com");
		
		driver.findElement(By.name("email")).sendKeys("sureshbabu.qedge@gmail.com");
		driver.findElement(By.name("password")).sendKeys("demo");
		driver.findElement(By.xpath("//button[@type='submit']")).click();
		
		driver.findElement(By.xpath("/html/body/header/nav/div/div[3]/ul/li[2]/div/a/i")).click();
	
-----------------------------------------------------------------------------------
CSSSelector
-----------------------------------------------------------------------------------

Syntax : tagname[propname='propvalue']		

------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");
		driver.findElement(By.cssSelector("input[name='email']")).sendKeys("demo");
----------------------------------------------------------------------------------

4_july_2024

WebElement Class Methods
-------------------------------------------------------------------------------------
click() : It is used to perform click action on the specified WebElement.

	  WebElement.click();

-------------------------------------------------------------------------------------
sendKeys() : It is used to send data to the specified WebElement.

	  WebElement.sendKeys("data");	   

-------------------------------------------------------------------------------------
clear() : It ised to remove the existing data present in a WebElement.

	  WebElement.clear();

------------------------------------------------------------------------------------
Script to Create New Employee in OrangeHRM Application
------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("Qedge123!@#");
		driver.findElement(By.name("Submit")).click();
		
		driver.findElement(By.linkText("PIM")).click();
		driver.findElement(By.linkText("Add Employee")).click();
		driver.findElement(By.id("firstName")).sendKeys("Veeresh");
		driver.findElement(By.id("lastName")).sendKeys("Kumar");
		
		WebElement element = driver.findElement(By.id("employeeId"));
		element.clear();
		element.sendKeys("2233");
		
		driver.findElement(By.id("btnSave")).click();
------------------------------------------------------------------------------------
getText() : It is used to capture Visible Text of the specified WebElement.Its return 
	    type is String.

	  WebElement.getText();

--------------------------------------------------------------------------------------
getText()
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");
		String msg = driver.findElement(By.className("_8eso")).getText();
		System.out.println(msg);
-----------------------------------------------------------------------------------
getText()
----------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://primusbank.qedgetech.com");
		
		String content = driver.findElement(By.xpath("//table/tbody/tr[2]/td[1]/p[1]")).getText();
		System.out.println(content);
-------------------------------------------------------------------------------------
Script to Print First Link present in Google Page using : getText()
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		List<WebElement> links = driver.findElements(By.tagName("a"));
		
		String firstlink = links.get(0).getText();
		System.out.println(firstlink);
------------------------------------------------------------------------------------
Script to Print First Link present in Google Page using : getText()
------------------------------------------------------------------------------------		
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		String firstlink = driver.findElement(By.tagName("a")).getText();
		System.out.println(firstlink);
----------------------------------------------------------------------------------
Script to print all links present in google page
-----------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		List<WebElement> links = driver.findElements(By.tagName("a"));
		
		System.out.println("Count of Links : "+links.size());
		
		for(WebElement element : links)
		{
			System.out.println(element.getText());
		}
-------------------------------------------------------------------------------------
getAttribute() : It returns specified property value of the element during runtime.


		WebElement.getAttribute("pname");

-------------------------------------------------------------------------------------
getAttribute()
--------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");
		String x = driver.findElement(By.id("email")).getAttribute("placeholder");
		System.out.println(x);
---------------------------------------------------------------------------------------
Script to capture Employee Id generated while adding a New Employee in OrangeHRM App
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("Qedge123!@#");
		driver.findElement(By.name("Submit")).click();
		
		driver.findElement(By.linkText("PIM")).click();
		driver.findElement(By.linkText("Add Employee")).click();
		
		String empid =  driver.findElement(By.id("employeeId")).getAttribute("value");
		System.out.println(empid);

-----------------------------------------------------------------------------------------------------------

9_july_2024


isDisplayed()
-------------------------------------------------------------------------------------

	WebElement.isDisplayed();

------------------------------------------------------------------------------------
Script to check "Sign in" Link is Present in the google.com Home Page or not?
------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		
		String link_tobe_check = "Sign in";
		
		try 
		{
		if(driver.findElement(By.linkText(link_tobe_check)).isDisplayed())
			{
				System.out.println("test pass");
			}
			
		} catch (Exception e) 
		{
			System.out.println("test fail");
		}
------------------------------------------------------------------------------------
Script to check "Sign up" Link is Present in the google.com Home Page or not?
------------------------------------------------------------------------------------

		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		
		String link_tobe_check = "Sign up";
		
		try 
		{
		if(driver.findElement(By.linkText(link_tobe_check)).isDisplayed())
			{
				System.out.println("test pass");
			}
			
		} catch (Exception e) 
		{
			System.out.println("test fail");			
		}
-------------------------------------------------------------------------------------
Script to Check Admin Login Feature in OrangeHRM Application
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("Qedge123!@#");
		driver.findElement(By.name("Submit")).click();
		
		try 
		{
			if(driver.findElement(By.linkText("Admin")).isDisplayed())
			{
				System.out.println("Admin Login Test Pass");
			}
		} catch (Exception e) 
		{
			System.out.println("Admin Login Test Fail");
		}

------------------------------------------------------------------------------------
Script to Check Employee Login Feature in OrangeHRM Application
-----------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Rakesh");
		driver.findElement(By.id("txtPassword")).sendKeys("Rakesh123!@#");
		driver.findElement(By.name("Submit")).click();
		
		try 
		{
			if(driver.findElement(By.linkText("Admin")).isDisplayed())
			{
				System.out.println("Employee Login Test Fail");
			}
			
		} catch (Exception e) 
		{
			System.out.println("Employee Logn Test Pass");
		}
--------------------------------------------------------------------------

10_july_2024

Script to capture all  textboxes present in a page
-------------------------------------------------------------------------------------
System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");
		List<WebElement> editlist = driver.findElements(By.xpath("//input		[@type='text' or @type='password'] "));
		
		System.out.println(editlist.size());
-------------------------------------------------------------------------------------
Textbox Operations:

	1. Entering some data - sendKeys("data");	
	2. Removing existing data - clear();
	3. Capture value present in a Textbox - getAttribute("value");
	4. Handling Auto Suggetions / AJAX Elements
------------------------------------------------------------------------------------
Script to Count and Print all sugeetions for the keyword "Selenium" in google search
------------------------------------------------------------------------------------
System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		driver.findElement(By.name("q")).sendKeys("Selenium");
		Thread.sleep(2000);
		
		List<WebElement> keywordlist = driver.findElement(By.className("G43f7e")).findElements(By.tagName("li"));
		
		System.out.println(keywordlist.size());
		
		for(WebElement element : keywordlist)
		{
			String keyword = element.getText();
			System.out.println(keyword);
		}
--------------------------------------------------------------------------------
Script to click "Selenium Download" from auto suggetion list in google search
for the keyword "selenium".
---------------------------------------------------------------------------------
System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		driver.findElement(By.name("q")).sendKeys("Selenium");
		Thread.sleep(2000);
		
		List<WebElement> keywordlist = driver.findElement(By.className("G43f7e")).findElements(By.tagName("li"));
		
		for(WebElement element : keywordlist)
		{
			String keyword = element.getText();
			if(keyword.equalsIgnoreCase("selenium download"))
			{
				element.click();
				break;
			}
		}

--------------------------------------------------------------------------------------------
11_july_2024

Script to count links present in a page
---------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		List<WebElement> links = driver.findElements(By.tagName("a"));
		System.out.println(links.size());
---------------------------------------------------------------------------------------------
Script to print all links present in a page
---------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		List<WebElement> links = driver.findElements(By.tagName("a"));
		
		for(WebElement element : links)
		{
			System.out.println(element.getText());
		}
------------------------------------------------------------------------------------------
Script to print all links and their redirected URLs
---------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		List<WebElement> links = driver.findElements(By.tagName("a"));
		
		for(WebElement element : links)
		{
			String linkname = element.getText();
			String linkurl = element.getAttribute("href");
			System.out.println(linkname+"  "+linkurl);
			
		}
---------------------------------------------------------------------------------------------
Script to select DOB while crteating New Account in faceBook
---------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");
		driver.findElement(By.linkText("Create new account")).click();
		
		
		Select dlist = new Select(driver.findElement(By.id("day")));
		dlist.selectByIndex(0);
		
		Select mlist = new Select(driver.findElement(By.id("month")));
		mlist.selectByValue("10");
		
		WebElement yearelement = driver.findElement(By.id("year"));
		Select ylist = new Select(yearelement);
		ylist.selectByVisibleText("1990");
		
----------------------------------------------------------------------------------------
Script to to select "Books" in amazon.com Product Category List
------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://amazon.in");
		
		
		Select cat = new Select(driver.findElement(By.id("searchDropdownBox")));		
		cat.selectByVisibleText("Books");
-------------------------------------------------------------------------------------------
12_july_2024

Script to count no. of items present in a DropDownList
--------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://amazon.in");		
		Select cat = new Select(driver.findElement(By.id("searchDropdownBox")));		
		List<WebElement> catlist = cat.getOptions();
		System.out.println(catlist.size());
-------------------------------------------------------------------------------------------
Script to print all items present in a DropDownList
---------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://amazon.in");		
		Select cat = new Select(driver.findElement(By.id("searchDropdownBox")));		
		List<WebElement> catlist = cat.getOptions();
		
		for(WebElement element : catlist)
		{
			System.out.println(element.getText());
		}
--------------------------------------------------------------------------------------------
Script to check the specified item present in the DropDownList or not?
--------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://amazon.in");		
		Select cat = new Select(driver.findElement(By.id("searchDropdownBox")));		
		
		String item_tobe_check = "Flights";
		
		try 
		{
			cat.selectByVisibleText(item_tobe_check);
			System.out.println(item_tobe_check+" is present in the list, test pass");
		} catch (Exception e) 
		{
			System.out.println(item_tobe_check+" is not present in the list, test fail");
		}
-----------------------------------------------------------------------------------------------------------------------
Script to check all items present in the dropdownlist are displayed in alphabetical order or not?
-----------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://amazon.in");		
		Select cat = new Select(driver.findElement(By.id("searchDropdownBox")));		
		List<WebElement> catlist = cat.getOptions();
		
		String cat1,cat2;
		boolean ordered = true;
		
		for(int i=2;i<catlist.size();i++)
		{
			cat1 = catlist.get(i-1).getText();
			cat2 = catlist.get(i).getText();
			if(cat2.compareToIgnoreCase(cat1)<0)
			{
				ordered = false;
				break;
			}
		}
		
		if(ordered)
		{
			System.out.println("All items are displayed in alphabetical order, test pass");
		}else
		{
			System.out.println("Items are not displayed in alphabetical order, test fail");
		}

------------------------------------------------------------------------------------------------------------------------
Script to select a checkbox based on its default selected status
------------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com");		
		driver.findElement(By.linkText("Register")).click();
		
		WebElement element = driver.findElement(By.id("flexCheckChecked")); 
		if(! element.isSelected())
		{
			element.click();
		}
-----------------------------------------------------------------------------------------------------------------------
Script to select a Radio Button
----------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");		
		driver.findElement(By.linkText("Create new account")).click();
		driver.findElement(By.xpath("//input[@name='sex' and @value='2']")).click();
----------------------------------------------------------------------------------------------------------------------
Script to Select Last item present in a DropDownList
----------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://amazon.in");		
		Select cat = new Select(driver.findElement(By.id("searchDropdownBox")));		
		List<WebElement> catlist = cat.getOptions();		
		
		cat.selectByIndex(catlist.size()-1);
----------------------------------------------------------------------------------------------------------------------
13_july_2024

Script to count no. of Rows present in IRCTC Trains Table
-------------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://www.railyatri.in/time-table");
		WebElement trains_table =  driver.findElement(By.xpath("//div[2]/div[4]/div/table"));
		List<WebElement> rows = trains_table.findElements(By.tagName("tr"));
		System.out.println(rows.size());
----------------------------------------------------------------------------------------------------------------------
Script to count no. of columns in a Table Row
----------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://www.railyatri.in/time-table");
		WebElement trains_table =  driver.findElement(By.xpath("//div[2]/div[4]/div/table"));
		List<WebElement> rows = trains_table.findElements(By.tagName("tr"));
		
		List<WebElement> cols = rows.get(1).findElements(By.tagName("td"));
		System.out.println(cols.size());
-------------------------------------------------------------------------------------------------------------------------
Script to Read all Train_numbers and Train_nammes present in IRCTC Table
-------------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://www.railyatri.in/time-table");
		WebElement trains_table =  driver.findElement(By.xpath("//div[2]/div[4]/div/table"));
		List<WebElement> rows = trains_table.findElements(By.tagName("tr"));
		
		for(int i=1;i<rows.size();i++)
		{
			List<WebElement> cols = rows.get(i).findElements(By.tagName("td"));
			String train_number = cols.get(0).getText();
			String train_name = cols.get(1).getText();
			System.out.println(train_number+"  "+train_name);
		}
--------------------------------------------------------------------------------------------------------------------
Script to Read and Print all Rows of data present i IRCTC Trains Table
-------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://www.railyatri.in/time-table");
		WebElement trains_table =  driver.findElement(By.xpath("//div[2]/div[4]/div/table"));
		List<WebElement> rows = trains_table.findElements(By.tagName("tr"));
		
		for(int i=1;i<rows.size();i++)
		{
			List<WebElement> cols = rows.get(i).findElements(By.tagName("td"));
			for(WebElement element : cols)
			{
				String data = element.getText();
				System.out.println(data);
			}
		}
------------------------------------------------------------------------------------------------------------------------

16_july_2024

Script to check New Employee Registered in present in the Employee List or not?
-----------------------------------------------------------------------------------------------------------------------
System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("Qedge123!@#");
		driver.findElement(By.name("Submit")).click();
	
		driver.findElement(By.linkText("PIM")).click();
		driver.findElement(By.linkText("Add Employee")).click();
		driver.findElement(By.id("firstName")).sendKeys("Deepika");
		driver.findElement(By.id("lastName")).sendKeys("demo");
		String empid = driver.findElement(By.id("employeeId")).getAttribute("value");
		driver.findElement(By.id("btnSave")).click();
		
		driver.findElement(By.linkText("Employee List")).click();
		driver.findElement(By.id("empsearch_id")).sendKeys(empid);
		driver.findElement(By.id("searchBtn")).click();
		
		
		WebElement emptable = driver.findElement(By.id("resultTable"));
		List<WebElement> rows = emptable.findElements(By.tagName("tr"));
		
		for(int i=1;i<rows.size();i++)
		{
			List<WebElement> cols = rows.get(i).findElements(By.tagName("td"));
			if(cols.get(1).getText().equals(empid))
			{
			System.out.println("Newly Registered Employee is displayed in Employee List , test pass");
			}else
			{
			System.out.println("Newly Registered Employee is not displayed in Employee List , test fail");
			}
		}
-----------------------------------------------------------------------------------------------------------------------
Script to Enter "DOB" while creating new user in flights application using : sendKeys()
-----------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com/");
		driver.findElement(By.linkText("Register")).click();
		driver.findElement(By.name("dob")).sendKeys("14-08-1996");	
----------------------------------------------------------------------------------------------------------------------
Script to Select "DOB" while creating new user in flights application by operating the calendar
-------------------------------------------------------------------------------------------------------------------------	
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com/");
		driver.findElement(By.linkText("Register")).click();
		driver.findElement(By.name("dob")).click();
		
		String dob = "3/Nov/2003";
		String[] temp = dob.split("/");
		String dt = temp[0];
		String month = temp[1];
		String year = temp[2];
		
		Select ylist = new Select(driver.findElement(By.className("ui-datepicker-year")));
		ylist.selectByVisibleText(year);
		
		Select mlist = new Select(driver.findElement(By.className("ui-datepicker-month")));
		mlist.selectByVisibleText(month);
		
		WebElement cal = driver.findElement(By.className("ui-datepicker-calendar"));
		List<WebElement> rows = cal.findElements(By.tagName("tr"));
		for(int i=1;i<rows.size();i++)
		{
			List<WebElement> cols = rows.get(i).findElements(By.tagName("td"));
			for(WebElement element : cols)
			{
				if(element.getText().equals(dt))
				{	
					element.click();
					break;
				}
			}
		}

----------------------------------------------------------------------------------------------------------------------
Script to Enter "Date of Fly" while booking a ticket in flights application : using sendKeys()
----------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com");
		
		driver.findElement(By.name("email")).sendKeys("sureshbabu.qedge@gmail.com");
		driver.findElement(By.name("password")).sendKeys("demo");
		driver.findElement(By.xpath("//button[@type='submit']")).click();
		
		driver.findElement(By.id("search-date")).sendKeys("12/18/2024");
----------------------------------------------------------------------------------------------------------------------
Script to Select "Date of Fly" while booking a ticket in flights application : by operating the calendar
----------------------------------------------------------------------------------------------------------------------
	System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com");
		
		driver.findElement(By.name("email")).sendKeys("sureshbabu.qedge@gmail.com");
		driver.findElement(By.name("password")).sendKeys("demo");
		driver.findElement(By.xpath("//button[@type='submit']")).click();
		
		driver.findElement(By.id("search-date")).click();
		
		String flydate = "24/May/2030";
		
		String[] temp = flydate.split("/");
		String dt = temp[0];
		String month = temp[1];
		String year = temp[2];
		
		String calyear = driver.findElement(By.className("ui-datepicker-year")).getText();
		while(!calyear.equals(year))
		{
			driver.findElement(By.linkText("Next")).click();
			calyear = driver.findElement(By.className("ui-datepicker-year")).getText();
		}
	
		String calmonth = driver.findElement(By.className("ui-datepicker-month")).getText();
		while(!calmonth.equalsIgnoreCase(month))
		{
			driver.findElement(By.linkText("Next")).click();
			calmonth = driver.findElement(By.className("ui-datepicker-month")).getText();
		}
		
		WebElement cal = driver.findElement(By.className("ui-datepicker-calendar"));
		List<WebElement> rows = cal.findElements(By.tagName("tr"));
		for(int i=1;i<rows.size();i++)
		{
			List<WebElement> cols = rows.get(i).findElements(By.tagName("td"));
			for(WebElement element : cols)
			{
				if(element.getText().equals(dt))
				{	
					element.click();
					break;
				}
			}
		}
	}
-----------------------------------------------------------------------------------------------------------------------
17_july_2024

Selenium Actions Class provided


			.sendKeys()
			.moveToElement()
			.click()
			.contextClick()
			.doubleClick()
			.dragAndDrop()
			.build()
			.perform()
to automate KeyBoard and Mouse Operations.
-------------------------------------------------------------------------------------------------------------------
Script to move Mouse over specified element and perform right click
------------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://snapdeal.com");
		
		Actions act = new Actions(driver);
		act.moveToElement(driver.findElement(By.linkText("Home & Kitchen")));
		act.contextClick();
		act.build().perform();
		
------------------------------------------------------------------------------------------------------------------------
iFrame
------------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://google.com");
		driver.switchTo().frame(0);
		driver.findElement(By.xpath("//button[@aria-label='Stay signed out']")).click();
-------------------------------------------------------------------------------------------------------------------------
18_july_2024

Script to  capture current browser window id using : getWindowHandle()
-------------------------------------------------------------------------------------------------------------------------
		
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://gmail.com");
		String current_window_id =  driver.getWindowHandle();
		System.out.println(current_window_id);
------------------------------------------------------------------------------------------------------------------------
Script to capture all browser window ids using : getWindowHandles()
------------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://gmail.com");	
		driver.findElement(By.linkText("Help")).click();
		
		Set<String> allwindows = driver.getWindowHandles();
		System.out.println(allwindows);
------------------------------------------------------------------------------------------------------------------------
Script to switch between multiple browser windows
------------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://gmail.com");	
		driver.findElement(By.linkText("Help")).click();
		
		Set<String> allwindows = driver.getWindowHandles();
		
		// code to seperate window ids
		Object[] windows = allwindows.toArray();
		String window1 = windows[0].toString();
		String window2 = windows[1].toString();
		
		driver.switchTo().window(window2);
		driver.findElement(By.linkText("Community")).click();
		
		driver.switchTo().window(window1);
		driver.findElement(By.id("identifierId")).sendKeys("demo");
------------------------------------------------------------------------------------------------------------------------

19_july_2024

Script to handle Alert/Popup 
------------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com");
		
		driver.findElement(By.name("email")).sendKeys("sureshbabu.qedge@gmail.com");
		driver.findElement(By.name("password")).sendKeys("demo");
		driver.findElement(By.xpath("//button[@type='submit']")).click();
		
		driver.findElement(By.linkText("Flight Bookings")).click();
		driver.findElement(By.linkText("Delete")).click();
		
		String alertmsg = driver.switchTo().alert().getText();
		if(alertmsg.contains("Delete"))
		{
			driver.switchTo().alert().accept();
		}else
		{
			driver.switchTo().alert().dismiss();
		}
---------------------------------------------------------------------------------------------------------------------
Script delete the specified OrderNo in Flights Orders Table
--------------------------------------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://flights.qedgetech.com");
		
		driver.findElement(By.name("email")).sendKeys("sureshbabu.qedge@gmail.com");
		driver.findElement(By.name("password")).sendKeys("demo");
		driver.findElement(By.xpath("//button[@type='submit']")).click();
		
		driver.findElement(By.linkText("Flight Bookings")).click();
		
		String order_tobe_deleted = "11340";
		
		WebElement orderstable = driver.findElement(By.className("flights_table"));
		
		List<WebElement> rows = orderstable.findElements(By.tagName("tr"));
		for(int i=1;i<rows.size();i++)
		{
			List<WebElement> cols = rows.get(i).findElements(By.tagName("td"));
			if(cols.get(0).getText().equals(order_tobe_deleted))
			{
				cols.get(9).findElement(By.linkText("Delete")).click();
				
				driver.switchTo().alert().accept();
				break;
			}
		}
----------------------------------------------------------------------------------------------------------
ExplicitWait
----------------------------------------------------------------------------------------------------------------------
				
				WebDriverWait wait = new WebDriverWait(driver, 10);
				wait.until(ExpectedConditions.alertIsPresent());				
				driver.switchTo().alert().accept();
------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------

20_july_2024



WebElement Class Methods
-------------------------------------------------------------------------------------
click() : It is used to perform click action on the specified WebElement.

	  WebElement.click();

-------------------------------------------------------------------------------------
sendKeys() : It is used to send data to the specified WebElement.

	  WebElement.sendKeys("data");	   

-------------------------------------------------------------------------------------
clear() : It ised to remove the existing data present in a WebElement.

	  WebElement.clear();

------------------------------------------------------------------------------------
Script to Create New Employee in OrangeHRM Application
------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("Qedge123!@#");
		driver.findElement(By.name("Submit")).click();
		
		driver.findElement(By.linkText("PIM")).click();
		driver.findElement(By.linkText("Add Employee")).click();
		driver.findElement(By.id("firstName")).sendKeys("Veeresh");
		driver.findElement(By.id("lastName")).sendKeys("Kumar");
		
		WebElement element = driver.findElement(By.id("employeeId"));
		element.clear();
		element.sendKeys("2233");
		
		driver.findElement(By.id("btnSave")).click();
------------------------------------------------------------------------------------
getText() : It is used to capture Visible Text of the specified WebElement.Its return 
	    type is String.

	  WebElement.getText();

--------------------------------------------------------------------------------------
getText()
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");
		String msg = driver.findElement(By.className("_8eso")).getText();
		System.out.println(msg);
-----------------------------------------------------------------------------------
getText()
----------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://primusbank.qedgetech.com");
		
		String content = driver.findElement(By.xpath("//table/tbody/tr[2]/td[1]/p[1]")).getText();
		System.out.println(content);
-------------------------------------------------------------------------------------
Script to Print First Link present in Google Page using : getText()
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		List<WebElement> links = driver.findElements(By.tagName("a"));
		
		String firstlink = links.get(0).getText();
		System.out.println(firstlink);
------------------------------------------------------------------------------------
Script to Print First Link present in Google Page using : getText()
------------------------------------------------------------------------------------		
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		String firstlink = driver.findElement(By.tagName("a")).getText();
		System.out.println(firstlink);
----------------------------------------------------------------------------------
Script to print all links present in google page
-----------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://google.com");
		List<WebElement> links = driver.findElements(By.tagName("a"));
		
		System.out.println("Count of Links : "+links.size());
		
		for(WebElement element : links)
		{
			System.out.println(element.getText());
		}
-------------------------------------------------------------------------------------
getAttribute() : It returns specified property value of the element during runtime.


		WebElement.getAttribute("pname");

-------------------------------------------------------------------------------------
getAttribute()
--------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://facebook.com");
		String x = driver.findElement(By.id("email")).getAttribute("placeholder");
		System.out.println(x);
---------------------------------------------------------------------------------------
Script to capture Employee Id generated while adding a New Employee in OrangeHRM App
-------------------------------------------------------------------------------------
		System.setProperty("webdriver.chrome.driver","chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("http://orangehrm.qedgetech.com");
		
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("Qedge123!@#");
		driver.findElement(By.name("Submit")).click();
		
		driver.findElement(By.linkText("PIM")).click();
		driver.findElement(By.linkText("Add Employee")).click();
		
		String empid =  driver.findElement(By.id("employeeId")).getAttribute("value");
		System.out.println(empid);



------------------------------------------------------------------------------------------------------------------------
26_july_2024

Syntax of Creating a Method
------------------------------------------------------------------------------------------------------------------------

	[public] [static] void/return_type methodName([arg1,arg2,...argn])
	{
		
		statement 1;
		statement 2;

		statement n;	
		
           [return value_tobe_returned;]		
	}
------------------------------------------------------------------------------------------------------------------------

27_july_2024

Local Variables & Global Variables
-----------------------------------------------------------------------------------------------------------
public class DemoClass
{
	String url; // Global Variable
	
	void f1()
	{
		
		url = "htttp://google.com";
		System.out.println(url);
		
		int x;  // Local variable
	}
	
	
	void f2()
	{
		
		System.out.println(url);
	}	

}
--------------------------------------------------------------------------------------------------------
TestCase 1 : Admin Login Test with Valid Credentials

    Step 1 : Launch OrangeHRM App
    Step 2 : Login as Admin and check Admin Module Displayed or not?
    Step 3 : Logout
    Step 4 : Close App
--------------------------------------------------------------------------------------------------------
TestCase 2 : Admin Login Test with Invalid Credentials				

    Step 1 : Launch OrangeHRM App
    Step 2 : Login with invalid credentials and check appropriate error message displayed or not?	
    Step 3 : Close App
---------------------------------------------------------------------------------------------------------


29_july_2024

-----------------------------------------------------------------------------------------------------------

31_july_2024

TestNG annotations
-----------------------------------------------------------------------------------------------------------

TestNG provided

		@Test
		@BeforeTest
		@AfterTest
		@BeforeSuite
		@AfterSuite
annotations to execute testcases and also to configure pre-condtions and post conditions for a TestCase/Test Suite.

----------------------------------------------------------------------------------------------------------
@Test	: If any method is configured using @Test annotation, TestNG executes that methods, if the code 	  executed successfully with no errors TestNG produce result as "Pass". If any errors are occured 
	  TestNG produce result as "Fail".

	@Test
	void method()
	{

	}

----------------------------------------------------------------------------------------------------------
@BeforeTest : If any method is configured using @BeforeTest annotation , this method will be executed 
	      before executing each testcase present in the Test Suite.


	@BeforeTest
	void method()
	{

	}

----------------------------------------------------------------------------------------------------------
@AfterTest  : If any method is configured using @AfterTest annotation , this method will be executed 
	      after executing each testcase present in the Test Suite.

	@AfterTest
	void method()
	{

	}

----------------------------------------------------------------------------------------------------------
@BeforeSuite : A method configured using @BeforeSuite will be executed once before running the Test Suite.


@AfterSuite : A method configured using @AfterSuite will be executed once at the end of the Test Suite.

-----------------------------------------------------------------------------------------------------------
Creating Test Suite
-----------------------------------------------------------------------------------------------------------
In TestNG we can group TestCases into a TestSuite using testng.xml file, so that if we run TestSuite all
TestCases present in the suite will be executed one by one.

----------------------------------------------------------------------------------------------------------
1_july_2024

Step 1 : Defining Parameters in TestNG.xml File [Test Suite]

Step 2 : Accessing these parameters in Testcases 

----------------------------------------------------------------------------------------------------------
Step 1 : Defining Parameters in TestNG.xml File [Test Suite]

	<test name="TestCase Title">
	<parameter name="paraname" value="paravalue"></parameter>	
		

	</test>
----------------------------------------------------------------------------------------------------------
Step 2 : Accessing these parameters in Testcases ie, in @Test methods
---------------------------------------------------------------------------------------------------------
	
	@Parameters({"paraname"})		
	@Test
	void test1(arg1)
	{

	}

	@Parameters({"para1","para2"})
	@Test
	void test2(arg1,arg2)
	{
	
	}
---------------------------------------------------------------------------------------------------------
TestNG Assertions: 
---------------------------------------------------------------------------------------------------------

TestNG provided Assert Class, This Assert Class provided 


				.assertEquals()
				.assertTrue()
				.assertFalse()

methods to implement functional validations.
----------------------------------------------------------------------------------------------------------

3rd aug_2024

TestNG Assertions
---------------------------------------------------------------------------------------------------------
assertEquals()
----------------------------------------------------------------------------------------------------------
public class DemoTest 
{
	
	@Test
	void test1()
	{
		String exptitle,acttitle;		
		exptitle = "Google";
		acttitle = "Google";		
		Assert.assertEquals(acttitle, exptitle);		
	}
	

	@Test
	void test2()
	{
		String exptitle,acttitle;		
		exptitle = "Google";
		acttitle = "Gmail";		
		Assert.assertEquals(acttitle, exptitle);		
	}
	
}
--------------------------------------------------------------------------------------------------------
	
--------------------------------------------------------------------------------------------------------
public class DemoTest 
{
	
	@Test
	void test1()
	{
		boolean actres = true;
		Assert.assertTrue(actres);
	}
	
	@Test
	void test2()
	{
		boolean actres = false;
		Assert.assertTrue(actres);
	}
	
}
--------------------------------------------------------------------------------------------------------
assertFalse()
-----------------------------------------------------------------------------------------------------------
public class DemoTest 
{
	
	@Test
	void test1()
	{
		boolean actres = false;
		Assert.assertFalse(actres);
	}
	
	@Test
	void test2()
	{
		boolean actres = true;
		Assert.assertFalse(actres);
	}
	
}
----------------------------------------------------------------------------------------------------------
Scheduling Test Executing Order using : priority keyword
----------------------------------------------------------------------------------------------------------
public class DemoTest 
{
	
	@Test(priority = 0)
	void launchApp()
	{
		System.out.println("Launch Gmail App");
	}
	
	@Test(priority = 1)
	void closeApp()
	{
		System.out.println("Close GMail App"); 
	}
	
}
----------------------------------------------------------------------------------------------------------
Disabling / Suspending Test Methods from Test Execution using : enabled = false
----------------------------------------------------------------------------------------------------------
public class DemoTest 
{
	
	@Test
	void test1()
	{
		System.out.println("This is TestCase 1");
	}
	
	@Test(enabled = true)
	void test2()
	{
		System.out.println("This is TestCase 2");
	}
	
	@Test(enabled = false)
	void test3()
	{
		System.out.println("This is TestCase 3");
	}
	
	
}
----------------------------------------------------------------------------------------------------------
Commenting TestCases in Test Suite : <!-- code -->
----------------------------------------------------------------------------------------------------------
<suite name="GMail Test Suite">

	<test name="Send Mail TestCase">
	<parameter name="email" value="sureshbabu.qedge@gmail.com"></parameter>
	<parameter name="sub" value="Selenium Interview Schedule"></parameter>
		<classes>
			<class name="testcases.SendMailTest"></class>
		</classes>	
	</test>

<!--  

	<test name="Receive Mail TestCase">
		<classes>
			<class name="testcases.ReceiveMailTest"></class>
		</classes>
	</test>
-->

</suite>
-----------------------------------------------------------------------------------------------------------
Diff. Automation Frameworks
---------------------------------------------------------------------------------------------------------
	1. Modularity [TestNG] Framework
	
	2. Data-Driven-Framework

	3. Hybrid Framework

	4. Page Object Model [POM]

	5. Cucumber BDD Framework

--------------------------------------------------------------------------------------------------------
OBJECT REPOSITORY
DATE = 19-08-2024

#Locators for Primus bank with xpath
Url = http://primusbank.qedgetech.com/
Objuser = //input[@id='txtuId']
Objpass = //input[@id='txtPword']
Objlogin = //input[@id='login']
# Test data foor login
Enteruser = Admin
Enterpass =Admin
# Locators for Branch creation
ObjBranches = (//img)[5]
ObjNewBranch = //input[@id='BtnNewBR']
ObjBname = //input[@id='txtbName']
ObjAddress1 = //input[@id='txtAdd1']
ObjAddress2 = //input[@id='Txtadd2']
ObjAddress3 = //input[@id='txtadd3']
ObjArea = //input[@id='txtArea']
Objzip = //input[@id='txtZip']
ObjCountry = //select[@id='lst_counrtyU']
Objstate = //select[@id='lst_stateI']
Objcity = //select[@id='lst_cityI']
Objsubmit = //input[@id='btn_insert']
# test data for new branch creation
EnterbranchN = kadiri
EnterAdd1 = Anantapur
EnterAdd2 = Madanapalli
EnterAdd3 = Srnagar
EnterArea = Kaadiri
Enterzip = 24569
SelectCountry = INDIA
SelectState = GOA
SelectCity = GOA
# Locator values for Role creation
ObjRoles = //img[@src='images/Roles_but.jpg'] 
ObjNewRole = //input[@id='btnRoles']
ObjRoleName = //input[@id='txtRname']
ObjRoleDesc = //input[@id='txtRDesc']
ObjRoleType = //select[@id='lstRtypeN']
ObjSubmitbtn = //input[@id='btninsert']
# test data for new Role creation
EnterRole = clerk
EnterRoleDesc = iam working as a clerk
SelectRoletype = E
# Locator for logout
ObjLogout = (//img)[4]

=====================================================================
package aub19;

import java.io.FileInputStream;
import java.time.Duration;
import java.util.Properties;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.Test;

public class Using_Property {
WebDriver driver;
Properties conpro;
@BeforeMethod
public void setUp()throws Throwable
{
	conpro = new Properties();
	//load property file
	conpro.load(new FileInputStream("primus.properties"));
	driver = new ChromeDriver();
	driver.manage().window().maximize();
	driver.get(conpro.getProperty("Url"));
	driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
	driver.findElement(By.xpath(conpro.getProperty("Objuser"))).sendKeys(conpro.getProperty("Enteruser"));
	driver.findElement(By.xpath(conpro.getProperty("Objpass"))).sendKeys(conpro.getProperty("Enterpass"));
	driver.findElement(By.xpath(conpro.getProperty("Objlogin"))).click();
}
@Test
public void branchcreation() throws Throwable
{
	driver.findElement(By.xpath(conpro.getProperty("ObjBranches"))).click();
	driver.findElement(By.xpath(conpro.getProperty("ObjNewBranch"))).click();
	driver.findElement(By.xpath(conpro.getProperty("ObjBname"))).sendKeys(conpro.getProperty("EnterbranchN"));
	driver.findElement(By.xpath(conpro.getProperty("ObjAddress1"))).sendKeys(conpro.getProperty("EnterAdd1"));
	driver.findElement(By.xpath(conpro.getProperty("ObjAddress2"))).sendKeys(conpro.getProperty("EnterAdd2"));
	driver.findElement(By.xpath(conpro.getProperty("ObjAddress3"))).sendKeys(conpro.getProperty("EnterAdd3"));
	driver.findElement(By.xpath(conpro.getProperty("ObjArea"))).sendKeys(conpro.getProperty("EnterArea"));
	driver.findElement(By.xpath(conpro.getProperty("Objzip"))).sendKeys(conpro.getProperty("Enterzip"));
	new Select(driver.findElement(By.xpath(conpro.getProperty("ObjCountry")))).selectByVisibleText(conpro.getProperty("SelectCountry"));
	Thread.sleep(3000);
	new Select(driver.findElement(By.xpath(conpro.getProperty("Objstate")))).selectByVisibleText(conpro.getProperty("SelectState"));
	Thread.sleep(3000);
	new Select(driver.findElement(By.xpath(conpro.getProperty("Objcity")))).selectByVisibleText(conpro.getProperty("SelectCity"));
	Thread.sleep(3000);
	driver.findElement(By.xpath(conpro.getProperty("Objsubmit"))).click();
	String alerttext = driver.switchTo().alert().getText();
	System.out.println(alerttext);
	Thread.sleep(3000);
	driver.switchTo().alert().accept();
	
}
@Test
public void roleCreation() throws Throwable
{
	driver.findElement(By.xpath(conpro.getProperty("ObjRoles"))).click();
	driver.findElement(By.xpath(conpro.getProperty("ObjNewRole"))).click();
	driver.findElement(By.xpath(conpro.getProperty("ObjRoleName"))).sendKeys(conpro.getProperty("EnterRole"));
	driver.findElement(By.xpath(conpro.getProperty("ObjRoleDesc"))).sendKeys(conpro.getProperty("EnterRoleDesc"));
	new Select(driver.findElement(By.xpath(conpro.getProperty("ObjRoleType")))).selectByVisibleText(conpro.getProperty("SelectRoletype"));
	Thread.sleep(2000);
	driver.findElement(By.xpath(conpro.getProperty("ObjSubmitbtn"))).click();
	String alerttext = driver.switchTo().alert().getText();
	System.out.println(alerttext);
	Thread.sleep(3000);
	driver.switchTo().alert().accept();
		
}
@AfterMethod
public void tearDown()
{
	driver.findElement(By.xpath(conpro.getProperty("ObjLogout"))).click();
	driver.quit();
}
}

DATE = 20 -08-2024 

EXTENT REPORST

package aug20;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

import com.relevantcodes.extentreports.ExtentReports;
import com.relevantcodes.extentreports.ExtentTest;
import com.relevantcodes.extentreports.LogStatus;

public class Advance_Reports {
ExtentReports reports;
ExtentTest logger;
WebDriver driver;
@BeforeTest
public void generateReports()
{
	//define path of html
	reports = new ExtentReports("./ExtenReports/Demo.html");
}
@BeforeMethod
public void setUp()
{
	driver = new ChromeDriver();
	driver.manage().window().maximize();
	driver.get("https:/google.com");
}
@Test
public void firstTestCase()
{
	logger = reports.startTest("Pass Test");
	logger.assignAuthor("Ranga");
	String Expected ="Google";
	String Actual = driver.getTitle();
	if(Actual.equalsIgnoreCase(Expected))
	{
		logger.log(LogStatus.PASS, "Title is Matching::::"+Expected+"---------"+Actual);
	}
	else
	{
		logger.log(LogStatus.FAIL, "Title is Not Matching::::"+Expected+"---------"+Actual);
	}
	
	
}
@Test
public void seconTestCase()
{
	logger = reports.startTest("Fail Test");
	logger.assignAuthor("Ranga");
	String Expected ="Gmail";
	String Actual = driver.getTitle();
	if(Actual.equalsIgnoreCase(Expected))
	{
		logger.log(LogStatus.PASS, "Title is Matching::::"+Expected+"---------"+Actual);
	}
	else
	{
		logger.log(LogStatus.FAIL, "Title is Not Matching::::"+Expected+"---------"+Actual);
	}
}
@AfterMethod
public void tearDown()
{
	reports.endTest(logger);
	reports.flush();
	driver.quit();
}
}

DATA  DRIVEN FRAME WORK
DATE = 21-08-2024

Test Automation Framework Interview Questions and Answers:

1. What is a Framework?
A framework defines a set of rules or best practices which we can follow in a systematic way to achieve the desired results.
The structural way to implement the scripts for better maintenance is known as framework.
Maintenance means how we are implementing the script. Is it easy to analyze, update, execute and getting the test report.
Automation Frameworks?
•	Modular Testing Framework
•	Data Driven Testing Framework
•	Keyword Driven Testing Framework
•	Hybrid Testing Framework

3. Why Framework?
In a test automation project, we do perform different tasks by using different types of files like .xlsx, .txt, .properties, xml, etc. To organize and manage all the files and to finish all the tasks in a systematic approach we use a framework.

4. Have you created any Framework?
If you are a beginner: No, I didn’t get a chance to create a framework. I have used the framework which is already available.
If you are an experienced tester: Yes, I have created a framework (Or) No, but I have involved in the creation of the framework.

5. What are the advantages of using Test Automation Framework?
1.	Saves time and money. Automation testing is faster in execution
2.	Reusability of code. Create one time and execute multiple times with less or no maintenance
3.	Easy reporting. It generates automatic reports after test execution
4.	Easy for compatibility testing. It enables parallel execution in combination of different OS and browser environments
5.	Low cost maintenance. It is cheaper compared to manual testing in a long run
6.	Automated testing is more reliable
7.	Automated testing is more powerful and versatile
8.	It is mostly used for regression testing. Supports execution of repeated test cases
9.	Maximum coverage. It helps to increase the test coverage

6. Which Test Automation Framework you are using and why?
Some of the Test Automation Frameworks are:
•	Data Driven Testing Framework
•	Keyword Driven Testing Framework
•	Hybrid Testing Framework

7. Mention the name of the framework which ‘you are currently using’ or which ‘you have hands on experience’.
Example: 
Answers should be, Already the organization which I am working for is using that particular framework or I have an experience on that particular framework or Its easy to handle all my scripts to execute and generate logs, screenshots and reports by using this framework.

8. Can you explain the Framework  

9. What is Automation testing? What are the advantages of Automation Testing?
Automation testing is the process of testing the software using an automation tool to find the defects. In this process, executing the test scripts and generating the results are performed automatically by automation tools. Some most popular tools to do automation testing are HP QTP/UFT,  etc.,
For advantages refer to question 5 of this post “Test Automation Framework Interview Questions”

10. What are the most popular testing tools for functional testing?
1.	Selenium
2.	QTP(Quick Test Professional) / UFT(Unified Functional Testing)
11. Why do you prefer Selenium Automation Tool?
1.	Free and open source
2.	Have large user base and helping communities
3.	Cross browser compatibility
4.	Platform compatibility
5.	Multiple programming languages support

12. What type of test cases do you pick up to automate?
I focus on the test cases which should be executed in a repetitive manner such as regression test cases, smoke and sanity test cases

13. What type of test cases you won’t pick up to automate?
Before picking up the test cases to automate, I do check whether the application is stable or not. So based on this, I don’t pickup test cases when the AUT changes frequently and the test cases which I run rarely and run only one time. When I do usability and exploratory testing.

14. How many test cases you have automated per day?
It depends on Test case scenario complexity and length. I did automate 2-5 test scenarios per day when the complexity is limited. Sometimes just 1 or fewer test scenarios in a day when the complexity is high.

15. How you build Object Repository in your project? 
In QTP, there is an Object Repository concept. When a user records a test, the objects and its properties are captured by default in an Object Repository. QTP uses this Object Repository to play back the scripts. Coming to Selenium, there is no default Object Repository concept. It doesn’t mean that there is no Object Repository in Selenium. Even though there is no default one still we could create our own. In Selenium, we call objects as locators (such as ID, Name, Class Name, Tag Name, Link Text, Partial Link Text, XPath, and CSS). Object repository is a collection of objects. One of the ways to create Object Repository is to place all the locators in a separate file (i.e., properties file). But the best way is to use Page Object Model. In the Page Object Model Design Pattern, each web page is represented as a class. All the objects related to a particular page of a web application are stored in a class.


EXCEL METHODES
DATE 24-08-2024

package utilities;

import java.io.FileInputStream;
import java.io.FileOutputStream;

import org.apache.poi.ss.usermodel.CellType;
import org.apache.poi.ss.usermodel.IndexedColors;
import org.apache.poi.xssf.usermodel.XSSFCell;
import org.apache.poi.xssf.usermodel.XSSFCellStyle;
import org.apache.poi.xssf.usermodel.XSSFFont;
import org.apache.poi.xssf.usermodel.XSSFRow;
import org.apache.poi.xssf.usermodel.XSSFSheet;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;

public class ExcelFileUtil {
XSSFWorkbook wb;
//creating constructor for reading excel path
public ExcelFileUtil(String excelpath)throws Throwable
{
	FileInputStream fi = new FileInputStream(excelpath);
	wb = new XSSFWorkbook(fi);
}
//count no of rows ina sheet
public int rowCount(String sheetname)
{
	return wb.getSheet(sheetname).getLastRowNum();
}
//method for reading cell data
public String getCellData(String sheetname,int row,int column)
{
	String data="";
	if(wb.getSheet(sheetname).getRow(row).getCell(column).getCellType()==CellType.NUMERIC)
	{
		int celldata =(int) wb.getSheet(sheetname).getRow(row).getCell(column).getNumericCellValue();
		data =String.valueOf(celldata);
	}
	else
	{
		data =wb.getSheet(sheetname).getRow(row).getCell(column).getStringCellValue();
	}
	return data;
}
//method for writing status into new wb
public void setCellData(String sheetname,int row,int column,String status,String WriteExcel)throws Throwable
{
	//get sheet from wb
	XSSFSheet ws = wb.getSheet(sheetname);
	//getrow from sheet
	XSSFRow rowNum =ws.getRow(row);
	//create cell
	XSSFCell cell = rowNum.createCell(column);
	cell.setCellValue(status);
	if(status.equalsIgnoreCase("Pass"))
	{
		XSSFCellStyle style = wb.createCellStyle();
		XSSFFont font = wb.createFont();
		font.setColor(IndexedColors.GREEN.getIndex());
		font.setBold(true);
		style.setFont(font);
		rowNum.getCell(column).setCellStyle(style);
	}
	else if(status.equalsIgnoreCase("Fail"))
	{
		XSSFCellStyle style = wb.createCellStyle();
		XSSFFont font = wb.createFont();
		font.setColor(IndexedColors.RED.getIndex());
		font.setBold(true);
		style.setFont(font);
		rowNum.getCell(column).setCellStyle(style);
	}
	else if(status.equalsIgnoreCase("Blocked"))
	{
		XSSFCellStyle style = wb.createCellStyle();
		XSSFFont font = wb.createFont();
		font.setColor(IndexedColors.BLUE.getIndex());
		font.setBold(true);
		style.setFont(font);
		rowNum.getCell(column).setCellStyle(style);
	}
	FileOutputStream fo =new FileOutputStream(WriteExcel);
	wb.write(fo);
	
	
}
public static void main(String[] args) throws Throwable {
	ExcelFileUtil xl = new ExcelFileUtil("D:/Sample.xlsx");
	int rc =xl.rowCount("Emp");
	System.out.println(rc);
	//iterate all rows
	for(int i=1;i<=rc;i++)
		
	{
		String fname = xl.getCellData("Emp", i, 0);
		String mname = xl.getCellData("Emp", i, 1);
		String lname = xl.getCellData("Emp", i, 2);
		String eid = xl.getCellData("Emp", i, 3);
		System.out.println(fname+"    "+mname+"    "+lname+"   "+eid);
		//write status as pass
		//xl.setCellData("emp", i, 4, "pass", "D:/Results.xlsx");
		//xl.setCellData("emp", i, 4, "Fail", "D:/Results.xlsx");
		xl.setCellData("emp", i, 4, "Blocked", "D:/Results.xlsx");
	}
}
}

EXCEL DATA

DATA DRIVERN FRAME WORK
24-08-2024

//preparing property file
======================================================
#Locators for login
Browser = chrome
Url = http://webapp.qedgetech.com/
ObjReset = //button[@id='btnreset']
ObjUser = //input[@id='username']
Objpass = //input[@id='password']
ObjLogin = //button[@id='btnsubmit']
ObjError = //div[contains(text(),'Incorrect user ID or password')]
ObjOk = (//button[contains(text(),'OK')])[6]
ObjLogout = (//a[starts-with(text(),' Logout')])[2]

=============================================================
//preparing apputil class
==============================================================
package config;

import java.io.FileInputStream;
import java.util.Properties;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.testng.Reporter;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;

public class AppUtil {
	public static WebDriver driver;
	public static Properties conpro;
	@BeforeTest
	public static void setUp()throws Throwable
	{
		conpro = new Properties();
		//load property file
		conpro.load(new FileInputStream("./PropertyFiles/Environment.properties"));
		if(conpro.getProperty("Browser").equalsIgnoreCase("chrome"))
		{
			driver = new ChromeDriver();
			driver.manage().window().maximize();
		}
		else if(conpro.getProperty("Browser").equalsIgnoreCase("firefox"))
		{
			driver= new FirefoxDriver();
		}
		else
		{
			Reporter.log("Browser value is Not Matching",true);
		}
	}
	@AfterTest
	public static void tearDown()
	{
		driver.quit();
	}

}
==========================================================================================
//preparing Functionlibrary class
========================================================================================
package commonFunctions;

import java.time.Duration;

import org.openqa.selenium.By;
import org.testng.Reporter;

import config.AppUtil;

public class FunctionLibrary extends AppUtil {
public static boolean adminLogin(String user,String pass) throws Throwable
{
	driver.get(conpro.getProperty("Url"));
	driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
	driver.findElement(By.xpath(conpro.getProperty("ObjReset"))).click();
	driver.findElement(By.xpath(conpro.getProperty("ObjUser"))).sendKeys(user);
	driver.findElement(By.xpath(conpro.getProperty("Objpass"))).sendKeys(pass);
	driver.findElement(By.xpath(conpro.getProperty("ObjLogin"))).click();
	Thread.sleep(2000);
	String Expected ="dashboard";
	String Actual = driver.getCurrentUrl();
	if(Actual.contains(Expected))
	{
		Reporter.log("Login success::"+Expected+"        "+Actual,true);
		//click logout link
		driver.findElement(By.xpath(conpro.getProperty("ObjLogout"))).click();
		return true;
	}
	else
	{
	String error_Message = driver.findElement(By.xpath(conpro.getProperty("ObjError"))).getText();
	Thread.sleep(2000);
	driver.findElement(By.xpath(conpro.getProperty("ObjOk"))).click();
	Reporter.log(error_Message+"     "+Expected+"        "+Actual,true);
	return false;
	}
	
	
}
}
===================================================================================
//preparing driverScript class
======================================================================================
package driverFactory;

import java.io.File;

import org.apache.commons.io.FileUtils;
import org.openqa.selenium.OutputType;
import org.openqa.selenium.TakesScreenshot;
import org.testng.Reporter;
import org.testng.annotations.Test;

import com.relevantcodes.extentreports.ExtentReports;
import com.relevantcodes.extentreports.ExtentTest;
import com.relevantcodes.extentreports.LogStatus;

import commonFunctions.FunctionLibrary;
import config.AppUtil;
import utilities.ExcelFileUtil;

public class DriverScript extends AppUtil{
ExtentReports reports;
ExtentTest logger;
String inputpath="./FileInput/TestData.xlsx";
String outputpath ="./FileOutput/DataDrivenResults.xlsx";
@Test
public void startTest() throws Throwable
{
	//define path of html report
	reports = new ExtentReports("./Reports/Login.html");
	//create reference object for excel file util class
	ExcelFileUtil xl = new ExcelFileUtil(inputpath);
	//count no of rows in login Sheet
	int rc =xl.rowCount("Login");
	Reporter.log("No of rows are::"+rc,true);
	//iterate all rows in login sheet
	for(int i=1;i<=rc;i++)
	{
		logger = reports.startTest("Login Test");
		logger.assignAuthor("Ranga");
		//read username and password cells
		String username = xl.getCellData("Login", i, 0);
		String password = xl.getCellData("Login", i, 1);
		logger.log(LogStatus.INFO,username+"     "+password);
		//call login method and assign parametrs
		boolean res =FunctionLibrary.adminLogin(username, password);
		if(res)
		{
			//if res is true write as login success into results cell
			xl.setCellData("Login", i, 2, "Login success", outputpath);
			//if res is true write as pass into status cell
			xl.setCellData("Login", i, 3, "pass", outputpath);
			logger.log(LogStatus.PASS, "Valid Username and password");
		}
		else
		{
			//adding screen shot for fail test
			File screen =((TakesScreenshot)driver).getScreenshotAs(OutputType.FILE);
			//copy screen shot into local system
			FileUtils.copyFile(screen, new File("./Screenshot/Iteration/"+i+"Login.png"));
			//if res is false write as login Fail into results cell
			xl.setCellData("Login", i, 2, "Login Fail", outputpath);
			//if res is false write as Fail into status cell
			xl.setCellData("Login", i, 3, "Fail", outputpath);
			logger.log(LogStatus.FAIL, "Invalid username and password");
		}
		
		reports.endTest(logger);
		reports.flush();
		
	}
}
}

MAVEN 
27-08-2024
What is Maven?
Maven is a software project management and comprehension tool primarily used with Java-based projects but that can also be used to manage projects in other programming languages like C# and Ruby. Maven helps manage builds, documentation, reporting, dependencies, software configuration management (SCM), releases and distribution. 
Few Glossaries around Maven

Maven's key features include:
A standard, easy way to build projects in which unnecessary details are hidden
A uniform build system, where a standard strategy is followed when building any project
Quality project information, such as dependency lists, cross referenced sources and unit test reports
Dependency management, including automatic updating and dependency closures
The ability to handle multiple projects simultaneously
Dynamic downloading of necessary Java libraries and plug-ins from Maven repositories
Maven was created by Jason Van Zyl in 2002 as part of the Apache Turbine project. It became an Apache Software Foundation project in 2003. After that, several versions of Maven were released, including Maven v1.0, v2.0 and v3.0.
Summary:
•	Maven is an automation and management tool.
•	It is written in Java Language and used to build and manage projects written in C#, Ruby, Scala, and other languages.
•	Maven helps the developer to create a java-based project more easily.
•	To configure the Maven, you need to use Project Object Model, which is stored in a pom.xml-file.




Maven is a software project management and comprehension tool primarily used with Java-based projects but that can also be used to manage projects in other programming languages like C# and Ruby. Maven helps manage builds, documentation, reporting, dependencies, software configuration management (SCM), releases and distribution. 

 Maven Local Repository
This is the place where Maven stores all the project jars files or libraries or dependencies. By default the folder name is ‘.m2‘and by default the location in windows 7 is ‘C:\Users\john\.m2\repository ‘.
 Maven Central Repository
Maven central repository is the default location ‘http://mvnrepository.com/‘for Maven to download all the project dependency libraries. For any library required in the project, Maven first look in to the .m2 folder of Local Repository, if it does not find the required library then it looks in Central Repository and download the library in to local repository.
Dependency Keyword
Dependencies are the libraries, which are required by the project. For example Log4j jars, Apache Poi jars, Selenium Jars etc. Dependencies are mentioned in the Maven pom.xml like this:
	 	<dependency>  		<groupId>org.seleniumhq.selenium</groupId>
  		<artifactId>selenium-java</artifactId>
  		<version>3.4.0</version>
  	</dependency>
 
Surefire Plugin
The Surefire Plugin is used during the test phase of the build lifecycle to execute the unit tests of an application. It generates reports in 2 different file formats like plain text file, xml files and html files as well. Even if you are using TestNG or Junits framework for reporting, this plugin is must to use, as it helps Maven to identify tests.
 
Maven POM.xml
POM is Project Object Model XML file that contains information about the project and configuration details used by Maven to build the project. It contains default values for most projects. Some of the configuration that can be specified in the POM are the project dependencies, the plugins or goals that can be executed, the build profiles, and so on.
 
POM
//preparing property file for url and browser
=================================================
Browser = firefox
Url = http://webapp.qedgetech.com/
===============================================

//preparing Pom for login page
===========================================
package applicationLayer;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.support.FindBy;

public class LoginPage {
	
//Define Repository for login
	@FindBy(xpath = "//button[@id='btnreset']")
	WebElement ObjReset;
	@FindBy(id ="username")
	WebElement ObjUser;
	@FindBy(name ="password")
	WebElement Objpass;
	@FindBy(xpath = "//button[@id='btnsubmit']")
	WebElement ObjLogin;
	//write method to perform action
	public void adminLogin(String user,String pass)
	{
		ObjReset.click();
		ObjUser.sendKeys(user);
		Objpass.sendKeys(pass);
		ObjLogin.click();
	}
}

======================================================================
//Preparing Pom for Supplier page
=========================================================================
package applicationLayer;

import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.FindBy;
import org.openqa.selenium.support.ui.WebDriverWait;
import org.testng.Reporter;

public class SupplierPage {
	WebDriver driver;
	WebDriverWait wait;
	public SupplierPage(WebDriver driver)
	{
		this.driver=driver;
	}
	@FindBy(xpath="(//a[text()='Suppliers'])[2]")
	WebElement clickSuppierlink;
	@FindBy(xpath="(//span[@data-caption='Add'])[1]")
	WebElement clickAddIcon;
	@FindBy(name="x_Supplier_Number")
	WebElement SupplierNumber;
	@FindBy(name="x_Supplier_Name")
	WebElement SupplierName;
	@FindBy(name="x_Address")
	WebElement Address;
	@FindBy(name="x_City")
	WebElement City;
	@FindBy(name="x_Country")
	WebElement Country;
	@FindBy(name="x_Contact_Person")
	WebElement ContactPerson;
	@FindBy(name="x_Phone_Number")
	WebElement PhoneNumber;
	@FindBy(name="x__Email")
	WebElement Email;
	@FindBy(name="x_Mobile_Number")
	WebElement MobileNumber;
	@FindBy(name="x_Notes")
	WebElement Notes;
	@FindBy(name="btnAction")
	WebElement ClickAddBtn;
	@FindBy(xpath="//button[contains(text(),'OK!')]")
	WebElement clickConfirmOkBtn;
	@FindBy(xpath="(//button[text()='OK'])[6]")
	WebElement clickAlertOkBtn;
	@FindBy(xpath="//span[@data-caption='Search']")
	WebElement clickSearchPanelBtn;
	@FindBy(name="psearch")
	WebElement SearchTextbox;
	@FindBy(name="btnsubmit")
	WebElement SearchBtn;
	@FindBy(xpath = "//table[@class='table ewTable']/tbody/tr[1]/td[6]/div/span/span")
	WebElement webTable;
	//method for supplier creation
	public boolean addSupplier(String SupplierName,String Address,String City,String Country,
			String contactPerson,String PhoneNumber,String email,String MobileNumber,String Notes) throws Throwable
	{
		Actions ac = new Actions(driver);
		ac.moveToElement(this.clickSuppierlink).click().perform();
		Thread.sleep(2000);
		ac.moveToElement(this.clickAddIcon).click().perform();
		Thread.sleep(2000);
		String Exp_Data = this.SupplierNumber.getAttribute("value");
		this.SupplierName.sendKeys(SupplierName);
		this.Address.sendKeys(Address);
		this.City.sendKeys(City);
		this.Country.sendKeys(Country);
		this.ContactPerson.sendKeys(contactPerson);
		this.PhoneNumber.sendKeys(PhoneNumber);
		this.Email.sendKeys(email);
		this.MobileNumber.sendKeys(MobileNumber);
		this.Notes.sendKeys(Notes);
		this.ClickAddBtn.sendKeys(Keys.ENTER);
		Thread.sleep(2000);
		this.clickConfirmOkBtn.click();
		Thread.sleep(2000);
		this.clickAlertOkBtn.click();
		Thread.sleep(2000);
		if(!this.SearchTextbox.isDisplayed())
			this.clickSearchPanelBtn.click();
		this.SearchTextbox.clear();
		this.SearchTextbox.sendKeys(Exp_Data);
		this.SearchBtn.click();
		Thread.sleep(3000);
		String Act_Data =webTable.getText();
		if(Act_Data.equals(Exp_Data))
		{
			Reporter.log("Add Supplier is Success:::"+Exp_Data+"      "+Act_Data,true);
			return true;
		}
		else
		{
			Reporter.log("Add Supplier is Fail:::"+Exp_Data+"      "+Act_Data,true);
			return false;
		}
		
	}
}




===========================================================================
//preparing pom for Logout page
===============================================================================
package applicationLayer;

import org.openqa.selenium.WebElement;
import org.openqa.selenium.support.FindBy;

public class LogoutPage {
@FindBy(xpath = "(//a[starts-with(text(),' Logout')])[2]")
WebElement logoutClick;
public void adminLogout()
{
	logoutClick.click();
}

}





====================================================================================
//preparing Apputil1 Class for preconditions and post conditions
======================================================================================
package config;

import java.io.FileInputStream;
import java.time.Duration;
import java.util.Properties;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.PageFactory;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;

import applicationLayer.LoginPage;
import applicationLayer.LogoutPage;

public class AppUtil1 {
public static WebDriver driver;
public static Properties conpro;
@BeforeTest
public static void setUp()throws Throwable

{
	conpro= new Properties();
	conpro.load(new FileInputStream("./PropertyFiles/Environment.properties"));
	if(conpro.getProperty("Browser").equalsIgnoreCase("chrome"))
	{
		driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get(conpro.getProperty("Url"));
		driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
		LoginPage login =PageFactory.initElements(driver, LoginPage.class);
		//call login method
		login.adminLogin("admin", "master");
		
	}
	else if(conpro.getProperty("Browser").equalsIgnoreCase("firefox"))
	{
		driver = new FirefoxDriver();
		driver.get(conpro.getProperty("Url"));
		driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
		LoginPage login =PageFactory.initElements(driver, LoginPage.class);
		//call login method
		login.adminLogin("admin", "master");
	}
}
@AfterTest
public static void tearDown()
{
	LogoutPage logut =PageFactory.initElements(driver, LogoutPage.class);
	logut.adminLogout();
	driver.quit();
}
}









==========================================================================================
//preparing TestScript class for supplier Test case
=============================================================================================
package driverFactory;

import org.openqa.selenium.support.PageFactory;
import org.testng.Reporter;
import org.testng.annotations.Test;

import com.relevantcodes.extentreports.ExtentReports;
import com.relevantcodes.extentreports.ExtentTest;
import com.relevantcodes.extentreports.LogStatus;

import applicationLayer.SupplierPage;
import config.AppUtil1;
import utilities.ExcelFileUtil;

public class TestScript extends AppUtil1{
String inputpath ="./FileInput/SupplierData.xlsx";
String outputpath="./FileOutput/SupplierResults.xlsx";
ExtentReports reports;
ExtentTest logger;
String TCsheet ="Supplier";
@Test
public void startTest() throws Throwable
{
	reports = new ExtentReports("./ExtentReports/Supplier.html");
	ExcelFileUtil xl = new ExcelFileUtil(inputpath);
	int rc = xl.rowCount(TCsheet);
	Reporter.log("No of rows are::"+rc,true);
	for(int i=1;i<=rc;i++)
	{
		logger =reports.startTest("Validate Supplier Test");
		String sname = xl.getCellData(TCsheet, i, 0);
		String address = xl.getCellData(TCsheet, i, 1);
		String city = xl.getCellData(TCsheet, i, 2);
		String country = xl.getCellData(TCsheet, i, 3);
		String cperson = xl.getCellData(TCsheet, i, 4);
		String pnumber = xl.getCellData(TCsheet, i, 5);
		String email = xl.getCellData(TCsheet, i, 6);
		String mnumber = xl.getCellData(TCsheet, i, 7);
		String notes = xl.getCellData(TCsheet, i, 8);
		logger.log(LogStatus.INFO, sname+"  "+address+"   "+city+"   "+country+"   "+cperson+"   "+pnumber+"   "+email+"    "+mnumber+"   "+notes);
		SupplierPage sup =PageFactory.initElements(driver, SupplierPage.class);
		boolean res = sup.addSupplier(sname, address, city, country, cperson, pnumber, email, mnumber, notes);
		if(res)
		{
			xl.setCellData(TCsheet, i, 9, "Pass", outputpath);
			logger.log(LogStatus.PASS, "Add Supplier Success");
		}
		else
		{
			xl.setCellData(TCsheet, i, 9, "Fail", outputpath);
			logger.log(LogStatus.FAIL, "Add Supplier Fail");
		}
		reports.endTest(logger);
		reports.flush();
		
	}
	
}
}

28-08-2024

 What is Page Object model using Selenium Webdriver?
1- It is design pattern in which will help you to maintain the code and code duplication, which is a crucial thing in Test automation.
2- You can store all locators and respective methods in the separate class and Call them from the test in which you have to use. So the benefit from this will be if any changes in Page then you do not have to modify the test simply modify the respective page and that all.
3- You can create a layer between your test script and application page, which you have to automate.
4- In other words, it will behave as Object repository where all locators are saved.
 Implementation of Page Object model using Selenium Webdriver
1 – Page Object model without PageFactory
2- Page Object Model with Pagefactory.
Selenium has built in class called PageFactory, which they mainly created for Page Object purpose, which allows you to store elements.
Advantages of using Page Object Model
•	Increases code reusability - code to work with events of a page is written only once and used in different test cases
•	Improves code maintainability - any UI change leads to updating the code in page object classes only leaving the test classes unaffected
•	Makes code more readable and easy to understand.
How to store locators
@FindBy(locataorname=”value”)
Webelement   user;




import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.support.CacheLookup;
import org.openqa.selenium.support.FindBy;
import org.openqa.selenium.support.How;

* This class will store all the locator and methods of login page
*
*/
public class LoginPage 
{

WebDriver driver;



By username=By.id("user_login");
By password=By.xpath(".//*[@id='user_pass']");
By loginButton=By.name("wp-submit");


public LoginPage(WebDriver driver)
{
this.driver=driver;
}


public void loginToWordpress(String userid,String pass)
{

driver.findElement(username).sendKeys(userid);
driver.findElement(password).sendKeys(pass);
driver.findElement(loginButton).click();

}


public void typeUserName(String uid)
{

driver.findElement(username).sendKeys(uid);
}

public void typePassword(String pass)
{

driver.findElement(password).sendKeys(pass);
}

public void clickOnLoginButton()
{
driver.findElement(loginButton).click();
}
}


package com.wordpress.Testcases;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.testng.annotations.Test;

import com.wordpress.Pages.LoginPage;

public class VerifyWordpressLogin 
{


@Test
public void verifyValidLogin()
{

WebDriver driver=new FirefoxDriver();

driver.manage().window().maximize();

driver.get("http://demosite.center/wordpress/wp-login.php");

LoginPage login=new LoginPage(driver);



login.clickOnLoginButton();


driver.quit();

}


}


Page Object Model using Selenium Webdriver with Page Factory
Selenium has built in class called PageFactory, which they mainly created for Page Object purpose, which allows you to store elements in cache lookup.
The only difference, which you will get without PageFactory and with PageFactory, is just initElement statement.Let us check the code and will see what changes required for with PageFactory Approach
Code for Page Object Model Using Selenium Webdriver using Page Factory

http://artoftesting.com/automationTesting/pageObjectModel.html
29-08-2024
HYBRID FRAME WORK
//preparing Property file
==============================================
Browser = chrome
Url = http://webapp.qedgetech.com/

===============================================

//preparing function library  class
==================================================
package commonFunctions;

import java.io.FileInputStream;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.time.Duration;
import java.util.Date;
import java.util.Properties;

import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;
import org.testng.Assert;
import org.testng.Reporter;

public class FunctionLibrary {
public static WebDriver driver;
public static Properties conpro;
//method for launch ing browser
public static WebDriver startBrowser()throws Throwable
{
	conpro = new Properties();
	conpro.load(new FileInputStream("./PropertyFiles\\Environment.properties"));
	if(conpro.getProperty("Browser").equalsIgnoreCase("chrome"))
	{
		driver = new ChromeDriver();
		driver.manage().window().maximize();
	}
	else if(conpro.getProperty("Browser").equalsIgnoreCase("firefox"))
	{
		driver = new FirefoxDriver();
	}
	else
	{
		Reporter.log("Browser value is Not Matching",true);
	}
	return driver;
}
//method for launch url
public static void openUrl()
{
	driver.get(conpro.getProperty("Url"));
}
//method for wait for any webelement 
public static void waitForElement(String LocatorType,String LocatorValue,String TestData)
{
WebDriverWait mywait = new WebDriverWait(driver, Duration.ofSeconds(Integer.parseInt(TestData)));
if(LocatorType.equalsIgnoreCase("xpath"))
{
	mywait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath(LocatorValue)));
}
if(LocatorType.equalsIgnoreCase("id"))
{
	mywait.until(ExpectedConditions.visibilityOfElementLocated(By.id(LocatorValue)));
}
if(LocatorType.equalsIgnoreCase("name"))
{
	mywait.until(ExpectedConditions.visibilityOfElementLocated(By.name(LocatorValue)));
}
}
//method for any textbox
public static void typeAction(String LocatorType,String LocatorValue,String TestData)
{
	if(LocatorType.equalsIgnoreCase("xpath"))
	{
		driver.findElement(By.xpath(LocatorValue)).clear();
		driver.findElement(By.xpath(LocatorValue)).sendKeys(TestData);
	}
	if(LocatorType.equalsIgnoreCase("id"))
	{
		driver.findElement(By.id(LocatorValue)).clear();
		driver.findElement(By.id(LocatorValue)).sendKeys(TestData);
	}
	if(LocatorType.equalsIgnoreCase("name"))
	{
		driver.findElement(By.name(LocatorValue)).clear();
		driver.findElement(By.name(LocatorValue)).sendKeys(TestData);
	}
	
}
//method for click elements like buttons,images,links,checkboxes and radio button
public static void clickAction(String LocatorType,String LocatorValue)
{
	if(LocatorType.equalsIgnoreCase("xpath"))
	{
		driver.findElement(By.xpath(LocatorValue)).click();
	}
	if(LocatorType.equalsIgnoreCase("name"))
	{
		driver.findElement(By.name(LocatorValue)).click();
	}
	if(LocatorType.equalsIgnoreCase("id"))
	{
		driver.findElement(By.id(LocatorValue)).sendKeys(Keys.ENTER);
	}
}
//method for validating title
public static void validateTitle(String Expected_Title)
{
	String Actual_Title = driver.getTitle();
	try {
	Assert.assertEquals(Actual_Title, Expected_Title, "Title is Not matching");
	}catch(Throwable t)
	{
		System.out.println(t.getMessage());
	}
}
//method for closing browser
public static void closeBrowser()
{
	driver.quit();
}
//method for gneratedate
public static String generateDate()
{
	Date date = new Date();
	DateFormat df = new SimpleDateFormat("YYYY_MM_dd hh_mm_ss");
	return df.format(date);
}
}
======================================

02-09-2024
=========================================================
search-panel = //span[@data-caption='Search']
search-textbox = //input[@id='psearch']
search-button = //button[@id='btnsubmit']
============================================================
//method for selecting items in listboxes
public static void dropDownAction(String LocatorType,String Locatorvalue,String TestData)
{
	if(LocatorType.equalsIgnoreCase("name"))
	{
		int value = Integer.parseInt(TestData);
		Select element = new Select(driver.findElement(By.name(Locatorvalue)));
		element.selectByIndex(value);
		
	}
	if(LocatorType.equalsIgnoreCase("xpath"))
	{
		int value = Integer.parseInt(TestData);
		Select element = new Select(driver.findElement(By.xpath(Locatorvalue)));
		element.selectByIndex(value);
	}
	if(LocatorType.equalsIgnoreCase("id"))
	{
		int value = Integer.parseInt(TestData);
		Select element = new Select(driver.findElement(By.id(Locatorvalue)));
		element.selectByIndex(value);
	}
}
//method for capture stock number into note pad
public static void captureStock(String LocatorType,String LocatorValue)throws Throwable
{
	String stockNum="";
	if(LocatorType.equalsIgnoreCase("name"))
	{
		stockNum =driver.findElement(By.name(LocatorValue)).getAttribute("value");
		
	}
	if(LocatorType.equalsIgnoreCase("xpath"))
	{
		stockNum =driver.findElement(By.xpath(LocatorValue)).getAttribute("value");
		
	}
	if(LocatorType.equalsIgnoreCase("id"))
	{
		stockNum =driver.findElement(By.id(LocatorValue)).getAttribute("value");
		
	}
	//create new notepad into capturedata folder
	FileWriter fw = new FileWriter("./CaptureData/stockNumber.txt");
	BufferedWriter bw =new BufferedWriter(fw);
	bw.write(stockNum);
	bw.flush();
	bw.close();
	
	
}
//verify stock number from stock table
public static void stockTable()throws Throwable
{
	//read stock number from above notepad
	FileReader fr = new FileReader("./CaptureData/stockNumber.txt");
	BufferedReader br = new BufferedReader(fr);
	//read stock number from notepad
	String Exp_Data =br.readLine();
	if(!driver.findElement(By.xpath(conpro.getProperty("search-textbox"))).isDisplayed())
		driver.findElement(By.xpath(conpro.getProperty("search-panel"))).click();
	driver.findElement(By.xpath(conpro.getProperty("search-textbox"))).clear();
	//enter stock number into textbox
	driver.findElement(By.xpath(conpro.getProperty("search-textbox"))).sendKeys(Exp_Data);
	//click search button
	driver.findElement(By.xpath(conpro.getProperty("search-button"))).click();
	Thread.sleep(4000);
	String Act_Data = driver.findElement(By.xpath("//table[@class='table ewTable']/tbody/tr[1]/td[8]/div/span/span")).getText();
	Reporter.log(Exp_Data+"     "+Act_Data,true);
	try {
	Assert.assertEquals(Act_Data, Exp_Data, "Stock Number Not Matching");
	}catch(Throwable t)
	{
		System.out.println(t.getMessage());
	}
}
03=09=2024

//method capture supplier number into note pad
public static void captureSup(String LocatorName,String LocatorValue)throws Throwable
{
	String supplierNum="";
	if(LocatorName.equalsIgnoreCase("xpath"))
	{
		supplierNum = driver.findElement(By.xpath(LocatorValue)).getAttribute("value");
	}
	if(LocatorName.equalsIgnoreCase("name"))
	{
		supplierNum = driver.findElement(By.name(LocatorValue)).getAttribute("value");
	}
	if(LocatorName.equalsIgnoreCase("id"))
	{
		supplierNum = driver.findElement(By.id(LocatorValue)).getAttribute("value");
	}
	//create note pad and write supplier number
	FileWriter fw = new FileWriter("./CaptureData/suppliernumber.txt");
	BufferedWriter bw = new BufferedWriter(fw);
	bw.write(supplierNum);
	bw.flush();
	bw.close();
}
03-09-2024
package driverFactory;

import org.openqa.selenium.WebDriver;

import com.relevantcodes.extentreports.ExtentReports;
import com.relevantcodes.extentreports.ExtentTest;

import commonFunctions.FunctionLibrary;
import utilities.ExcelFileUtil;

public class DriverScript {
String inputpath ="./FileInput/Controller.xlsx";
String outputpath ="./FileOutput/HyridResults.xlsx";
ExtentReports reports;
ExtentTest logger;
public static WebDriver driver;
String TCSheet ="MasterTestCases";
public void startTest() throws Throwable
{
	String Module_Status="";
	String Module_New="";
	//create instance object for Excelfile util class
	ExcelFileUtil xl = new ExcelFileUtil(inputpath);
	//iterate all rows in TCSheet
	for(int i=1;i<=xl.rowCount(TCSheet);i++)
	{
		if(xl.getCellData(TCSheet, i, 2).equalsIgnoreCase("Y"))
		{
			//read corresponding sheet into TCMOdule variable
			String TCModule =xl.getCellData(TCSheet, i, 1);
			//iterate all rows in TCModule
			for(int j=1;j<=xl.rowCount(TCModule);j++)
			{
				String Description = xl.getCellData(TCModule, j, 0);
				String Object_Type = xl.getCellData(TCModule, j, 1);
				String Ltype = xl.getCellData(TCModule, j, 2);
				String LValue = xl.getCellData(TCModule, j, 3);
				String TData = xl.getCellData(TCModule, j, 4);
				try {
					if(Object_Type.equalsIgnoreCase("startBrowser"))
					{
						driver =FunctionLibrary.startBrowser();
					}
					if(Object_Type.equalsIgnoreCase("openUrl"))
					{
						FunctionLibrary.openUrl();
					}
					if(Object_Type.equalsIgnoreCase("waitForElement"))
					{
						FunctionLibrary.waitForElement(Ltype, LValue, TData);
					}
					if(Object_Type.equalsIgnoreCase("typeAction"))
					{
						FunctionLibrary.typeAction(Ltype, LValue, TData);
					}
					if(Object_Type.equalsIgnoreCase("clickAction"))
					{
						FunctionLibrary.clickAction(Ltype, LValue);
					}
					if(Object_Type.equalsIgnoreCase("validateTitle"))
					{
						FunctionLibrary.validateTitle(TData);
					}
					if(Object_Type.equalsIgnoreCase("closeBrowser"))
					{
						FunctionLibrary.closeBrowser();
					}
					if(Object_Type.equalsIgnoreCase("dropDownAction"))
					{
						FunctionLibrary.dropDownAction(Ltype, LValue, TData);
					}
					if(Object_Type.equalsIgnoreCase("captureStock"))
					{
						FunctionLibrary.captureStock(Ltype, LValue);
					}
					if(Object_Type.equalsIgnoreCase("stockTable"))
					{
						FunctionLibrary.stockTable();
					}
					
					//write as pass into status cell in TCModule
					xl.setCellData(TCModule, j, 5, "Pass", outputpath);
					Module_Status="True";;
				}catch(Exception e)
				{
					System.out.println(e.getMessage());
					//write as Fail into status cell in TCModule
					xl.setCellData(TCModule, j, 5, "Fail", outputpath);
					Module_New="False";
				}
				if(Module_Status.equalsIgnoreCase("True"))
				{
					xl.setCellData(TCSheet, i, 3, "Pass", outputpath);
				}
				if(Module_New.equalsIgnoreCase("False"))
				{
					xl.setCellData(TCSheet, i, 3, "Fail", outputpath);
				}
				
			}
			
		}
		else
		{
			//write as blocked into status cell in TCsheet
			xl.setCellData(TCSheet, i, 3, "Blocked", outputpath);
		}
	}
}
}

==================================================================
//preparing apptest
===================================================================
package driverFactory;

import org.testng.annotations.Test;

public class AppTest {
@Test
public void kickStart() throws Throwable
{
	DriverScript ds = new DriverScript();
	ds.startTest();
}
}






































 




































































	
	












































	 
































			



		
	

	





















		


		





















































	























































		
	




	









		






































		
















	
















		



	
	










			




		























































		






























		


















		


















		


















		
















