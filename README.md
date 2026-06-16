<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>السياحة في الباحة</title>
    <style>
        /* تنسيق الألوان بدرجات الأزرق */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f7fc; /* أزرق ثلجي فاتح جداً للخلفية */
            color: #012a4a; /* أزرق داكن جداً للنصوص */
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #014f86; /* أزرق عميق */
            color: white;
            text-align: center;
            padding: 2rem;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        header h1 {
            margin: 0;
            font-size: 2.5rem;
        }

        header p {
            margin: 0.5rem 0 0 0;
            font-size: 1.2rem;
            color: #a9d6e5; /* أزرق سماوي فاتح */
        }

        .container {
            max-width: 1000px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        h2 {
            color: #2a6f97; /* أزرق متوسط */
            border-bottom: 2px solid #014f86;
            padding-bottom: 0.5rem;
        }

        /* تنسيق كروت الأماكن السياحية */
        .places-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .place-card {
            background-color: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 4px 15px rgba(1, 79, 134, 0.1);
            border-top: 5px solid #2a6f97;
            transition: transform 0.3s;
        }

        .place-card:hover {
            transform: translateY(-5px);
        }

        .place-card h3 {
            margin-top: 0;
            color: #014f86;
        }

        /* تنسيق جدول المسافات (الخريطة التوضيحية) */
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1rem;
            background-color: white;
            box-shadow: 0 4px 15px rgba(1, 79, 134, 0.05);
            border-radius: 8px;
            overflow: hidden;
        }

        th, td {
            padding: 12px 15px;
            text-align: right;
        }

        th {
            background-color: #2a6f97;
            color: white;
            font-weight: bold;
        }

        tr:nth-child(even) {
            background-color: #e6f2ff; /* تموج أزرق خفيف للمصفوفات */
        }

        tr:hover {
            background-color: #d0e7ff;
        }

        footer {
            text-align: center;
            padding: 1.5rem;
            background-color: #012a4a;
            color: white;
            margin-top: 4rem;
        }
    </style>
</head>
<body>

    <header>
        <h1>سحر الباحة</h1>
        <p>دليلك السياحي لأجمل مناطق الضباب والخضرة في المملكة</p>
    </header>

    <div class="container">
        
        <section>
            <h2>أبرز الأماكن السياحية</h2>
            <div class="places-grid">
                <div class="place-card">
                    <h3>غابة رغدان</h3>
                    <p>من أشهر غابات الوطن العربي، تتميز بأشجار العرعر الكثيفة والضباب الذي يداعب القمم، وبها جسر معلق وممرات جميلة للمشي.</p>
                </div>
                <div class="place-card">
                    <h3>قرية ذي عين الأثرية</h3>
                    <p>قرية تاريخية مبنية من الحجارة البيضاء على قمة جبل من المرو الأسود، وتشتهر بزراعة الموز والكادي ووجود عين ماء عذبة جارية.</p>
                </div>
                <div class="place-card">
                    <h3>جبل شدا الأعلى</h3>
                    <p>موقع فريد لعشاق الطبيعة والجيولوجيا، يتميز بتشكيلاته الصخرية العجيبة وكهوفه المحورة التي تحولت إلى نزل سياحية فريدة.</p>
                </div>
            </div>
        </section>

        <section>
            <h2>دليل المسافات (البُعد عن مركز مدينة الباحة)</h2>
            <p>جدول توضيحي يسهل عليكِ تخطيط رحلتكِ بناءً على المسافة والزمن من وسط المدينة:</p>
            
            <table>
                <thead>
                    <tr>
                        <th>الموقع السياحي</th>
                        <th>المسافة التقريبية (كم)</th>
                        <th>الزمن المتوقع بالسيارة</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>غابة رغدان</strong></td>
                        <td>5 كم</td>
                        <td>10 دقائق</td>
                    </tr>
                    <tr>
                        <td><strong>منتزه القيم</strong></td>
                        <td>8 كم</td>
                        <td>12 دقيقة</td>
                    </tr>
                    <tr>
                        <td><strong>غابة خيره (شلال جدر)</strong></td>
                        <td>20 كم</td>
                        <td>25 دقيقة</td>
                    </tr>
                    <tr>
                        <td><strong>قرية ذي عين الأثرية</strong></td>
                        <td>24 كم</td>
                        <td>30 دقيقة (نزولاً عبر العقبة)</td>
                    </tr>
                    <tr>
                        <td><strong>جبل شدا الأعلى</strong></td>
                        <td>65 كم</td>
                        <td>ساعة و 10 دقائق</td>
                    </tr>
                </tbody>
            </table>
        </section>

    </div>

    <footer>
        <p>تم التطوير بكل حب | سياحة الباحة عبر GitHub Pages</p>
    </footer>

</body>
</html>
