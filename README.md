#### Build Status [Build Status](http://63.34.40.219/buildStatus/icon?job=SensaiSelenium)

# Sensai Automated Testing

This repo contains the Selenium SIDE files that are used by Jenkins to perform automated testing agianst the Sensai Test Account.

Currently these tests comprise of testing the creation and training of models in the Pre-Release tenant (djsunderland@sensai.test.pre).

When changes are made locally to the Selenium SIDE file, they need to be uploaded to this repo using the filename sensai-test-model-create.side

Once this has been completed, the Jenkins project 'SensaiSelenium' can be built which will clone this repo and execute the selenium-side-runner on Jenkins using the sensai-test-model-create.side file.

To initiate the build, the following must be run from the command line:
sudo curl -X POST http://djsunderland:11a3417c68f5cb7ae9ca5b42e86addd18c@http://63.34.40.219/job/selenium/build?token=0oWERtBkrycGJewLExsKpPab7aDIlJcx

Alternatively, you can login to Jenkins (http://63.34.40.219/job/SensaiSelenium/) and click 'Build Now'.

On completion of the build, an email will be sent to qa@cloudapps.com with the build log.
