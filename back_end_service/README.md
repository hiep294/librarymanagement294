# README

## Scenario
Open university would like to have library website. 
1. Student: can view and search books, view books in detail, view number of quantity
2. Librarian: can manage books, students (creating, updating, reading, and deleting). create and update ticket when students borrow books and return books

## Product specification
1. The app is responsive in mobile and desktop devices.
2. When list objects(book, student), there needs to make paginations
3. Book and student infomation include image
4. In book management, each book should need the due days. due days means the number of days which the student has to return book.
5. The app supports creating and updating tickets. When the student borrows book, there needs to minus 1 of book quantity. When the student returns book, if the book is still good, plus 1 of this book quantity; if the book is not good, this book quantity will not change.
6. In policy of library, each student can hold a limit of books, so there needs to define how many books which the students has been borrowing, also has been borrowing but over due date.
## System Requirements:

* Ruby version: 2.5.3

* Rails version: 5.2.3

* NodeJS: 8.15.1 or more

* MySQL: 14.4

* Browser: Google Chrome

## Installation

### Download gems
In main folder, run this command:
```
bundle install
```

### Download node modules
In folder 'client', run this command:
```
npm install
```
## Configuration
### Set up database
In config>database.yml, config your database.
There should use MySQL because this app uses MySQL queries. Then run the following commands in main folder: 
```
rails db:create #to create database
rails db:migrate #to create tables
```

### Create a user, due days
In main folder, run commands:
```
rails c
User.create(email: 'youremail@gmail.com', password: 'yourpassword')
DueDay.create(type_of_book: "Reference Book", due_days: 14)
DueDay.create(type_of_book: "Text Book", due_days: 62)
```
In this table, due day is set in default, each book can set its own due days
## Start App
1. Start your MySQL
2. Start Rails. In main folder, run this command:
```
rails s
```
3. Start client(ReactJS). In folder 'client', run this command:
```
npm start
```
## Demo app

