User_id:primary key,UUID,indexed
first_name:VARCHAR,NOT NULL
last_name:VARCHAR,NOT NULL
email:VARCHAR,UNIQUE,NOT NULL
password_hash:VARCHAR,NOT NULL
phone_number:VARCHAR,NULL
role:ENUM,NOT NULL
created_at:TIMESTAMP,DEFAULT CURRENT_TIMESTAMP

PROPERTY
property_id:primary key,UUID,indexed
host_id:foreign key, references user
name:VARCHAR,NOT NULL
description:TEXT,NOT NULL
location:VARCHAR,NOT NULL
pricepernight:Decimal,NOT NULL
created_at:TIMESTAMP,DEFAULT CURRENT_TIMESTAMP
updated_at:TIMESTAMP,OM UPDATE CURRENT_TIMESTAMP

BOOKING
booking_id:primary key,UUID,indexed
property_id:foreign key, references property
user_id:foreign key,references user
start_date:DATE,NOT NULL
end_date:DATE, NOT NULL
total_price:Decimal,NOT NULL
status:ENUM,NOT NULL
created_at:TIMESTAMP,DEFAULT CURRENT_TIMESTAMP

THE RELATIONSHIP BETWEEN THE ENTITIES
User to Booking:One-to-many
Property to Booking:one-to-many
User to Property:one-to-many

user
