---
title: "Curse of Big Data"
description: "Trong nhiều lĩnh vực nghiên cứu, chi phí thu thập data hiện nay thấp hơn, đôi khi thấp hơn nhiều so ới chi phí phân tích data. Khó khăn…"
date: "2022-07-28T14:15:49.455Z"
categories: []
published: true
canonical_link: https://medium.com/@firefliesqn/curse-of-big-data-bd42f198ca5a
redirect_from:
  - /curse-of-big-data-bd42f198ca5a
---

undefined

Trong nhiều lĩnh vực nghiên cứu, chi phí thu thập data hiện nay thấp hơn, đôi khi thấp hơn nhiều so ới chi phí phân tích data. Khó khăn trong việc chuyển đổi dữ liệu lớn thành tri thức có liên quan đến độ phức tạp của nó , bản chất được nắm bắt rộng rãi với ‘Four Vs’: volume, velocity, variety and veracity.

### 1\. Volume

Việc xử lý các tập dữ liệu lớn có thể yêu cầu một cơ sở hạ tầng đặc biệt như Hadoop nơi một số lượng lớn các records được lưu trưc trong các phần riêng biệt rải trên nhiều Node. Chi phí của processors, memory và disk space tiếp tục giảm , yếu tố hạn chế hiện nay thường là giao tiếp giữa các máy. Do đó không thể hoặc không thực tế để truy cập toàn bộ data trên một processor nhất định và nhiều phương pháp sẽ thất bại vì chúng không được xây dựng để triển khai từ các phân dữ liệu riêng biệt. Cần phải có những phát triển và đang được thực hiện để cung cấp các phương pháp thống kê dược sử dụng rộng rãi cho dữ liệu phân tán như vậy.

EDA là một bước chuẩn bị và làm sạch dữ liệu rất quan trọng trở nên khó khăn hơn đáng kể khi kích thước data ngày càng tăng. Ngoài sự phức tạp về mặt kĩ thuật của việc quản lý data, mà số trong các graphical vài triệu pixel về cơ bản cần các biểu diễn chiều thấp hơn, dễ giải thích đó là cách bộ não con người hoạt đ. Một ví dụ khác là chúng ta thường chỉ trực quan hoá một tập con nhỏ của dữ liệu tại một thời điểm và điều này có thể mang lại cái nhìn bias.

### 2\. Variety

Đối với nhiều vấn đề về dữ liệu lớn, sự đa dạng của các loại dữ liệu có liên quan mật thiết đến sự gia tăng độ phức tạp. Phần lớn mô hình thống kê cổ điển giả định cấu trúc dữ liệu ‘cao và gầy’ với nhiều hàng hơn, lập chỉ mục các đơn vị quan sát hoặc thực nghiệm , hơn là các cột, lập chỉ mục các biến . Hình ảnh, cả hai chiều và ba chiều, bài đăng trên blog, nguồn cấp dữ liệu twitter, mạng xã hội, bản ghi âm, mạng cảm biến và video chỉ là một số ví dụ về các loại dữ liệu mới không phù hợp với mô hình ‘hình chữ nhật’ này. Thông thường, dữ liệu hình chữ nhật được tạo hơi giả tạo: ví dụ: đối với hình ảnh hai chiều, bằng cách sắp xếp các pixel theo hàng và ghi lại một hoặc nhiều giá trị được liên kết với mỗi pixel, do đó làm mất thông tin về cấu trúc của dữ liệu.

Đối với nhiều loại dữ liệu lớn, số lượng biến lớn hơn, thường lớn hơn nhiều so với số lượng quan sát. Sự thay đổi mối quan hệ giữa n và p này có thể dẫn đến hành vi phản trực giác, hoặc phá vỡ hoàn toàn các phương pháp phân tích thông thường. Các vấn đề trong đó p tỷ lệ với n là rất phổ biến: ví dụ, trong các mô hình mạng gán một tham số cho mỗi nút, có p = n tham số cho một đồ thị có n × n cạnh có thể có (Chung và Lu, 2002). Tương tự, Bioucas-Dias et al. (2013) thảo luận về dữ liệu ảnh viễn thám siêu kính, có thể có hàng trăm hoặc hàng nghìn dải phổ, p, nhưng một số lượng rất nhỏ các mẫu huấn luyện, n. Trong một nghiên cứu gen gần đây được báo cáo bởi 1000 Genomes Project Consortium (2012), các nhà di truyền học đã thu thập dữ liệu về p = 38 triệu đa hình nucleotide đơn ở chỉ n = 1092 cá thể.

Các tính chất tiệm cận của phương pháp cổ điển trong một chế độ mà p tăng theo n là hoàn toàn khác so với trong chế độ cổ điển của p cố định. Ví dụ: nếu Xi, i = 1,…, n độc lập và được phân phối giống nhau dưới dạng N (0, I) và p / n không đổi khi p và n tăng lên, các giá trị riêng của ma trận hiệp phương sai thực nghiệm không hội tụ về giá trị thực của 1, mà có phân phối giới hạn được mô tả bởi định luật Marcenko — Pastur. Donoho và Gavish (2014) cho thấy luật này có liên quan như thế nào để hiểu được rủi ro tối thiểu tiệm cận trong việc ước tính ma trận hạng thấp từ các phép đo nhiễu bằng cách lập ngưỡng các giá trị kỳ dị. Donoho và cộng sự. (2013) thu được kết quả tương tự cho bài toán khôi phục ma trận.

### 3\. Veracity

Một số dữ liệu lớn thu được bằng cách ghép một số bộ dữ liệu chưa được thu thập với câu hỏi nghiên cứu hiện tại trong tâm trí: điều này đôi khi được gọi là ‘dữ liệu tìm thấy’ hoặc ‘mẫu tiện lợi’. Loại dữ liệu này thường sẽ có cấu trúc cực kỳ không đồng nhất (Hodas và Lerman, 2014) và có thể hoàn toàn không đại diện cho nhóm dân cư quan tâm. Phần lớn dữ liệu lớn là quan sát nhưng quan trọng hơn có thể được thu thập rất bừa bãi. Những ý tưởng cổ điển về thiết kế thử nghiệm, lấy mẫu khảo sát và thiết kế các nghiên cứu quan sát thường bị lạc trong sự phấn khích của sự sẵn có của một lượng lớn dữ liệu. Các vấn đề về sai lệch lấy mẫu, nếu bị bỏ qua, có thể dẫn đến suy luận sai dễ dàng với dữ liệu lớn cũng như với dữ liệu nhỏ. Harford (2014) trình bày một số thất bại nổi tiếng, từ cuộc thăm dò của Tạp chí Văn học năm 1936, có hai triệu người tham gia, đến Google Xu hướng Dịch cúm vào năm 2010, dựa trên các dự đoán của mình trên các cụm từ tìm kiếm trên internet đã đánh giá quá cao mức độ phổ biến của bệnh cúm. Bất chấp những hạn chế đó, các cơ quan thống kê quốc gia đang phát triển các phương pháp để sử dụng cẩn thận các dữ liệu đó, ví dụ, như một biện pháp hỗ trợ cho việc áp đặt trên các khu vực nhỏ (Marchetti et al.2015).

Việc làm sạch khối lượng lớn dữ liệu là một thách thức và tính xác thực bị ảnh hưởng bởi việc làm sạch không đầy đủ hoặc không chính xác và thiếu các công cụ để đánh giá chất lượng dữ liệu. Ví dụ, để xác nhận rằng thước đo tình cảm được tính toán từ phương tiện truyền thông xã hội là đúng đắn, Daas et al. (2015) đã đánh giá tính nhất quán của nó với một chỉ số được xác nhận tốt về niềm tin của người tiêu dùng. Mặc dù rõ ràng là dữ liệu mạng xã hội bị nhiễu và dễ bay hơi, nhưng dữ liệu thu thập từ các cảm biến cũng có thể gặp một số vấn đề, bao gồm một tỷ lệ lớn các giá trị bị thiếu. Daas và cộng sự. (2015) được coi là một ví dụ về các vấn đề liên quan đến việc làm sạch dữ liệu bộ dò vòng lặp lưu lượng.

Chất lượng dữ liệu trong cơ sở dữ liệu hành chính lớn là một vấn đề cấp bách: sự không đồng nhất bổ sung có thể được đưa ra khi dữ liệu được ghi lại bởi nhiều bên liên quan với các ưu tiên và khuyến khích khác nhau. Lix và cộng sự. (2012) sử dụng mô hình hóa để đánh giá và cải thiện chất lượng dữ liệu trong cơ sở dữ liệu dịch vụ y tế lớn.

### 4\. Velocity

Trong nhiều lĩnh vực ứng dụng, dữ liệu là ‘lớn’ vì nó đến với tốc độ cao, ví dụ như từ các thiết bị đo hoạt động liên tục, khi xem xét các tình huống lái xe tự động (Geiger và cộng sự.2012) hoặc thông qua dịch vụ phát trực tuyến. Có thể cần các phương pháp phân tích tuần tự hoặc trực tuyến, đòi hỏi các phương pháp suy luận có thể được tính toán nhanh chóng, thích ứng nhiều lần với dữ liệu được thêm vào tuần tự và không bị đánh lừa bởi sự xuất hiện đột ngột của dữ liệu không liên quan, chẳng hạn như đã thảo luận bởi Jain et al. (2006) và Hoens et al. (2012). Các lĩnh vực ứng dụng sử dụng học tuần tự rất đa dạng. Ví dụ, Li và Fei-Fei (2010) sử dụng các kỹ thuật nhận dạng đối tượng theo cách tuần tự hiệu quả để tìm hiểu các mô hình danh mục đối tượng từ bất kỳ số lượng lớn hình ảnh tùy ý nào từ web. Monteleoni và cộng sự. (2011) sử dụng học tập tuần tự cho mô hình biến đổi khí hậu để ước tính xác suất chuyển đổi giữa các mô hình khí hậu khác nhau. Đối với một số ứng dụng, chẳng hạn như vật lý năng lượng cao, các loạt dữ liệu đến nhanh đến mức không thể ghi lại tất cả. Trong trường hợp này, cần có nhiều chuyên môn khoa học để đảm bảo rằng dữ liệu được giữ lại có liên quan đến vấn đề quan tâm.

### 5\. Beyond the Vs

Dữ liệu lớn là về con người, nó cung cấp những khả năng mới và do đó, nó đặt ra những câu hỏi đạo đức mới. Ví dụ, Duhigg (2012) đã báo cáo cách các cửa hàng bán lẻ mục tiêu thực hiện phân tích để gửi tài liệu tiếp thị được nhắm mục tiêu đến khách hàng của họ, bao gồm cả các chương trình khuyến mãi liên quan đến việc mang thai được gửi đến một thiếu niên mà bố chưa biết đến em bé sắp chào đời. Tại Facebook, Kramer et al. (2014) đã tiến hành một thử nghiệm quy mô lớn về cảm xúc mà không có được sự đồng ý của người dùng cụ thể (xem thêm Meyer, 2014).

Quyền riêng tư cũng là một mối quan tâm lớn, đặc biệt khi xem xét rằng việc liên kết các cơ sở dữ liệu có thể tiết lộ thông tin được coi là ẩn danh. Nói chung, nếu dữ liệu được phát hành có thể được liên kết với dữ liệu có sẵn công khai, chẳng hạn như các bài báo trên phương tiện truyền thông, thì quyền riêng tư hoàn toàn có thể bị xâm phạm. Vụ kiện sau Thử thách Netflix là một ví dụ nổi bật về việc liên kết dữ liệu được cung cấp với các đánh giá trên cơ sở dữ liệu phim internet IMDB cho phép xác định một số người dùng (Singel, 2009; 2010). Một ví dụ nổi bật khác là việc công bố hồ sơ sức khỏe của Thống đốc Massachusetts, từ đó dẫn đến luật nghiêm ngặt về thu thập và công bố dữ liệu sức khỏe ở Hoa Kỳ được gọi là ‘quy tắc HIPAA’ (Tarran, 2014). Ngoài quyền riêng tư, các câu hỏi pháp lý cũng chưa được giải đáp: chẳng hạn như bản quyền và quyền sở hữu dữ liệu không phải lúc nào cũng rõ ràng (ví dụ: Struijs và cộng sự, 2014).

Sub-sampling từ một tập dữ liệu lớn thường được trình bày như một giải pháp cho một số vấn đề đặt ra trong phân tích dữ liệu lớn; một ví dụ là ‘túi giày dép nhỏ’ của Kleiner et al. (2014). Mặc dù chiến lược này có thể hữu ích để phân tích một tập dữ liệu rất lớn, nhưng nếu không thường xuyên, nó không thể giải quyết nhiều thách thức đã được trình bày trong phần này.

---

Nguyễn Chiến 28–7–2022

References: [https://onlinelibrary.wiley.com/doi/full/10.1111/insr.12176](https://onlinelibrary.wiley.com/doi/full/10.1111/insr.12176)
