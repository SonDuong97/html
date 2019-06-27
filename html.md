# Html

## Mục tiêu chung

* Hiểu được cấu trúc file html
* Các thẻ (tag) html cơ bản và ý nghĩa của các thẻ đó (thẻ nào dùng vào việc gì)
* Xây dựng được các khối html cơ bản

## Hướng dẫn chung

* Tham khảo các tài liệu trên mạng theo từ khóa:
	* Ví dụ: khi tìm hiểu thẻ `input` có thể search google `html input tag`
* Các nguồn tài liệu tham khảo được khuyến khích
	* [HtmlDog](http://www.htmldog.com/guides/html/)
	* [W3schools](http://www.w3schools.com/html/default.asp)
	* [Mozilla Developer Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)

## Guideline

### 1. Cấu trúc cơ bản

```html
<!DOCTYPE html><!-- Thẻ này này là để khai báo rằng đây là HTML -->
<html><!-- Thẻ này này là để khai báo phần tử root của trang HTML, định nghĩa toàn bộ document -->
<head><!-- Thẻ này này là để chứa các metadata của HTML vd như title, meta, links, styles, scripts-->
	<meta charset="UTF-8"><!-- Thẻ này này là gì có tác dụng gì? -->
	<title>Page Title</title><!-- Thẻ này này là để khai báo tiêu đề của trang HTML -->
</head><!-- Thẻ này này là thẻ đóng của thẻ head -->
<body><!-- Thẻ này này là chứa nội dung của HTML -->
  <!-- class: là để khai báo lớp cho một thẻ. Một thẻ có thể có nhiều class và class không phải là duy nhất -->
  <!-- id: là để khai báo id cho một thẻ. id là duy nhất -->
    <p id="this-p" class="paragraphs">This is my first web page</p>
    <!-- Comment trong html -->
</body>
</html>
```
### 2. Thẻ heading

```html
<!-- Thẻ heading định nghĩa 1 đề mục, h1 có mức độ quan trọng nhất, h5 có mức độ quan trọng ít nhất -->
<!-- Các công cụ tìm kiếm sử dụng heading để làm chỉ mục cấu trúc và cấu trúc của trang web -->
<h1>Heading 1</h1> <!-- Sử dụng khi làm heading chính cho HTML -->
<h2>Heading 2</h2> <!-- Còn các thẻ còn lại dùng tùy trường hợp -->
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
```

### 3. Thẻ paragraph

```html
<p>This is a paragraph</p>
```

### 4. Thẻ link

```html
<!-- Ý nghĩa của các attribute href, title, target là gì. Các giá trị có thể có của các attribute này là gì? -->
<a href="/url" title="Link title" target="_blank">This is a link</a>
<!-- href: chứa url đích cần đến -->
<!-- title: khi trỏ chuột vào link thì nó sẽ hiển thị title -->
<!-- target: chỉ định nơi mở link, ví dụ _blank là mở trong tab mới -->
```

### 4. Thẻ image

```html
<!-- Hiểu được ý nghĩa và giá trị có thể có của các attribute -->
<!-- Thẻ tự đóng nghĩa là gì -->
<img src="/uri" alt="image" width="50px" height="50px" />
<!-- src: chứa đường dẫn của image -->
<!-- alt: khi không load được ảnh thì sẽ hiển thị lên -->
<!-- width, height là chiều dài và chiều rộng của ảnh -->
```

### 5. Thẻ list

```html
<!-- Phân biệt các thẻ ul, ol, dl. Trường hợp nào nên dùng thẻ nào -->

<!-- Hiển thị danh sách theo các kí tự đặc biệt mặc định là dấu chấm đen -->
<ul>
	<li>item</li>
<ul>

<!-- Hiển thị danh sách có đánh thứ tự mặc định là số -->
<ol>
	<li>item</li>
<ol>

<!-- Hiển thị danh sách mà mỗi item trong danh sách đều có mô tả, thẻ dt là tên, thẻ dd là mô tả -->
<dl>
	<dt>title</dt>
	<dd>item</dd><!-- Có thể có nhiều thẻ dd cho cùng một thẻ dt -->
	<dd>item</dd>
<dl>

<!-- Sử dụng các cấu trúc list lồng nhau như thế nào -->
<!-- Trong các thẻ <li> của <ul> cha thì lại chèn các thẻ <ul> để lồng vào trong list -->
<ul>
	<li>item</li>
	<li>
    <ul>
			<li>sub-item</li>
		</ul>
  </li>
<ul>
```

### 6. Thẻ table

```html
<table>
 <tr>
    <th>1</th><!-- Phân biệt th là tiêu đề của cột, td là chứa dữ liệu của cột tương ứng -->
    <th>2</th> 
    <th>3</th>
  </tr>
  <tr>
    <td rowspan="3">1</td><!-- rowspan có nghĩa là để tạo một khoảng bằng 3 rows -->
    <td>2</td> 
    <td>3</td>
  </tr>
  <tr><!-- tại sao row này chỉ có 2 phần tử? Vì cột trên đã chiếm 1 col nên ở dưới chỉ có 2 -->
    <td>2</td> 
    <td>3</td>
  </tr>
  <tr><!-- tại sao row này chỉ có 1 phần tử? Vì colspan=2 có kích thước bằng 2 cột, và 1 cột do row thứ nhất chiếm-->
    <td colspan="2">3</td><!-- colspan có nghĩa là gì? Tạo một cột có kích thước bằng 2 cột-->
  </tr>
</table>
```

### 7. Thẻ form và các thẻ input

```html
<!-- Các attribute action, method có ý nghĩa gì, các giá trị có thể có -->
<!-- action: là nơi xử lí dữ liệu form submit lên-->
<!-- method: là phương thức submit -->
<form action="action_page.php" method="get">
	<!-- Các type có thể có của thẻ input: text, date, radio, submit ....  -->
    <!-- Các attribue value, name có ý nghĩa như thế nào? -->
    <!-- name: tên thẻ input -->
    <!-- value: giá trị của thẻ input -->
	<input type="hidden" value="" name="" />
	
	<!-- Label for có ý nghĩa gì -->
  <!-- Tạo nhãn cho thẻ input -->
	<label for="">Label</label>
	
    <input type="text" value="" name="" />
    <input type="password" value="" name="" />
    <input type="checkbox" value="" name="" checked /><!-- checked có ý nghĩa là checkbox đã được checked-->
    <input type="radio" value="" name="" />
    <input type="button" value="" name="" /> 
    <input type="submit" value="" name="" />
    
    <!-- Các type có thể có của thẻ button: button, submit, ... -->
    <button type="button">Click me</button>
    
    <!-- rows, cols của thẻ span có ý nghĩa gì -->
    <!-- Kích thước của textarea -->
    <textarea rows="3" cols="10"></textarea>
    
    <select name="">
  		<option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
		<option value="fiat" selected>Fiat</option><!-- selected có ý nghĩa là gì, trường hợp mặc định thì select hiển thị giá trị gì -->
    <!-- selected là giá trị đã được chọn, và select sé hiển thị Fiat -->
		<option value="audi">Audi</option>
	</select>
</form>
```

### 8. Thẻ trung tính (meaningless)

```html
<!-- Thẻ trung tính nghĩa là gì, dùng trong trường hợp nào -->
<!-- Thẻ trung tính nghĩa là thẻ chỉ hiển thị ra mỗi nội dung trong thẻ, thường được sử dụng để css trên cùng một dòng  -->
<!-- Phân biệt thẻ div và thẻ span: thẻ div nó sẽ xuống dòng còn span thì ngay dòng hiện tại-->
<div>
	<span>F</span>irst
</div>
```

### 9. Thẻ style

```html
<!-- Phân biệt style inline, và style load từ file css -->
<!-- inline style: dùng cho một thẻ xác định -->
<!-- style load: liên kết với một file css bên ngoài được khai báo trong thẻ head -->
<head>
  <link rel="stylesheet" href="/background.css">

  <style type="text/css">
      div { background: red; }
  </style>
</head>
<body>
	<div style="background: red;"><div>
</body>
```

### 10. Thẻ script

```html
<!-- Phân biệt script inline, và script load từ file js -->
<!-- script inline: dùng cho một thẻ xác định -->
<!-- script load: liên kết với một file js bên ngoài được khai báo trong thẻ head -->
<body>
	<script src="/alert.js"></script>

 	<script type="text/javscript">
		alert('hello');
    </script>
</body>
```