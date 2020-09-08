[![npm version](http://img.shields.io/npm/v/nk-vector.svg?style=flat)](https://npmjs.org/package/nk-vector "View this project on npm")

# Giới thiệu về NK-VECTOR!

## Lý do ra đời
>  Về cơ bản, NK-VEC là một Neural Network Embeddings, có nhiệm vụ giống tất cả các mô hình nhúng từ hiện tại, nhưng nó có cấu tạo đơn giản hơn rất nhiều. Thông qua thư viện NK-VECTOR, bạn có thể sử dụng mô hình NK-VEC để build bộ vector theo dữ liệu riêng của bạn một cách đơn giản nhất. Ngoài ra NK-VECTOR còn cung cấp cho bạn một số tính năng, thuật toán hữu ích dùng để giải quyết các bài toán NLP.
## Về tên gọi
> Tôi tạo ra nó trong lúc nghiên cứu dự án lớn tại phòng tin học của trường THCS-THPT Nguyễn Khuyến, nên NK là chữ viết tắt của tên trường, đây dấu ấn tôi muốn lưu lại và nó xứng đáng được thế.

# Các tính năng hiện tại
> * Tạo one hot vector
> * Tạo windows words
> * Cho phép người dùng build bộ vector theo bộ dữ liệu riêng của họ
> * Tìm từ tương tự
> *  Fast KNN (KNN K-d tree)
> * Build vetor cho câu, cho đoạn văn, văn bản
> * Tách từ tiếng Việt và tiếng Anh
> * Làm sạch câu cho tiếng Việt và tiếng Anh
> * Xóa từ lặp lại
# Cách sử dụng
## Cài đặt
> npm i nk-vector
## Sử dụng
```javascript
let  NKV = require('nk-vector')
```
> Ví dụ: Sử dụng hàm knn
```javascript
let  points = [
[ 1, 2 ],
[ 3, 4 ],
[ 5, 6 ],
[ 7, 8 ]
];
let  nearest = NKV.knn([ 7, 8 ], 'eculid', points, 4);
console.log(nearest);
/*result:
[ [ { '0': 7, '1': 8 }, 0 ],
  [ { '0': 5, '1': 6 }, 8 ],
  [ { '0': 3, '1': 4 }, 32 ],
  [ { '0': 1, '1': 2 }, 72 ] ]*/
```