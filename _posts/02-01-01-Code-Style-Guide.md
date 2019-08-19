---
anchor: code_style_guide
---

# Hướng dẫn code đẹp và chuẩn (Code Style) {#code_style_guide_title}

Cộng đồng PHP rất lớn và đa dạng, bao gồm vô số thư viện, frameworks và components. Thông thường các nhà phát triển PHP chọn một vài trong số này và kết hợp chúng thành một dự án duy nhất. Điều quan trọng là mã PHP tuân thủ (càng gần càng tốt) một code style chung để giúp các nhà phát triển dễ dàng trộn và kết hợp các thư viện khác nhau cho các dự án của họ.

[Framework Interop Group][fig] đã đề nghị và phê duyệt một loạt các đề nghị về code style. Không phải toàn bộ chúng đều liên quan đến code style, nhưng những thứ đó là [PSR-1][psr1], [PSR-2][psr2] và [PSR-4][psr4]. Các đề xuất này chỉ đơn thuần là một bộ quy tắc mà nhiều dự án như Drupal, Zend, Symfony, Laravel, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium, v.v. sử dụng. Bạn có thể sử dụng chúng cho các dự án của riêng bạn, hoặc tiếp tục sử dụng phong cách cá nhân của riêng bạn.

Tốt nhất, bạn nên viết mã PHP tuân thủ một tiêu chuẩn đã biết. Đây có thể là bất kỳ sự kết hợp nào của PSR hoặc một trong những tiêu chuẩn mã hóa được tạo bởi PEAR hoặc Zend. Điều này có nghĩa là các nhà phát triển khác có thể dễ dàng đọc và làm việc với mã của bạn và các ứng dụng triển khai các thành phần có thể có tính nhất quán ngay cả khi làm việc với nhiều mã của bên thứ ba.

* [Tìm hiểu thêm về PSR-1][psr1]
* [Tìm hiểu thêm về PSR-2][psr2]
* [Tìm hiểu thêm về PSR-4][psr4]
* [Tìm hiểu thêm về PEAR Coding Standards][pear-cs]
* [Tìm hiểu thêm về Symfony Coding Standards][symfony-cs]

Bạn có thể sử dụng [PHP_CodeSniffer][phpcs] để kiểm tra mã theo bất kỳ một trong những đề xuất này và các plugin cho trình soạn thảo văn bản như [Sublime Text][st-cs] để nhận được phản hồi theo thời gian thực.

Bạn có thể tự động sửa bố cục mã bằng cách sử dụng một trong các công cụ sau:

- [PHP Coding Standards Fixer][phpcsfixer] có một cơ sở mã được kiểm tra rất kỹ.
- [PHP Code Beautifier and Fixer][phpcbf] công cụ này đã bao gồm PHP_CodeSniffer và có thể được sử dụng để điều chỉnh mã của bạn cho phù hợp.

Và bạn có thể chạy phpc thủ công từ shell:

    phpcs -sw --standard=PSR2 file.php

Nó sẽ hiển thị lỗi và mô tả cách sửa chúng. Nó cũng có thể hữu ích khi bao gồm lệnh này trong một git hook. Theo cách đó, các nhánh chứa vi phạm theo tiêu chuẩn đã chọn không thể đưa vào kho lưu trữ cho đến khi các vi phạm đó được khắc phục.

Nếu bạn có PHP_CodeSniffer, thì bạn có thể tự động sửa các vấn đề về bố cục mã được báo cáo bởi [PHP Code Beautifier and Fixer][phpcbf].

    phpcbf -w --standard=PSR2 file.php

Một tùy chọn khác là sử dụng [PHP Coding Standards Fixer][phpcsfixer].
Nó sẽ chỉ ra loại lỗi nào mà cấu trúc mã có trước khi sửa chúng.

    php-cs-fixer fix -v --level=psr2 file.php

Tiếng Anh được ưu tiên cho tất cả các tên biểu tượng (symbol names) và cơ sở hạ tầng mã (code infrastructure). Comments có thể được viết bằng bất kỳ ngôn ngữ nào dễ đọc cho tất cả các bên hiện tại và tương lai, những người có thể sẽ và đang làm việc với codebase đó.

Cuối cùng, một tài nguyên bổ sung tốt để viết mã PHP sạch là [Clean Code PHP][cleancode].

[fig]: https://www.php-fig.org/
[psr1]: https://chungnguyen.xyz/posts/psr-1-chuan-viet-code-php-co-ban/
[psr2]: https://chungnguyen.xyz/posts/psr-2-chuan-trinh-bay-code-php-dep/
[psr4]: https://www.php-fig.org/psr/psr-4/
[pear-cs]: https://pear.php.net/manual/en/standards.php
[symfony-cs]: https://symfony.com/doc/current/contributing/code/standards.html
[phpcs]: https://pear.php.net/package/PHP_CodeSniffer/
[phpcbf]: https://github.com/squizlabs/PHP_CodeSniffer/wiki/Fixing-Errors-Automatically
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: https://cs.sensiolabs.org/
[cleancode]: https://github.com/nguyentranchung/clean-code-php
