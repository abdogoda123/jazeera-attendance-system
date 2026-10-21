<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>نظام الحضور الذكي - معهد الجزيرة العالي للهندسة والتكنولوجيا</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800&display=swap" rel="stylesheet">
  <style> body { font-family: 'Cairo', sans-serif; } </style>
</head>
<body class="bg-slate-100 min-h-screen p-4 md:p-8">

  <!-- Header & Official Branding Card -->
  <header class="max-w-4xl mx-auto bg-white rounded-2xl shadow-lg border-t-4 border-[#0088cc] p-6 mb-8 text-center">
    <div class="flex flex-col md:flex-row items-center justify-between gap-4 border-b pb-4 mb-4">
      <div class="flex items-center gap-4">
        <div class="w-20 h-20 bg-slate-50 border rounded-xl p-1 flex items-center justify-center">
          <img src="https://raw.githubusercontent.com/abdogoda123/assets/main/egi-logo.png" alt="EGI Logo" class="max-h-full max-w-full object-contain" onerror="this.src='https://via.placeholder.com/80?text=EGI'">
        </div>
        <div class="text-right">
          <h1 class="text-xl md:text-2xl font-extrabold text-[#0088cc]">AL-JAZEERA HIGHER INSTITUTE</h1>
          <p class="text-xs md:text-sm font-semibold text-slate-600">FOR ENGINEERING AND MODERN TECHNOLOGY</p>
        </div>
      </div>
      <div class="bg-amber-50 border border-amber-200 px-4 py-2 rounded-xl text-center">
        <span class="text-xs font-bold text-amber-700 block">رؤية مصر 2030</span>
        <span class="text-xs text-slate-500 font-medium">التحول الرقمي والذكاء الاصطناعي</span>
      </div>
    </div>
    
    <div class="bg-gradient-to-r from-[#0088cc] to-[#005580] text-white py-3 rounded-xl shadow-inner">
      <h2 class="text-lg font-bold tracking-wide">SMART ATTENDANCE SYSTEM - نظام الحضور الذكي</h2>
    </div>
  </header>

  <!-- Navigation Tabs -->
  <div class="max-w-4xl mx-auto flex justify-center gap-2 mb-6">
    <button onclick="showPage('student')" id="tab-student" class="px-6 py-2.5 rounded-xl font-bold bg-[#0088cc] text-white shadow-md transition">صفحة الطالب</button>
    <button onclick="showPage('doctor')" id="tab-doctor" class="px-6 py-2.5 rounded-xl font-bold bg-white text-slate-700 shadow hover:bg-slate-50 transition">صفحة الدكتور / المعيد</button>
    <button onclick="showPage('reports')" id="tab-reports" class="px-6 py-2.5 rounded-xl font-bold bg-white text-slate-700 shadow hover:bg-slate-50 transition">تقارير الطالب</button>
  </div>

  <!-- 1. STUDENT PAGE -->
  <main id="page-student" class="max-w-xl mx-auto bg-white rounded-2xl shadow-xl p-6 md:p-8">
    <div class="flex items-center gap-3 mb-6 pb-3 border-b">
      <span class="text-2xl">👤</span>
      <div>
        <h3 class="text-lg font-bold text-slate-800">تسجيل حضور طالب</h3>
        <p class="text-xs text-slate-500">يرجى التأكد من تشغيل الموقع الجغرافي GPS</p>
      </div>
    </div>

    <form onsubmit="event.preventDefault();" class="space-y-4">
      <div>
        <label class="block text-xs font-bold text-slate-700 mb-1">الاسم الثلاثي / الرباعي</label>
        <input type="text" value="عبدالرحمن جودة منصور" class="w-full px-4 py-2.5 rounded-xl border border-slate-300 focus:ring-2 focus:ring-[#0088cc] focus:outline-none text-sm font-semibold">
      </div>

      <div class="grid grid-cols-2 gap-4">
        <div>
          <label class="block text-xs font-bold text-slate-700 mb-1">الرقم الأكاديمي (ID)</label>
          <input type="text" value="202401928" class="w-full px-4 py-2.5 rounded-xl border border-slate-300 focus:ring-2 focus:ring-[#0088cc] focus:outline-none text-sm font-semibold">
        </div>
        <div>
          <label class="block text-xs font-bold text-slate-700 mb-1">المستوى الدراسي</label>
          <select class="w-full px-4 py-2.5 rounded-xl border border-slate-300 focus:ring-2 focus:ring-[#0088cc] focus:outline-none text-sm font-semibold">
            <option>المستوى الثالث (3/2)</option>
            <option>المستوى الأول</option>
            <option>المستوى الثاني</option>
            <option>المستوى الرابع</option>
            <option>المستوى الخامس</option>
          </select>
        </div>
      </div>

      <div>
        <label class="block text-xs font-bold text-slate-700 mb-1">القسم / التخصص</label>
        <select class="w-full px-4 py-2.5 rounded-xl border border-slate-300 focus:ring-2 focus:ring-[#0088cc] focus:outline-none text-sm font-semibold">
          <option>هندسة الاتصالات والإلكترونيات (Electronics & Comms)</option>
          <option>إعدادي هندسة (Preparatory)</option>
          <option>هندسة مدنية (Civil Engineering)</option>
          <option>هندسة معمارية (Architectural Engineering)</option>
        </select>
      </div>

      <div class="pt-4 space-y-3">
        <button class="w-full bg-[#0088cc] hover:bg-[#0077bb] text-white py-3.5 rounded-xl font-bold shadow-lg shadow-blue-500/30 flex items-center justify-center gap-2 transition">
          <span>📷</span> فتح الكاميرا ومسح الـ QR Code
        </button>
        <button onclick="showPage('reports')" class="w-full bg-slate-100 hover:bg-slate-200 text-slate-700 py-3 rounded-xl font-bold flex items-center justify-center gap-2 transition text-sm">
          <span>📊</span> عرض سجلي وتقارير الحضور الخاصة بي
        </button>
      </div>
    </form>
  </main>

  <!-- 2. DOCTOR PAGE -->
  <main id="page-doctor" class="max-w-2xl mx-auto bg-white rounded-2xl shadow-xl p-6 md:p-8 hidden">
    <div class="flex items-center justify-between mb-6 pb-3 border-b">
      <div class="flex items-center gap-3">
        <span class="text-2xl">👨‍🏫</span>
        <div>
          <h3 class="text-lg font-bold text-slate-800">شاشة المحاضر / عضو هيئة التدريس</h3>
          <p class="text-xs text-slate-500">الحساب الحالي: admin1 (د. أحمد منصور)</p>
        </div>
      </div>
      <span class="px-3 py-1 bg-green-100 text-green-700 font-bold text-xs rounded-full">جلسة نشطة #108</span>
    </div>

    <div class="bg-slate-50 border-2 border-dashed border-slate-300 rounded-2xl p-6 text-center mb-6">
      <div class="inline-block bg-white p-4 rounded-2xl shadow-md border mb-3">
        <div id="qr-box" class="w-48 h-48 bg-slate-900 rounded-xl flex items-center justify-center text-white font-mono text-xs p-2 text-center transition-all duration-300">
          <div>
            <div class="text-2xl mb-1">🏁</div>
            <div>DYNAMIC QR CODE</div>
            <div class="text-[10px] text-amber-400 mt-1" id="qr-token">TOKEN: A8X9-2026</div>
          </div>
        </div>
      </div>
      <div class="flex items-center justify-center gap-2 text-sm font-bold text-slate-700 mb-2">
        <span>⏱️ يتغير الكود تلقائياً خلال:</span>
        <span id="timer" class="text-red-600 font-mono text-lg">3</span> ثوانٍ
      </div>
      <p class="text-xs text-slate-500">نظام حماية الموقع الجغرافي (GPS Geofence) مفعّل داخل حرم المعهد</p>
    </div>

    <div class="grid grid-cols-2 gap-4 mb-6">
      <div class="bg-blue-50 border border-blue-200 p-4 rounded-xl text-center">
        <span class="text-xs text-slate-500 font-bold block mb-1">المادة الحالية</span>
        <span class="text-sm font-extrabold text-[#0088cc]">تحليل متجهات (Vector Analysis)</span>
      </div>
      <div class="bg-green-50 border border-green-200 p-4 rounded-xl text-center">
        <span class="text-xs text-slate-500 font-bold block mb-1">عدد الحاضرين الآن</span>
        <span class="text-xl font-black text-green-600">42 طالب</span>
      </div>
    </div>

    <div class="flex gap-3">
      <button class="flex-1 bg-red-600 hover:bg-red-700 text-white py-3 rounded-xl font-bold shadow transition">إغلاق المحاضرة</button>
      <button class="flex-1 bg-emerald-600 hover:bg-emerald-700 text-white py-3 rounded-xl font-bold shadow transition flex items-center justify-center gap-2">
        <span>📥</span> تصدير الحضور Excel
      </button>
    </div>
  </main>

  <!-- 3. REPORTS PAGE -->
  <main id="page-reports" class="max-w-3xl mx-auto bg-white rounded-2xl shadow-xl p-6 md:p-8 hidden">
    <div class="flex items-center justify-between mb-6 pb-3 border-b">
      <div>
        <h3 class="text-lg font-bold text-slate-800">تقرير الحضور الأكاديمي الشامل</h3>
        <p class="text-xs text-slate-500">الطالب: عبدالرحمن جودة منصور | ID: 202401928</p>
      </div>
      <span class="px-3 py-1 bg-blue-100 text-[#0088cc] font-bold text-xs rounded-full">نسبة الحضور العادي: 92%</span>
    </div>

    <div class="overflow-x-auto">
      <table class="w-full text-right text-sm">
        <thead>
          <tr class="bg-slate-100 text-slate-700">
            <th class="p-3 rounded-r-xl">المادة</th>
            <th class="p-3">الدكتور / المعيد</th>
            <th class="p-3 text-center">المحاضرات</th>
            <th class="p-3 text-center">الحالة</th>
          </tr>
        </thead>
        <tbody class="divide-y text-slate-700 font-medium">
          <tr>
            <td class="p-3 font-bold text-slate-900">تحليل متجهات</td>
            <td class="p-3">د. أحمد منصور (admin1)</td>
            <td class="p-3 text-center font-mono">6/6</td>
            <td class="p-3 text-center"><span class="px-2 py-0.5 bg-green-100 text-green-700 rounded-full text-xs font-bold">ممتاز (100%)</span></td>
          </tr>
          <tr>
            <td class="p-3 font-bold text-slate-900">خرسانة مسلحة</td>
            <td class="p-3">د. محمد علي (admin2)</td>
            <td class="p-3 text-center font-mono">5/6</td>
            <td class="p-3 text-center"><span class="px-2 py-0.5 bg-green-100 text-green-700 rounded-full text-xs font-bold">جيد جداً (83%)</span></td>
          </tr>
        </tbody>
      </table>
    </div>
  </main>

  <script>
    function showPage(pageId) {
      document.getElementById('page-student').classList.add('hidden');
      document.getElementById('page-doctor').classList.add('hidden');
      document.getElementById('page-reports').classList.add('hidden');
      document.getElementById('page-' + pageId).classList.remove('hidden');

      const tabs = ['student', 'doctor', 'reports'];
      tabs.forEach(tab => {
        const btn = document.getElementById('tab-' + tab);
        if(tab === pageId) {
          btn.className = "px-6 py-2.5 rounded-xl font-bold bg-[#0088cc] text-white shadow-md transition";
        } else {
          btn.className = "px-6 py-2.5 rounded-xl font-bold bg-white text-slate-700 shadow hover:bg-slate-50 transition";
        }
      });
    }

    let timeLeft = 3;
    setInterval(() => {
      timeLeft--;
      if (timeLeft < 1) {
        timeLeft = 3;
        const randomToken = 'TOKEN-' + Math.random().toString(36).substring(2, 7).toUpperCase();
        const qrTokenEl = document.getElementById('qr-token');
        if(qrTokenEl) qrTokenEl.innerText = randomToken;
      }
      const timerEl = document.getElementById('timer');
      if(timerEl) timerEl.innerText = timeLeft;
    }, 1000);
  </script>
</body>
</html>
