**1.Útskýrðu Prototype kerfiðí JavaScript. Hver er munurinn á því t.d. og 
Object-Oriented forritun (OOP)í öðrum málumeins og Python? (1%)**

Prototype er sérstakt oobject-oriented-forritun sem leyfir manni að endurnota klasana með t.d að klóna hann.
Munurinn er að prototype vinnur með objectið en oop vinnur frá objectinu .

**2.Útskýrðu eins vel og þú getur hvað gerist í kóðanum(1%)**
  a.Þegar prototype er slepp
b.Hvað gerir prototype í Book.prototype.getIsbn
 ```javascript
function Book(isbn) {
this.isbn = isbn;}
// Book.prototype.getIsbnBook.getIsbn = function () {return "Isbn is " + this.isbn;};
 ```
A Þá vísa allir Book() hlutir á sama fall og það kemur mjög líklega villa
B Prototype sérgreinir fallið og gerir sína eigin útgáfu til að spara minnið

**3.Classical Model (function constructor and prototype)(2%)**
 ```javascript
 a.
 
 function createShip(name,life,speed){
    this.name = name;
    this.life = 10;
    this.speed = 10;
};

b.
let space_1 = new createShip(["battlesstar"],10,7); 
let space_2 = new createShip(["falcon"],10,8);
let space_3 = new createShip(["dargon_destroy"],10,10);

c.
createShip.prototype.fly= function(){this.speed += 1};

d.
var space_4 = Object.create(space_2);
space_4.setlife = function(){this.life += 1}; 

var space_5 =Object.create(space_4)
space_5.setlife = function(){this.life +=1};

 ```
