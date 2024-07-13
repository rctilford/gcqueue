## Queue Manager for GC ResLife Staff

### Goals

 - Help keep ResLife staff stay organized during checkout and enable collaboration so multiple staff can be on checkout duty at one time.
 - Show residents an estimated wait time for a staff member to come check their room.
 - Reduce frustration and stress for all parties.
 - Demonstrate efficacy to ResLife Pro-Staff so they can vie for its integration to the portal.

### Planned Operation

This project is meant to create a queue management website for Georgetown College ResLife staff to use during the checkout process. It will allow the RAs and RHCs to create accounts protected by 2FA. Residents will then be able to visit the site and signal that they are ready to checkout. The residents that have done this will be shown in a queue to the ResLife staff. The staff would then be able to claim the next person in line and thus remove them from the queue shown to other staff. Once claimed the staff will have the option to remove the person from the queue or begin the checkout process. If the staff clicks the checkout option they will be redirected to the GC Portal.

### Access Structure

There will be 3 tiers of access with different permissions:

 - Residents
   - Resident permissions:
   - Enter/Exit a queue.
   - View estimated wait time.
 - ResLife staff (RAs and RHCs)
   - ResLife staff permissions:
   - All permissions of Residents.
   - View the people in the queue.
   - Claim and respond to the next in line.
 - ResLife Pro-Staff (Admin, Cam Snapp, Katie Baker)
   - ResLife Pro-Staff permissions:
   - All permissions of previous tiers.
   - Initialize a queue.
   - Add and remove Resident access to the ResLife Staff Tier.
   - Add and remove ResLife Staff and Resident access to active queues.
   - Delete existing queues.
   - View an analytics dashboard of data on the queue volume over time.

### Functions

#### Queue Initialization

This function should open a pop up window with the following selection options:

 - Name the queue.
 - Select access to the queue.

#### Queue Entrance

This function should redirect the user to a page where they can select their name. This will populate a new tile in the queue with their name and room number.

#### Queue Claim

This function would allow ResLife staff to claim the next Resident in line. It should be called when a staff member clicks on a tile in the queue.


### Databases

#### Accounts (managed with the httr R package)

 - Username (hopefully matching the user's GC Username)
 - Password (perhaps stored as a hash if you can figure that out)
 - Name
 - Access Tier
   - 3: Residents
   - 2: ResLife staff
   - 1: ResLife Pro-Stuff
 - Dorm
 



