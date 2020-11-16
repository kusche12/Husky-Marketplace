# Husky-Marketplace
Buy and Sell anything you would like for the students at the University of Washington!


### **Project Description**
We all know what it feels like to be a broke college student. Whether we spend all our cash at the Local Point or our favorite bar on the Ave, we can all use a few extra bucks in our pocket. Wouldn’t it be nice to have a way to earn just a little extra cash on the side? Enter: The Husky Marketplace.  
The Husky Marketplace is an online application that allows the user to create listings of items that he or she hopes to sell. The user can post a listing, comment on other listings, and even direct message other users to negotiate pricing. The application is restricted to UW students only, and therefore, will require a UW Email address for authentication. This will create a tight-knit community of people that share the common interest of buying and selling their goods.   
As developers, we recognize the importance of this application. We hope that we can create an easier, smoother experience of buying and selling items. Although there are other applications such as Craigslist or the Facebook Marketplace that offer a similar service, we believe wholeheartedly that the Husky Marketplace will be a much safer and more effective alternative for the students at the University of Washington.


### **User Stories**
1. As a Seller, I want to post a listing of something I want to sell:  
Our **Go server** would receive and handle the POST request from the browser and send the listing information to our **MySQL** database.

2. As a Buyer, I want to browse what is listed for sale:  
Here we would store listings in our **MySQL** database and populate a web page with all these listings. Our **Go server** would retrieve the listings and send them to the browser.

3. As a user, I want to comment on listings: 
We would store comments on listings in our **MySQL** database. Our **Go server** would retrieve the listings and send them to the browser.

4. As a user, I want to view other users' profiles:  
Profile information would be stored on our **MySQL** database. Our **Go server** would pass the requested user from the database to the browser to populate a web page.

5. As a user, I want to update my profile information:  
Profile information would be stored on our MySQL database. Our Go server would pass the updated information to the database.



### **Architectural Diagram**
![architectural diagram of system](https://github.com/kusche12/Husky-Marketplace/blob/main/arch%20diagram.png)



### **Endpoints**
- /v1/users : GET users and POST to create a new user
- /v1/users/{:id} : GET specific user and PATCH to update user account info


### **SQL Database Schema**
USER {  
    id int not null auto_increment primary key,  
    firstName varchar(64) not null,  
    lastName varchar(64) not null,  
    email varchar(128) not null,  
    passHash varchar(64) not null,  
    photoUrl varchar(255),  
}

POST {  
    id int not null auto_increment primary key,  
commentPostID int secondary key not null,  
userID int secondary key not null,  
    title varchar(128) not null,  
    description varchar(128) not null,  
    posted datetime not null,  
    updated datetime not null,  
    listingPrice int not null,  
}  

COMMENT_POST {  
    id int not null auto_increment primary key,   
    postID int secondary key not null,  
    commentID int secondary key not null,  
}  

COMMENT_ID {  
    id int not null auto_increment primary key,  
    userID int secondary key not null,  
    message varchar(128) not null,  
    amountOfLikes int not null,  
}  

PROFILE {  
    id int not null auto_increment primary key,  
    userID int secondary key not null,  
    dateOfBirth datetime,  
    major varchar(64),  
    yearInSchool varchar(64),  
    description varchar(255),  
    bannerPhotoURL varchar(255)  
}  
