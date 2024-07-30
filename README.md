# Repair-Shop-Sales-Analysis
Introduction
The purpose of the project was to analyze the performance a vehicle repairing shop in order to optimize performance, improve sales as well as increasing customer satisfaction level and also to determine the total revenue generated from the shop over a period of time.
## Data Ingestion and Preparation
The following dataset were provided by the company, which ease the analysis processes:
Invoice.csv: which detailed the receipt generated for every job performed in the shop, 
Job.csv: This detailed the type of service performed on every walk-in from the shop which also include the amount paid on each job
customer.csv: It detailed the information about the customer such as customer name, address and phone number.
car.csv: It shown the information of each car that was worked on in the shop, such as there make, model, year of manufacturing and the total mileage covered.
Part.csv: It detailed the part used in each services performed ,there cost for each and the revenue generated from each part.
### Data Preparation
I created tables according to the data about to be imported to mysql workbench using the following queries.
_create database da_abiodunuthmanamusat;
create table Customer(CustomerID int not null primary key auto_increment,
Name varchar(70), Address Varchar(150), phone text);
create table Invvoice (InvoiceID int not null,InvoiceDate datetime,
Subtotal float,SalesTaxRate Int, SalesTax float,TotalLabour Int,
TotalParts float, Total float, CustomerID int, VehicleID Int);
Create table Vehicles(VehicleID Int Not Null primary key auto_increment,
Make varChar(20),Model varchar(20),Year int, Color text,Vin text,
RegNumber Text,Mileage Int, OwnnerName Text);
create table Job(JobId Int primary key,VehicleId Int, Description varchar(100),
Hours float,Rate Int,Amount float,InvoiceID Int);
Create Table Parts(PartId Int Not null primary key, JobId int,PartNumber Varchar(25),
PartName Text,Quantity Int,UnitPrice float,Amount float, InvoiceId Int);_
After which all the data were successfully imported using data import/export wizard.


## Analysis Report
### Customer Analysis
#### Top 5 customer that spent the most on part and repair

![amount spent on part](https://github.com/user-attachments/assets/096a0b68-2f90-40e0-9280-626822c25256)

Amount spent on part

![amount spent on vehicle repair](https://github.com/user-attachments/assets/79aa3c1f-2af6-4965-baa2-d72b195126ad)

Amount spent on vehicle

#### Average spending of customers on repairs and parts.

![Avergae spending on part and repair](https://github.com/user-attachments/assets/48e81c49-1ae8-4e46-ad55-c7980201dc24)

#### Frequency of customer visits and patterns identification.

![Frequency visit of customer](https://github.com/user-attachments/assets/31b55d9b-9146-4031-9161-c83c24159fa3)

### Vehicle Analysis
#### Average mileage of vehicles serviced

![avg mileage of vehicles](https://github.com/user-attachments/assets/23abfb3e-0eff-4ecb-89a4-3ad80ffa2a96)

#### The most common vehicle makes and models brought in for service

![The most common vehicles brought in for service](https://github.com/user-attachments/assets/74a24bc9-703e-4aa4-85ec-22e79e4cdef7)

#### Vehicles age and service required 
![Vehicles age and service distribution](https://github.com/user-attachments/assets/a7493ad5-d90e-4b12-90e1-00fa4e171755)

### Job performance analysis
Most common type of job
![most common type of job](https://github.com/user-attachments/assets/e6bcd50c-e121-4791-b362-3202d83f781d)

#### Revenue generated per job
![Revenue per job type](https://github.com/user-attachments/assets/3faf15bc-dc2c-4b36-b861-c234a71970ea)

#### Average cost of job
![Job with the highest average cost](https://github.com/user-attachments/assets/a5ea9f20-2310-45ba-8c97-4df71f2c59d2)

Highest cost of job

![Job with the lowest average cost](https://github.com/user-attachments/assets/0bffad4b-3458-4d3a-a0a7-8da4833dabae)

Lowest cost of job
### Part usage analysis
#### Five most frequently used part and their usage
![Frequently useed part](https://github.com/user-attachments/assets/50dbe471-b764-4a81-8c80-b42859c0f591)

Average cost of part used
![average cost of part used](https://github.com/user-attachments/assets/eb403903-2a3a-422c-b431-fa74e18f3f2a)

Total revenue generated from parts sales
![Total revenue generated from part sales](https://github.com/user-attachments/assets/ff562634-6498-471b-9d12-ba2b56b00f19)

### Financial Analysis
Total revenue generated per month from job and part sales
![Refvenue generated per month](https://github.com/user-attachments/assets/fe7763b3-9cd0-4335-b12e-7f44d3fb4fa4)

Overall profitability of the repair shop

Sales Tax Impact on the Revenue generated
![Tax Impact](https://github.com/user-attachments/assets/8a648180-dbbd-4cbf-99a2-5228f1983808)
