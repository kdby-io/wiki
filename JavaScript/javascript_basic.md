# JavaScript

```js
confirm("~");
prompt("question");
prompt("question", "placeholder");

console.log();

"abcdef".substring(3,5);
"abcdef".length;
"abcdef".toUpperCase();
"abcdef".toLowerCase();

var a; // 함수 scope
let b; // 블럭 scope
c; // 변수 찾아 쭉 올라가다가 없어서 전역 scope

// ==은 값만 비교, ===은 값과 데이터 타입을 모두 비교

var func_name = function (parameter) {
	return parameter;
};
function func_name(parameter) {	//코드 위치 상관없음

}

Math.random();
Math.floor(3.2);

var array = [3, 5, "a"];
var array = new Array();
array.length
array.push("abc");

isNaN('abc');	//true
isNaN('43');	//false -> 자동으로 숫자로 바꾼다.
isNaN(43);		//false

//object 선언1
var a = {
	key: value,
	key2: value2,
	func: function() {};
}
//object 선언2
var a = new Object();

a.key;
a["key"];

for (var key in array) {

}

// 생성자
function Person(name, age) {
	this.name = name;
	this.age = age;
}
var a = new Person("a", 11);

typeof a;

myObj.hasOwnProperty('name');

// prototype의 프로퍼티 추가
Animal.prototype.name = 'a';

function Animal() {}
function Dog() {}
Dog.prototype = new Animal()	// 상속


function Class(a) {
	this.a = 1;	// public 프로퍼티
	var b = 2;	// private 프로퍼티
	this.getB = function() {	// public 메소드
		return b;
	};

	var method1 = function() {};	// private 메소드
	this.method2 = function() {		// public 메소드
		return method1;
	}
}

```
