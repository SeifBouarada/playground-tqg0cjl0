# Call(), Apply() and Bind() Methods in JavaScript.

Working with JavaScript “this” keyword can be tricky. Not knowing the background rules may end up with the famous “it works, but I don’t know why” or worse: “it doesn’t work and I don’t know why”. It’s good to know the theory before putting things into practice. Call(), Apply() and Bind() methods can come in handy when setting the “this” value.

#### <strong>Basic rules worth remembering:</strong>
<ol>
<li>“this” always refers to an object.</li>
<li>“this” refers to an object which calls the function it contains.</li>
<li>In the global context “this” refers to either window object or is undefined if the ‘strict mode’ is used.</li>
</ol>

```javascript
var car = { 
    registrationNumber: "GA12345",
    brand: "Toyota",

    displayDetails: function(){
        console.log(this.registrationNumber + " " + this.brand);
    }
}
```
The above will work perfectly fine as long as we use it this way:
```javascript
car.displayDetails()
```
But what if we want to borrow a method?
```javascript
var myCarDetails =  car.displayDetails;
myCarDetails()
```

Well, this won’t work as the “this” will be now assigned to the global context which doesn’t have neither the registrationNumber nor the brand property.

## The Bind() Method


