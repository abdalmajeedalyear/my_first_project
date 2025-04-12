# my_first_project<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أمثلة على CSS Transitions</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        
        h1, h2 {
            color: #2c3e50;
            text-align: center;
        }
        
        .example-container {
            background: white;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 30px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .example {
            padding: 20px;
            margin: 15px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .code {
            background: #f8f8f8;
            padding: 10px;
            border-radius: 5px;
            font-family: monospace;
            white-space: pre-wrap;
            margin: 10px 0;
            direction: ltr;
            text-align: left;
        }
        
        /* 1. مثال الانتقال البسيط */
        .simple-transition {
            width: 100px;
            height: 100px;
            background-color: #3498db;
            margin: 0 auto;
            transition: background-color 0.5s ease;
        }
        
        .simple-transition:hover {
            background-color: #e74c3c;
        }
        
        /* 2. تغيير الحجم مع الانتقال */
        .scale-transition {
            width: 100px;
            height: 100px;
            background-color: #2ecc71;
            margin: 0 auto;
            transition: transform 0.4s ease-in-out;
        }
        
        .scale-transition:hover {
            transform: scale(1.2);
        }
        
        /* 3. دوران العنصر */
        .rotate-transition {
            width: 100px;
            height: 100px;
            background-color: #9b59b6;
            margin: 0 auto;
            transition: transform 0.7s ease;
        }
        
        .rotate-transition:hover {
            transform: rotate(180deg);
        }
        
        /* 4. انتقال متعدد الخصائص */
        .multiple-transition {
            width: 100px;
            height: 100px;
            background-color: #f1c40f;
            margin: 0 auto;
            border-radius: 0;
            transition: 
                background-color 0.3s ease,
                border-radius 0.6s ease,
                transform 0.4s ease;
        }
        
        .multiple-transition:hover {
            background-color: #e67e22;
            border-radius: 50%;
            transform: scale(0.8);
        }
        
        /* 5. انتقال مع تأخير */
        .delay-transition {
            width: 100px;
            height: 100px;
            background-color: #1abc9c;
            margin: 0 auto;
            transition: 
                transform 0.5s ease,
                background-color 0.5s ease 0.5s;
        }
        
        .delay-transition:hover {
            transform: translateX(50px);
            background-color: #16a085;
        }
        
        /* 6. انتقال على العنصر عند الظهور */
        .fade-transition {
            width: 100px;
            height: 100px;
            background-color: #e74c3c;
            margin: 0 auto;
            opacity: 0.5;
            transition: opacity 1s ease, box-shadow 0.5s ease;
        }
        
        .fade-transition:hover {
            opacity: 1;
            box-shadow: 0 0 10px rgba(0,0,0,0.3);
        }
        
        /* 7. انتقال على الحدود */
        .border-transition {
            width: 100px;
            height: 100px;
            background-color: #3498db;
            margin: 0 auto;
            border: 2px solid transparent;
            transition: border 0.4s ease;
        }
        
        .border-transition:hover {
            border: 2px solid #2c3e50;
            border-radius: 10px;
        }
        
        /* 8. انتقال بطيء وسريع (توقيت مختلف) */
        .timing-transition {
            width: 200px;
            height: 50px;
            background-color: #34495e;
            margin: 0 auto;
            color: white;
            padding: 10px;
            transition: 
                width 1s ease-in,
                height 1s ease-out,
                background-color 1s linear;
        }
        
        .timing-transition:hover {
            width: 250px;
            height: 70px;
            background-color: #7f8c8d;
        }
    </style>
</head>
<body>
    <h1>أمثلة على CSS Transitions</h1>
    
    <div class="example-container">
        <h2>1. الانتقال البسيط</h2>
        <p>تغيير لون الخلفية عند التحويم</p>
        <div class="example">
            <div class="simple-transition"></div>
        </div>
        <div class="code">
.simple-transition {
    transition: background-color 0.5s ease;
}
.simple-transition:hover {
    background-color: #e74c3c;
}
        </div>
    </div>
    
    <div class="example-container">
        <h2>2. تغيير الحجم مع الانتقال</h2>
        <p>تكبير العنصر عند التحويم</p>
        <div class="example">
            <div class="scale-transition"></div>
        </div>
        <div class="code">
.scale-transition {
    transition: transform 0.4s ease-in-out;
}
.scale-transition:hover {
    transform: scale(1.2);
}
        </div>
    </div>
    
    <div class="example-container">
        <h2>3. دوران العنصر</h2>
        <p>تدوير العنصر 180 درجة عند التحويم</p>
        <div class="example">
            <div class="rotate-transition"></div>
        </div>
        <div class="code">
.rotate-transition {
    transition: transform 0.7s ease;
}
.rotate-transition:hover {
    transform: rotate(180deg);
}
        </div>
    </div>
    
    <div class="example-container">
        <h2>4. انتقال متعدد الخصائص</h2>
        <p>تغيير لون الخلفية، الشكل إلى دائري، وتصغير الحجم</p>
        <div class="example">
            <div class="multiple-transition"></div>
        </div>
        <div class="code">
.multiple-transition {
    transition: 
        background-color 0.3s ease,
        border-radius 0.6s ease,
        transform 0.4s ease;
}
.multiple-transition:hover {
    background-color: #e67e22;
    border-radius: 50%;
    transform: scale(0.8);
}
        </div>
    </div>
    
    <div class="example-container">
        <h2>5. انتقال مع تأخير</h2>
        <p>حركة النقل تأتي أولاً، ثم تغيير اللون بعد نصف ثانية</p>
        <div class="example">
            <div class="delay-transition"></div>
        </div>
        <div class="code">
.delay-transition {
    transition: 
        transform 0.5s ease,
        background-color 0.5s ease 0.5s;
}
.delay-transition:hover {
    transform: translateX(50px);
    background-color: #16a085;
}
        </div>
    </div>
    
    <div class="example-container">
        <h2>6. انتقال على العنصر عند الظهور</h2>
        <p>زيادة الوضوح وإضافة ظل عند التحويم</p>
        <div class="example">
            <div class="fade-transition"></div>
        </div>
        <div class="code">
.fade-transition {
    transition: opacity 1s ease, box-shadow 0.5s ease;
}
.fade-transition:hover {
    opacity: 1;
    box-shadow: 0 0 10px rgba(0,0,0,0.3);
}
        </div>
    </div>
    
    <div class="example-container">
        <h2>7. انتقال على الحدود</h2>
        <p>تغيير الحدود من غير مرئية إلى مرئية مع حواف مدورة</p>
        <div class="example">
            <div class="border-transition"></div>
        </div>
        <div class="code">
.border-transition {
    transition: border 0.4s ease;
}
.border-transition:hover {
    border: 2px solid #2c3e50;
    border-radius: 10px;
}
        </div>
    </div>
    
    <div class="example-container">
        <h2>8. انتقال بطيء وسريع (توقيت مختلف)</h2>
        <p>تغيير العرض ببطء، والارتفاع بسرعة، واللون بتوقيت خطي</p>
        <div class="example">
            <div class="timing-transition">انظر إلى التوقيت</div>
        </div>
        <div class="code">
.timing-transition {
    transition: 
        width 1s ease-in,
        height 1s ease-out,
        background-color 1s linear;
}
.timing-transition:hover {
    width: 250px;
    height: 70px;
    background-color: #7f8c8d;
}
        </div>
    </div>
</body>
</html>
