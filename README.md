# Run Selenium Tests With Codeception — TestMu AI (Formerly LambdaTest)

![image](https://user-images.githubusercontent.com/70570645/171664104-53b037da-d823-4326-b7fb-71034fea0040.png)


<p align="center">
  <a href="https://www.testmuai.com/blog/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample" target="_bank">Blog</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/support/docs/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample" target="_bank">Docs</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/learning-hub/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample" target="_bank">Learning Hub</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/newsletter/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample" target="_bank">Newsletter</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/certifications/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample" target="_bank">Certifications</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.youtube.com/@TestMuAI" target="_bank">YouTube</a>
</p>
&emsp;
&emsp;
&emsp;

*Learn how to use Codeception framework to configure and run your PHP automation testing scripts on the TestMu AI platform*

[<img height="58" width="200" src="https://user-images.githubusercontent.com/70570645/171866795-52c11b49-0728-4229-b073-4b704209ddde.png">](https://accounts.lambdatest.com/register?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)


## Table Of Contents

* [Pre-requisites](#pre-requisites)
* [Run Your First Test](#run-your-first-test)
* [Local Testing With Codeception](#testing-locally-hosted-or-privately-hosted-projects)


## Prerequisites

Before you begin automation testing with Selenium and Codeception, you would need to:

* Make sure that you have the latest **PHP** installed on your system. You can download and install **PHP** using following commands in the terminal:

* **MacOS:** Previous versions of **MacOS** have **PHP** installed by default. But for the latest **MacOS** versions starting with **Monterey**, **PHP** has to be downloaded and installed manually by using below commands: 

  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  brew install php
  ```
* **Windows:** 

  ```bash
  sudo apt-get install curl libcurl3 libcurl3-dev php
  ```

**Note:** For **Windows**, you can download **PHP** from [here](http://windows.php.net/download/). Also, refer to this [documentation](http://php.net/manual/en/install.windows.php) for ensuring the accessibility of PHP through Command Prompt(cmd).


## Download composer in the project directory (use below links)
* [Linux/MacOS](https://getcomposer.org/download/)
* [Windows](https://getcomposer.org/doc/00-intro.md#installation-windows)

**Note:** To use the **composer** command directly, it either should have been downloaded in the project directory or should be accessible globally which can be done by the command below(if not executed already as per composed download page steps):

  ```bash
  mv composer.phar /usr/local/bin/composer
  ```

### Installing Selenium Dependencies And Tutorial Repo

**Step 1:** Clone the TestMu AI Codeception-selenium-sample repository and navigate to the code directory as shown below:

```bash
git clone https://github.com/LambdaTest/codeception-selenium-sample
cd codeception-selenium-sample
```

**Step 2:** Install the composer dependencies in the current project directory using the command below:
```bash
composer install
```

### Setting Up Your Authentication

Make sure you have your TestMu AI credentials with you to run test automation scripts. You can get these credentials from the [TestMu AI Automation Dashboard](https://automation.lambdatest.com/build?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample) or by your [TestMu AI Profile](https://accounts.lambdatest.com/login?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample).

**Step 3:** Set TestMu AI `Username` and `Access Key` in environment variables.
  
  * For **Linux/macOS**:
  ```bash
  export LT_USERNAME="YOUR_USERNAME" export LT_ACCESS_KEY="YOUR ACCESS KEY"
  ```
  
  * For **Windows**:
  ```bash
  set LT_USERNAME="YOUR_USERNAME" set LT_ACCESS_KEY="YOUR ACCESS KEY"
  ```


## Run Your First Test


>**Test Scenario**: Check out the sample acceptance [FirstCest.php](https://github.com/LambdaTest/codeception-selenium-sample/blob/master/tests/acceptance/FirstCest.php) file. This Codeception Selenium script tests a sample to-do list app by marking couple items as done, adding a new item to the list and finally displaying the count of pending items as output.

### Configuration Of Your Test Capabilities

**Step 4:** Refer to the [acceptance.yml](https://github.com/LambdaTest/codeception-selenium-sample/blob/master/tests/acceptance.suite.yml) file to update your test capabilities. 

Notice the declaration of class name **“AcceptanceTester”**. We used this class to specify test configuration, port number, browser name, browser version and other desired capabilities.

> **Note:** You can generate capabilities for your test requirements with the help of **[Desired Capability Generator](https://www.testmuai.com/capabilities-generator/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)**.

### Executing the Test

**Step 5:** The tests can be executed in the terminal using the following command:

```bash
./vendor/bin/codecept run --steps
```

Your test results would be displayed on the test console (or command-line interface if you are using terminal/cmd) and on TestMu AI Automation Dashboard. 


## Testing Locally Hosted Or Privately Hosted Projects

You can test your locally hosted or privately hosted projects with TestMu AI Selenium grid using TestMu AI Tunnel. All you would have to do is set up an SSH tunnel using tunnel and pass toggle `tunnel = True` via desired capabilities. TestMu AI Tunnel establishes a secure SSH protocol based tunnel that allows you in testing your locally hosted or privately hosted pages, even before they are live.

Refer our [TestMu AI Tunnel documentation](https://www.testmuai.com/support/docs/testing-locally-hosted-pages/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample) for more information.

Here’s how you can establish TestMu AI Tunnel.

Download the binary file of:
* [TestMu AI Tunnel for Windows](https://downloads.lambdatest.com/tunnel/v3/windows/64bit/LT_Windows.zip)
* [TestMu AI Tunnel for macOS](https://downloads.lambdatest.com/tunnel/v3/mac/64bit/LT_Mac.zip)
* [TestMu AI Tunnel for Linux](https://downloads.lambdatest.com/tunnel/v3/linux/64bit/LT_Linux.zip)

Open command prompt and navigate to the binary folder.

Run the following command:

```bash
LT --user {user’s login email} --key {user’s access key}
```
So if your user name is lambdatest@example.com and key is 123456, the command would be:

```bash
LT --user lambdatest@example.com --key 123456
```
Once you are able to connect **TestMu AI Tunnel** successfully, you would just have to pass on tunnel capabilities in the code shown below :

**Tunnel Capability**

```
$capability = array(
	"LT:Options" => array(
		"username" => "LT_USERNAME",
		"accessKey" => "LT_ACCESS_KEY",
		"tunnel" => true,
	)
);
```


## Additional Links
***
* [Advanced Configuration for Capabilities](https://www.testmuai.com/support/docs/selenium-automation-capabilities/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)
* [How to test locally hosted apps](https://www.testmuai.com/support/docs/testing-locally-hosted-pages/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)
* [How to integrate TestMu AI with CI/CD](https://www.testmuai.com/support/docs/integrations-with-ci-cd-tools/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)


## Documentation & Resources :books:

      
Visit the following links to learn more about TestMu AI's features, setup and tutorials around test automation, mobile app testing, responsive testing, and manual testing.

* [TestMu AI Documentation](https://www.testmuai.com/support/docs/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)
* [TestMu AI Blog](https://www.testmuai.com/blog/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)
* [TestMu AI Learning Hub](https://www.testmuai.com/learning-hub/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)    


## TestMu AI Community :busts_in_silhouette:

The [TestMu AI Community](https://community.testmuai.com/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample) allows people to interact with tech enthusiasts. Connect, ask questions, and learn from tech-savvy people. Discuss best practises in web development, testing, and DevOps with professionals from across the globe 🌎


## What's New At TestMu AI ❓

To stay updated with the latest features and product add-ons, visit [Changelog](https://changelog.testmuai.com/) 
      

## 🚀 [LambdaTest is Now TestMu AI](https://www.testmuai.com/lambdatest-is-now-testmuai/)

👋 Welcome to TestMu AI, the next evolution of LambdaTest. As of January 2026, LambdaTest has officially rebranded to TestMu AI. We have evolved from a cross-browser testing cloud into a unified, AI-native quality engineering platform designed for the modern DevOps era.

Whether you have been part of the LambdaTest community for years or are just discovering TestMu AI, our mission remains the same: to help you ship faster with high-scale test execution, autonomous testing, and deep quality analytics.

**🔄 Our Rebrand Journey**

We chose the name TestMu AI to reflect our shift towards intelligent, autonomous testing. While our identity has changed, our core technology and commitment to the testing community stay the same.

**✨ Specialties**

- 🤖 AI-Native Test Execution (Formerly LambdaTest)
- ⚡ Autonomous Test Automation
- 🌐 Cross-Browser & Mobile Testing
- 📊 Unified Quality Intelligence

👉 Find [LambdaTest's New Home](https://www.testmuai.com/).

## We are here to help you :headphones:

* Got a query? we are available 24x7 to help. [Contact Us](mailto:support@testmuai.com)
* For more info, visit - [TestMu AI](https://www.testmuai.com/?utm_source=github&utm_medium=repo&utm_campaign=codeception-selenium-sample)
