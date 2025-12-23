<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>أداة التقارير التعليمية | وزارة التعليم</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --primary: #083024;
  --primary-light: #0a3c2d;
  --secondary: #059669;
  --secondary-dark: #047857;
  --accent: #d97706;
  --light: #f8fafc;
  --dark: #1f2937;
  --gray: #6b7280;
  --light-gray: #e5e7eb;
  --danger: #dc2626;
  --success: #059669;
  --warning: #d97706;
  --border-radius: 8px;
  --box-shadow: 0 2px 4px -1px rgba(0, 0, 0, 0.1);
  --box-shadow-hover: 0 5px 10px -3px rgba(0, 0, 0, 0.1);
  --transition: all 0.2s ease;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  -webkit-tap-highlight-color: transparent;
}

body {
  font-family: 'Cairo', sans-serif;
  background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
  color: var(--dark);
  line-height: 1.6;
  min-height: 100vh;
  padding: 0;
  overflow-x: hidden;
}

/* تحسينات للأجهزة المحمولة */
@media (max-width: 768px) {
  body {
    font-size: 14px;
    -webkit-text-size-adjust: 100%;
  }
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 10px;
}

/* الهيدر مع خلفية شعار وزارة التعليم */
.header {
  background: white url('https://i.ibb.co/kVWFFwhW/9-C92-E57-B-23-FA-479-D-A024-1-D5-F871-B4-F8-D.png') center/contain no-repeat;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: 10px 15px;
  margin-bottom: 10px;
  display: flex;
  flex-direction: column;
  gap: 10px;
  border-right: 3px solid var(--primary);
  position: relative;
  min-height: 100px;
}

.header::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background: rgba(255, 255, 255, 0.9);
  border-radius: var(--border-radius);
  z-index: 1;
}

.header > * {
  position: relative;
  z-index: 2;
}

.header-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 8px;
}

.header-bottom {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

@media (max-width: 480px) {
  .header-top {
    flex-direction: column;
    text-align: center;
  }
  
  .header-bottom {
    flex-direction: column;
  }
}

.logo-section {
  display: flex;
  align-items: center;
  gap: 10px;
}

.logo-icon {
  width: 40px;
  height: 40px;
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 20px;
  flex-shrink: 0;
}

.logo-text h1 {
  font-size: 16px;
  font-weight: 700;
  color: var(--dark);
  margin-bottom: 2px;
  line-height: 1.2;
}

.logo-text p {
  font-size: 12px;
  color: var(--gray);
  line-height: 1.3;
}

/* زر القائمة للجوال */
.mobile-menu-btn {
  display: none;
  background: none;
  border: none;
  color: var(--primary);
  font-size: 20px;
  cursor: pointer;
  padding: 5px;
}

@media (max-width: 768px) {
  .mobile-menu-btn {
    display: block;
  }
}

/* شريط التنقل السفلي للجوال */
.mobile-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: white;
  box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  padding: 8px 5px;
  display: none;
  justify-content: space-around;
  backdrop-filter: blur(10px);
}

@media (max-width: 768px) {
  .mobile-nav {
    display: flex;
  }
  
  .container {
    padding-bottom: 70px;
  }
}

.nav-btn {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 3px;
  background: none;
  border: none;
  color: var(--gray);
  font-size: 10px;
  padding: 5px 3px;
  cursor: pointer;
  flex: 1;
  min-width: 0;
  transition: var(--transition);
}

.nav-btn.active {
  color: var(--primary);
}

.nav-btn i {
  font-size: 14px;
}

.nav-btn:hover {
  transform: translateY(-2px);
}

/* المحتوى الرئيسي */
.main-content {
  display: grid;
  grid-template-columns: 1fr;
  gap: 10px;
}

@media (min-width: 1024px) {
  .main-content {
    grid-template-columns: 1fr 300px;
  }
}

/* لوحة التحكم */
.control-panel {
  background: white;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: 15px;
  height: fit-content;
  position: sticky;
  top: 10px;
}

@media (max-width: 1024px) {
  .control-panel {
    position: static;
    order: 2;
  }
}

/* القوالب السريعة */
.quick-templates {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
  gap: 8px;
  margin-bottom: 15px;
}

@media (max-width: 480px) {
  .quick-templates {
    grid-template-columns: 1fr;
  }
}

.template-btn {
  background: white;
  border: 1px solid var(--light-gray);
  border-radius: 6px;
  padding: 8px;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 6px;
  text-align: center;
  min-height: 70px;
  justify-content: center;
}

.template-btn:hover {
  border-color: var(--primary);
  transform: translateY(-1px);
  box-shadow: var(--box-shadow-hover);
}

.template-btn i {
  font-size: 16px;
  color: var(--primary);
}

.template-btn span {
  font-size: 11px;
  font-weight: 500;
}

/* أزرار العمل */
.action-buttons {
  display: flex;
  flex-direction: column;
  gap: 8px;
  margin-top: 15px;
}

.action-btn {
  padding: 10px;
  border: none;
  border-radius: 6px;
  font-family: 'Cairo', sans-serif;
  font-size: 13px;
  font-weight: 600;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
}

.action-btn-primary {
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  color: white;
}

.action-btn-primary:hover {
  transform: translateY(-1px);
  box-shadow: var(--box-shadow-hover);
}

.action-btn-secondary {
  background: white;
  color: var(--primary);
  border: 1px solid var(--primary);
}

.action-btn-secondary:hover {
  background: var(--primary);
  color: white;
}

.action-btn-success {
  background: linear-gradient(135deg, var(--success), var(--secondary-dark));
  color: white;
}

.action-btn-success:hover {
  transform: translateY(-1px);
  box-shadow: var(--box-shadow-hover);
}

/* نموذج الإدخال */
.form-container {
  background: white;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  overflow: hidden;
}

.form-header {
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  color: white;
  padding: 12px 15px;
}

.form-header h2 {
  font-size: 16px;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 8px;
}

.form-content {
  padding: 15px;
}

/* تحسينات للحقول في الجوال */
.form-section {
  margin-bottom: 15px;
}

.form-section-title {
  font-size: 14px;
  font-weight: 600;
  color: var(--dark);
  margin-bottom: 10px;
  padding-bottom: 5px;
  border-bottom: 1px solid var(--light-gray);
  display: flex;
  align-items: center;
  gap: 6px;
}

.form-section-title i {
  color: var(--primary);
  font-size: 14px;
}

.form-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 10px;
}

@media (max-width: 768px) {
  .form-grid {
    grid-template-columns: 1fr;
  }
}

.form-group {
  margin-bottom: 10px;
}

.form-label {
  display: block;
  font-size: 12px;
  font-weight: 600;
  color: var(--dark);
  margin-bottom: 5px;
  display: flex;
  align-items: center;
  gap: 6px;
}

.form-label i {
  color: var(--primary);
  font-size: 12px;
}

.form-control {
  width: 100%;
  padding: 8px 10px;
  border: 1px solid var(--light-gray);
  border-radius: 6px;
  font-family: 'Cairo', sans-serif;
  font-size: 13px;
  color: var(--dark);
  transition: var(--transition);
  background: white;
  -webkit-appearance: none;
}

/* مربعات المحتوى */
.objective-box {
  background: rgba(8, 48, 36, 0.1);
  color: var(--primary);
  padding: 12px;
  border-radius: var(--border-radius);
  text-align: center;
  margin-bottom: 12px;
  border: 1px solid rgba(8, 48, 36, 0.3);
  max-width: 100%;
}

.objective-box h3 {
  font-size: 14px;
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
}

.objective-box textarea {
  background: rgba(255, 255, 255, 0.9);
  color: #1f2937;
  border: 1px solid rgba(8, 48, 36, 0.3);
  border-radius: 6px;
  padding: 8px;
  font-size: 13px;
  text-align: center;
  min-height: 60px;
  max-width: 100%;
  resize: vertical;
  line-height: 1.4;
}

.row-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 8px;
  margin-bottom: 8px;
}

@media (max-width: 768px) {
  .row-grid {
    grid-template-columns: 1fr;
  }
}

.content-box {
  padding: 10px;
  border-radius: var(--border-radius);
  border: 1px solid;
  min-height: 120px;
  display: flex;
  flex-direction: column;
  background: rgba(255, 255, 255, 0.9);
}

.content-box textarea {
  width: 100%;
  flex: 1;
  border: none;
  background: none;
  resize: vertical;
  font-family: 'Cairo', sans-serif;
  font-size: 12px;
  line-height: 1.4;
  color: #1f2937;
  padding: 4px;
  max-height: 150px;
  min-height: 80px;
}

.content-box textarea:focus {
  outline: none;
}

.box-title {
  font-size: 13px;
  font-weight: 600;
  margin-bottom: 6px;
  display: flex;
  align-items: center;
  gap: 6px;
  padding-bottom: 5px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.box-title i {
  font-size: 14px;
}

/* ألوان شفافة للمربعات */
.steps-box {
  border-color: rgba(8, 48, 36, 0.3);
}

.steps-box .box-title {
  color: var(--primary);
}

.results-box {
  border-color: rgba(217, 119, 6, 0.3);
}

.results-box .box-title {
  color: #92400e;
}

.recommendations-box {
  border-color: rgba(29, 78, 216, 0.3);
}

.recommendations-box .box-title {
  color: #1e40af;
}

.strengths-box {
  border-color: rgba(5, 150, 105, 0.3);
}

.strengths-box .box-title {
  color: #065f46;
}

.improvements-box {
  border-color: rgba(234, 88, 12, 0.3);
  margin-top: 8px;
}

.improvements-box .box-title {
  color: #9a3412;
}

/* منطقة رفع الصور */
.upload-section {
  margin-top: 12px;
}

.upload-area {
  border: 1px dashed var(--light-gray);
  border-radius: 6px;
  padding: 12px;
  text-align: center;
  cursor: pointer;
  transition: var(--transition);
  margin-bottom: 10px;
  background: #f9fafb;
}

.upload-area:hover {
  border-color: var(--primary);
  background: #f3f4f6;
}

.upload-area i {
  font-size: 30px;
  color: var(--primary);
  margin-bottom: 6px;
}

.upload-area p {
  color: var(--gray);
  margin-bottom: 3px;
  font-size: 13px;
}

.upload-area small {
  font-size: 11px;
  color: var(--gray);
}

.image-preview {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
  gap: 8px;
  margin-top: 10px;
}

.preview-image {
  position: relative;
  border-radius: 6px;
  overflow: hidden;
  height: 80px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
}

.preview-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.remove-image {
  position: absolute;
  top: 3px;
  left: 3px;
  background: rgba(220, 38, 38, 0.9);
  color: white;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: var(--transition);
  font-size: 10px;
}

.remove-image:hover {
  background: var(--danger);
}

/* التوقيعات */
.signatures-section {
  background: #f9fafb;
  border-radius: 6px;
  padding: 12px;
  margin-top: 12px;
}

.signatures-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 12px;
}

@media (max-width: 480px) {
  .signatures-grid {
    grid-template-columns: 1fr;
  }
}

.signature-field {
  text-align: center;
}

.signature-input {
  width: 100%;
  padding: 8px;
  border: 1px solid var(--light-gray);
  border-radius: 6px;
  font-family: 'Cairo', sans-serif;
  font-size: 13px;
  text-align: center;
  background: white;
  margin-top: 5px;
}

/* نافذة المعاينة */
.preview-overlay {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.9);
  display: none;
  align-items: center;
  justify-content: center;
  z-index: 2000;
  padding: 10px;
  backdrop-filter: blur(5px);
}

.preview-container {
  background: white;
  border-radius: var(--border-radius);
  width: 100%;
  max-width: 800px;
  max-height: 90vh;
  overflow-y: auto;
  position: relative;
  animation: slideIn 0.3s ease;
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.preview-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 15px;
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  color: white;
  position: sticky;
  top: 0;
  z-index: 1;
}

.close-preview {
  background: none;
  border: none;
  color: white;
  font-size: 18px;
  cursor: pointer;
  padding: 4px;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.close-preview:hover {
  background: rgba(255, 255, 255, 0.2);
}

/* شاشة التحميل */
.loading-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.9);
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  z-index: 3000;
  color: white;
  font-size: 16px;
  text-align: center;
  padding: 15px;
}

.loading-spinner {
  width: 40px;
  height: 40px;
  border: 2px solid rgba(255, 255, 255, 0.3);
  border-top-color: white;
  border-radius: 50%;
  animation: spin 1s linear infinite;
  margin-bottom: 15px;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

/* تحسينات للتمرير */
::-webkit-scrollbar {
  width: 6px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 3px;
}

::-webkit-scrollbar-thumb {
  background: var(--primary);
  border-radius: 3px;
}

::-webkit-scrollbar-thumb:hover {
  background: var(--primary-light);
}

/* رسائل التنبيه */
.alert {
  padding: 8px 10px;
  border-radius: 6px;
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 12px;
  animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-8px); }
  to { opacity: 1; transform: translateY(0); }
}

.alert-success {
  background: #d1fae5;
  color: #065f46;
  border-right: 3px solid var(--success);
}

.alert-warning {
  background: #fef3c7;
  color: #92400e;
  border-right: 3px solid var(--warning);
}

.alert-error {
  background: #fee2e2;
  color: #991b1b;
  border-right: 3px solid var(--danger);
}

.alert-info {
  background: #dbeafe;
  color: #1e40af;
  border-right: 3px solid var(--primary);
}

/* حدود 250 حرف */
.char-count {
  font-size: 11px;
  color: var(--gray);
  text-align: left;
  margin-top: 3px;
}

/* تحسينات عامة */
.form-control::placeholder {
  font-size: 11px;
}

textarea.form-control::placeholder {
  font-size: 11px;
}

.signature-input::placeholder {
  font-size: 11px;
}

.form-group + .form-group {
  margin-top: 5px;
}

.row-grid + .row-grid {
  margin-top: 5px;
}

.content-box + .content-box {
  margin-top: 5px;
}

.fa-lg {
  font-size: 1.2em;
}

.form-content > * {
  margin-bottom: 8px;
}
</style>
</head>
<body>
<div class="container">
  <!-- الهيدر -->
  <header class="header">
    <div class="header-top">
      <div class="logo-section">
        <div class="logo-icon">
          <i class="fas fa-graduation-cap"></i>
        </div>
        <div class="logo-text">
          <h1>أداة التقارير التعليمية</h1>
          <p>وزارة التعليم - نظام إعداد التقارير الذكي</p>
        </div>
      </div>
      <button class="mobile-menu-btn" onclick="toggleMenu()">
        <i class="fas fa-bars"></i>
      </button>
    </div>
    
    <div class="header-bottom">
      <div class="alert alert-success">
        <i class="fas fa-check-circle"></i>
        <span>جميع البيانات مؤمنة ومشفرة</span>
      </div>
      <div class="alert alert-info">
        <i class="fas fa-mobile-alt"></i>
        <span>متوافق مع جميع الأجهزة</span>
      </div>
    </div>
  </header>

  <!-- المحتوى الرئيسي -->
  <div class="main-content">
    <!-- نموذج الإدخال -->
    <main class="form-container">
      <div class="form-header">
        <h2><i class="fas fa-edit"></i> إعداد تقرير جديد</h2>
      </div>

      <div class="form-content">
        <!-- معلومات المدرسة -->
        <div class="form-section">
          <h3 class="form-section-title">
            <i class="fas fa-school"></i>
            معلومات المدرسة
          </h3>
          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-university"></i>
                اسم المدرسة
              </label>
              <input type="text" class="form-control" id="school-name" 
                     placeholder="أدخل اسم المدرسة الكامل" required>
            </div>
            
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-map-marker-alt"></i>
                إدارة التعليم
              </label>
              <select class="form-control" id="education-department">
                <option value="">اختر إدارة التعليم</option>
                <option value="الرياض">الإدارة العامة للتعليم بمنطقة الرياض</option>
                <option value="مكة">الإدارة العامة للتعليم بمنطقة مكة المكرمة</option>
                <option value="الشرقية">الإدارة العامة للتعليم بالمنطقة الشرقية</option>
                <option value="المدينة">الإدارة العامة للتعليم بمنطقة المدينة المنورة</option>
              </select>
            </div>
          </div>
        </div>

        <!-- الهدف التربوي -->
        <div class="objective-box">
          <h3><i class="fas fa-bullseye"></i> الهدف التربوي</h3>
          <textarea class="form-control" id="educational-goal" 
                    placeholder="صغ الهدف التربوي من النشاط..." 
                    rows="2" required maxlength="250"></textarea>
          <div class="char-count"><span id="goal-chars">0</span>/250 حرف</div>
        </div>

        <!-- إجراءات التنفيذ والنتائج المتحققة -->
        <div class="row-grid">
          <div class="content-box steps-box">
            <div class="box-title">
              <i class="fas fa-tasks"></i>
              إجراءات التنفيذ
            </div>
            <textarea id="implementation-steps" 
                      placeholder="صف خطوات التنفيذ بالتفصيل..." 
                      maxlength="250"></textarea>
            <div class="char-count"><span id="steps-chars">0</span>/250 حرف</div>
          </div>
          
          <div class="content-box results-box">
            <div class="box-title">
              <i class="fas fa-chart-line"></i>
              النتائج المتحققة
            </div>
            <textarea id="achieved-results" 
                      placeholder="ما هي النتائج التي تحققت؟" 
                      maxlength="250"></textarea>
            <div class="char-count"><span id="results-chars">0</span>/250 حرف</div>
          </div>
        </div>

        <!-- التوصيات ونقاط القوة -->
        <div class="row-grid">
          <div class="content-box recommendations-box">
            <div class="box-title">
              <i class="fas fa-comments"></i>
              التوصيات والمقترحات
            </div>
            <textarea id="recommendations" 
                      placeholder="ما هي توصياتك للمستقبل؟" 
                      maxlength="250"></textarea>
            <div class="char-count"><span id="recommendations-chars">0</span>/250 حرف</div>
          </div>
          
          <div class="content-box strengths-box">
            <div class="box-title">
              <i class="fas fa-thumbs-up"></i>
              نقاط القوة
            </div>
            <textarea id="strengths" 
                      placeholder="ما هي نقاط القوة في النشاط؟" 
                      maxlength="250"></textarea>
            <div class="char-count"><span id="strengths-chars">0</span>/250 حرف</div>
          </div>
        </div>

        <!-- فرص التحسين -->
        <div class="content-box improvements-box">
          <div class="box-title">
            <i class="fas fa-lightbulb"></i>
            فرص التحسين
          </div>
          <textarea id="improvements" 
                    placeholder="ما هي فرص التحسين؟" 
                    maxlength="250"></textarea>
          <div class="char-count"><span id="improvements-chars">0</span>/250 حرف</div>
        </div>

        <!-- معلومات إضافية -->
        <div class="form-grid" style="margin-top: 12px;">
          <div class="form-group">
            <label class="form-label">
              <i class="fas fa-users"></i>
              الفئة المستهدفة
            </label>
            <input type="text" class="form-control" id="target-audience" 
                   placeholder="مثال: طلاب الصف الثالث الثانوي">
          </div>
          
          <div class="form-group">
            <label class="form-label">
              <i class="fas fa-book"></i>
              المادة الدراسية
            </label>
            <input type="text" class="form-control" id="subject" 
                   placeholder="مثال: الرياضيات">
          </div>
          
          <div class="form-group">
            <label class="form-label">
              <i class="fas fa-map-pin"></i>
              مكان التنفيذ
            </label>
            <input type="text" class="form-control" id="execution-place" 
                   placeholder="مثال: مختبر البحث">
          </div>
        </div>

        <!-- الصور التوثيقية -->
        <div class="upload-section">
          <h3 class="form-section-title">
            <i class="fas fa-images"></i>
            الصور التوثيقية (صورتين كحد أقصى)
          </h3>
          
          <div class="upload-area" onclick="document.getElementById('image-upload').click()">
            <i class="fas fa-cloud-upload-alt"></i>
            <p>انقر أو اسحب الصور هنا</p>
            <small>يسمح بصورتين كحد أقصى (JPEG, PNG)</small>
          </div>
          
          <input type="file" id="image-upload" accept="image/*" multiple 
                 style="display: none" onchange="handleImageUpload(this)">
          
          <div class="image-preview" id="image-preview"></div>
        </div>

        <!-- التوقيعات -->
        <div class="signatures-section">
          <h3 class="form-section-title">
            <i class="fas fa-signature"></i>
            التوقيعات
          </h3>
          
          <div class="signatures-grid">
            <div class="signature-field">
              <label class="form-label">
                <i class="fas fa-chalkboard-teacher"></i>
                اسم المعلم
              </label>
              <input type="text" class="signature-input" id="teacher-name" 
                     placeholder="أدخل اسمك الكامل" required>
            </div>
            
            <div class="signature-field">
              <label class="form-label">
                <i class="fas fa-user-tie"></i>
                اسم المدير
              </label>
              <input type="text" class="signature-input" id="principal-name" 
                     placeholder="اسم مدير المدرسة">
            </div>
          </div>
        </div>
      </div>
    </main>

    <!-- لوحة التحكم -->
    <aside class="control-panel">
      <h3 class="form-section-title">
        <i class="fas fa-magic"></i>
        قوالب جاهزة
      </h3>
      
      <div class="quick-templates">
        <button class="template-btn" onclick="loadTemplate(1)">
          <i class="fas fa-star"></i>
          <span>نشاط إثرائي</span>
        </button>
        
        <button class="template-btn" onclick="loadTemplate(2)">
          <i class="fas fa-heart"></i>
          <span>خطة علاجية</span>
        </button>
        
        <button class="template-btn" onclick="loadTemplate(3)">
          <i class="fas fa-lightbulb"></i>
          <span>نشاط إبداعي</span>
        </button>
        
        <button class="template-btn" onclick="loadTemplate(4)">
          <i class="fas fa-chart-bar"></i>
          <span>تقرير تقويمي</span>
        </button>
      </div>
      
      <h3 class="form-section-title">
        <i class="fas fa-cogs"></i>
        أدوات التحكم
      </h3>
      
      <div class="action-buttons">
        <button class="action-btn action-btn-primary" onclick="showPreview()">
          <i class="fas fa-eye"></i>
          معاينة التقرير
        </button>
        
        <button class="action-btn action-btn-success" onclick="printReport()">
          <i class="fas fa-print"></i>
          طباعة التقرير
        </button>
        
        <button class="action-btn action-btn-secondary" onclick="saveDraft()">
          <i class="fas fa-save"></i>
          حفظ كمسودة
        </button>
        
        <button class="action-btn" style="background: #ef4444; color: white;" onclick="clearForm()">
          <i class="fas fa-trash"></i>
          مسح النموذج
        </button>
      </div>
      
      <div class="alert alert-warning" style="margin-top: 12px;">
        <i class="fas fa-info-circle"></i>
        <span>يتم الحفظ تلقائياً في ذاكرة المتصفح</span>
      </div>
    </aside>
  </div>
</div>

<!-- شريط التنقل السفلي للجوال -->
<nav class="mobile-nav">
  <button class="nav-btn active" onclick="scrollToTop()">
    <i class="fas fa-home"></i>
    <span>الرئيسية</span>
  </button>
  
  <button class="nav-btn" onclick="showPreview()">
    <i class="fas fa-eye"></i>
    <span>معاينة</span>
  </button>
  
  <button class="nav-btn" onclick="printReport()">
    <i class="fas fa-print"></i>
    <span>طباعة</span>
  </button>
  
  <button class="nav-btn" onclick="saveDraft()">
    <i class="fas fa-save"></i>
    <span>حفظ</span>
  </button>
</nav>

<!-- نافذة المعاينة -->
<div class="preview-overlay" id="preview-overlay">
  <div class="preview-container">
    <div class="preview-header">
      <h3><i class="fas fa-file-pdf"></i> معاينة التقرير</h3>
      <button class="close-preview" onclick="hidePreview()">
        <i class="fas fa-times"></i>
      </button>
    </div>
    <div class="report-content" id="report-content">
      <!-- محتوى التقرير -->
    </div>
  </div>
</div>

<!-- شاشة التحميل -->
<div class="loading-overlay" id="loading-overlay">
  <div class="loading-spinner"></div>
  <p>جاري إنشاء التقرير...</p>
</div>

<script>
// بيانات التطبيق
const templates = {
  1: {
    name: "نشاط إثرائي",
    type: "اثرائي",
    goal: "تنمية مهارات التفكير النقدي والإبداعي لدى الطلاب المتميزين من خلال أنشطة متقدمة تحفز الابتكار وتطور القدرات البحثية.",
    steps: `1. اختيار الطلاب الموهوبين بناءً على معايير محددة
2. عقد ورش عمل متخصصة في التفكير الإبداعي
3. تنفيذ مشاريع بحثية مصغرة
4. تنظيم مسابقات علمية محفزة
5. متابعة وتقييم فردي لكل طالب`,
    results: `• تطوير 8 مشاريع بحثية مبتكرة
• تحسن ملحوظ في مهارات التحليل بنسبة 40%
• مشاركة ناجحة في المسابقات المحلية
• زيادة الثقة العلمية لدى الطلاب`,
    recommendations: `• توسيع نطاق البرنامج ليشمل المزيد من الطلاب
• تدريب معلمين متخصصين في الإثراء العلمي
• إنشاء مكتبة مصادر رقمية متخصصة
• توثيق التجارب الناجحة ونشرها`,
    strengths: `• تفاعل الطلاب الإيجابي مع الأنشطة
• تنوع الأساليب التعليمية المستخدمة
• توافر الموارد التعليمية المساعدة
• دعم إدارة المدرسة للبرنامج`,
    improvements: `• زيادة وقت الأنشطة العملية
• توفير المزيد من الأجهزة التقنية
• تطوير أدوات تقييم أكثر شمولية
• تعزيز الشراكة مع أولياء الأمور`,
    target: "طلاب الصف الثالث الثانوي المتميزين",
    subject: "الفيزياء",
    executionPlace: "مختبر البحث"
  },
  2: {
    name: "خطة علاجية",
    type: "علاجي",
    goal: "معالجة الصعوبات القرائية والكتابية لدى الطلاب المتأخرين دراسياً وتحسين مهاراتهم الأساسية في اللغة العربية.",
    steps: `1. تشخيص فردي للصعوبات التعليمية
2. تصميم خطط علاجية مخصصة
3. جلسات علاجية مكثفة أسبوعياً
4. استخدام وسائل تعليمية مساعدة
5. متابعة أسرية وتقييم دوري`,
    results: `• تحسن مهارات القراءة بنسبة 65%
• تحسن مهارات الكتابة بنسبة 55%
• زيادة مشاركة الطلاب في الفصل
• تحسن الثقة بالنفس لدى الطلاب`,
    recommendations: `• تطوير أدوات تشخيص أكثر دقة
• تدريب فرق علاجية متخصصة
• إنشاء بنك أنشطة علاجية
• تعزيز الشراكة مع أولياء الأمور`,
    strengths: `• البرنامج الفردي المخصص
• استخدام وسائل تعليمية متنوعة
• المتابعة المستمرة للطلاب
• التعاون مع أولياء الأمور`,
    improvements: `• زيادة عدد الجلسات العلاجية
• توفير مختبر لغوي متكامل
• تدريب أكثر تخصصاً للمعلمين
• تطوير مواد تعليمية إضافية`,
    target: "الطلاب المتأخرين دراسياً في اللغة العربية",
    subject: "اللغة العربية",
    executionPlace: "قاعة المصادر"
  },
  3: {
    name: "نشاط إبداعي",
    type: "اثرائي",
    goal: "تنمية المهارات التقنية والبرمجية لدى الطلاب الموهوبين وتهيئتهم لمتطلبات العصر الرقمي.",
    steps: `1. تدريب على أساسيات البرمجة
2. ورش عمل في التصميم الرقمي
3. مشاريع تقنية تطبيقية
4. مسابقات برمجية
5. زيارات ميدانية لشركات تقنية`,
    results: `• تصميم 12 موقعاً إلكترونياً تعليمياً
• تطوير 5 تطبيقات تعليمية
• فوز في مسابقات برمجية محلية
• اكتشاف مواهب تقنية واعدة`,
    recommendations: `• توفير معامل حاسوب متطورة
• تأهيل مدربين في المجال التقني
• إنشاء نادي تقني مدرسي
• شراكات مع مؤسسات تقنية`,
    strengths: `• حماس الطلاب للتقنية
• توافر الأجهزة الحديثة
• دعم المجتمع المحلي
• نجاح المشاريع التطبيقية`,
    improvements: `• تحديث الأجهزة بشكل دوري
• زيادة ساعات التدريب
• تنويع المجالات التقنية
• تعزيز الجانب العملي`,
    target: "طلاب المرحلة الثانوية المهتمين بالتكنولوجيا",
    subject: "الحاسب الآلي",
    executionPlace: "معمل الحاسب الآلي"
  },
  4: {
    name: "تقرير تقويمي",
    type: "تقويمي",
    goal: "تقويم أداء الطلاب في نهاية الفصل الدراسي وتحديد مستوى تحقيق الأهداف التعليمية.",
    steps: `1. إعداد اختبارات تقويمية شاملة
2. تحليل نتائج الاختبارات
3. مقابلات فردية مع الطلاب
4. دراسة مؤشرات الأداء
5. تقييم المنهج الدراسي`,
    results: `• تحقيق 85% من الطلاب للمستوى المطلوب
• تحسن في متوسط الدرجات بنسبة 15%
• ارتفاع مؤشر الرضا عن التعليم
• تحديد نقاط القوة والضعف`,
    recommendations: `• تطوير استراتيجيات التدريس
• تحسين الوسائل التعليمية
• تنويع أساليب التقويم
• تعزيز التعلم الذاتي`,
    strengths: `• شمولية عملية التقويم
• موضوعية النتائج
• مشاركة الطلاب في التقييم
• دقة التحليل الإحصائي`,
    improvements: `• تطوير أدوات قياس أكثر دقة
• زيادة فترات التقويم
• تدريب المعلمين على التقويم
• تحليل نتائج أكثر تفصيلاً`,
    target: "جميع طلاب الصف",
    subject: "الرياضيات",
    executionPlace: "الفصل الدراسي"
  }
};

let uploadedImages = [];

// تحديث عداد الأحرف
function updateCharCount(textareaId, counterId) {
  const textarea = document.getElementById(textareaId);
  const counter = document.getElementById(counterId);
  
  if (!textarea || !counter) return;
  
  textarea.addEventListener('input', function() {
    const chars = this.value.length;
    counter.textContent = chars;
    
    if (chars > 250) {
      this.value = this.value.substring(0, 250);
      counter.textContent = 250;
      counter.style.color = '#dc2626';
    } else {
      counter.style.color = '#6b7280';
    }
  });
  
  // التهيئة الأولية
  const initialChars = textarea.value.length;
  counter.textContent = initialChars;
  if (initialChars > 250) {
    counter.style.color = '#dc2626';
  }
}

// تحميل القالب
function loadTemplate(templateId) {
  const template = templates[templateId];
  if (!template) return;
  
  // تعبئة الحقول
  document.getElementById('educational-goal').value = template.goal;
  document.getElementById('implementation-steps').value = template.steps;
  document.getElementById('achieved-results').value = template.results;
  document.getElementById('recommendations').value = template.recommendations;
  document.getElementById('strengths').value = template.strengths;
  document.getElementById('improvements').value = template.improvements;
  document.getElementById('target-audience').value = template.target;
  document.getElementById('subject').value = template.subject;
  document.getElementById('execution-place').value = template.executionPlace;
  
  // تحديث عداد الأحرف
  ['educational-goal', 'implementation-steps', 'achieved-results', 
   'recommendations', 'strengths', 'improvements'].forEach((id, index) => {
    updateCharCount(id, ['goal-chars', 'steps-chars', 'results-chars', 
                        'recommendations-chars', 'strengths-chars', 
                        'improvements-chars'][index]);
  });
  
  // إضافة قيم افتراضية
  if (!document.getElementById('school-name').value) {
    document.getElementById('school-name').value = "مدرسة الملك عبدالله الثانوية";
  }
  if (!document.getElementById('teacher-name').value) {
    document.getElementById('teacher-name').value = "أحمد محمد علي";
  }
  if (!document.getElementById('principal-name').value) {
    document.getElementById('principal-name').value = "خالد بن عبدالله السليم";
  }
  
  showAlert(`تم تحميل قالب "${template.name}" بنجاح`, 'success');
}

// مسح النموذج
function clearForm() {
  if (!confirm('هل أنت متأكد من رغبتك في مسح جميع البيانات؟')) return;
  
  const fields = [
    'school-name', 'target-audience', 'educational-goal',
    'implementation-steps', 'achieved-results', 'recommendations',
    'teacher-name', 'principal-name', 'subject', 'strengths', 
    'improvements', 'execution-place'
  ];
  
  fields.forEach(fieldId => {
    const element = document.getElementById(fieldId);
    if (element) element.value = '';
  });
  
  // مسح الصور
  uploadedImages = [];
  const preview = document.getElementById('image-preview');
  if (preview) preview.innerHTML = '';
  const uploadInput = document.getElementById('image-upload');
  if (uploadInput) uploadInput.value = '';
  
  // إعادة تعيين القوائم المنسدلة
  const departmentSelect = document.getElementById('education-department');
  if (departmentSelect) departmentSelect.value = '';
  
  // تحديث عداد الأحرف
  ['educational-goal', 'implementation-steps', 'achieved-results', 
   'recommendations', 'strengths', 'improvements'].forEach((id, index) => {
    updateCharCount(id, ['goal-chars', 'steps-chars', 'results-chars', 
                        'recommendations-chars', 'strengths-chars', 
                        'improvements-chars'][index]);
  });
  
  showAlert('تم مسح جميع البيانات بنجاح', 'success');
}

// رفع الصور
function handleImageUpload(input) {
  const files = Array.from(input.files).slice(0, 2);
  const preview = document.getElementById('image-preview');
  
  if (!preview) return;
  
  if (files.length > 2) {
    showAlert('يمكنك رفع صورتين كحد أقصى', 'error');
    input.value = '';
    return;
  }
  
  uploadedImages = [];
  preview.innerHTML = '';
  
  files.forEach((file, index) => {
    if (!file.type.match('image.*')) {
      showAlert('يرجى رفع ملفات صور فقط', 'error');
      return;
    }
    
    if (file.size > 5 * 1024 * 1024) {
      showAlert('حجم الصورة يجب أن يكون أقل من 5MB', 'error');
      return;
    }
    
    const reader = new FileReader();
    reader.onload = function(e) {
      uploadedImages.push({
        data: e.target.result,
        name: file.name
      });
      
      const imgDiv = document.createElement('div');
      imgDiv.className = 'preview-image';
      imgDiv.innerHTML = `
        <img src="${e.target.result}" alt="صورة ${index + 1}">
        <div class="remove-image" onclick="removeImage(${index})">
          <i class="fas fa-times"></i>
        </div>
      `;
      preview.appendChild(imgDiv);
    };
    reader.readAsDataURL(file);
  });
  
  if (files.length > 0) {
    showAlert(`تم رفع ${files.length} صورة بنجاح`, 'success');
  }
}

// إزالة صورة
function removeImage(index) {
  uploadedImages.splice(index, 1);
  const preview = document.getElementById('image-preview');
  if (!preview) return;
  
  preview.innerHTML = '';
  
  uploadedImages.forEach((img, i) => {
    const imgDiv = document.createElement('div');
    imgDiv.className = 'preview-image';
    imgDiv.innerHTML = `
      <img src="${img.data}" alt="صورة ${i + 1}">
      <div class="remove-image" onclick="removeImage(${i})">
        <i class="fas fa-times"></i>
      </div>
    `;
    preview.appendChild(imgDiv);
  });
}

// توليد HTML للتقرير حسب التصميم الجديد
function generateReportHTML(data) {
  // دالة للحصول على التاريخ الهجري (دون الاعتماد على API خارجي)
  const getHijriDate = () => {
    const today = new Date();
    const startGregorian = new Date(2024, 6, 7); // 7 يوليو 2024م تقريباً
    const diffTime = Math.abs(today - startGregorian);
    const diffDays = Math.ceil(diffTime / (1000 * 60 * 60 * 24));
    const hijriDay = (diffDays % 30) + 1;
    const hijriMonthNum = Math.floor((diffDays / 30) % 12);
    const hijriYear = 1446 + Math.floor(diffDays / 354);

    const hijriMonths = ["محرم", "صفر", "ربيع الأول", "ربيع الآخر", "جمادى الأولى", "جمادى الآخرة", "رجب", "شعبان", "رمضان", "شوال", "ذو القعدة", "ذو الحجة"];
    const hijriMonth = hijriMonths[hijriMonthNum] || "محرم";

    return `${hijriDay} ${hijriMonth} ${hijriYear} هـ`;
  };

  const getDepartmentName = (value) => {
    const departments = {
      'الرياض': 'الإدارة العامة للتعليم بمنطقة الرياض',
      'مكة': 'الإدارة العامة للتعليم بمنطقة مكة المكرمة',
      'الشرقية': 'الإدارة العامة للتعليم بالمنطقة الشرقية',
      'المدينة': 'الإدارة العامة للتعليم بمنطقة المدينة المنورة'
    };
    return departments[value] || value;
  };

  // ملء القيم الافتراضية للحقول غير الموجودة في النموذج القديم
  const semester = 'الأول';
  const studentCount = '15';
  const executionPlace = data.executionPlace || 'مختبر البحث';

  return `
    <div class="header">
      <div class="admin-name">${getDepartmentName(data.department)}</div>
      <div class="school-name">${data.school}</div>
      <div class="hijri-date">${getHijriDate()}</div>
    </div>

    <div class="info-wrapper">
      <div class="info-grid">
        <div class="info-box"><strong>الفصل الدراسي</strong>${semester}</div>
        <div class="info-box"><strong>الصف</strong>${data.target || 'غير محدد'}</div>
        <div class="info-box"><strong>المادة</strong>${data.subject || 'غير محدد'}</div>
      </div>

      <div class="info-grid second">
        <div class="info-box"><strong>التقرير</strong>تقرير نشاط إثرائي</div>
        <div class="info-box"><strong>المستهدفون</strong>${data.target || 'غير محدد'}</div>
        <div class="info-box"><strong>العدد</strong>${studentCount}</div>
        <div class="info-box"><strong>مكان التنفيذ</strong>${executionPlace}</div>
      </div>
    </div>

    <div class="page-content">
      <div class="report-objective-box">${data.goal || 'لم يتم تحديد الهدف التربوي'}</div>

      <div class="report-grid">
        <div class="report-box">
          <div class="report-box-title">خطوات التنفيذ</div>
          <div class="report-box-content">${data.steps || 'لم يتم تحديد خطوات التنفيذ'}</div>
        </div>
        <div class="report-box">
          <div class="report-box-title">النتائج</div>
          <div class="report-box-content">${data.results || 'لم يتم تحديد النتائج'}</div>
        </div>
        <div class="report-box">
          <div class="report-box-title">نقاط القوة</div>
          <div class="report-box-content">${data.strengths || 'لم يتم تحديد نقاط القوة'}</div>
        </div>
        <div class="report-box">
          <div class="report-box-title">التوصيات</div>
          <div class="report-box-content">${data.recommendations || 'لم يتم تحديد توصيات'}</div>
        </div>
      </div>

      <div class="improvements-box">
        <div class="report-box-title">نقاط التحسين</div>
        <div class="report-box-content">${data.improvements || 'لم يتم تحديد نقاط للتحسين'}</div>
      </div>

      ${uploadedImages.length > 0 ? `
        <div class="image-evidence-grid">
          ${uploadedImages.slice(0,2).map(img => `
            <div class="image-box">
              <img src="${img.data}" alt="صورة توثيقية" style="width:100%; height:100%; object-fit:cover; border-radius: 6px;">
            </div>
          `).join('')}
        </div>
      ` : `
        <div class="image-evidence-grid">
          <div class="image-box">شواهد الصور</div>
          <div class="image-box">شواهد الصور</div>
        </div>
      `}
    </div>
  `;
}

// بناء محتوى التقرير للمعاينة
function buildPreviewContent(data) {
  const content = document.getElementById('report-content');
  if (!content) return;
  
  // إضافة أنماط التصميم الجديد للمعاينة
  content.innerHTML = `
    <style>
      .preview-container .header {
        width: 100%;
        height: 90px;
        background-color: #083024;
        position: relative;
      }
      .preview-container .header::before {
        content: "";
        position: absolute;
        inset: 0;
        background-image: url('https://i.ibb.co/kVWFFwhW/9-C92-E57-B-23-FA-479-D-A024-1-D5-F871-B4-F8-D.png');
        background-repeat: no-repeat;
        background-position: center;
        background-size: 38%;
        opacity: 0.95;
      }
      .preview-container .admin-name {
        position: absolute;
        top: 6px;
        right: 12px;
        font-size: 8px;
        color: #ffffff;
        z-index: 2;
      }
      .preview-container .school-name {
        position: absolute;
        bottom: 6px;
        right: 12px;
        font-size: 8px;
        color: #ffffff;
        z-index: 2;
      }
      .preview-container .hijri-date {
        position: absolute;
        bottom: 6px;
        left: 12px;
        font-size: 8px;
        color: #ffffff;
        z-index: 2;
      }
      .preview-container .info-wrapper {
        padding: 6px 10px;
        max-width: 210mm;
        margin: auto;
      }
      .preview-container .info-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 4px;
        margin-bottom: 4px;
      }
      .preview-container .info-grid.second {
        grid-template-columns: repeat(4, 1fr);
      }
      .preview-container .info-box {
        border: 1px solid #083024;
        border-radius: 4px;
        padding: 3px 4px;
        text-align: center;
        font-size: 7px;
        background: rgba(255,255,255,0.95);
        line-height: 1.2;
      }
      .preview-container .info-box strong {
        display: block;
        font-size: 7.5px;
        margin-bottom: 1px;
      }
      .preview-container .page-content {
        padding: 12px;
        max-width: 210mm;
        margin: auto;
      }
      .preview-container .report-objective-box {
        background: rgba(8,48,36,0.15);
        border: 1px solid rgba(8,48,36,0.4);
        border-radius: 6px;
        padding: 6px;
        margin-bottom: 10px;
        text-align: center;
        font-size: 8px;
        white-space: pre-line;
      }
      .preview-container .report-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 8px;
        margin-bottom: 8px;
      }
      .preview-container .report-box {
        border-radius: 6px;
        border: 1px solid rgba(0,0,0,0.2);
        padding: 6px;
        background: rgba(0,0,0,0.03);
      }
      .preview-container .report-box-title {
        font-size: 7px;
        margin-bottom: 3px;
        border-bottom: 1px solid rgba(0,0,0,0.15);
        padding-bottom: 2px;
      }
      .preview-container .report-box-content {
        font-size: 6px;
        line-height: 1.4;
        white-space: pre-line;
      }
      .preview-container .improvements-box {
        background: rgba(234,88,12,0.12);
        border: 1px solid rgba(234,88,12,0.4);
        border-radius: 6px;
        padding: 6px;
        margin-bottom: 10px;
      }
      .preview-container .image-evidence-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 8px;
        margin-top: 8px;
      }
      .preview-container .image-box {
        border: 1px dashed #083024;
        border-radius: 6px;
        height: 120px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 7px;
        color: #083024;
        background: rgba(8,48,36,0.05);
        overflow: hidden;
      }
      .preview-container .image-box img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
      @media (max-width: 768px) {
        .preview-container .report-grid {
          grid-template-columns: 1fr;
        }
        .preview-container .info-grid,
        .preview-container .info-grid.second {
          grid-template-columns: 1fr;
        }
      }
    </style>
    
    ${generateReportHTML(data)}
  `;
}

// طباعة التقرير
function printReport() {
  const data = collectFormData();
  
  if (!validateForm()) {
    showAlert('الرجاء تعبئة الحقول المطلوبة قبل الطباعة', 'error');
    return;
  }
  
  // إنشاء نافذة طباعة مع التصميم الجديد
  const printWindow = window.open('', '_blank');
  printWindow.document.write(`
    <!DOCTYPE html>
    <html dir="rtl" lang="ar">
    <head>
      <meta charset="UTF-8">
      <title>تقرير تعليمي - ${data.school}</title>
      <style>
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&display=swap');
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html, body {
          width: 100%;
          font-family: 'Cairo', sans-serif;
          background: #ffffff;
          color: #1f2937;
        }
        .header {
          width: 100%;
          height: 90px;
          background-color: #083024;
          position: relative;
        }
        .header::before {
          content: "";
          position: absolute;
          inset: 0;
          background-image: url('https://i.ibb.co/kVWFFwhW/9-C92-E57-B-23-FA-479-D-A024-1-D5-F871-B4-F8-D.png');
          background-repeat: no-repeat;
          background-position: center;
          background-size: 38%;
          opacity: 0.95;
        }
        .admin-name {
          position: absolute;
          top: 6px;
          right: 12px;
          font-size: 8px;
          color: #ffffff;
          z-index: 2;
        }
        .school-name {
          position: absolute;
          bottom: 6px;
          right: 12px;
          font-size: 8px;
          color: #ffffff;
          z-index: 2;
        }
        .hijri-date {
          position: absolute;
          bottom: 6px;
          left: 12px;
          font-size: 8px;
          color: #ffffff;
          z-index: 2;
        }
        .info-wrapper {
          padding: 6px 10px;
          max-width: 210mm;
          margin: auto;
        }
        .info-grid {
          display: grid;
          grid-template-columns: repeat(3, 1fr);
          gap: 4px;
          margin-bottom: 4px;
        }
        .info-grid.second {
          grid-template-columns: repeat(4, 1fr);
        }
        .info-box {
          border: 1px solid #083024;
          border-radius: 4px;
          padding: 3px 4px;
          text-align: center;
          font-size: 7px;
          background: rgba(255,255,255,0.95);
          line-height: 1.2;
        }
        .info-box strong {
          display: block;
          font-size: 7.5px;
          margin-bottom: 1px;
        }
        .page-content {
          padding: 12px;
          max-width: 210mm;
          margin: auto;
        }
        .report-objective-box {
          background: rgba(8,48,36,0.15);
          border: 1px solid rgba(8,48,36,0.4);
          border-radius: 6px;
          padding: 6px;
          margin-bottom: 10px;
          text-align: center;
          font-size: 8px;
          white-space: pre-line;
        }
        .report-grid {
          display: grid;
          grid-template-columns: 1fr 1fr;
          gap: 8px;
          margin-bottom: 8px;
        }
        .report-box {
          border-radius: 6px;
          border: 1px solid rgba(0,0,0,0.2);
          padding: 6px;
          background: rgba(0,0,0,0.03);
        }
        .report-box-title {
          font-size: 7px;
          margin-bottom: 3px;
          border-bottom: 1px solid rgba(0,0,0,0.15);
          padding-bottom: 2px;
        }
        .report-box-content {
          font-size: 6px;
          line-height: 1.4;
          white-space: pre-line;
        }
        .improvements-box {
          background: rgba(234,88,12,0.12);
          border: 1px solid rgba(234,88,12,0.4);
          border-radius: 6px;
          padding: 6px;
          margin-bottom: 10px;
        }
        .image-evidence-grid {
          display: grid;
          grid-template-columns: 1fr 1fr;
          gap: 8px;
          margin-top: 8px;
        }
        .image-box {
          border: 1px dashed #083024;
          border-radius: 6px;
          height: 120px;
          display: flex;
          align-items: center;
          justify-content: center;
          font-size: 7px;
          color: #083024;
          background: rgba(8,48,36,0.05);
          overflow: hidden;
        }
        .image-box img {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
        @media print {
          .info-grid,
          .info-grid.second {
            grid-template-columns: repeat(3, 1fr) !important;
          }
          .report-grid {
            grid-template-columns: 1fr 1fr !important;
          }
        }
        @media (max-width: 768px) {
          .info-grid,
          .info-grid.second {
            grid-template-columns: 1fr;
          }
          .report-grid {
            grid-template-columns: 1fr;
          }
        }
      </style>
    </head>
    <body>
      ${generateReportHTML(data)}
    </body>
    </html>
  `);
  
  printWindow.document.close();
  printWindow.focus();
  
  setTimeout(() => {
    printWindow.print();
    printWindow.close();
  }, 500);
}

// عرض المعاينة
function showPreview() {
  const data = collectFormData();
  
  if (!validateForm()) {
    showAlert('الرجاء تعبئة الحقول المطلوبة (اسم المدرسة، الهدف التربوي، اسم المعلم)', 'error');
    return;
  }
  
  buildPreviewContent(data);
  const previewOverlay = document.getElementById('preview-overlay');
  if (previewOverlay) {
    previewOverlay.style.display = 'flex';
    document.body.style.overflow = 'hidden';
  }
}

// إخفاء المعاينة
function hidePreview() {
  const previewOverlay = document.getElementById('preview-overlay');
  if (previewOverlay) {
    previewOverlay.style.display = 'none';
    document.body.style.overflow = 'auto';
  }
}

// حفظ المسودة
function saveDraft() {
  const data = collectFormData();
  
  try {
    localStorage.setItem('report_draft', JSON.stringify({
      ...data,
      images: uploadedImages,
      timestamp: new Date().toISOString()
    }));
    
    showAlert('تم حفظ المسودة بنجاح في ذاكرة المتصفح', 'success');
  } catch (e) {
    showAlert('حدث خطأ أثناء حفظ المسودة', 'error');
  }
}

// تحميل المسودة
function loadDraft() {
  try {
    const draft = JSON.parse(localStorage.getItem('report_draft'));
    if (!draft) return;
    
    if (confirm('تم العثور على مسودة محفوظة. هل تريد تحميلها؟')) {
      const fields = {
        'school-name': draft.school || '',
        'education-department': draft.department || '',
        'target-audience': draft.target || '',
        'subject': draft.subject || '',
        'educational-goal': draft.goal || '',
        'implementation-steps': draft.steps || '',
        'achieved-results': draft.results || '',
        'recommendations': draft.recommendations || '',
        'strengths': draft.strengths || '',
        'improvements': draft.improvements || '',
        'teacher-name': draft.teacher || '',
        'principal-name': draft.principal || '',
        'execution-place': draft.executionPlace || ''
      };
      
      Object.entries(fields).forEach(([id, value]) => {
        const element = document.getElementById(id);
        if (element) element.value = value;
      });
      
      if (draft.images && draft.images.length > 0) {
        uploadedImages = draft.images;
        updateImagePreview();
      }
      
      // تحديث عداد الأحرف
      ['educational-goal', 'implementation-steps', 'achieved-results', 
       'recommendations', 'strengths', 'improvements'].forEach((id, index) => {
        updateCharCount(id, ['goal-chars', 'steps-chars', 'results-chars', 
                            'recommendations-chars', 'strengths-chars', 
                            'improvements-chars'][index]);
      });
      
      showAlert('تم تحميل المسودة بنجاح', 'success');
    }
  } catch (e) {
    console.error('خطأ في تحميل المسودة:', e);
  }
}

// تحديث معاينة الصور
function updateImagePreview() {
  const preview = document.getElementById('image-preview');
  if (!preview) return;
  
  preview.innerHTML = '';
  
  uploadedImages.forEach((img, i) => {
    const imgDiv = document.createElement('div');
    imgDiv.className = 'preview-image';
    imgDiv.innerHTML = `
      <img src="${img.data}" alt="صورة ${i + 1}">
      <div class="remove-image" onclick="removeImage(${i})">
        <i class="fas fa-times"></i>
      </div>
    `;
    preview.appendChild(imgDiv);
  });
}

// جمع بيانات النموذج
function collectFormData() {
  return {
    department: document.getElementById('education-department')?.value || '',
    school: document.getElementById('school-name')?.value.trim() || '',
    target: document.getElementById('target-audience')?.value.trim() || '',
    subject: document.getElementById('subject')?.value.trim() || '',
    goal: document.getElementById('educational-goal')?.value.trim() || '',
    steps: document.getElementById('implementation-steps')?.value.trim() || '',
    results: document.getElementById('achieved-results')?.value.trim() || '',
    recommendations: document.getElementById('recommendations')?.value.trim() || '',
    strengths: document.getElementById('strengths')?.value.trim() || '',
    improvements: document.getElementById('improvements')?.value.trim() || '',
    teacher: document.getElementById('teacher-name')?.value.trim() || '',
    principal: document.getElementById('principal-name')?.value.trim() || '',
    executionPlace: document.getElementById('execution-place')?.value.trim() || ''
  };
}

// التحقق من صحة البيانات
function validateForm() {
  const data = collectFormData();
  const requiredFields = ['school', 'goal', 'teacher'];
  
  for (const field of requiredFields) {
    if (!data[field]) {
      return false;
    }
  }
  
  return true;
}

// عرض التنبيهات
function showAlert(message, type = 'info') {
  const alert = document.createElement('div');
  alert.className = `alert alert-${type}`;
  alert.innerHTML = `
    <i class="fas fa-${type === 'success' ? 'check-circle' : 
                      type === 'warning' ? 'exclamation-triangle' : 
                      type === 'error' ? 'times-circle' : 'info-circle'}"></i>
    <span>${message}</span>
  `;
  
  const container = document.querySelector('.container');
  if (container) {
    container.prepend(alert);
    
    setTimeout(() => {
      if (alert.parentNode) {
        alert.remove();
      }
    }, 5000);
  }
}

// وظائف القائمة الجوال
function scrollToTop() {
  window.scrollTo({ top: 0, behavior: 'smooth' });
  setActiveNavBtn(0);
}

function setActiveNavBtn(index) {
  const navBtns = document.querySelectorAll('.nav-btn');
  navBtns.forEach((btn, i) => {
    if (i === index) {
      btn.classList.add('active');
    } else {
      btn.classList.remove('active');
    }
  });
}

function toggleMenu() {
  const controlPanel = document.querySelector('.control-panel');
  if (controlPanel) {
    controlPanel.style.display = controlPanel.style.display === 'none' ? 'block' : 'none';
  }
}

// إغلاق التنبيه بالنقر
document.addEventListener('click', function(e) {
  if (e.target.closest('.alert')) {
    e.target.closest('.alert').remove();
  }
});

// إغلاق المعاينة بالزر ESC
document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') {
    hidePreview();
  }
});

// إغلاق المعاينة بالنقر خارجها
const previewOverlay = document.getElementById('preview-overlay');
if (previewOverlay) {
  previewOverlay.addEventListener('click', function(e) {
    if (e.target === this) {
      hidePreview();
    }
  });
}

// تحسين تجربة اللمس
document.addEventListener('DOMContentLoaded', function() {
  // تحميل المسودة عند البدء
  loadDraft();
  
  // تحديث عداد الأحرف
  ['educational-goal', 'implementation-steps', 'achieved-results', 
   'recommendations', 'strengths', 'improvements'].forEach((id, index) => {
    updateCharCount(id, ['goal-chars', 'steps-chars', 'results-chars', 
                        'recommendations-chars', 'strengths-chars', 
                        'improvements-chars'][index]);
  });
  
  // تعيين القيم الافتراضية إذا لم تكن موجودة
  if (!document.getElementById('school-name')?.value) {
    const schoolNameInput = document.getElementById('school-name');
    if (schoolNameInput) schoolNameInput.value = "مدرسة الملك عبدالله الثانوية";
  }
  
  // إضافة مستمعين للأزرار في الجوال
  const navBtns = document.querySelectorAll('.nav-btn');
  navBtns.forEach((btn, index) => {
    btn.addEventListener('click', () => setActiveNavBtn(index));
  });
  
  // الترحيب
  setTimeout(() => {
    showAlert('مرحباً بك في نظام إعداد التقارير التعليمية', 'success');
  }, 1000);
});

// دعم سحب وإفلات الصور
const uploadArea = document.querySelector('.upload-area');
if (uploadArea) {
  uploadArea.addEventListener('dragover', (e) => {
    e.preventDefault();
    uploadArea.style.borderColor = '#083024';
    uploadArea.style.background = '#f3f4f6';
  });

  uploadArea.addEventListener('dragleave', () => {
    uploadArea.style.borderColor = '';
    uploadArea.style.background = '';
  });

  uploadArea.addEventListener('drop', (e) => {
    e.preventDefault();
    uploadArea.style.borderColor = '';
    uploadArea.style.background = '';
    
    const files = Array.from(e.dataTransfer.files);
    const input = document.getElementById('image-upload');
    
    // إنشاء DataTransfer object لتعيين الملفات
    const dataTransfer = new DataTransfer();
    files.slice(0, 2).forEach(file => dataTransfer.items.add(file));
    input.files = dataTransfer.files;
    
    handleImageUpload(input);
  });
}
</script>
</body>
</html>