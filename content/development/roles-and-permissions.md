+++
title= "Roles and Permissions"
date= 2018-02-28T19:31:41+05:30
description = ""
draft= false
weight = 21
+++

Repair Rabbit has total 4 types of users. Each user has cetain roles nd permissions given to access resources. Below are the list of users supported in the system.

### [Customers](/development/roles-and-permissions/#a-name-customers-customers-a)
### [Employees](/development/roles-and-permissions/#a-name-employees-employees-a)
### [Store Admin](/development/roles-and-permissions/#a-name-store-admin-store-admin-a)
### [Super/Main Admin](/development/roles-and-permissions/#a-name-super-admin-super-main-admin-a)

<hr>

## <a name="#customers">Customers</a>

`Customers` type user i.e. user who has role customer can perform following actions.

* Create A New Appointments
* View Appointments
* Edit Appointments
* View Profile
* Edit Profile
* Reset Password

## <a name="#employees">Employees</a>

`Employees` type user i.e. user who has role employee can perform following actions.

**In Dashboard:**

An employee has following access in `Dashboard` page.

* Year to date Appointments
* Appointment - Previous Year
* Year to date Tickets
* Tickets - Previous Year
* Appointments
* Repairs By Employee

**In Agenda:**

An employee has following access in `Agenda` page.

* Appointments
* Leaves
* Store Holidays


**In Tickets:**

An employee has following access in `Tickets` page.

* Listing
* Add
* View
* Edit
* Print
* Deduct Stock
* Generate Invoice
* View Invoice
* History


**In Appointments:**

An employee has following access in `Appointments` page.

* Listing
* Add
* View
* Edit
* Convert Into Ticket(start repair)
* View Ticket


**In Customers:**

An employee has following access in `Customers` page.

* Listing
* Add
* View
* Edit
* Change Password
* Import Sample data Csv
* Tickets, Appointments listing of that perticular customer with a perticular store of a employee
* Ticket, Appointment add new of that perticular customer with a perticular store of a employee


**In Invoices:**

An employee has following access in `Invoices` page.

* Add
* View
* Print
* Preview

## <a name="#store_admin">Store Admin</a>

**In Dashboard:**

* Year to date Appointment
* Appointment - Previous Year
* Year to date Tickets
* Tickets - Previous Year
* Total earning amount
* Total Price Of Stock
* Employees Status
* Stores Status
* Appointments
* Repairs By Employee

**In Agenda:**

* Appointments
* Leaves
* Store Holidays

**In Tickets:**

* Listing
* Add
* View
* Edit
* Delete
* Print
* Deduct Stock
* Revert Stock
* Generate Invoice
* View Invoice
* Restore
* History


**In Appointments:**

* Listing
* Add
* View
* Edit
* Delete
* Convert Into Ticket(start repair)
* View Ticket

**In Customers:**

* Listing
* Add
* View
* Edit
* Change Password
* Delete
* Import Sample data Csv
* Tickets, Appointments, Invoices listing of that perticular customer with a perticular store
* Ticket, Appointment, Invoice add new of that perticular customer with a perticular store


**In Invoices:**

* Listing
* Add
* View
* Edit
* Print
* Preview

**In Employees:**

* Listing
* Add
* View
* Edit
* Change Password
* Change Role
* Delete

**In Store Closed(Holidays):**

* Listing
* Add
* Edit
* Delete

**In Inventory:**

* Listing(with add, return and transfer for a perticular store also)
* Add
* Return
* Transfer
* History of stock
* History of a perticular product also

**In Master Management:**

*Shops*

* View(With Employee listing, add, edit, view, change password, delete of a perticular store)
* Edit

*Accessories*

* Listing
* View
* Add
* Edit

## <a name="#super_admin">Super/Main Admin</a>

**In Dashboard:**

In this all blocks, admin having rights of all stores which are listing as following:


* Year to date Appointment
* Appointment - Previous Year
* Year to date Tickets
* Tickets - Previous Year
* Total earning amount
* Total Price Of Stock
* Employees Status
* Stores Status
* Appointments
* Repairs By Employee

**In Agenda:**

In this all blocks, admin having rights of all stores with employees which are listing as following:

* Appointments
* Leaves
* Store Holidays

**In Tickets:**

In this all blocks, admin having rights of all stores which are listing as following:

* Listing
* Add
* View
* Edit
* Delete
* Print
* Deduct Stock
* Revert Stock
* Generate Invoice
* View Invoice
* Restore
* History


**In Appointments:**

In this all blocks, admin having rights of all stores which are listing as following:

* Listing
* Add
* View
* Edit
* Delete
* Convert Into Ticket(start repair)
* View Ticket

**In Customers:**

In this all blocks, admin having rights of all customers from all stores which are listing as following:

* Listing
* Add
* View
* Edit
* Change Password
* Delete
* Import Sample data Csv
* Tickets, Appointments, Invoices listing of that perticular customer
* Ticket, Appointment, Invoice add new of that perticular customer

**In Invoices:**

* Listing
* Add
* View
* Edit
* Print
* Preview
* Delete

**In Employees:**

* Listing
* Add
* View
* Edit
* Change Password
* Change Role
* Delete

**In Store Closed(Holidays):**

* Listing
* Add
* Edit
* Delete

**In Inventory:**

* Listing(with add, return and transfer for a perticular store also)
* Add
* Return
* Transfer
* History of stock
* History of a perticular product also

**In Master:**

*Device Categories*

* Listing
* View
* Add
* Edit
* Delete

*Devices*

* Listing
* View
* Add
* Edit
* Delete

*Products*

* Listing
* View
* Add
* Edit
* Delete

*Shops*

* Listing
* View(With Employee listing, add, edit, view, change password, delete of a perticular store)
* Add
* Edit
* Delete

*Email Templates*

* Listing
* View
* Add
* Edit
* Delete

*Data Backup*

* Download the data of all with date and range wise for all stores

*Accessories*

* Listing
* View
* Add
* Edit
* Delete
