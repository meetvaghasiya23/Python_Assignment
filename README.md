# Assignment_Solution

Ques-1) Program to GET random data of an user and write it in a file named users.csv. I have used Random Data API.

#1 Connecting to Random Data API

Step-1: Importing the necessary library

      - In order to connect to an API and perform actions on it, we need to import Python "requests"library into the environment.

      - To install the "requests" library
        -> pip install requests
        
      - Then import the requests library
        -> import requests
        
Step-2: We have passed the url to which the connection needs to be made into the get() function.

      -> response = requests.get(url)
         where url="https://random-data-api.com/api/v2/users"   
         (it is URL of the Random Data API)
         
#2 Opening CSV file and creating its writer object

       -> # Open a CSV file for writing
         with open("users.csv", "w", newline="") as file:
    
          # Create a CSV writer object
          writer = csv.writer(file)

          # Write the header row
          writer.writerow(
          ["id", "first_name", "last_name", "username", "email", "avatar", "gender", "date_of_birth", "address"])
          
#3  Writing data to csv file named "users.csv"

        -> writer.writerow(
            [data["id"], data["first_name"], data["last_name"], data["username"], data["email"], data['avatar'],
             data["gender"], data["date_of_birth"], data["address"]])
             
#4  After this, a "users.csv" file will be formed, where you can see the data extracted for 10 requests to API


Ques-2) Program to read users.csv and create users-sorted.csv by applying sorting algorithm on first_name

#1  We will need to import pandas and numpy libraries for reading csv file and doing operations on the file.

        -> import pandas as pd
        -> import numpy as np
        
#2  We read the "users.csv" file

        -> df = pd.read_csv('users.csv')
        
        -> df
        
        -> Now, it will give us a output of a dataframe i.e your csv data will be stored in a tabular form
        
        ![image](https://user-images.githubusercontent.com/85356809/218279626-ad83f636-3ca6-4b7a-b15e-ff82138e7d88.png)



         
      
      
  





