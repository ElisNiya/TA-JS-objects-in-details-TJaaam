In this assignment you have to add methods to the `prototype` of Array. Array is a constructor function and all the array methods like `map`, `forEach` and `filter` etc comes from `Array.prototyp`. So when you add a new method in `Array.prototype` the method gets added to all the instance of the array.

1. Create a function named `myMap` and add the method to `Array.prototype`. `myMap` will behave similar to how the `Array.map` works. To test the implementation use the code below.



Array.prototype.myMap = function(cb){
   let final = [];
      for(let i = 0; i<this.length; i++){
         const element = this[i];
         cb(element, i, this);
         final.push(cb(element,i, this))
      }
      return final;
}
 
  


**You should know once you add an extra method to Array.prototype and refresh the page. The method you added will be gone.**

2. Add a method named `myFilter` to Array.prototype. myFilter should behave similar to Array.filter. After adding the function test it using the code below.
Array.prototype.myFilter = function(cb){
  let final = [];
      for(let i = 0; i<this.length; i++){
         const element = this[i];
            if(cb(element, i, this)){
            final.push(cb(element,i, this))
            }
      }
      return final;
  }
3. Add a method named `shuffle` to Array.prototype. Using the method shuffle will return a new array and in the new array the index of the elements will be shuffled (randomly reorders).
  Array.prototype.shuffle =function(){
   return [...this.sort(() => Math.random() - 0.5)]
  }
   
4. Add a method named `unique` to Array.prototype. Using the method will return a new array and it should only contain unique elements in the array. Unique means no element should come multiple times.
Array.prototype.unique = function(){
     return this.reduce((acc,cv) =>{
         if(!acc.includes(cv)){
            acc.push(cv)
         }
         return acc;
     },[])
  }
 
5. Add a method named `intersection` to Array.prototype. The method intersection will accept an array and returns a new array that will contain only element that is common in both the array.
Array.prototype.intersection = function(arr){
     return this.reduce((acc,cv) =>{
         if(acc.includes(cv)){
            acc.push(cv)
         }
         return acc;
     },[]).unique();   //to take once only
  }
 
6. Add a method named `chunk` to Array.prototype. The method chunk will accept one parameter `length` and split the array into groups the length of size. If array can't be split evenly, the final chunk will be the remaining elements. `length` should default to 1.
 
 Array.prototype.chunk = function(size = 1){
   let arr = [...this];
   let final = [];
 for(let i = 0; i <= Math.floor(this.length/size); i++){
   let chunk = arr.splice(0, size);
   final.push(chunk)
  }
  return final.filter((elm) => elm.length);
}
