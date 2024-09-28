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











































	
	












































	 
































			



		
	

	





















		


		





















































	























































		
	




	









		






































		
















	
















		



	
	










			




		























































		






























		


















		


















		


















		
















