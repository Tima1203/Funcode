# Funcode

from selenium import webdriver
from time import sleep

driver = webdriver.Chrome()
url = "http://learn.funcode.school/login"
driver.get(url)
login = 'tyukovich1'
password = '9738'
sleep(3)

login_input = driver.find_element('xpath', '//*[@id="root"]/section/form/div/div[1]/div/input')
login_input.send_keys(login)
sleep(1)

password_input = driver.find_element('xpath', '//*[@id="root"]/section/form/div/div[2]/div/input')
password_input.send_keys(password)
sleep(1)
button = driver.find_element("xpath", '//*[@id="root"]/section/form/div/div[4]/button')
button.click()
sleep(5)
driver.quit()
