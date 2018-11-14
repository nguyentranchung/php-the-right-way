---
isChild: true
anchor:  mac_setup
---

## Thiết lập trên Mac {#mac_setup_title}

macOS được đóng gói sẵn với PHP nhưng nó thường là chậm hơn một chút so với bản phát hành ổn định mới nhất. Có nhiều cách để cài đặt phiên bản PHP mới nhất trên macOS.

### Cài đặt PHP thông qua Homebrew

[Homebrew] là một công cụ quản lý gói mạnh mẽ cho macOS, sẽ giúp bạn cài đặt PHP và các phần mở rộng dễ dàng. Homebrew core repository cung cấp "formulae" cho PHP 5.6, 7.0, 7.1, và 7.2. Cài đặt phiên bản mới nhất với câu lệnh:

```
brew install php@7.2
```

Bạn có thể chuyển đổi qua lại phiên bản Homebrew PHP bằng cách thay đổi biến `PATH`. Cách khác, bạn có thể dùng [brew-php-switcher][brew-php-switcher] để chuyển đồi phiên bản PHP một cách tự động.

### Cài đặt PHP thông qua Macports

[MacPorts] Project là một dự án mã nguồn mở để thiết kế một hệ thống dễ sử dụng cho biên dịch, cài đặt và nâng cấp ngay cả trên command-line, X11 hay Aqua dựa vào các phần mềm mã nguồn mở trên OS X.

MacPorts hỗ trợ các tệp nhị phân được biên dịch trước, vì vậy bạn không cần phải biên dịch lại mọi phụ thuộc từ tệp tarball nguồn, tiết kiệm thời gian của bạn nếu bạn không có bất kỳ gói nào được cài đặt trên hệ thống của mình.

Tại thời điểm này, bạn có thể cài `php54`, `php55`, `php56`, `php70` or `php71` sử dụng `port install` command, ví dụ nhé:

    sudo port install php56
    sudo port install php71

Và bạn có thể chạy `select` command để kích hoạt phiên bản PHP mong muốn:

    sudo port select --set php php71

### Cài đặt PHP thông qua phpbrew

[phpbrew] là công cụ có thể cài đặt và quản lý nhiều phiên bản PHP khác nhau, rất hữu ích nếu bạn có hai ứng dụng/project chạy trên hai phiên bản PHP khác nhau và bạn không sử dụng máy ảo.

### Cài đặt PHP thông qua Liip's binary installer

Một sự lựa chọn phổ biến khác là [php-osx.liip.ch], nó cung cấp một phương thức cài đặt cho PHP phiên bản 5.3 đến 7.3.
Nó không ghi đè lên phiên bản PHP mà Apple đã cài, mà cài đặt trên một thư mục khác (/usr/local/php5).

### Biên dịch từ Source

Một tùy chọn khác cung cấp cho bạn quyền kiểm soát phiên bản PHP bạn cài đặt, đó là [compile it yourself][mac-compile].
Trong trường hợp đó, hãy chắc chắn đã cài đặt [Xcode][xcode-gcc-substitution] hay thay thế Apple's ["Command Line Tools for XCode"] có thể tải về từ Apple's Mac Developer Center.

### All-in-One Installers

Các giải pháp được liệt kê ở trên chủ yếu là xử lý PHP, và không cung cấp những thứ như Apache, Nginx hay SQL server.
Giải pháp "All-in-one" ở đây là: [MAMP][mamp-downloads] và [XAMPP][xampp] sẽ cài đặt các phần mềm khác cho bạn và kết hợp tất cả chúng lại với nhau, dễ dàng cài đặt đi kèm với sự cân bằng và tính linh hoạt.

[Homebrew]: https://brew.sh/
[Homebrew PHP]: https://github.com/Homebrew/homebrew-php#installation
[MacPorts]: https://www.macports.org/install.php
[phpbrew]: https://github.com/phpbrew/phpbrew
[php-osx.liip.ch]: https://php-osx.liip.ch/
[mac-compile]: https://secure.php.net/install.macosx.compile
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
["Command Line Tools for XCode"]: https://developer.apple.com/downloads
[mamp-downloads]: https://www.mamp.info/en/downloads/
[xampp]: https://www.apachefriends.org/index.html
[brew-php-switcher]: https://github.com/philcook/brew-php-switcher
