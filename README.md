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

### Phổ biến rộng rãi
JSON là một định dạng được sử dụng rộng rãi, vì vậy bạn sẽ thường xuyên bắt gặp nó. Nhờ đó, bạn có thể dễ dàng tìm thấy tài liệu và các ví dụ hướng dẫn cách làm việc với nó. Điều này giúp bạn nhanh chóng làm quen với định dạng này và sử dụng các API dựa trên JSON, vì cú pháp của nó rất quen thuộc.

### Nhược điểm của JSON
Mặc dù JSON là một định dạng tuyệt vời, nhưng nó cũng có một số nhược điểm mà bạn cần lưu ý.

### Không hỗ trợ comments
Khi JSON object trở nên lớn và phức tạp hơn, bạn có thể muốn thêm comments để giải thích mục đích của từng trường dữ liệu. Điều này đặc biệt quan trọng nếu bạn sử dụng JSON để định nghĩa tệp cấu hình (config file) cho ứng dụng của mình.

Tuy nhiên, JSON không hỗ trợ comments, vì vậy bạn không thể làm điều này. Điều này có thể khiến việc duy trì các tệp JSON trở nên khó khăn hơn khi chúng ngày càng lớn. Do đó, tùy vào trường hợp sử dụng, bạn có thể cân nhắc sử dụng định dạng khác như YAML hoặc PHP array thay vì JSON.

### Không thể xác thực theo schema
Không giống như XML, JSON không hỗ trợ khái niệm schema. Trong XML, bạn có thể định nghĩa một schema để chỉ định cấu trúc của tài liệu XML.

Điều này rất hữu ích để xác thực rằng tài liệu XML được định dạng đúng và chứa các trường cần thiết. Trong ngữ cảnh API, đây là một tính năng hữu ích vì bạn có thể xác thực request body trước khi gửi API request, đảm bảo rằng API sẽ chấp nhận nó vì cùng một schema cũng được sử dụng để kiểm tra cấu trúc request ở phía API.

Do JSON không có hỗ trợ schema một cách tự nhiên, nên sẽ không dễ dàng đảm bảo rằng dữ liệu của bạn có đúng cấu trúc hay không.

### XML
Extensible Markup Language (XML) là một định dạng dữ liệu khác có thể được sử dụng để cấu trúc dữ liệu. Trong các ứng dụng Laravel, bạn có thể đã gặp các tệp XML, chẳng hạn như tệp phpunit.xml được sử dụng để cấu hình PHPUnit trong thư mục gốc của dự án.

Cấu trúc và cách viết của XML khá giống với HTML, vì vậy khi làm việc với các object đơn giản, nó có thể mang lại cảm giác quen thuộc. Tuy nhiên, do tính chất verboseness (dài dòng), XML đôi khi trở nên khó đọc và viết hơn khi cấu trúc dữ liệu trở nên phức tạp.

Hãy cùng xem cách chúng ta có thể biểu diễn cấu trúc JSON trước đó dưới dạng XML:

![image](https://github.com/user-attachments/assets/067b22e9-460e-4036-9af7-0dd66086701d)

Trong object XML ở trên, cấu trúc tương đối dễ đọc.
Ngoài ra, chúng ta cũng có thể thêm attributes vào các XML elements để cung cấp thông tin bổ sung.

Ví dụ, thay vì sử dụng element <approved>, chúng ta có thể chuyển nó thành một attribute trong element <person> như sau:

![image](https://github.com/user-attachments/assets/399ccd7c-4fe6-4320-bed8-cb547cd9fa00)

### Ưu điểm của XML
Bây giờ chúng ta đã hiểu XML là gì, hãy cùng xem một số lợi ích khi sử dụng XML.

### Tự mô tả (Self Describing)
Do tính chất dài dòng của XML, một tài liệu XML có cấu trúc tốt thường dễ hiểu. Điều này là do tags và attributes trong XML giúp mô tả rõ ràng nội dung của tài liệu.

### Có thể được xác thực dựa trên Schema
XML cho phép xác định schema cho một tài liệu. Điều này giúp đảm bảo cấu trúc của tài liệu đúng như mong đợi và có thể được sử dụng như một phần của quá trình kiểm tra tính hợp lệ để đảm bảo tài liệu chứa các fields và attributes cần thiết.

Ví dụ, giả sử chúng ta muốn kiểm tra rằng một object <person> phải chứa các field <name>, <email>, và <age>. Chúng ta có thể định nghĩa schema cho đối tượng này như sau:

![image](https://github.com/user-attachments/assets/3edb1148-6027-4181-ae03-b66dfa182495)

Để đảm bảo đối tượng hợp lệ, chúng ta có thể định nghĩa một schema cho XML.
Có một số định dạng có thể được sử dụng để xác định schema của XML, nhưng phổ biến nhất là XML Schema Definition (XSD).

Trong ví dụ của chúng ta, một XSD có thể trông như thế này:

![image](https://github.com/user-attachments/assets/fecd084c-6928-4936-a7ed-566f90eb37ce)

Như bạn có thể thấy trong schema ở trên, chúng ta đã định nghĩa rằng trường <age> phải là một integer.
Do đó, nếu chúng ta tạo một đối tượng <person> với một giá trị kiểu string cho trường <age>, schema sẽ không hợp lệ và đối tượng sẽ bị coi là không hợp lệ.

Schema XML có thể được sử dụng để xác thực đối tượng một cách lập trình trước khi sử dụng nó. Ví dụ:

Bạn có thể xác thực tài liệu XML trước khi gửi nó làm request body đến một external API.
Hoặc API có thể muốn xác thực tài liệu XML khi nhận được nó trước khi xử lý.
Tương tự, nếu bạn đang tạo tài liệu XML theo cách thủ công (chẳng hạn như trong một config file), môi trường phát triển tích hợp (IDE) của bạn có thể xác thực đối tượng dựa trên schema và hiển thị thông báo lỗi nếu đối tượng không khớp với schema.

Để thực hiện điều này, chúng ta có thể cập nhật tài liệu XML như sau (giả sử tệp schema nằm tại https://example.com/my-person-schema.xsd):

![image](https://github.com/user-attachments/assets/ea8d885f-5837-467a-b72d-fe32cb8f1a3b)

### Hỗ trợ nhận xét (comments)
Một lợi thế của XML so với JSON là nó hỗ trợ comments (nhận xét).
Điều này có thể hữu ích khi bạn muốn cung cấp thông tin bổ sung về cấu trúc hoặc nội dung của tài liệu.

Comments trong XML được định nghĩa theo cách tương tự như trong HTML.
Ví dụ, hãy thêm một comment vào tài liệu XML ở trên:

![image](https://github.com/user-attachments/assets/60956841-415d-41c8-8620-c24fd4ebcb48)

### Nhược điểm của XML
Mặc dù XML có một số ưu điểm, nhưng nó cũng có một số nhược điểm mà bạn cần lưu ý.

### Dài dòng (Verbose)
Do tính chất dài dòng của XML và việc hỗ trợ cả elements và attributes,
các tài liệu XML có thể trở nên khó đọc khi chúng ngày càng phức tạp và lớn hơn.

### Khó phân tích cú pháp hơn trong PHP và JavaScript
So với JSON, XML có thể khó phân tích cú pháp hơn trong PHP và JavaScript.
Mặc dù cả hai ngôn ngữ này đều có thể đọc tài liệu XML, nhưng nó không đơn giản
như việc sử dụng json_encode() hoặc json_decode() trong PHP khi làm việc với JSON.
Do đó, việc xử lý tài liệu XML có thể làm tăng độ phức tạp của mã nguồn.

### Cấu trúc thông điệp HTTP
Trong suốt cuốn sách này, chúng ta sẽ xem xét nhiều ví dụ về thông điệp HTTP
được gửi dưới dạng yêu cầu (request) và phản hồi (response) của API.
Các ví dụ này sẽ tuân theo một cấu trúc chuẩn hóa để giúp bạn hiểu về các phần khác nhau của thông điệp.

Để làm quen với cấu trúc này, hãy cùng xem một ví dụ về yêu cầu API và phản hồi API.

### Ví dụ về thông điệp yêu cầu HTTP
Giả sử chúng ta muốn gửi một yêu cầu đến một API endpoint để tạo mới một người dùng.
Để thực hiện việc này, chúng ta cần gửi một yêu cầu POST đến endpoint /users.
Chúng ta cũng cần bao gồm một Authentication header, chứa API key để xác thực yêu cầu.

Ngoài ra, chúng ta cần gửi thêm Content-Type và Accept headers để báo cho API biết rằng:

Chúng ta đang gửi dữ liệu trong định dạng JSON.
Chúng ta muốn nhận phản hồi từ API cũng ở định dạng JSON.
Thông điệp HTTP request có thể trông như sau:

![image](https://github.com/user-attachments/assets/cec291aa-9555-4310-849b-a5ca74648802)

Thông điệp trên có thể được chia thành ba phần riêng biệt:

Start line (Dòng bắt đầu)
Headers (Tiêu đề HTTP)
Body (Nội dung yêu cầu)
Phần start line và headers được tách biệt với body bằng một dòng trống.

1. Start line (Dòng bắt đầu)
Dòng đầu tiên của thông điệp:
```plaintext
POST /users HTTP/3
```
Dòng này chỉ định rằng chúng ta muốn gửi một yêu cầu POST bằng giao thức HTTP/3
đến endpoint /users.

2. Headers (Tiêu đề HTTP)
Sau start line, chúng ta có phần headers, chứa các thông tin bổ sung về yêu cầu.
Headers có thể bao gồm phương thức HTTP, URL, chi tiết xác thực, v.v.

Ví dụ về headers:

```plaintext
Host: example.com
Content-Type: application/json
Accept: application/json
```
Trong ví dụ trên:

Host: example.com → Xác định máy chủ nơi gửi yêu cầu.
Điều này có nghĩa là yêu cầu sẽ được gửi đến https://example.com/users.
Content-Type: application/json → Cho biết body của yêu cầu sẽ được gửi dưới định dạng JSON.
Accept: application/json → Cho biết chúng ta muốn nhận phản hồi dưới định dạng JSON.
3. Body (Nội dung yêu cầu)
Phần cuối cùng của thông điệp chính là body, chứa dữ liệu mà chúng ta muốn gửi.
```json
{
  "name": "John Smith",
  "email": "john@example.com",
  "password": "secret"
}
```
Phần thân yêu cầu được định dạng dưới dạng JSON và chứa dữ liệu mà chúng ta muốn gửi đến API. Trong trường hợp này, chúng ta đang gửi tên, email và mật khẩu của người dùng mà chúng ta muốn tạo.

### Ví dụ về phản hồi HTTP
Tiếp tục với ví dụ tạo người dùng thông qua yêu cầu API, bây giờ chúng ta hãy xem phản hồi HTTP mà chúng ta có thể nhận được từ API.

Thông điệp HTTP phản hồi có thể trông như sau:

```plaintext
HTTP/3 201 Created
Content-Type: application/json
{
 "id": 1,
 "name": "John Smith",
 "email": "john@example.com"
}
```
Bạn có thể nhận thấy rằng cấu trúc của phản hồi rất giống với cấu trúc của yêu cầu, vì nó cũng bao gồm một dòng bắt đầu, phần header và phần thân.

Dòng bắt đầu và phần header của phản hồi tạo thành phần đầu tiên của thông điệp:

```plaintext
HTTP/3 201 Created  
Content-Type: application/json 
``` 
Chúng ta có thể thấy rằng phản hồi được trả về sử dụng giao thức HTTP phiên bản 3 và phần thân phản hồi có định dạng JSON.

Phản hồi cũng chứa mã trạng thái 201 Created, cho biết rằng yêu cầu đã thành công và một tài nguyên mới đã được tạo.

Phần thân của phản hồi là phần thứ hai của thông điệp:
```json
{
 "id": 1,
 "name": "John Smith",
 "email": "john@example.com"
}
```

Phần thân của phản hồi sau đó chứa một số thông tin về người dùng vừa được tạo. Tùy thuộc vào API mà bạn đang tương tác, phản hồi này có thể chứa nhiều thông tin hơn về người dùng mới. Mặt khác, một số API có thể chỉ trả về ID của tài nguyên vừa được tạo.

Bây giờ, chúng ta hãy nhanh chóng xem qua một số thông điệp phản hồi HTTP phổ biến khác mà bạn có thể gặp khi làm việc với API.

Bạn có thể thường xuyên bắt gặp phản hồi HTTP 404 Not Found, cho biết rằng tài nguyên bạn đang cố gắng truy cập không tồn tại:

```plaintext
HTTP/3 404 Not Found
Content-Type: application/json
{
 "status": 404,
 "error": "Not Found",
 "message": "The requested resource could not be found on this
server."
}
```
Một phản hồi phổ biến khác mà bạn có thể gặp phải là HTTP 401 Unauthorized, thường cho biết rằng khóa API của bạn không hợp lệ:

![image](https://github.com/user-attachments/assets/713e7bb9-cb07-4ec2-ae11-14050341f3a9)

Một phản hồi phổ biến khác mà bạn có thể gặp phải là HTTP 422 Unprocessable Entity, thường cho biết rằng phần thân yêu cầu chứa dữ liệu không hợp lệ. Bạn có thể bắt gặp phản hồi này khi cố gắng tạo hoặc cập nhật một tài nguyên thông qua yêu cầu API:

![image](https://github.com/user-attachments/assets/2dfd0dec-9386-4767-9e07-b714f49ee6a9)

Bây giờ, sau khi chúng ta đã tìm hiểu sơ lược về cấu trúc của các thông điệp HTTP, điều này sẽ giúp bạn hiểu rõ hơn về các ví dụ mà chúng ta sẽ xem xét trong suốt phần còn lại của cuốn sách.

### Các loại Web API
Cuốn sách này tập trung vào REST API sử dụng JSON, vì đây có lẽ là loại API phổ biến nhất mà bạn sẽ gặp khi xây dựng ứng dụng Laravel. Tuy nhiên, điều quan trọng là bạn cũng nên biết về các loại API khác (chẳng hạn như GraphQL, RPC và SOAP) mà bạn có thể gặp phải và cách chúng được sử dụng.

Thông thường, bạn sẽ làm việc với REST API trong ứng dụng của mình bằng JSON, nhưng đôi khi bạn cũng có thể cần sử dụng các loại API khác. Vì lý do này, chúng ta sẽ đi sâu vào REST API nhiều hơn so với các loại khác, nhưng vẫn sẽ điểm qua nhanh về chúng.

### REST API
REST (Representational State Transfer) API là loại API mà bạn thường gặp khi xây dựng ứng dụng Laravel. REST là một phong cách kiến trúc để xây dựng API và cung cấp một tập hợp các ràng buộc (có thể coi như các nguyên tắc hoặc quy tắc) mà các nhà phát triển có thể tuân theo.

Thông thường, bạn giao tiếp với REST API thông qua giao thức Hypertext Transfer Protocol Secure (HTTPS). Điều này có nghĩa là bạn có thể sử dụng các phương thức HTTP (chẳng hạn như GET, POST, PUT, PATCH và DELETE) để thực hiện các thao tác tạo, đọc, cập nhật và xóa (CRUD) trên các tài nguyên.

REST API có thể sử dụng XML hoặc JSON để gửi và nhận dữ liệu, nhưng JSON là định dạng phổ biến hơn.

Các ràng buộc của REST khuyến khích một cách tiếp cận đơn giản và tiêu chuẩn hóa trong giao tiếp API, giúp các nhà phát triển dễ dàng hiểu và sử dụng API hơn. Hãy cùng xem xét các ràng buộc mà REST API tuân theo:

### 1. Ràng buộc Client-Server
Kiến trúc REST được xây dựng dựa trên mô hình client-server (máy khách-máy chủ).

Client (Máy khách): Là ứng dụng hoặc thiết bị tiêu thụ API. Máy khách thường chịu trách nhiệm xử lý giao diện người dùng và đầu vào của người dùng.
Server (Máy chủ): Là ứng dụng hoặc thiết bị cung cấp API. Máy chủ thường chịu trách nhiệm chấp nhận các yêu cầu API, xử lý logic nghiệp vụ và gửi phản hồi lại cho máy khách.
Ràng buộc này có nghĩa là client (máy khách) và server (máy chủ) có thể tồn tại độc lập, và sự tách biệt này cho phép mỗi bên được cập nhật mà không ảnh hưởng đến bên còn lại.

### 2. Ràng buộc Stateless (Không trạng thái)
Kiến trúc REST quy định rằng tất cả các yêu cầu gửi đến API phải không có trạng thái (stateless). Điều này có nghĩa là máy chủ không nên lưu trữ bất kỳ trạng thái nào của yêu cầu, và mỗi yêu cầu phải độc lập với các yêu cầu trước đó.

Do đó, một REST API không nên sử dụng các cơ chế như cookie, session hoặc tham số URL để lưu trạng thái.

Thay vào đó, máy khách cần gửi đầy đủ mọi thông tin mà máy chủ cần để xử lý yêu cầu trong chính yêu cầu đó.

Cách tiếp cận này giúp tách biệt giữa client và server, giúp API dễ dàng mở rộng (scalability) vì máy chủ không cần quản lý trạng thái giữa các yêu cầu.

### 3. Ràng buộc Cacheable (Có thể lưu vào bộ nhớ đệm)
Kiến trúc REST yêu cầu rằng client phải có khả năng lưu vào bộ nhớ đệm (cache) các phản hồi mà máy chủ gửi đi. Vì vậy, phản hồi từ máy chủ phải bao gồm thông tin cho biết liệu phản hồi có thể được cache không và nếu có thì trong bao lâu.

Việc cho phép client cache phản hồi có thể giúp:
✅ Giảm số lượng yêu cầu API mà client cần gửi.
✅ Cải thiện hiệu suất ứng dụng của client.
✅ Giảm tải cho máy chủ.

Điều này đặc biệt hữu ích khi có một số lượng lớn client sử dụng API.

Ví dụ, giả sử bạn đang gửi yêu cầu đến một API để lấy thông tin tỷ giá hối đoái giữa hai loại tiền tệ tại một ngày cụ thể. Bạn có thể muốn lưu trữ phản hồi này vào bộ nhớ cache để không cần phải gửi lại yêu cầu trong tương lai (vì tỷ giá hối đoái của một ngày cụ thể sẽ không thay đổi).

Điều này có nghĩa là các yêu cầu trong tương lai cho cùng một ngày có thể được phục vụ từ bộ nhớ cache hoặc các hệ thống lưu trữ như Redis hoặc cơ sở dữ liệu, thay vì gửi một yêu cầu mới đến API.

### 4. Ràng buộc Giao diện Đồng nhất (Uniform Interface)
Kiến trúc REST quy định rằng API phải có một giao diện đồng nhất (uniform interface). Điều này có nghĩa là API cần có một cách giao tiếp chuẩn hóa, giúp các lập trình viên dễ dàng hiểu và sử dụng API.

Ràng buộc này được chia thành bốn ràng buộc nhỏ:

### 4.1. Xác định tài nguyên trong yêu cầu (Resource Identification in Requests)
Ràng buộc này quy định rằng mỗi tài nguyên phải có thể được xác định trong yêu cầu. Nói cách khác, yêu cầu phải chỉ rõ tài nguyên cần tương tác, thường thông qua một resource identifier (định danh tài nguyên) trong URI.

Ví dụ:
✅ Nếu bạn muốn lấy danh sách tất cả người dùng, bạn có thể gửi một yêu cầu GET đến /users. URI này đại diện cho tài nguyên "users".
✅ Nếu bạn muốn lấy thông tin của một người dùng cụ thể có ID là 1, bạn có thể gửi yêu cầu GET đến /users/1. URI này đại diện cho tài nguyên "user" có ID 1.

### 4.2. Thao tác trên tài nguyên thông qua biểu diễn (Resource Manipulation Through Representations)
Ràng buộc này quy định rằng client có thể thao tác (tạo, cập nhật, xóa) tài nguyên bằng cách gửi biểu diễn của tài nguyên đó trong nội dung yêu cầu (request body).

Biểu diễn này phải chứa tất cả thông tin mà máy chủ cần để thực hiện hành động trên tài nguyên.

Ví dụ:
✅ Nếu bạn muốn tạo một người dùng mới, bạn có thể gửi yêu cầu POST đến /users. URI này đại diện cho tài nguyên "users", còn phần request body sẽ chứa thông tin của người dùng cần tạo.

Giả sử request body ở định dạng JSON, một ví dụ đơn giản có thể như sau:
{
  "name": "John Smith",
  "email": "john@example.com",
  "password": "secret"
}
Điều này cho phép API nhận dữ liệu từ client, xử lý và lưu trữ tài nguyên mới trên máy chủ.
Ví dụ JSON và Cập nhật Người dùng
Ví dụ JSON trên chứa tất cả thông tin mà máy chủ cần để tạo một người dùng mới.
Tương tự, nếu chúng ta muốn cập nhật người dùng, ta có thể gửi một yêu cầu khác với biểu diễn mới của người dùng đến API.

### 4.3. Tin nhắn tự mô tả (Self-Descriptive Messages)
Ràng buộc này quy định rằng API phải sử dụng các tin nhắn có khả năng tự mô tả (self-descriptive messages) cho cả yêu cầu (request) và phản hồi (response).
Điều này có nghĩa là tất cả thông tin cần thiết để máy chủ và client hiểu được yêu cầu hoặc phản hồi phải được bao gồm trong chính yêu cầu hoặc phản hồi đó, mà không cần dựa vào các nguồn thông tin bên ngoài.

Các phương thức HTTP và ý nghĩa
Các phương thức HTTP khác nhau giúp xác định hành động của yêu cầu đối với tài nguyên, làm cho tin nhắn trở nên tự mô tả.
Dưới đây là một số phương thức HTTP phổ biến:

✅ GET – Lấy một tài nguyên.

Thường là thao tác chỉ đọc (read-only) và không làm thay đổi trạng thái tài nguyên.
✅ POST – Tạo một tài nguyên mới.

Không idempotent, có nghĩa là gửi cùng một yêu cầu nhiều lần có thể tạo ra nhiều tài nguyên giống nhau.
✅ PUT – Cập nhật tài nguyên hiện có hoặc tạo một tài nguyên mới nếu nó chưa tồn tại.

Idempotent, có nghĩa là gửi cùng một yêu cầu nhiều lần chỉ tạo hoặc cập nhật một tài nguyên duy nhất.

Các phương thức HTTP khác
✅ DELETE – Xóa một tài nguyên hiện có.

Tương tự như PUT, DELETE là idempotent, có nghĩa là tài nguyên sẽ vẫn bị xóa dù yêu cầu được gửi nhiều lần.
✅ PATCH – Cập nhật một tài nguyên hiện có (thường chỉ cập nhật một phần của tài nguyên).

Không idempotent, tức là gửi cùng một yêu cầu nhiều lần có thể dẫn đến nhiều thay đổi trên tài nguyên.
Các phương thức HTTP khác ít phổ biến hơn
✅ HEAD – Lấy thông tin tiêu đề (header) của tài nguyên.

Tương tự như GET, nhưng không trả về nội dung của phản hồi.
Hữu ích khi lấy thông tin metadata về tài nguyên mà không cần tải toàn bộ dữ liệu.
Có thể được sử dụng để kiểm tra xem một tài nguyên có tồn tại hay không.
✅ OPTIONS – Lấy thông tin về các phương thức HTTP được hỗ trợ cho tài nguyên.

Hữu ích khi xác định những phương thức HTTP nào có thể sử dụng với một tài nguyên cụ thể.
Headers trong HTTP Request & Response
Ngoài việc sử dụng phương thức HTTP để xác định hành động, các headers trong request có thể cung cấp thông tin bổ sung mà máy chủ có thể sử dụng.
Ví dụ:

🔹 Request Headers

Chứa tokens xác thực (authentication tokens).
🔹 Response Headers

Có thể chứa thông tin về giới hạn tốc độ (rate limiting), kiểu dữ liệu của payload, và thông tin về caching.
Content-Type Header & Accept Header
✅ Content-Type Header

Được gửi trong request hoặc response để xác định định dạng của dữ liệu trong body.
Ví dụ:
Nếu request body ở dạng JSON, header sẽ là:
```plaintext
Content-Type: application/json
```
Nếu request body ở dạng XML, header sẽ là:
```plaintext
Content-Type: application/xml
```
Điều này giúp máy chủ biết cách phân tích nội dung của request body.
✅ Accept Header

Được gửi bởi client để yêu cầu một định dạng phản hồi cụ thể.
Ví dụ:
Nếu client muốn phản hồi ở dạng JSON, header sẽ là:
```plaintext
Accept: application/json
```
Nếu client muốn phản hồi ở dạng XML, header sẽ là:
```plaintext
Accept: application/xml
```
Điều này giúp client biết cách xử lý dữ liệu trong response body.

Mã Trạng Thái HTTP
Để hỗ trợ client tốt hơn, API có thể sử dụng mã trạng thái HTTP để thông báo về kết quả của yêu cầu.

Ví dụ:

Nếu yêu cầu thành công, API có thể trả về mã trạng thái 200 OK.
Nếu không tìm thấy tài nguyên, API có thể trả về mã trạng thái 404 Not Found.
Dưới đây là một số mã trạng thái HTTP phổ biến:

Mã Thành Công (2xx)
✅ Chỉ ra rằng yêu cầu đã được nhận, hiểu và chấp nhận.

Mã trạng thái	Ý nghĩa
200 OK	Yêu cầu thành công.
201 Created	Tài nguyên mới đã được tạo.
202 Accepted	Yêu cầu đã được chấp nhận, nhưng chưa xử lý xong (ví dụ: hành động được đưa vào hàng đợi).
204 No Content	Yêu cầu thành công nhưng không có nội dung phản hồi.
Mã Lỗi Từ Phía Client (4xx)
✅ Cho biết rằng yêu cầu không thành công do lỗi từ phía client.

Mã trạng thái	Ý nghĩa
400 Bad Request	Yêu cầu không hợp lệ (ví dụ: URL sai, thiếu headers, v.v.).
401 Unauthorized	Client chưa xác thực (thiếu hoặc sai token đăng nhập).
403 Forbidden	Client không có quyền truy cập tài nguyên này.
404 Not Found	Không tìm thấy tài nguyên.
405 Method Not Allowed	Phương thức HTTP (GET, POST, v.v.) không được hỗ trợ trên tài nguyên này.
422 Unprocessable Entity	Dữ liệu trong request body không hợp lệ (ví dụ: dữ liệu không hợp lệ khi tạo/cập nhật tài nguyên).
Mã Lỗi Từ Phía Server (5xx)
✅ Cho biết rằng có lỗi xảy ra từ phía server.

Mã trạng thái	Ý nghĩa
500 Internal Server Error	Lỗi trên server khiến yêu cầu không thể xử lý.
Các mã trạng thái HTTP này giúp client dễ dàng xác định trạng thái của yêu cầu và xử lý phản hồi phù hợp.

Do sử dụng payload, phương thức HTTP, headers, và mã trạng thái, các yêu cầu và phản hồi có thể tự mô tả (self-descriptive) và chứa tất cả thông tin cần thiết để server và client hiểu chúng mà không cần tham chiếu đến bất kỳ thông tin bên ngoài nào.

Những nguyên tắc này giúp API tuân thủ "Ràng buộc Không Trạng thái" (Stateless Constraint) bằng cách loại bỏ sự cần thiết phải dựa vào thông tin bên ngoài để hiểu yêu cầu hoặc phản hồi.

Ví dụ về yêu cầu tự mô tả
Để làm rõ hơn, hãy tham khảo lại ví dụ từ phần "Cấu trúc thông điệp HTTP" (HTTP Message Structure).
Giả sử ta gửi một yêu cầu để tạo người dùng mới – đây là một ví dụ về một yêu cầu tự mô tả.

Yêu cầu gửi đi:
```plaintext
POST /users HTTP/3
Host: example.com
Content-Type: application/json
Accept: application/json

{
    "name": "John Smith",
    "email": "john@example.com",
    "password": "secret"
}
```
✅ Giải thích:

POST: Gửi yêu cầu tạo người dùng mới đến URI /users trên **example.com`.
HTTP/3: Sử dụng phiên bản HTTP 3.
Content-Type: application/json: Định dạng JSON cho dữ liệu gửi đi.
Accept: application/json: Yêu cầu phản hồi cũng ở định dạng JSON.
Payload: Chứa thông tin người dùng mới cần tạo (tên, email, mật khẩu).
Yêu cầu này chứa tất cả thông tin cần thiết để server có thể xử lý mà không cần tham chiếu đến dữ liệu bên ngoài.

Phản hồi từ server:
Giả sử yêu cầu thành công và server đã tạo người dùng mới, phản hồi có thể như sau:
```plaintext
HTTP/3 201 Created
Content-Type: application/json

{
    "id": 1,
    "name": "John Smith",
    "email": "john@example.com"
}
```
✅ Giải thích:

201 Created: Xác nhận tài nguyên (người dùng) đã được tạo thành công.
Content-Type: application/json: Định dạng phản hồi là JSON.
Payload: Server trả về thông tin của người dùng mới vừa được tạo, bao gồm id, name, và email (mật khẩu không được hiển thị vì lý do bảo mật).
Trong ví dụ trên, ta có thể thấy phản hồi được trả về bằng giao thức HTTP phiên bản 3, với body phản hồi ở định dạng JSON.
Phản hồi cũng chứa mã trạng thái 201 Created, cho biết rằng yêu cầu đã thành công và tài nguyên mới đã được tạo.
Nội dung phản hồi chứa thông tin về người dùng mới được tạo.

### 4.4. Hypermedia as the Engine of Application State (HATEOAS)
Một ràng buộc khác trong kiến trúc REST là "Hypermedia as the Engine of Application State" (HATEOAS).
Ràng buộc này quy định rằng API phải cung cấp các liên kết đến tài nguyên liên quan trong phản hồi.

Điều này cho phép client điều hướng API mà không cần biết trước URL của các tài nguyên liên quan.
Ví dụ, nếu ta muốn lấy danh sách bài viết trên blog của một người dùng, ta cần truy vấn API để lấy thông tin người dùng trước, sau đó mới gửi yêu cầu khác để lấy danh sách bài viết.

Trong một API REST thông thường, điều này thường yêu cầu hai yêu cầu riêng biệt:

Lấy thông tin người dùng.
Tìm URL của bài viết blog và gửi yêu cầu thứ hai để lấy danh sách bài viết.
Nếu API không tuân thủ HATEOAS, phản hồi từ yêu cầu đầu tiên có thể trông như sau:

```plaintext
{
    "id": 1,
    "name": "John Smith",
    "email": "john@example.com"
}
```
Như ta thấy, phản hồi này chỉ chứa thông tin người dùng, không có đường dẫn đến danh sách bài viết.
Nếu ta muốn lấy danh sách bài viết blog của người dùng này, ta phải tự tìm URL của tài nguyên (ví dụ như users/1/posts) từ tài liệu API rồi tạo thủ công URL trong mã nguồn.

API có hỗ trợ HATEOAS
Nếu API tuân thủ HATEOAS, phản hồi từ yêu cầu đầu tiên có thể như sau:

```plaintext
{
    "id": 1,
    "name": "John Smith",
    "email": "john@example.com",
    "links": [
        {
            "rel": "posts",
            "href": "/users/1/posts"
        }
    ]
}
```
✅ Điểm khác biệt quan trọng:

Phản hồi chứa trường links, trong đó:
rel (relationship) chỉ ra rằng đây là liên kết đến bài viết blog.
href chứa URL của tài nguyên bài viết (/users/1/posts).
Điều này giúp client dễ dàng điều hướng đến tài nguyên liên quan mà không cần tạo URL thủ công, giúp API dễ sử dụng và linh hoạt hơn.

Như ta có thể thấy trong phản hồi JSON, giờ đây đã có thuộc tính links, chứa một mảng các liên kết đến các tài nguyên liên quan.
Trong trường hợp này, ta có thể sử dụng thuộc tính rel của liên kết để xác định liên kết nào cần sử dụng để lấy danh sách bài viết blog của người dùng.
Nhờ vậy, khi gửi yêu cầu thứ hai để lấy danh sách bài viết, ta không cần biết trước URL mà có thể lấy URL một cách tự động từ phản hồi đầu tiên.

⚠ Lưu ý:
Không có một tiêu chuẩn bắt buộc nào để triển khai HATEOAS trong API.
Do đó, thuộc tính links có thể được đặt tên khác, chẳng hạn như related hoặc resources.
Tương tự, thuộc tính rel có thể có tên khác như type hoặc name.

Ngoài ra, thuộc tính links có thể không nằm trong phản hồi JSON, mà có thể được trả về trong phản hồi header.
Ví dụ, API có thể sử dụng header Link để cung cấp các liên kết đến các tài nguyên liên quan.




