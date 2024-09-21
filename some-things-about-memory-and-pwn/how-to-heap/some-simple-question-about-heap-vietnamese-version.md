# Some simple question about heap (vietnamese version)

### Tại sao sau khi sử dụng free thì vùng heap vẫn giữ nguyên

```
- Free mục đích đánh dấu khối bộ nhớ có thể sử dụng lại trong các lệnh malloc tương lai
- Giúp tăng hiệu xuất vì nó giảm số lần gọi hệ thống (sys call)
```

