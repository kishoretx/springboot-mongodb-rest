

**To run MongoDB (i.e. the mongod process) as a macOS service, run:**

brew services start mongodb-community@7.0

**To stop a mongod running as a macOS service, use the following command as needed:**

brew services stop mongodb-community@7.0



Create a Person:
POST http://localhost:8080/person
{
"firstName": "Pushkar",
"lastName": "Dahal",
"emailId": "Pushkar.D@yahoo.com",
"addresses": [
{
"id": "5005",
"street": "2023 Peach Hill",
"city": "Fairfax",
"zip": "78258"
},
{
"id": "6004",
"street": "2101 Lincon Road",
"city": "New York",
"zip": "41023"
}
]
}

List all Persons:
GET http://localhost:8080/person

Get Person by ID:
GET http://localhost:8080/person/{id}

MongoDB connection string:
mongodb://localhost:27017