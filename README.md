# Team 1 Mist 4610 Group Project 1

## Team Name: 
21484 Group 6

## Team Members:

1. Erika Evan [@erikaevan](https://www.github.com/erikaevan)
2. William Malonda [@WMalonda](https://www.github.com/WMalonda)
3. Luke Michaelis [@lukemichaelis](https://www.github.com/lukemichaelis)
4. Brendan Sheehan [@bds65537](https://www.github.com/bds65537)
5. Jason Vu [@jdv14934](https://www.github.com/jdv14934)

## Problem Description:

Our project entails developing a comprehensive database solution for our client, a tennis club deeply invested in enhancing its operations and member services. This database must efficiently handle tasks such as managing member information, tracking program participation and event attendance, and facilitating effective communication between members and staff. By creating a streamlined and user-friendly database, we aim to optimize administrative tasks, improve resource allocation, and ultimately enhance the overall member experience. 

## Data Model

Explanation of data model: 

Our data model represents a tennis club whose goal is to provide facilities, services, and programs to promote the sport of tennis within the local community. At the core of the model is the member of the tennis club. Each member has their own profile, which contains their unique identification, first name, last name, phone, email, address, and the type of membership they currently have. The different types of memberships each have their own ID and give details on the price of the membership, the number of days the membership provides, and when the membership will end. When making payments for their membership, the club tracks the payment ID, the amount paid, the date of payment, the billing number and address, and the member making the payment. Additionally, members can do things such as buy products, go to events and lessons, and create reservations. 

A member can purchase multiple products without limitation. Upon purchasing products, the member is required to complete a transaction that uniquely records the date and time of the transaction and the member who made the transaction. Additionally, another set of details is recorded, which include the transaction, the products bought, the quantity of the product, and the price of each product bought. For the products themselves, the club records each product’s ID, their name, a description of the product, the product type, the cost of the product, and the quantity of the product currently in stock. 

A member can go to as many lessons as they decide to, if it fits their schedule. The club keeps track of each lesson separately and records the date of the lesson, the time the lesson is being held, the duration of the lesson, the staff who is teaching the lesson, and the member if they decide to go. Usually, a lesson is taught by only one staff member, but they can teach many different lessons. Additionally, a member can go to as many events as they would like to. The club tracks events using each event’s ID, the type of event it is, the date of the event, a description of the event, the member if they go to the event, and which facility the event will be held at. Many events can be held at the facility, but each event is held only at one facility. There are also sponsors that may sponsor the event. Sponsors are tracked using their ID, name, phone, email, and which event they are sponsoring. Typically, sponsors only sponsor one event, but an event can have multiple sponsors. 

If a member decides to make reservations for a court, the club tracks it with the reservation’s unique ID, the date of the reservation, the time of the reservation, the duration of the reservation, which member is making the reservation, and which court the reservation is being made for. Each court is also tracked separately with their own ID, the court number, the surface type of the court, the availability of the court, and which facility the court is located in. Each facility contains many different courts. 

Another entity that the club’s data model heavily revolves around is the staff that works there. Many different staff are hired at the club and keep track of things such as each staff member’s ID, their first name, last name, position, phone, email, date of their shift, their clock-in and clock-out times, and which facility they work at. Staff typically only work at one facility at a time, but a facility does contain multiple staff members.	

Each facility at the club is tracked with the facility’s ID, the name of the facility, and the address. Additionally, at the facility, there is equipment available to be used. Each piece of equipment is tracked with its own ID, the name of the equipment, the type of equipment, the quantity of the equipment available, the condition it is in, and which facility the equipment is located at. 

![DataModel](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/DataModel.jpg)

## Data Dictionary:
![Courts](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/01.Courts.png)

![Events](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/02.Events.png)

![Facility](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/03.Facility.png)

![Equipment](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/04.Equipment.png)

![Lesson](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/05.Lesson.png)

![Member](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/06.Member.png)

![Membership](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/07.Membership.png)

![Payments](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/08.Payments.png)

![Products](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/09.Products.png)

![Reservation](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/10.Reservation.png)

![Sponsor](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/11.Sponsor.png)

![Staff](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/12.Staff.png)

![Transaction](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/13.Transaction.png)

![TransactionDetails](https://github.com/lukemichaelis/MIST4610GroupProject1/blob/main/14.TransactionDetails.png)

## Queries:

![Screen Shot 2023-03-31 at 6 37 36 PM](https://user-images.githubusercontent.com/128402101/229244775-f60ebfa8-49b5-4dc1-95f4-ae027192c111.png)

1. Query 1 lists the type of equipment and the sum of quantity for each type of equipment.

![Screen Shot 2023-03-31 at 5 50 12 PM](https://user-images.githubusercontent.com/128402101/229239154-7637136b-5ddd-400c-9335-f3e571507ed7.png)

Query 1 organizes each type of equipment based on the amount of inventory pieces in that equipment. This is useful as a tennis club operator because it is always important to keep a proper inventory of each item, as well as how much space each type of equipment will take up.

2.	Query 2 lists the first and last name concatenated of the staff member and the duration of the lessons in descending order that are at least 90 minutes long. 

![Screen Shot 2023-03-31 at 5 50 39 PM](https://user-images.githubusercontent.com/128402101/229239237-725cac35-598a-49e5-9b5d-bfc96fb18714.png)

Query 2 allows the database administrators to see which coaches are teaching the longer lessons. This tells the administrators which coaches will be spending more time on the court at a given time, in order to possibly assign bonuses or accolades to employees. For example, the employee who has given the most 2 hour lessons may earn an accolade at the end of the year.

3.	Query 3 counts the total number of lessons conducted by all staff members and lists the staff members’ first and last name. 

![Screen Shot 2023-03-31 at 5 52 01 PM](https://user-images.githubusercontent.com/128402101/229239403-19acc956-7345-406e-b7ba-a6eaf1c8db88.png)

Query 3 allows management to keep a running list of staff members currently coaching lessons to members. By joining the lessons data and the staff data, management can quickly provide members with names of coaches actively teaching lessons. This query also allows management to keep track of how many lessons each coach has taught, which allows management to see what coach members prefer getting lessons from. 

4.	Query 4 shows the product name and the total number of that product sold.
 
![Screen Shot 2023-03-31 at 5 53 30 PM](https://user-images.githubusercontent.com/128402101/229239730-7f5416bd-0aff-4c4a-b64d-7f365f246a36.png)

Query 4 helps management keep track of product inventory. Its function is to show the total quantity of each product currently available for sale. This information allows an up-to-date record of stock levels, enabling efficient management of inventory. The monitoring of product sales aids in detecting any discrepancies between the quantity of goods in stock and the corresponding records management has. These inconsistencies may indicate an issue of stealing or inaccuracies in inventory recording .

5.	Query 5 displays the member’s name and the city the member is from, only listing who has bought a product from the pro shop. The cities are ordered alphabetically.

![Screen Shot 2023-03-31 at 5 54 41 PM](https://user-images.githubusercontent.com/128402101/229239947-e3c0ab47-c77c-474b-81c1-1b187548b89c.png)

Query 5 provides management with a clear overview of members who have purchased products from the pro shop, along with their respective cities. This information enables targeted marketing campaigns for cities where pro shop sales are low as selling products from pro shops will help gain revenue for management.  It also allows all null values to be excluded so management is only looking at data where there are pro shop sales. 

6.	Query 6 lists members names who have reserved more than one court and the number of courts they have reserved.

![Screen Shot 2023-03-31 at 5 55 37 PM](https://user-images.githubusercontent.com/128402101/229240045-10ca60c7-1cb2-49e2-a224-256c841e5fd8.png)

Query 6 helps management identify members who have reserved more than one court, along with the count of courts each member has reserved. By understanding which members utilize multiple courts, management can allocate resources more efficiently and potentially identify opportunities to offer specialized services or promotions to these members to enhance their experience.

7.	Query 7 identifies coaches with the highest revenue generated from lessons. 
![Screen Shot 2023-03-31 at 5 56 06 PM](https://user-images.githubusercontent.com/128402101/229240108-152740f1-4c85-4a38-9194-c981cf33fc42.png)

Query 7 provides management with insights into the revenue generated by coaches through conducting lessons. By listing coaches along with the total revenue generated from lessons, management can identify high-performing coaches and potentially incentivize them further. Understanding the revenue generated by each coach helps management make informed decisions regarding staffing, compensation, and resource allocation.

8.	Query 8 This query retrieves members with expired memberships who have not made any court reservations.

![Screen Shot 2023-03-31 at 6 34 05 PM](https://user-images.githubusercontent.com/128402101/229244470-c29f68b3-f837-4a18-97bb-f86345b84431.png)

Query 8 retrieves members with expired memberships who have not made any court reservations. It helps management identify inactive members who may need to renew their memberships or be encouraged to utilize club facilities more actively. By targeting these members, management can implement retention strategies to prevent membership lapses and promote member engagement.

9.	Query 9 lists the member name concatenated and the total dollars spent for transactions that contained more than one product in descending order

![Screen Shot 2023-03-31 at 5 56 31 PM](https://user-images.githubusercontent.com/128402101/229240166-bb0bc849-08dd-4521-8608-7a85ff53ae46.png)

Query 9 query proves useful for the database administrators because it allows them to see which club members have spent the most dollars on products they sell. It helps management identify members who make bulk purchases, allowing them to understand purchasing behavior and potentially offer tailored promotions or discounts to incentivize further spending.

10.	Query 10 retrieves information about facilities in Georgia and calculates the total number of reservations made for each of these facilities.

![Screen Shot 2023-03-31 at 5 57 00 PM](https://user-images.githubusercontent.com/128402101/229240218-c01fb32b-5f71-4562-b014-b656bfe051bb.png)

Query 10 provides useful for managers by counting the reservations associated with each tennis facility, managers can assess the popularity and demand for tennis amenities among club members. This information allows managers to make data-driven decisions regarding resource allocation, facility maintenance schedules, and potential expansion or improvement of tennis facilities.

## Database information:

Name of the database: ns_Sp24_21484_Group6

Additional information: Each query listed above is marked in the database using stored procedures which can be call using the following format (Replace X with the question number): 
CALL TP_QX();
