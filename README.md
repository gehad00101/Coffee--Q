<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>كوفي كيو</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f7f3ed; /* لون خلفية فاتح مستوحى من القهوة */
            color: #333;
        }
        /* Updated Product Card Styling */
        .product-card {
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            background-color: #ffffff; /* White background for cards */
            border-radius: 1.5rem; /* More rounded corners */
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1); /* Stronger shadow */
            overflow: hidden;
        }
        .product-card:hover {
            transform: translateY(-8px); /* Slightly more lift on hover */
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15); /* Even stronger shadow on hover */
        }
        .message-box {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #4CAF50; /* لون أخضر للنجاح */
            color: white;
            padding: 15px 25px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
            text-align: center;
        }
        .message-box.show {
            opacity: 1;
        }
        /* Custom button styling for a more prominent look */
        .add-to-cart-btn {
            background: linear-gradient(to right, #d97706, #fbbf24); /* Gradient background */
            border: none;
            color: white;
            font-weight: bold;
            padding: 0.75rem 1.5rem;
            border-radius: 0.75rem; /* Rounded button */
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        .add-to-cart-btn:hover {
            background: linear-gradient(to right, #fbbf24, #d97706); /* Reverse gradient on hover */
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
            transform: translateY(-2px);
        }
    </style>
</head>
<body class="flex flex-col min-h-screen">

    <div id="messageBox" class="message-box">
        تمت إضافة المنتج إلى السلة!
    </div>

    <header class="bg-gray-800 text-white p-4 shadow-lg">
        <div class="container mx-auto flex flex-col md:flex-row justify-between items-center">
            <h1 class="text-3xl font-bold text-amber-300 mb-2 md:mb-0">كوفي كيو</h1>
            <nav>
                <ul class="flex space-x-4 md:space-x-6 text-lg">
                    <li><a href="#" class="hover:text-amber-300 transition duration-300">الرئيسية</a></li>
                    <li><a href="#products" class="hover:text-amber-300 transition duration-300">المنتجات</a></li>
                    <li><a href="#" class="hover:text-amber-300 transition duration-300">عنا</a></li>
                    <li><a href="#" class="hover:text-amber-300 transition duration-300">تواصل معنا</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="bg-cover bg-center h-96 flex items-center justify-center text-white shadow-inner" style="background-image: url('https://placehold.co/1200x500/A0522D/FFFFFF?text=استمتع+بنكهة+القهوة+الفريدة');">
        <div class="text-center bg-black bg-opacity-50 p-6 rounded-lg">
            <h2 class="text-5xl font-extrabold mb-4">اكتشف عالم القهوة</h2>
            <p class="text-xl mb-6">أجود أنواع البن من حول العالم، محضرة بشغف.</p>
            <a href="#products" class="bg-amber-500 hover:bg-amber-600 text-white font-bold py-3 px-8 rounded-full text-lg transition duration-300 shadow-lg">تسوق الآن</a>
        </div>
    </section>

    <section id="products" class="container mx-auto px-4 py-12 flex-grow">
        <h2 class="text-4xl font-bold text-center mb-10 text-gray-800">منتجاتنا المميزة</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
            <div class="product-card">
                <img src="https://placehold.co/600x400/8B4513/FFFFFF?text=بن+أثيوبي" alt="بن أثيوبي فاخر" class="w-full h-48 object-cover rounded-t-2xl">
                <div class="p-6">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-2">بن أثيوبي فاخر</h3>
                    <p class="text-gray-600 text-sm mb-4">حبوب بن أرابيكا محمصة بعناية من مرتفعات إثيوبيا، بإيحاءات الفواكه الحمراء والزهور.</p>
                    <div class="flex justify-between items-center mb-4">
                        <span class="text-3xl font-bold text-amber-600">65 ر.س</span>
                        <span class="text-gray-500 line-through">75 ر.س</span>
                    </div>
                    <button class="add-to-cart-btn w-full">أضف إلى السلة</button>
                </div>
            </div>

            <div class="product-card">
                <img src="https://placehold.co/600x400/6A0DAD/FFFFFF?text=بن+كولومبي" alt="بن كولومبي مميز" class="w-full h-48 object-cover rounded-t-2xl">
                <div class="p-6">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-2">بن كولومبي مميز</h3>
                    <p class="text-gray-600 text-sm mb-4">قهوة كولومبية غنية النكهة، بقوام متوازن وإيحاءات الشوكولاتة والمكسرات.</p>
                    <div class="flex justify-between items-center mb-4">
                        <span class="text-3xl font-bold text-amber-600">58 ر.س</span>
                    </div>
                    <button class="add-to-cart-btn w-full">أضف إلى السلة</button>
                </div>
            </div>

            <div class="product-card">
                <img src="https://placehold.co/600x400/4B0082/FFFFFF?text=آلة+اسبريسو+منزلية" alt="آلة اسبريسو منزلية" class="w-full h-48 object-cover rounded-t-2xl">
                <div class="p-6">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-2">آلة اسبريسو منزلية</h3>
                    <p class="text-gray-600 text-sm mb-4">آلة اسبريسو مدمجة وسهلة الاستخدام، مثالية لتحضير قهوتك المفضلة في المنزل.</p>
                    <div class="flex justify-between items-center mb-4">
                        <span class="text-3xl font-bold text-amber-600">999 ر.س</span>
                    </div>
                    <button class="add-to-cart-btn w-full">أضف إلى السلة</button>
                </div>
            </div>

            <div class="product-card">
                <img src="https://placehold.co/600x400/8B0000/FFFFFF?text=مطحنة+قهوة+يدوية" alt="مطحنة قهوة يدوية" class="w-full h-48 object-cover rounded-t-2xl">
                <div class="p-6">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-2">مطحنة قهوة يدوية</h3>
                    <p class="text-gray-600 text-sm mb-4">مطحنة يدوية عالية الجودة، للحصول على طحن متجانس وتحكم كامل بدرجة الطحن.</p>
                    <div class="flex justify-between items-center mb-4">
                        <span class="text-3xl font-bold text-amber-600">180 ر.س</span>
                        <span class="text-gray-500 line-through">200 ر.س</span>
                    </div>
                    <button class="add-to-cart-btn w-full">أضف إلى السلة</button>
                </div>
            </div>

            <div class="product-card">
                <img src="https://placehold.co/600x400/556B2F/FFFFFF?text=أكواب+قهوة+سيراميك" alt="أكواب قهوة سيراميك" class="w-full h-48 object-cover rounded-t-2xl">
                <div class="p-6">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-2">أكواب قهوة سيراميك</h3>
                    <p class="text-gray-600 text-sm mb-4">طقم أكواب سيراميك فاخرة بتصميم أنيق، مثالية لتجربة قهوة متكاملة.</p>
                    <div class="flex justify-between items-center mb-4">
                        <span class="text-3xl font-bold text-amber-600">90 ر.س</span>
                    </div>
                    <button class="add-to-cart-btn w-full">أضف إلى السلة</button>
                </div>
            </div>

            <div class="product-card">
                <img src="https://placehold.co/600x400/2F4F4F/FFFFFF?text=ميزان+قهوة+رقمي" alt="ميزان قهوة رقمي" class="w-full h-48 object-cover rounded-t-2xl">
                <div class="p-6">
                    <h3 class="text-2xl font-semibold text-gray-900 mb-2">ميزان قهوة رقمي</h3>
                    <p class="text-gray-600 text-sm mb-4">ميزان دقيق مع مؤقت، أساسي لتحضير قهوة مثالية بالوزن الصحيح.</p>
                    <div class="flex justify-between items-center mb-4">
                        <span class="text-3xl font-bold text-amber-600">120 ر.س</span>
                    </div>
                    <button class="add-to-cart-btn w-full">أضف إلى السلة</button>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-gray-800 text-white p-6 mt-12">
        <div class="container mx-auto text-center text-sm">
            <p>&copy; 2025 كوفي كيو. جميع الحقوق محفوظة.</p>
            <div class="flex justify-center space-x-4 mt-2">
                <a href="#" class="hover:text-amber-300 transition duration-300">سياسة الخصوصية</a>
                <a href="#" class="hover:text-amber-300 transition duration-300">شروط الاستخدام</a>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const addToCartButtons = document.querySelectorAll('.add-to-cart-btn');
            const messageBox = document.getElementById('messageBox');
            let messageTimeout;

            addToCartButtons.forEach(button => {
                button.addEventListener('click', () => {
                    // إظهار رسالة التنبيه
                    messageBox.classList.add('show');

                    // مسح أي مؤقت سابق لضمان عدم اختفاء الرسالة قبل الوقت المحدد
                    clearTimeout(messageTimeout);

                    // إخفاء الرسالة بعد 3 ثوانٍ
                    messageTimeout = setTimeout(() => {
                        messageBox.classList.remove('show');
                    }, 3000);
                });
            });
        });
    </script>
</body>
</html>
