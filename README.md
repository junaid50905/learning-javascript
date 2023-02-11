# learning-javascript
  - <a href="#object">object methods</a>
    - <a href="#object_preventExtensions_seal_freeze">object.preventExtensions(), object.seal(), object.freeze()</a>
 
 <br>
 -------------------------------------------------------------------------------------------------

<h2 id="object">
Object
</h2>
<h4 id="object_preventExtensions_seal_freeze">object.preventExtensions(), object.seal(), object.freeze()</h4>

```javascript
var person = {
  name: 'junaid',
  age: 19,
  address: {
    presentAddress : 'Gazipur',
    permanentAddress : 'Chandpur'
  },
  phone: {
    home: '0150000',
    office: '01600',
    shop : {
      shopPhoneOne : '012000000',
      shopPhoneTwo : '01900000'
    }
  }
}
//for a mutable object we can do anything
//add
person['maritalStatus'] = 'unmarried'
//modify
person.name = 'arman'
//delete
delete person.age
console.log('mutable object ',person);
```

### freeze(object)
```javascript
var freezePerson = Object.freeze(person)
console.log('freeze object',freezePerson);
```
top level property: name, age, address, phone <br>

second level property: presentAddress,permanentAddress, home, office, shop <br>

third level property: shopPhoneOne, shopPhoneTwo <br>

<p>Here we can not change the top lavel property. But We can change the properties of all levels except the top level.
</p>

#### example :
```javascript
var freezePerson = Object.freeze(person)
//can't modify
freezePerson.name = 'arman'
//can't add
freezePerson['maritalStatus'] = 'unmarried'
//can't delete
delete freezePerson.age
console.log('freeze object',freezePerson);
```
<font style="color: red">TypeError: Cannot assign to read only property 'name' of object '#<Object>'</font>

<p>
</p>
```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
---------------------------------------------------------------------------------------------------
