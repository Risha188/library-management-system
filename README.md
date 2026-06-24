# library-management-system   
    this is a libarary management api backend for the management of users and books
    
# Routes and The Endpoints

## /users
GET: Get all the users in the system
POST: Create/Register a new User

## /users/{id}
GET: Get a user by their ID
PUT: Update a user by their ID
DELETE: Delete a user by their ID (check if the user still has an issued book) && (Is there any fine/penalty to be collected with that particular user)

## /users/subscription-details/{id}
GET: Get a user subscription details by their ID
    >> Date of subscription
    >> Valid till ?
    >> Fine if any ?



## /books
GET: Get all books in the system
POST: Create or Add a new book to the system

## /books/{id}
GET: Get a book by it's ID
PUT: Update a book by it's ID
DELETE: Delete a book by it's ID

## /books/issued
GET: Get all the issued books

## /books/issued/withFine
GET: Get all issued books with their fine amount

### Subscription Types
    >> Basic (3 months)
    >> Standard (6 months)
    >> Premium (12 months)
    
>> If a user misses the renewal date, then user should be collected with $100
>> If a user misses the subscription, then user is expected to pay $100
>> If a user misses both renewal and subscription, then the collected amount should be $200

## Commands
npm init
npm i express
npm i nodemon --save-dev
npm run dev