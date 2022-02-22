# PythonTasks
# IITM Task -1

import csv

userID = input("Please enter userID: ")

#print(userID.index("@"))

if "@" in userID:       # should have "@"
    if "." in userID:   # should have "."
        #if userID.index("@")<userID
        if userID[0] in "abcdefghijklmnopqrstuwxyz" or userID[0] in "ABCDEFGHIJKLMNOPRSTUVWXYZ":
            for i in range (0,len(userID)):
                if userID[i] == ".":
                    if userID.index("@") != userID.index(".")-1 and userID.index("@") < userID.index(".")-1:
                        print("Good")
                    else:
                        print("invalid userID")
        else:
            print("invalid userID")
    else:
         print("invalid userID")
else:
    print("invalid userID")
                   
password=input("Enter password: ")
if password in "!@#$%&_="):
    if password in "abcdefghijklmnopqrstuwxyz":
        if password in "ABCDEFGHIJKLMNOPQRSTUVWXYZ":
            if password in "[0-9]":
                print("Good Password")
            else:
                print("No Number")
        else:
            print("No Caps")
    else:
        print("No Small")
else:
    print("No Special chars")
   
# File Handling Operations

open("MyFile.csv",w,newline='') as f:
    thewriter = csv.writer(f)
    thewriter.writerow([userID,password])

for row in csv_file:
    if userID == row[0]:
        password1 = input("Enter your password to login: ")
        if password1 == password:
            print ("Login Suceess full")
        else:
            print("Incorrect Password")
     else:
         print("This user ID is not registered with us.Please register to login.")
