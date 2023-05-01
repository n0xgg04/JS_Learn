##Try-catch-finally trong JS
Xử lý ngoại lệ lỗi trong Javascript

```js
try {
    //code
    throw "lỗi" //trả về lỗi và đi tới catch
}
catch(err){ //lỗi thay vì hiện trên console sẽ gán vào err

}finally{
    //code xử lý sau khi chạy code trong try mà không có lỗi
}
```

#####Xử lý cho từng loại lỗi
```js
try {
  foo.bar();
} catch (e) {
  if (e instanceof EvalError) {
    console.error(`${e.name}: ${e.message}`);
  } else if (e instanceof RangeError) {
    console.error(`${e.name}: ${e.message}`);
  }
  // etc.
  else {
    // If none of our cases matched leave the Error unhandled
    throw e;
  }
}
```