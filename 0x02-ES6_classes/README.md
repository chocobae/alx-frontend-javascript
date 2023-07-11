# 0x02. ES6 classes

Introduction to JavaScript ES6 Classes JavaScript ES6 introduced a new way to define object-oriented classes using the class keyword. This syntax is similar to other object-oriented languages, such as Java or C#, and makes it easier for developers familiar with those languages to write object-oriented code in JavaScript.

Defining a Class To define a class in JavaScript ES6, you can use the class keyword followed by the name of the class. The class definition is enclosed in curly braces, and the body of the class contains the methods and properties of the class.

Here is an example of a simple class definition:

constructor(name, age) { this.name = name; this.age = age; }

sayHello() { console.log(Hello, my name is ${this.name} and I am ${this.age} years old.); } }```

Introduction to JavaScript ES6 Classes JavaScript ES6 introduced a new way to define object-oriented classes using the class keyword. This syntax is similar to other object-oriented languages, such as Java or C#, and makes it easier for developers familiar with those languages to write object-oriented code in JavaScript.

Defining a Class

To define a class in JavaScript ES6, you can use the class keyword followed by the name of the class. The class definition is enclosed in curly braces, and the body of the class contains the methods and properties of the class.

Here is an example of a simple class definition:

  constructor(name, age) {
    this.name = name;
    this.age = age;
  }```

  ```sayHello() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}```

The constructor method is a special method that is called when an instance of the class is created. It is used to initialize the properties of the object. In the example above, the constructor method takes two arguments: name and age, which are used to initialize the name and age properties of the object.
The sayHello method is a simple method that logs a greeting to the console.

## Creating an instance of a class
To create an instance of a class, you can use the new keyword followed by the name of the class. For example:
``` const person = new Person("John", 30);```

This creates a new instance of the Person class and assigns it to the person variable.
## Accessing properties and methods
Once you have an instance of a class, you can access its properties and methods using the dot notation. For example:
```console.log(person.name); // Outputs "John"
person.sayHello(); // Outputs "Hello, my name is John and I am 30 years old."```

## Extending a class
You can also create a new class that extends an existing class using the extends keyword. The new class will inherit all of the methods and properties of the parent class, and you can also add additional methods and properties.
Here is an example of a class that extends the Person class defined earlier:
``` class Student extends Person {
  constructor(name, age, major) {
    super(name, age);
    this.major = major;
  }```

  ```sayHello() {
    console.log(`Hello, my name is ${this.name} and I am studying ${this.major}.`);
  }
}```

The Student class has a constructor method that calls the constructor method of the parent class using the super keyword. It also has its own sayHello method that overrides the sayHello method of the parent class.
To create an instance of the Student class, you can use the same syntax as before:
```const student = new Student("Jane", 20, "Computer Science");```

### Conclusion
JavaScript ES6 classes provide


**1-make_classrooms.js:** Import the ClassRoom class from 0-classroom.js.
Implement a function named initializeRooms. It should return an array of 3 ClassRoom objects with the sizes 19, 20, and 34 (in this order).


**2-hbtn_course.js:** Implement a class named HolbertonCourse:
Constructor attributes:
name (String).
length (Number).
students (array of Strings).
Make sure to verify the type of attributes during object creation.
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
Implement a getter and setter for each attribute.


**3-currency.js:** Implement a class named Currency:
- Constructor attributes:
code (String).
name (String).
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
Implement a getter and setter for each attribute.
Implement a method named displayFullCurrency that will return the attributes in the following format name (code).


**4-pricing.js:** Import the class Currency from 3-currency.js
Implement a class named Pricing:
Constructor attributes:
amount (Number).
currency (Currency).
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
Implement a getter and setter for each attribute.
Implement a method named displayFullPrice that returns the attributes in the following format amount currency_name (currency_code).
Implement a static method named convertPrice. It should accept two arguments: amount (Number), conversionRate (Number). The function should return the amount multiplied by the conversion rate.


**5-building.js:** Implement a class named Building:
Constructor attributes:
sqft (Number).
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
Implement a getter for each attribute.
Consider this class as an abstract class. And make sure that any class that extends from it should implement a method named evacuationWarningMessage.
If a class that extends from it does not have a evacuationWarningMessage method, throw an error with the message Class extending Building must override evacuationWarningMessage.


**6-sky_high.js:** Import Building from 5-building.js.
Implement a class named SkyHighBuilding that extends from Building:
Constructor attributes:
sqft (Number) (must be assigned to the parent class Building).
floors (Number).
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
Implement a getter for each attribute.
Override the method named evacuationWarningMessage and return the following string Evacuate slowly the NUMBER_OF_FLOORS floors.


**7-airport.js:** Implement a class named Airport:
Constructor attributes:
name (String).
code (String).
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
The default string description of the class should return the airport code (example below).


**8-hbtn_class.js:** Implement a class named HolbertonClass:
Constructor attributes:
size (Number).
location (String).
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
When the class is cast into a Number, it should return the size.
When the class is cast into a String, it should return the location.


**9-hoisting.js:** Fix this code and make it work.

const class2019 = new HolbertonClass(2019, 'San Francisco');
const class2020 = new HolbertonClass(2020, 'San Francisco');

export class HolbertonClass {
  constructor(year, location) {
    this._year = year;
    this._location = location;
  }

  get year() {
    return this._year;
  }

  get location() {
    return this._location;
  }
}

const student1 = new StudentHolberton('Guillaume', 'Salva', class2020);
const student2 = new StudentHolberton('John', 'Doe', class2020);
const student3 = new StudentHolberton('Albert', 'Clinton', class2019);
const student4 = new StudentHolberton('Donald', 'Bush', class2019);
const student5 = new StudentHolberton('Jason', 'Sandler', class2019);

export class StudentHolberton {
  constructor(firstName, lastName) {
    this._firstName = firstName;
    this._lastName = lastName;
    this._holbertonClass = holbertonClass;
  }

  get fullName() {
    return `${this._firstName} ${this._lastName}`;
  }

  get holbertonClass() {
    return this.holbertonClass;
  }

  get fullStudentDescription() {
    return `${self._firstName} ${self._lastName} - ${self._holbertonClass.year} - ${self._holbertonClass.location}`;
  }
}


export const listOfStudents = [student1, student2, student3, student4, student5];


**10-car.js:** Implement a class named Car:
Constructor attributes:
brand (String).
motor (String).
color (String).
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
Add a method named cloneCar. This method should return a new object of the class.


**100-evcar.js:** Import Car from 10-car.js.
Implement a class named EVCar that extends the Car class:
Constructor attributes:
brand (String).
motor (String).
color (String).
range (String).
Each attribute must be stored in an “underscore” attribute version (ex: name is stored in _name).
For privacy reasons, when
