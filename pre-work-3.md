# ES6 Classes

## Objects and Inheritance
* JavaScript objects use prototype-based inheritance.
* It can be loosely described by saying that when methods or properties are attached to object’s prototype they become available for use on that object and its descendants, but not directly attached to them.
* Prototype Inheritence:

function Animal(name) {
  this.name = name;
}
Animal.prototype.walk = function() {}

function Bird(name) {
  // I can do all the things animals can do!
  Animal.call(this, name);
}
// Unlike other animals, birds can fly
Bird.prototype.fly = function() {}

// Make a new bird ..
let parrot = new Bird('parrot');
parrot.fly();
parrot.walk();

## Classes
* Classes are standalone, self-contained object (instance) factories. Ultimately, they result in a prototype, but are easier to comprehend and work with.
* **function()** becomes **class {}**
* **call()** becomes **extends**

class Animal {
  constructor(name) {
    this.name  = name;
  }

  walk() {}
}

// Thanks to 'extends', all birds can now do all things animals can
class Bird extends Animal {
  // Birds can walk, becuase they're animals also do their own thing.
  fly() {}
}

// Make one (the same was as before, but wasn't the class creation much easier?)
let parrot = new Bird('parrot');
parrot.fly();
parrot.walk();


## Examples
const Animal = function(name, legs) {
  this.name = name;
  this.legs = legs;
  this.eat = function() {
    this.isEating = true;
  }
}
Animal.prototype.walk = function() {
  this.isWalking = true;
}

const Dog = function(name, legs) {
  Animal.call(this, name, legs);
}
Dog.prototype = Object.create(Animal.prototype);

let puppy = new Dog('blake', 4);
puppy.walk();
puppy.eat();
console.log(puppy);
console.log(puppy instanceof Animal);
console.log(puppy instanceof Dog);



const Animal = function(name, legs) {
  this.name = name;
  this.legs = legs;
  this.eat = function() {
    this.isEating = true;
  }
}
Animal.prototype.walk = function() {
  this.isWalking = true;
}

const Dog = function(name, legs) {
  Animal.call(this, name, legs);
}
Dog.prototype = Object.create(Animal.prototype);

let puppy = new Dog('blake', 4);
puppy.walk();
puppy.eat();
console.log(puppy);
console.log(puppy instanceof Animal);
console.log(puppy instanceof Dog);


### References
* <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain>
* <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this>
* <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes>
