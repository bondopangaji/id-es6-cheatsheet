<div id="top"></div>


<div align="center">

<h3 align="center">ES6 Cheatsheet</h3>
    <p align="center">
        ECMAScript 6 Cheatsheet versi guweh
    </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
   <summary>Table of Contents</summary>
   <ol>
      <li><a href="#scope">Scope</a></li>
      <li><a href="#object-mutation">Object Mutation</a></li>
      <li><a href="#arrow-function">Arrow Function</a></li>
      <li><a href="#license">License</a></li>
      <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- Lingkup -->
## Scope

##### Karakteristik:

| `var`                                       | `let`                                       | `const`                                          |
|---------------------------------------------|---------------------------------------------|--------------------------------------------------|
| functional scope                            | block scope                                 | block scope                                      |
| bisa deklarasi tanpa <br/>inisialisasi nilai| bisa deklarasi tanpa <br/>inisialisasi nilai| gak bisa deklarasi tanpa<br/> inisialisasi nilai |
| bisa di-update dan bisa redeclare           | bisa di-update tapi gak bisa redeclare      | gak bisa di-update dan di-redeclare              |

```js
function varFn() {
  var a = 99 // fn scope, bisa diakses selama masih didalem function
  console.log(a) // 99
}

varFn();
console.log(a); // gak bisa diakses, udah di luar lingkup fungsi


let a = 99

function letFn() {
  if (true) {
    let b = 9
    console.log(b) // bakalan ngeprint objek b yang ada di lingkup if
  }
  console.log(b) // gak bisa diakses karena deklarasi di lingkup if
}

letFn()
console.log(a) // 99


const a = 99

function constFn() {
  if (true) {
    const b = 9
    console.log(b) // bakalan ngeprint objek b yang ada di lingkup if
  }
  console.log(b) // gak bisa diakses karena deklarasi di lingkup if
}

constFn()
console.log(a) // 99


var aa = 'aa'
var aa = 'bb' // aman aja, 'aa' bisa diganti dengan 'bb'


let bb = 'aa'
let bb = 'bb' // ga bisa re-declare


const cc = 'aa'
const cc = 'bb' // ga bisa re-declare

```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- Mutasi -->
## Object Mutation

developer sekarang demen make `const`, kecuali kalo emang butuh banget buat update value mereka make `let`

```js
// mutasi objek array
const arr = [1, 2, 3]
arr[2] = 99 // assign value di index 2 jadi 99
console.log(arr) // [ 1, 2, 99 ]


// mutasi objek js
const objMut = {
  name: "John Doe",
  age: 99
}
objMut.name = "Jane Doe" // mutasi data name jadi "Jane Doe"
objMut.age = 100 // mutasi data age jadi 100
console.log(objMut) // { name: 'Jane Doe', age: 100 }


// cegah buat objek bisa dimutasi
const obj = {
  name: "John Doe",
  age: 99
}
Object.freeze(obj) // freeze function buat cegah objek di-mutasi
obj.name = "Jane Doe"
obj.age = 100
console.log(obj) // { name: 'John Doe', age: 99 }

```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- Fungsi Panah -->
## Arrow Function

fungsi gak bernama? pake fungsi arrow/panah

lambda function gak sih? roughly the same thing!

```js
// fungsi b aja
const myFunc = function () {
  const myVar = "value"
  return myVar
}


// fungsi arrow
const myFunc = () => {
  const myVar = "value"
  return myVar
}


// kalau cuma butuh return value, bisa lebih simpel lagi
const myFunc = () => "value";


// pake parameter vesi body
const multiplierFn = (val, multi) => {
  const result = val * multi
  return result
}


// pake parameter versi inline-body
const multiplierFn = (val, multi) => val * multi


// pake default parameter
const incrementFn = (number, value = 1) => number += value
console.log(increment(1, 2)) // 3
console.log(increment(1)) // 2, karena default value = 1

```

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->

## Contact

Bondo Pangaji - [bondopangaji@gmail.com](mailto:bondopangaji@gmail.com)

Project Link: [https://github.com/bondopangaji/id-es6-cheatsheet](https://github.com/bondopangaji/id-es6-cheatsheet)

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- REFERENCE -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
