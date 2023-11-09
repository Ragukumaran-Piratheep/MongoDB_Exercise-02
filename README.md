# MongoDB_Exercise-02
<code>
**1.Create a Database called customers.**
...
test> use customers
switched to db customers
...


**2. Create a collection called customerdetails.**
...
db.createCollection("customerdetails")
{ ok: 1 }
...


**3. Insert all documents into the collection named   customerdetails.**
...
db.customerdetails.insertMany([{"name":"John","age":"25","gender":"Male","city":"New York"},{"name":"Emily","age":"25","gender":"Female","city":"London"},{"name":"Daniel","age":"22","gender":"Male","city":"Sydney"},{"name":"Sophia","age":"28","gender":"Female","city":"Paris"},{"name":"William","age":"26","gender":"Male","city":"Chicago"},{"name":"Olivia","age":"23","gender":"Female","city":"Los Angeles"},{"name":"Benjamin","age":"27","gender":"Male","city":"Toronto"},{"name":"Mila","age":"30","gender":"Female","city":"Berlin"},{"name":"James","age":"30","gender":"Male","city":"Tokyo"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("654cb07aa71a47ec4d1ae7d7"),
    '1': ObjectId("654cb07aa71a47ec4d1ae7d8"),
    '2': ObjectId("654cb07aa71a47ec4d1ae7d9"),
    '3': ObjectId("654cb07aa71a47ec4d1ae7da"),
    '4': ObjectId("654cb07aa71a47ec4d1ae7db"),
    '5': ObjectId("654cb07aa71a47ec4d1ae7dc"),
    '6': ObjectId("654cb07aa71a47ec4d1ae7dd"),
    '7': ObjectId("654cb07aa71a47ec4d1ae7de"),
    '8': ObjectId("654cb07aa71a47ec4d1ae7df")
  }
}

...
**4. Retrieve all documents from the collection and sort the results by the “age” field    in ascending order.**
...
db.customerdetails.find().sort({age:1 }).pretty()
[
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7d9"),
    name: 'Daniel',
    age: '22',
    gender: 'Male',
    city: 'Sydney'
  },
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7dc"),
    name: 'Olivia',
    age: '23',
    gender: 'Female',
    city: 'Los Angeles'
  },
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7d7"),
    name: 'John',
    age: '25',
    gender: 'Male',
    city: 'New York'
  },
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7d8"),
    name: 'Emily',
    age: '25',
    gender: 'Female',
    city: 'London'
  },
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7db"),
    name: 'William',
    age: '26',
    gender: 'Male',
    city: 'Chicago'
  },
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7dd"),
    name: 'Benjamin',
    age: '27',
    gender: 'Male',
    city: 'Toronto'
  },
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7da"),
    name: 'Sophia',
    age: '28',
    gender: 'Female',
    city: 'Paris'
  },
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7de"),
    name: 'Mila',
    age: '30',
    gender: 'Female',
    city: 'Berlin'
  },
  {
    _id: ObjectId("654cb07aa71a47ec4d1ae7df"),
    name: 'James',
    age: '30',
    gender: 'Male',
    city: 'Tokyo'
  }
]

...
**5. Count the number of females.** 

...
db.customerdetails.countDocuments({"gender":"Female"})
4

...
**6.Insert one document into the customerdetails collection.**

...
db.customerdetails.insertOne({"name":"Piranavan","age":"23","gender":"Male","city":"Jaffna"})
{
  acknowledged: true,
  insertedId: ObjectId("654cb70ca71a47ec4d1ae7e0")
}
...
**7. Update city=SriLanka to John.**
...

...

**8. Remove the customer from Tokyo.**
**9.  Find customers not from Los Angeles.**
**10.Find the customers who are older than age 25.**
**11.Retrieve the males who are less than 25.**
**12.Update Francis age to 35, if Francis is not available upsert.**
**13.Retrieve males who are younger than 30 and older than25.**
**14.Find a customer who is lesser than or equal to 23.**
**15.Remove the customer from Tokyo.**
</code>
