# ITT626-TICKET-SYSTEM
Ticketing system
Helpdesk System https://www.gorgias.com/blog/what-is-a-help-desk

Purpose: To create a helpdesk system for communication between higher ups and staff

Problem such as:
1) PC crashed, data loss, needing upgrade, software, data recovery, IT advice , log in prob
, slow computer, internet problem, printing problem,shared drive, viruses
2) set priorty list of problems that needs to be attend
3) Hardware and software upgrade, problems
4) FAQ, contact

Users:

1) IT SU and staff
2) Department Bosses
3) Normal Employees

Function:

1) Super User: 	Login/logout
		Add, modify, remove user, promote user (pangkat etc)
		Create, modify and delete ticket (categories, and tags) (set priorty list of problems that needs to be attend)
		Create, modify and delete tracking progress (Public and private actions on tickets)
		Create modify delete FAQ and rules and guidelines

2) IT Admin:	Login/logout
		Create, modify and delete ticket (categories, and tags forums, in progress etc)
		Create, modify and delete tracking progress 
		Create modify delete FAQ and rules and guidelines

3) Normal:	Login/logout 
		Create Ticket
		Read FAQ, contact, read others ticket, notification

-----------------------------------------------------------------------------------------------------------------------------------------------------
Function Details:

1) Login/Logout
- Account details uses employees' ID and pass
- Register pages can only be seen by SU after login session
- SU Account is NOT Company's Account
- If missing SU account must refer to web app documentation by dev

2) Add, modify, remove user, promote user
- Uses hierachy system (Superuser > IT Admin > normal)
-Only SU can create, modify and delete user
-Only removes user from helpdesk system not the company's system
- User page in form format

3) Create, modify and delete ticket
- Uses hierachy system (Superuser > IT Admin > normal)
- ALL USERS can create, modify and delete ticket
- Normal Users can use all categories, tags to enchance their ticket
- SU and IT Admin can set priorty of each tickets (non readable by normal users)
- If there any modification or deletion on the ticket, IT admin will receive a notification (Ticket has been deleted/modified) (Using AJAX Technology)
- All users can sort by categories, tags etc
-Level of Priority (Critical - Important - Normal - Low)
	a) Critical - Issue must be address at once
	b) Important -  Issue is important and must be dealt within a short time limit
	c) Normal - Issue can be dealt with normally within a week
	d) Low - Issue can dealt at anytime in working hour
- All users can see their ticket and chat history
-Normal User can chat with admin within their ticket problem (only when Admin prompts)

4) Create, modify and delete tracking progress
- Uses hierachy system (Superuser > IT Admin > normal)
- Only SU and IT Admin can modify tracking progress
- Notification for normal users to check their ticket progress
- Level of tracking (Created - Pending - In progress - Completed)
	a) Created - Ticket created
	b) Pending - Ticket has been viewed by IT admin
	c) In Progress - Ticket is being solved (Message between admin and users may be needed)
	d) Completed - Ticket solved and awaiting notice from staff (admin must pressed complete then normal will get notified)
-sort by priority list, categories, tags
- A TICKET CAN ONLY BE USED BY 1 ADMIN UNLESS ADMIN MODIFIED IT TO CREATED LEVEL

5) Create modify delete FAQ and rules and guidelines
- Uses hierachy system (Superuser > IT Admin > normal)
- Only SU and IT Admin can create, modify and delete FAQ and guidelines
- Normal users can only read FAQ and guidelines

6) Message function
- Between Admin and normal users
- In an email form
- must be linked with (In Progress Ticket)
- can be reviewed at anytime in chat history within a (Completed) ticket	
