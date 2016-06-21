## Node.js

```js
var module = require('module');	// 모듈 불러오기


var fs = require('fs');
// 동기적으로 파일 읽기
var data = fs.readFileSync('input.txt');
console.log(data.toString());
console.log("Program has ended");

// 비동기적으로 파일 읽기
fs.readFile('input.txt', function(err, data) {
  if (err) return console.error(err);
  console.log(data.toString());
});
console.log("Program has ended");


/////// 이벤트 예제 ///////
var events = require('events');	// events 모듈 사용
var eventEmitter = new events.EventEmitter();	// EventEmitter 객체 생성
var connectHandler = function connected() {	// EventHandler 함수 생성
  console.log("Connection Successful");

  eventEmitter.emit("data_received");	// data_received 이벤트를 발생시키기
}
eventEmitter.on('connection', connectHandler);
eventEmitter.on('data_received', function() {
  console.log("Data Received");
});
eventEmitter.emit('connection');
console.log("Program has ended");
// 'connection' 이벤트 발생 -> connectHandler 함수 실행 -> 'data_received' 이벤트 발생 -> 익명 함수 실행
```


참조 : https://velopert.com
