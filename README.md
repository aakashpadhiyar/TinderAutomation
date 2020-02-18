# TinderAutomation
        Tinder is a location-based social search mobile app and Web application most often used as a dating service, that allows users to use a swiping motion to like or dislike other users, and allows users to chat if both parties like each other. Wikipedia

# Python - Selenium
##    Python libraries import
            from selenium import webdriver
            from time import sleep

##      Secrets id's & passwords
            from secrets import username, password

## TinderBot():
        # starting browser
                def __init__(self):
                    self.driver = webdriver.Chrome(executable_path='./chromedriver')
        # Loading Tinder Home Page
                def login(self):
                    self.driver.get('https://tinder.com')
        # Wait for 2sec
                sleep(2)