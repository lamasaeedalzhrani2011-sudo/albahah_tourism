<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل الباحة السياحي التفاعلي</title>
    <style>
        /* التنسيق العام بدرجات الأزرق */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #eef1f6;
            color: #0d2b45;
            margin: 0;
            padding: 0;
        }

        header {
            background: linear-gradient(135deg, #0d2b45 0%, #203c56 100%);
            color: white;
            text-align: center;
            padding: 2.5rem 1rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }

        header h1 { margin: 0; font-size: 2.3rem; font-weight: 700; }
        header p { margin: 0.5rem 0 0 0; color: #9bc53d; font-size: 1.1rem; color: #a3c2dd; }

        /* شريط الخيارات التفاعلي (الأزرار) */
        .nav-tabs {
            display: flex;
            justify-content: center;
            background-color: #203c56;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .tab-btn {
            background: none;
            border: none;
            color: #a3c2dd;
            padding: 15px 25px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
        }

        .tab-btn:hover { color: white; background-color: #2a4d6c; }
        .tab-btn.active { color: white; background-color: #0066cc; border-bottom: 3px solid #66b2ff; }

        .container { max-width: 1100px; margin: 2rem auto; padding: 0 1rem; }

        /* التحكم في عرض الأقسام واختفائها */
        .tab-content { display: none; animation: fadeIn 0.5s ease; }
        .tab-content.active { display: block; }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        /* كروت الأماكن مع الصور */
        .places-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .place-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border: 1px solid #d0daf0;
            transition: transform 0.3s;
        }

        .place-card:hover { transform: translateY(-5px); }
        .place-card img { width: 100%; height: 200px; object-fit: cover; }
        .place-card-body { padding: 1.5rem; }
        .place-card h3 { margin: 0 0 0.5rem 0; color: #004080; }
        .place-card p { margin: 0; line-height: 1.6; color: #4a5568; }

        /* جدول المسافات الخريطة الرقمية */
        table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        th, td { padding: 15px; text-align: right; }
        th { background-color: #0056b3; color: white; }
        tr:nth-child(even) { background-color: #f4f8fc; }

        /* إطار خريطة قوقل المدمجة */
        .map-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            border: 2px solid #0056b3;
        }

        .map-container iframe {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%; border: 0;
        }

        footer { text-align: center; padding: 2rem; background-color: #0d2b45; color: white; margin-top: 4rem; }
    </style>
</head>
<body>

    <header>
        <h1>اكتشفي الباحة التفاعلية</h1>
        <p>دليلكِ السياحي الذكي لأجمل معالم منطقة الضباب</p>
    </header>

    <!-- أزرار التحكم التفاعلية للتبديل بين الصفحات بدون تحميل -->
    <nav class="nav-tabs">
        <button class="tab-btn active" onclick="openTab(event, 'home')">الرئيسية</button>
        <button class="tab-btn" onclick="openTab(event, 'places')">الأماكن السياحية</button>
        <button class="tab-btn" onclick="openTab(event, 'map-section')">الخريطة والمسافات</button>
    </nav>

    <div class="container">

        <!-- القسم الأول: الرئيسية -->
        <div id="home" class="tab-content active">
            <h2>مرحباً بكِ في الباحة</h2>
            <p style="font-size: 1.2rem; line-height: 1.8;">تعتبر منطقة الباحة من أهم الوجهات السياحية في المملكة العربية السعودية، حيث تقع على مرتفعات جبال السروات وتتميز بأجوائها العليلة الباردة، وغاباتها الكثيفة التي يعانقها الضباب، وقراها الأثرية التاريخية الضاربة في عمق التاريخ.</p>
            <p>💡 <em>استخدمي شريط الخيارات في الأعلى للتحول بين الأماكن السياحية واستكشاف دليل الخريطة المباشر.</em></p>
        </div>

        <!-- القسم الثاني: الأماكن السياحية مع الصور -->
        <div id="places" class="tab-content">
            <h2>أبرز المعالم السياحية بالصور</h2>
            <div class="places-grid">
                <div class="place-card">
                    <img src="https://images.unsplash.com/photo-1542273917363-3b1817f69a2d?auto=format&fit=cover&w=600&q=80" alt="غابة رغدان">
                    <div class="place-card-body">
                        <h3>غابة رغدان</h3>
                        <p>تتميز بأشجار العرعر الكثيفة التي تغطي المنحدرات الجبلية، والضباب المستمر، وتوفر مسارات للمشي وجسراً معلقاً لعشاق المغامرة.</p>
                    </div>
                </div>
                <div class="place-card">
                    <img src="https://images.unsplash.com/photo-1590001155093-a3c66ab0c3ff?auto=format&fit=cover&w=600&q=80" alt="قرية ذي عين">
                    <div class="place-card-body">
                        <h3>قرية ذي عين الأثرية</h3>
                        <p>قلعة حجرية تاريخية مذهلة مبنية على جبل من المرو الأبيض، تحيط بها مزارع الموز والكادي وتجري من تحتها عين ماء عذبة لا تنقطع.</p>
                    </div>
                </div>
                <div class="place-card">
                    <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=cover&w=600&q=80" alt="جبل شدا">
                    <div class="place-card-body">
                        <h3>جبل شدا الأعلى</h3>
                        <p>موقع فريد لعشاق الجيولوجيا والطبيعة البكر، يشتهر بوجود مغارات وكهوف صخرية ضخمة تم تحويل بعضها بنجاح إلى نُزل سياحية ريفية.</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- القسم الثالث: الخريطة التفاعلية وجدول الأبعاد -->
        <div id="map-section" class="tab-content">
            <h2>خريطة الباحة ودليل المسافات عن المركز</h2>
            <p>هنا يمكنكِ رؤية خريطة تفاعلية حية لمنطقة الباحة، والاطلاع على بُعد كل موقع عن وسط المدينة بالزمن والمسافة:</p>
            
            <div class="map-container" style="margin-bottom: 2rem;">
                <!-- خريطة حية مدمجة من قوقل مابس لمنطقة الباحة -->
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1m4!1s0x15feab1bbf2eb1d5%3A0x6bde128dc1f6871a!2z2KfZhNio2KfZitipIDY1NTEx!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x15feab1bbf2eb1d5%3A0x6bde128dc1f6871a!2z2KfZhNio2KfZitip!5e0!3m2!1sar!2ssa!4v1718500000000!5m2!1sar!2ssa" allowfullscreen="" loading="lazy"></iframe>
            </div>

            <table>
                <thead>
                    <tr>
                        <th>الموقع السياحي</th>
                        <th>المسافة عن مركز الباحة</th>
                        <th>الزمن التقريبي بالسيارة</th>
                    </tr>
                </thead>
                <tbody>
                    <tr><td><strong>غابة رغدان</strong></td><td>5 كم</td><td>10 دقائق</td></tr>
                    <tr><td><strong>منتزه القيم</strong></td><td>8 كم</td><td>12 دقيقة</td></tr>
                    <tr><td><strong>غابة خيره (شلال جدر)</strong></td><td>20 كم</td><td>25 دقيقة</td></tr>
                    <tr><td><strong>قرية ذي عين الأثرية</strong></td><td>24 كم</td><td>30 دقيقة (عبر العقبة)</td></tr>
                    <tr><td><strong>جبل شدا الأعلى</strong></td><td>65 كم</td><td>ساعة و 10 دقائق</td></tr>
                </tbody>
            </table>
        </div>

    </div>

    <footer>
        <p>تم التطوير بكل حب | تطبيق سياحة الباحة التفاعلي</p>
    </footer>

    <!-- الجزء البرمجي المسؤول عن تشغيل الأزرار والتبديل تفاعلياً -->
    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tablinks;
            tabcontent = document.getElementsByClassName("tab-content");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].classList.remove("active");
            }
            tablinks = document.getElementsByClassName("tab-btn");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].classList.remove("active");
            }
            document.getElementById(tabName).classList.add("active");
            evt.currentTarget.classList.add("active");
        }
    </script>
</body>
</html>
