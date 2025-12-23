<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>أداة التقارير التعليمية | وزارة التعليم</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --primary: #1B4F72;
  --primary-light: #2E86C1;
  --secondary: #196F3D;
  --secondary-light: #27AE60;
  --accent: #CA6F1E;
  --accent-light: #E67E22;
  --light: #F8F9FA;
  --light-gray: #EAECEE;
  --medium-gray: #BFC9CA;
  --dark: #2C3E50;
  --dark-gray: #566573;
  --success: #27AE60;
  --warning: #F39C12;
  --danger: #E74C3C;
  --border-radius: 12px;
  --box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  --box-shadow-hover: 0 8px 20px rgba(0, 0, 0, 0.12);
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
  background: linear-gradient(135deg, #f0f9ff 0%, #f0fff4 100%);
  color: var(--dark);
  line-height: 1.6;
  min-height: 100vh;
  padding: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 15px;
}

/* الهيدر مع خلفية شعار الوزارة */
.header {
  background: linear-gradient(rgba(27, 79, 114, 0.95), rgba(27, 79, 114, 0.98)), 
              url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiB2aWV3Qm94PSIwIDAgMTI4MCAxNDAiIHByZXNlcnZlQXNwZWN0UmF0aW89Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGcgZmlsbD0ibm9uZSIgZmlsbC1ydWxlPSJldmVub2RkIj48cGF0aCBkPSJNMTI4MCAxMzkuNUgwdjIuNWgxMjgweiIgZmlsbD0iIzAwMCIvPjxwYXRoIGQ9Ik0wIDBoMTI4MHYxNDBIMHoiIGZpbGw9InVybCgjYSkiLz48cGF0aCBkPSJNMCAwaDEyODB2MTQwSDB6IiBmaWxsPSJ1cmwoI2IpIi8+PHBhdGggZD0iTTEwNS44IDY4LjNsNy4yLTEyLjUgNy4zIDEyLjVoLTE0LjV6IiBmaWxsPSIjRkZGIi8+PHBhdGggZD0iTTEyMi4xIDU3LjhoMTAuM3YyMS4xaC0xMC4zeiIgZmlsbD0iI0ZGRiIvPjxwYXRoIGQ9Ik0xNDQuMSA3MS4zbDcuMi0xMi41IDcuMyAxMi41aC0xNC41eiIgZmlsbD0iI0ZGRiIvPjxwYXRoIGQ9Ik0xNjAuNCA1Ny44aDEwLjN2MjEuMWgtMTAuM3oiIGZpbGw9IiNGRkYiLz48cGF0aCBkPSJNMTgyLjQgNzEuM2w3LjItMTIuNSA3LjMgMTIuNWgtMTQuNXoiIGZpbGw9IiNGRkYiLz48L2c+PGRlZnM+PGxpbmVhckdyYWRpZW50IGlkPSJhIiB4MT0iMCUiIHkxPSIwJSIgeDI9IjEwMCUiIHkyPSIxMDAlIj48c3RvcCBzdG9wLWNvbG9yPSIjMUI0RjcyIiBvZmZzZXQ9IjAlIi8+PHN0b3Agc3RvcC1jb2xvcj0iIzJFODZDMSIgb2Zmc2V0PSIxMDAlIi8+PC9saW5lYXJHcmFkaWVudD48bGluZWFyR3JhZGllbnQgaWQ9ImIiIHgxPSIwJSIgeTE9IjAlIiB4Mj0iMTAwJSIgeTI9IjEwMCUiPjxzdG9wIHN0b3AtY29sb3I9InJnYmEoMjYsNjYsMTE0LDAuMykiIG9mZnNldD0iMCUiLz48c3RvcCBzdG9wLWNvbG9yPSJyZ2JhKDI2LDY2LDExNCwwKSIgb2Zmc2V0PSIxMDAlIi8+PC9saW5lYXJHcmFkaWVudD48L2RlZnM+PC9zdmc+') center/cover;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: 20px 15px;
  margin-bottom: 20px;
  color: white;
  position: relative;
  overflow: hidden;
  min-height: 150px;
  display: flex;
  align-items: center;
}

.header-content {
  position: relative;
  z-index: 2;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 15px;
  width: 100%;
}

@media (max-width: 768px) {
  .header-content {
    flex-direction: column;
    text-align: center;
    gap: 12px;
  }
  
  .header {
    min-height: 140px;
    padding: 15px 12px;
  }
}

@media (max-width: 480px) {
  .header {
    min-height: 130px;
    padding: 12px 10px;
  }
}

.logo-section {
  display: flex;
  align-items: center;
  gap: 12px;
  flex: 1;
  min-width: 0;
}

.logo-icon {
  width: 55px;
  height: 55px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 24px;
  backdrop-filter: blur(10px);
  border: 2px solid rgba(255, 255, 255, 0.3);
  flex-shrink: 0;
}

@media (max-width: 480px) {
  .logo-icon {
    width: 45px;
    height: 45px;
    font-size: 20px;
  }
}

.logo-text {
  flex: 1;
  min-width: 0;
}

.logo-text h1 {
  font-size: 18px;
  font-weight: 700;
  margin-bottom: 5px;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
  line-height: 1.3;
}

@media (max-width: 768px) {
  .logo-text h1 {
    font-size: 16px;
  }
}

.logo-text p {
  font-size: 13px;
  opacity: 0.95;
  font-weight: 300;
  line-height: 1.4;
}

@media (max-width: 768px) {
  .logo-text p {
    font-size: 12px;
  }
}

.header-stats {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
  justify-content: center;
  flex-shrink: 0;
}

@media (max-width: 768px) {
  .header-stats {
    gap: 6px;
  }
}

.stat-item {
  background: rgba(255, 255, 255, 0.15);
  padding: 6px 10px;
  border-radius: 20px;
  font-size: 12px;
  display: flex;
  align-items: center;
  gap: 5px;
  backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  white-space: nowrap;
}

@media (max-width: 480px) {
  .stat-item {
    font-size: 11px;
    padding: 5px 8px;
  }
  
  .stat-item i {
    font-size: 12px;
  }
}

/* شريط التنقل للجوال */
.mobile-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: white;
  box-shadow: 0 -4px 15px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  padding: 10px 5px;
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

@media (max-width: 480px) {
  .mobile-nav {
    padding: 8px 4px;
  }
}

.nav-btn {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
  background: none;
  border: none;
  color: var(--dark-gray);
  font-size: 11px;
  padding: 6px 3px;
  cursor: pointer;
  flex: 1;
  transition: var(--transition);
  border-radius: 8px;
  min-width: 0;
}

.nav-btn:hover, .nav-btn.active {
  color: var(--primary);
  background: rgba(27, 79, 114, 0.08);
}

.nav-btn i {
  font-size: 16px;
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

@media (max-width: 480px) {
  .nav-btn {
    font-size: 10px;
    padding: 5px 2px;
    gap: 3px;
  }
  
  .nav-btn i {
    font-size: 15px;
  }
}

/* المحتوى الرئيسي */
.main-content {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
}

@media (min-width: 992px) {
  .main-content {
    grid-template-columns: 1fr 350px;
  }
}

@media (max-width: 768px) {
  .main-content {
    gap: 15px;
  }
}

/* لوحة التحكم */
.control-panel {
  background: white;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: 20px;
  height: fit-content;
  position: sticky;
  top: 20px;
  border: 1px solid var(--light-gray);
}

@media (max-width: 992px) {
  .control-panel {
    position: relative;
    top: 0;
  }
}

@media (max-width: 768px) {
  .control-panel {
    padding: 15px;
  }
}

.control-panel h3 {
  color: var(--primary);
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid var(--primary-light);
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 17px;
}

@media (max-width: 768px) {
  .control-panel h3 {
    font-size: 16px;
  }
}

/* القوالب السريعة */
.quick-templates {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
  margin-bottom: 20px;
}

.template-btn {
  background: white;
  border: 2px solid var(--light-gray);
  border-radius: 10px;
  padding: 12px 8px;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.template-btn:hover {
  border-color: var(--primary);
  transform: translateY(-2px);
  box-shadow: var(--box-shadow-hover);
}

.template-btn i {
  font-size: 22px;
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

@media (max-width: 768px) {
  .template-btn {
    padding: 10px 6px;
  }
  
  .template-btn i {
    font-size: 20px;
  }
}

.template-btn span {
  font-size: 13px;
  font-weight: 600;
  color: var(--dark);
}

@media (max-width: 768px) {
  .template-btn span {
    font-size: 12px;
  }
}

/* أزرار التحكم */
.action-buttons {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-top: 20px;
}

.action-btn {
  padding: 14px;
  border: none;
  border-radius: 10px;
  font-family: 'Cairo', sans-serif;
  font-size: 15px;
  font-weight: 600;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  position: relative;
  overflow: hidden;
}

.action-btn i {
  font-size: 16px;
}

@media (max-width: 768px) {
  .action-btn {
    padding: 12px;
    font-size: 14px;
  }
  
  .action-btn i {
    font-size: 15px;
  }
}

.btn-preview {
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  color: white;
}

.btn-preview:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 15px rgba(27, 79, 114, 0.3);
}

.btn-print {
  background: linear-gradient(135deg, var(--accent), var(--accent-light));
  color: white;
}

.btn-print:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 15px rgba(230, 126, 34, 0.3);
}

.btn-save {
  background: linear-gradient(135deg, #17A589, #48C9B0);
  color: white;
}

.btn-save:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 15px rgba(23, 165, 137, 0.3);
}

.btn-clear {
  background: linear-gradient(135deg, #E74C3C, #C0392B);
  color: white;
}

.btn-clear:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 15px rgba(231, 76, 60, 0.3);
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
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  color: white;
  padding: 18px 20px;
  position: relative;
  overflow: hidden;
}

@media (max-width: 768px) {
  .form-header {
    padding: 15px 18px;
  }
}

.form-header h2 {
  font-size: 18px;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 10px;
  position: relative;
  z-index: 1;
}

@media (max-width: 768px) {
  .form-header h2 {
    font-size: 17px;
  }
}

.form-content {
  padding: 20px;
}

@media (max-width: 768px) {
  .form-content {
    padding: 15px;
  }
}

/* أقسام النموذج */
.form-section {
  margin-bottom: 25px;
  padding: 18px;
  background: var(--light);
  border-radius: var(--border-radius);
  border-right: 4px solid var(--primary);
}

@media (max-width: 768px) {
  .form-section {
    padding: 15px;
    margin-bottom: 20px;
  }
}

.section-title {
  font-size: 17px;
  font-weight: 600;
  color: var(--primary);
  margin-bottom: 15px;
  padding-bottom: 8px;
  border-bottom: 2px solid var(--primary-light);
  display: flex;
  align-items: center;
  gap: 8px;
}

@media (max-width: 768px) {
  .section-title {
    font-size: 16px;
  }
}

.section-title i {
  color: var(--primary);
  background: rgba(27, 79, 114, 0.1);
  width: 32px;
  height: 32px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

@media (max-width: 768px) {
  .section-title i {
    width: 28px;
    height: 28px;
    font-size: 14px;
  }
}

/* الحقول */
.form-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 15px;
}

@media (max-width: 768px) {
  .form-grid {
    grid-template-columns: 1fr;
    gap: 12px;
  }
}

.form-group {
  margin-bottom: 15px;
}

.form-label {
  display: block;
  font-size: 14px;
  font-weight: 600;
  color: var(--dark);
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  gap: 8px;
}

@media (max-width: 768px) {
  .form-label {
    font-size: 13.5px;
  }
}

.form-label i {
  color: var(--primary);
  width: 22px;
  height: 22px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(27, 79, 114, 0.1);
  border-radius: 5px;
  flex-shrink: 0;
}

.form-control {
  width: 100%;
  padding: 12px 14px;
  border: 2px solid var(--light-gray);
  border-radius: 8px;
  font-family: 'Cairo', sans-serif;
  font-size: 14px;
  color: var(--dark);
  transition: var(--transition);
  background: white;
  -webkit-appearance: none;
}

.form-control:focus {
  outline: none;
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(27, 79, 114, 0.1);
}

@media (max-width: 768px) {
  .form-control {
    padding: 11px 13px;
    font-size: 16px; /* منع التكبير في iOS */
  }
}

textarea.form-control {
  min-height: 100px;
  resize: vertical;
  line-height: 1.6;
}

/* منطقة رفع الصور */
.upload-area {
  border: 3px dashed var(--primary-light);
  border-radius: 10px;
  padding: 25px;
  text-align: center;
  cursor: pointer;
  transition: var(--transition);
  margin-bottom: 15px;
  background: rgba(27, 79, 114, 0.05);
  touch-action: manipulation;
}

.upload-area:hover {
  border-color: var(--primary);
  background: rgba(27, 79, 114, 0.1);
}

@media (max-width: 768px) {
  .upload-area {
    padding: 20px;
  }
}

.upload-area i {
  font-size: 42px;
  color: var(--primary);
  margin-bottom: 12px;
  display: block;
}

@media (max-width: 768px) {
  .upload-area i {
    font-size: 36px;
  }
}

.upload-area p {
  color: var(--dark);
  font-size: 15px;
  margin-bottom: 6px;
  font-weight: 500;
}

@media (max-width: 768px) {
  .upload-area p {
    font-size: 14px;
  }
}

.upload-area small {
  font-size: 12px;
  color: var(--dark-gray);
}

.image-preview {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
  gap: 12px;
  margin-top: 15px;
}

@media (max-width: 480px) {
  .image-preview {
    grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    gap: 10px;
  }
}

.preview-image {
  position: relative;
  border-radius: 8px;
  overflow: hidden;
  height: 120px;
  box-shadow: var(--box-shadow);
  transition: var(--transition);
}

@media (max-width: 480px) {
  .preview-image {
    height: 100px;
  }
}

.preview-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.remove-image {
  position: absolute;
  top: 6px;
  left: 6px;
  background: linear-gradient(135deg, var(--danger), #C0392B);
  color: white;
  width: 26px;
  height: 26px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: var(--transition);
  opacity: 0.9;
  font-size: 12px;
  touch-action: manipulation;
}

.remove-image:hover {
  opacity: 1;
  transform: scale(1.1);
}

/* قسم التوقيعات */
.signatures-section {
  background: linear-gradient(135deg, rgba(27, 79, 114, 0.05), rgba(39, 174, 96, 0.05));
  border-radius: 10px;
  padding: 20px;
  margin-top: 20px;
  border: 1px solid rgba(27, 79, 114, 0.15);
}

@media (max-width: 768px) {
  .signatures-section {
    padding: 15px;
  }
}

.signatures-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

@media (max-width: 768px) {
  .signatures-grid {
    grid-template-columns: 1fr;
    gap: 15px;
  }
}

.signature-field {
  text-align: center;
  background: white;
  padding: 18px;
  border-radius: 8px;
  box-shadow: var(--box-shadow);
}

@media (max-width: 768px) {
  .signature-field {
    padding: 15px;
  }
}

.signature-input {
  width: 100%;
  padding: 12px;
  border: 2px solid var(--light-gray);
  border-radius: 8px;
  font-family: 'Cairo', sans-serif;
  font-size: 15px;
  text-align: center;
  background: white;
  margin-top: 10px;
  transition: var(--transition);
}

.signature-input:focus {
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(27, 79, 114, 0.1);
}

/* التنبيهات */
.alert {
  padding: 12px 16px;
  border-radius: 8px;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 14px;
  animation: slideIn 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
  border-right: 4px solid;
  position: fixed;
  top: 20px;
  left: 15px;
  right: 15px;
  z-index: 10000;
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
  max-width: 500px;
  margin-left: auto;
  margin-right: auto;
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

@media (max-width: 768px) {
  .alert {
    left: 10px;
    right: 10px;
    font-size: 13px;
    padding: 10px 14px;
  }
}

.alert-success {
  background: linear-gradient(135deg, rgba(39, 174, 96, 0.95), rgba(46, 204, 113, 0.95));
  color: white;
  border-right-color: var(--success);
}

.alert-warning {
  background: linear-gradient(135deg, rgba(243, 156, 18, 0.95), rgba(245, 176, 65, 0.95));
  color: white;
  border-right-color: var(--warning);
}

.alert-error {
  background: linear-gradient(135deg, rgba(231, 76, 60, 0.95), rgba(235, 110, 98, 0.95));
  color: white;
  border-right-color: var(--danger);
}

.alert-info {
  background: linear-gradient(135deg, rgba(52, 152, 219, 0.95), rgba(93, 173, 226, 0.95));
  color: white;
  border-right-color: var(--primary);
}

/* نافذة المعاينة */
.preview-overlay {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.95);
  display: none;
  align-items: center;
  justify-content: center;
  z-index: 2000;
  padding: 15px;
  backdrop-filter: blur(10px);
}

.preview-container {
  background: white;
  border-radius: var(--border-radius);
  width: 100%;
  max-width: 800px;
  max-height: 90vh;
  overflow-y: auto;
  position: relative;
  animation: scaleIn 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4);
}

@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.95);
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
  padding: 18px 20px;
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  color: white;
  position: sticky;
  top: 0;
  z-index: 10;
  border-radius: var(--border-radius) var(--border-radius) 0 0;
}

@media (max-width: 768px) {
  .preview-header {
    padding: 15px 18px;
  }
}

.close-preview {
  background: rgba(255, 255, 255, 0.2);
  border: none;
  color: white;
  font-size: 18px;
  cursor: pointer;
  padding: 6px;
  width: 36px;
  height: 36px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: var(--transition);
  touch-action: manipulation;
}

.close-preview:hover {
  background: rgba(255, 255, 255, 0.3);
  transform: rotate(90deg);
}

/* تصميم التقرير للطباعة */
.report-content {
  padding: 25px;
  font-family: 'Cairo', sans-serif;
  background: white;
}

@media (max-width: 768px) {
  .report-content {
    padding: 20px;
  }
}

/* الهدف التربوي في الأعلى */
.goal-section {
  background: linear-gradient(135deg, #27AE60, #2ECC71);
  color: white;
  padding: 25px;
  border-radius: 12px;
  margin-bottom: 25px;
  text-align: center;
  box-shadow: var(--box-shadow);
  border-right: 6px solid #229954;
}

@media (max-width: 768px) {
  .goal-section {
    padding: 20px;
    margin-bottom: 20px;
  }
}

.goal-section h3 {
  font-size: 20px;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

@media (max-width: 768px) {
  .goal-section h3 {
    font-size: 18px;
  }
}

.goal-section .goal-content {
  background: rgba(255, 255, 255, 0.15);
  padding: 20px;
  border-radius: 10px;
  font-size: 16px;
  line-height: 1.8;
  text-align: right;
  backdrop-filter: blur(10px);
  border: 2px solid rgba(255, 255, 255, 0.3);
  max-height: 200px;
  overflow-y: auto;
}

@media (max-width: 768px) {
  .goal-section .goal-content {
    padding: 15px;
    font-size: 15px;
    max-height: 180px;
  }
}

/* الصف الثاني: إجراءات التنفيذ والنتائج المتحققة */
.row-2 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin-bottom: 25px;
}

@media (max-width: 768px) {
  .row-2 {
    grid-template-columns: 1fr;
    gap: 15px;
    margin-bottom: 20px;
  }
}

.implementation-box, .results-box {
  padding: 20px;
  border-radius: 12px;
  box-shadow: var(--box-shadow);
  min-height: 250px;
  max-height: 300px;
  overflow-y: auto;
}

@media (max-width: 768px) {
  .implementation-box, .results-box {
    padding: 15px;
    min-height: 220px;
  }
}

.implementation-box {
  background: linear-gradient(135deg, #3498DB, #5DADE2);
  color: white;
  border-right: 6px solid #2980B9;
}

.results-box {
  background: linear-gradient(135deg, #9B59B6, #BB8FCE);
  color: white;
  border-right: 6px solid #8E44AD;
}

.implementation-box h4, .results-box h4 {
  font-size: 18px;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  gap: 10px;
}

@media (max-width: 768px) {
  .implementation-box h4, .results-box h4 {
    font-size: 16px;
  }
}

.implementation-content, .results-content {
  background: rgba(255, 255, 255, 0.15);
  padding: 15px;
  border-radius: 8px;
  font-size: 15px;
  line-height: 1.7;
  min-height: 180px;
  overflow-y: auto;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

/* الصف الثالث: التوصيات ونقاط القوة */
.row-3 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin-bottom: 25px;
}

@media (max-width: 768px) {
  .row-3 {
    grid-template-columns: 1fr;
    gap: 15px;
    margin-bottom: 20px;
  }
}

.recommendations-box, .strengths-box {
  padding: 20px;
  border-radius: 12px;
  box-shadow: var(--box-shadow);
  min-height: 220px;
  max-height: 250px;
  overflow-y: auto;
}

@media (max-width: 768px) {
  .recommendations-box, .strengths-box {
    padding: 15px;
    min-height: 200px;
  }
}

.recommendations-box {
  background: linear-gradient(135deg, #2E86C1, #5DADE2);
  color: white;
  border-right: 6px solid #1B4F72;
}

.strengths-box {
  background: linear-gradient(135deg, #58D68D, #ABEBC6);
  color: #196F3D;
  border-right: 6px solid #27AE60;
}

.recommendations-box h4, .strengths-box h4 {
  font-size: 18px;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  gap: 10px;
}

@media (max-width: 768px) {
  .recommendations-box h4, .strengths-box h4 {
    font-size: 16px;
  }
}

.recommendations-content, .strengths-content {
  background: rgba(255, 255, 255, 0.2);
  padding: 15px;
  border-radius: 8px
  font-size: 15px;
  line-height: 1.7;
  min-height: 150px;
  overflow-y: auto;
}

/* فرص التحسين في الأسفل */
.improvements-box {
  background: linear-gradient(135deg, #E67E22, #F39C12);
  color: white;
  padding: 25px;
  border-radius: 12px;
  box-shadow: var(--box-shadow);
  margin-bottom: 25px;
  border-right: 6px solid #D35400;
  min-height: 200px;
  max-height: 250px;
  overflow-y: auto;
}

@media (max-width: 768px) {
  .improvements-box {
    padding: 20px;
    margin-bottom: 20px;
    min-height: 180px;
  }
}

.improvements-box h4 {
  font-size: 20px;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  gap: 10px;
}

@media (max-width: 768px) {
  .improvements-box h4 {
    font-size: 18px;
  }
}

.improvements-content {
  background: rgba(255, 255, 255, 0.2);
  padding: 20px;
  border-radius: 10px;
  font-size: 16px;
  line-height: 1.8;
  min-height: 130px;
  overflow-y: auto;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.3);
}

@media (max-width: 768px) {
  .improvements-content {
    padding: 15px;
    font-size: 15px;
    min-height: 120px;
  }
}

/* قسم الصور */
.images-section {
  margin-bottom: 25px;
}

.images-section h4 {
  font-size: 18px;
  color: var(--primary);
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.report-images {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
}

@media (max-width: 768px) {
  .report-images {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 12px;
  }
}

.report-image {
  border: 3px solid var(--light-gray);
  border-radius: 10px;
  overflow: hidden;
  transition: var(--transition);
  box-shadow: var(--box-shadow);
  height: 180px;
}

@media (max-width: 768px) {
  .report-image {
    height: 150px;
  }
}

.report-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* التوقيعات */
.report-signatures {
  display: flex;
  justify-content: space-between;
  margin-top: 30px;
  padding-top: 20px;
  border-top: 2px solid var(--primary-light);
  flex-wrap: wrap;
  gap: 20px;
}

@media (max-width: 768px) {
  .report-signatures {
    flex-direction: column;
    align-items: center;
    margin-top: 25px;
    gap: 15px;
  }
}

.signature-box {
  text-align: center;
  flex: 1;
  min-width: 200px;
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: var(--box-shadow);
  border-top: 4px solid var(--primary);
}

@media (max-width: 768px) {
  .signature-box {
    width: 100%;
    padding: 15px;
  }
}

.signature-title {
  font-size: 16px;
  font-weight: 700;
  color: var(--primary);
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

.signature-name {
  font-size: 16px;
  color: var(--dark);
  margin-top: 15px;
  padding: 12px;
  background: rgba(27, 79, 114, 0.05);
  border-radius: 8px;
  font-weight: 600;
  border: 2px dashed rgba(27, 79, 114, 0.2);
}

.signature-line {
  width: 150px;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--primary), transparent);
  margin: 15px auto;
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
  background: linear-gradient(135deg, rgba(27, 79, 114, 0.3), rgba(39, 174, 96, 0.3));
  padding: 30px;
  border-radius: 15px;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

@media (max-width: 768px) {
  .loading-content {
    padding: 20px;
  }
}

.loading-spinner {
  width: 60px;
  height: 60px;
  border: 4px solid rgba(255, 255, 255, 0.1);
  border-top-color: var(--primary-light);
  border-radius: 50%;
  animation: spin 1s linear infinite;
  margin-bottom: 20px;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

@media (max-width: 768px) {
  .loading-spinner {
    width: 50px;
    height: 50px;
  }
}

.loading-overlay p {
  font-size: 18px;
  margin-bottom: 10px;
  font-weight: 600;
}

@media (max-width: 768px) {
  .loading-overlay p {
    font-size: 16px;
  }
}

.loading-overlay small {
  font-size: 13px;
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
    padding: 15mm;
    font-size: 12pt;
  }
  
  .goal-section, .implementation-box, .results-box,
  .recommendations-box, .strengths-box, .improvements-box {
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
  width: 8px;
  height: 8px;
}

::-webkit-scrollbar-track {
  background: rgba(27, 79, 114, 0.1);
  border-radius: 10px;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(135deg, var(--primary), var(--primary));
}

/* عدادات الأحرف */
.char-counter {
  text-align: left;
  font-size: 12px;
  margin-top: 5px;
  padding: 4px 8px;
  background: rgba(27, 79, 114, 0.05);
  border-radius: 4px;
  display: inline-block;
  border-right: 2px solid var(--primary);
  color: var(--dark-gray);
}

.char-limit {
  color: #e74c3c;
  font-weight: bold;
}

.form-hint {
  font-size: 12px;
  color: var(--dark-gray);
  margin-top: 5px;
  display: flex;
  align-items: center;
  gap: 5px;
}

.form-hint i {
  color: var(--accent);
}

/* تحسينات للجوال الصغير جداً */
@media (max-width: 480px) {
  .container {
    padding: 10px 8px;
  }
  
  .header {
    min-height: 120px;
    padding: 12px 10px;
  }
  
  .logo-icon {
    width: 40px;
    height: 40px;
    font-size: 18px;
  }
  
  .logo-text h1 {
    font-size: 15px;
    margin-bottom: 3px;
  }
  
  .logo-text p {
    font-size: 11px;
  }
  
  .stat-item {
    font-size: 10px;
    padding: 4px 6px;
  }
  
  .stat-item i {
    font-size: 11px;
  }
  
  .form-content {
    padding: 12px;
  }
  
  .form-section {
    padding: 12px;
  }
  
  .section-title {
    font-size: 15px;
  }
  
  .section-title i {
    width: 26px;
    height: 26px;
    font-size: 13px;
  }
  
  .form-control {
    padding: 10px 12px;
    font-size: 14px;
  }
  
  .upload-area {
    padding: 15px;
  }
  
  .upload-area i {
    font-size: 32px;
  }
  
  .upload-area p {
    font-size: 13px;
  }
  
  .upload-area small {
    font-size: 11px;
  }
  
  .preview-image {
    height: 90px;
  }
  
  .action-btn {
    padding: 10px;
    font-size: 13px;
  }
  
  .action-btn i {
    font-size: 14px;
  }
  
  .template-btn {
    padding: 8px 4px;
  }
  
  .template-btn i {
    font-size: 18px;
  }
  
  .template-btn span {
    font-size: 11px;
  }
  
  .mobile-nav {
    padding: 6px 3px;
  }
  
  .nav-btn {
    font-size: 9px;
    padding: 4px 1px;
  }
  
  .nav-btn i {
    font-size: 14px;
  }
}

/* تحسينات اللمس */
@media (hover: none) and (pointer: coarse) {
  .action-btn:active, .template-btn:active {
    transform: scale(0.98);
  }
  
  .form-control, .signature-input {
    font-size: 16px; /* منع التكبير في iOS */
  }
  
  /* تحسينات للأزرار على الجوال */
  button, .action-btn, .template-btn {
    min-height: 44px; /* الحد الأدنى للزر للجوال */
  }
  
  input, textarea, select {
    font-size: 16px; /* منع التكبير التلقائي في iOS */
  }
}

/* تحسينات للوضع الأفقي في الجوال */
@media (max-height: 500px) and (orientation: landscape) {
  .header {
    min-height: 100px;
    padding: 10px;
  }
  
  .mobile-nav {
    display: none; /* إخفاء شريط التنقل في الوضع الأفقي */
  }
  
  .container {
    padding-bottom: 20px;
  }
}

/* تحسينات خاصة لآيفون */
@supports (-webkit-touch-callout: none) {
  input, textarea {
    font-size: 16px !important;
  }
}
</style>
</head>
<body>
<div class="container">
  <!-- الهيدر مع خلفية شعار الوزارة -->
  <header class="header">
    <div class="header-content">
      <div class="logo-section">
        <div class="logo-icon">
          <i class="fas fa-graduation-cap"></i>
        </div>
        <div class="logo-text">
          <h1>أداة التقارير التعليمية الذكية</h1>
          <p>وزارة التعليم - إعداد تقارير احترافية</p>
        </div>
      </div>
      
      <div class="header-stats">
        <div class="stat-item">
          <i class="fas fa-check-circle"></i>
          <span>بيانات مؤمنة</span>
        </div>
        <div class="stat-item">
          <i class="fas fa-print"></i>
          <span>طباعة مباشرة</span>
        </div>
        <div class="stat-item">
          <i class="fas fa-mobile-alt"></i>
          <span>متجاوب</span>
        </div>
      </div>
    </div>
  </header>

  <!-- المحتوى الرئيسي -->
  <div class="main-content">
    <!-- نموذج الإدخال -->
    <main class="form-container">
      <div class="form-header">
        <h2><i class="fas fa-file-alt"></i> إنشاء تقرير تعليمي</h2>
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
                     placeholder="أدخل اسم المدرسة" required>
              <div class="form-hint">
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
                <option value="الرياض">تعليم الرياض</option>
                <option value="مكة">تعليم مكة</option>
                <option value="الشرقية">تعليم الشرقية</option>
                <option value="المدينة">تعليم المدينة</option>
                <option value="القصيم">تعليم القصيم</option>
              </select>
            </div>
          </div>
        </div>

        <!-- معلومات التقرير -->
        <div class="form-section">
          <h3 class="section-title">
            <i class="fas fa-info-circle"></i>
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
                     placeholder="مثال: طلاب الصف الثالث الثانوي">
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
                     placeholder="مثال: الرياضيات - الفيزياء">
            </div>
          </div>
        </div>

        <!-- محتوى التقرير - صفحة واحدة -->
        <div class="form-section">
          <h3 class="section-title">
            <i class="fas fa-edit"></i>
            محتوى التقرير (صفحة واحدة)
          </h3>
          
          <div class="form-group">
            <label class="form-label">
              <i class="fas fa-bullseye"></i>
              الهدف التربوي (الأخضر - أعلى الصفحة)
            </label>
            <textarea class="form-control" id="educational-goal" 
                      placeholder="اكتب الهدف التربوي هنا (حد أقصى 250 حرف)..." 
                      rows="3" maxlength="250" required></textarea>
            <div class="char-counter" id="goal-counter">0/250 حرف</div>
          </div>
          
          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-tasks"></i>
                إجراءات التنفيذ (الأزرق - الصف الثاني)
              </label>
              <textarea class="form-control" id="implementation-steps" 
                        placeholder="صف إجراءات التنفيذ هنا (حد أقصى 250 حرف)..." 
                        rows="3" maxlength="250"></textarea>
              <div class="char-counter" id="steps-counter">0/250 حرف</div>
            </div>
            
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-chart-line"></i>
                النتائج المتحققة (البنفسجي - الصف الثاني)
              </label>
              <textarea class="form-control" id="achieved-results" 
                        placeholder="سجل النتائج المتحققة هنا (حد أقصى 250 حرف)..." 
                        rows="3" maxlength="250"></textarea>
              <div class="char-counter" id="results-counter">0/250 حرف</div>
            </div>
          </div>
          
          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-comments"></i>
                التوصيات (الأزرق - الصف الثالث)
              </label>
              <textarea class="form-control" id="recommendations" 
                        placeholder="اكتب التوصيات هنا (حد أقصى 250 حرف)..." 
                        rows="3" maxlength="250"></textarea>
              <div class="char-counter" id="rec-counter">0/250 حرف</div>
            </div>
            
            <div class="form-group">
              <label class="form-label">
                <i class="fas fa-thumbs-up"></i>
                نقاط القوة (الأخضر الفاتح - الصف الثالث)
              </label>
              <textarea class="form-control" id="strengths" 
                        placeholder="اكتب نقاط القوة هنا (حد أقصى 250 حرف)..." 
                        rows="3" maxlength="250"></textarea>
              <div class="char-counter" id="strengths-counter">0/250 حرف</div>
            </div>
          </div>
          
          <div class="form-group">
            <label class="form-label">
              <i class="fas fa-lightbulb"></i>
              فرص التحسين (البرتقالي - أسفل الصفحة)
            </label>
            <textarea class="form-control" id="improvements" 
                      placeholder="اكتب فرص التحسين هنا (حد أقصى 250 حرف)..." 
                      rows="3" maxlength="250"></textarea>
            <div class="char-counter" id="improvements-counter">0/250 حرف</div>
          </div>
        </div>

        <!-- الصور التوثيقية (صورتان كحد أقصى) -->
        <div class="form-section">
          <h3 class="section-title">
            <i class="fas fa-images"></i>
            الصور التوثيقية (صورتان كحد أقصى)
          </h3>
          
          <div class="upload-area" onclick="document.getElementById('image-upload').click()">
            <i class="fas fa-cloud-upload-alt"></i>
            <p>انقر أو اسحب الصور هنا للرفع</p>
            <small>يسمح بصورتين كحد أقصى (JPEG, PNG) - 5MB لكل صورة</small>
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
      <h3><i class="fas fa-magic"></i> قوالب جاهزة</h3>
      
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
        
        <button class="action-btn btn-print" onclick="printReport()">
          <i class="fas fa-print"></i>
          طباعة التقرير
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
      
      <div class="alert alert-info" style="margin-top: 20px; position: static;">
        <i class="fas fa-info-circle"></i>
        <span>التقارير تحفظ تلقائياً في المتصفح</span>
      </div>
      
      <div style="margin-top: 20px; padding: 15px; background: var(--light); border-radius: 10px;">
        <h4 style="color: var(--primary); margin-bottom: 10px; font-size: 15px;">
          <i class="fas fa-question-circle"></i> تلميحات
        </h4>
        <ul style="font-size: 13px; color: var(--dark-gray); padding-right: 15px; line-height: 1.6;">
          <li>كل مربع محدود بـ 250 حرف</li>
          <li>يسمح بصورتين كحد أقصى</li>
          <li>التقرير سيُنشأ في صفحة واحدة</li>
          <li>يمكن حفظ المسودة لمواصلة لاحقاً</li>
        </ul>
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
  
  <button class="nav-btn" onclick="saveToLocalStorage()">
    <i class="fas fa-save"></i>
    <span>حفظ</span>
  </button>
</nav>

<!-- نافذة المعاينة -->
<div class="preview-overlay" id="preview-overlay">
  <div class="preview-container">
    <div class="preview-header">
      <h3><i class="fas fa-print"></i> معاينة التقرير (صفحة واحدة)</h3>
      <button class="close-preview" onclick="hidePreview()">
        <i class="fas fa-times"></i>
      </button>
    </div>
    <div class="report-content" id="report-content">
      <!-- محتوى التقرير سيتم إضافته هنا -->
    </div>
  </div>
</div>

<!-- شاشة التحميل -->
<div class="loading-overlay" id="loading-overlay">
  <div class="loading-content">
    <div class="loading-spinner"></div>
    <p>جاري إعداد التقرير للطباعة...</p>
    <small>يرجى الانتظار</small>
  </div>
</div>

<script>
// بيانات التطبيق
const templates = {
  1: {
    name: "نشاط إثرائي",
    type: "اثرائي",
    goal: "تنمية مهارات التفكير النقدي والإبداعي لدى الطلاب المتميزين من خلال أنشطة متقدمة تحفز الابتكار وتطور القدرات البحثية، مع التركيز على تطوير مشاريع علمية مبتكرة.",
    steps: "1. اختيار الطلاب الموهوبين بناءً على معايير محددة (التحصيل العلمي، الإبداع، المهارات)\n2. عقد ورش عمل متخصصة في التفكير الإبداعي وحل المشكلات\n3. تنفيذ مشاريع بحثية مصغرة تحت إشراف متخصصين\n4. تنظيم مسابقات علمية محفزة مع جوائز تشجيعية",
    results: "• تطوير 8 مشاريع بحثية مبتكرة في مجالات متنوعة\n• تحسن ملحوظ في مهارات التحليل والتفكير النقدي بنسبة 40%\n• مشاركة ناجحة في 3 مسابقات علمية محلية\n• ارتفاع مستوى الدافعية للتعلم لدى المشاركين",
    recommendations: "• توسيع نطاق البرنامج ليشمل المزيد من الطلاب المتميزين\n• تدريب معلمين متخصصين في الإثراء العلمي\n• إنشاء مكتبة مصادر رقمية متخصصة للطلاب الموهوبين\n• توثيق التجارب الناجحة ونشرها كنماذج استرشادية",
    target: "طلاب الصف الثالث الثانوي المتميزين أكاديمياً",
    subject: "الفيزياء المتقدمة",
    strengths: "تنوع الأنشطة، جودة الإشراف، الموارد المتاحة، تفاعل الطلاب الإيجابي، التخطيط المنظم، المتابعة المستمرة، الدعم الإداري الكامل",
    improvements: "توفير مزيد من الوقت للأنشطة، زيادة الميزانية المخصصة، توسيع قاعدة المشاركة، توفير تدريب إضافي للمعلمين، تحسين التجهيزات التقنية"
  },
  2: {
    name: "خطة علاجية",
    type: "علاجي",
    goal: "معالجة الصعوبات القرائية والكتابية لدى الطلاب المتأخرين دراسياً في اللغة العربية وتحسين مهاراتهم الأساسية، ورفع مستوى الثقة لديهم في التعامل مع النصوص العربية.",
    steps: "1. تشخيص فردي دقيق للصعوبات التعليمية لكل طالب\n2. تصميم خطط علاجية مخصصة تناسب مستوى كل طالب\n3. جلسات علاجية مكثفة أسبوعياً (3 جلسات أسبوعياً)\n4. استخدام وسائل تعليمية مساعدة وبرامج محوسبة",
    results: "• تحسن مهارات القراءة الجهرية والصامتة بنسبة 65%\n• تحسن مهارات الكتابة والإملاء بنسبة 55%\n• زيادة مشاركة الطلاب في الحصص والأنشطة الصفية\n• تحسن ملحوظ في الثقة بالنفس والتعبير الشفهي",
    recommendations: "• تطوير أدوات تشخيص أكثر دقة وشاملة\n• تدريب فرق علاجية متخصصة في صعوبات التعلم\n• إنشاء بنك أنشطة علاجية متدرجة الصعوبة\n• تعزيز الشراكة مع أولياء الأمور عبر ورش توعوية",
    target: "الطلاب المتأخرين دراسياً في مهارات اللغة العربية",
    subject: "اللغة العربية",
    strengths: "الاهتمام الفردي بالطلاب، التنوع في الأساليب العلاجية، المتابعة المستمرة للتقدم، التعاون مع أولياء الأمور، استخدام التقنية المساعدة",
    improvements: "توفير موارد تعليمية إضافية، زيادة وقت الجلسات العلاجية، تدريب إضافي للمعلمين، تحسين بيئة التعلم، توفير أجهزة وتقنيات حديثة"
  },
  3: {
    name: "نشاط إبداعي",
    type: "اثرائي",
    goal: "تنمية المهارات التقنية والبرمجية لدى الطلاب الموهوبين في مجال التكنولوجيا، وتهيئتهم لمتطلبات العصر الرقمي من خلال مشاريع تطبيقية مبتكرة.",
    steps: "1. تدريب مكثف على أساسيات البرمجة والتفكير الحاسوبي\n2. ورش عمل في التصميم الرقمي وتطوير الواجهات\n3. مشاريع تقنية تطبيقية (تطبيقات - مواقع إلكترونية)\n4. مسابقات برمجية وجوائز تحفيزية",
    results: "• تصميم وتطوير 12 موقعاً إلكترونياً تعليمياً تفاعلياً\n• تطوير 5 تطبيقات تعليمية على منصتي Android و iOS\n• فوز الفريق في 3 مسابقات برمجية محلية وإقليمية\n• اكتشاف وتطوير 15 موهبة تقنية واعدة",
    recommendations: "• توفير معامل حاسوب متطورة مجهزة بأحدث البرامج\n• تأهيل مدربين متخصصين في المجال التقني والبرمجة\n• إنشاء نادي تقني دائم وتوفير ميزانية تشغيلية\n• إقامة شراكات مع مؤسسات تقنية وجامعات متخصصة",
    target: "طلاب المرحلة الثانوية المهتمين بالتكنولوجيا والبرمجة",
    subject: "الحاسب الآلي وتقنية المعلومات",
    strengths: "التطبيق العملي المباشر، الإبداع التقني المتميز، الدعم الفني والإداري الكامل، تفاعل الطلاب الإيجابي، التنظيم الجيد للورش والتدريبات",
    improvements: "تحديث الأجهزة والتقنيات المستخدمة، توسيع نطاق المشاركة ليشمل المزيد من الطلاب، زيادة الموارد المالية لدعم المشاريع، تطوير منهج تدريبي أكثر شمولية"
  },
  4: {
    name: "تقرير تقويمي",
    type: "تقويمي",
    goal: "تقويم أداء الطلاب في نهاية الفصل الدراسي وتحليل نتائجهم، وتحديد مستوى تحقيق الأهداف التعليمية، ووضع خطط تطويرية للفصل القادم.",
    steps: "1. إعداد اختبارات تقويمية شاملة تغطي جميع المهارات\n2. تحليل إحصائي دقيق لنتائج الاختبارات باستخدام أدوات متخصصة\n3. مقابلات فردية مع الطلاب لمناقشة النتائج والتحديات\n4. دراسة مؤشرات الأداء ومقارنتها مع المعايير الوطنية",
    results: "• تحقيق 85% من الطلاب للمستوى المطلوب في جميع المواد\n• تحسن في متوسط الدرجات بنسبة 15% مقارنة بالفصل السابق\n• ارتفاع مؤشر الرضا عن العملية التعليمية إلى 88%\n• تحديد نقاط القوة والضعف بدقة للطلاب والمعلمين",
    recommendations: "• تطوير استراتيجيات تدريس تتناسب مع أنماط التعلم المختلفة\n• تحسين الوسائل التعليمية وتوفير موارد تعليمية متنوعة\n• تنويع أساليب التقويم لتشمل المهارات العملية\n• تعزيز التعلم الذاتي والبحث العلمي لدى الطلاب",
    target: "جميع طلاب الصف العاشر",
    subject: "الرياضيات والعلوم",
    strengths: "الدقة العلمية في التحليل الإحصائي، الشمولية في التغطية، المشاركة الفعالة من الطلاب والمعلمين، الموضوعية في التقييم، الوضوح في عرض النتائج",
    improvements: "تطوير أدوات التقويم لتكون أكثر شمولية، زيادة التغذية الراج
    improvements: "تطوير أدوات التقويم لتكون أكثر شمولية، زيادة التغذية الراجعة للطلاب، تحسين توقيت الاختبارات التقويمية، تدريب المعلمين على استخدام أدوات تقييم حديثة"
  }
};

let uploadedImages = [];

// تحميل القالب
function loadTemplate(templateId) {
  const template = templates[templateId];
  if (!template) return;
  
  // قص النصوص لتناسب 250 حرف
  const truncateText = (text, maxLength = 250) => {
    return text.length > maxLength ? text.substring(0, maxLength) + "..." : text;
  };
  
  // تعبئة الحقول مع قص النصوص
  document.getElementById('report-type').value = template.type;
  document.getElementById('educational-goal').value = truncateText(template.goal);
  document.getElementById('implementation-steps').value = truncateText(template.steps);
  document.getElementById('achieved-results').value = truncateText(template.results);
  document.getElementById('recommendations').value = truncateText(template.recommendations);
  document.getElementById('target-audience').value = template.target;
  document.getElementById('subject').value = template.subject;
  document.getElementById('strengths').value = truncateText(template.strengths);
  document.getElementById('improvements').value = truncateText(template.improvements);
  
  // تحديث العدادات
  updateCharCounters();
  
  // إشعار
  showAlert(`تم تحميل قالب "${template.name}" بنجاح!`, 'success');
}

// تحديث عدادات الأحرف
function updateCharCounters() {
  const fields = [
    {id: 'educational-goal', counter: 'goal-counter', max: 250},
    {id: 'implementation-steps', counter: 'steps-counter', max: 250},
    {id: 'achieved-results', counter: 'results-counter', max: 250},
    {id: 'recommendations', counter: 'rec-counter', max: 250},
    {id: 'strengths', counter: 'strengths-counter', max: 250},
    {id: 'improvements', counter: 'improvements-counter', max: 250}
  ];
  
  fields.forEach(field => {
    const textarea = document.getElementById(field.id);
    const counter = document.getElementById(field.counter);
    if (!textarea || !counter) return;
    
    const length = textarea.value.length;
    const percentage = (length / field.max) * 100;
    
    counter.textContent = `${length}/${field.max} حرف`;
    counter.className = 'char-counter' + (percentage >= 90 ? ' char-limit' : '');
    
    // إضافة تحذير إذا تجاوز الحد
    if (length > field.max) {
      textarea.value = textarea.value.substring(0, field.max);
      counter.textContent = `${field.max}/${field.max} حرف (تم قص النص)`;
      showAlert(`تم قص النص في "${field.id}" ليتناسب مع الحد الأقصى (${field.max} حرف)`, 'warning');
    }
  });
}

// مسح النموذج مع تأكيد
function showClearConfirmation() {
  if (confirm('هل أنت متأكد من رغبتك في مسح جميع البيانات؟\nلن يمكنك استرجاع البيانات بعد المسح.')) {
    clearForm();
  }
}

// مسح النموذج
function clearForm() {
  const fields = [
    'school-name', 'target-audience', 'educational-goal',
    'implementation-steps', 'achieved-results', 'recommendations',
    'teacher-name', 'principal-name', 'subject', 'strengths', 'improvements'
  ];
  
  fields.forEach(fieldId => {
    const element = document.getElementById(fieldId);
    if (element) element.value = '';
  });
  
  uploadedImages = [];
  const preview = document.getElementById('image-preview');
  if (preview) preview.innerHTML = '';
  
  const uploadInput = document.getElementById('image-upload');
  if (uploadInput) uploadInput.value = '';
  
  updateCharCounters();
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
  
  let imagesLoaded = 0;
  
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
        <img src="${e.target.result}" alt="صورة ${index + 1}" loading="lazy">
        <div class="remove-image" onclick="removeImage(${index})">
          <i class="fas fa-times"></i>
        </div>
      `;
      preview.appendChild(imgDiv);
      
      imagesLoaded++;
      if (imagesLoaded === files.length && files.length > 0) {
        showAlert(`تم رفع ${files.length} صورة بنجاح`, 'success');
      }
    };
    reader.onerror = function() {
      showAlert('حدث خطأ أثناء تحميل الصورة', 'error');
    };
    reader.readAsDataURL(file);
  });
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
      <img src="${img.data}" alt="صورة ${i + 1}" loading="lazy">
      <div class="remove-image" onclick="removeImage(${i})">
        <i class="fas fa-times"></i>
      </div>
    `;
    preview.appendChild(imgDiv);
  });
  
  showAlert('تم إزالة الصورة', 'info');
}

// حفظ في localStorage
function saveToLocalStorage() {
  const data = collectFormData();
  
  try {
    localStorage.setItem('educational_report_draft', JSON.stringify({
      ...data,
      images: uploadedImages,
      savedAt: new Date().toLocaleString('ar-SA')
    }));
    
    showAlert('تم حفظ المسودة بنجاح في ذاكرة المتصفح', 'success');
  } catch (e) {
    showAlert('حدث خطأ أثناء حفظ المسودة', 'error');
    console.error('Error saving to localStorage:', e);
  }
}

// تحميل من localStorage
function loadFromLocalStorage() {
  try {
    const saved = localStorage.getItem('educational_report_draft');
    if (!saved) return;
    
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
    
    updateCharCounters();
    showAlert('تم تحميل المسودة المحفوظة مسبقاً', 'info');
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
      <img src="${img.data}" alt="صورة ${i + 1}" loading="lazy">
      <div class="remove-image" onclick="removeImage(${i})">
        <i class="fas fa-times"></i>
      </div>
    `;
    preview.appendChild(imgDiv);
  });
}

// عرض المعاينة
function showPreview() {
  const data = collectFormData();
  
  if (!validateForm()) {
    showAlert('الرجاء تعبئة الحقول المطلوبة (اسم المدرسة، الهدف التربوي، اسم المعلم)', 'error');
    return;
  }
  
  buildReportPreview(data);
  document.getElementById('preview-overlay').style.display = 'flex';
  document.body.style.overflow = 'hidden';
  
  // إضافة تأثير للمعاينة على الجوال
  if (window.innerWidth <= 768) {
    document.querySelector('.preview-container').style.animation = 'scaleIn 0.3s ease';
  }
}

// إخفاء المعاينة
function hidePreview() {
  document.getElementById('preview-overlay').style.display = 'none';
  document.body.style.overflow = 'auto';
}

// طباعة التقرير
function printReport() {
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
    buildReportPreview(data);
    
    // انتظار لحظة لضمان تحميل الصور
    setTimeout(() => {
      // فتح نافذة الطباعة
      window.print();
      
      // إخفاء شاشة التحميل
      loadingOverlay.style.display = 'none';
      
      showAlert('تم فتح نافذة الطباعة، يمكنك طباعة التقرير الآن', 'success');
    }, 800);
  }, 1200);
}

// بناء معاينة التقرير (صفحة واحدة)
function buildReportPreview(data) {
  const content = document.getElementById('report-content');
  if (!content) return;

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

  // قص النص إذا تجاوز 250 حرف
  const truncateForBox = (text, maxLength = 250) => {
    if (!text || text.trim() === '') return 'لم يتم إضافة محتوى';
    return text.length > maxLength ? text.substring(0, maxLength) + "..." : text;
  };

  // تحويل النص إلى أسطر
  const formatTextWithLines = (text) => {
    if (!text) return '';
    return text.replace(/\n/g, '<br>');
  };

  content.innerHTML = `
    <!-- رأس التقرير -->
    <div style="text-align: center; margin-bottom: 25px; padding-bottom: 15px; border-bottom: 3px solid #1B4F72;">
      <h1 style="color: #1B4F72; font-size: 24px; margin-bottom: 10px;">وزارة التعليم</h1>
      <h2 style="color: #27AE60; font-size: 18px; margin-bottom: 8px;">${getDepartmentName(data.department)}</h2>
      <h3 style="color: #2C3E50; font-size: 16px; margin-bottom: 10px;">${data.school}</h3>
      <div style="background: #E67E22; color: white; padding: 8px 20px; border-radius: 20px; display: inline-block; font-weight: bold;">
        <i class="fas fa-calendar-alt" style="margin-left: 8px;"></i>
        ${getCurrentDate()} | ${getReportTypeName(data.type)} | الفصل ${data.semester}
      </div>
    </div>
    
    <!-- المعلومات الأساسية -->
    <div style="background: #F8F9FA; padding: 15px; border-radius: 10px; margin-bottom: 20px; border-right: 4px solid #2E86C1;">
      <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px;">
        <div style="background: white; padding: 12px; border-radius: 8px; border: 2px solid #EAECEE;">
          <strong style="color: #1B4F72;">المادة الدراسية:</strong><br>
          ${data.subject || 'غير محدد'}
        </div>
        <div style="background: white; padding: 12px; border-radius: 8px; border: 2px solid #EAECEE;">
          <strong style="color: #1B4F72;">الفئة المستهدفة:</strong><br>
          ${data.target || 'غير محدد'}
        </div>
      </div>
    </div>
    
    <!-- الهدف التربوي (أخضر - أعلى الصفحة) -->
    <div class="goal-section">
      <h3><i class="fas fa-bullseye"></i> الهدف التربوي</h3>
      <div class="goal-content">
        ${formatTextWithLines(data.goal || 'لم يتم تحديد الهدف التربوي')}
      </div>
    </div>
    
    <!-- الصف الثاني: إجراءات التنفيذ والنتائج المتحققة -->
    <div class="row-2">
      <div class="implementation-box">
        <h4><i class="fas fa-tasks"></i> إجراءات التنفيذ</h4>
        <div class="implementation-content">
          ${formatTextWithLines(truncateForBox(data.steps))}
        </div>
      </div>
      
      <div class="results-box">
        <h4><i class="fas fa-chart-line"></i> النتائج المتحققة</h4>
        <div class="results-content">
          ${formatTextWithLines(truncateForBox(data.results))}
        </div>
      </div>
    </div>
    
    <!-- الصف الثالث: التوصيات ونقاط القوة -->
    <div class="row-3">
      <div class="recommendations-box">
        <h4><i class="fas fa-comments"></i> التوصيات والمقترحات</h4>
        <div class="recommendations-content">
          ${formatTextWithLines(truncateForBox(data.recommendations))}
        </div>
      </div>
      
      <div class="strengths-box">
        <h4><i class="fas fa-thumbs-up"></i> نقاط القوة</h4>
        <div class="strengths-content">
          ${formatTextWithLines(truncateForBox(data.strengths))}
        </div>
      </div>
    </div>
    
    <!-- فرص التحسين (برتقالي - أسفل الصفحة) -->
    <div class="improvements-box">
      <h4><i class="fas fa-lightbulb"></i> فرص التحسين</h4>
      <div class="improvements-content">
        ${formatTextWithLines(truncateForBox(data.improvements))}
      </div>
    </div>
    
    <!-- الصور التوثيقية (صورتان كحد أقصى) -->
    ${uploadedImages.length > 0 ? `
      <div class="images-section">
        <h4><i class="fas fa-images"></i> الصور التوثيقية</h4>
        <div class="report-images">
          ${uploadedImages.map((img, index) => `
            <div class="report-image">
              <img src="${img.data}" alt="صورة توثيقية ${index + 1}" loading="lazy">
            </div>
          `).join('')}
        </div>
      </div>
    ` : ''}
    
    <!-- التوقيعات -->
    <div class="report-signatures">
      <div class="signature-box">
        <div class="signature-title">
          <i class="fas fa-chalkboard-teacher"></i>
          المعلم / المشرف
        </div>
        <div class="signature-line"></div>
        <div class="signature-name">
          ${data.teacher}
        </div>
      </div>
      
      <div class="signature-box">
        <div class="signature-title">
          <i class="fas fa-user-tie"></i>
          مدير المدرسة
        </div>
        <div class="signature-line"></div>
        <div class="signature-name">
          ${data.principal || '.................'}
        </div>
      </div>
    </div>
    
    <!-- تذييل الصفحة -->
    <div style="margin-top: 30px; padding: 15px; background: #F8F9FA; border-radius: 10px; text-align: center; color: #566573; font-size: 13px; border-top: 2px solid #EAECEE;">
      <div style="display: flex; align-items: center; justify-content: center; gap: 10px; margin-bottom: 5px;">
        <i class="fas fa-qrcode" style="color: #2E86C1;"></i>
        <span>تم إنشاء هذا التقرير بواسطة أداة التقارير التعليمية الذكية - وزارة التعليم</span>
      </div>
      <div>
        ${new Date().toLocaleString('ar-SA')}
      </div>
    </div>
  `;
  
  // إضافة تحميل lazy للصور في المعاينة
  setTimeout(() => {
    const images = content.querySelectorAll('img');
    images.forEach(img => {
      if (!img.complete) {
        img.onload = function() {
          console.log('تم تحميل الصورة:', img.src);
        };
        img.onerror = function() {
          console.error('فشل تحميل الصورة:', img.src);
        };
      }
    });
  }, 100);
}

// جمع بيانات النموذج
function collectFormData() {
  return {
    department: document.getElementById('education-department').value,
    school: document.getElementById('school-name') ? document.getElementById('school-name').value.trim() : '',
    type: document.getElementById('report-type').value,
    target: document.getElementById('target-audience') ? document.getElementById('target-audience').value.trim() : '',
    semester: document.getElementById('semester').value,
    subject: document.getElementById('subject') ? document.getElementById('subject').value.trim() : '',
    goal: document.getElementById('educational-goal') ? document.getElementById('educational-goal').value.trim() : '',
    steps: document.getElementById('implementation-steps') ? document.getElementById('implementation-steps').value.trim() : '',
    results: document.getElementById('achieved-results') ? document.getElementById('achieved-results').value.trim() : '',
    recommendations: document.getElementById('recommendations') ? document.getElementById('recommendations').value.trim() : '',
    strengths: document.getElementById('strengths') ? document.getElementById('strengths').value.trim() : '',
    improvements: document.getElementById('improvements') ? document.getElementById('improvements').value.trim() : '',
    teacher: document.getElementById('teacher-name') ? document.getElementById('teacher-name').value.trim() : '',
    principal: document.getElementById('principal-name') ? document.getElementById('principal-name').value.trim() : ''
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
  // إزالة التنبيهات السابقة
  const existingAlerts = document.querySelectorAll('.alert');
  existingAlerts.forEach(alert => {
    if (alert.parentNode) {
      alert.parentNode.removeChild(alert);
    }
  });
  
  const alert = document.createElement('div');
  alert.className = `alert alert-${type}`;
  alert.innerHTML = `
    <i class="fas fa-${type === 'success' ? 'check-circle' : 
                      type === 'warning' ? 'exclamation-triangle' : 
                      type === 'error' ? 'times-circle' : 'info-circle'}"></i>
    <span>${message}</span>
  `;
  
  document.body.appendChild(alert);
  
  // إخفاء التنبيه بعد 5 ثواني
  setTimeout(() => {
    if (alert.parentNode) {
      alert.style.animation = 'fadeOut 0.5s ease';
      setTimeout(() => {
        if (alert.parentNode) {
          alert.remove();
        }
      }, 500);
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
    btn.classList.toggle('active', i === index);
  });
}

// إضافة مستمعين للأحداث عند تحميل الصفحة
document.addEventListener('DOMContentLoaded', function() {
  // تحديث العدادات عند الكتابة
  const textareas = ['educational-goal', 'implementation-steps', 'achieved-results', 
                     'recommendations', 'strengths', 'improvements'];
  
  textareas.forEach(id => {
    const element = document.getElementById(id);
    if (element) {
      element.addEventListener('input', updateCharCounters);
      element.addEventListener('input', function() {
        if (this.value.length > 250) {
          this.value = this.value.substring(0, 250);
          updateCharCounters();
        }
      });
    }
  });
  
  // تحميل المسودة المحفوظة تلقائياً
  loadFromLocalStorage();
  
  // تعيين القيم الافتراضية إذا كانت فارغة
  if (!document.getElementById('school-name').value) {
    document.getElementById('school-name').value = "مدرسة النخبة العلمية الثانوية";
  }
  
  if (!document.getElementById('teacher-name').value) {
    document.getElementById('teacher-name').value = "أحمد بن محمد العلي";
  }
  
  // تحديث العدادات الأولية
  updateCharCounters();
  
  // الترحيب بعد تحميل الصفحة
  setTimeout(() => {
    showAlert('مرحباً بك في نظام التقارير التعليمية!', 'info');
  }, 1000);
  
  // تحسين تجربة اللمس للجوال
  if ('ontouchstart' in window) {
    document.querySelectorAll('.action-btn, .template-btn').forEach(btn => {
      btn.addEventListener('touchstart', function() {
        this.style.transform = 'scale(0.98)';
      });
      
      btn.addEventListener('touchend', function() {
        setTimeout(() => {
          this.style.transform = '';
        }, 150);
      });
    });
    
    // تحسين الحقول للجوال
    document.querySelectorAll('input, textarea, select').forEach(field => {
      field.addEventListener('focus', function() {
        if (window.innerWidth <= 768) {
          setTimeout(() => {
            this.scrollIntoView({ behavior: 'smooth', block: 'center' });
          }, 300);
        }
      });
    });
  }
  
  // دعم سحب وإفلات الصور
  const uploadArea = document.querySelector('.upload-area');
  if (uploadArea) {
    uploadArea.addEventListener('dragover', (e) => {
      e.preventDefault();
      uploadArea.style.borderColor = '#2E86C1';
      uploadArea.style.background = 'rgba(46, 134, 193, 0.1)';
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
      
      if (input && files.length > 0) {
        const dataTransfer = new DataTransfer();
        files.slice(0, 2).forEach(file => dataTransfer.items.add(file));
        input.files = dataTransfer.files;
        
        handleImageUpload(input);
      }
    });
  }
  
  // تحسين الأداء للجوال
  if ('connection' in navigator && navigator.connection.saveData === true) {
    console.log('وضع توفير البيانات مفعل، تم تحميل الملفات الأساسية فقط');
  }
});

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
  
  // دعم اختصارات لوحة المفاتيح
  if (e.ctrlKey || e.metaKey) {
    switch(e.key) {
      case 'p':
        e.preventDefault();
        printReport();
        break;
      case 's':
        e.preventDefault();
        saveToLocalStorage();
        break;
    }
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

// دعم الطابعة
window.addEventListener('beforeprint', () => {
  console.log('جاري التحضير للطباعة...');
});

window.addEventListener('afterprint', () => {
  console.log('تم الانتهاء من الطباعة');
  showAlert('تم الانتهاء من عملية الطباعة', 'info');
});

// دعم عدم اتصال الإنترنت
window.addEventListener('online', () => {
  showAlert('تم استعادة الاتصال بالإنترنت', 'success');
});

window.addEventListener('offline', () => {
  showAlert('فقدت الاتصال بالإنترنت، يمكنك الاستمرار في العمل محلياً', 'warning');
});

// إضافة أنماط CSS للـ fadeOut
const fadeOutStyle = document.createElement('style');
fadeOutStyle.textContent = `
  @keyframes fadeOut {
    from { opacity: 1; transform: translateY(0); }
    to { opacity: 0; transform: translateY(-20px); }
  }
  
  /* تحسينات الطباعة */
  @media print {
    .no-print {
      display: none !important;
    }
    
    .goal-section, .implementation-box, .results-box,
    .recommendations-box, .strengths-box, .improvements-box {
      page-break-inside: avoid;
    }
    
    .report-images {
      page-break-inside: avoid;
    }
  }
`;
document.head.appendChild(fadeOutStyle);

// تحسين أداء التمرير على الجوال
if ('ontouchstart' in window) {
  let lastTouchEnd = 0;
  document.addEventListener('touchend', function(event) {
    const now = Date.now();
    if (now - lastTouchEnd <= 300) {
      event.preventDefault();
    }
    lastTouchEnd = now;
  }, false);
}

// دعم خاصية التثبيت (PWA)
if ('serviceWorker' in navigator) {
  window.addEventListener('load', function() {
    navigator.serviceWorker.register('/sw.js').then(function(registration) {
      console.log('ServiceWorker registration successful');
    }, function(err) {
      console.log('ServiceWorker registration failed: ', err);
    });
  });
}

// إضافة خاصية حفظ تلقائي أثناء الكتابة
let autoSaveTimeout;
document.querySelectorAll('input, textarea, select').forEach(element => {
  element.addEventListener('input', function() {
    clearTimeout(autoSaveTimeout);
    autoSaveTimeout = setTimeout(() => {
      saveToLocalStorage();
    }, 3000); // حفظ تلقائي بعد 3 ثواني من التوقف عن الكتابة
  });
});

// تحسين عرض التاريخ على الجوال
function formatMobileDate() {
  const now = new Date();
  const options = { 
    year: 'numeric', 
    month: 'long', 
    day: 'numeric',
    weekday: 'long'
  };
  return now.toLocaleDateString('ar-SA', options);
}

// تحديث التاريخ في الهيدر بشكل دوري (كل ساعة)
setInterval(() => {
  const dateElements = document.querySelectorAll('.report-date, [data-date]');
  dateElements.forEach(el => {
    if (el.textContent.includes('م -')) {
      // تحديث التاريخ فقط إذا كان يحتوي على التاريخ الهجري
      el.textContent = formatMobileDate();
    }
  });
}, 3600000); // كل ساعة
</script>
</body>
</html>