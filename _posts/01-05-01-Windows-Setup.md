---
isChild: true
anchor:  windows_setup
---

## Thiết lập trên Windows {#windows_setup_title}

Bạn có thể tải xuống file cài đặt từ [windows.php.net/download][php-downloads]. Sau khi giải nén PHP, bạn nên thiết lập [PATH][windows-path] đến thư mục gốc của thư mục PHP (nơi chứa file php.exe) của bạn để bạn có thể thực thi PHP từ bất cứ đâu.

Đối với học tập và dev local, bạn có thể dùng webserver cung cấp sẵn từ PHP 5.4+ và không cần lo lắng về việc cấu hình. Bạn cũng có thể cài đặt các gói "all-in-one" có đầy đủ webserver và MySQL như là [Web Platform Installer][wpi], [XAMPP][xampp], [EasyPHP][easyphp], [OpenServer][openserver] và [WAMP][wamp] sẽ giúp có được môi trường phát triển Windows và chạy một cách nhanh chóng. Điều đó nói rằng, những công cụ này sẽ khác một chút so với sản xuất, vì vậy hãy cẩn thận về sự khác biệt về môi trường nếu bạn đang làm việc trên Windows và triển khai lên Linux.

Nếu bạn cần chạy production system của mình trên Windows, thì IIS7 sẽ cung cấp cho bạn hiệu suất ổn định và tốt nhất. Bạn có thể dùng [phpmanager][phpmanager] (một loại GUI plugin cho IIS7) để cấu hình và quản lý PHP một cách đơn giản. IIS7 đi kèm với FastCGI được tích hợp sẵn và sẵn sàng để đi, bạn chỉ cần cấu hình PHP như một trình xử lý (handler). Để được hỗ trợ và có thêm nguồn lực bổ sung, có một [khu vực dành riêng trên iis.net][php-iis] cho PHP.

Nói chung chạy ứng dụng của bạn trên môi trường khác nhau trong phát triển và sản xuất có thể dẫn đến các lỗi lạ xuất hiện khi bạn live. Nếu bạn đang phát triển trên Windows và triển khai lên Linux (hoặc bất kỳ thứ gì không phải Windows) thì bạn nên cân nhắc sử dụng một [Máy ảo](#virtualization_title).

Chris Tankersley có một bài đăng trên blog rất hữu ích về những công cụ mà anh ta sử dụng để [phát triển PHP bằng Windows][windows-tools].

[easyphp]: http://www.easyphp.org/
[phpmanager]: http://phpmanager.codeplex.com/
[openserver]: http://open-server.ru/
[wamp]: http://www.wampserver.com/en/
[php-downloads]: http://windows.php.net/download/
[php-iis]: http://php.iis.net/
[windows-path]: http://www.windows-commandline.com/set-path-command-line/
[windows-tools]: http://ctankersley.com/2016/11/13/developing-on-windows-2016/
[wpi]: https://www.microsoft.com/web/downloads/platform.aspx
[xampp]: http://www.apachefriends.org/en/xampp.html
