# Husky-Marketplace
Buy and Sell anything you would like for the students at the University of Washington!


### **Project Description**
&nbsp;&nbsp;&nbsp;We all know what it feels like to be a broke college student. Whether we spend all our cash at the Local Point or our favorite bar on the Ave, we can all use a few extra bucks in our pocket. Wouldn’t it be nice to have a way to earn just a little extra cash on the side? Enter: The Husky Marketplace.  
&nbsp;&nbsp;&nbsp;The Husky Marketplace is an online application that allows the user to create listings of items that he or she hopes to sell. The user can post a listing, comment on other listings, and even direct message other users to negotiate pricing. The application is restricted to UW students only, and therefore, will require a UW Email address for authentication. This will create a tight-knit community of people that share the common interest of buying and selling their goods.   
&nbsp;&nbsp;&nbsp;As developers, we recognize the importance of this application. We hope that we can create an easier, smoother experience of buying and selling items. Although there are other applications such as Craigslist or the Facebook Marketplace that offer a similar service, we believe wholeheartedly that the Husky Marketplace will be a much safer and more effective alternative for the students at the University of Washington.


### **User Stories **
1. As a Seller, I want to post a listing of something I want to sell.
-- Our **Go server** would receive and handle the POST request from the browser and send the listing information to our **MySQL** database.
2. As a Buyer, I want to browse what is listed for sale
-- Here we would store listings in our **MySQL** database and populate a web page with all these listings. Our **Go server** would retrieve the listings and send them to the browser.
