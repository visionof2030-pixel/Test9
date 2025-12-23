<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>أداة التقارير التعليمية | وزارة التعليم</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --primary: #2E86C1;
  --primary-light: #5DADE2;
  --primary-dark: #1B4F72;
  --secondary: #27AE60;
  --secondary-light: #58D68D;
  --secondary-dark: #196F3D;
  --accent: #E67E22;
  --accent-light: #F39C12;
  --accent-dark: #CA6F1E;
  --purple: #8E44AD;
  --purple-light: #BB8FCE;
  --pink: #E84393;
  --pink-light: #FD79A8;
  --teal: #17A589;
  --teal-light: #48C9B0;
  --light: #F8F9FA;
  --light-gray: #EAECEE;
  --medium-gray: #BFC9CA;
  --dark: #2C3E50;
  --dark-gray: #566573;
  --success: #27AE60;
  --warning: #F39C12;
  --danger: #E74C3C;
  --border-radius: 14px;
  --box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
  --box-shadow-hover: 0 10px 25px rgba(0, 0, 0, 0.12);
  --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  -webkit-tap-highlight-color: transparent;
}

body {
  font-family: 'Cairo', sans-serif;
  background: linear-gradient(135deg, #F0F8FF 0%, #E8F8F5 50%, #FEF9E7 100%);
  color: var(--dark);
  line-height: 1.7;
  min-height: 100vh;
  padding: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 15px;
}

/* الهيدر بألوان جميلة */
.header {
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: 20px;
  margin-bottom: 25px;
  color: white;
  position: relative;
  overflow: hidden;
}

.header::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 150px;
  height: 150px;
  background: linear-gradient(45deg, rgba(255,255,255,0.1), transparent);
  border-radius: 50%;
  transform: translate(30%, -30%);
}

.header-content {
  position: relative;
  z-index: 1;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 15px;
}

@media (max-width: 768px) {
  .header-content {
    flex-direction: column;
    text-align: center;
  }
}

.logo-section {
  display: flex;
  align-items: center;
  gap: 15px;
}

.logo-icon {
  width: 60px;
  height: 60px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 28px;
  backdrop-filter: blur(10px);
  border: 2px solid rgba(255, 255, 255, 0.3);
}

.logo-text h1 {
  font-size: 22px;
  font-weight: 700;
  margin-bottom: 5px;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.logo-text p {
  font-size: 14px;
  opacity: 0.9;
}

.header-stats {
  display: flex;
  gap: 15px;
  flex-wrap: wrap;
}

.stat-item {
  background: rgba(255, 255, 255, 0.15);
  padding: 8px 15px;
  border-radius: 30px;
  font-size: 14px;
  display: flex;
  align-items: center;
  gap: 8px;
  backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.stat-item i {
  font-size: 16px;
}

/* شريط التنقل للجوال */
.mobile-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: white;
  box-shadow: 0 -4px 20px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  padding: 10px;
  display: none;
  justify-content: space-around;
  border-top: 3px solid var(--primary);
}

@media (max-width: 768px) {
  .mobile-nav {
    display: flex;
  }
  
  .container {
    padding-bottom: 85px;
  }
}

.nav-btn {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5px;
  background: none;
  border: none;
  color: var(--dark-gray);
  font-size: 12px;
  padding: 8px 5px;
  cursor: pointer;
  flex: 1;
  transition: var(--transition);
  border-radius: 10px;
}

.nav-btn:hover, .nav-btn.active {
  color: var(--primary);
  background: rgba(46, 134, 193, 0.1);
  transform: translateY(-3px);
}

.nav-btn i {
  font-size: 18px;
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-btn.active i {
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

/* المحتوى الرئيسي */
.main-content {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
}

@media (min-width: 1024px) {
  .main-content {
    grid-template-columns: 1fr 380px;
  }
}

/* لوحة التحكم */
.control-panel {
  background: white;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: 25px;
  height: fit-content;
  position: sticky;
  top: 20px;
  border: 1px solid var(--light-gray);
}

.control-panel h3 {
  color: var(--primary-dark);
  margin-bottom: 20px;
  padding-bottom: 10px;
  border-bottom: 2px solid var(--primary-light);
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 18px;
}

/* القوالب السريعة */
.quick-templates {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
  margin-bottom: 25px;
}

.template-btn {
  background: white;
  border: 2px solid var(--light-gray);
  border-radius: 12px;
  padding: 15px 10px;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.template-btn::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 4px;
  background: var(--primary);
  transform: translateY(-100%);
  transition: var(--transition);
}

.template-btn:hover {
  border-color: var(--primary);
  transform: translateY(-5px);
  box-shadow: var(--box-shadow-hover);
}

.template-btn:hover::before {
  transform: translateY(0);
}

.template-btn:nth-child(1)::before { background: var(--primary); }
.template-btn:nth-child(2)::before { background: var(--secondary); }
.template-btn:nth-child(3)::before { background: var(--accent); }
.template-btn:nth-child(4)::before { background: var(--purple); }

.template-btn i {
  font-size: 24px;
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.template-btn:nth-child(1) i {
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.template-btn:nth-child(2) i {
  background: linear-gradient(135deg, var(--secondary), var(--secondary-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.template-btn:nth-child(3) i {
  background: linear-gradient(135deg, var(--accent), var(--accent-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.template-btn:nth-child(4) i {
  background: linear-gradient(135deg, var(--purple), var(--purple-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.template-btn span {
  font-size: 14px;
  font-weight: 600;
  color: var(--dark);
}

/* أزرار التحكم */
.action-buttons {
  display: flex;
  flex-direction: column;
  gap: 12px;
  margin-top: 25px;
}

.action-btn {
  padding: 16px;
  border: none;
  border-radius: 12px;
  font-family: 'Cairo', sans-serif;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 12px;
  position: relative;
  overflow: hidden;
}

.action-btn::after {
  content: '';
  position: absolute;
  top: 50%;
  right: 50%;
  width: 0;
  height: 0;
  background: rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  transform: translate(50%, -50%);
  transition: width 0.6s, height 0.6s;
}

.action-btn:hover::after {
  width: 300px;
  height: 300px;
}

.action-btn i {
  font-size: 18px;
  position: relative;
  z-index: 1;
}

.btn-preview {
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  color: white;
}

.btn-preview:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(46, 134, 193, 0.3);
}

.btn-print {
  background: linear-gradient(135deg, var(--secondary), var(--secondary-dark));
  color: white;
}

.btn-print:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(39, 174, 96, 0.3);
}

.btn-save {
  background: linear-gradient(135deg, var(--teal), #148F77);
  color: white;
}

.btn-save:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(23, 165, 137, 0.3);
}

.btn-clear {
  background: linear-gradient(135deg, #E74C3C, #C0392B);
  color: white;
}

.btn-clear:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(231, 76, 60, 0.3);
}

/* نموذج الإدخال */
.form-container {
  background: white;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  overflow: hidden;
  border: 1px solid var(--light-gray);
}

.form-header {
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  color: white;
  padding: 20px;
  position: relative;
  overflow: hidden;
}

.form-header::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 100px;
  height: 100px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 50%;
  transform: translate(30%, -30%);
}

.form-header h2 {
  font-size: 20px;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 12px;
  position: relative;
  z-index: 1;
}

.form-content {
  padding: 25px;
}

/* أقسام النموذج */
.form-section {
  margin-bottom: 30px;
  padding: 20px;
  background: var(--light);
  border-radius: var(--border-radius);
  border-right: 4px solid var(--primary);
  transition: var(--transition);
}

.form-section:hover {
  transform: translateX(-5px);
  box-shadow: var(--box-shadow);
}

.section-title {
  font-size: 18px;
  font-weight: 600;
  color: var(--primary-dark);
  margin-bottom: 20px;
  padding-bottom: 10px;
  border-bottom: 2px solid var(--primary-light);
  display: flex;
  align-items: center;
  gap: 10px;
}

.section-title i {
  color: var(--primary);
  background: rgba(46, 134, 193, 0.1);
  width: 36px;
  height: 36px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* الحقول */
.form-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

@media (max-width: 768px) {
  .form-grid {
    grid-template-columns: 1fr;
  }
}

.form-group {
  margin-bottom: 20px;
}

.form-label {
  display: block;
  font-size: 15px;
  font-weight: 600;
  color: var(--dark);
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.form-label i {
  color: var(--primary);
  width: 24px;
  height: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(46, 134, 193, 0.1);
  border-radius: 6px;
}

.form-control {
  width: 100%;
  padding: 14px 16px;
  border: 2px solid var(--light-gray);
  border-radius: 10px;
  font-family: 'Cairo', sans-serif;
  font-size: 15px;
  color: var(--dark);
  transition: var(--transition);
  background: white;
}

.form-control:focus {
  outline: none;
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(46, 134, 193, 0.1);
  background: white;
}

textarea.form-control {
  min-height: 120px;
  resize: vertical;
  line-height: 1.6;
}

/* منطقة رفع الصور */
.upload-area {
  border: 3px dashed var(--primary-light);
  border-radius: 12px;
  padding: 30px;
  text-align: center;
  cursor: pointer;
  transition: var(--transition);
  margin-bottom: 20px;
  background: rgba(46, 134, 193, 0.05);
  position: relative;
  overflow: hidden;
}

.upload-area:hover {
  border-color: var(--primary);
  background: rgba(46, 134, 193, 0.1);
  transform: translateY(-3px);
}

.upload-area i {
  font-size: 48px;
  color: var(--primary);
  margin-bottom: 15px;
  display: block;
}

.upload-area p {
  color: var(--dark);
  font-size: 16px;
  margin-bottom: 8px;
  font-weight: 500;
}

.upload-area small {
  font-size: 13px;
  color: var(--dark-gray);
}

.image-preview {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
  gap: 15px;
  margin-top: 20px;
}

.preview-image {
  position: relative;
  border-radius: 10px;
  overflow: hidden;
  height: 140px;
  box-shadow: var(--box-shadow);
  transition: var(--transition);
}

.preview-image:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: var(--box-shadow-hover);
}

.preview-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.remove-image {
  position: absolute;
  top: 8px;
  left: 8px;
  background: linear-gradient(135deg, var(--danger), #C0392B);
  color: white;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: var(--transition);
  opacity: 0.9;
}

.remove-image:hover {
  opacity: 1;
  transform: scale(1.1);
}

/* قسم التوقيعات */
.signatures-section {
  background: linear-gradient(135deg, rgba(46, 134, 193, 0.05), rgba(39, 174, 96, 0.05));
  border-radius: 12px;
  padding: 25px;
  margin-top: 25px;
  border: 1px solid rgba(46, 134, 193, 0.2);
}

.signatures-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 25px;
}

.signature-field {
  text-align: center;
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: var(--box-shadow);
  transition: var(--transition);
}

.signature-field:hover {
  transform: translateY(-5px);
  box-shadow: var(--box-shadow-hover);
}

.signature-input {
  width: 100%;
  padding: 14px;
  border: 2px solid var(--light-gray);
  border-radius: 10px;
  font-family: 'Cairo', sans-serif;
  font-size: 16px;
  text-align: center;
  background: white;
  margin-top: 12px;
  transition: var(--transition);
}

.signature-input:focus {
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(46, 134, 193, 0.1);
}

/* التنبيهات */
.alert {
  padding: 15px 20px;
  border-radius: 10px;
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 15px;
  animation: slideIn 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
  border-right: 4px solid;
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateX(30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.alert-success {
  background: linear-gradient(135deg, rgba(39, 174, 96, 0.1), rgba(46, 204, 113, 0.1));
  color: var(--secondary-dark);
  border-right-color: var(--success);
}

.alert-warning {
  background: linear-gradient(135deg, rgba(243, 156, 18, 0.1), rgba(245, 176, 65, 0.1));
  color: #B9770E;
  border-right-color: var(--warning);
}

.alert-error {
  background: linear-gradient(135deg, rgba(231, 76, 60, 0.1), rgba(235, 110, 98, 0.1));
  color: #C0392B;
  border-right-color: var(--danger);
}

.alert-info {
  background: linear-gradient(135deg, rgba(52, 152, 219, 0.1), rgba(93, 173, 226, 0.1));
  color: var(--primary-dark);
  border-right-color: var(--primary);
}

/* نافذة المعاينة */
.preview-overlay {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.85);
  display: none;
  align-items: center;
  justify-content: center;
  z-index: 2000;
  padding: 20px;
  backdrop-filter: blur(10px);
}

.preview-container {
  background: white;
  border-radius: var(--border-radius);
  width: 100%;
  max-width: 1000px;
  max-height: 90vh;
  overflow-y: auto;
  position: relative;
  animation: scaleIn 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
}

@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.9);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.preview-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 25px;
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  color: white;
  position: sticky;
  top: 0;
  z-index: 10;
  border-radius: var(--border-radius) var(--border-radius) 0 0;
}

.close-preview {
  background: rgba(255, 255, 255, 0.2);
  border: none;
  color: white;
  font-size: 20px;
  cursor: pointer;
  padding: 8px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: var(--transition);
}

.close-preview:hover {
  background: rgba(255, 255, 255, 0.3);
  transform: rotate(90deg);
}

/* تصميم التقرير الملون */
.report-content {
  padding: 30px;
  font-family: 'Cairo', sans-serif;
}

.report-header {
  text-align: center;
  margin-bottom: 40px;
  padding-bottom: 25px;
  border-bottom: 3px solid var(--primary);
  position: relative;
  background: linear-gradient(135deg, rgba(46, 134, 193, 0.05), rgba(39, 174, 96, 0.05));
  padding: 25px;
  border-radius: 12px;
}

.report-header h1 {
  color: var(--primary-dark);
  font-size: 28px;
  margin-bottom: 10px;
  font-weight: 700;
}

.report-header h2 {
  color: var(--secondary-dark);
  font-size: 20px;
  margin-bottom: 8px;
  font-weight: 600;
}

.report-header h3 {
  color: var(--dark);
  font-size: 18px;
  margin-bottom: 15px;
}

.report-date {
  color: var(--accent);
  font-size: 16px;
  font-weight: 500;
  background: white;
  padding: 8px 20px;
  border-radius: 30px;
  display: inline-block;
  margin-top: 10px;
  border: 2px solid var(--accent-light);
}

.report-section {
  margin-bottom: 30px;
  padding: 25px;
  border-radius: 12px;
  background: white;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
  border-right: 4px solid;
  transition: var(--transition);
}

.report-section:hover {
  transform: translateX(-5px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
}

.report-section:nth-child(odd) {
  border-right-color: var(--primary);
  background: linear-gradient(135deg, rgba(46, 134, 193, 0.03), white);
}

.report-section:nth-child(even) {
  border-right-color: var(--secondary);
  background: linear-gradient(135deg, rgba(39, 174, 96, 0.03), white);
}

.report-section-title {
  color: var(--primary-dark);
  font-size: 20px;
  margin-bottom: 20px;
  padding-bottom: 12px;
  border-bottom: 2px solid;
  display: flex;
  align-items: center;
  gap: 12px;
  font-weight: 700;
}

.report-section:nth-child(odd) .report-section-title {
  border-bottom-color: var(--primary);
  color: var(--primary-dark);
}

.report-section:nth-child(even) .report-section-title {
  border-bottom-color: var(--secondary);
  color: var(--secondary-dark);
}

.report-section-title i {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 18px;
}

.report-section:nth-child(odd) .report-section-title i {
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
}

.report-section:nth-child(even) .report-section-title i {
  background: linear-gradient(135deg, var(--secondary), var(--secondary-light));
}

.report-section-content {
  color: var(--dark);
  line-height: 1.8;
  font-size: 16px;
  white-space: pre-line;
  padding: 15px;
  background: rgba(255, 255, 255, 0.5);
  border-radius: 8px;
  border-right: 3px solid rgba(46, 134, 193, 0.2);
}

.report-images {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

.report-image {
  border: 2px solid var(--light-gray);
  border-radius: 10px;
  overflow: hidden;
  transition: var(--transition);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.report-image:hover {
  border-color: var(--primary);
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

.report-image img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}

.report-signatures {
  display: flex;
  justify-content: space-between;
  margin-top: 50px;
  padding-top: 30px;
  border-top: 2px solid var(--primary-light);
  flex-wrap: wrap;
  gap: 30px;
  background: linear-gradient(135deg, rgba(46, 134, 193, 0.05), rgba(39, 174, 96, 0.05));
  padding: 30px;
  border-radius: 15px;
}

@media (max-width: 768px) {
  .report-signatures {
    flex-direction: column;
    align-items: center;
  }
}

.signature-box {
  text-align: center;
  flex: 1;
  min-width: 250px;
  background: white;
  padding: 25px;
  border-radius: 12px;
  box-shadow: var(--box-shadow);
  transition: var(--transition);
  border-top: 4px solid var(--primary);
}

.signature-box:hover {
  transform: translateY(-8px);
  box-shadow: var(--box-shadow-hover);
}

.signature-box:nth-child(2) {
  border-top-color: var(--secondary);
}

.signature-title {
  font-size: 18px;
  font-weight: 700;
  color: var(--primary-dark);
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.signature-box:nth-child(2) .signature-title {
  color: var(--secondary-dark);
}

.signature-name {
  font-size: 18px;
  color: var(--dark);
  margin-top: 20px;
  padding: 15px;
  background: rgba(46, 134, 193, 0.05);
  border-radius: 10px;
  font-weight: 600;
  border: 2px dashed rgba(46, 134, 193, 0.3);
}

.signature-box:nth-child(2) .signature-name {
  background: rgba(39, 174, 96, 0.05);
  border-color: rgba(39, 174, 96, 0.3);
}

.signature-line {
  width: 180px;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--primary), transparent);
  margin: 20px auto;
}

.signature-box:nth-child(2) .signature-line {
  background: linear-gradient(90deg, transparent, var(--secondary), transparent);
}

/* شاشة التحميل */
.loading-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.95);
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  z-index: 3000;
  color: white;
  text-align: center;
  backdrop-filter: blur(10px);
}

.loading-content {
  background: linear-gradient(135deg, rgba(46, 134, 193, 0.2), rgba(39, 174, 96, 0.2));
  padding: 40px;
  border-radius: 20px;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.loading-spinner {
  width: 70px;
  height: 70px;
  border: 4px solid rgba(255, 255, 255, 0.1);
  border-top-color: var(--primary-light);
  border-radius: 50%;
  animation: spin 1s linear infinite;
  margin-bottom: 25px;
}

.loading-overlay p {
  font-size: 20px;
  margin-bottom: 15px;
  font-weight: 600;
}

.loading-overlay small {
  font-size: 14px;
  opacity: 0.8;
  color: var(--light-gray);
}

/* تحسينات الطباعة */
@media print {
  body * {
    visibility: hidden;
  }
  
  .preview-container,
  .preview-container * {
    visibility: visible;
  }
  
  .preview-container {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    max-width: 100%;
    box-shadow: none;
    border-radius: 0;
    margin: 0;
    padding: 0;
  }
  
  .preview-header,
  .mobile-nav,
  .action-buttons,
  .control-panel {
    display: none !important;
  }
  
  .report-content {
    padding: 20mm;
  }
  
  .report-header {
    background: none !important;
    border-bottom: 3px solid #000 !important;
  }
  
  .report-section {
    break-inside: avoid;
    box-shadow: none !important;
    border: 1px solid #ddd !important;
  }
  
  .report-images {
    grid-template-columns: repeat(2, 1fr) !important;
  }
}

/* تخصيص شريط التمرير */
::-webkit-scrollbar {
  width: 10px;
  height: 10px;
}

::-webkit-scrollbar-track {
  background: rgba(46, 134, 193, 0.1);
  border-radius: 10px;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(135deg, var(--primary-dark), var(--primary));
}
</style>
</head>
<body>
<div class="container">
  <!-- الهيدر الملون -->
  <header class="header">
    <div class="header-content">
      <div class="logo-section">
        <div class="logo-icon">
          <i class="fas fa-graduation-cap"></i>
        </div>
        <div class="logo-text">
          <h1>أداة التقارير التعليمية الذكية</h1>
          <p>وزارة التعليم - إعداد تقارير احترافية بألوان جميلة</p>
        </div>
      </div>
      
      <div class="header-stats">
        <div class="stat-item">
          <i class="fas fa-check-circle"></i>
          <span>بيانات مؤمنة</span>
        </div>
        <div class="stat-item">
          <i class="fas fa-palette"></i>
          <span>تصميم ملون</span>
        </div>
        <div class="stat-item">
          <i class="fas fa-mobile-alt"></i>
          <span>متجاوب بالكامل</span>
        </div>
      </div>
    </div>
  </header>

  <!-- المحتوى الرئيسي -->
  <div class="main-content">
    <!-- نموذج الإدخال -->
    <main class="form-container">
      <div class="form-header">
        <h2><i class="fas fa-palette"></i> إنشاء تقرير ملون جديد
      </h2>
      </div>

      <div class="form-content">
        <!-- معلومات المدرسة -->
        <div class="form-section">
          <h3 class="section-title">
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
              <div class="form-hint" style="font-size: 13px; color: var(--dark-gray); margin-top: 5px;">
                <i class="fas fa-lightbulb"></i>
                مثال: مدرسة النخبة العلمية الثانوية
              </div>
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
                <option value="القصيم">الإدارة العامة للتعليم بمنطقة القصيم</option>
              </select>
            </div>
          </div>
        </div>

        <!-- معلومات التقرير -->
        <div class="form-section">
          <h3 class="section-title">
            <i class="fas fa-file-alt"></i>
            معلومات التقرير
          </h3>
          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-file"></i>
                نوع التقرير
              </label>
              <select class="form-control" id="report-type">
                <option value="اثرائي">تقرير نشاط إثرائي</option>
                <option value="علاجي">تقرير خطة علاجية</option>
                <option value="تقويمي">تقرير تقويمي</option>
                <option value="متابعة">تقرير متابعة</option>
                <option value="بحثي">تقرير بحث علمي</option>
              </select>
            </div>
            
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-users"></i>
                الفئة المستهدفة
              </label>
              <input type="text" class="form-control" id="target-audience" 
                     placeholder="مثال: طلاب الصف الثالث الثانوي المتميزين">
            </div>
            
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-calendar"></i>
                الفصل الدراسي
              </label>
              <select class="form-control" id="semester">
                <option value="الأول">الفصل الدراسي الأول</option>
                <option value="الثاني">الفصل الدراسي الثاني</option>
                <option value="الصيفي">الفصل الصيفي</option>
              </select>
            </div>
            
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-book"></i>
                المادة الدراسية
              </label>
              <input type="text" class="form-control" id="subject" 
                     placeholder="مثال: الرياضيات - الفيزياء - اللغة العربية">
            </div>
          </div>
        </div>

        <!-- محتوى التقرير -->
        <div class="form-section">
          <h3 class="section-title">
            <i class="fas fa-file-signature"></i>
            محتوى التقرير الملون
          </h3>
          
          <div class="form-group">
            <label class="form-label">
              <i class="fas fa-bullseye"></i>
              الهدف التربوي
            </label>
            <textarea class="form-control" id="educational-goal" 
                      placeholder="اكتب الهدف التربوي من النشاط بشكل واضح ومحدد..." 
                      rows="4" required></textarea>
            <div class="char-counter" id="goal-counter">0/300 حرف</div>
          </div>
          
          <div class="form-group">
            <label class="form-label">
              <i class="fas fa-tasks"></i>
              إجراءات التنفيذ
            </label>
            <textarea class="form-control" id="implementation-steps" 
                      placeholder="صف خطوات التنفيذ بالترتيب مع تحديد المسؤوليات..." 
                      rows="5"></textarea>
            <div class="char-counter" id="steps-counter">0/500 حرف</div>
          </div>
          
          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-chart-line"></i>
                النتائج المتحققة
              </label>
              <textarea class="form-control" id="achieved-results" 
                        placeholder="سجل النتائج الملموسة والأثر الإيجابي..." 
                        rows="4"></textarea>
              <div class="char-counter" id="results-counter">0/400 حرف</div>
            </div>
            
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-comments"></i>
                التوصيات والمقترحات
              </label>
              <textarea class="form-control" id="recommendations" 
                        placeholder="اقترح تحسينات للمستقبل وتوصيات عملية..." 
                        rows="4"></textarea>
              <div class="char-counter" id="rec-counter">0/400 حرف</div>
            </div>
          </div>
          
          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-thumbs-up"></i>
                نقاط القوة
              </label>
              <textarea class="form-control" id="strengths" 
                        placeholder="ما الذي نجح بشكل ممتاز في النشاط؟" 
                        rows="3"></textarea>
            </div>
            
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-lightbulb"></i>
                فرص التحسين
              </label>
              <textarea class="form-control" id="improvements" 
                        placeholder="ما الذي يمكن تحسينه في المرات القادمة؟" 
                        rows="3"></textarea>
            </div>
          </div>
        </div>

        <!-- الصور التوثيقية -->
        <div class="form-section">
          <h3 class="section-title">
            <i class="fas fa-images"></i>
            الصور التوثيقية الملونة
          </h3>
          
          <div class="upload-area" onclick="document.getElementById('image-upload').click()">
            <i class="fas fa-cloud-upload-alt"></i>
            <p>انقر أو اسحب الصور هنا للرفع</p>
            <small>يسمح بصورتين كحد أقصى (JPEG, PNG, GIF) - 5MB لكل صورة</small>
          </div>
          
          <input type="file" id="image-upload" accept="image/*" multiple 
                 style="display: none" onchange="handleImageUpload(this)">
          
          <div class="image-preview" id="image-preview"></div>
        </div>

        <!-- التوقيعات -->
        <div class="signatures-section">
          <h3 class="section-title">
            <i class="fas fa-signature"></i>
            التوقيعات والاعتماد
          </h3>
          
          <div class="signatures-grid">
            <div class="signature-field">
              <label class="form-label">
                <i class="fas fa-chalkboard-teacher"></i>
                اسم المعلم / المشرف
              </label>
              <input type="text" class="signature-input" id="teacher-name" 
                     placeholder="أدخل اسمك الكامل" required>
            </div>
            
            <div class="signature-field">
              <label class="form-label">
                <i class="fas fa-user-tie"></i>
                اسم مدير المدرسة
              </label>
              <input type="text" class="signature-input" id="principal-name" 
                     placeholder="اسم مدير المدرسة الكامل">
            </div>
          </div>
        </div>
      </div>
    </main>

    <!-- لوحة التحكم -->
    <aside class="control-panel">
      <h3><i class="fas fa-magic"></i> قوالب ملونة جاهزة</h3>
      
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
      
      <h3><i class="fas fa-tools"></i> أدوات التحكم</h3>
      
      <div class="action-buttons">
        <button class="action-btn btn-preview" onclick="showPreview()">
          <i class="fas fa-eye"></i>
          معاينة التقرير
        </button>
        
        <button class="action-btn btn-print" onclick="generateColoredReport()">
          <i class="fas fa-print"></i>
          إنشاء وطباعة
        </button>
        
        <button class="action-btn btn-save" onclick="saveToLocalStorage()">
          <i class="fas fa-save"></i>
          حفظ مسودة
        </button>
        
        <button class="action-btn btn-clear" onclick="showClearConfirmation()">
          <i class="fas fa-trash"></i>
          مسح النموذج
        </button>
      </div>
      
      <div class="alert alert-info" style="margin-top: 20px;">
        <i class="fas fa-info-circle"></i>
        <span>التقارير الملونة تحفظ تلقائياً في المتصفح</span>
      </div>
      
      <div class="color-palette" style="margin-top: 25px; padding: 15px; background: var(--light); border-radius: 10px;">
        <h4 style="color: var(--primary-dark); margin-bottom: 10px; font-size: 16px;">
          <i class="fas fa-palette"></i> ألوان التقرير
        </h4>
        <div style="display: flex; gap: 8px; flex-wrap: wrap;">
          <div style="width: 25px; height: 25px; background: var(--primary); border-radius: 5px; cursor: pointer;" onclick="changeColorScheme('blue')"></div>
          <div style="width: 25px; height: 25px; background: var(--secondary); border-radius: 5px; cursor: pointer;" onclick="changeColorScheme('green')"></div>
          <div style="width: 25px; height: 25px; background: var(--accent); border-radius: 5px; cursor: pointer;" onclick="changeColorScheme('orange')"></div>
          <div style="width: 25px; height: 25px; background: var(--purple); border-radius: 5px; cursor: pointer;" onclick="changeColorScheme('purple')"></div>
          <div style="width: 25px; height: 25px; background: var(--pink); border-radius: 5px; cursor: pointer;" onclick="changeColorScheme('pink')"></div>
        </div>
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
  
  <button class="nav-btn" onclick="generateColoredReport()">
    <i class="fas fa-print"></i>
    <span>طباعة</span>
  </button>
  
  <button class="nav-btn" onclick="saveToLocalStorage()">
    <i class="fas fa-save"></i>
    <span>حفظ</span>
  </button>
</nav>

<!-- نافذة المعاينة -->
<div class="preview-overlay" id="preview-overlay">
  <div class="preview-container">
    <div class="preview-header">
      <h3><i class="fas fa-file-pdf"></i> معاينة التقرير الملون</h3>
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
  <div class="loading-content">
    <div class="loading-spinner"></div>
    <p>جاري إنشاء التقرير الملون...</p>
    <small>يرجى الانتظار، التقرير قيد الإعداد</small>
  </div>
</div>

<script>
// بيانات التطبيق
const templates = {
  1: {
    name: "نشاط إثرائي",
    type: "اثرائي",
    goal: "تنمية مهارات التفكير النقدي والإبداعي لدى الطلاب المتميزين من خلال أنشطة متقدمة تحفز الابتكار وتطور القدرات البحثية، مع التركيز على تطوير مشاريع علمية مبتكرة.",
    steps: `1. اختيار الطلاب الموهوبين بناءً على معايير محددة (التحصيل العلمي، الإبداع، المهارات)
2. عقد ورش عمل متخصصة في التفكير الإبداعي وحل المشكلات
3. تنفيذ مشاريع بحثية مصغرة تحت إشراف متخصصين
4. تنظيم مسابقات علمية محفزة مع جوائز تشجيعية
5. متابعة وتقييم فردي لكل طالب مع توفير تغذية راجعة
6. تنظيم معرض لعرض إنجازات الطلاب`,
    results: `• تطوير 8 مشاريع بحثية مبتكرة في مجالات متنوعة
• تحسن ملحوظ في مهارات التحليل والتفكير النقدي بنسبة 40%
• مشاركة ناجحة في 3 مسابقات علمية محلية وحصول على مراكز متقدمة
• زيادة الثقة العلمية والمهارات العرضية لدى الطلاب
• ارتفاع مستوى الدافعية للتعلم لدى المشاركين`,
    recommendations: `• توسيع نطاق البرنامج ليشمل المزيد من الطلاب المتميزين
• تدريب معلمين متخصصين في الإثراء العلمي والتفكير الإبداعي
• إنشاء مكتبة مصادر رقمية متخصصة للطلاب الموهوبين
• توثيق التجارب الناجحة ونشرها كنماذج استرشادية
• إقامة شراكات مع مؤسسات بحثية وجامعات محلية`,
    target: "طلاب الصف الثالث الثانوي المتميزين أكاديمياً",
    subject: "الفيزياء المتقدمة",
    strengths: "تنوع الأنشطة، جودة الإشراف، الموارد المتاحة، تفاعل الطلاب الإيجابي",
    improvements: "توفير مزيد من الوقت، زيادة الميزانية، توسيع قاعدة المشاركة"
  },
  2: {
    name: "خطة علاجية",
    type: "علاجي",
    goal: "معالجة الصعوبات القرائية والكتابية لدى الطلاب المتأخرين دراسياً في اللغة العربية وتحسين مهاراتهم الأساسية، ورفع مستوى الثقة لديهم في التعامل مع النصوص العربية.",
    steps: `1. تشخيص فردي دقيق للصعوبات التعليمية لكل طالب
2. تصميم خطط علاجية مخصصة تناسب مستوى كل طالب
3. جلسات علاجية مكثفة أسبوعياً (3 جلسات أسبوعياً)
4. استخدام وسائل تعليمية مساعدة وبرامج محوسبة
5. متابعة أسرية منتظمة وتقييم دوري كل أسبوعين
6. أنشطة تعزيزية وتطبيقات عملية`,
    results: `• تحسن مهارات القراءة الجهرية والصامتة بنسبة 65%
• تحسن مهارات الكتابة والإملاء بنسبة 55%
• زيادة مشاركة الطلاب في الحصص والأنشطة الصفية
• تحسن ملحوظ في الثقة بالنفس والتعبير الشفهي
• ارتفاع مستوى الرضا لدى أولياء الأمور عن التحسن`,
    recommendations: `• تطوير أدوات تشخيص أكثر دقة وشاملة
• تدريب فرق علاجية متخصصة في صعوبات التعلم
• إنشاء بنك أنشطة علاجية متدرجة الصعوبة
• تعزيز الشراكة مع أولياء الأمور عبر ورش توعوية
• توفير بيئة تعلم داعمة وخالية من التوتر`,
    target: "الطلاب المتأخرين دراسياً في مهارات اللغة العربية",
    subject: "اللغة العربية",
    strengths: "الاهتمام الفردي، التنوع في الأساليب، المتابعة المستمرة",
    improvements: "توفير موارد أكثر، زيادة وقت الجلسات، تدريب إضافي للمعلمين"
  },
  3: {
    name: "نشاط إبداعي",
    type: "اثرائي",
    goal: "تنمية المهارات التقنية والبرمجية لدى الطلاب الموهوبين في مجال التكنولوجيا، وتهيئتهم لمتطلبات العصر الرقمي من خلال مشاريع تطبيقية مبتكرة.",
    steps: `1. تدريب مكثف على أساسيات البرمجة والتفكير الحاسوبي
2. ورش عمل في التصميم الرقمي وتطوير الواجهات
3. مشاريع تقنية تطبيقية (تطبيقات - مواقع إلكترونية)
4. مسابقات برمجية وجوائز تحفيزية
5. زيارات ميدانية لشركات تقنية ومؤسسات ريادية
6. تقديم مشاريع الطلاب في معرض تقني خاص`,
    results: `• تصميم وتطوير 12 موقعاً إلكترونياً تعليمياً تفاعلياً
• تطوير 5 تطبيقات تعليمية على منصتي Android و iOS
• فوز الفريق في 3 مسابقات برمجية محلية وإقليمية
• اكتشاف وتطوير 15 موهبة تقنية واعدة
• إنشاء نادٍ تقني مدرسي نشط ومؤثر`,
    recommendations: `• توفير معامل حاسوب متطورة مجهزة بأحدث البرامج
• تأهيل مدربين متخصصين في المجال التقني والبرمجة
• إنشاء نادي تقني دائم وتوفير ميزانية تشغيلية
• إقامة شراكات مع مؤسسات تقنية وجامعات متخصصة
• تطوير منهج تقني متكامل للمراحل الدراسية`,
    target: "طلاب المرحلة الثانوية المهتمين بالتكنولوجيا والبرمجة",
    subject: "الحاسب الآلي وتقنية المعلومات",
    strengths: "التطبيق العملي، الإبداع التقني، الدعم المتميز",
    improvements: "تحديث الأجهزة، توسيع النطاق، زيادة الموارد"
  },
  4: {
    name: "تقرير تقويمي",
    type: "تقويمي",
    goal: "تقويم أداء الطلاب في نهاية الفصل الدراسي وتحليل نتائجهم، وتحديد مستوى تحقيق الأهداف التعليمية، ووضع خطط تطويرية للفصل القادم.",
    steps: `1. إعداد اختبارات تقويمية شاملة تغطي جميع المهارات
2. تحليل إحصائي دقيق لنتائج الاختبارات باستخدام أدوات متخصصة
3. مقابلات فردية مع الطلاب لمناقشة النتائج والتحديات
4. دراسة مؤشرات الأداء ومقارنتها مع المعايير الوطنية
5. تقييم المنهج الدراسي وطرق التدريس المستخدمة
6. ورش عمل مع المعلمين لتحليل النتائج ووضع الخطط`,
    results: `• تحقيق 85% من الطلاب للمستوى المطلوب في جميع المواد
• تحسن في متوسط الدرجات بنسبة 15% مقارنة بالفصل السابق
• ارتفاع مؤشر الرضا عن العملية التعليمية إلى 88%
• تحديد نقاط القوة والضعف بدقة للطلاب والمعلمين
• تحسن في مهارات التقويم الذاتي لدى الطلاب`,
    recommendations: `• تطوير استراتيجيات تدريس تتناسب مع أنماط التعلم المختلفة
• تحسين الوسائل التعليمية وتوفير موارد تعليمية متنوعة
• تنويع أساليب التقويم لتشمل المهارات العملية
• تعزيز التعلم الذاتي والبحث العلمي لدى الطلاب
• تطوير نظام متابعة فردي للطلاب المتأخرين`,
    target: "جميع طلاب الصف العاشر",
    subject: "الرياضيات والعلوم",
    strengths: "الدقة في التحليل، الشمولية، المشاركة الفعالة",
    improvements: "تطوير أدوات التقويم، زيادة التغذية الراجعة، تحسين التوقيت"
  }
};

let uploadedImages = [];
let currentColorScheme = 'blue';

// تحميل القالب
function loadTemplate(templateId) {
  const template = templates[templateId];
  if (!template) return;
  
  // تعبئة الحقول
  document.getElementById('report-type').value = template.type;
  document.getElementById('educational-goal').value = template.goal;
  document.getElementById('implementation-steps').value = template.steps;
  document.getElementById('achieved-results').value = template.results;
  document.getElementById('recommendations').value = template.recommendations;
  document.getElementById('target-audience').value = template.target;
  document.getElementById('subject').value = template.subject;
  document.getElementById('strengths').value = template.strengths;
  document.getElementById('improvements').value = template.improvements;
  
  // تحديث العدادات
  updateCharCounters();
  
  // إشعار
  showAlert(`تم تحميل قالب "${template.name}" بنجاح!`, 'success');
}

// تحديث عدادات الأحرف
function updateCharCounters() {
  const fields = [
    {id: 'educational-goal', counter: 'goal-counter', max: 300},
    {id: 'implementation-steps', counter: 'steps-counter', max: 500},
    {id: 'achieved-results', counter: 'results-counter', max: 400},
    {id: 'recommendations', counter: 'rec-counter', max: 400}
  ];
  
  fields.forEach(field => {
    const textarea = document.getElementById(field.id);
    const counter = document.getElementById(field.counter);
    const length = textarea.value.length;
    const percentage = (length / field.max) * 100;
    
    counter.textContent = `${length}/${field.max} حرف`;
    
    // تغيير اللون حسب النسبة
    counter.style.color = percentage >= 90 ? '#e74c3c' : 
                         percentage >= 75 ? '#f39c12' : 
                         '#27ae60';
  });
}

// إضافة مستمعين للأحداث
document.addEventListener('DOMContentLoaded', function() {
  // تحديث العدادات عند الكتابة
  ['educational-goal', 'implementation-steps', 'achieved-results', 'recommendations'].forEach(id => {
    document.getElementById(id).addEventListener('input', updateCharCounters);
  });
  
  // تحميل المسودة المحفوظة
  loadFromLocalStorage();
  
  // تعيين القيم الافتراضية
  if (!document.getElementById('school-name').value) {
    document.getElementById('school-name').value = "مدرسة النخبة العلمية الثانوية";
  }
  if (!document.getElementById('teacher-name').value) {
    document.getElementById('teacher-name').value = "أحمد بن محمد العلي";
  }
  
  // تحديث العدادات الأولية
  updateCharCounters();
  
  // الترحيب
  setTimeout(() => {
    showAlert('مرحباً بك في نظام التقارير التعليمية الملونة!', 'info');
  }, 1000);
});

// مسح النموذج مع تأكيد
function showClearConfirmation() {
  const modal = document.createElement('div');
  modal.style.cssText = `
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: rgba(0,0,0,0.8);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 3000;
    padding: 20px;
    backdrop-filter: blur(10px);
  `;
  
  modal.innerHTML = `
    <div style="background: white; padding: 30px; border-radius: 15px; max-width: 400px; width: 100%; text-align: center;">
      <div style="color: #e74c3c; font-size: 50px; margin-bottom: 20px;">
        <i class="fas fa-exclamation-triangle"></i>
      </div>
      <h3 style="color: #2c3e50; margin-bottom: 15px;">تأكيد المسح</h3>
      <p style="color: #566573; margin-bottom: 25px; line-height: 1.6;">
        هل أنت متأكد من رغبتك في مسح جميع البيانات؟<br>
        <small style="color: #95a5a6;">لن يمكنك استرجاع البيانات بعد المسح</small>
      </p>
      <div style="display: flex; gap: 15px; justify-content: center;">
        <button onclick="clearForm()" style="background: #e74c3c; color: white; border: none; padding: 12px 30px; border-radius: 8px; cursor: pointer; font-family: 'Cairo'; font-weight: bold; transition: all 0.3s;">
          نعم، مسح الكل
        </button>
        <button onclick="this.closest('div').parentElement.remove()" style="background: #2ecc71; color: white; border: none; padding: 12px 30px; border-radius: 8px; cursor: pointer; font-family: 'Cairo'; font-weight: bold; transition: all 0.3s;">
          إلغاء
        </button>
      </div>
    </div>
  `;
  
  document.body.appendChild(modal);
}

// مسح النموذج
function clearForm() {
  const fields = [
    'school-name', 'target-audience', 'educational-goal',
    'implementation-steps', 'achieved-results', 'recommendations',
    'teacher-name', 'principal-name', 'subject', 'strengths', 'improvements'
  ];
  
  fields.forEach(fieldId => {
    document.getElementById(fieldId).value = '';
  });
  
  uploadedImages = [];
  document.getElementById('image-preview').innerHTML = '';
  document.getElementById('image-upload').value = '';
  
  document.getElementById('report-type').value = 'اثرائي';
  document.getElementById('education-department').value = '';
  document.getElementById('semester').value = 'الأول';
  
  updateCharCounters();
  
  document.querySelector('div[style*="position: fixed"]')?.remove();
  
  showAlert('تم مسح جميع البيانات بنجاح', 'success');
}

// رفع الصور
function handleImageUpload(input) {
  const files = Array.from(input.files).slice(0, 2);
  const preview = document.getElementById('image-preview');
  
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
        name: file.name,
        size: file.size
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

// حفظ في localStorage
function saveToLocalStorage() {
  const data = collectFormData();
  
  try {
    localStorage.setItem('colored_report_draft', JSON.stringify({
      ...data,
      images: uploadedImages,
      colorScheme: currentColorScheme,
      savedAt: new Date().toLocaleString('ar-SA')
    }));
    
    showAlert('تم حفظ المسودة بنجاح في ذاكرة المتصفح', 'success');
  } catch (e) {
    showAlert('حدث خطأ أثناء حفظ المسودة', 'error');
  }
}

// تحميل من localStorage
function loadFromLocalStorage() {
  try {
    const saved = localStorage.getItem('colored_report_draft');
    if (!saved) return;
    
    if (confirm('تم العثور على مسودة محفوظة. هل تريد تحميلها؟')) {
      const data = JSON.parse(saved);
      
      document.getElementById('school-name').value = data.school || '';
      document.getElementById('education-department').value = data.department || '';
      document.getElementById('report-type').value = data.type || 'اثرائي';
      document.getElementById('target-audience').value = data.target || '';
      document.getElementById('semester').value = data.semester || 'الأول';
      document.getElementById('subject').value = data.subject || '';
      document.getElementById('educational-goal').value = data.goal || '';
      document.getElementById('implementation-steps').value = data.steps || '';
      document.getElementById('achieved-results').value = data.results || '';
      document.getElementById('recommendations').value = data.recommendations || '';
      document.getElementById('strengths').value = data.strengths || '';
      document.getElementById('improvements').value = data.improvements || '';
      document.getElementById('teacher-name').value = data.teacher || '';
      document.getElementById('principal-name').value = data.principal || '';
      
      if (data.images && data.images.length > 0) {
        uploadedImages = data.images;
        updateImagePreview();
      }
      
      if (data.colorScheme) {
        changeColorScheme(data.colorScheme);
      }
      
      updateCharCounters();
      showAlert('تم تحميل المسودة بنجاح', 'success');
    }
  } catch (e) {
    console.error('خطأ في تحميل المسودة:', e);
  }
}

// تحديث معاينة الصور
function updateImagePreview() {
  const preview = document.getElementById('image-preview');
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

// تغيير نظام الألوان
function changeColorScheme(scheme) {
  currentColorScheme = scheme;
  
  const root = document.documentElement;
  const colors = {
    blue: {
      primary: '#2E86C1',
      primaryLight: '#5DADE2',
      primaryDark: '#1B4F72',
      secondary: '#27AE60'
    },
    green: {
      primary: '#27AE60',
      primaryLight: '#58D68D',
      primaryDark: '#196F3D',
      secondary: '#2E86C1'
    },
    orange: {
      primary: '#E67E22',
      primaryLight: '#F39C12',
      primaryDark: '#CA6F1E',
      secondary: '#2E86C1'
    },
    purple: {
      primary: '#8E44AD',
      primaryLight: '#BB8FCE',
      primaryDark: '#6C3483',
      secondary: '#27AE60'
    },
    pink: {
      primary: '#E84393',
      primaryLight: '#FD79A8',
      primaryDark: '#B33771',
      secondary: '#27AE60'
    }
  };
  
  const schemeColors = colors[scheme];
  if (!schemeColors) return;
  
  root.style.setProperty('--primary', schemeColors.primary);
  root.style.setProperty('--primary-light', schemeColors.primaryLight);
  root.style.setProperty('--primary-dark', schemeColors.primaryDark);
  root.style.setProperty('--secondary', schemeColors.secondary);
  
  showAlert(`تم تغيير الألوان إلى ${scheme === 'blue' ? 'الأزرق' : scheme === 'green' ? 'الأخضر' : scheme === 'orange' ? 'البرتقالي' : scheme === 'purple' ? 'البنفسجي' : 'الوردي'}`, 'info');
}

// عرض المعاينة
function showPreview() {
  const data = collectFormData();
  
  if (!validateForm()) {
    showAlert('الرجاء تعبئة الحقول المطلوبة (اسم المدرسة، الهدف التربوي، اسم المعلم)', 'error');
    return;
  }
  
  buildColoredReport(data);
  document.getElementById('preview-overlay').style.display = 'flex';
  document.body.style.overflow = 'hidden';
}

// إخفاء المعاينة
function hidePreview() {
  document.getElementById('preview-overlay').style.display = 'none';
  document.body.style.overflow = 'auto';
}

// إنشاء تقرير ملون
function generateColoredReport() {
  const data = collectFormData();
  
  if (!validateForm()) {
    showAlert('الرجاء تعبئة الحقول المطلوبة قبل الطباعة', 'error');
    return;
  }
  
  // عرض شاشة التحميل
  const loadingOverlay = document.getElementById('loading-overlay');
  loadingOverlay.style.display = 'flex';
  
  // محاكاة وقت التحميل
  setTimeout(() => {
    buildColoredReport(data);
    
    // انتظار لحظة لضمان تحميل الصور
    setTimeout(() => {
      // حفظ التقرير كصورة ثم PDF
      saveColoredReportAsImage();
      
      loadingOverlay.style.display = 'none';
      
      showAlert('تم إنشاء التقرير الملون بنجاح وسيبدأ التنزيل الآن', 'success');
    }, 1000);
  }, 1500);
}

// حفظ التقرير كصورة
function saveColoredReportAsImage() {
  const reportContent = document.getElementById('report-content');
  
  html2canvas(reportContent, {
    scale: 2,
    useCORS: true,
    allowTaint: true,
    backgroundColor: '#ffffff',
    logging: false,
    windowWidth: reportContent.scrollWidth,
    windowHeight: reportContent.scrollHeight
  }).then(canvas => {
    // تحويل Canvas إلى صورة
    const imgData = canvas.toDataURL('image/jpeg', 1.0);
    
    // إنشاء PDF باستخدام الصورة
    const pdf = new jsPDF({
      orientation: 'portrait',
      unit: 'mm',
      format: 'a4'
    });
    
    const imgWidth = 210; // A4 width in mm
    const pageHeight = 297; // A4 height in mm
    const imgHeight = (canvas.height * imgWidth) / canvas.width;
    
    let heightLeft = imgHeight;
    let position = 0;
    
    // إضافة الصورة الأولى
    pdf.addImage(imgData, 'JPEG', 0, position, imgWidth, imgHeight);
    heightLeft -= pageHeight;
    
    // إضافة صفحات إضافية إذا لزم الأمر
    while (heightLeft >= 0) {
      position = heightLeft - imgHeight;
      pdf.addPage();
      pdf.addImage(imgData, 'JPEG', 0, position, imgWidth, imgHeight);
      heightLeft -= pageHeight;
    }
    
    // حفظ الملف
    const fileName = `تقرير_تعليمي_ملون_${new Date().toISOString().split('T')[0]}.pdf`;
    pdf.save(fileName);
  });
}

// بناء التقرير الملون
function buildColoredReport(data) {
  const content = document.getElementById('report-content');
  
  const getDepartmentName = (value) => {
    const departments = {
      'الرياض': 'الإدارة العامة للتعليم بمنطقة الرياض',
      'مكة': 'الإدارة العامة للتعليم بمنطقة مكة المكرمة',
      'الشرقية': 'الإدارة العامة للتعليم بالمنطقة الشرقية',
      'المدينة': 'الإدارة العامة للتعليم بمنطقة المدينة المنورة',
      'القصيم': 'الإدارة العامة للتعليم بمنطقة القصيم'
    };
    return departments[value] || value;
  };

  const getReportTypeName = (type) => {
    const types = {
      'اثرائي': 'تقرير نشاط إثرائي',
      'علاجي': 'تقرير خطة علاجية',
      'تقويمي': 'تقرير تقويمي',
      'متابعة': 'تقرير متابعة',
      'بحثي': 'تقرير بحث علمي'
    };
    return types[type] || 'تقرير تعليمي';
  };

  const getCurrentDate = () => {
    const now = new Date();
    const date = now.getDate().toString().padStart(2, '0');
    const month = (now.getMonth() + 1).toString().padStart(2, '0');
    const year = now.getFullYear();
    const hijriYear = 1446;
    
    return `${date}/${month}/${year} م - ${hijriYear} هـ`;
  };

  // تحديد ألوان حسب النظام المختار
  const getColors = () => {
    const colors = {
      blue: {
        primary: '#2E86C1',
        secondary: '#27AE60',
        accent: '#E67E22'
      },
      green: {
        primary: '#27AE60',
        secondary: '#2E86C1',
        accent: '#E67E22'
      },
      orange: {
        primary: '#E67E22',
        secondary: '#2E86C1',
        accent: '#27AE60'
      },
      purple: {
        primary: '#8E44AD',
        secondary: '#27AE60',
        accent: '#E67E22'
      },
      pink: {
        primary: '#E84393',
        secondary: '#27AE60',
        accent: '#2E86C1'
      }
    };
    return colors[currentColorScheme] || colors.blue;
  };

  const colors = getColors();

  content.innerHTML = `
    <div class="report-header" style="background: linear-gradient(135deg, ${colors.primary}20, ${colors.secondary}20); border-bottom: 4px solid ${colors.primary};">
      <h1 style="color: ${colors.primary};">وزارة التعليم</h1>
      <h2 style="color: ${colors.secondary};">${getDepartmentName(data.department)}</h2>
      <h3 style="color: #2C3E50;">${data.school}</h3>
      <div class="report-date" style="background: white; border: 2px solid ${colors.accent}; color: ${colors.accent};">
        <i class="fas fa-calendar-alt" style="margin-left: 8px;"></i>
        ${getCurrentDate()} | ${getReportTypeName(data.type)} | الفصل ${data.semester}
      </div>
    </div>
    
    <div class="report-section" style="border-right-color: ${colors.primary}; background: linear-gradient(135deg, ${colors.primary}08, white);">
      <div class="report-section-title" style="border-bottom-color: ${colors.primary}; color: ${colors.primary};">
        <i class="fas fa-info-circle" style="background: linear-gradient(135deg, ${colors.primary}, ${colors.primary}cc);"></i>
        المعلومات الأساسية
      </div>
      <div class="report-section-content" style="border-right-color: ${colors.primary}30;">
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px;">
          <div style="background: ${colors.primary}10; padding: 12px; border-radius: 8px; border-right: 3px solid ${colors.primary};">
            <strong style="color: ${colors.primary};">المادة الدراسية:</strong><br>
            ${data.subject || 'غير محدد'}
          </div>
          <div style="background: ${colors.secondary}10; padding: 12px; border-radius: 8px; border-right: 3px solid ${colors.secondary};">
            <strong style="color: ${colors.secondary};">الفئة المستهدفة:</strong><br>
            ${data.target || 'غير محدد'}
          </div>
          <div style="background: ${colors.accent}10; padding: 12px; border-radius: 8px; border-right: 3px solid ${colors.accent};">
            <strong style="color: ${colors.accent};">الفصل الدراسي:</strong><br>
            الفصل ${data.semester}
          </div>
        </div>
      </div>
    </div>
    
    <div class="report-section" style="border-right-color: ${colors.secondary}; background: linear-gradient(135deg, ${colors.secondary}08, white);">
      <div class="report-section-title" style="border-bottom-color: ${colors.secondary}; color: ${colors.secondary};">
        <i class="fas fa-bullseye" style="background: linear-gradient(135deg, ${colors.secondary}, ${colors.secondary}cc);"></i>
        الهدف التربوي
      </div>
      <div class="report-section-content" style="border-right-color: ${colors.secondary}30; background: linear-gradient(135deg, ${colors.secondary}05, white);">
        ${data.goal}
      </div>
    </div>
    
    <div class="report-section" style="border-right-color: ${colors.primary}; background: linear-gradient(135deg, ${colors.primary}08, white);">
      <div class="report-section-title" style="border-bottom-color: ${colors.primary}; color: ${colors.primary};">
        <i class="fas fa-tasks" style="background: linear-gradient(135deg, ${colors.primary}, ${colors.primary}cc);"></i>
        إجراءات التنفيذ
      </div>
      <div class="report-section-content" style="border-right-color: ${colors.primary}30; background: linear-gradient(135deg, ${colors.primary}05, white);">
        ${data.steps || 'لم يتم تحديد إجراءات التنفيذ'}
      </div>
    </div>
    
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin-bottom: 30px;">
      <div class="report-section" style="border-right-color: ${colors.secondary}; background: linear-gradient(135deg, ${colors.secondary}08, white);">
        <div class="report-section-title" style="border-bottom-color: ${colors.secondary}; color: ${colors.secondary};">
          <i class="fas fa-chart-line" style="background: linear-gradient(135deg, ${colors.secondary}, ${colors.secondary}cc);"></i>
          النتائج المتحققة
        </div>
        <div class="report-section-content" style="border-right-color: ${colors.secondary}30; background: linear-gradient(135deg, ${colors.secondary}05, white);">
          ${data.results || 'لم يتم تحديد النتائج'}
        </div>
      </div>
      
      <div class="report-section" style="border-right-color: ${colors.accent}; background: linear-gradient(135deg, ${colors.accent}08, white);">
        <div class="report-section-title" style="border-bottom-color: ${colors.accent}; color: ${colors.accent};">
          <i class="fas fa-comments" style="background: linear-gradient(135deg, ${colors.accent}, ${colors.accent}cc);"></i>
          التوصيات والمقترحات
        </div>
        <div class="report-section-content" style="border-right-color: ${colors.accent}30; background: linear-gradient(135deg, ${colors.accent}05, white);">
          ${data.recommendations || 'لم يتم تحديد توصيات'}
        </div>
      </div>
    </div>
    
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin-bottom: 30px;">
      <div class="report-section" style="border-right-color: ${colors.primary}; background: linear-gradient(135deg, ${colors.primary}08, white);">
        <div class="report-section-title" style="border-bottom-color: ${colors.primary}; color: ${colors.primary};">
          <i class="fas fa-thumbs-up" style="background: linear-gradient(135deg, ${colors.primary}, ${colors.primary}cc);"></i>
          نقاط القوة
        </div>
        <div class="report-section-content" style="border-right-color: ${colors.primary}30; background: linear-gradient(135deg, ${colors.primary}05, white);">
          ${data.strengths || 'لم يتم تحديد نقاط القوة'}
        </div>
      </div>
      
      <div class="report-section" style="border-right-color: ${colors.secondary}; background: linear-gradient(135deg, ${colors.secondary}08, white);">
        <div class="report-section-title" style="border-bottom-color: ${colors.secondary}; color: ${colors.secondary};">
          <i class="fas fa-lightbulb" style="background: linear-gradient(135deg, ${colors.secondary}, ${colors.secondary}cc);"></i>
          فرص التحسين
        </div>
        <div class="report-section-content" style="border-right-color: ${colors.secondary}30; background: linear-gradient(135deg, ${colors.secondary}05, white);">
          ${data.improvements || 'لم يتم تحديد فرص التحسين'}
        </div>
      </div>
    </div>
    
    ${uploadedImages.length > 0 ? `
      <div class="report-section" style="border-right-color: #8E44AD; background: linear-gradient(135deg, #8E44AD08, white);">
        <div class="report-section-title" style="border-bottom-color: #8E44AD; color: #8E44AD;">
          <i class="fas fa-images" style="background: linear-gradient(135deg, #8E44AD, #8E44ADcc);"></i>
          الصور التوثيقية
        </div>
        <div class="report-images">
          ${uploadedImages.map((img, index) => `
            <div class="report-image" style="border: 2px solid ${colors.primary}40;">
              <img src="${img.data}" alt="صورة توثيقية ${index + 1}">
              <div style="padding: 8px; background: ${colors.primary}10; text-align: center; color: ${colors.primary}; font-size: 14px; border-top: 2px solid ${colors.primary}30;">
                <i class="fas fa-camera" style="margin-left: 5px;"></i>
                صورة ${index + 1}
              </div>
            </div>
          `).join('')}
        </div>
      </div>
    ` : ''}
    
    <div class="report-signatures" style="background: linear-gradient(135deg, ${colors.primary}05, ${colors.secondary}05); border-top: 2px solid ${colors.primary}50;">
      <div class="signature-box" style="border-top: 4px solid ${colors.primary};">
        <div class="signature-title" style="color: ${colors.primary};">
          <i class="fas fa-chalkboard-teacher"></i>
          المعلم / المشرف
        </div>
        <div class="signature-line" style="background: linear-gradient(90deg, transparent, ${colors.primary}, transparent);"></div>
        <div class="signature-name" style="background: ${colors.primary}10; border: 2px dashed ${colors.primary}40;">
          ${data.teacher}
        </div>
      </div>
      
      <div class="signature-box" style="border-top: 4px solid ${colors.secondary};">
        <div class="signature-title" style="color: ${colors.secondary};">
          <i class="fas fa-user-tie"></i>
          مدير المدرسة
        </div>
        <div class="signature-line" style="background: linear-gradient(90deg, transparent, ${colors.secondary}, transparent);"></div>
        <div class="signature-name" style="background: ${colors.secondary}10; border: 2px dashed ${colors.secondary}40;">
          ${data.principal || '.................'}
        </div>
      </div>
    </div>
    
    <div style="margin-top: 30px; padding: 20px; background: linear-gradient(135deg, ${colors.accent}05, white); border-radius: 12px; border: 2px solid ${colors.accent}30; text-align: center;">
      <div style="color: ${colors.accent}; font-size: 14px; display: flex; align-items: center; justify-content: center; gap: 10px;">
        <i class="fas fa-qrcode"></i>
        <span>تم إنشاء هذا التقرير بواسطة نظام التقارير التعليمية الملون</span>
      </div>
      <div style="color: #95a5a6; font-size: 12px; margin-top: 10px;">
        ${new Date().toLocaleString('ar-SA', { 
          year: 'numeric', 
          month: 'long', 
          day: 'numeric',
          hour: '2-digit',
          minute: '2-digit'
        })}
      </div>
    </div>
  `;
}

// جمع بيانات النموذج
function collectFormData() {
  return {
    department: document.getElementById('education-department').value,
    school: document.getElementById('school-name').value.trim(),
    type: document.getElementById('report-type').value,
    target: document.getElementById('target-audience').value.trim(),
    semester: document.getElementById('semester').value,
    subject: document.getElementById('subject').value.trim(),
    goal: document.getElementById('educational-goal').value.trim(),
    steps: document.getElementById('implementation-steps').value.trim(),
    results: document.getElementById('achieved-results').value.trim(),
    recommendations: document.getElementById('recommendations').value.trim(),
    strengths: document.getElementById('strengths').value.trim(),
    improvements: document.getElementById('improvements').value.trim(),
    teacher: document.getElementById('teacher-name').value.trim(),
    principal: document.getElementById('principal-name').value.trim()
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
  container.prepend(alert);
  
  // تحريك التنبيه
  alert.style.animation = 'slideIn 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55)';
  
  setTimeout(() => {
    if (alert.parentNode) {
      alert.style.animation = 'fadeOut 0.3s ease';
      setTimeout(() => {
        if (alert.parentNode) {
          alert.remove();
        }
      }, 300);
    }
  }, 5000);
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

// إغلاق التنبيه بالنقر
document.addEventListener('click', function(e) {
  if (e.target.closest('.alert')) {
    const alert = e.target.closest('.alert');
    alert.style.animation = 'fadeOut 0.3s ease';
    setTimeout(() => {
      if (alert.parentNode) {
        alert.remove();
      }
    }, 300);
  }
});

// إغلاق المعاينة بالزر ESC
document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') {
    hidePreview();
  }
});

// إغلاق المعاينة بالنقر خارجها
document.getElementById('preview-overlay').addEventListener('click', function(e) {
  if (e.target === this) {
    hidePreview();
  }
});

// دعم سحب وإفلات الصور
const uploadArea = document.querySelector('.upload-area');
uploadArea.addEventListener('dragover', (e) => {
  e.preventDefault();
  uploadArea.style.borderColor = 'var(--primary)';
  uploadArea.style.background = 'rgba(46, 134, 193, 0.15)';
  uploadArea.style.transform = 'scale(1.02)';
});

uploadArea.addEventListener('dragleave', () => {
  uploadArea.style.borderColor = '';
  uploadArea.style.background = '';
  uploadArea.style.transform = '';
});

uploadArea.addEventListener('drop', (e) => {
  e.preventDefault();
  uploadArea.style.borderColor = '';
  uploadArea.style.background = '';
  uploadArea.style.transform = '';
  
  const files = Array.from(e.dataTransfer.files);
  const input = document.getElementById('image-upload');
  
  // إنشاء DataTransfer object لتحديث الملفات
  const dataTransfer = new DataTransfer();
  files.forEach(file => dataTransfer.items.add(file));
  input.files = dataTransfer.files;
  
  handleImageUpload(input);
});

// تحسين تجربة اللمس
document.addEventListener('DOMContentLoaded', function() {
  // تحميل المسودة المحفوظة
  loadFromLocalStorage();
  
  // إضافة تأثير اللمس للأزرار
  document.querySelectorAll('.action-btn, .template-btn').forEach(btn => {
    btn.addEventListener('touchstart', function() {
      this.style.transform = 'scale(0.98)';
    });
    
    btn.addEventListener('touchend', function() {
      this.style.transform = '';
    });
  });
  
  // إضافة مقياس الأحرف
  const style = document.createElement('style');
  style.textContent = `
    .char-counter {
      text-align: left;
      font-size: 12px;
      margin-top: 5px;
      padding: 4px 8px;
      background: rgba(46, 134, 193, 0.05);
      border-radius: 4px;
      display: inline-block;
      border-right: 2px solid var(--primary);
    }
    
    @keyframes fadeOut {
      from { opacity: 1; transform: translateX(0); }
      to { opacity: 0; transform: translateX(30px); }
    }
    
    .form-hint {
      font-size: 13px;
      color: var(--dark-gray);
      margin-top: 5px;
      display: flex;
      align-items: center;
      gap: 6px;
    }
    
    .form-hint i {
      color: var(--accent);
    }
  `;
  document.head.appendChild(style);
});

// التمرير السلس
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function (e) {
    e.preventDefault();
    const targetId = this.getAttribute('href');
    if (targetId === '#') return;
    
    const targetElement = document.querySelector(targetId);
    if (targetElement) {
      targetElement.scrollIntoView({
        behavior: 'smooth',
        block: 'start'
      });
    }
  });
});

// إضافة تأثيرات للصور عند التمرير
const observerOptions = {
  threshold: 0.1,
  rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.style.opacity = '1';
      entry.target.style.transform = 'translateY(0)';
    }
  });
}, observerOptions);

// مراقبة عناصر التقرير
document.querySelectorAll('.report-section, .report-image').forEach(el => {
  el.style.opacity = '0';
  el.style.transform = 'translateY(20px)';
  el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
  observer.observe(el);
});
</script>

<!-- إضافة مكتبات jsPDF و html2canvas -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
<script>
// تهيئة jsPDF
window.jsPDF = window.jspdf.jsPDF;
</script>
</body>
</html>
