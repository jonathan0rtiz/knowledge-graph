---
id: 50285ae8-2138-460f-98b5-67bee36ff3e7
title: Objects
desc: ''
updated: 1623640301037
created: 1623244802306
---

#### Javascript Objects
Although Javascript is an OOP language, there are no classes. 
```javascript
var superhero = {};
 
superhero.name = 'Superman';  
superhero.strength = 100;
```

Javascript objects are just like a Java HashMap of related properties, where the keys are Strings only. This means that Javascript is a multi-level 'hash map' of key/value pairs.
```java
// equivalent Java code
Map<String,Object> superhero = new HashMap<>();
 
superhero.put("name","Superman");  
superhero.put("strength", 100);
```

#### 'this' keyword usage
// add notes

#### Classic vs Prototypal Inheritance
In Javascript, there is no class inheritance instead objects can inherit directly from other objects. Each object has an implicit property that points to another object. That property is called `__proto__`, and the parent object is called the object's prototype, hence the name Prototypal Inheritance.
```javascript
var avengersHero = {  
    editor: 'Marvel'
};
 
var ironMan = {};
 
ironMan.__proto__ = avengersHero;
 
console.log('Iron Man is copyrighted by ' + ironMan.editor);
// output: Iron Man is copyrighted by Marvel
```

#### Closures vs lambdas
Javascript closures are not that different from Java anonymous inner classes.
```java
// Java

public interface FlyCommand {  
    public void fly();
}
 
public class FlyingHero {
 
    private String name;
 
    public FlyingHero(String name) {
        this.name = name;
    }
 
    public void fly(FlyCommand flyCommand) {
        flyCommand.fly();
    }
}
.
.
.
// We can can pass it a fly command like this in Java 8
String destination = "Mars";  
// Notice the lambda had to 'remember' the variable [destination]
superMan.fly(() -> System.out.println("Flying to " +  destination ));
```
This notion of a function that remembers about variables outside it's block scope for later use is called a **Closure** in Javascript.

A Javascript closure looks like this:
```javascript
var destination = 'Mars';
 
var fly = function() {  
    console.log('Fly to ' + destination);
}
 
fly();
```

#### Functions
Functions in Javascript are just values of type `Function`.
```javascript
var flyFunction = function() {  
    console.log('Flying like a bird!');
};
 
superhero.fly = flyFunction;
```
This creates a function (a value of type `Function`) and assigns it to a variable `flyFunction`. A new property named `fly` is then created in the `superhero` object, that can be invoked like this:
```javascript
// prints 'Flying like a bird!' to the console
superhero.fly();
```