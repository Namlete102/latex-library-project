# Giới thiệu 

(Đối với phần thư mục thì trình bày mức cơ bản ở đoạn đầu tài liệu, để giúp mọi người hình dung được ban đầu, còn nâng cao sẽ trình bày sau các bài học, và nó sẽ trả lời câu hỏi quan trọng là khi nào thi ta nên sử dụng cách sắp xếp thư mục này . . . và sau đó mới đến như thế nào để hướng dẫn người dùng cách sử dụng nó

Nói tóm lại ta sẽ có các câu hỏi làm chủ đạo chính sau đây: 

+ Là gì ? 
+ Tại sao ? 
+ Khi nào ? 
+ Như thế nào ?)

Phần này sẽ trình bày về cấu trúc của: 

+ Thư mục (khó)
+ Soạn thảo văn bản (căn bản) 
+ Lệnh (căn bản)

## Cấu trúc lệnh và môi trường cơ bản của LaTeX

Cơ bản là sử dụng các từ quen thuộc đi kèm với dấu \ .

Ví dụ: 

```tex
\latex 
```

Nếu ta bắt đầu bằng lệnh begin và kết thúc bằng lệnh end sao cho giá trị bên trong cả hai lệnh đều giống nhau như ví dụ sau: 

```tex
\begin{documents}
. . . 
\end{documents}
```

giúp chúng tạo thành một môi trường (enviroments), và môi trường ở ví dụ trên là môi trường tài liệu (documents).  

Tổng hợp các lệnh và môi trường ở đây: https://www.tug.org/texniques/tn10/latex_cribsheet.pdf

**Câu hỏi**: Vậy sự khác nhau giữa lệnh và môi trường là gì ? 

## Cấu trúc soạn thảo LaTeX

Từ cấu trúc lệnh và môi trường cơ bản của LaTeX trên ta có một cấu trúc toàn cục (global structure) trong phần soạn thảo LaTeX từ đoạn mã sau.  

```latex
\documentclass[12pt]{article}

\begin{document}
Hello \LaTeX
\end{document}
```

Bên trong môi trường `document` là nơi ta viết nội dung chính, mà khi biên dịch (compile) sẽ xuất hiện ở trong trang tài liệu. 

Còn ở giữa lệnh `\documentclass` và môi trường `document` được gọi là **preamble** (tạm dịch là vùng lời tựa). 


## Cấu trúc thư mục cho các tệp LaTeX 

Gồm: 

+ main.tex (phần đầu não) 
+ preamble.tex (quản lý các package)
+ bibliography.tex (tài liệu tham khảo) 
+ images (thư mục chứa hình ảnh)
+ section (thư mục chứa các phần, ..vv..)
+ style (chứa các bài học nâng cao khác)

câu nối giữa các thư mục để vào `main.tex` gồm: 

+ lệnh `\input` 
+ lệnh `\import` 
+ lệnh `\include` 
