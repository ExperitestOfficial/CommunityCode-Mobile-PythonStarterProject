# Community Code - Mobile - Python Starter Project
This project demonstrates how to write tests for Continuous Testing Cloud using Python. Once cloned and set up properly, it runs as is.

## Setting Up the Sample Project

1. Clone the sample project.
    ```bash
    git clone https://github.com/ExperitestOfficial/CommunityCode-Mobile-PythonStarterProject
    cd CommunityCode-Mobile-PythonStarterProject
    ```
1. Set up authentication by updating these  parameters in [cloud.properties](cloud.properties):
    * url - URL for the cloud to run the test in. For example, https://company.digitai.ai/
    * accessKey -  Personal authentication. See [Obtaining Access Key](https://docs.experitest.com/pages/viewpage.action?pageId=52593435) to learn how to obtain an access key.
1. Make sure that Python 3 is installed.
1. Install the dependencies.
```bash
pip install -r requirements.txt
```

## Running Tests
To run all tests in this project, run this on the command line: 

```bash
python -m unittest test
```

## Upload Application to the Cloud

The example tests in this project use a demo application.
To upload your own application to cloud:
1. Log in to the cloud using a browser.
1. In the left menu click Applications.
1. Click Upload.
1. Click the application file to upload.

In your tests, change *com.experitest.ExperiBank* (and activity if needed) in desired capabilities for your application, in the following lines:

* For Android:
```
self.dc['appPackage'] = 'com.experitest.ExperiBank'
self.dc['appActivity'] = '.LoginActivity'
```
* For iOS:
```
self.dc['app'] = 'cloud:com.experitest.ExperiBank'
self.dc['bundleId'] = 'com.experitest.ExperiBank'
```
For more ways to upload your application to the cloud, see [Native Applications Testing](https://docs.experitest.com/display/TE/Native+Applications+Testing).

## Desired Capabilities

Continuous Cloud Testing expands Appium's capabilities and allows better control over the device and test.
In these examples we use the desired capabilities to set the test name and choose devices to run on, as well as set the application.
See [Capabilities in Appium Based Tests](https://docs.experitest.com/display/TE/Capabilties+in+Appium+Based+Tests) to learn how to customize the desired capabilities for your tests.

## Documentation
To find out more about Continuous Cloud Testing usage, features, and best practices, visit our online [documentation](https://docs.experitest.com/display/TE/Test+Execution+Home).

## Support
If you encounter an issue that is not covered here or in our online documentation, contact us at [support@digital.ai](mailto:support@digital.ai).
