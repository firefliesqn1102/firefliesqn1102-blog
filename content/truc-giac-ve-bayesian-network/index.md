---
title: "Trực giác về Bayesian Network"
description: "Chúng ta hãy bắt đầu câu chuyện về Bayesian Network thông qua một ví dụ đơn giản. Chúng ta có một joint distribution gồm 8 biến ngẫu nhiên…"
date: "2022-07-28T13:49:32.273Z"
categories: []
published: true
canonical_link: https://medium.com/@firefliesqn/tr%E1%BB%B1c-gi%C3%A1c-v%E1%BB%81-bayesian-network-f06034bdec95
redirect_from:
  - /trực-giác-về-bayesian-network-f06034bdec95
---

undefined

Chúng ta hãy bắt đầu câu chuyện về Bayesian Network thông qua một ví dụ đơn giản. Chúng ta có một joint distribution gồm 8 biến ngẫu nhiên như sau P(X1, X2, X3, X4, X5, X6, X7, X8), các biến của chúng ta đều là bernoulli’s distribution. Mỗi biến có 2 khả năng xảy ra tức là có ²⁸ phần tử trong không gian sự kiện của joint distribution, một con số khổng lồ nếu bạn muốn lấy mẫu trong thực tế và giải bài toán xác định joint distribution của chúng ta.

undefined

Sẽ như thế nào nếu chúng ta biết trước về mối quan hệ giữa các biến trông như hình trên. Khi đó chúng ta sẽ đơn giản đi rất nhiều độ khó bài toán ban đầu với không gian sự kiện là ²⁸, lúc này chỉ còn là việc xác định các phân phối xác suất riêng lẻ với kích thước không gian sự kiện rất nhỏ. Xác suất các bạn cần tính mô tả như hình bên dưới.

undefined

Hãy khoan thắc mắc về các mối quan hệ được định nghĩa thế nào mà ta có thể tính toán bằng công thức trên, chúng ta sẽ “get it” trong các bài sau của chủ đề này. Tinh thần của câu chuyện hiện tại là chúng ta biết cách giảm Complexity bài toán bằng cách khai thác mối quan hệ được biết trước. Thế giới mà chúng ta đang sống, nơi mà các sự kiện liên quan với nhau, chúng ta muốn xây dựng các mô hình xác suất để ra quyết định bằng cách lấy mẫu và giải bài toán Machine Learning. Sẽ tốt hơn rất nhiều nếu chúng ta khai thác lượng thông tin biết trước, lời giải cho bài toán cần tìm sẽ bớt đau khổ đi phần nào.

undefined

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

### Conclusion

Congratulations! You have just completed a cool data science topic with me.

Thank you for reading!  
Nguyễn Chiến 28–7–2022.
