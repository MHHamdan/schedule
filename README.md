# schedule
#How to code schedule script in Python
# first you need to install schedule python lib using : 
# pip install schedule
#or in conda install schedule

#import necessary packages
import schedule
import time

#define a method 
def fun():
    print("I'm studyin right away...")

schedule.every(5).minutes.do(fun) # every 5 minutes 
schedule.every().hour.do(fun) # every 5 minutes  
schedule.every().day.at("10:30").do(fun) # for specific tiem 
schedule.every().monday.do(fun) # for target days 
schedule.every().wednesday.at("13:15").do(fun) # again for days' time


while True:
    schedule.run_pending()
    time.sleep(3) #mins
