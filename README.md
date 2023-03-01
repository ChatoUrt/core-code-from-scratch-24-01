# core-code-from-scratch-24-01

## ---"This" is another problem---

* [Test](https://www.codewars.com/kata/547f1a8d4a437abdf800055c/train/javascript)

Solution / /

``` javascript {
function NamedOne(first, last) {
    // -- SHOULD be changed --
    this._firstName = first;
    this._lastName = last;

  
    Object.defineProperties(this, {
      firstName: {
        get: function() {
          return this._firstName;
        },
        set: function (newFirstName) {
          this._firstName = newFirstName;
        }
      },
      lastName: {
        get: function() {
          return this._lastName;
        },
        set: function (newLastName) {
           this._lastName = newLastName;
        }
      },
      fullName: {
         get: function() {
          return `${this._firstName} ${this._lastName}`;
        },
        set: function (newFullName) {
          const newFullNameArray = newFullName.trim().split(' ');
          if(newFullNameArray.length == 2) {
            this._firstName = newFullNameArray[0];
            this._lastName = newFullNameArray[1];
          }
        }
      },
    });
}
```
---

## ---Who likes it---

* [Test](https://www.codewars.com/kata/5266876b8f4bf2da9b000362/train/javascript)

Solution / /

``` javascript
function likes(names) {
  switch(names.length){
    case 0: return 'no one likes this'; break;
    case 1: return names[0] + ' likes this'; break;
    case 2: return names[0] + ' and ' + names[1] + ' like this'; break;
    case 3: return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this'; break;
    default: return names[0] + ', ' + names[1] + ' and ' + (names.length - 2) + ' others like this';
  }
}
```
---

## ---Convert str to camel case---

* [Test](https://www.codewars.com/kata/517abf86da9663f1d2000003/train/javascript)

Solution / / 

``` javascript 
function toCamelCase(str){
  if(str === '') return str;
  let noSpace = str.replace(/-/g, ' ').replace(/_/g, ' ');
  const mayus = noSpace.split(' ');
  for (let i = 1; i < mayus.length; i++) {
    mayus[i] = mayus[i][0].toUpperCase() + mayus[i].substr(1);
  }
  let result = mayus.join(' ').replace(/[' ']/g, '');
  return result;
}
```
---

## ---Knowledge Base---

* [Object Define Property](https://programacion.net/articulo/como_utilizar_los_metodos_defineproperty_y_defineproperties_1923)
