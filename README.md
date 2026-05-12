# Online Shopping System

A console based Online Shopping System built in C++ for my 2nd semester Object Oriented Programming course at UET Taxila. The whole project was about putting OOP concepts to actual use instead of just writing toy classes that didnt do anything meaningful.

## What it does

It simulates a basic online store with two types of users, an Admin who manages the inventory and a Customer who shops from it. Each user logs in, gets their own menu, and can do different things based on who they are.

The Admin can add new products to the inventory, remove existing ones, and view the entire product list. The Customer can register a new account, login with their email and password, browse the available products, add stuff to a shopping cart, view what they have in the cart, and finally checkout to place an order. On checkout it calculates the total, reduces the stock automatically, generates a clean order receipt, and saves the order to a file so its tracked.

All the data persists between runs because everything is saved to text files, customers.txt for user accounts, products.txt for the inventory, and orders.txt for the order history. So when you close the program and run it again, everything is still there.

## How its built

The whole thing is built around inheritance. There is a base User class that holds the common stuff like name, email and address, and then Admin and Customer both inherit from it and add their own specific features. Admin gets a password and product management functions, Customer gets a shopping cart and checkout flow.

There is also a Product class that holds all the product info like id, name, category, price and stock, and an Order class that handles everything related to a single order including the list of products bought, total price calculation, and saving the receipt to a file.

The project uses encapsulation through private and protected attributes with getters and setters, inheritance for the User hierarchy, and constructors for proper initialization. File handling is done using fstream for reading and writing to the text files.

## How to run it

Open the project in Visual Studio (or any C++ compiler you prefer), build it, and run. On startup you will get the main menu where you can either login as Admin, login as Customer, or register a new customer account.

The Admin password is hardcoded in the code if you want to test the admin features.

## Tech

Language is C++, IDE used was Visual Studio. Standard library only, no external dependencies.

## Notes

This was a 2nd semester project so its kept simple, no dynamic memory, no STL containers, just plain arrays with fixed maximum sizes. Looking back now there are a lot of things I would do differently, like using vectors instead of fixed arrays, hashing the passwords instead of storing them as plain text, and probably splitting everything into separate header and source files instead of dumping it all in one cpp. But for the scope of the course and the OOP concepts we had to demonstrate, it worked exactly how it was supposed to and taught me a lot about how classes actually connect in a real program rather than just on paper.
