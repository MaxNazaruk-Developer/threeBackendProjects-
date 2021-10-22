
## Job description
Technical Test – Salesforce Developer

Please set up a test environment and email and work through the tasks outlined. There is no time limit to this test, however you should spend a few hours at most. If you feel stuck at any task, please document your approach within this document. Value code quality over functionality. Use LWC.

1. Create a Case from a new incoming email
Every enquiry from a customer is sent to a specific email address (you can create a fake one for this testing purpose). Link all incoming emails to Salesforce, so that a new Case is created for every enquiry. Incoming emails might have an associated TripID in the format [T#12345] at the bottom of the email.

2. Trigger to link an Account to the Case based on TripID
In order to associate incoming enquiries with the customer, we want to set them based on the TripID.

   - 2.1 Schema of architecture
Every customer can have multiple trips and multiple service tickets associated to them. What objects would you use to map out this architecture and how do they relate to each other? Please create a database schema diagram.  
   - 2.2 Set customer
Every incoming email with a TripID in the body of the email should be linked to the customer object (whatever object you’ve chosen in 2.1). What type of relationship have you used and why?

3. Lightning web component that displays all trips
Create a lightning web component on the Case that shows a table of all trips related to the linked customer.

4. Extra: Write a scheduled batch class
Every night we want a bulk job checking all our open Cases that have no customer linked against our TripIDs and set the customer for found matches.


Provide please credentials to your test org where we can see the working task
and GitHub link so we can see the code.
Thanks.
## Job performance
For this task, we used three objects: Account with a custom email field, Case with a custom TripId field, and a custom Trip object.   
The following block diagram shows the logic of email processing.
![схема](https://user-images.githubusercontent.com/84872903/138463440-ae37afd4-a2db-4f89-8ee5-53f5238a7220.png)

There was also сreate a lightning web component on the Case that shows a table of all trips related to the linked customer.
When you load the Case object page, you see a table with three columns: Name Trip - shows the name of the trip, Account Id - shows the id of the tied to this trip account, Date Create - shows the creation date trip

![image](https://user-images.githubusercontent.com/84872903/138464894-cd09fcaa-4477-4ae7-834a-45afbdeae8b3.png)
