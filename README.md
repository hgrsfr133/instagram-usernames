/* الألوان الرئيسية */
:root {
    --primary-color: #9c27b0;
    --secondary-color: #ffc107;
    --dark-primary: #6a1b9a;
    --dark-color: #212121;
    --light-color: #f5f5f5;
    --text-color: #f5f5f5;
    --text-dark: #212121;
    --success-color: #4caf50;
    --error-color: #f44336;
    --warning-color: #ff9800;
    --info-color: #2196f3;
}

/* إعادة ضبط عام */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Cairo', sans-serif;
    background-color: var(--dark-color);
    color: var(--text-color);
    line-height: 1.6;
    position: relative;
    overflow-x: hidden;
}

/* الخلفية المتحركة */
.animated-bg, .page-animated-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    z-index: -1;
}

.page-animated-bg {
    position: fixed;
    height: 100vh;
}

.bg-circle {
    position: absolute;
    border-radius: 50%;
    opacity: 0.15;
    filter: blur(20px);
    z-index: -1;
}

@keyframes float {
    0%, 100% {
        transform: translateY(0) translateX(0);
    }
    25% {
        transform: translateY(-20px) translateX(10px);
    }
    50% {
        transform: translateY(10px) translateX(-15px);
    }
    75% {
        transform: translateY(15px) translateX(20px);
    }
}

/* الحاويات */
.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
}

/* الهيدر */
header {
    background-color: rgba(33, 33, 33, 0.9);
    padding: 15px 0;
    position: relative;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
    overflow: hidden;
}

header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    display: flex;
    align-items: center;
}

.logo img {
    width: 50px;
    height: 50px;
    margin-left: 10px;
}

.logo h1 {
    font-size: 1.5rem;
    color: var(--secondary-color);
    text-shadow: 0 0 5px rgba(156, 39, 176, 0.5);
}

nav {
    display: flex;
    gap: 15px;
}

nav a {
    color: var(--text-color);
    text-decoration: none;
    padding: 8px 15px;
    border-radius: 5px;
    transition: all 0.3s ease;
    position: relative;
}

nav a:hover, nav a.active {
    color: var(--secondary-color);
}

nav a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    width: 0;
    height: 2px;
    background-color: var(--secondary-color);
    transition: all 0.3s ease;
    transform: translateX(-50%);
}

nav a:hover::after, nav a.active::after {
    width: 80%;
}

/* القسم الرئيسي */
main {
    min-height: calc(100vh - 200px);
    padding: 50px 0;
}

/* قسم البطل */
.hero-section {
    padding: 80px 0;
    text-align: center;
    position: relative;
}

.hero-content {
    max-width: 800px;
    margin: 0 auto;
}

.hero-content h1 {
    font-size: 2.5rem;
    margin-bottom: 20px;
    color: var(--secondary-color);
    text-shadow: 0 0 10px rgba(156, 39, 176, 0.5);
}

.hero-content p {
    font-size: 1.2rem;
    margin-bottom: 30px;
}

/* أزرار الدعوة للعمل */
.cta-buttons {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 30px;
    position: relative;
    z-index: 10;
}

.btn {
    display: inline-block;
    padding: 12px 30px;
    background-color: var(--primary-color);
    color: var(--text-color);
    text-decoration: none;
    border-radius: 50px;
    font-weight: bold;
    transition: all 0.3s ease;
    border: none;
    cursor: pointer;
    box-shadow: 0 4px 10px rgba(156, 39, 176, 0.3);
    position: relative;
    z-index: 10;
}

.btn:hover {
    background-color: var(--dark-primary);
    transform: translateY(-3px);
    box-shadow: 0 6px 15px rgba(156, 39, 176, 0.4);
}

.btn-secondary {
    background-color: var(--secondary-color);
    color: var(--text-dark);
    box-shadow: 0 4px 10px rgba(255, 193, 7, 0.3);
}

.btn-secondary:hover {
    background-color: #e6ac00;
    box-shadow: 0 6px 15px rgba(255, 193, 7, 0.4);
}

/* قسم المميزات */
.features-section {
    padding: 80px 0;
}

.section-title {
    text-align: center;
    margin-bottom: 50px;
}

.section-title h2 {
    font-size: 2rem;
    color: var(--secondary-color);
    position: relative;
    display: inline-block;
    padding-bottom: 15px;
}

.section-title h2::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 100px;
    height: 3px;
    background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
    border-radius: 3px;
}

.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.feature-card {
    background-color: rgba(33, 33, 33, 0.7);
    padding: 30px;
    border-radius: 10px;
    text-align: center;
    transition: all 0.3s ease;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    position: relative;
    overflow: hidden;
    z-index: 1;
}

.feature-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, rgba(156, 39, 176, 0.1), rgba(255, 193, 7, 0.1));
    z-index: -1;
    opacity: 0;
    transition: all 0.3s ease;
}

.feature-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
}

.feature-card:hover::before {
    opacity: 1;
}

.feature-icon {
    width: 80px;
    height: 80px;
    background-color: var(--primary-color);
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto 20px;
    box-shadow: 0 5px 15px rgba(156, 39, 176, 0.3);
}

.feature-icon i {
    font-size: 2rem;
    color: var(--text-color);
}

.feature-card h3 {
    font-size: 1.5rem;
    margin-bottom: 15px;
    color: var(--secondary-color);
}

/* قسم الدعوة للعمل */
.cta-section, .auth-cta-section {
    padding: 60px 0;
    text-align: center;
}

/* الفوتر */
footer {
    background-color: rgba(33, 33, 33, 0.9);
    padding: 50px 0 20px;
    position: relative;
    box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.3);
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
    margin-bottom: 30px;
}

.footer-column h3 {
    font-size: 1.3rem;
    margin-bottom: 20px;
    color: var(--secondary-color);
    position: relative;
    padding-bottom: 10px;
}

.footer-column h3::after {
    content: '';
    position: absolute;
    bottom: 0;
    right: 0;
    width: 50px;
    height: 2px;
    background-color: var(--primary-color);
}

.footer-links {
    list-style: none;
}

.footer-links li {
    margin-bottom: 10px;
}

.footer-links a, .footer-column a {
    color: var(--text-color);
    text-decoration: none;
    transition: all 0.3s ease;
}

.footer-links a:hover, .footer-column a:hover {
    color: var(--secondary-color);
    padding-right: 5px;
}

.social-links {
    display: flex;
    gap: 15px;
    margin-top: 20px;
}

.social-links a {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 40px;
    background-color: var(--primary-color);
    color: var(--text-color);
    border-radius: 50%;
    transition: all 0.3s ease;
}

.social-links a:hover {
    background-color: var(--secondary-color);
    color: var(--text-dark);
    transform: translateY(-3px);
}

.copyright {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    font-size: 0.9rem;
    color: rgba(255, 255, 255, 0.7);
}

/* نموذج التسجيل وتسجيل الدخول */
.auth-form-container {
    max-width: 500px;
    margin: 0 auto;
    background-color: rgba(33, 33, 33, 0.8);
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.auth-form-container h2 {
    text-align: center;
    margin-bottom: 30px;
    color: var(--secondary-color);
}

.form-group {
    margin-bottom: 20px;
}

.form-group label {
    display: block;
    margin-bottom: 8px;
    font-weight: bold;
}

.form-control {
    width: 100%;
    padding: 12px 15px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 5px;
    background-color: rgba(255, 255, 255, 0.05);
    color: var(--text-color);
    transition: all 0.3s ease;
}

.form-control:focus {
    outline: none;
    border-color: var(--primary-color);
    box-shadow: 0 0 0 2px rgba(156, 39, 176, 0.2);
}

.form-footer {
    text-align: center;
    margin-top: 20px;
}

.form-footer a {
    color: var(--secondary-color);
    text-decoration: none;
}

.form-footer a:hover {
    text-decoration: underline;
}

/* صفحة توليد الأسماء */
.generator-container {
    max-width: 800px;
    margin: 0 auto;
    background-color: rgba(33, 33, 33, 0.8);
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.generator-form {
    margin-bottom: 30px;
}

.form-row {
    display: flex;
    gap: 20px;
    margin-bottom: 20px;
}

.form-row .form-group {
    flex: 1;
    margin-bottom: 0;
}

.checkbox-group {
    display: flex;
    align-items: center;
    gap: 10px;
}

.checkbox-group input[type="checkbox"] {
    width: 18px;
    height: 18px;
}

.generator-results {
    margin-top: 30px;
}

.result-card {
    background-color: rgba(33, 33, 33, 0.6);
    padding: 15px;
    border-radius: 5px;
    margin-bottom: 15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: all 0.3s ease;
}

.result-card:hover {
    background-color: rgba(33, 33, 33, 0.8);
    transform: translateY(-3px);
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
}

.result-card .username {
    font-size: 1.2rem;
    font-weight: bold;
    color: var(--secondary-color);
}

.result-card .actions {
    display: flex;
    gap: 10px;
}

.result-card .actions button {
    background: none;
    border: none;
    color: var(--text-color);
    cursor: pointer;
    font-size: 1.2rem;
    transition: all 0.3s ease;
}

.result-card .actions button:hover {
    color: var(--secondary-color);
    transform: scale(1.1);
}

.availability {
    display: inline-block;
    padding: 5px 10px;
    border-radius: 50px;
    font-size: 0.8rem;
    margin-right: 10px;
}

.available {
    background-color: rgba(76, 175, 80, 0.2);
    color: #4caf50;
}

.unavailable {
    background-color: rgba(244, 67, 54, 0.2);
    color: #f44336;
}

/* الإشعارات */
#notifications-container {
    position: fixed;
    top: 20px;
    left: 20px;
    z-index: 1000;
}

.notification {
    background-color: rgba(33, 33, 33, 0.9);
    color: var(--text-color);
    padding: 15px 20px;
    border-radius: 5px;
    margin-bottom: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    display: flex;
    align-items: center;
    animation: slideIn 0.3s ease forwards;
    max-width: 300px;
}

.notification.success {
    border-right: 4px solid var(--success-color);
}

.notification.error {
    border-right: 4px solid var(--error-color);
}

.notification.warning {
    border-right: 4px solid var(--warning-color);
}

.notification.info {
    border-right: 4px solid var(--info-color);
}

.notification i {
    margin-left: 10px;
    font-size: 1.2rem;
}

.notification.success i {
    color: var(--success-color);
}

.notification.error i {
    color: var(--error-color);
}

.notification.warning i {
    color: var(--warning-color);
}

.notification.info i {
    color: var(--info-color);
}

@keyframes slideIn {
    from {
        transform: translateX(-100%);
        opacity: 0;
    }
    to {
        transform: translateX(0);
        opacity: 1;
    }
}

@keyframes slideOut {
    from {
        transform: translateX(0);
        opacity: 1;
    }
    to {
        transform: translateX(-100%);
        opacity: 0;
    }
}

/* لوحة التحكم */
.dashboard-container {
    display: grid;
    grid-template-columns: 1fr 3fr;
    gap: 30px;
}

.dashboard-sidebar {
    background-color: rgba(33, 33, 33, 0.8);
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.dashboard-sidebar .user-info {
    text-align: center;
    margin-bottom: 30px;
    padding-bottom: 20px;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.dashboard-sidebar .user-avatar {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background-color: var(--primary-color);
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto 15px;
    font-size: 2.5rem;
    color: var(--text-color);
}

.dashboard-sidebar .user-name {
    font-size: 1.2rem;
    margin-bottom: 5px;
}

.dashboard-sidebar .user-email {
    font-size: 0.9rem;
    color: rgba(255, 255, 255, 0.7);
}

.dashboard-sidebar .sidebar-menu {
    list-style: none;
}

.dashboard-sidebar .sidebar-menu li {
    margin-bottom: 10px;
}

.dashboard-sidebar .sidebar-menu a {
    display: flex;
    align-items: center;
    padding: 10px 15px;
    border-radius: 5px;
    text-decoration: none;
    color: var(--text-color);
    transition: all 0.3s ease;
}

.dashboard-sidebar .sidebar-menu a:hover, .dashboard-sidebar .sidebar-menu a.active {
    background-color: rgba(156, 39, 176, 0.2);
    color: var(--secondary-color);
}

.dashboard-sidebar .sidebar-menu i {
    margin-left: 10px;
    font-size: 1.2rem;
}

.dashboard-content {
    background-color: rgba(33, 33, 33, 0.8);
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.dashboard-content h2 {
    margin-bottom: 30px;
    color: var(--secondary-color);
    position: relative;
    padding-bottom: 10px;
}

.dashboard-content h2::after {
    content: '';
    position: absolute;
    bottom: 0;
    right: 0;
    width: 50px;
    height: 2px;
    background-color: var(--primary-color);
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin-bottom: 30px;
}

.stat-card {
    background-color: rgba(33, 33, 33, 0.6);
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    transition: all 0.3s ease;
}

.stat-card:hover {
    background-color: rgba(33, 33, 33, 0.8);
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.stat-card .stat-icon {
    font-size: 2rem;
    color: var(--secondary-color);
    margin-bottom: 10px;
}

.stat-card .stat-value {
    font-size: 1.8rem;
    font-weight: bold;
    margin-bottom: 5px;
}

.stat-card .stat-label {
    font-size: 0.9rem;
    color: rgba(255, 255, 255, 0.7);
}

.favorites-list {
    margin-top: 30px;
}

.favorites-list .result-card {
    background-color: rgba(33, 33, 33, 0.6);
}

/* التوافق مع الأجهزة المحمولة */
@media (max-width: 768px) {
    header .container {
        flex-direction: column;
        gap: 15px;
    }
    
    nav {
        width: 100%;
        justify-content: center;
        flex-wrap: wrap;
    }
    
    .hero-content h1 {
        font-size: 2rem;
    }
    
    .cta-buttons {
        flex-direction: column;
        gap: 15px;
    }
    
    .form-row {
        flex-direction: column;
        gap: 15px;
    }
    
    .dashboard-container {
        grid-template-columns: 1fr;
    }
    
    .footer-content {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 480px) {
    .hero-content h1 {
        font-size: 1.8rem;
    }
    
    .feature-card {
        padding: 20px;
    }
    
    .feature-icon {
        width: 60px;
        height: 60px;
    }
    
    .feature-icon i {
        font-size: 1.5rem;
    }
    
    .feature-card h3 {
        font-size: 1.2rem;
    }
    
    .auth-form-container {
        padding: 20px;
    }
}
# instagram-usernames
