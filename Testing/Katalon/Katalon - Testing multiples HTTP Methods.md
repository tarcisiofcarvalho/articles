## Katalon - Testing multiples methods GET, POST, UPDATE and DELETE

If you would like to how your API handles HTTP methods, you can use the code below as reference. The scenario behind this code is related to an API that should just support POST request, the other ones should be return HTTP code 405.


```java
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.cucumber.keyword.CucumberBuiltinKeywords as CucumberKW
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import internal.GlobalVariable as GlobalVariable
import com.kms.katalon.core.testobject.RequestObject as RequestObject

/**
 * Testing the HTTP Method POST
 */
RequestObject request = findTestObject('<add here the name of you object in Object Repository>')

response = WS.sendRequest(request)

WS.verifyResponseStatusCode(response, 200)

/**
 * Testing the HTTP Method GET
 */
request = findTestObject('<add here the name of you object in Object Repository>')

request.setRestRequestMethod('GET')

response = WS.sendRequest(request)

WS.verifyResponseStatusCode(response, 405)

/**
 * Testing the HTTP Method UPDATE
 */
request = findTestObject('<add here the name of you object in Object Repository>')

request.setRestRequestMethod('UPDATE')

response = WS.sendRequest(request)

WS.verifyResponseStatusCode(response, 405)

/**
 * Testing the HTTP Method DELETE
 */
request = findTestObject('<add here the name of you object in Object Repository>	')

request.setRestRequestMethod('DELETE')

response = WS.sendRequest(request)

WS.verifyResponseStatusCode(response, 405)


```