# Consuming-APIs-in-Laravel

### Khám Phá Tương Lai Của Phân Tích API
API Insights không chỉ là một công cụ thông thường; nó là một bước ngoặt trong phân tích lược đồ API. Chúng tôi đi sâu vào ba khía cạnh quan trọng của API của bạn – Hiệu suất, Thiết kế và Bảo mật – mang đến những thông tin vô giá và đánh giá toàn diện.

#### 1. Bảo mật – Ưu Tiên Hàng Đầu
Các bài kiểm tra độc quyền của chúng tôi không chỉ dừng lại ở bề mặt mà còn giúp phát hiện những rủi ro bảo mật tiềm ẩn. Chúng tôi xác định các lỗ hổng như lộ khóa API, rủi ro tấn công ID tuần hoàn và IDOR. Với API Insights, bạn không chỉ có một công cụ giúp đảm bảo an toàn cho API mà còn bảo vệ dữ liệu mà nó xử lý.

#### 2. Hiệu Suất Vượt Trội
Một API hoạt động tốt sẽ mang lại trải nghiệm hài lòng cho người dùng. Chúng tôi đánh giá hiệu suất API của bạn bằng các kỹ thuật tiên tiến. Từ việc kiểm tra tiêu đề trong một yêu cầu GET duy nhất, đánh giá bộ nhớ đệm, sử dụng CDN, và hỗ trợ HTTP/2 hoặc HTTP/3, chúng tôi không bỏ sót bất kỳ chi tiết nào. Hãy kỳ vọng một API nhanh hơn và ổn định hơn nếu bạn áp dụng những đề xuất của chúng tôi.

#### 3. Thiết Kế Quan Trọng
Thiết kế tốt là cốt lõi của mọi API thành công. API Insights đánh giá mức độ đáp ứng nhu cầu của nhà phát triển và tính hiệu quả trong thiết kế API của bạn. Chúng tôi xem xét các yếu tố như xử lý mã lỗi, rủi ro lộ thông tin cá nhân (PII), tính nhất quán ngôn ngữ, cũng như mô tả tham số và endpoint.

Sẵn sàng cách mạng hóa trải nghiệm lược đồ API của bạn? Truy cập apiinsights.io ngay hôm nay để tận dụng tối đa công cụ miễn phí 100% này!

### Giới thiệu
Chào bạn!

Tôi là Ash Allen, một freelance Laravel web developer sống tại Vương Quốc Anh.

Trong năm năm qua, tôi đã làm việc trên nhiều dự án khác nhau, từ các website cho doanh nghiệp nhỏ địa phương đến các enterprise application quy mô lớn dành cho các công ty lớn.

Trong khoảng thời gian này, tôi may mắn được làm việc với những con người và công ty tuyệt vời, học hỏi được rất nhiều từ họ. Tôi cũng đã tham gia vào các dự án thú vị và quan sát cách các nhóm khác nhau giải quyết các vấn đề theo những cách khác nhau.

Nếu có một điều tôi nhận thấy trong suốt thời gian này, đó là hầu hết web application đều sẽ tích hợp với một external API vào một thời điểm nào đó. Dù chỉ đơn giản như gửi email hay phức tạp hơn như tích hợp với third-party payment gateway, việc tận dụng các hệ thống bên ngoài để xử lý công việc nặng giúp ích rất nhiều cho application của bạn. Điều này cho phép bạn tập trung vào các core feature của application và để các công ty bên thứ ba xử lý những thứ mà bạn không cần (và cũng không muốn) lo lắng. Ví dụ, thay vì tự xây dựng một hệ thống thanh toán cho web application của bạn, bạn có thể sử dụng Stripe để xử lý thanh toán. Điều này giúp bạn tập trung vào phát triển những tính năng thú vị hơn trong khi Stripe lo việc xử lý giao dịch thanh toán.

Tôi đã làm việc với rất nhiều API, bao gồm Stripe, Mailgun, Twilio, Marketo, Zapier, Twitter, Vonage, GitHub, và nhiều dịch vụ khác. Trong quá trình làm việc với những API này, tôi nhận thấy có những pattern và best practice chung mà tôi (hoặc nhóm của tôi) có thể áp dụng. Tôi cũng đã thấy những sai lầm và thiếu sót khiến chúng tôi gặp rắc rối sau này.

Trong cuốn sách này, chúng ta sẽ tìm hiểu về các kỹ thuật mà tôi đã học được, giúp bạn hiểu rõ hơn về cách tiêu thụ API trực tiếp từ Laravel application của mình.

Chúng ta sẽ bắt đầu với những khái niệm cơ bản về API, lợi ích mà chúng mang lại, các loại API khác nhau mà bạn có thể gặp phải và cách authenticate với chúng. Tiếp theo, chúng ta sẽ thảo luận về các kỹ thuật lập trình giúp việc làm việc với API trở nên dễ dàng hơn, bao gồm final class, readonly class & property, composition over inheritance, interface, data transfer object, và nhiều kỹ thuật khác.

Sau đó, chúng ta sẽ tìm hiểu cách tiêu thụ một API từ Laravel application bằng Saloon. Chúng ta sẽ thảo luận về các chủ đề như making request, OAuth2, caching response, error handling, và testing API integration.

Cuối cùng, chúng ta sẽ nói về webhook – chúng là gì, cách thiết lập và cách xử lý chúng một cách an toàn trong Laravel application của bạn.

Sau khi đọc xong cuốn sách này, bạn sẽ có một hiểu biết vững chắc về cách tiêu thụ API trực tiếp từ Laravel application của mình bằng cách sử dụng code có thể maintain, test và extend dễ dàng. Bạn cũng sẽ tự tin trong việc tích hợp với third-party API một cách an toàn và mạnh mẽ.

### Giới thiệu về API
Trước khi viết bất kỳ dòng code nào, chúng ta cần hiểu một số khái niệm về API. Chương này sẽ đề cập đến API là gì, các loại API mà bạn có thể gặp, cũng như những lợi ích và hạn chế của việc sử dụng API trong web application. Chúng ta cũng sẽ tìm hiểu về các định dạng dữ liệu phổ biến trong API, các phương thức authentication khác nhau, và best practice về bảo mật khi tích hợp API.

Sau khi hoàn thành chương này, bạn sẽ hiểu cách sử dụng API trong Laravel application của mình và có một nền tảng vững chắc để tiếp tục các phần còn lại của cuốn sách.
### API là gì?
Về cơ bản, API (Application Programming Interface) là một cách để các hệ thống giao tiếp với nhau. Chúng cho phép bạn tích hợp với các hệ thống và dịch vụ khác để cung cấp nhiều tính năng hơn cho người dùng.

API thường được sử dụng để gửi và nhận dữ liệu mà không cần biết chi tiết nội bộ của một hệ thống. Điều này giúp bạn có thể tập trung vào việc xây dựng core system, trong khi các tính năng chuyên biệt có thể được xử lý bởi những hệ thống khác.

Ví dụ, bạn có thể sử dụng third-party payment system như Stripe để xử lý thanh toán. Điều này có nghĩa là bạn không cần phải lo lắng về những vấn đề phức tạp như PCI (Payment Card Industry) compliance, vì Stripe sẽ chịu trách nhiệm lưu trữ thông tin thẻ.

Một ví dụ khác về việc sử dụng API trong application của bạn là sử dụng HubSpot để quản lý khách hàng. Bạn có thể sử dụng HubSpot API để tự động tạo một contact mới trong HubSpot khi người dùng đăng ký nhận bản tin hoặc điền vào biểu mẫu liên hệ trên website của bạn. Điều này giúp bạn quản lý dữ liệu khách hàng tập trung ở một nơi và dễ dàng hơn trong việc theo dõi.

Bạn cũng có thể sử dụng API như một phần của authentication và authorization trong application. Ví dụ, bạn có thể cho phép người dùng đăng nhập vào ứng dụng của mình bằng tài khoản Google. Để thực hiện điều này, bạn có thể sử dụng Google API để authenticate người dùng và lấy các thông tin của họ (chẳng hạn như tên, email, ảnh đại diện, v.v.). Bạn có thể đã từng thấy điều này khi đăng nhập vào một ứng dụng với các tùy chọn như "Sign in with Google" hoặc "Sign in with Facebook".

Dưới đây là sơ đồ mô tả high-level flow của việc gửi yêu cầu API đến một hệ thống bên ngoài và nhận phản hồi:

![image](https://github.com/user-attachments/assets/4fd0177d-3deb-4825-915f-c25886b15b51)

Tùy thuộc vào loại dự án Laravel mà bạn làm việc, có thể bạn đã từng tương tác với external APIs mà không nhận ra. Dưới đây là một số API phổ biến mà bạn có thể đã từng sử dụng và các use case của chúng:

Stripe – Xử lý thanh toán
Mailgun – Gửi email
Mailchimp – Tiếp thị qua email
Twilio – Gửi tin nhắn SMS
Vonage – Gửi tin nhắn SMS
Facebook – Lên lịch đăng bài trên mạng xã hội
Twitter – Đăng nhập bằng mạng xã hội
Instagram – Đăng nhập bằng mạng xã hội
Google – Đăng nhập bằng mạng xã hội và lưu trữ đám mây (Google Drive)
GitHub – Truy cập repositories và dữ liệu người dùng
AWS – Lưu trữ đám mây (S3)

Ngoài việc sử dụng API để giao tiếp với hệ thống bên ngoài, chúng cũng có thể được sử dụng để giao tiếp giữa các internal systems.

Ví dụ, giả sử bạn có một trang e-commerce được chia thành hai ứng dụng riêng biệt:

Website dành cho khách hàng để xem sản phẩm và đặt hàng.
Admin panel dành cho nhân viên quản lý kho và đơn hàng.
Admin panel có thể cần hiển thị một số thống kê từ website khách hàng. Để làm điều này, bạn có thể tạo một API trên website khách hàng để trả về dữ liệu thống kê. Sau đó, admin panel có thể gửi yêu cầu đến API này để lấy dữ liệu và hiển thị chúng.

Điều này có nghĩa là admin panel không cần biết cách website khách hàng hoạt động, nó chỉ cần biết cách gửi request đến API. Điều này giúp bạn giữ cho hai hệ thống tách biệt và dễ bảo trì hơn. Nếu bạn thay đổi cách hoạt động của website khách hàng, bạn không cần phải thay đổi admin panel vì nó chỉ tương tác với API.

Đây là một ví dụ điển hình về cách APIs có thể được sử dụng để giao tiếp giữa các internal systems trong khi vẫn ẩn đi logic nội bộ của từng hệ thống. Bạn cũng có thể giới hạn quyền truy cập của API website khách hàng bằng cách đặt nó ở chế độ private, chỉ cho phép admin panel gửi request.

Dưới đây là sơ đồ mô tả high-level flow của việc gửi yêu cầu API giữa hai hệ thống:

![image](https://github.com/user-attachments/assets/078cdcf8-138d-41ed-ac4b-f7f5c880592f)

### Định dạng dữ liệu: JSON vs. XML
Cuốn sách này sẽ tập trung vào việc tiêu thụ (consuming) các API sử dụng JSON làm request body và trả về JSON làm response body. Tuy nhiên, điều quan trọng là bạn cũng nên biết rằng có các định dạng dữ liệu khác có thể được sử dụng, chẳng hạn như XML.

Mặc dù hầu hết các API mà bạn làm việc trong Laravel đều sử dụng JSON, nhưng đôi khi bạn vẫn có thể cần phải làm việc với XML APIs.

Hãy cùng tìm hiểu sự khác biệt giữa JSON và XML, cũng như ưu nhược điểm của từng định dạng.
### JSON
JavaScript Object Notation (JSON) là một định dạng nhẹ được sử dụng để cấu trúc dữ liệu. Nhìn chung, nó dễ đọc và ghi trong PHP, vì vậy bạn sẽ thường xuyên bắt gặp nó.

Trong các ứng dụng Laravel, JSON thường được sử dụng cho các mục đích như:

API response bodies (dữ liệu phản hồi được gửi từ hoặc đến ứng dụng của bạn).
API request bodies (dữ liệu yêu cầu được gửi từ hoặc đến ứng dụng của bạn).
Lưu trữ các bản dịch trong ứng dụng (ví dụ: tệp resources/lang/en.json).
JSON hỗ trợ một số kiểu dữ liệu giới hạn, bao gồm:
✔ Strings (chuỗi)
✔ Numbers (số)
✔ Booleans (giá trị đúng/sai)
✔ Arrays (mảng)
✔ Objects (đối tượng)

Dưới đây là một ví dụ về JSON data sử dụng tất cả các kiểu dữ liệu trên:

![image](https://github.com/user-attachments/assets/f7a8de53-c94e-42bb-a1fa-104f8275c82a)

Hãy phân tích cấu trúc JSON ở trên:

Ở cấp cao nhất của object, các trường name, email, và phone đều là strings.
Trường approved là một boolean.
Trường age là một number.
Trường hobbies là một array chứa các strings.
Trường address là một object, bên trong chứa các trường street, city, state, và zip, tất cả đều là strings.

### Ưu điểm của JSON
Bây giờ chúng ta đã hiểu JSON là gì, hãy cùng xem xét một số lợi ích khi sử dụng JSON.

### Dễ đọc và dễ viết
Mặc dù các cấu trúc dữ liệu như JSON thường được đọc và ghi bằng chương trình, nhưng bạn cũng sẽ thường xuyên cần đọc chúng trực tiếp. Bạn có thể muốn kiểm tra cấu trúc của API response hoặc thêm một trường mới vào tệp cấu hình.
Với cú pháp đơn giản và định dạng dễ hiểu, JSON thường thân thiện với con người hơn so với các định dạng dữ liệu khác như XML, giúp bạn dễ dàng làm việc hơn.

### Kích thước request, response và file nhỏ hơn
Do JSON có định dạng nhẹ, nên kích thước request, response, và file thường nhỏ hơn so với các định dạng khác như XML.
Kích thước request và response có thể không quan trọng đối với các ứng dụng nhỏ, nhưng với các ứng dụng lớn xử lý nhiều lưu lượng truy cập, hiệu suất là điều cần lưu ý.
Giữ kích thước response nhỏ nhất có thể giúp giảm nguy cơ vượt quá giới hạn băng thông và cải thiện thời gian phản hồi.

### Hỗ trợ tự nhiên trong JavaScript
Một lợi ích lớn của JSON là nó được hỗ trợ tự nhiên trong JavaScript và có thể dễ dàng được parse.
Điều này giúp bạn truyền dữ liệu từ Laravel Blade views trực tiếp vào mã JavaScript hoặc thực hiện API request đến các dịch vụ bên ngoài từ tệp JavaScript một cách đơn giản.


