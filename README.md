# Motyam-brand
متيم هو متجر إلكتروني لبيع الملابس بتصميم عصري ومتجاوب، يهدف إلى تقديم تجربة تسوق سهلة وأنيقة عبر الإنترنت.
<h1>مرحبًا في موقع متيم ❤️</h1>
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متيم - موقع لبيع وشراء الملابس</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #007bff;
            color: white;
            padding: 20px;
            text-align: center;
        }
        nav {
            background-color: #333;
            padding: 10px;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
        }
        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .product {
            display: inline-block;
            width: 30%;
            margin: 10px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: center;
        }
        .product img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #218838;
        }
        form {
            margin-top: 20px;
        }
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>متيم</h1>
        <p>موقعك المفضل لبيع وشراء الملابس</p>
    </header>
    <nav>
        <a href="#home">الرئيسية</a>
        <a href="#sell">بيع ملابس</a>
        <a href="#contact">اتصل بنا</a>
    </nav>
    <div class="container" id="home">
        <h2>ملابس متاحة للبيع</h2>
        <div id="products">
            <!-- منتجات أولية -->
            <div class="product">
                <img src="https://via.placeholder.com/300x200?text=قميص" alt="قميص">
                <h3>قميص رجالي</h3>
                <p>سعر: 50 ريال</p>
                <button onclick="buyItem('قميص رجالي')">اشترِ الآن</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/300x200?text=فستان" alt="فستان">
                <h3>فستان نسائي</h3>
                <p>سعر: 80 ريال</p>
                <button onclick="buyItem('فستان نسائي')">اشترِ الآن</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/300x200?text=بنطال" alt="بنطال">
                <h3>بنطال جينز</h3>
                <p>سعر: 70 ريال</p>
                <button onclick="buyItem('بنطال جينز')">اشترِ الآن</button>
            </div>
        </div>
    </div>
    <div class="container" id="sell">
        <h2>أضف ملابس للبيع</h2>
        <form id="sellForm">
            <input type="text" id="itemName" placeholder="اسم الملابس" required>
            <input type="number" id="itemPrice" placeholder="السعر" required>
            <textarea id="itemDesc" placeholder="وصف الملابس" required></textarea>
            <button type="submit">أضف للبيع</button>
        </form>
    </div>
    <div class="container" id="contact">
        <h2>اتصل بنا</h2>
        <p>لأي استفسارات، أرسل بريدًا إلكترونيًا إلى: info@matim.com</p>
    </div>

    <script>
        function buyItem(item) {
            alert(`تم شراء ${item}! شكرًا لاستخدام متيم.`);
        }

        document.getElementById('sellForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('itemName').value;
            const price = document.getElementById('itemPrice').value;
            const desc = document.getElementById('itemDesc').value;
            const productsDiv = document.getElementById('products');
            const newProduct = document.createElement('div');
            newProduct.className = 'product';
            newProduct.innerHTML = `
                <img src="https://via.placeholder.com/300x200?text=${name}" alt="${name}">
                <h3>${name}</h3>
                <p>سعر: ${price} ريال</p>
                <p>${desc}</p>
                <button onclick="buyItem('${name}')">اشترِ الآن</button>
            `;
            productsDiv.appendChild(newProduct);
            alert('تم إضافة الملابس للبيع!');
            document.getElementById('sellForm').reset();
        });
    </script>
</body>
</html>
