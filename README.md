# Library Room Booking App
Created by 
- Vamshidhar Reddy Palle( vpalle)
- Anshul Goel (agoel4)
- Rushabh Doshi(radoshi)
-Note: please don't change password for the following users because there will be an option to update user details.
	You can create new users and test the edit user functionality.
<b>Pre-configured Admin and User Details:</b>
<table border=1>
	<th> Role </th>
	<th> Name </th>
	<th> Email ID </th>
	<th> Password </th>
	<tr> <td> Super Admin <td> Vamshidhar <td>vamshi@ncsu.edu <td> vamshi</tr>
	<tr> <td> Admin <td> Harsha <td>harsha@ncsu.edu <td> harsha</tr>
	<tr> <td> Member <td> Viswa <td>viswa@ncsu.edu <td> viswa</tr>
	<tr> <td> Admin <td> Shashi <td>shashi@ncsu.edu <td> shashi</tr>
	<tr> <td> Member <td> Vineet <td>vineet@ncsu.edu <td> vineet</tr>

</table>

There are three types of users in the system: Admin, Super Admin and Member.

Below are the tasks that can be performed by each user type

<b> Admin and Super Admin</b>
- Edit profile
	* Click on Edit Profile tab, change the details and click on Update User
- Manage Users
	* You can search using email or name or usertype of the user.
        * Upon results pop up you can see his profile details, his booking history and can delete him if he is not the person
          who is logged in and a super admin.
	* Click on Add Admin tab to add admins/members
- Manage Rooms
	* You can search for a room based on roomno,building and size. Below actions can be performed on results
		* Show - Details of the room can be seen.
		* View Booking history - List of Bookings made for that room.
		* Edit - To edit the room details
		* Delete - To delete the room
	* Click on Add Room tab to create new room. 
        * Click on Book Room to see the existing future reservations and list of rooms
        * You can search for a room based on roomno,building and size.
        * Once the results pop up each room will have an option called create reservation using which you can enter details and book a             room.
        *An admin can release any room by pressing release room button.
- Add admin
        * you can add new members and admins.
- Search users
        * Can search for users based on name,email and usertype.
                *Can edit,see the details, view booking history of user and delete a user.
- Add Room
    	* Can add new rooms.
- Book a room
    	*A page with existing future reservations and list of rooms will pop up.
    	* Using Release Room can release a room.
    	* Can create reservation by clicking on create reservation beside the room details.
    	* Can search for rooms based on roomno,building and room size and based on results can create a reservation.
    	* Upon clicking create reservation a Page with title New Reservation pops up. Being admin can book for other user by entering 
    	<b> email address </b> in the booked user textbox.
    	* Constraints for invalid roomno,invalid user email, reservation for more than two hours, booking for a date which is 
       7 days in future, booking for a past date are applied.
    	* An email can be sent to multiple users with booking details by entering valid emails in the format prescribed
      	near Invite textbox. 
<b> Member </b>
- Edit profile
	* Click on Edit Profile tab, change the details and click on Update User
- Search Rooms
  * You can search for a room based on roomno,building and size. Below actions can be performed on results
		  * Show - Details of the room can be seen.
  * Book Room tab can be used to book a room.
    *A page with existing future reservations and list of rooms will pop up.
    * Using Release Room can release a room if the room is booked by this user.
    * Can create reservation by clicking on create reservation beside the room details.
    * Can search for rooms based on roomno,building and room size and based on results can create a reservation.
    * Upon clicking create reservation a Page with title New Reservation pops up. 
    * Constraints for invalid roomno,invalid user email, reservation for more than two hours, booking for a date which is 
       7 days in future, booking for a past date are applied.
    * An email can be sent to multiple users with booking details by entering valid emails in the format prescribed
      near Invite textbox.
- View Booking History
	* Can view his list of reservations.


<b> Edge Case Handling </b>
- When a room with an existing reservation is deleted the reservation also gets deleted.This is achieved using dependent destroy. 
  So the reservation is not showed anymore in the reservation history of user.
- When a user with an existing reservation is deleted the reservation also gets deleted. This is achieved using dependent destory.
  So the reservation is not showed anymore in the reservation history of room. 



<b> Extra Credit </b>
- System can send an email to people if a user types their email address while booking a room.
