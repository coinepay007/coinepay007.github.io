---
title: "Hướng dẫn Cloudflare: 10 tính năng quan trọng mà người mới bắt đầu nên biết"
slug: cloud
date: 2026-11-03
draft: false
---
# Hướng dẫn Cloudflare: 10 tính năng quan trọng mà người mới bắt đầu nên biết

## 1. Cloudflare là gì?

Cloudflare là một nền tảng cung cấp các dịch vụ mạng và bảo mật website, giúp cải thiện tốc độ truy cập, bảo vệ website khỏi các cuộc tấn công mạng và nâng cao độ ổn định khi người dùng truy cập.

Cloudflare cung cấp nhiều tính năng hữu ích, bao gồm quản lý DNS, CDN, chứng chỉ SSL/TLS, bộ nhớ đệm (Cache), chống tấn công DDoS, tường lửa ứng dụng web (WAF), chuyển hướng URL, phân tích lưu lượng truy cập, Workers và Pages.

Đối với người mới bắt đầu xây dựng website, Cloudflare là một công cụ đáng tìm hiểu. Nhiều tính năng cơ bản có thể được sử dụng miễn phí.

## 2. Cách đăng ký tài khoản Cloudflare và thêm website

Trước khi sử dụng các tính năng của Cloudflare, bạn cần tạo tài khoản và thêm tên miền của mình.

### Bước 1: Truy cập website chính thức

Mở trang web chính thức của Cloudflare:

[https://www.cloudflare.com/](https://www.cloudflare.com/)

Nhấn nút Sign Up để đăng ký tài khoản. Bạn có thể sử dụng địa chỉ email và mật khẩu để tạo tài khoản mới.

### Bước 2: Thêm tên miền

Sau khi đăng nhập, chọn Add a site hoặc Add a domain, sau đó nhập tên miền bạn muốn kết nối với Cloudflare.

Cloudflare sẽ quét các bản ghi DNS hiện có và hiển thị danh sách để bạn kiểm tra.

### Bước 3: Chọn gói dịch vụ

Cloudflare cung cấp nhiều gói dịch vụ khác nhau. Người mới bắt đầu có thể chọn gói Free để trải nghiệm những tính năng cơ bản.

### Bước 4: Thay đổi Nameservers

Cloudflare sẽ cung cấp cho bạn các địa chỉ Nameserver riêng.

Hãy đăng nhập vào trang quản lý tên miền của nhà cung cấp tên miền và thay thế Nameserver hiện tại bằng Nameserver do Cloudflare cung cấp.

Sau khi hoàn tất, hãy chờ DNS cập nhật. Thời gian cập nhật có thể khác nhau tùy nhà cung cấp và hệ thống DNS.

## 3. 10 tính năng Cloudflare quan trọng mà người mới nên biết

## Tính năng 1: Quản lý DNS

DNS là một trong những tính năng quan trọng nhất của Cloudflare.

Thông qua trang quản lý DNS, bạn có thể thêm, chỉnh sửa hoặc xóa các bản ghi như A, AAAA, CNAME, MX và TXT.

Ví dụ:

- A Record: Trỏ tên miền đến địa chỉ IPv4 của máy chủ.
- AAAA Record: Trỏ tên miền đến địa chỉ IPv6.
- CNAME Record: Tạo bí danh cho một tên miền khác.
- MX Record: Cấu hình máy chủ nhận email.
- TXT Record: Xác minh quyền sở hữu tên miền hoặc thiết lập các cấu hình liên quan.

### Phân biệt Proxied và DNS Only

Khi thêm bản ghi DNS, Cloudflare thường cung cấp hai chế độ:

**Proxied (đám mây màu cam):** Lưu lượng truy cập website được chuyển qua mạng proxy của Cloudflare. Chế độ này có thể hỗ trợ tăng tốc độ và bảo vệ website.

**DNS Only (đám mây màu xám):** Cloudflare chỉ cung cấp dịch vụ phân giải DNS, lưu lượng truy cập không đi qua proxy của Cloudflare.

Người mới nên hiểu rõ sự khác biệt giữa hai chế độ này trước khi thay đổi cấu hình DNS.

## Tính năng 2: CDN và tăng tốc website

CDN là mạng lưới phân phối nội dung, giúp người dùng truy cập tài nguyên website thông qua các máy chủ gần vị trí của họ hơn.

Cloudflare có mạng lưới máy chủ phân tán trên nhiều khu vực, giúp cải thiện tốc độ tải nội dung tĩnh như hình ảnh, CSS và JavaScript.

### Lợi ích của CDN

- Giảm thời gian tải tài nguyên website.
- Giảm số lượng yêu cầu trực tiếp đến máy chủ gốc.
- Cải thiện trải nghiệm truy cập cho người dùng ở nhiều quốc gia.
- Hỗ trợ giảm tải cho máy chủ gốc.

Để sử dụng tính năng này, bạn cần bật chế độ Proxied cho những bản ghi DNS phù hợp.

Lưu ý: CDN không đảm bảo mọi website đều tăng tốc như nhau. Hiệu quả còn phụ thuộc vào cấu hình website, vị trí máy chủ và loại nội dung được lưu vào bộ nhớ đệm.

## Tính năng 3: SSL/TLS và mã hóa HTTPS

SSL/TLS giúp mã hóa dữ liệu truyền giữa người dùng và website, đồng thời hỗ trợ bảo vệ thông tin trong quá trình kết nối.

Cloudflare cung cấp nhiều chế độ SSL/TLS khác nhau:

- Off: Không sử dụng mã hóa SSL/TLS.
- Flexible: Mã hóa kết nối giữa người dùng và Cloudflare, nhưng không mã hóa kết nối từ Cloudflare đến máy chủ gốc.
- Full: Mã hóa cả hai chặng kết nối, nhưng không yêu cầu chứng chỉ máy chủ gốc phải được xác minh đầy đủ.
- Full (strict): Mã hóa cả hai chặng và xác minh chứng chỉ SSL/TLS của máy chủ gốc.

### Nên chọn chế độ SSL/TLS nào?

Nếu máy chủ gốc đã cài đặt chứng chỉ SSL/TLS hợp lệ, thông thường nên sử dụng Full (strict).

Chế độ này giúp bảo vệ kết nối tốt hơn và tránh một số rủi ro liên quan đến chứng chỉ không hợp lệ.

Nếu gặp lỗi 525 hoặc 526, hãy kiểm tra chứng chỉ SSL/TLS trên máy chủ gốc, cấu hình HTTPS và khả năng kết nối giữa Cloudflare với máy chủ.

## Tính năng 4: Cache và quy tắc bộ nhớ đệm

Cache giúp lưu trữ tạm thời các tài nguyên website để giảm thời gian tải trong những lần truy cập tiếp theo.

Cloudflare có thể lưu các tài nguyên tĩnh như:

- Hình ảnh.
- Tệp CSS.
- Tệp JavaScript.
- Một số nội dung tĩnh khác.

### Cách xóa Cache

Nếu bạn vừa cập nhật website nhưng nội dung cũ vẫn xuất hiện, có thể cần xóa bộ nhớ đệm.

Các bước thực hiện:

1. Đăng nhập vào Cloudflare.
2. Chọn tên miền cần quản lý.
3. Mở mục Caching.
4. Chọn Purge Cache.
5. Chọn Purge Everything nếu muốn xóa toàn bộ Cache, hoặc sử dụng tùy chọn xóa theo URL nếu phù hợp.

### Lưu ý khi sử dụng Cache Rules

Không nên tùy tiện lưu Cache cho những trang chứa thông tin cá nhân hoặc dữ liệu động, chẳng hạn như:

- Trang đăng nhập.
- Trang giỏ hàng.
- Trang thanh toán.
- Trang quản lý tài khoản.
- Các trang hiển thị thông tin riêng tư của người dùng.

Cấu hình Cache không phù hợp có thể khiến người dùng nhìn thấy nội dung cũ hoặc nội dung không đúng với phiên truy cập của họ.

## Tính năng 5: Bảo vệ DDoS và bảo mật website

DDoS là hình thức tấn công sử dụng lượng lớn lưu lượng truy cập giả hoặc độc hại để làm quá tải máy chủ, khiến website hoạt động chậm hoặc không thể truy cập.

Cloudflare cung cấp các cơ chế bảo vệ DDoS nhằm phát hiện và giảm thiểu nhiều loại lưu lượng truy cập bất thường.

### Lợi ích của bảo vệ DDoS

- Hỗ trợ giảm thiểu lưu lượng tấn công.
- Giảm áp lực lên máy chủ gốc.
- Cải thiện khả năng duy trì hoạt động của website.
- Hỗ trợ bảo vệ website trước một số hình thức tấn công phổ biến.

Người quản trị có thể theo dõi các hoạt động bảo mật trong bảng điều khiển Cloudflare và điều chỉnh cấu hình phù hợp với nhu cầu của website.

## Tính năng 6: WAF – Tường lửa ứng dụng web

WAF (Web Application Firewall) là tường lửa ứng dụng web, giúp phát hiện và ngăn chặn một số yêu cầu HTTP độc hại trước khi chúng tiếp cận máy chủ gốc.

WAF có thể hỗ trợ bảo vệ website trước những hình thức tấn công phổ biến như:

- SQL Injection.
- Cross-Site Scripting (XSS).
- Một số yêu cầu HTTP bất thường.
- Các mẫu tấn công được xác định trong bộ quy tắc bảo mật.

### Managed Rules và Custom Rules

Cloudflare cung cấp các nhóm quy tắc bảo mật khác nhau:

**Managed Rules:** Các quy tắc được Cloudflare quản lý và cập nhật nhằm phát hiện những mẫu tấn công phổ biến.

**Custom Rules:** Cho phép người quản trị tự tạo quy tắc dựa trên IP, quốc gia, đường dẫn URL, loại yêu cầu hoặc các điều kiện khác.

Người mới nên bắt đầu với các quy tắc được quản lý sẵn, sau đó điều chỉnh khi đã hiểu rõ hoạt động của website.

Lưu ý: Nếu cấu hình quá nghiêm ngặt, WAF có thể chặn nhầm người dùng hợp lệ. Khi website gặp lỗi truy cập, hãy kiểm tra Security Events để tìm nguyên nhân.

## Tính năng 7: Redirect Rules – Chuyển hướng URL

Redirect Rules cho phép chuyển hướng người dùng từ một URL sang URL khác.

Ví dụ:

- Chuyển từ HTTP sang HTTPS.
- Chuyển từ tên miền cũ sang tên miền mới.
- Chuyển hướng một đường dẫn cũ đến đường dẫn mới.
- Chuẩn hóa URL để tránh các phiên bản trùng lặp.

### Phân biệt 301 và 302

**301 Redirect:** Chuyển hướng vĩnh viễn. Thường được sử dụng khi website thay đổi URL hoặc chuyển sang tên miền mới lâu dài.

**302 Redirect:** Chuyển hướng tạm thời. Phù hợp khi việc chuyển hướng chỉ diễn ra trong một khoảng thời gian.

Khi thiết lập Redirect Rules, hãy kiểm tra kỹ điều kiện và URL đích để tránh tạo vòng lặp chuyển hướng.

## Tính năng 8: Analytics – Phân tích lưu lượng truy cập

Cloudflare Analytics cung cấp thông tin về lưu lượng truy cập và hoạt động của website.

Bạn có thể theo dõi một số dữ liệu như:

- Số lượng yêu cầu truy cập.
- Lưu lượng dữ liệu truyền tải.
- Lưu lượng được Cloudflare xử lý.
- Các yêu cầu bị chặn bởi hệ thống bảo mật.
- Hoạt động của Cache.
- Một số thông tin về nguồn truy cập và khu vực địa lý.

### Cloudflare Analytics có thay thế Google Analytics không?

Không hoàn toàn.

Cloudflare Analytics chủ yếu cung cấp dữ liệu về lưu lượng mạng, yêu cầu HTTP, bảo mật và hiệu suất.

Trong khi đó, Google Analytics tập trung nhiều hơn vào hành vi người dùng, sự kiện, chuyển đổi và hoạt động trên website.

Hai công cụ có thể được sử dụng kết hợp để giúp người quản trị hiểu rõ hơn về hoạt động của website.

## Tính năng 9: Cloudflare Workers

Cloudflare Workers là nền tảng cho phép chạy mã JavaScript hoặc các ứng dụng tương thích tại mạng lưới Cloudflare mà không cần tự quản lý một máy chủ truyền thống.

Workers có thể được sử dụng cho nhiều mục đích như:

- Xử lý yêu cầu HTTP.
- Tạo API.
- Chuyển tiếp hoặc sửa đổi yêu cầu.
- Xử lý dữ liệu trước khi trả về cho người dùng.
- Xây dựng các chức năng phía máy chủ.

### Người mới có nên sử dụng Workers không?

Nếu bạn chỉ cần quản lý DNS, CDN và SSL/TLS thì chưa nhất thiết phải sử dụng Workers.

Tuy nhiên, nếu muốn xây dựng API, xử lý yêu cầu hoặc tạo các chức năng tùy chỉnh, đây là một công cụ rất đáng tìm hiểu.

Hãy kiểm tra giới hạn sử dụng và mức phí hiện hành của gói dịch vụ trước khi triển khai ứng dụng thực tế.

## Tính năng 10: Cloudflare Pages

Cloudflare Pages là nền tảng triển khai website, đặc biệt phù hợp với các website tĩnh và dự án frontend.

Bạn có thể kết nối kho mã nguồn GitHub để tự động triển khai website sau mỗi lần cập nhật mã nguồn.

### Các bước triển khai website bằng Cloudflare Pages

1. Đăng nhập vào bảng điều khiển Cloudflare.
2. Chọn Workers & Pages.
3. Tạo một dự án Pages mới.
4. Kết nối tài khoản GitHub.
5. Chọn kho mã nguồn cần triển khai.
6. Cấu hình Build command và Build output directory nếu dự án yêu cầu.
7. Bắt đầu triển khai và chờ quá trình hoàn tất.
8. Thêm tên miền tùy chỉnh nếu cần.

Sau khi triển khai thành công, Cloudflare Pages sẽ cung cấp một địa chỉ truy cập cho website.

Đây là lựa chọn phù hợp cho blog, trang giới thiệu sản phẩm, tài liệu trực tuyến và nhiều dự án frontend khác.

## 4. Cấu hình Cloudflare được khuyến nghị cho người mới

Nếu bạn vừa kết nối website với Cloudflare, có thể bắt đầu với những thiết lập cơ bản sau:

- Kiểm tra các bản ghi DNS để bảo đảm tên miền trỏ đúng máy chủ.
- Bật Proxied cho những bản ghi website phù hợp.
- Sử dụng HTTPS và cấu hình SSL/TLS phù hợp với chứng chỉ trên máy chủ gốc.
- Nếu máy chủ gốc có chứng chỉ hợp lệ, ưu tiên Full (strict).
- Bật các tính năng bảo mật phù hợp với nhu cầu.
- Thiết lập Cache Rules cẩn thận.
- Không lưu Cache cho trang đăng nhập, thanh toán và thông tin cá nhân.
- Theo dõi Analytics và Security Events để phát hiện vấn đề.

Không nên bật hoặc thay đổi quá nhiều tùy chọn cùng lúc. Hãy điều chỉnh từng phần và kiểm tra website sau mỗi lần thay đổi.

## 5. Các lỗi Cloudflare thường gặp và cách khắc phục

### Lỗi 1: Website không hoạt động sau khi kết nối Cloudflare

Nguyên nhân có thể bao gồm:

- Nameserver chưa cập nhật hoàn toàn.
- Bản ghi DNS cấu hình sai.
- Địa chỉ IP máy chủ gốc không chính xác.
- Máy chủ gốc không phản hồi.
- Cấu hình SSL/TLS không phù hợp.

Cách khắc phục:

1. Kiểm tra trạng thái tên miền trong Cloudflare.
2. Kiểm tra các bản ghi DNS.
3. Xác nhận địa chỉ IP máy chủ gốc.
4. Kiểm tra cấu hình SSL/TLS.
5. Kiểm tra xem máy chủ gốc có hoạt động bình thường hay không.

### Lỗi 2: Error 522 – Connection Timed Out

Lỗi 522 thường xuất hiện khi Cloudflare không nhận được phản hồi kịp thời từ máy chủ gốc.

Một số nguyên nhân phổ biến:

- Máy chủ gốc bị quá tải.
- Tường lửa chặn địa chỉ IP của Cloudflare.
- Máy chủ không phản hồi trong thời gian quy định.
- Kết nối mạng giữa Cloudflare và máy chủ gốc gặp sự cố.

Cách khắc phục:

- Kiểm tra trạng thái hoạt động của máy chủ.
- Kiểm tra cấu hình tường lửa.
- Cho phép các dải IP chính thức của Cloudflare nếu cần.
- Liên hệ nhà cung cấp hosting để kiểm tra kết nối máy chủ.

### Lỗi 3: Error 525 – SSL Handshake Failed

Lỗi 525 thường liên quan đến quá trình thiết lập kết nối SSL/TLS giữa Cloudflare và máy chủ gốc.

Bạn nên kiểm tra:

- Máy chủ gốc đã cài đặt chứng chỉ SSL/TLS hay chưa.
- Máy chủ có hỗ trợ kết nối HTTPS hay không.
- Chứng chỉ và cấu hình SSL trên máy chủ có hợp lệ không.
- Các cài đặt SSL/TLS trong Cloudflare có phù hợp không.

### Lỗi 4: Hình ảnh hoặc nội dung website vẫn hiển thị phiên bản cũ

Nguyên nhân thường là do nội dung cũ vẫn được lưu trong Cache.

Cách khắc phục:

1. Đăng nhập Cloudflare.
2. Chọn tên miền cần quản lý.
3. Mở Caching.
4. Chọn Purge Cache.
5. Xóa Cache toàn bộ hoặc theo URL cần cập nhật.
6. Tải lại website và kiểm tra kết quả.

### Lỗi 5: Gói miễn phí Cloudflare có đủ dùng không?

Đối với nhiều website cá nhân, blog, website giới thiệu và dự án nhỏ, gói Free có thể đáp ứng các nhu cầu cơ bản.

Bạn có thể sử dụng các tính năng như DNS, CDN, SSL/TLS và một số chức năng bảo mật mà không cần trả phí.

Tuy nhiên, nếu website có lượng truy cập lớn, yêu cầu bảo mật nâng cao hoặc cần các tính năng chuyên biệt, bạn nên tham khảo những gói trả phí và giới hạn sử dụng hiện hành.

## 6. Tài liệu chính thức của Cloudflare

Nếu muốn tìm hiểu sâu hơn về các tính năng và cách cấu hình, bạn có thể tham khảo những tài liệu chính thức sau:

- Trang chủ Cloudflare: [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Trung tâm tài liệu: [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- Hướng dẫn DNS: [https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)
- Hướng dẫn SSL/TLS: [https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)
- Hướng dẫn Cache: [https://developers.cloudflare.com/cache/](https://developers.cloudflare.com/cache/)
- Hướng dẫn WAF: [https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Hướng dẫn Workers: [https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)
- Hướng dẫn Pages: [https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

## 7. Kết luận

Cloudflare là một nền tảng hữu ích dành cho những người quản trị website, từ người mới bắt đầu đến nhà phát triển chuyên nghiệp.

Mười tính năng được giới thiệu trong bài viết bao gồm quản lý DNS, CDN, SSL/TLS, Cache, bảo vệ DDoS, WAF, Redirect Rules, Analytics, Workers và Pages.

Người mới không cần phải sử dụng tất cả các tính năng ngay từ đầu. Bạn có thể bắt đầu bằng việc kết nối tên miền, cấu hình DNS, bật HTTPS và thiết lập các tùy chọn bảo mật cơ bản.

Sau khi đã hiểu rõ cách hoạt động của Cloudflare, bạn có thể tiếp tục tìm hiểu các tính năng nâng cao để cải thiện hiệu suất, bảo mật và khả năng quản lý website.

## 8. Dịch vụ thẻ thanh toán trực tuyến và thuê năng lượng TRON

💳 **CoinePay – Dịch vụ thẻ ảo (Virtual Card)**

Tìm hiểu thêm về các lựa chọn thanh toán trực tuyến và dịch vụ liên quan đến thẻ ảo.

👉 [https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

⚡ **TRXAPI – Dịch vụ thuê năng lượng TRON**

Tìm hiểu dịch vụ thuê năng lượng TRON phục vụ các giao dịch blockchain tương thích.

👉 [https://login.trxapi.io/energy](https://login.trxapi.io/energy)

Lưu ý: CoinePay và TRXAPI là các dịch vụ bên thứ ba độc lập, không phải sản phẩm của Cloudflare và không được giới thiệu là đối tác chính thức của Cloudflare.

## 9. Tài liệu tham khảo

Các thông tin kỹ thuật trong bài viết được tổng hợp từ tài liệu chính thức của Cloudflare. Giao diện, tên tính năng, giới hạn sử dụng và chính sách dịch vụ có thể thay đổi theo thời gian. Người dùng nên tham khảo tài liệu chính thức để cập nhật thông tin mới nhất.