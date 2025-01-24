**task - 01**

**COMPANY NAME**: CODTECH IT SOLUTION PVT.LTD

**NAME**: OM JOSHI

**INTER ID**: CT6WKCL.

**DOMAIN**: SOFTWARE TESTING.

**BATCH DURATION**: January 5th,2025 to February 20TH,2025.

**MENTOR NAME**: NEELA SANTHOSH

**DESCRIPTION**:  AUTOMATE THE TESTING OF A SAMPLE WEB APPLICATION’S LOGIN

Automating the Testing of a Sample Web Application’s Login Automated testing is an essential practice for ensuring the reliability and performance of a web application. In this case, we will walk through the process of automating the testing of a sample web application’s login feature using Selenium WebDriver, a popular tool for automating web browsers.

Prerequisites To automate the testing of the login functionality, the following tools and libraries are required:

Selenium WebDriver: For automating browser actions. JUnit or TestNG: To run and structure tests. Maven (or Gradle): For managing dependencies. Java: Programming language for writing the test scripts. Browser Driver (e.g., ChromeDriver): Needed to interface Selenium with the browser. Step 1: Setting Up the Project To begin, set up a Java Maven project in your favorite Integrated Development Environment (IDE) such as IntelliJ IDEA or Eclipse.

Add Maven dependencies: In your pom.xml file, include the following dependencies for Selenium and JUnit. xml Copy code org.seleniumhq.selenium selenium-java 4.0.0

org.junit.jupiter junit-jupiter-api 5.7.0 test Download Browser Driver: Depending on the browser you intend to use (e.g., Chrome, Firefox), download the respective WebDriver (e.g., ChromeDriver) and add it to your project’s src/main/resources folder or system path. Step 2: Writing the Test Script Create a test class for the login functionality. The script will open the browser, navigate to the login page, enter credentials, submit the form, and verify the result. java Copy code import org.junit.jupiter.api.; import org.openqa.selenium.; import org.openqa.selenium.chrome.ChromeDriver; import static org.junit.jupiter.api.Assertions.*;
public class LoginTest // {

WebDriver driver;

@BeforeEach public void setUp() { // Set the path for ChromeDriver System.setProperty("webdriver.chrome.driver", "path/to/chromedriver"); driver = new ChromeDriver(); }

@Test public void testValidLogin() { // Navigate to the login page driver.get("https://example.com/login");

WebElement usernameField = driver.findElement(By.id("username"));
WebElement passwordField = driver.findElement(By.id("password"));
WebElement loginButton = driver.findElement(By.id("loginButton"));

usernameField.sendKeys("testuser");
passwordField.sendKeys("password123");

loginButton.click();
assertEquals("https://example.com/dashboard", driver.getCurrentUrl());
}

@Test public void testInvalidLogin() { // Navigate to the login page driver.get("https://example.com/login");
WebElement usernameField = driver.findElement(By.id("username"));
WebElement passwordField = driver.findElement(By.id("password"));
WebElement loginButton = driver.findElement(By.id("loginButton"));

usernameField.sendKeys("invalidUser");
passwordField.sendKeys("wrongPassword");

loginButton.click();

WebElement errorMessage = driver.findElement(By.id("errorMessage"));
assertTrue(errorMessage.isDisplayed());
}
{
@AfterEach public void tearDown() { driver.quit(); } }

Step 3: Test Explanation Setup (@BeforeEach): This method initializes the WebDriver and opens a new instance of the browser before each test. Test for Valid Login: In the testValidLogin method, the script: Navigates to the login page. Locates the username, password input fields, and login button using their HTML attributes (such as id). Enters valid credentials and clicks the login button. Verifies that the user is redirected to the dashboard page. Test for Invalid Login: In the testInvalidLogin method, the script performs similar steps but enters invalid credentials and checks that an error message appears. Teardown (@AfterEach): This method closes the browser after each test to ensure no browser instances remain open.

Step 4: Running the Test To execute the test, simply run the JUnit test in your IDE or use the Maven command:

bash Copy code mvn test This will run both the valid and invalid login tests.

Step 5: Enhancing the Test Add Assertions: You can enhance the tests by adding more detailed assertions. For example, checking for specific elements (e.g., login success message or error text) or verifying the presence of certain UI elements after login. Parameterized Testing: You can use JUnit’s @ParameterizedTest to test different sets of login credentials (valid and invalid). Handling Waits: Use WebDriverWait to handle dynamic elements or situations where page loading time may vary. Conclusion Automating the testing of a web application's login functionality with Selenium WebDriver improves efficiency, consistency, and test coverage. This simple approach to automation ensures that the login page behaves as expected under different conditions. The above steps guide you in setting up the necessary environment, writing effective test scripts, and running them for both valid and invalid login cases.
----------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------
**DELIVERABLE: A SCRIPT REPOSITORY AND A TEST EXECUTION REPORT.**

Script Repository
A Script Repository is a centralized platform or storage location where automated test scripts, related code, and resources are maintained. It serves as the main archive for scripts used in testing, offering a structured way to organize and manage them. The repository helps ensure that testing scripts are easily accessible, version-controlled, and shared among the team members working on the project.

Key features of a script repository:

Version Control: Tracks changes to the scripts over time, allowing users to revert to previous versions if necessary.
Collaboration: Multiple team members can contribute to the repository, enhancing collaboration and reducing duplication of effort.
Organization: Scripts can be categorized based on function, feature, or project to make them easier to find and manage.
Centralized Storage: With a centralized repository, all members have access to the latest version of scripts, improving consistency across testing efforts.
Popular tools used to create script repositories include Git, Bitbucket, and GitHub, which support features like branching, merging, and tracking code changes.

Test Execution Report
A Test Execution Report is a document or output file that summarizes the results of executed test cases during the testing process. It provides a detailed overview of the test execution status, helping stakeholders understand the effectiveness of the tests and any issues that need to be addressed.

Key elements of a Test Execution Report:

Test Case Details: The names or IDs of the test cases executed, along with any associated descriptions or IDs.
Execution Status: Information about whether each test case passed or failed. If a test fails, it usually includes error messages or stack traces to assist in troubleshooting.
Execution Time: The duration each test case took to execute, which can help identify performance issues.
Test Coverage: A summary of how much of the system or application was tested, often presented in terms of feature coverage or lines of code tested.
Defects: Any bugs or issues found during testing are often listed, including their severity, status, and any steps to reproduce.
Summary and Trends: A high-level summary that shows trends, such as increasing or decreasing test pass rates, which can indicate the stability of the application.
A test execution report is important because it offers stakeholders (testers, developers, managers) insight into the quality and stability of the software. It helps decision-makers understand whether the system is ready for deployment or needs more work.

Tools like JUnit, TestNG, Selenium, and others often generate these reports automatically. The format of the report can vary depending on the tools and preferences, but common formats include HTML, PDF, and XML.

Conclusion
In short, a Script Repository serves as a secure, organized location for storing and managing test scripts, enabling collaboration and version control. Meanwhile, a Test Execution Report provides a comprehensive view of the test execution results, helping identify defects and track test progress. Both are essential components of the software testing process, ensuring efficient testing, clear communication, and a reliable product release.
----------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------
