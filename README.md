# Nemesis-Assignment
# -*- coding: utf-8 -*-
from selenium import webdriver
from selenium.webdriver.support.select import Select
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.by import By
from selenium.common.exceptions import NoSuchElementException

def site_swaglabs(driver):

#tell location of the webdriver and call it 'driver'
driver = webdriver.Chrome(E:Usersayesheclipse-workspaceSeleniumchromedriver_win32chromedriver.exe)

driver.get("https://www.saucedemo.com/")                                          

driver.find_element_by_xpath("//*[@id="user-name"]").send_keys("standard_user")    #Entering email address  

driver.find_element_by_xpath("//*[@id="password"]").send_keys("secret_sauce")  #Entering the given password   

driver.find_element_by_xpath("//*[@id="login-button"]").click()    #Clicking submit button to login 
                  
                                                                                                             
                                                                                                             
 #add to cart
driver.find_element_by_xpath("/html/body/div[1]/div[2]/div[2]/div/div[2]/div/div[1]/div[3]/button").click()

driver.find_element_by_xpath("/html/body/div[1]/div[2]/div[2]/div/div[2]/div/div[4]/div[3]/button").click()


#click on cart (for check out)

driver.find_element_by_xpath("/html/body/div[1]/div[2]/div[1]/div[2]/a/svg/path").click()    

#go to checkout

driver.find_element_by_xpath("/html/body/div[1]/div[2]/div[3]/div/div[2]/a[2]").click()

driver.close();
