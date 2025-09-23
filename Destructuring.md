# Destructuring

Menyalin dan membuat `array/obj` baru, bisa untuk `field/element` tertentu

## Array

```js
const name = ["farid", "nubaili", "alkatiri"]
const [firstName, lastName, ...others] = name
// others = ["alkatiri"]
```

## Objek

(nama key harus sesuai)

```js
const person = {
 firstName: "farid", 
 lastName: "nubaili", 
 age: 23
}
const [firstName, lastName, ...others] = person

// others = {age: 23}

//  nested
// mengambil field name dan country dari address
{
 name, 
 address:{name, country}, 
 contact
 }
```
