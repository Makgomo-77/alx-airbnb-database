User Table
unique constraint on email
Non-null constraints  on required field

Property Table
Foreign  key constraints on host_id
Non-null constraints on essential attributes

Booking Table
Foreign key constraints on property id and user id
Status must be one of pending ,confirmed or canceled

Payment Table
Foreign key constraint on booking_id ,ensuring payment is linked to valid bookings

Review Table
Constraints on rating values(1-5)
Foreign key constraints on property _id and user_id

INDEXING
Primary keys:indexed automatically
Additional indexes
email in the user table ,property_id in the property and booking table
booking_id in the booking and payment tables


b
