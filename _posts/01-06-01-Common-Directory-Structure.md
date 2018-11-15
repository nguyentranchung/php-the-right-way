---
title:   Cấu trúc thư mục chung
isChild: true
anchor:  common_directory_structure
---

## Cấu trúc thư mục chung {#common_directory_structure_title}

Một câu hỏi phổ biến trong số những người bắt đầu với các chương trình viết cho web là "tôi đặt mấy thứ tôi viết ở đâu?" Qua nhiều năm, câu trả lời này luôn được cho là "ở `DocumentRoot`". Mặc dù câu trả lời này chưa trọn vẹn, nhưng đó là một nơi tuyệt vời để bắt đầu

Vì lý do bảo mật, các tệp cấu hình không được truy cập bởi khách truy cập của trang web; do đó, các public scripts được lưu giữ trong một thư mục public và các cấu hình riêng tư và dữ liệu cá nhân được giữ bên ngoài thư mục đó (DocumentRoot).

Đối với mỗi team, CMS hoặc trong một framework, cấu trúc thư mục chuẩn được sử dụng bởi các thành viên. Tuy nhiên, nếu ai đó bắt đầu dự án một mình, biết được cấu trúc hệ thống tập tin để sử dụng có thể gây khó khăn.

[Paul M. Jones] đã thực hiện một số nghiên cứu tuyệt vời về các thực hành phổ biến của hàng chục nghìn dự án github trong lĩnh vực PHP. Ông đã biên soạn một cấu trúc thư mục và tệp tiêu chuẩn có tên là [Standard PHP Package Skeleton] dựa trên cơ sở đã nghiên cứu. Trong cấu trúc thư mục này, `DocumentRoot` nên trỏ đến `public/`, unit tests phải ở trong thư mục `tests/`, và các gói thư viện thứ 3, phải cài đặt thông qua [composer], và đặt trong thư mục `vendor/`. Đối với các tệp và thư mục khác, tuân thủ [Standard PHP Package Skeleton] sẽ có ý nghĩa nhất đối với những người đóng góp của một dự án.

[Paul M. Jones]: https://twitter.com/pmjones
[Standard PHP Package Skeleton]: https://github.com/php-pds/skeleton
[Composer]: /#composer_and_packagist
