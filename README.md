# TinderAutomation
    Tinder is a location-based social search mobile app and Web application most often used as a dating service, that allows users to use a swiping motion to like or dislike other users, and allows users to chat if both parties like each other. Wikipedia

# Python - Selenium
##    Python libraries import
    from selenium import webdriver
    from time import sleep

##  Secrets id's & passwords
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

## Select Button (Log In With Facebook) & Click
    # Select that element
    fb_btn = self.driver.find_element_by_xpath('//*[@id="modal-manager"]/div/div/div/div/div[3]/div[2]/button')

    # Click That Button
    fb_btn.click()
    
## Switch to login popup
    # Facebook window Selection
    # Tinder site window
    base_window = self.driver.window_handles[0]
    # Faceboot site window
    self.driver.switch_to_window(self.driver.window_handles[1])

## Select login Username Textbox element via xpath
    # select login Username Textbox
    email_in = self.driver.find_element_by_xpath('//*[@id="email"]')
    # Sending email Or Username
    email_in.send_keys(username)

## Select login Password Textbox element via xpath
    # select login Password Textbox
    pw_in = self.driver.find_element_by_xpath('//*[@id="pass"]')
    # Sending Password
    pw_in.send_keys(password)

## Select Login Button & click
    #   select login button
    login_btn = self.driver.find_element_by_xpath('//*[@id="u_0_0"]')
    # click That Button
    login_btn.click()
## Back to tinder window
    self.driver.switch_to_window(base_window)

WebSite : https://aakashpadhiyar.github.io/
Skype : live:8afc3e69a745ee48
