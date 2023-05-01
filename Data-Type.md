###Kiểu dữ liệu
Trong JS có 6 kiểu dữ liệu cơ bản ( kiểu dữ liệu nguyên thuỷ primitive ):

- Number : Số
- Boolean : Logic ( true, false)
- String : Xâu kí tự


- Null : Không có giá trị
- Undefined : Không định nghĩa
- Object : Đối tượng

> Trong JS không có khái niệm kiểu dữ liệu cứng, không cần chỉ định rõ ràng kiểu, JS tự động ép kiểu phù hợp...

- Ví dụ :
```js
let name = "anh" //tự ép kiểu name là string
let numOfStudent = 4 //tự nhận dạng numOfStudent là number
let studentObject = {
    "name":"anh",
    "age":"19
} // tự nhận dạng là object
```


Và các kiểu dữ liệu  cũng có thể có method và property như object, nhưng thực sự không phải. Đó là trick của JS, khi chúng ta dùng tới bất kì property hoặc method nào, JS sẽ biến đối tượng primitive thành một wrapper. Wrapper là kiểu primitive, được gói thành một object và sử dụng như object, do đó nó có thuộc tính và phương thức.

```js
let x = new Number(10);
let s = new String("Hello");
let z = new Boolean(true);
```

Tuy nhiên, không nên sử dụng dạng như trên. Nó vừa gây rối code, vừa dài dòng không cần thiết, lại vừa sinh ra một số vấn đề khác. Ví dụ như phép so sánh hai kiểu wrapper sẽ luôn trả về false, vì JS không so sánh value chứa bên trong. Nếu bạn không hiểu rõ, bạn sẽ gặp lỗi. Do đó, primitive thì cứ dùng như bình thường thôi.

Và đối với wrapper, có thể dùng method ``valueOf()`` để lấy ra nội dung primitive được gói bên trong.

Kiểu dữ liệu còn lại là object, có thể chứa thuộc tính (property) và phương thức (method). Object phải được khởi tạo bằng từ khóa new và Object constructor.
```js
let obj = new Object();
...
```

Các phiên bản JS mới hơn cho phép sử dụng cú pháp dấu ngoặc {} để tạo object gọn gàng hơn.

```js
let obj = {
    ...
}
```
Từ kiểu object, có thể phát sinh thêm nhiều kiểu object khác, như mảng (array) cũng là object, function cũng là object (mặc dù tên kiểu là function), Date cũng là object,...

- Kiểu dữ liệu Date : Ngày tháng
```js
let birthDay = new Data() //lấy thời gian hiện tại
```

Kết quả :
```
Wed Apr 26 2023 21:38:43 GMT+0700 (Indochina Time)
```
```js
let birthDay = new Date(2000,3,23,5,6,9,34) //đặt thời gian là ngày ngày 23/3/2000 05:06:09:34
```
Kết quả :
```
Sun Apr 23 2000 05:06:09 GMT+0700 (Indochina Time) {}
```



###Liên quan :
[Null, Undefined, NaN](./null-undefined-nan.md)
[Object](./object.md)