# Inheritance

Convert the below requirements into inheritance using prototypal patters.

#### Animal

Properties:

- `location`
- `numberOfLegs`

Methods

- `eat()` - log a message saying `I live in ${location} and I can eat`

- `changeLocation(newLocation)` - accepts location and updates the location of the animal

- `summary()` - returns `I live in ${location} and I have ${numberOfLegs}`


```js
class Animal{
constructor(location, numberOfLegs){
  this.location = location;
  this.numberOfLegs = numberOfLegs
  }
  eat(){
  `I live in ${location} and I can eat`
  }
  changeLocation(newLocation){
    this.location = newLocation;
  }
  summary(){
    return `I live in ${location} and I have ${numberOfLegs}`
  }
}

```


#### Dog

It will have all the properties and methods of the Animal. These are the extra properties and methods these dogs will have.

Properties:

- `name`
- `color`

Methods:

- `bark()` - alerts a message saying `I am ${name} and I can bark 🐶`
- `changeName(newName)` - accepts the name property and updates the name of the dog
- `changeColor(newColor)` - accepts the new color and updates the color of the dog
- `summary()` - returns `I am ${name} and I am of ${color} color. I can also bark`


class Dog extends Animal{
  constructor(name, color){
    this.name = name,
    this.color = color,
    super(name, color)
  }
  bark(){
  return `I am ${name} and I can bark 🐶`
  }
  changeName(newName){
    this.name = newName;
  }
  changeColor(newColor){
    this.color = newColor;
  }
  summary(){
  return `I am ${name} and I am of ${color} color. I can also bark`
  }
}

#### Cat

It will have all the properties and methods of the Animal. These are the extra properties and methods these dogs will have.

Properties:

- `name`
- `colorOfEyes`

Methods:

- `meow()` - alerts a message saying `I am ${name} and I can mewo meow 😹`

- `changeName(newName)` - accepts the name property and updates the name of the dog

- `changeColorOfEyes(newColor)` - accepts the new color and updates the color of the dog

- `summary()` - returns `I am ${name} and the color of my eyes are ${colorOfEyes}. I can also do meow meow`



class Cat extends Animal{
  constructor(name, colorOfEyes){
    this.name = name,
    this.color = colorOfEyes,
    super(name, colorOfEyes)
  }
  meow(){
  return `I am ${name} and I can mewo meow 😹`
  }
  changeName(newName){
    this.name = newName;
  }
  changeColorOfEyes(newColor){
    this.color = newColor;
  }
  summary(){
  return `I am ${name} and the color of my eyes are ${colorOfEyes}. I can also do meow meow`
  }
}
