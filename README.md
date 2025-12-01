# behavioral-biometrics-demo[index.html](https://github.com/user-attachments/files/23863378/index.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نموذج البصمة السلوكية</title>

<!-- أيقونات -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
/* ثيم الألوان */
:root {
  --main: #4A00E0;
  --secondary: #8E2DE2;
  --bg: #f6f5fb;
}

/* تنسيق عام */
body {
  font-family: "Tajawal", sans-serif;
  background: var(--bg);
  margin: 0;
  padding: 0;
}

/* حركة بسيطة */
.fade-in {
  animation: fadeIn 0.9s ease forwards;
  opacity: 0;
}
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

/* كارد */
.card {
  background: white;
  padding: 25px;
  margin: 20px auto;
  width: 85%;
  max-width: 500px;
  border-radius: 14px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
}

/* عنوان */
.title {
  text-align: center;
  font-size: 24px;
  font-weight: 700;
  color: var(--main);
}

/* زر */
button {
  width: 100%;
  padding: 12px;
  border: none;
  border-radius: 10px;
  background: var(--main);
  color: white;
  font-size: 16px;
  cursor: pointer;
  transition: 0.2s;
}
button:hover {
  background: var(--secondary);
}

/* لوقو بسيط */
.logo {
  display: block;
  margin: 25px auto 10px auto;
  font-size: 45px;
  color: var(--main);
}
</style>

</head>
<body>

<!-- لوجو -->
<i class="fa-solid fa-fingerprint logo fade-in"></i>

<!-- عنوان -->
<h2 class="title fade-in">نموذج البصمة السلوكية - Behavioral ID</h2>

<!-- كارد تسجيل الدخول -->
<div class="card fade-in">
  <h3 style="margin-top:0;">تجربة تسجيل الدخول</h3>
  <p>قم بمحاكاة طريقة تسجيل دخول المستخدم بناءً على بصمته السلوكية.</p>

  <label>اسم المستخدم</label>
  <input type="text" style="width:100%; padding:10px; margin:8px 0; border:1px solid #ddd; border-radius:8px;">

  <label>التحقق السلوكي</label>
  <input type="text" placeholder="محاكاة الكتابة..." 
         style="width:100%; padding:10px; margin:8px 0; border:1px solid #ddd; border-radius:8px;">

  <button onclick="demo()">تحقق من البصمة السلوكية</button>
</div>

<!-- كارد النتيجة -->
<div class="card fade-in" id="result" style="display:none;">
  <h3 style="margin-top:0;">النتيجة</h3>
  <p id="result-text"></p>
</div>

<script>
function demo() {
  document.getElementById("result").style.display = "block";
  document.getElementById("result-text").innerHTML =
    "✔️ تمت مطابقة البصمة السلوكية بنجاح.<br>المستخدم موثوق بنسبة 94%";
}
</script>

</body>
</html>
