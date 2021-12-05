## Create Class

Convert the give image into class using inheritance.

- `name` is the property
- `eat()` is the method

Property ending with `()` is method. And others are properties.

![Inheritance](../assets/inheritance.png)


class Person {
  constructor(name, age,gender){
      this.name = name;
      this.age = age;
      this.gender = gender;
  }
  eat(){
  
  }
  sleep(){
  
  }
  walk(){
  
  }
}

class Player extends Person {
  constructor(super(name, age,gender,sportsName){
   this.sportsName = sportsName
   super(name, age,gender);
  }
  play(){
  
  }
}

class Teacher extends Person {
  constructor(name, age,gender,instituteName){
  super(name, age,gender);
    this.instituteName = instituteName;
  }
  teach(){
  
  }
}
class Artist extends Person {
  constructor(name, age,gender,kind){
    super(name, age,gender);
    this.kind = kind
  }
    createArt(){
  
  }
}

class Cricketer extends Player {
  constructor(name, age,gender,sportsName, teeamName){
    super(name, age,gender, sportsName);
    this.teamName = teamName;
    }
    playCricket(){
  
  }
}
