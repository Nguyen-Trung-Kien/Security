# Memory Areas

## Stack Segment

used primarily to manage local variables and information related to functions

* **LIFO Principle**: The stack operates on a "Last In, First Out" (LIFO) principle, meaning that the last item added to the stack is the first one to be removed.
* **Initialization and Deallocation**(Khởi tạo và giải phóng): When a function is called, a new stack frame is created to store information for that function. When the function exits, this frame is deallocated.

Components of a Stack Frame:&#x20;

* **Return address:** The address of the next instruction to execute after the function finishes.
* **Local variables**: Các biến được khai báo trong hàm
* **Argument parameters**: Các tham số được truy vào hàm
* **Saved copies of registers modified by subprograms that could need restoration**(Temporary Data): Thông tin tạm thời cần thiết cho việc thực thi hàm, có thể là thông tin sao lưu từ thanh ghi

Size and Limits:

* **Size limit**: Kích thước của stack thường có giới hạn nhất định (có thể thay đổi theo hệ điều hành hoặc cấu hình). Nếu quá giới hạn, sẽ xảy ra lỗi tràn stack (stack overflow).
* **Frame Size:** Các biến cục bộ sẽ tự động được giải phóng khi hàm kết thúc, giúp giảm nguy cơ rò rỉ bộ nhớ.

## HEAP Segment

used to manage cached memory

**Structure And Operation**

* **Dynamic Memory Management:** Heap cho phép cấp phát và giải phóng bộ nhớ trong quá trình thực thi của chương trình. Khi cần bộ nhớ, chương trình có thể yêu cầu từ heap thay vì sử dụng stack.
* **No Fixed Structure**: Dữ liệu trong heap có thể được lưu trữ ở các địa chỉ không liên tiếp, và các khối bộ nhớ có thể có kích thước khác nhau.

**Memory Allocation**

* **Allocation Functions**: Trong C/C++, bạn sử dụng các hàm như `malloc`, `calloc`, `realloc` để cấp phát bộ nhớ từ heap, và `free` để giải phóng bộ nhớ.
* **Timing of Allocation**: Bộ nhớ có thể được cấp phát bất kỳ lúc nào trong quá trình thực thi, không giống như stack, nơi bộ nhớ được cấp phát và giải phóng theo thứ tự.

## Text Segment

contains the compiled machine code of the program, which the CPU will execute. It includes the instructions that make up the logic and functionality of the program.

**Characteristic**

* Read Only: Vùng text segment thường được đánh dấu là chỉ đọc để ngăn chặn việc sửa đổi mã trong quá trình thực thi. Điều này giúp bảo vệ tính toàn vẹn của chương trình.
* Fixed Size: Kích thước của vùng text segment được xác định tại thời điểm biên dịch và giữ nguyên trong suốt quá trình thực thi.

Structure

* Function Definitions:Chứa mã biên dịch cho tất cả các hàm được định nghĩa trong chương trình.
* Global Variables (if applicable): Một số hằng số toàn cục có thể cũng được lưu trữ ở đây.
* Instruction Order: Các lệnh trong vùng text segment được sắp xếp theo thứ tự mà chúng sẽ được thực thi.
