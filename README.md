# Airbnb-Hospitality-Intelligence-hub
Airbnb is a leading online marketplace that provides accommodation options across various neighborhoods in New York City and around the globe. To ensure their business operations run smoothly, Airbnb has developed a cutting-edge 'Hospitality Intelligence Hub' that analyzes
data from various sources for better insights and trends. By using this tool, Airbnb gains valuable insights into their business operations, which help them make informed, data-driven decisions. The 'Hospitality Intelligence Hub' uses MySQL to analyze data which contains information on various neighborhoods in New York City, including the types of listings available, the prices of these listings, and
their availability. The system tracks trends in customer behavior and preferences, such as frequently booked room types, price trends for
specific neighborhoods etc. 

With this tool, Airbnb can identify areas for improvement and make changes to their operations to improve customer satisfaction. For
example, the 'Hospitality Intelligence Hub' helps Airbnb optimize pricing for different neighborhoods to increase occupancy rates,
improve listings based on customer preferences, and enhance the customer experience by identifying areas for improvement.
In our case study on Airbnb's Hospitality Intelligence Hub, we have two tables: 'Listings' and ‘Booking_Details. The ‘Listings' table contains information on the various neighborhoods in New York City, including the types of listings available in each neighborhood. The 'Reviews' table, on the other hand, has information on the prices of these listings, reviews and their availability. 

Code:

show databases;
create database AIRBNB_Project;
use AIRBNB_Project;

rename table airbnb_project.sql_airbnb_project16875986150 to Booking_Details;
rename table airbnb_project.sql_airbnb_project16875986151 to Listing_Details;

drop table Booking_Details;
drop table Listing_Details;

#1
select * from Listing_Details;
#2
select * from Booking_Details;
#3
select count(id) from Listing_Details;
#4
select count(listing_id) from Booking_Details;
#5
select host_id from Listing_Details;
#6
select distinct host_name from Listing_Details;
#7
select distinct neighbourhood_group from Listing_Details;
#8 
select distinct neighbourhood from Listing_Details;
#9
select distinct room_type from Listing_Details;
#10
select * from Listing_Details where neighbourhood_group in ('Brooklyn','Manhattan');
#11
select max(price) from Booking_Details;
#12
select min(price) from Booking_Details;
#13
select avg(price) from Booking_Details;
#14
select min(minimum_nights)from Booking_Details;
#15
select max(minimum_nights)from Booking_Details;
#16
select avg(availability_365) from Booking_Details;
#17
select listing_id,availability_365 from Booking_Details where availability_365>300;
#18
select  count(minimum_nights) 
from Booking_Details 
where minimum_nights>100;

