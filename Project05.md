// Name: Project 5
// Author: James Smelser
// Date: August 08, 2019

---------------------------------------------------------
```
CREATE DATABASE iKompare
GO

use iKompare;

DROP TABLE IF EXISTS LoginData;
CREATE TABLE dbo.LoginData
(
LoginID int not null,
FirstName nchar(50) not null,
Lastname nchar(50) not null,
Password nvarchar(50) not null,
CONSTRAINT PK_LoginData PRIMARY KEY CLUSTERED (LoginID)
)

DROP TABLE IF EXISTS SearchCompare;
CREATE TABLE dbo.SearchCompare
(
LoginID int not null,
ItemBarcode int not null,
ProductName nchar(50) null,
ProductPrice float null,
ProductRating nvarchar(max) null,
ProductAPI nchar(50) not null,
CONSTRAINT PK_SearchCompare PRIMARY KEY CLUSTERED (ItemBarcode)
)

DROP TABLE IF EXISTS SaveSearch;
CREATE TABLE dbo.SaveSearch
(
LoginID int not null,
ItemBarcode int not null,
ProductName nchar(50) null,
ProductPrice float null,
ProductRating nvarchar(max) null,
ProductAPI nchar(50) not null
)

DROP TABLE IF EXISTS GoogleAPI;
CREATE TABLE dbo.GoogleAPI
(
LoginID int not null,
ItemBarcode int not null,
ProductName nchar(50) null,
ProductPrice float null,
ProductRating nvarchar(max) null,
ProductAPI nchar(50) not null
)

DROP TABLE IF EXISTS AmazonAPI;
CREATE TABLE dbo.AmazonAPI
(
LoginID int not null,
ItemBarcode int not null,
ProductName nchar(50) null,
ProductPrice float null,
ProductRating nvarchar(max) null,
ProductAPI nchar(50) not null
)

ALTER TABLE dbo.SaveSearch
ADD CONSTRAINT FK_SaveSearch_LoginData
FOREIGN KEY(LoginID)
REFERENCES LoginData(LoginID)
ON DELETE CASCADE
ON UPDATE CASCADE

ALTER TABLE dbo.SearchCompare
ADD CONSTRAINT FK_SearchCompare_LoginData
FOREIGN KEY(LoginID)
REFERENCES LoginData(LoginID)
ON DELETE CASCADE
ON UPDATE CASCADE

ALTER TABLE dbo.GoogleAPI
ADD CONSTRAINT FK_GoogleAPI_SearchCompare
FOREIGN KEY(ItemBarcode)
REFERENCES SearchCompare(ItemBarcode)
ON DELETE CASCADE
ON UPDATE CASCADE

ALTER TABLE dbo.AmazonAPI
ADD CONSTRAINT FK_AmazonAPI_SearchCompare
FOREIGN KEY(ItemBarcode)
REFERENCES SearchCompare(ItemBarcode)
ON DELETE CASCADE
ON UPDATE CASCADE
```
