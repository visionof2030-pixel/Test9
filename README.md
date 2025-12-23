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
  --primary: #1a56db;
  --primary-dark: #1e40af;
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
  --border-radius: 12px;
  --box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
  --box-shadow-hover: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
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
    font-size: 15px;
    -webkit-text-size-adjust: 100%;
  }
}

.container {
  max-width: 100%;
  margin: 0 auto;
  padding: 15px;
}

/* الهيدر مع خلفية شعار وزارة التعليم */
.header {
  background: white url('https://i.ibb.co/kVWFFwhW/9-C92-E57-B-23-FA-479-D-A024-1-D5-F871-B4-F8-D.png') center/contain no-repeat;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: 15px;
  margin-bottom: 15px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  border-right: 4px solid var(--primary);
  position: relative;
  min-height: 120px;
}

.header::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background: rgba(255, 255, 255, 0.85);
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
  gap: 10px;
}

.header-bottom {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
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
  gap: 12px;
}

.logo-icon {
  width: 45px;
  height: 45px;
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 22px;
  flex-shrink: 0;
}

.logo-text h1 {
  font-size: 18px;
  font-weight: 700;
  color: var(--dark);
  margin-bottom: 3px;
  line-height: 1.3;
}

.logo-text p {
  font-size: 13px;
  color: var(--gray);
  line-height: 1.4;
}

/* زر القائمة للجوال */
.mobile-menu-btn {
  display: none;
  background: none;
  border: none;
  color: var(--primary);
  font-size: 24px;
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
  padding: 10px 5px;
  display: none;
  justify-content: space-around;
  backdrop-filter: blur(10px);
}

@media (max-width: 768px) {
  .mobile-nav {
    display: flex;
  }
  
  .container {
    padding-bottom: 80px;
  }
}

.nav-btn {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
  background: none;
  border: none;
  color: var(--gray);
  font-size: 11px;
  padding: 6px 4px;
  cursor: pointer;
  flex: 1;
  min-width: 0;
  transition: var(--transition);
}

.nav-btn.active {
  color: var(--primary);
}

.nav-btn i {
  font-size: 16px;
}

.nav-btn:hover {
  transform: translateY(-2px);
}

/* المحتوى الرئيسي */
.main-content {
  display: grid;
  grid-template-columns: 1fr;
  gap: 15px;
}

@media (min-width: 1024px) {
  .main-content {
    grid-template-columns: 1fr 350px;
  }
}

/* لوحة التحكم - تصميم متجاوب */
.control-panel {
  background: white;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: 20px;
  height: fit-content;
  position: sticky;
  top: 15px;
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
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  gap: 10px;
  margin-bottom: 20px;
}

@media (max-width: 480px) {
  .quick-templates {
    grid-template-columns: 1fr;
  }
}

.template-btn {
  background: white;
  border: 2px solid var(--light-gray);
  border-radius: 10px;
  padding: 12px;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  text-align: center;
  min-height: 90px;
  justify-content: center;
}

.template-btn:hover {
  border-color: var(--primary);
  transform: translateY(-2px);
  box-shadow: var(--box-shadow-hover);
}

.template-btn i {
  font-size: 20px;
  color: var(--primary);
}

.template-btn span {
  font-size: 13px;
  font-weight: 500;
}

/* أزرار العمل */
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
}

.action-btn-primary {
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  color: white;
}

.action-btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: var(--box-shadow-hover);
}

.action-btn-secondary {
  background: white;
  color: var(--primary);
  border: 2px solid var(--primary);
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
  transform: translateY(-2px);
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
  background: linear-gradient(135deg, var(--primary), var(--primary-dark));
  color: white;
  padding: 15px 20px;
}

.form-header h2 {
  font-size: