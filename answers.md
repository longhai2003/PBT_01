
Câu A1 

Nguồn: 01_introduction_html_universe.md (phần Browser hoạt động)

Khi mình gõ https://shopee.vn vào trình duyệt thì sẽ có các bước sau:

1. Trình duyệt kiểm tra cache xem đã có dữ liệu chưa
2. Thực hiện DNS lookup để đổi tên miền thành địa chỉ IP
3. Thiết lập kết nối TCP với server
4. Thiết lập HTTPS (TLS handshake) để bảo mật
5. Trình duyệt gửi HTTP request (GET)
6. Server trả về HTTP response (HTML, CSS, JS...)
7. Trình duyệt đọc HTML và tạo DOM
8. Load CSS và JS
9. Render trang web ra màn hình

Tab Network trong DevTools cho biết:

- Các request được gửi đi (HTML, CSS, JS, ảnh...)
- Status code (200, 404…)
- Thời gian load
- Dung lượng file
- Loại file (document, css, script…)


Câu A2 
Nguồn: Chương 04 — Semantic HTML

Trang web bị SEO thấp vì dùng toàn `<div>` thay vì thẻ semantic.

 Các lỗi:

1. Dùng `<div>` thay cho `<header>`
2. Không dùng `<nav>` cho menu
3. Sản phẩm không dùng `<article>`
4. Không có thẻ tiêu đề `<h1>, <h2>`
5. Footer dùng `<div>` thay vì `<footer>`

 Sửa lại:

```html
<header>
    <h1>ShopTLU</h1>
    <nav>
        <a href="/">Trang chủ</a>
        <a href="/products">Sản phẩm</a>
    </nav>
</header>

<main>
    <article>
        <h2>iPhone 16 Pro</h2>
        <p>25.990.000đ</p>
        <figure>
            <img src="iphone.jpg" alt="iPhone">
        </figure>
    </article>
</main>

<footer>
    <p>© 2026 ShopTLU</p>
</footer>

 Câu A3

Kết quả hiển thị:

Hộp 1
Text A Text B
Hộp 2
Text C Text D
Hộp 3

Giải thích:

* `<div>` là block nên luôn xuống dòng
* `<span>` và `<strong>` là inline nên nằm cùng dòng

Nguồn: Chương 03

 Câu A4 — Table

Nguồn: Chương 05

`<thead>`: phần tiêu đề bảng
`<tbody>`: phần nội dung chính
`<tfoot>`: phần cuối (tổng kết)
 Không nên dùng table để layout vì:
- Khó responsive
- Code khó đọc
- Không tốt cho SEO
- Khó sửa sau này

 PHẦN B

 Bài B3 — Debug HTML

Các lỗi mình tìm được:

Lỗi 1: `<!DOCTYPE>` sai → sửa thành `<!DOCTYPE html>`
Lỗi 2: `<title>` chưa đóng
Lỗi 3: charset sai → UTF-8
Lỗi 4: `<h1>` không đóng đúng
Lỗi 5: `<a>` không đóng
Lỗi 6: `<img>` thiếu dấu ngoặc kép
Lỗi 7: `<b>` đóng sai vị trí
Lỗi 8: thiếu `<thead>` trong table
Lỗi 9: có 2 thẻ `<main>`
Lỗi 10: `<footer>` không đóng

 Bài B4 —  Tiki.vn

 Semantic HTML

- `<header>`: phần đầu trang
- `<nav>`: menu
- `<footer>`: cuối trang

 2 lỗi senmantic

- Dùng nhiều `<div>` thay vì `<section>`
- Không dùng `<article>` cho sản phẩm

Table

không tìm thấy table

 Form 

không tìm thấy form

PHẦN C

 Câu C1 

```html
<header>
    <nav> <!-- menu điều hướng -->
        <a href="#">Trang chủ</a>
    </nav>
</header>

<nav aria-label="breadcrumb"> <!-- breadcrumb -->
    <ol>
        <li>Trang chủ</li>
        <li>Điện thoại</li>
        <li>iPhone 16</li>
    </ol>
</nav>

<main>

<section> <!-- ảnh sản phẩm -->
    <figure><img src="#"></figure>
    <figure><img src="#"></figure>
</section>

<section> <!-- thông tin -->
    <h1>Tên sản phẩm</h1>
    <p>Giá</p>
    <p>Đánh giá</p>
</section>

<section> <!-- thông số -->
    <table></table>
</section>

<section> <!-- bình luận -->
    <article>Review 1</article>
</section>

<aside> <!-- sản phẩm liên quan -->
    <p>Gợi ý</p>
</aside>

</main>

<footer>
    <p>© 2026</p>
</footer>
```

Câu C2 

Dùng semantic HTML là cần thiết.
- SEO. Khi dùng các thẻ như `<header>`, `<article>`, `<nav>`, Google sẽ hiểu rõ nội dung trang hơn, từ đó giúp trang dễ lên top hơn.
- accessibility. Các công cụ đọc màn hình sẽ dựa vào các thẻ này để đọc cho người khiếm thị. Nếu dùng toàn `<div>` thì họ sẽ rất khó hiểu cấu trúc trang.
Ví dụ như một trang sản phẩm nếu dùng `<article>` cho mỗi sản phẩm thì sẽ rõ ràng hơn rất nhiều so với dùng `<div>`.
Tuy nhiên, `<div>` vẫn cần dùng trong những trường hợp layout hoặc khi không có thẻ semantic phù hợp.
- semantic HTML không phải là dư thừa mà giúp code dễ hiểu và chuyên nghiệp hơn.
