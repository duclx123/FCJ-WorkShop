---
title: "Blog 2"
date: 2025-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Giới thiệu các triển khai Landing Zone Accelerator theo khu vực mới trên AWS nhằm hỗ trợ chủ quyền số

**Tác giả: Max Peterson — đăng ngày 27/05/2025**  
**Chuyên mục: AWS Well-Architected Framework, Compliance, Europe, Foundational (100), Public Sector, Security, Identity & Compliance, Thought Leadership**

Khách hàng thường nói với tôi rằng họ mong muốn có con đường đơn giản hơn để đáp ứng các yêu cầu tuân thủ và quy định ngành của họ tại các vùng địa lý riêng biệt. Trong các cuộc hợp tác sâu với đối tác và khách hàng, chúng tôi đã học được rằng một trong những thách thức lớn nhất là việc biến các yêu cầu về bảo mật và tuân thủ thành các technical controls riêng biệt.

Tại Amazon Web Services (AWS), bảo mật là ưu tiên hàng đầu của chúng tôi, và chúng tôi hiểu rằng việc bảo vệ dữ liệu của bạn trong một thế giới với quy định, công nghệ và rủi ro thay đổi đòi hỏi sự hợp tác. Như chúng tôi đã nói, bảo mật là nền tảng của chủ quyền số.

AWS giúp các tổ chức phát triển và tiến hóa khả năng về security, identity, và compliance thành những yếu tố thúc đẩy kinh doanh; đó là lý do tại sao chúng tôi cam kết làm việc với các cơ quan mạng quốc gia và các nhà quản lý để giúp định nghĩa và thiết lập cách mà các tiêu chuẩn tuân thủ của họ có thể được chuyển đổi thành best practices về bảo mật trên đám mây. Chúng tôi đang đáp lại các yêu cầu từ khách hàng để tạo ra các cách tiếp cận được tùy chỉnh theo địa phương, phù hợp với các tiêu chuẩn khu vực nội địa do các cơ quan trong vùng đặt ra.

---

## Thực hành kiến trúc tốt nhất – được bản địa hóa theo khu vực  
*(Architectural best practice, locally tailored)*

Kể từ khi ra mắt vào năm 2022, **Landing Zone Accelerator on AWS (LZA)** đã giúp hàng nghìn khách hàng triển khai nền tảng cloud tuân thủ nhiều framework toàn cầu và các AWS best practices, bao gồm:

- **Baseline Informatiebeveiliging Overheid (BIO)** – Hà Lan  
- **Esquema Nacional de Seguridad (ENS)** – Tây Ban Nha  

AWS cam kết mở rộng các bản triển khai khu vực nhằm giúp khách hàng đáp ứng các tiêu chuẩn quốc gia, khu vực và mục tiêu chủ quyền số cụ thể.

Vào tháng 3 vừa qua, chúng tôi đã công bố thỏa thuận hợp tác giữa **Federal Office for Information Security (BSI)** và AWS — trong đó AWS cam kết thúc đẩy chủ quyền số và best practices về an ninh mạng tại Đức cũng như toàn Liên minh Châu Âu (EU).

Vì vậy, chúng tôi vui mừng thông báo rằng bản triển khai khu vực tiếp theo của Landing Zone Accelerator on AWS sẽ hỗ trợ các workload tại **Đức**, với **C5-ready Landing Zone Accelerator**, được thiết kế để giúp khách hàng đáp ứng các mục tiêu tuân thủ **C5 (Cloud Computing Compliance Criteria Catalogue)** trên cloud.

Dự kiến ra mắt vào **quý 3 năm 2025**, bản triển khai này cũng sẽ khả dụng trong **AWS European Sovereign Cloud**.

---

## Tiêu chuẩn C5 và hợp tác với Schellman  
*(C5 Compliance and Partnership with Schellman)*

Tiêu chuẩn **C5 attestation scheme**, do chính phủ Đức hậu thuẫn và được BSI giới thiệu năm 2016, giúp các tổ chức chứng minh năng lực bảo mật vận hành trước các mối đe dọa mạng phổ biến khi sử dụng dịch vụ đám mây.  
AWS đã tuân thủ các yêu cầu của C5 ngay từ khi tiêu chuẩn này được giới thiệu.

Để giúp khách hàng chuẩn bị cho quá trình đánh giá tuân thủ, AWS đã hợp tác với **AWS Global Security & Compliance (GSCA) Partner – Schellman** nhằm cung cấp cái nhìn chuyên sâu cho các đơn vị đánh giá về cách mà **C5-ready Landing Zone Accelerator** có thể đơn giản hóa và tăng tốc hành trình đạt chứng nhận C5 trên AWS.

---

## Schellman – đối tác hàng đầu trong đánh giá C5  
*(Schellman: A Leading Partner in C5 Assessments)*

Là một trong số ít các công ty có chuyên môn sâu trong lĩnh vực đánh giá C5, Schellman đã thực hiện hàng chục đánh giá trên nhiều loại hình khách hàng — từ startup linh hoạt đến tập đoàn toàn cầu.

> “Nhóm của chúng tôi đã chứng kiến tận mắt cách tiêu chuẩn C5 thúc đẩy minh bạch và xây dựng niềm tin trong dịch vụ đám mây. Chúng tôi tự hào không chỉ giúp khách hàng hiểu C5, mà còn biết cách tận dụng tiêu chuẩn này để nâng cao bảo mật và năng lực cạnh tranh toàn cầu.”  
> — **Jeff Schiess, Managing Director, Schellman**

Giảm rào cản tiếp cận – Schellman nhận thấy việc đạt được tuân thủ C5 đôi khi có thể gây áp lực, đặc biệt với các tổ chức mới tiếp cận framework này.

Để hỗ trợ, Schellman đã thực hiện đánh giá trên nền tảng hạ tầng của **LZA on AWS**, được thiết kế để đơn giản hóa quá trình đạt chuẩn C5.

> “Với Landing Zone Accelerator, tổ chức có thể bắt đầu trên một nền tảng C5-ready ngay từ đầu. Đây là một giải pháp thực tiễn, có thể mở rộng cho các doanh nghiệp vốn coi tiêu chuẩn C5 là phức tạp.”  
> — **Kristen Wilbur, Principal, Schellman**

---

## Sovereign by Design – Chủ quyền số ngay từ thiết kế  
*(Sovereign by Design: Embedding Digital Sovereignty from the Start)*

Landing Zone Accelerator on AWS tự động triển khai hàng trăm khả năng bảo mật tương ứng với các yêu cầu kiểm soát trong nhiều framework tuân thủ khu vực khác nhau. Điều này giúp khách hàng tiết kiệm hàng trăm giờ trong việc lên kế hoạch và cấu hình bảo mật, nhờ nền tảng được xây dựng dựa trên **AWS Well-Architected Security Pillar** và các **AWS security best practices**.

Những khả năng cốt lõi mà khách hàng cần trong workload “**sovereign-by-design**” bao gồm:

- Đáp ứng yêu cầu tuân thủ  
- Kiểm soát truy cập và hạn chế truyền dữ liệu có thể xác minh  
- Quyền tự chủ trong lựa chọn công nghệ  
- Khả năng phục hồi trước gián đoạn quy mô lớn  

AWS cung cấp hướng dẫn chi tiết về cấu hình LZA phù hợp với yêu cầu bảo mật, tuân thủ và chủ quyền số địa phương, bao gồm **control mapping** với quy định trong nước và các chính sách nội bộ.

---

## Kiểm soát vị trí và quyền truy cập dữ liệu  
*(Data Location and Access Control)*

Landing Zone Accelerator on AWS mang đến cho khách hàng các cơ chế **kiểm soát phòng ngừa**, **giám sát**, và **chủ động** có thể cấu hình, giúp họ đáp ứng mục tiêu về **data residency**, **security**, và **compliance** — dù là:

- cơ quan nhà nước cần lưu dữ liệu trong một **AWS Region duy nhất**, hoặc  
- doanh nghiệp đa quốc gia với yêu cầu chủ quyền số phức tạp.

Không chỉ dừng ở môi trường multi-account an toàn, LZA còn thiết lập **kiến trúc nhiều tài khoản có cấu trúc tốt**, dựa trên AWS Organizations, giúp:

- Cô lập workload, chức năng quản lý và kiểm soát bảo mật  
- Tăng cường bảo mật, hiệu quả vận hành  
- Thực thi chính sách thống nhất về data residency, access management và compliance  

Nhờ đó, khách hàng có thể nhanh chóng tận dụng khả năng đổi mới của cloud, đồng thời duy trì nền tảng bảo mật và tuân thủ vững chắc.

---

## Đối tác – trung tâm của hệ sinh thái chủ quyền số  
*(Partners at the Core of the Digital Sovereignty Ecosystem)*

AWS hiểu rằng việc điều hướng bức tranh chủ quyền số phức tạp đòi hỏi sự hợp tác.  
Thông qua **AWS Digital Sovereignty Competency**, khách hàng có thể kết nối với các đối tác đáng tin cậy, có kinh nghiệm tư vấn và thiết kế đáp ứng yêu cầu chủ quyền số, đồng thời tận dụng toàn bộ tiềm năng của AWS Cloud.

Chương trình này hỗ trợ đối tác giải quyết các thách thức trong 4 trụ cột chính:

- Data Residency  
- Data Protection  
- Access Control  
- Survivability  

> “Tuân thủ các quy định như C5 là điều bắt buộc với khách hàng khu vực công và các ngành được quản lý chặt, đặc biệt khi họ ưu tiên chủ quyền số. Sự ra mắt của C5 LZA giúp giảm đáng kể độ phức tạp kỹ thuật, rút ngắn thời gian ra thị trường và thúc đẩy đổi mới.”  
> — **Boris Hecker, Managing Director, ATOS Germany**

> “Khách hàng trong khu vực công và các ngành được quản lý cần các giải pháp vừa đáp ứng quy định, vừa hỗ trợ đổi mới. SVA tin tưởng vào Landing Zone Accelerator on AWS như một giải pháp giúp cân bằng giữa tuân thủ và đổi mới, kết hợp hạ tầng public cloud hàng đầu với các yêu cầu pháp lý địa phương.”  
> — **Patrick Glawe, Hyperscaler Lead, SVA**

---

## Tác giả

### Max Peterson  
Max là **Vice President of AWS Sovereign Cloud**. Ông dẫn dắt các nỗ lực nhằm đảm bảo rằng tất cả khách hàng của AWS trên toàn thế giới đều có quyền truy cập vào tập hợp đầy đủ nhất các **sovereignty controls**, **privacy safeguards**, và **security features** tiên tiến nhất trên nền tảng cloud.

Trước vai trò hiện tại, Max từng là **Vice President của AWS Worldwide Public Sector (WWPS)**, nơi ông sáng lập và lãnh đạo **WWPS International Sales division**, tập trung vào hỗ trợ các tổ chức trong lĩnh vực:

- government  
- education  
- healthcare  
- aerospace & satellite  
- nonprofit  

Max có hơn **30 năm kinh nghiệm** trong khu vực công và từng giữ nhiều vị trí **technology leadership** trước khi gia nhập Amazon.  
Ông tốt nghiệp **Cử nhân Tài chính (BA in Finance)** và **MBA chuyên ngành MIS** tại University of Maryland.