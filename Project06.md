// Name: Project 6
// Author: James Smelser
// Date: August 10, 2019

-------------------------------------------------------
### Project Step 9

#### USE CASE: Login Authentication

##### Actors:
- User
- System

##### Trigger:
- The user uses the iCompare application

##### Precondition:
- The user requires the use of the iCompare application

##### Post-condition:
- The system stores and assigns the user with a valid Login ID number and password

##### Normal Flow:
1. The user selects the iCompare application
2. The Login page is displayed on the user device
3. The user fills in their first name, last name, and valid password
4. The system searches the database to check if the user has an account
5. The user has an account go to Alternate Flow A(1)
6. The system will prompt the user to re-verify the password
7. The user re-verifies their password
8. The system will assign a Login ID number to the user
9. The system will present the iCompare GUI to the user

##### Alternate Flow:
###### A. The user has already made an account
1. The system will prompt the user for the Login ID number and password
2. The user inputs their Login ID number and password
3. The system will present the iCompare GUI to the user

###### B. The user cannot remember their password
1. The system will require the user to input their Login ID number and password
2. The user inputs their Login ID number and password
3. The system alerts the user of an incorrect password
4. The system will request the user Login ID number and password
5. The user inputs their Login ID number and password
6. The system alerts the user of an incorrect password
7. The system prompts the user to create a new password
8. The user creates a new password
9. The system will prompt the user to re-verify the password
10. The user re-verifies their password
11. The system will present the iCompare GUI to the user

###### C. The user cannot remember their Login ID number
1. The system will require the user to input their Login ID number and password
2. The user inputs their Login ID number and password
3. The system alerts the user of an incorrect Login ID number
4. The system will request the user Login ID number and password
5. The user inputs their Login ID number and password
6. The system alerts the user of an incorrect Login ID number
7. The system prompts the user to enter their first name, last name and password
8. The user inputs their first name, last name and password
9. The system will display the users Login ID number
10. The system will present the iCompare GUI to the user
