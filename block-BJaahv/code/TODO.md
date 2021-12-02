# 🎖 Object Creation Patterns

Create a object using the following patterns given below.

## Create in all 4 formats

- [ ] Using function to create object
- [ ] Using Object.create (prototypal pattern)
- [ ] Using Pseudoclassical Way
- [ ] Using Class

## Requirements

Create User (class/function) with the following properties.

- [ ] properties (data):
  - [ ] name
  - [ ] id
  - [ ] noOfProjects
- [ ] methods:
  - [ ] getProjects -> return number of project
  - [ ] changeName -> accepts one parameter (newName)returns old user name
  - [ ] incrementProject -> returns updated number of projects
  - [ ] decrementProject -> returns updated number of projects

Write 2 tests for all the different ways of creating object. Test all the methods on these objects.
____________-

function createUser(name, id, noOfProjects){
  let user = {};
  user.name = name;
     this.id = id;
    this.noOfProjects= noOfProjects;
    user.getProjects = function() {
    return user.noOfProjects;
    
   }
   user.changeName(newName){
    let prevName = user.name;
    user.name = newName;
    return prevName;
   } 
    user.incrementProject = function(){
    return noOfProjects++;
  }
  user.decrementProject = function(){
  return noOfProjects--;
  }
}
_______________
class User {
  constructor(name, id, noOfProjects){
    this.name = name;
    this.id = id;
    this.noOfProjects= noOfProjects;
  }
  getProjects(){
    return this.noOfProjects
  }
  changeName(newName){
      this.name = newName;
  }
  incrementProject(){
    return noOfProjects++;
  }
  decrementProject(){
  return noOfProjects--;
  }
}
