# CENG211 – Programming Fundamentals

# Homework # 4

In this homework you are expected to implement an “Customer Complaint App” in Java.
You should fulfill the concepts of:

```
 Object Oriented Design
 UML Class Diagrams
 UML Sequence Diagrams
 UML Statechart Diagrams
```
In the Customer Complaint Application, you are expected to create an app which customers can
add their complaints, and producers can monetarize and change the state of complaints. In the
app, mentioned data will be stored in csv files. CSV files should be as below:

```
 User.csv:
UserID, Username, Password, DisplayedName, UserType
 Product.csv:
ProductID, ProducerID, ProductName, ProductType
 Complaint.csv:
ComplaintID, CustomerID, ProducerID, ProductID,
ComplaintTitle, Complaint, Status
```
```
 User.csv will include IDs of users, usernames, passwords, names of the users that are
displayed in the application, and type of users. Type can be Customer , Producer , and
Admin.
i.e.: 15, johndoe, password!127, John Doe, customer
i.e.: 8 , lenovocom, pass 454 word, Lenovo, producer
 Product.csv will include IDs of products, producers ID, names of the products, and types of
the products.
i.e.: 23, 8, Computer, Electronic
 Complaint.csv will include IDs of complaints, IDs of customers, IDs of producers, IDs of
products, titles of the complaints, complaints themself, and status of the complaints. Status
can be New , Seen , Working , Fixed , Deleted
i.e.: 12, 15, 8, 23, fan noise, extreme rattling noise coming from the fan, working
```

Working of the app:

Firstly, the app should introduce a login or sign-up selection. Users should be able to login the
system with their credentials or sign-up if they have not any registration. Users can sign-up as
customer or producer; they cannot select to be an admin. (Define an admin user in your csv file
with username: admin, password: password)

If the user is a customer, customers can add a complaint or see their previous complaints if there
any.
If they choose to add a complaint, the steps should be as follow:

```
 Choose a producer from the producer list
 Choose a product type from the product type list
 Choose a product from the product list
 Add a complaint title and a complaint
```
If they choose to see their previous complaints, the steps should be as follow:

```
 Choose a complaint from the complaint list
 See the complaint and delete it if it is intended (deletion is not mandatory, customer may
want to check the content of the complaint)
Notes:
 A complaint should be added with the status New.
 A complaint can be deleted if the status of the complaint is not Fixed.
 Deletion of the complaint should not be a deletion from the csv file, it should be a
status change as Deleted.
 In the complaint list, content of the complaints should not be shown. In the list,
displayed areas should be: Complaint ID, Producer name, Product, Complaint title,
Complaint status. The complaints that have a status Deleted should not be displayed.
Details of a complaint can be seen if the complaint is selected.
```
If the user is a producer, producers can add new product with related product type or see the
complaints that are related to them.
If they choose to add a product, the steps should be as follow:

```
 Choose a product type if intended product type is in the product type list; if it is not in the
list, add a new one
 Add a new product
```
If they choose to see the complaints that are related to them, the steps should be as follow:

```
 Choose a complaint from the complaint list
 If a complaint is opened, the status of the complaint should be changed to Seen
automatically (If the status is New )
```

```
 Change the status of the complaint as Working or Fixed if it is intended (change is not
mandatory, producer may want to check the content of the complaint)
Notes:
 The status of a complaint cannot be changed to Seen.
 Producers cannot delete a complaint.
 In the complaint list, content of the complaints should not be shown. In the list,
displayed areas should be: Complaint ID, Customer name, Product, Complaint title,
Complaint status. The complaints that have a status Deleted should not be displayed.
Details of a complaint can be seen if the complaint is selected.
```
If the user is an admin, admins can see all the complaints in the system. They can change the status
of the complaints as they want. Therefore, when they enter the system, all the complaints should
be listed directly.
If they choose to see a complaint from the list, the steps should be as follow:

```
 Choose a complaint from the complaint list
 See the complaint and change the status of it if it is intended (change is not mandatory,
admin may want to check the content of the complaint)
```
## Notes:

```
 In the complaint list, content of the complaints should not be shown. In the list,
displayed areas should be: Complaint ID, Customer name, Producer Name, Product,
Complaint title, Complaint status. Even the complaints have a status Deleted , they
should be displayed. Details of a complaint can be seen if the complaint is selected.
```
You are expected to satisfy object-oriented design guidelines.

You are expected to draw a **UML Class Diagram** , **UML Sequence Diagram** , and **UML Statechart
Diagram** in the given scenario. For the UML Sequence Diagram, you should only draw _Adding A
Complaint_ part.

Please add your csv files and UML diagrams inside your project. To be tested easily, please fill your
csv files with some entries by using your application.
