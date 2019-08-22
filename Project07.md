// Name: Project 07
// Author: James Smelser
// Date: August 17, 2019

# Project Step 07
## SRS

1 User Class 1 - The User

1.1 Functional requirement 1.1
ID: FR1
TITLE: Download mobile application
DESC: A user should be able to download the mobile application through either an application
store or similar service on the mobile phone. The application should be free to download.
RAT: In order for a user to download the mobile application.
DEP: None

1.2 Functional requirement 1.2
ID: FR2
TITLE: User registration - Mobile application
DESC: Given that a user has downloaded the mobile application, then the user should be able to register
through the mobile application. The user must provide first name, last name, and password.
RAT: In order for a user to register on the mobile application.
DEP: FR1

1.3 Functional requirement 1.3
ID: FR3
TITLE: User log-in - Mobile application
DESC: Given that a user has registered, then the user should be able to log in to the mobile application.
The log-in information will be stored on the phone and in the future the user should be logged in automatically.
RAT: In order for a user to register on the mobile application.
DEP: FR1, FR2

1.4 Functional requirement 1.4
ID: FR4
TITLE: Reset password
DESC: Given that a user has registered, then the user should be able to reset password using their login ID number.
RAT: In order for a user to reset their password.
DEP: FR2

1.5 Functional requirement 1.5
ID: FR5
TITLE: Mobile application - Compare
DESC: Given that a user is logged in to the mobile application, then the first page that is shown will be the comparison page. The user will be able to compare an item by entering the barcode manually or using the camera scanner. The comparison will return are Name, Price, Barcode Number, and Product Ratings. The comparison will return these values from at least two sources (Google API / Amazon API).
RAT: In order for a user to quickly compare an items ratings by barcode.
DEP: FR3

1.6 Functional requirement 1.6
ID: FR6
TITLE: Mobile application - Comparison Saved Search
DESC: Given that the user has compared at least one item the saved search will be accessible from the comparison page. The
saved search feature will save the last 25 comparisons and will return all data from the original comparison to the user
upon selection.
RAT: In order to provide information to the user on previously compared items.
DEP: FR5
