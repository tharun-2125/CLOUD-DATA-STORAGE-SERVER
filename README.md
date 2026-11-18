# CLOUD-DATA-STORAGE-SERVER

### NAME: THARUN N
### REG NO: 212225240173

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output
<img width="762" height="670" alt="Screenshot 2026-11-18 092021" src="https://github.com/user-attachments/assets/dbd95dc9-f61f-4422-a3d2-54f389b356f4" />
<img width="762" height="642" alt="Screenshot 2026-11-18 092203" src="https://github.com/user-attachments/assets/e0fe122f-e018-4d4b-b6ef-eba291b641c8" />
<img width="765" height="631" alt="Screenshot 2026-11-18 093208" src="https://github.com/user-attachments/assets/36f22757-a0a4-4c4e-b874-802807dbfa21" />
<img width="746" height="702" alt="Screenshot 2026-11-18 093232" src="https://github.com/user-attachments/assets/99519cd5-a0b1-4303-ad59-96d1fe4678fa" />
<img width="767" height="406" alt="Screenshot 2026-11-18 093248" src="https://github.com/user-attachments/assets/dcee770a-4474-4aac-b2a1-bde07d3fa912" />
<img width="1523" height="637" alt="Screenshot 2026-11-18 093501" src="https://github.com/user-attachments/assets/4a7eb061-857e-41f6-addc-610b3abc1077" />
<img width="1292" height="518" alt="Screenshot 2026-11-18 093617" src="https://github.com/user-attachments/assets/b563da74-d149-4b76-ae2c-4784d7752d19" />
<img width="1405" height="682" alt="Screenshot 2026-11-18 093641" src="https://github.com/user-attachments/assets/b83389fb-3432-42af-b1cc-a3330d61c4ee" />


## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.

