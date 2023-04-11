# Week 3 Review - Automated UI Testing with Java

## Selenium WebDriver - Java (Continued)
---
### Driver Interactions (Continued)
- **POM (Page Object Model)**
    - A design pattern used in test automation to create an object repository for web UI elements
    - Separates the UI elements and the associated methods into separate classes
    - ```java
      public class LoginPage {
          private WebDriver driver;
      
          @FindBy(name = "username")
          private WebElement username;
      
          @FindBy(name = "password")
          private WebElement password;
      
          @FindBy(css = "input[type='submit']")
          private WebElement submitButton;
      
          public LoginPage(WebDriver driver) {
              this.driver = driver;
              PageFactory.initElements(driver, this);
          }
      }
    - The `PageFactory` is used to initialize page elements with the `@FindBy` annotation
- **PageFactory**
    - A class in Selenium that initializes Page Objects
    - Used in conjunction with the POM design pattern to create and manage page objects
    - Allows us to use annotations such as @FindBy to locate and identify web elements on a page
    - Examples of `@FindBy`:
        - Find by id
            - ```java
              @FindBy(id = "username")
              WebElement usernameField;
        - Find by name
            - ```java
              @FindBy(name = "password")
              WebElement passwordField;
        - Find by class name
            - ```java
              @FindBy(className = "submit-button")
              WebElement submitButton;
        - Find by tag name
            - ```java
              @FindBy(tagName = "h1")
              WebElement heading;
        - Find by link text
            - ```java
              @FindBy(linkText = "Sign In")
              WebElement signInLink;
        - Find by CSS Selector
            - ```java
              @FindBy(css = "#user-info .username")
              WebElement usernameLabel;
        - Find by XPath
            - ```java
              @FindBy(xpath = "//div[@class='content']//a[@href='/logout']")
              WebElement logoutLink;
- **Upload File**
    - Uses the `sendKeys()` method of the `WebElement` class to specify the file path of the file to be uploaded
    - ```java
      WebElement uploadElement = driver.findElement(By.id("uploadFile"));
      uploadElement.sendKeys("C:\\file_to_upload.txt");
- **Get Snapshot**
    - To take a screenshot in Selenium, use the `TakesScreenshot` interface to capture the screenshot and save it as a file with the method `getScreenshotAs()`
    - It can be saved as a file or returned as a byte array
    - ```java
      TakesScreenshot ts = (TakesScreenshot) driver;
      File source = ts.getScreenshotAs(OutputType.FILE);
      FileUtils.copyFile(source, new File("C:\\screenshot.png"));
- **Actions API**
    - A set of advanced interactions that can be performed on web elements
    - Allows for complex interactions such as drag and drop, mouse hover, double click, etc.
    - Can be used to chain multiple actions together using the `build()` and `perform()` methods
    - `build()`: Used to build a composite action containing a sequence of individual actions
    - `perform()`: Used to execute the composite actions on the web page
    - Examples:
        - Moving the mouse to an element and clicking it
            - ```java
              Actions actions = new Actions(driver);
              WebElement element = driver.findElement(By.id("my-element"));
              actions.moveToElement(element).click().perform();
        - Double clicking an element
            - ```java
              Actions actions = new Actions(driver);
              WebElement element = driver.findElement(By.id("my-element"));
              actions.doubleClick(element).perform();
        - Sending keys using the Actions API
            - ```java
              Actions actions = new Actions(driver);
              WebElement element = driver.findElement(By.id("my-element"));
              actions.sendKeys(element, "Hello, world!").perform();
- **Resize Browser**
- **Handle Popups**
- **Change Tabs**
## BDD - Gherkin / Cucumber
---
### Orientation
---
- **BDD**
- **Gherkin**
### Cucumber
---
- **Cucumber**
- **Feature File**
- **Given**
- **When**
- **Then**
- **Scenario**
### Integration
---
- **Glue Code**
- **Step Implementations**
- **JUnit Runner**
- **Scenario Outline**
