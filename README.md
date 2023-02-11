# Assignment_Solution

****Ques-1) Program to GET random data of an user and write it in a file named users.csv. I have used Random Data API.****

**#1 Connecting to Random Data API**

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
         
**#2 Opening CSV file and creating its writer object**

       -> # Open a CSV file for writing
         with open("users.csv", "w", newline="") as file:
    
          # Create a CSV writer object
          writer = csv.writer(file)

          # Write the header row
          writer.writerow(
          ["id", "first_name", "last_name", "username", "email", "avatar", "gender", "date_of_birth", "address"])
          
**#3  Writing data to csv file named "users.csv"**

        -> writer.writerow(
            [data["id"], data["first_name"], data["last_name"], data["username"], data["email"], data['avatar'],
             data["gender"], data["date_of_birth"], data["address"]])
             
**#4  After this, a "users.csv" file will be formed, where you can see the data extracted for 10 requests to API**


****Ques-2) Program to read users.csv and create users-sorted.csv by applying sorting algorithm on first_name****

**#1  We will need to import pandas and numpy libraries for reading csv file and doing operations on the file.**

        -> import pandas as pd
        -> import numpy as np
        
**#2  We read the "users.csv" file**

        -> df = pd.read_csv('users.csv')
        
        -> df
        
        -> Now, it will give us a output of a dataframe i.e your csv data will be stored in a tabular form which is much easier to analyze
        
**#3  Then creating "users_sorted" csv file by sorting the values by firstname**

        -> users_sorted = df.sort_values(by=['first_name'])
        
        -> users_sorted
        
        -> Now, we will get a table, in which the values will be sorted by their firstnames (alphabetical order) 
       
        -> users_sorted.to_csv('users-sorted')  
        
        -> It will create a separate users-sorted csv file in which the values will be sorted by their firstnames (alphabetical order) 
        
  
  ****Ques-3) Program to Input Id or Username of an user and return the details of that user in the output of the program****
  
  **#1  To input username of user**
  
        -> df.query('username=="ervin.rau"')
        
        -> This will give all the details of the username=ervin.rau
        
  **#2  To input id of a user**
       
       ->  df.query('id==339')
       
 
 Note: If you follow these steps, you can easily get the output. You can also refer to the Google Colab link provided in the repository.
 
        



         
      
      
  





