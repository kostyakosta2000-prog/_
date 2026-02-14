
<html lang="ru">

<head>
    <script>
        // Меняем заголовок страницы мгновенно
        document.title = "Академия Кибербезопасности";
        
        // Удаляем любые элементы, которые могут добавлять название репозитория
        (function() {
            // Функция для удаления элементов с текстом "-_-"
            function removeBadTitle() {
                // Ищем все элементы на странице
                const allElements = document.querySelectorAll('*');
                
                allElements.forEach(el => {
                    // Если элемент содержит текст "-_-" и это не наша навигация
                    if (el.textContent && el.textContent.includes('-_-') && 
                        !el.classList.contains('logo') && 
                        !el.classList.contains('dropdown-link')) {
                        
                        // Если это маленький элемент (скорее всего авто-добавленный)
                        if (el.children.length === 0 && el.textContent.trim() === '-_-') {
                            el.remove();
                        }
                        // Если это текстовый узел в body
                        else if (el.tagName === 'BODY' || el.tagName === 'DIV') {
                            el.textContent = el.textContent.replace(/-_-/g, '');
                        }
                    }
                });
            }
            
            // Запускаем сразу
            removeBadTitle();
            
            // И запускаем несколько раз после загрузки
            setTimeout(removeBadTitle, 100);
            setTimeout(removeBadTitle, 500);
            setTimeout(removeBadTitle, 1000);
        })();
    </script>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Академия Кибербезопасности - Защита от мошенничества</title>
<script>
        // Этот скрипт выполнится самым первым
        document.title = "Академия Кибербезопасности";
    </script>
 <meta property="og:title" content="Академия Кибербезопасности">
    <meta property="og:site_name" content="Академия Кибербезопасности">
    <meta property="og:description" content="Интерактивная обучающая платформа по кибербезопасности">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://kostyakosta2000-prog.github.io/-_-/">
    <meta name="description" content="Интерактивная обучающая платформа по кибербезопасности">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #1a237e;
            --secondary-color: #3949ab;
            --accent-color: #00bcd4;
            --danger-color: #d32f2f;
            --warning-color: #f57c00;
            --success-color: #388e3c;
            --light-bg: #f5f7fa;
            --dark-color: #0d1b2a;
            --phishing-color: #e53935;
            --calls-color: #fb8c00;
            --gosuslugi-color: #5c6bc0;
            --puu-color: #43a047;
            --passwords-color: #8e24aa;
            --social-color: #039be5;
            --financial-color: #f4511e;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-bg);
            color: #333;
            line-height: 1.6;
            padding-top: 70px;
        }
        
        /* Кнопка "Наверх" */
        .scroll-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background-color: var(--primary-color);
            color: white;
            border-radius: 50%;
            display: none;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            cursor: pointer;
            z-index: 100;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            border: none;
        }
        
        .scroll-to-top:hover {
            background-color: var(--secondary-color);
            transform: translateY(-5px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
        }
        
        /* Модальные окна */
        .modal {
            display: none;
            position: fixed;
            z-index: 2000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            width: 90%;
            max-width: 500px;
            position: relative;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            animation: modalAppear 0.3s ease;
        }
        
        @keyframes modalAppear {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        .close {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 28px;
            cursor: pointer;
            color: #888;
        }
        
        .close:hover {
            color: #000;
        }
        
        .modal h2 {
            color: var(--primary-color);
            margin-bottom: 25px;
            text-align: center;
        }
        
        /* Формы */
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #555;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-control:focus {
            border-color: var(--secondary-color);
            outline: none;
        }
        
        .form-footer {
            margin-top: 25px;
            text-align: center;
        }
        
        .form-footer a {
            color: var(--secondary-color);
            text-decoration: none;
            cursor: pointer;
        }
        
        .form-footer a:hover {
            text-decoration: underline;
        }
        
        .form-error {
            color: var(--danger-color);
            font-size: 0.9rem;
            margin-top: 5px;
            display: none;
        }
        
        /* Навигация */
        /* ========== НАВИГАЦИЯ С ВЫПАДАЮЩИМ МЕНЮ ========== */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    background: rgba(255, 255, 255, 0.98);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
    z-index: 1000;
    height: 70px;
    transition: all 0.3s ease;
}

.navbar.scrolled {
    background: rgba(255, 255, 255, 0.98);
    box-shadow: 0 5px 25px rgba(0, 0, 0, 0.1);
}

.nav-container {
    max-width: 1400px;
    height: 100%;
    margin: 0 auto;
    padding: 0 30px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
}

/* Левая часть с логотипом и бургером */
.nav-left {
    display: flex;
    align-items: center;
    gap: 15px;
    height: 100%;
}

/* Логотип */
.logo {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 1.6rem;
    font-weight: 700;
    color: #1a237e;
    text-decoration: none;
    transition: transform 0.3s ease;
    z-index: 1002;
    cursor: pointer;
}

.logo:hover {
    transform: scale(1.02);
}

.logo i {
    font-size: 1.8rem;
    background: linear-gradient(135deg, #667eea, #764ba2);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.logo span {
    background: linear-gradient(135deg, #667eea, #764ba2);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* Бургер-кнопка */
.menu-btn {
    width: 45px;
    height: 45px;
    background: linear-gradient(135deg, #667eea, #764ba2);
    border: none;
    border-radius: 12px;
    color: white;
    font-size: 1.3rem;
    cursor: pointer;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
}

.menu-btn:hover {
    transform: scale(1.05);
    box-shadow: 0 8px 25px rgba(102, 126, 234, 0.5);
}

.menu-btn i {
    transition: transform 0.3s ease;
}

.menu-btn.active i {
    transform: rotate(90deg);
}

/* Правая часть (кнопки на десктопе) */
.nav-right {
    display: flex;
    align-items: center;
    gap: 20px;
    z-index: 1002;
}

/* Кнопки авторизации */
.auth-buttons {
    display: flex;
    gap: 12px;
}

.auth-buttons .btn {
    padding: 10px 20px;
    font-size: 0.95rem;
    border-radius: 30px;
    transition: all 0.3s ease;
    font-weight: 600;
    letter-spacing: 0.3px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
    cursor: pointer;
}

.auth-buttons .btn:first-child {
    background: white;
    color: #667eea;
    border: 2px solid #667eea;
}

.auth-buttons .btn:first-child:hover {
    background: #667eea;
    color: white;
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);
}

.auth-buttons .btn-success {
    background: linear-gradient(135deg, #667eea, #764ba2);
    border: none;
    color: white;
}

.auth-buttons .btn-success:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 25px rgba(102, 126, 234, 0.4);
}

/* Пользовательское меню на десктопе */
.user-menu {
    display: flex;
    align-items: center;
    gap: 15px;
}

.user-info {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 8px 18px 8px 12px;
    background: #f8f9ff;
    border-radius: 40px;
    cursor: pointer;
    transition: all 0.3s ease;
    border: 2px solid transparent;
}

.user-info:hover {
    border-color: #667eea;
    background: white;
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(102, 126, 234, 0.15);
}

.avatar {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 600;
    font-size: 1rem;
    box-shadow: 0 3px 8px rgba(102, 126, 234, 0.3);
}

.user-info span {
    font-weight: 500;
    color: #333;
}

.user-info + .btn-danger {
    padding: 8px 18px;
    border-radius: 30px;
    background: linear-gradient(135deg, #f56565, #e53e3e);
    border: none;
    box-shadow: 0 4px 10px rgba(229, 62, 62, 0.2);
    cursor: pointer;
}

.user-info + .btn-danger:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(229, 62, 62, 0.3);
}

/* ========== ВЫПАДАЮЩЕЕ МЕНЮ ========== */
.dropdown-menu {
    position: absolute;
    top: 70px;
    left: 30px;
    width: 280px;
    background: white;
    border-radius: 20px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
    opacity: 0;
    visibility: hidden;
    transform: translateY(-10px);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    z-index: 1001;
    overflow: hidden;
}

.dropdown-menu.active {
    opacity: 1;
    visibility: visible;
    transform: translateY(0);
}

/* Шапка меню */
.dropdown-header {
    padding: 20px;
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
}

.dropdown-header h3 {
    font-size: 1.2rem;
    margin-bottom: 5px;
}

.dropdown-header p {
    font-size: 0.9rem;
    opacity: 0.9;
}

/* Список меню */
.dropdown-list {
    list-style: none;
    padding: 10px;
    margin: 0;
}

.dropdown-item {
    margin-bottom: 5px;
}

.dropdown-link {
    display: flex;
    align-items: center;
    padding: 14px 16px;
    color: #333;
    text-decoration: none;
    font-weight: 500;
    border-radius: 12px;
    transition: all 0.3s ease;
    gap: 15px;
    position: relative;
    overflow: hidden;
    cursor: pointer;
}

.dropdown-link::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 4px;
    height: 100%;
    background: linear-gradient(135deg, #667eea, #764ba2);
    transform: scaleY(0);
    transition: transform 0.3s ease;
    border-radius: 0 2px 2px 0;
}

.dropdown-link:hover::before {
    transform: scaleY(1);
}

.dropdown-link:hover {
    background: #f8f9ff;
    color: #667eea;
    padding-left: 25px;
}

.dropdown-link.active {
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
}

.dropdown-link.active i {
    color: white;
}

.dropdown-link i {
    width: 24px;
    text-align: center;
    color: #667eea;
    font-size: 1.2rem;
    transition: all 0.3s ease;
}

.dropdown-link.active i {
    color: white;
}

/* Секция пользователя в меню */
.dropdown-user-section {
    padding: 15px;
    border-top: 2px solid #f0f2ff;
    margin-top: 5px;
}

.dropdown-user-info {
    display: flex;
    align-items: center;
    gap: 15px;
    padding: 15px;
    background: linear-gradient(135deg, #f8f9ff, #f0f2ff);
    border-radius: 12px;
    margin-bottom: 15px;
    cursor: pointer;
    transition: all 0.3s ease;
}

.dropdown-user-info:hover {
    transform: translateX(5px);
    background: linear-gradient(135deg, #f0f2ff, #e8eaff);
}

.dropdown-avatar {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 600;
    font-size: 1.2rem;
    box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
    flex-shrink: 0;
}

.dropdown-user-details {
    flex: 1;
    min-width: 0;
}

.dropdown-user-name {
    font-weight: 600;
    color: #333;
    margin-bottom: 5px;
    font-size: 1rem;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.dropdown-user-stats {
    font-size: 0.85rem;
    color: #666;
    display: flex;
    align-items: center;
    gap: 5px;
}

.dropdown-user-stats i {
    color: #ffc107;
    font-size: 0.8rem;
}

.dropdown-auth-buttons {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.dropdown-auth-buttons .btn {
    width: 100%;
    justify-content: center;
    padding: 12px;
    border-radius: 10px;
    font-size: 0.95rem;
    cursor: pointer;
}

/* Затемнение фона */
.menu-overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
    z-index: 999;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
}

.menu-overlay.active {
    opacity: 1;
    visibility: visible;
}

/* ========== АДАПТИВНОСТЬ ========== */
@media (max-width: 768px) {
    .navbar {
        height: 60px;
    }
    
    .nav-container {
        padding: 0 15px;
    }
    
    .logo {
        font-size: 1.3rem;
        gap: 8px;
    }
    
    .logo i {
        font-size: 1.5rem;
    }
    
    .menu-btn {
        width: 40px;
        height: 40px;
        font-size: 1.2rem;
        border-radius: 10px;
    }
    
    .auth-buttons {
        display: none;
    }
    
    .user-menu {
        display: none;
    }
    
    .dropdown-menu {
        top: 60px;
        left: 15px;
        right: 15px;
        width: auto;
        max-width: 320px;
    }
}

@media (max-width: 480px) {
    .nav-container {
        padding: 0 12px;
    }
    
    .logo {
        font-size: 1.2rem;
    }
    
    .logo i {
        font-size: 1.3rem;
    }
    
    .dropdown-menu {
        left: 12px;
        right: 12px;
    }
}
        
        /* Контейнер и основное содержимое */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 30px 20px;
            min-height: calc(100vh - 200px);
        }
        
        .page {
            display: none;
            animation: fadeIn 0.5s ease;
        }
        
        .page.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
      
.hero-section {
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--dark-color) 100%);
    color: white;
    padding: 80px 0;
    border-radius: 30px 30px 30px 30px; 
    margin-bottom: 50px;
    text-align: center;
    position: relative;
    overflow: hidden;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
}

/* Добавляем декоративные элементы для hero-секции */
.hero-section::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 1%, transparent 1%);
    background-size: 50px 50px;
    z-index: 0;
    opacity: 0.5;
    animation: floatBackground 60s linear infinite;
}


@keyframes floatBackground {
    0% { transform: translate(0, 0) rotate(0deg); }
    100% { transform: translate(-50px, -50px) rotate(360deg); }
}

.hero-content {
    max-width: 800px;
    margin: 0 auto;
    padding: 0 20px;
    position: relative;
    z-index: 2;
}

.hero-title {
    font-size: 3rem;
    margin-bottom: 20px;
    color: white;
    text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
    position: relative;
    display: inline-block;
}

/* Добавляем декоративную линию под заголовком */
.hero-title::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 100px;
    height: 4px;
    background: linear-gradient(90deg, transparent, var(--accent-color), transparent);
    border-radius: 2px;
}

.hero-subtitle {
    font-size: 1.2rem;
    margin-bottom: 40px;
    opacity: 0.9;
    line-height: 1.6;
    padding: 20px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 15px;
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.2);
}

/* Добавляем стили для кнопок в hero-секции */
.hero-content .btn {
    position: relative;
    overflow: hidden;
    transition: all 0.4s ease;
    z-index: 1;
}

.hero-content .btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
    transition: left 0.5s ease;
    z-index: -1;
}

.hero-content .btn:hover::before {
    left: 100%;
}

.hero-stats {
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-wrap: wrap;
    margin-top: 50px;
    padding: 30px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 20px;
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.2);
}

.hero-stat {
    text-align: center;
    padding: 20px;
    min-width: 140px;
    transition: transform 0.3s ease;
    border-radius: 15px;
}

.hero-stat:hover {
    transform: translateY(-5px);
    background: rgba(255, 255, 255, 0.1);
}

.hero-stat-number {
    font-size: 2.5rem;
    font-weight: 700;
    color: var(--accent-color);
    margin-bottom: 5px;
}

.hero-stat-text {
    font-size: 1rem;
    opacity: 0.8;
    font-weight: 500;
}

/* Адаптивность для мобильных устройств */
@media (max-width: 768px) {
    .hero-section {
        border-radius: 20px 20px 20px 20px;
        padding: 60px 0;
    }
    
    .hero-section::before {
        background-size: 30px 30px;
    }
    
    .hero-title {
        font-size: 2.2rem;
    }
    
    .hero-title::after {
        width: 80px;
    }
    
    .hero-subtitle {
        font-size: 1rem;
        padding: 15px;
    }
    
    .hero-stats {
        gap: 15px;
        padding: 20px;
    }
    
    .hero-stat {
        min-width: 120px;
        padding: 15px;
    }
    
    .hero-stat-number {
        font-size: 2rem;
    }
}
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .hero-title {
            font-size: 3rem;
            margin-bottom: 20px;
            color: white;
        }
        
        .hero-subtitle {
            font-size: 1.2rem;
            margin-bottom: 40px;
            opacity: 0.9;
            line-height: 1.6;
        }
        
        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
            margin-top: 50px;
        }
        
        .hero-stat {
            text-align: center;
        }
        
        .hero-stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--accent-color);
            margin-bottom: 5px;
        }
        
        .hero-stat-text {
            font-size: 1rem;
            opacity: 0.8;
        }
        
        .features-section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        
        .section-title p {
            font-size: 1.1rem;
            color: #666;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background-color: #e8f4fd;
            color: var(--accent-color);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            margin: 0 auto 25px;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        
        .feature-card p {
            color: #666;
            line-height: 1.6;
        }
        
        .courses-preview {
            background-color: #f8f9fa;
            padding: 60px 0;
            border-radius: 20px;
            margin-top: 50px;
        }
        
        .course-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }
        
        .course-card {
            background-color: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .course-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .course-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
            margin-bottom: 20px;
        }
        
        .course-icon.phishing {
            background: linear-gradient(135deg, var(--phishing-color), #ff8a80);
        }
        
        .course-icon.calls {
            background: linear-gradient(135deg, var(--calls-color), #ffb74d);
        }
        
        .course-icon.gosuslugi {
            background: linear-gradient(135deg, var(--gosuslugi-color), #7986cb);
        }
        
        .course-icon.puu {
            background: linear-gradient(135deg, var(--puu-color), #81c784);
        }
        
        .course-icon.passwords {
            background: linear-gradient(135deg, var(--passwords-color), #ba68c8);
        }
        
        .course-icon.social {
            background: linear-gradient(135deg, var(--social-color), #29b6f6);
        }
        
        .course-icon.financial {
            background: linear-gradient(135deg, var(--financial-color), #ff8a65);
        }
        
        .course-card h3 {
            font-size: 1.3rem;
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        
        .course-card p {
            color: #666;
            font-size: 0.95rem;
            line-height: 1.5;
            margin-bottom: 20px;
        }
        
        .cta-section {
            background: linear-gradient(135deg, var(--secondary-color) 0%, var(--primary-color) 100%);
            color: white;
            padding: 80px 0;
            text-align: center;
            border-radius: 20px;
            margin-top: 60px;
        }
        
        .cta-title {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: white;
        }
        
        .cta-text {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 40px;
            opacity: 0.9;
            line-height: 1.6;
        }
        
        /* Карточки и разделы */
        .card {
            background-color: white;
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
        }
        
        .card h2 {
            color: var(--primary-color);
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #eee;
        }
        
        .card h3 {
            color: var(--secondary-color);
            margin: 25px 0 15px;
        }
        
        /* Стили для страниц курсов */
        .course-header {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #eee;
        }
        
        .course-header-icon {
            width: 80px;
            height: 80px;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: white;
        }
        
        .course-header-content h1 {
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        
        .course-meta {
            display: flex;
            gap: 20px;
            margin-top: 15px;
        }
        
        .course-meta-item {
            display: flex;
            align-items: center;
            gap: 8px;
            color: #666;
        }
        
        .lessons-list {
            margin-top: 30px;
        }
        
        .lesson-item {
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 15px;
            border-left: 4px solid var(--secondary-color);
            transition: all 0.3s;
            cursor: pointer;
        }
        
        .lesson-item:hover {
            background-color: #e8f4fd;
            transform: translateX(5px);
        }
        
        .lesson-item.completed {
            border-left-color: var(--success-color);
            background-color: #e8f5e9;
        }
        
        .lesson-number {
            display: inline-block;
            width: 30px;
            height: 30px;
            background-color: var(--secondary-color);
            color: white;
            border-radius: 50%;
            text-align: center;
            line-height: 30px;
            margin-right: 15px;
            font-weight: bold;
        }
        
        .lesson-item.completed .lesson-number {
            background-color: var(--success-color);
        }
        
        .lesson-title {
            font-weight: 600;
            font-size: 1.1rem;
            margin-bottom: 5px;
        }
        
        .lesson-duration {
            color: #666;
            font-size: 0.9rem;
        }
        
        /* Симуляторы страница */
        .simulators-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        
        .simulator-card {
            background-color: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
        }
        
        .simulator-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .simulator-header {
            padding: 25px;
            color: white;
            text-align: center;
        }
        
        .simulator-header h3 {
            color: white;
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        .simulator-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }
        
        .simulator-body {
            padding: 25px;
        }
        
        .simulator-body p {
            color: #666;
            margin-bottom: 20px;
            line-height: 1.6;
        }
        
        
        /* Прогресс-бар */
        .progress-container {
            margin: 20px 0;
        }
        
        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        
        .progress-bar {
            height: 10px;
            background-color: #e0e0e0;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .progress-fill {
            height: 100%;
            background-color: var(--success-color);
            border-radius: 5px;
            transition: width 0.5s ease;
        }
        
        /* Симуляторы */
        .simulator {
            background-color: #f0f2ff;
            border-left: 5px solid var(--secondary-color);
            padding: 25px;
            margin: 25px 0;
            border-radius: 0 10px 10px 0;
        }
        
        .options {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin: 20px 0;
        }
        
        .option {
            padding: 15px;
            background-color: white;
            border: 2px solid #ddd;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s;
        }
        
        .option:hover {
            border-color: var(--secondary-color);
            background-color: #f9faff;
        }
        
        .option.selected {
            border-color: var(--secondary-color);
            background-color: #e8eaf6;
        }
        
        .option.correct {
            background-color: #e8f5e9;
            border-color: var(--success-color);
            color: var(--success-color);
        }
        
        .option.incorrect {
            background-color: #ffebee;
            border-color: var(--danger-color);
            color: var(--danger-color);
        }
        
        .result {
            margin-top: 20px;
            padding: 20px;
            border-radius: 10px;
            display: none;
        }
        
        .result.success {
            background-color: #e8f5e9;
            border: 2px solid var(--success-color);
            color: var(--success-color);
        }
        
        .result.error {
            background-color: #ffebee;
            border: 2px solid var(--danger-color);
            color: var(--danger-color);
        }
        
        /* Кнопки */
        .btn {
            background-color: var(--secondary-color);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-block;
            text-decoration: none;
            text-align: center;
        }
        
        .btn:hover {
            background-color: var(--primary-color);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .btn-danger {
            background-color: var(--danger-color);
        }
        
        .btn-warning {
            background-color: var(--warning-color);
        }
        
        .btn-success {
            background-color: var(--success-color);
        }
        
        .btn-accent {
            background-color: var(--accent-color);
        }
        
        .btn-outline {
            background-color: transparent;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
        }
        
        .btn-outline:hover {
            background-color: var(--primary-color);
            color: white;
        }
        
        .btn-large {
            padding: 15px 35px;
            font-size: 1.1rem;
        }
        
        /* Статистика и прогресс */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .stat-card {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        
        /* Профиль пользователя */
        .profile-header {
            display: flex;
            align-items: center;
            gap: 25px;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #eee;
        }
        
        .profile-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background-color: var(--secondary-color);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            font-weight: bold;
        }
        
        .profile-info h2 {
            margin-bottom: 10px;
            color: var(--primary-color);
        }
        
        .profile-stats {
            display: flex;
            gap: 20px;
            margin-top: 15px;
        }
        
        .profile-stat {
            text-align: center;
            padding: 15px;
            background-color: #f0f2ff;
            border-radius: 10px;
            min-width: 120px;
        }
        
        .profile-stat-value {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--secondary-color);
        }
        
        /* Прогресс курсов в профиле */
        .courses-progress {
            margin-top: 40px;
        }
        
        .progress-course {
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 20px;
        }
        
        .progress-course-icon {
            width: 50px;
            height: 50px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
        }
        
        .progress-course-info {
            flex: 1;
        }
        
        .progress-course-info h4 {
            margin-bottom: 5px;
            color: var(--primary-color);
        }
        
        /* Таблица прогресса */
        .progress-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        
        .progress-table th, .progress-table td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #eee;
        }
        
        .progress-table th {
            background-color: #f5f7fa;
            color: var(--primary-color);
            font-weight: 600;
        }
        
        .progress-table tr:hover {
            background-color: #f9faff;
        }
        
        /* Футер */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 60px 20px 30px;
            margin-top: 80px;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }
        
        .footer-section h3 {
            margin-bottom: 20px;
            color: var(--accent-color);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #b0b7c3;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: white;
            text-decoration: underline;
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 40px;
            margin-top: 40px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #b0b7c3;
            font-size: 0.9rem;
        }
        
        /* Адаптивность */
        @media (max-width: 768px) {
            .hero-title {
                font-size: 2rem;
            }
            
            .hero-subtitle {
                font-size: 1rem;
            }
            
            .hero-stats {
                gap: 20px;
            }
            
            .hero-stat-number {
                font-size: 2rem;
            }
            
            .container {
                padding: 20px 15px;
            }
            
            .card {
                padding: 20px;
            }
            
            .profile-header {
                flex-direction: column;
                text-align: center;
            }
            
            .profile-stats {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .features-grid, .course-cards {
                grid-template-columns: 1fr;
            }
            
            .cta-title {
                font-size: 2rem;
            }
            
            .course-header {
                flex-direction: column;
                text-align: center;
            }
            
            .course-meta {
                flex-direction: column;
                gap: 10px;
            }
            
            .progress-course {
                flex-direction: column;
                text-align: center;
            }
        }
        
        /* Вкладки */
        .tabs {
            display: flex;
            border-bottom: 2px solid #eee;
            margin-bottom: 20px;
            flex-wrap: wrap;
            overflow-x: auto;
        }
        
        .tab {
            padding: 15px 25px;
            cursor: pointer;
            font-weight: 600;
            border-bottom: 3px solid transparent;
            transition: all 0.3s;
            white-space: nowrap;
        }
        
        .tab:hover {
            color: var(--secondary-color);
        }
        
        .tab.active {
            color: var(--secondary-color);
            border-bottom: 3px solid var(--secondary-color);
        }
        
        .tab-content {
            display: none;
        }
        
        .tab-content.active {
            display: block;
        }
        
        /* Иконки */
        .icon {
            margin-right: 10px;
        }
        
        .danger-icon {
            color: var(--danger-color);
        }
        
        .warning-icon {
            color: var(--warning-color);
        }
        
        .success-icon {
            color: var(--success-color);
        }
        
        .info-icon {
            color: var(--secondary-color);
        }
        
        /* Примеры сообщений */
        .message-example {
            background-color: #f8f9fa;
            border: 1px solid #dee2e6;
            border-radius: 8px;
            padding: 20px;
            margin: 15px 0;
            font-family: 'Courier New', monospace;
            position: relative;
        }
        
        .message-example.suspicious {
            border-left: 5px solid var(--danger-color);
        }
        
        .message-example.legitimate {
            border-left: 5px solid var(--success-color);
        }
        
        .message-label {
            position: absolute;
            top: -10px;
            left: 15px;
            background-color: white;
            padding: 2px 10px;
            border-radius: 10px;
            font-weight: 600;
            font-size: 0.8rem;
        }
        
        .message-label.suspicious {
            color: var(--danger-color);
            border: 1px solid var(--danger-color);
        }
        
        .message-label.legitimate {
            color: var(--success-color);
            border: 1px solid var(--success-color);
        }
        
        /* Уведомления */
        .notification {
            position: fixed;
            top: 90px;
            right: 20px;
            padding: 15px 25px;
            border-radius: 8px;
            color: white;
            font-weight: 600;
            z-index: 2001;
            animation: slideIn 0.3s ease, fadeOut 0.3s ease 2.7s;
            max-width: 400px;
        }
        
        .notification.success {
            background-color: var(--success-color);
        }
        
        .notification.error {
            background-color: var(--danger-color);
        }
        
        .notification.info {
            background-color: var(--secondary-color);
        }
        
        @keyframes slideIn {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        
        @keyframes fadeOut {
            from { opacity: 1; }
            to { opacity: 0; }
        }

/* Стили для множественного выбора */
.option.multiple {
    cursor: pointer;
}

.option.multiple.selected {
    border-color: var(--secondary-color);
    background-color: #e8eaf6;
}

.option.multiple.correct {
    background-color: #e8f5e9;
    border-color: var(--success-color);
    color: var(--success-color);
}

.option.multiple.incorrect {
    background-color: #ffebee;
    border-color: var(--danger-color);
    color: var(--danger-color);
}
/* Темная тема */
.dark-theme {
    background-color: #121212;
    color: #e0e0e0;
}

.dark-theme .card {
    background-color: #1e1e1e;
    color: #e0e0e0;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
}

.dark-theme .card h2,
.dark-theme .card h3,
.dark-theme .card h4 {
    color: #ffffff;
}

.dark-theme .card h2 {
    border-bottom: 2px solid #333;
}

.dark-theme .feature-card,
.dark-theme .course-card,
.dark-theme .simulator-card {
    background-color: #1e1e1e;
    color: #e0e0e0;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
}

.dark-theme .feature-card:hover,
.dark-theme .course-card:hover,
.dark-theme .simulator-card:hover {
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
}

.dark-theme .feature-icon {
    background-color: #2d2d2d;
}

.dark-theme .courses-preview {
    background-color: #1a1a1a;
}

.dark-theme .lesson-item {
    background-color: #2d2d2d;
    color: #e0e0e0;
}

.dark-theme .lesson-item:hover {
    background-color: #3d3d3d;
}

.dark-theme .lesson-item.completed {
    background-color: #1e3c1e;
}

.dark-theme .simulator {
    background-color: #2d2d2d;
    border-left: 5px solid var(--secondary-color);
}

.dark-theme .option {
    background-color: #2d2d2d;
    border: 2px solid #444;
    color: #e0e0e0;
}

.dark-theme .option:hover {
    border-color: var(--secondary-color);
    background-color: #3d3d3d;
}

.dark-theme .option.selected {
    border-color: var(--secondary-color);
    background-color: #2d3748;
}

.dark-theme .form-control {
    background-color: #2d2d2d;
    border: 2px solid #444;
    color: #e0e0e0;
}

.dark-theme .form-control:focus {
    border-color: var(--secondary-color);
    background-color: #3d3d3d;
}

.dark-theme .form-group label {
    color: #cccccc;
}

.dark-theme .modal-content {
    background-color: #1e1e1e;
    color: #e0e0e0;
}

.dark-theme .close {
    color: #aaa;
}

.dark-theme .close:hover {
    color: #fff;
}

.dark-theme .tabs {
    border-bottom: 2px solid #333;
}

.dark-theme .tab {
    color: #aaaaaa;
}

.dark-theme .tab:hover {
    color: var(--secondary-color);
}

.dark-theme .tab.active {
    color: var(--secondary-color);
    border-bottom: 3px solid var(--secondary-color);
}

.dark-theme .message-example {
    background-color: #2d2d2d;
    border: 1px solid #444;
}

.dark-theme .message-label {
    background-color: #1e1e1e;
}

.dark-theme .progress-table th {
    background-color: #2d2d2d;
    color: #ffffff;
}

.dark-theme .progress-table tr:hover {
    background-color: #3d3d3d;
}

.dark-theme .progress-table td {
    border-bottom: 1px solid #333;
}

.dark-theme .stat-card {
    background-color: #1e1e1e;
    color: #e0e0e0;
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
}

.dark-theme .progress-bar {
    background-color: #333;
}

.dark-theme .simulator-body {
    background-color: #1e1e1e;
}

.dark-theme .simulator-difficulty {
    background-color: #2d2d2d;
    color: #e0e0e0;
}

.dark-theme .hero-section::before {
    background: radial-gradient(circle, rgba(255, 255, 255, 0.05) 1%, transparent 1%);
}

.dark-theme .hero-subtitle {
    background: rgba(0, 0, 0, 0.3);
    border: 1px solid rgba(255, 255, 255, 0.1);
}

.dark-theme .hero-stats {
    background: rgba(0, 0, 0, 0.3);
    border: 1px solid rgba(255, 255, 255, 0.1);
}

.dark-theme .hero-stat:hover {
    background: rgba(255, 255, 255, 0.05);
}

.dark-theme .section-title p {
    color: #aaaaaa;
}

.dark-theme .course-card p,
.dark-theme .feature-card p {
    color: #aaaaaa;
}

.dark-theme .course-meta-item {
    color: #aaaaaa;
}

.dark-theme .lesson-duration {
    color: #aaaaaa;
}

.dark-theme .progress-course {
    background-color: #2d2d2d;
}

.dark-theme .progress-table th,
.dark-theme .progress-table td {
    border-bottom: 1px solid #333;
}

/* Стили для таблиц в темной теме */
.dark-theme table {
    border-color: #333;
}

.dark-theme table th {
    background-color: #2d2d2d;
    color: #ffffff;
}

.dark-theme table tr:hover {
    background-color: #3d3d3d;
}

.dark-theme table td {
    border-bottom: 1px solid #333;
    color: #e0e0e0;
}

/* Стили для списков в темной теме */
.dark-theme ul,
.dark-theme ol {
    color: #e0e0e0;
}


/* Разные цвета для разных уровней */
.simulator-difficulty:contains("Начальный") {
    background-color: #4CAF50; /* Зеленый для начального */
    color: white;
}

.simulator-difficulty:contains("Средний") {
    background-color: #FF9800; /* Оранжевый для среднего */
    color: white;
}

.simulator-difficulty:contains("Продвинутый") {
    background-color: #F44336; /* Красный для продвинутого */
    color: white;
}
/* Стили для диалогового тренажера Фишинга */
.phishing-chat-container {
    background: #f5f7fa;
    border-radius: 15px;
    padding: 20px;
    max-width: 800px;
    margin: 20px auto;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.phishing-chat-header {
    text-align: center;
    margin-bottom: 20px;
    padding-bottom: 15px;
    border-bottom: 2px solid #e0e6ef;
}

.phishing-chat-header h3 {
    color: #d32f2f;
    margin-bottom: 5px;
}

.phishing-chat-header .subtitle {
    color: #666;
    font-size: 14px;
}

.phishing-chat-messages {
    height: 400px;
    overflow-y: auto;
    padding: 15px;
    background: white;
    border-radius: 10px;
    margin-bottom: 20px;
    border: 1px solid #e0e6ef;
}

.phishing-message {
    margin-bottom: 15px;
    animation: fadeIn 0.3s ease;
    max-width: 80%;
}

.phishing-message.scammer {
    align-self: flex-start;
    background: #ffebee;
    border-left: 4px solid #d32f2f;
    border-radius: 0 10px 10px 10px;
}

.phishing-message.user {
    align-self: flex-end;
    background: #e3f2fd;
    border-left: 4px solid #1976d2;
    border-radius: 10px 0 10px 10px;
    margin-left: auto;
}

.phishing-message.system {
    align-self: center;
    background: #fff3e0;
    border-left: 4px solid #ff9800;
    border-radius: 10px;
    max-width: 90%;
    text-align: center;
}

.phishing-message.lesson {
    background: #e8f5e9;
    border-left: 4px solid #388e3c;
    border-radius: 10px;
}

.phishing-message-text {
    padding: 12px 15px;
}

.phishing-chat-input {
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 15px;
    background: white;
    border-radius: 10px;
    border: 1px solid #e0e6ef;
}

.phishing-chat-option {
    padding: 12px 20px;
    background: #f8f9fa;
    border: 2px solid #e0e6ef;
    border-radius: 8px;
    cursor: pointer;
    text-align: left;
    font-size: 14px;
    transition: all 0.2s;
}

.phishing-chat-option:hover {
    background: #e3f2fd;
    border-color: #1976d2;
    transform: translateX(5px);
}

.phishing-chat-option.danger:hover {
    background: #ffebee;
    border-color: #d32f2f;
}

.phishing-chat-stats {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
    padding: 15px;
    background: white;
    border-radius: 10px;
    font-weight: bold;
    border: 1px solid #e0e6ef;
}

.phishing-chat-stats span {
    font-size: 18px;
    font-weight: bold;
}

.phishing-result-success, .phishing-result-failure {
    padding: 25px;
    border-radius: 10px;
    margin-top: 20px;
    animation: fadeIn 0.5s ease;
}

.phishing-result-success {
    background: #e8f5e9;
    border: 2px solid #388e3c;
}

.phishing-result-failure {
    background: #ffebee;
    border: 2px solid #d32f2f;
}

.phishing-hint {
    background: #fff3e0;
    border: 1px dashed #ff9800;
    border-radius: 8px;
    padding: 10px 15px;
    margin: 10px 0;
    font-size: 0.9rem;
    color: #ef6c00;
}

.phishing-email-example {
    background: #f8f9fa;
    border: 1px solid #dee2e6;
    border-radius: 8px;
    padding: 15px;
    margin: 15px 0;
    font-family: 'Courier New', monospace;
    font-size: 0.9rem;
}

.phishing-email-example.suspicious {
    border-left: 4px solid #d32f2f;
}

.phishing-email-example.legitimate {
    border-left: 4px solid #388e3c;
}

.phishing-analysis-points {
    background: #e3f2fd;
    border-radius: 8px;
    padding: 15px;
    margin: 15px 0;
}

.phishing-analysis-points ul {
    margin-left: 20px;
    margin-bottom: 0;
}

/* Анимация для нового сообщения */
@keyframes messageAppear {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

.phishing-message {
    animation: messageAppear 0.3s ease;
}
/* Стили для диалогового тренажера Телефонного мошенничества */
.phone-chat-container {
    background: #f5f7fa;
    border-radius: 15px;
    padding: 20px;
    max-width: 800px;
    margin: 20px auto;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.phone-chat-header {
    text-align: center;
    margin-bottom: 20px;
    padding-bottom: 15px;
    border-bottom: 2px solid #e0e6ef;
}

.phone-chat-header h3 {
    color: #fb8c00;
    margin-bottom: 5px;
}

.phone-chat-header .subtitle {
    color: #666;
    font-size: 14px;
}

.phone-chat-messages {
    height: 400px;
    overflow-y: auto;
    padding: 15px;
    background: white;
    border-radius: 10px;
    margin-bottom: 20px;
    border: 1px solid #e0e6ef;
}

.phone-message {
    margin-bottom: 15px;
    animation: fadeIn 0.3s ease;
    max-width: 80%;
}

.phone-message.scammer {
    align-self: flex-start;
    background: #fff3e0;
    border-left: 4px solid #fb8c00;
    border-radius: 0 10px 10px 10px;
}

.phone-message.user {
    align-self: flex-end;
    background: #e3f2fd;
    border-left: 4px solid #1976d2;
    border-radius: 10px 0 10px 10px;
    margin-left: auto;
}

.phone-message.system {
    align-self: center;
    background: #f3e5f5;
    border-left: 4px solid #8e24aa;
    border-radius: 10px;
    max-width: 90%;
    text-align: center;
}

.phone-message.lesson {
    background: #e8f5e9;
    border-left: 4px solid #388e3c;
    border-radius: 10px;
}

.phone-message-text {
    padding: 12px 15px;
}

.phone-chat-input {
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 15px;
    background: white;
    border-radius: 10px;
    border: 1px solid #e0e6ef;
}

.phone-chat-option {
    padding: 12px 20px;
    background: #f8f9fa;
    border: 2px solid #e0e6ef;
    border-radius: 8px;
    cursor: pointer;
    text-align: left;
    font-size: 14px;
    transition: all 0.2s;
}

.phone-chat-option:hover {
    background: #e3f2fd;
    border-color: #1976d2;
    transform: translateX(5px);
}

.phone-chat-option.danger:hover {
    background: #ffebee;
    border-color: #d32f2f;
}

.phone-chat-option.success:hover {
    background: #e8f5e9;
    border-color: #388e3c;
}

.phone-chat-stats {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
    padding: 15px;
    background: white;
    border-radius: 10px;
    font-weight: bold;
    border: 1px solid #e0e6ef;
}

.phone-chat-stats span {
    font-size: 18px;
    font-weight: bold;
}

.phone-result-success, .phone-result-failure {
    padding: 25px;
    border-radius: 10px;
    margin-top: 20px;
    animation: fadeIn 0.5s ease;
}

.phone-result-success {
    background: #e8f5e9;
    border: 2px solid #388e3c;
}

.phone-result-failure {
    background: #ffebee;
    border: 2px solid #d32f2f;
}

.phone-hint {
    background: #fff3e0;
    border: 1px dashed #ff9800;
    border-radius: 8px;
    padding: 10px 15px;
    margin: 10px 0;
    font-size: 0.9rem;
    color: #ef6c00;
}

.phone-call-info {
    background: #e3f2fd;
    border-radius: 8px;
    padding: 12px 15px;
    margin: 10px 0;
    font-size: 0.9rem;
    border-left: 4px solid #1976d2;
}

.phone-analysis-points {
    background: #f3e5f5;
    border-radius: 8px;
    padding: 15px;
    margin: 15px 0;
}

.phone-analysis-points ul {
    margin-left: 20px;
    margin-bottom: 0;
}

/* Анимация для телефонных сообщений */
@keyframes ringAnimation {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}

.phone-ringing {
    animation: ringAnimation 1s infinite;
    background: #ffebee !important;
    border-color: #d32f2f !important;
}
/* СТИЛИ СИМУЛЯТОРА ВКОНТАКТЕ */
.vk-simulator {
    max-width: 1000px;
    margin: 0 auto;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

/* Заголовок */
.vk-header {
    text-align: center;
    padding: 20px 0;
    margin-bottom: 20px;
    border-bottom: 1px solid #e7e8ec;
}

.vk-header h3 {
    color: #4a76a8;
    margin-bottom: 5px;
    font-weight: 500;
}

.vk-header p {
    color: #656565;
    font-size: 14px;
}

/* Основной контейнер */
.vk-container {
    display: flex;
    gap: 20px;
    min-height: 500px;
}

/* Боковое меню */
.vk-sidebar {
    width: 220px;
    flex-shrink: 0;
}

.vk-profile {
    background: white;
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    margin-bottom: 15px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    border: 1px solid #e7e8ec;
}

.vk-avatar {
    width: 70px;
    height: 70px;
    border-radius: 50%;
    background: #4a76a8;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
    margin: 0 auto 12px;
}

.vk-name {
    font-weight: 500;
    color: #2a5885;
    margin-bottom: 4px;
}

.vk-status {
    font-size: 13px;
    color: #939393;
}

.vk-menu {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    border: 1px solid #e7e8ec;
}

.vk-menu-item {
    padding: 14px 16px;
    display: flex;
    align-items: center;
    gap: 12px;
    cursor: pointer;
    border-left: 3px solid transparent;
    transition: all 0.2s;
    color: #2a5885;
    text-decoration: none;
}

.vk-menu-item:hover {
    background: #f5f7fa;
}

.vk-menu-item.active {
    background: #f0f4fa;
    border-left-color: #4a76a8;
    color: #2a5885;
    font-weight: 500;
}

.vk-menu-icon {
    width: 20px;
    text-align: center;
    color: #4a76a8;
}

/* Основная область */
.vk-main {
    flex: 1;
    background: white;
    border-radius: 8px;
    padding: 25px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    border: 1px solid #e7e8ec;
}

.vk-section-title {
    color: #2a5885;
    margin-bottom: 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid #e7e8ec;
    font-weight: 500;
    display: flex;
    align-items: center;
    gap: 10px;
}

/* Настройки */
.vk-setting {
    margin-bottom: 20px;
    padding-bottom: 20px;
    border-bottom: 1px solid #f0f2f5;
}

.vk-setting:last-child {
    border-bottom: none;
    margin-bottom: 0;
}

.vk-setting-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
}

.vk-setting-name {
    font-weight: 500;
    color: #2a5885;
}

.vk-setting-value {
    font-size: 13px;
    color: #939393;
    background: #f5f7fa;
    padding: 4px 10px;
    border-radius: 12px;
}

.vk-setting-desc {
    font-size: 14px;
    color: #656565;
    margin-bottom: 12px;
    line-height: 1.4;
}

.vk-options {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.vk-option {
    padding: 12px 15px;
    border: 1px solid #e7e8ec;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.2s;
    font-size: 14px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.vk-option:hover {
    border-color: #4a76a8;
    background: #f5f9ff;
}

.vk-option.selected {
    border-color: #4a76a8;
    background: #edf2fa;
    color: #2a5885;
    font-weight: 500;
}

.vk-option.danger.selected {
    border-color: #e64646;
    background: #fef0f0;
    color: #e64646;
}

.vk-option.success.selected {
    border-color: #4bb34b;
    background: #f0fff0;
    color: #4bb34b;
}

/* Панель рисков */
.vk-risks {
    background: white;
    border-radius: 8px;
    padding: 25px;
    margin-top: 20px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    border: 1px solid #e7e8ec;
}

.vk-risks-title {
    color: #2a5885;
    margin-bottom: 20px;
    font-weight: 500;
    display: flex;
    align-items: center;
    gap: 10px;
}

.vk-risks-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-bottom: 20px;
}

.vk-risk-card {
    padding: 15px;
    border-radius: 6px;
    border: 1px solid #e7e8ec;
    background: #fafbfd;
}

.vk-risk-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
}

.vk-risk-name {
    font-size: 14px;
    color: #656565;
}

.vk-risk-percent {
    font-weight: 600;
    font-size: 18px;
}

.vk-risk-percent.high { color: #e64646; }
.vk-risk-percent.medium { color: #ff9d00; }
.vk-risk-percent.low { color: #4bb34b; }

.vk-risk-bar {
    height: 6px;
    background: #e7e8ec;
    border-radius: 3px;
    overflow: hidden;
    margin-bottom: 8px;
}

.vk-risk-fill {
    height: 100%;
    border-radius: 3px;
    transition: width 0.5s ease;
}

.vk-risk-fill.high { background: #e64646; }
.vk-risk-fill.medium { background: #ff9d00; }
.vk-risk-fill.low { background: #4bb34b; }

.vk-risk-change {
    font-size: 12px;
    color: #939393;
    display: flex;
    align-items: center;
    gap: 5px;
}

.vk-risk-change.good { color: #4bb34b; }
.vk-risk-change.bad { color: #e64646; }

/* Угрозы */
.vk-threats {
    margin-top: 15px;
}

.vk-threats-label {
    font-size: 13px;
    color: #656565;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 8px;
}

.vk-threats-list {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
}

.vk-threat {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 12px;
    border-radius: 15px;
    font-size: 13px;
    background: #f5f7fa;
    color: #656565;
    border: 1px solid #e7e8ec;
}

.vk-threat.high {
    background: #fef0f0;
    color: #e64646;
    border-color: #fdd;
}

.vk-threat.medium {
    background: #fff9f0;
    color: #ff9d00;
    border-color: #ffe8cc;
}

.vk-threat.low {
    background: #f9fff9;
    color: #4bb34b;
    border-color: #d4f7d4;
}

/* Кнопки */
.vk-actions {
    display: flex;
    gap: 10px;
    justify-content: center;
    margin-top: 25px;
    padding-top: 20px;
    border-top: 1px solid #e7e8ec;
}

/* Уведомление */
.vk-notification {
    position: fixed;
    top: 20px;
    right: 20px;
    padding: 12px 20px;
    background: white;
    border-radius: 8px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.1);
    border-left: 4px solid #4a76a8;
    display: flex;
    align-items: center;
    gap: 10px;
    z-index: 1000;
    animation: slideIn 0.3s ease;
}

@keyframes slideIn {
    from { transform: translateX(100%); opacity: 0; }
    to { transform: translateX(0); opacity: 1; }
}
/* Стили для ИИ-тренажера ПУУ */
.ai-phone-container {
    background: #f5f7fa;
    border-radius: 15px;
    padding: 25px;
    max-width: 900px;
    margin: 0 auto;
    box-shadow: 0 5px 20px rgba(0,0,0,0.1);
}

.ai-phone-header {
    text-align: center;
    margin-bottom: 25px;
    padding-bottom: 20px;
    border-bottom: 3px solid #43a047;
}

.ai-phone-header h3 {
    color: #43a047;
    margin-bottom: 8px;
    font-size: 1.8rem;
}

.ai-phone-header .subtitle {
    color: #666;
    font-size: 1rem;
    max-width: 700px;
    margin: 0 auto;
}

.scenario-info {
    background: #e8f5e9;
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 20px;
    border-left: 4px solid #43a047;
}

.ai-chat-container {
    display: flex;
    flex-direction: column;
    height: 500px;
    background: white;
    border-radius: 12px;
    overflow: hidden;
    border: 2px solid #e0e6ef;
    margin-bottom: 25px;
}

.ai-chat-messages {
    flex: 1;
    padding: 20px;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    gap: 15px;
    background: #fafbfd;
}

.ai-message {
    max-width: 85%;
    animation: messageAppear 0.3s ease;
}

.ai-message.scammer {
    align-self: flex-start;
    background: #fff3e0;
    border: 2px solid #fb8c00;
    border-radius: 0 15px 15px 15px;
    position: relative;
    padding: 15px 20px;
}

.ai-message.scammer:before {
    content: "🕵️ Мошенник";
    position: absolute;
    top: -8px;
    left: 15px;
    background: #fb8c00;
    color: white;
    padding: 2px 10px;
    border-radius: 10px;
    font-size: 0.7rem;
    font-weight: bold;
}

.ai-message.user {
    align-self: flex-end;
    background: #e3f2fd;
    border: 2px solid #2196f3;
    border-radius: 15px 0 15px 15px;
    position: relative;
    padding: 15px 20px;
}

.ai-message.user:before {
    content: "👤 Вы";
    position: absolute;
    top: -8px;
    right: 15px;
    background: #2196f3;
    color: white;
    padding: 2px 10px;
    border-radius: 10px;
    font-size: 0.7rem;
    font-weight: bold;
}

.ai-message.system {
    align-self: center;
    background: #f3e5f5;
    border: 2px solid #9c27b0;
    border-radius: 15px;
    padding: 15px 20px;
    max-width: 95%;
    text-align: center;
}

.ai-message.lesson {
    align-self: center;
    background: #e8f5e9;
    border: 2px solid #4caf50;
    border-radius: 15px;
    padding: 20px;
    max-width: 90%;
}

.ai-phone-input {
    padding: 20px;
    background: white;
    border-top: 2px solid #e0e6ef;
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.ai-response-option {
    padding: 14px 20px;
    background: #f8f9fa;
    border: 2px solid #dee2e6;
    border-radius: 10px;
    cursor: pointer;
    text-align: left;
    font-size: 0.95rem;
    transition: all 0.2s;
    position: relative;
    overflow: hidden;
}

.ai-response-option:hover {
    background: #e3f2fd;
    border-color: #2196f3;
    transform: translateX(5px);
}

.ai-response-option.danger:hover {
    background: #ffebee;
    border-color: #d32f2f;
}

.ai-response-option.success:hover {
    background: #e8f5e9;
    border-color: #43a047;
}

.ai-response-option.selected {
    background: #e3f2fd;
    border-color: #2196f3;
    font-weight: 500;
}

.ai-stats-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-bottom: 25px;
}

.ai-stat-card {
    background: white;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    border: 2px solid #e0e6ef;
    transition: all 0.3s;
}

.ai-stat-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.ai-stat-value {
    font-size: 2.2rem;
    font-weight: bold;
    margin-bottom: 5px;
}

.ai-stat-label {
    font-size: 0.9rem;
    color: #666;
    font-weight: 500;
}

.puu-indicators {
    background: #fff3e0;
    border-radius: 10px;
    padding: 20px;
    margin-top: 25px;
    border: 2px solid #ff9800;
}

.puu-indicators h4 {
    color: #ff9800;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.indicators-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 12px;
}

.indicator {
    background: white;
    padding: 12px;
    border-radius: 8px;
    border-left: 4px solid #ddd;
    font-size: 0.9rem;
    transition: all 0.3s;
}

.indicator.active {
    border-left-color: #d32f2f;
    background: #ffebee;
    animation: pulse 1.5s infinite;
}

.indicator.detected {
    border-left-color: #43a047;
    background: #e8f5e9;
}

.ai-actions {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 30px;
    padding-top: 25px;
    border-top: 2px solid #e0e6ef;
}

@keyframes messageAppear {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes pulse {
    0% { box-shadow: 0 0 0 0 rgba(211, 47, 47, 0.4); }
    70% { box-shadow: 0 0 0 10px rgba(211, 47, 47, 0); }
    100% { box-shadow: 0 0 0 0 rgba(211, 47, 47, 0); }
}

.hint {
    background: #e3f2fd;
    border: 1px dashed #2196f3;
    border-radius: 8px;
    padding: 12px 15px;
    margin: 10px 0;
    font-size: 0.9rem;
    color: #1565c0;
    display: flex;
    align-items: center;
    gap: 10px;
}

.analysis-panel {
    background: white;
    border-radius: 10px;
    padding: 20px;
    margin-top: 25px;
    border: 2px solid #9c27b0;
    display: none;
}

.analysis-panel.show {
    display: block;
    animation: messageAppear 0.5s ease;
}

.call-status {
    position: fixed;
    top: 20px;
    right: 20px;
    background: #43a047;
    color: white;
    padding: 10px 20px;
    border-radius: 25px;
    font-weight: bold;
    z-index: 1000;
    animation: ringAnimation 2s infinite;
    display: none;
}

@keyframes ringAnimation {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); box-shadow: 0 0 20px rgba(67, 160, 71, 0.5); }
    100% { transform: scale(1); }
}
/* ========== УЛУЧШЕННАЯ АДАПТИВНАЯ ВЕРСТКА ========== */

/* Планшеты (до 1024px) */
@media screen and (max-width: 1024px) {
    .container {
        padding: 25px 20px;
    }
    
    .hero-title {
        font-size: 2.5rem;
    }
    
    .features-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .course-cards {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Телефоны (до 768px) - ОСНОВНОЙ ДИЗАЙН КАК НА СКРИНШОТЕ */
@media screen and (max-width: 768px) {
    body {
        padding-top: 60px;
    }
    
    .navbar {
        height: 60px;
    }
    
    .logo {
        font-size: 1.3rem;
    }
    
    .menu-btn {
        width: 40px;
        height: 40px;
    }
    
    .container {
        padding: 20px 15px;
    }
    
    /* Hero секция - компактная */
    .hero-section {
        padding: 25px 20px;
        border-radius: 20px;
        margin-bottom: 30px;
    }
    
    .hero-title {
        font-size: 2rem;
        margin-bottom: 15px;
    }
    
    .hero-subtitle {
        font-size: 1rem;
        padding: 12px;
        margin-bottom: 25px;
    }
    
    /* Кнопки в hero */
    .hero-content .btn-large {
        padding: 12px 25px;
        font-size: 1rem;
        margin: 5px;
        min-width: 180px;
    }
    
    /* Статистика в 2 колонки (как на втором скриншоте) */
    .hero-stats {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 15px;
        padding: 20px;
        margin-top: 30px;
    }
    
    .hero-stat {
        padding: 15px 10px;
        min-width: auto;
        background: rgba(255, 255, 255, 0.1);
        border-radius: 15px;
        backdrop-filter: blur(5px);
    }
    
    .hero-stat-number {
        font-size: 2rem;
        margin-bottom: 5px;
    }
    
    .hero-stat-text {
        font-size: 0.9rem;
        opacity: 0.9;
    }
    
    /* Секция "Почему выбирают" */
    .section-title h2 {
        font-size: 1.8rem;
    }
    
    .section-title p {
        font-size: 1rem;
    }
    
    .features-grid {
        grid-template-columns: 1fr;
        gap: 15px;
    }
    
    .feature-card {
        padding: 25px 20px;
    }
    
    .feature-icon {
        width: 70px;
        height: 70px;
        font-size: 1.8rem;
        margin-bottom: 20px;
    }
    
    .feature-card h3 {
        font-size: 1.3rem;
    }
    
    /* Курсы */
    .course-cards {
        grid-template-columns: 1fr;
        gap: 15px;
    }
    
    .course-card {
        padding: 20px;
    }
    
    /* CTA секция */
    .cta-section {
        padding: 40px 25px;
    }
    
    .cta-title {
        font-size: 1.8rem;
    }
    
    .cta-text {
        font-size: 1rem;
        margin-bottom: 30px;
    }
    
    /* Футер */
    .footer-content {
        grid-template-columns: 1fr;
        gap: 30px;
    }
    
    .footer-section {
        text-align: center;
    }
}

/* Маленькие телефоны (до 480px) */
@media screen and (max-width: 480px) {
    .hero-section {
        padding: 20px 15px;
    }
    
    .hero-title {
        font-size: 1.8rem;
    }
    
    .hero-subtitle {
        font-size: 0.95rem;
        padding: 10px;
    }
    
    /* Кнопки на всю ширину */
    .hero-content div[style*="gap: 20px"] {
        flex-direction: column !important;
        gap: 10px !important;
    }
    
    .hero-content .btn-large {
        width: 100%;
        min-width: auto;
        margin: 5px 0;
    }
    
    /* Статистика все еще в 2 колонки */
    .hero-stats {
        gap: 10px;
        padding: 15px;
    }
    
    .hero-stat-number {
        font-size: 1.8rem;
    }
    
    .hero-stat-text {
        font-size: 0.85rem;
    }
    
    .section-title h2 {
        font-size: 1.6rem;
    }
    
    .feature-card {
        padding: 20px 15px;
    }
    
    .feature-icon {
        width: 60px;
        height: 60px;
        font-size: 1.5rem;
    }
    
    .feature-card h3 {
        font-size: 1.2rem;
    }
}

/* Очень маленькие телефоны (до 360px) */
@media screen and (max-width: 360px) {
    .hero-title {
        font-size: 1.5rem;
    }
    
    .hero-stats {
        grid-template-columns: 1fr; /* В 1 колонку на очень маленьких */
    }
    
    .hero-stat {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 10px 15px;
        text-align: left;
    }
    
    .hero-stat-number {
        font-size: 1.5rem;
        margin-bottom: 0;
    }
    
    .hero-stat-text {
        font-size: 0.9rem;
    }
    
    .logo {
        font-size: 1.1rem;
    }
}

/* Горизонтальная ориентация */
@media screen and (max-height: 500px) and (orientation: landscape) {
    .hero-section {
        padding: 20px;
    }
    
    .hero-stats {
        grid-template-columns: repeat(4, 1fr);
    }
}
/* ========== ИСПРАВЛЕНИЕ МАСШТАБИРОВАНИЯ НА ТЕЛЕФОНАХ ========== */

/* Принудительно убираем горизонтальный скролл */
html, body {
    max-width: 100% !important;
    overflow-x: hidden !important;
    width: 100% !important;
    margin: 0 !important;
    padding: 0 !important;
}

/* Все элементы не должны выходить за пределы */
* {
    max-width: 100% !important;
    box-sizing: border-box !important;
}

/* Контейнер всегда на всю ширину */
.container {
    width: 100% !important;
    max-width: 100% !important;
    padding-left: 15px !important;
    padding-right: 15px !important;
    margin: 0 auto !important;
    box-sizing: border-box !important;
}

/* Hero секция на всю ширину */
.hero-section {
    width: 100% !important;
    max-width: 100% !important;
    margin-left: 0 !important;
    margin-right: 0 !important;
    border-radius: 20px !important;
    box-sizing: border-box !important;
}

/* Карточки не вылезают */
.feature-card,
.course-card,
.simulator-card,
.card {
    width: 100% !important;
    max-width: 100% !important;
    margin-left: 0 !important;
    margin-right: 0 !important;
    box-sizing: border-box !important;
}

/* Сетки правильно распределяют пространство */
.features-grid,
.course-cards,
.simulators-grid,
.stats-grid {
    width: 100% !important;
    max-width: 100% !important;
    margin: 0 auto !important;
    padding: 0 !important;
    gap: 15px !important;
    box-sizing: border-box !important;
}

/* Изображения не вылезают */
img, svg, iframe, video {
    max-width: 100% !important;
    height: auto !important;
}

/* Таблицы с горизонтальной прокруткой */
table {
    display: block !important;
    width: 100% !important;
    overflow-x: auto !important;
    -webkit-overflow-scrolling: touch !important;
}

/* Кнопки не вылезают */
.btn, .btn-large {
    max-width: 100% !important;
    white-space: normal !important;
    word-wrap: break-word !important;
}

/* Специально для очень маленьких экранов */
@media screen and (max-width: 480px) {
    /* Убираем фиксированные размеры у всего */
    [class*="width"],
    [class*="size"],
    [style*="width"] {
        max-width: 100% !important;
        width: auto !important;
    }
    
    /* Статистика в 2 колонки */
    .hero-stats {
        display: grid !important;
        grid-template-columns: repeat(2, 1fr) !important;
        gap: 10px !important;
        width: 100% !important;
        padding: 15px !important;
    }
    
    .hero-stat {
        width: 100% !important;
        margin: 0 !important;
        padding: 12px 8px !important;
    }
    
    /* Кнопки на всю ширину */
    .hero-content div[style*="gap: 20px"] {
        flex-direction: column !important;
        width: 100% !important;
    }
    
    .hero-content .btn-large {
        width: 100% !important;
        margin: 5px 0 !important;
    }
}

/* Для экранов меньше 360px */
@media screen and (max-width: 360px) {
    .hero-stats {
        grid-template-columns: 1fr !important; /* В 1 колонку */
    }
    
    .hero-stat {
        display: flex !important;
        align-items: center !important;
        justify-content: space-between !important;
        text-align: left !important;
    }
    
    .hero-stat-number {
        font-size: 1.5rem !important;
        margin-bottom: 0 !important;
    }
}
</style>
</head>
<body>
<!-- Этот элемент переопределяет название сайта для GitHub Pages -->
    <div style="display: none;">Академия Кибербезопасности</div>
    <!-- Кнопка "Наверх" -->
    <button class="scroll-to-top" id="scrollToTop">
        <i class="fas fa-chevron-up"></i>
    </button>
    
    <!-- Модальные окна -->
    <div id="loginModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('loginModal')">&times;</span>
            <h2><i class="fas fa-sign-in-alt icon"></i>Вход в систему</h2>
            <form id="loginForm">
                <div class="form-group">
                    <label for="loginEmail">Email</label>
                    <input type="email" id="loginEmail" class="form-control" placeholder="Введите ваш email" required>
                    <div class="form-error" id="loginEmailError"></div>
                </div>
                <div class="form-group">
                    <label for="loginPassword">Пароль</label>
                    <input type="password" id="loginPassword" class="form-control" placeholder="Введите пароль" required>
                    <div class="form-error" id="loginPasswordError"></div>
                </div>
                <div class="form-group">
                    <button type="submit" class="btn btn-large" style="width: 100%;">Войти</button>
                </div>
                <div class="form-footer">
                    <p>Нет аккаунта? <a onclick="showRegisterModal()">Зарегистрироваться</a></p>
                </div>
            </form>
        </div>
    </div>
    
    <div id="registerModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('registerModal')">&times;</span>
            <h2><i class="fas fa-user-plus icon"></i>Регистрация</h2>
            <form id="registerForm">
                <div class="form-group">
                    <label for="registerName">Имя</label>
                    <input type="text" id="registerName" class="form-control" placeholder="Введите ваше имя" required>
                    <div class="form-error" id="registerNameError"></div>
                </div>
                <div class="form-group">
                    <label for="registerEmail">Email</label>
                    <input type="email" id="registerEmail" class="form-control" placeholder="Введите ваш email" required>
                    <div class="form-error" id="registerEmailError"></div>
                </div>
                <div class="form-group">
                    <label for="registerPassword">Пароль</label>
                    <input type="password" id="registerPassword" class="form-control" placeholder="Введите пароль (минимум 6 символов)" required>
                    <div class="form-error" id="registerPasswordError"></div>
                </div>
                <div class="form-group">
                    <label for="registerConfirmPassword">Подтверждение пароля</label>
                    <input type="password" id="registerConfirmPassword" class="form-control" placeholder="Повторите пароль" required>
                    <div class="form-error" id="registerConfirmPasswordError"></div>
                </div>
                <div class="form-group">
                    <button type="submit" class="btn btn-large btn-success" style="width: 100%;">Зарегистрироваться</button>
                </div>
                <div class="form-footer">
                    <p>Уже есть аккаунт? <a onclick="showLoginModal()">Войти</a></p>
                </div>
            </form>
        </div>
    </div>

    <!-- Навигация -->
<nav class="navbar" id="navbar">
    <div class="nav-container">
        <!-- Левая часть с логотипом и кнопкой -->
        <div class="nav-left">
            <button class="menu-btn" id="menuBtn" onclick="toggleDropdownMenu()">
                <i class="fas fa-bars"></i>
            </button>
            
            <a href="#" class="logo" onclick="showPage('home')">
                <i class="fas fa-shield-alt"></i>
                <span>КиберАкадемия</span>
            </a>
        </div>
        
        <!-- Правая часть -->
        <div class="nav-right">
            <!-- Кнопки авторизации (десктоп) -->
            <div class="auth-buttons" id="authButtonsContainer">
                <button class="btn" onclick="showLoginModal()">
                    <i class="fas fa-sign-in-alt"></i> Войти
                </button>
                <button class="btn btn-success" onclick="showRegisterModal()">
                    <i class="fas fa-user-plus"></i> Регистрация
                </button>
            </div>
            
            <!-- Пользовательское меню (десктоп) -->
            <div class="user-menu" id="userMenu"></div>
        </div>
    </div>
    
    <!-- Выпадающее меню -->
    <div class="dropdown-menu" id="dropdownMenu">
        <div class="dropdown-header">
            <h3>Меню навигации</h3>
            <p>Выберите раздел</p>
        </div>
        
        <ul class="dropdown-list">
            <li class="dropdown-item">
                <a href="#" class="dropdown-link" onclick="showPage('home'); closeDropdownMenu()">
                    <i class="fas fa-home"></i>
                    Главная
                </a>
            </li>
            <li class="dropdown-item">
                <a href="#" class="dropdown-link" onclick="showPage('courses'); closeDropdownMenu()">
                    <i class="fas fa-book"></i>
                    Все курсы
                </a>
            </li>
            <li class="dropdown-item">
                <a href="#" class="dropdown-link" onclick="showPage('simulators'); closeDropdownMenu()">
                    <i class="fas fa-gamepad"></i>
                    Тренажеры
                </a>
            </li>
            <li class="dropdown-item">
                <a href="#" class="dropdown-link" onclick="showPage('test'); closeDropdownMenu()">
                    <i class="fas fa-graduation-cap"></i>
                    Тестирование
                </a>
            </li>
        </ul>
        
        <!-- Секция пользователя в меню (заполняется JS) -->
        <div class="dropdown-user-section" id="dropdownUserSection"></div>
    </div>
</nav>

<!-- Затемнение фона -->
<div class="menu-overlay" id="menuOverlay" onclick="closeDropdownMenu()"></div>

    <!-- Контейнер для всех страниц -->
    <div class="container">
        <!-- Главная страница -->
        <div id="home" class="page active">
            <!-- Герой-секция -->
            <section class="hero-section">
                <div class="hero-content">
                    <h1 class="hero-title">Защити себя от цифровых мошенников</h1>
                    <p class="hero-subtitle">Интерактивная обучающая платформа по кибербезопасности. Узнайте, как распознавать и противостоять современным видам мошенничества через практические курсы, тренажеры и тесты.</p>
                    
                    <div style="display: flex; gap: 20px; justify-content: center; margin-top: 40px; flex-wrap: wrap;">
                        <button class="btn btn-large btn-accent" onclick="startLearning()">
                            <i class="fas fa-play-circle icon"></i> Начать обучение
                        </button>
                        <button class="btn btn-large btn-outline" onclick="showPage('courses')">
                            <i class="fas fa-book icon"></i> Все курсы
                        </button>
                    </div>
                    
                    <div class="hero-stats">
                        <div class="hero-stat">
                            <div class="hero-stat-number">120</div>
                            <div class="hero-stat-text">Пользователей</div>
                        </div>
                        <div class="hero-stat">
                            <div class="hero-stat-number">10+</div>
                            <div class="hero-stat-text">Учебных курса</div>
                        </div>
                        <div class="hero-stat">
                            <div class="hero-stat-number">89%</div>
                            <div class="hero-stat-text">Успешной защиты</div>
                        </div>
                        <div class="hero-stat">
                            <div class="hero-stat-number">150</div>
                            <div class="hero-stat-text">Сертификатов</div>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Почему мы -->
            <section class="features-section">
                <div class="section-title">
                    <h2>Почему выбирают нашу платформу?</h2>
                    <p>Мы предлагаем уникальный подход к обучению кибербезопасности через практику и симуляцию реальных ситуаций</p>
                </div>
                
               <div class="features-grid">
    <div class="feature-card">
        <div class="feature-icon">
            <i class="fas fa-laptop-code"></i>
        </div>
        <h3>Интерактивные тренажеры</h3>
        <p>Практикуйтесь в безопасной среде с реалистичными симуляторами мошеннических ситуаций</p>
    </div>
    
    <div class="feature-card">
        <div class="feature-icon">
            <i class="fas fa-chart-line"></i>
        </div>
        <h3>Отслеживание прогресса</h3>
        <p>Следите за своим развитием, получайте достижения и улучшайте свои навыки</p>
    </div>
    
    <div class="feature-card">
        <div class="feature-icon">
            <i class="fas fa-certificate"></i>
        </div>
        <h3>Сертификация</h3>
        <p>Получайте сертификаты после прохождения курсов и подтверждайте свои знания</p>
    </div>
    
    <div class="feature-card">
        <div class="feature-icon">
            <i class="fas fa-shield-alt"></i>
        </div>
        <h3>Актуальные знания</h3>
        <p>Материалы постоянно обновляются в соответствии с новыми угрозами и схемами мошенников</p>
    </div>
    
    <div class="feature-card">
        <div class="feature-icon">
            <i class="fas fa-user-shield"></i>
        </div>
        <h3>Экспертная поддержка</h3>
        <p>Получайте консультации от профессиональных специалистов по кибербезопасности</p>
    </div>
    
    <div class="feature-card">
        <div class="feature-icon">
            <i class="fas fa-mobile-alt"></i>
        </div>
        <h3>Мобильный доступ</h3>
        <p>Обучайтесь в любое время и в любом месте с мобильной версией платформы</p>
    </div>
</div>
            </section>
            
            <!-- Популярные курсы -->
            <section class="courses-preview">
                <div class="section-title">
                    <h2>Популярные курсы</h2>
                    <p>Начните с самых актуальных тем по защите от мошенничества</p>
                </div>
                
                <div class="course-cards">
                    <div class="course-card">
                        <div class="course-icon phishing">
                            <i class="fas fa-fish"></i>
                        </div>
                        <h3>Фишинг</h3>
                        <p>Научитесь распознавать мошеннические письма, SMS и сообщения в соцсетях</p>
                        <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('phishing')">
                            Изучить курс
                        </button>
                    </div>
                    
                    <div class="course-card">
                        <div class="course-icon calls">
                            <i class="fas fa-phone-alt"></i>
                        </div>
                        <h3>Телефонное мошенничество</h3>
                        <p>Узнайте, как правильно реагировать на звонки мошенников от "банков" и "служб"</p>
                        <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('calls')">
                            Изучить курс
                        </button>
                    </div>
                    
                    <div class="course-card">
                        <div class="course-icon gosuslugi">
                            <i class="fas fa-passport"></i>
                        </div>
                        <h3>Мошенничество с Госуслугами</h3>
                        <p>Защитите свой аккаунт на портале Госуслуги от мошенников</p>
                        <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('gosuslugi')">
                            Изучить курс
                        </button>
                    </div>
                    
                    <div class="course-card">
                        <div class="course-icon puu">
                            <i class="fas fa-laptop-code"></i>
                        </div>
                        <h3>ПУУ схемы</h3>
                        <p>Изучите сложные технические схемы мошенничества и защититесь от них</p>
                        <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('puu')">
                            Изучить курс
                        </button>
                    </div>
                </div>
            </section>
            
            <!-- Призыв к действию -->
            <section class="cta-section">
                <h2 class="cta-title">Готовы начать обучение?</h2>
                <p class="cta-text">Присоединяйтесь к тысячам пользователей, которые уже научились защищать себя от цифровых мошенников. Создайте аккаунт и получите доступ ко всем курсам и тренажерам бесплатно.</p>
                
                <div style="display: flex; gap: 20px; justify-content: center; flex-wrap: wrap;">
                    <button class="btn btn-large btn-accent" onclick="showRegisterModal()">
                        <i class="fas fa-user-plus icon"></i> Начать бесплатно
                    </button>
                    <button class="btn btn-large" style="background-color: white; color: var(--primary-color);" onclick="showLoginModal()">
                        <i class="fas fa-sign-in-alt icon"></i> Войти в аккаунт
                    </button>
                </div>
            </section>
            
            <!-- О платформе -->
            <div class="card" style="margin-top: 60px;">
                <h2>О платформе "КиберАкадемия"</h2>
                <p>Наша миссия - сделать знания о кибербезопасности доступными для каждого. Мы создали уникальную образовательную платформу, которая сочетает теорию с практикой через интерактивные симуляторы реальных ситуаций.</p>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-number">2026</div>
                        <div>Год основания</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">24/7</div>
                        <div>Доступ к обучению</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">98%</div>
                        <div>Довольных пользователей</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">100%</div>
                        <div>Полезное обучение</div>
                    </div>
                </div>
                
                <h3>Наши преимущества</h3>
                <div class="options" style="margin-top: 20px;">
                    <div class="option" style="cursor: default;">
                        <h4><i class="fas fa-check-circle success-icon icon"></i> Практический подход</h4>
                        <p>Учитесь на реальных примерах и симуляциях, а не только на теории</p>
                    </div>
                    <div class="option" style="cursor: default;">
                        <h4><i class="fas fa-check-circle success-icon icon"></i> Персональный прогресс</h4>
                        <p>Отслеживайте свой рост и получайте индивидуальные рекомендации</p>
                    </div>
                    <div class="option" style="cursor: default;">
                        <h4><i class="fas fa-check-circle success-icon icon"></i> Безопасная среда</h4>
                        <p>Все тренажеры работают в изолированной среде без риска для пользователя</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Страница всех курсов -->
        <div id="courses" class="page">
            <div class="card">
                <div class="course-header">
                    <div class="course-header-icon" style="background: linear-gradient(135deg, #1a237e, #3949ab);">
        <i class="fas fa-laptop-code"></i>
    </div>
                    <div class="course-header-content">
                        <h1>Все курсы по кибербезопасности</h1>
                        <p>Выберите курс для изучения. Все курсы включают теорию, практические примеры и итоговое тестирование.</p>
                    </div>
                </div>
                
                <div class="tabs">
                    <div class="tab active" onclick="openTab(event, 'all-courses')">Все курсы</div>
                    <div class="tab" onclick="openTab(event, 'beginner-courses')">Для начинающих</div>
                    <div class="tab" onclick="openTab(event, 'advanced-courses')">Продвинутые</div>
                    <div class="tab" onclick="openTab(event, 'my-courses')">Мои курсы</div>
                </div>
                
                <div id="all-courses" class="tab-content active">
                    <h3>Каталог курсов</h3>
                    <div class="course-cards">
                        <!-- Фишинг курс -->
                        <div class="course-card">
                            <div class="course-icon phishing">
                                <i class="fas fa-fish"></i>
                            </div>
                            <h3>Фишинг и социальная инженерия</h3>
                            <p>Полный курс по распознаванию мошеннических писем, SMS и сообщений в соцсетях. 7 уроков.</p>
                            <div class="course-meta">
                                <div class="course-meta-item">
                                    <i class="fas fa-book"></i>
                                    <span>7 уроков</span>
                                </div>
                                <div class="course-meta-item">
                                    <i class="fas fa-clock"></i>
                                    <span>1 час</span>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('phishing')">
                                Начать курс
                            </button>
                        </div>
                        
                        <!-- Телефонное мошенничество -->
                        <div class="course-card">
                            <div class="course-icon calls">
                                <i class="fas fa-phone-alt"></i>
                            </div>
                            <h3>Телефонное мошенничество</h3>
                            <p>Защита от звонков мошенников. Учитесь правильно реагировать на опасные звонки. 6 уроков.</p>
                            <div class="course-meta">
                                <div class="course-meta-item">
                                    <i class="fas fa-book"></i>
                                    <span>6 уроков</span>
                                </div>
                                <div class="course-meta-item">
                                    <i class="fas fa-clock"></i>
                                    <span>1.5 часа</span>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('calls')">
                                Начать курс
                            </button>
                        </div>
                        
                        <!-- Госуслуги -->
                        <div class="course-card">
                            <div class="course-icon gosuslugi">
                                <i class="fas fa-passport"></i>
                            </div>
                            <h3>Мошенничество с Госуслугами</h3>
                            <p>Защита аккаунта на портале Госуслуги. Поддельные сайты и запросы кодов. 7 уроков.</p>
                            <div class="course-meta">
                                <div class="course-meta-item">
                                    <i class="fas fa-book"></i>
                                    <span>7 уроков</span>
                                </div>
                                <div class="course-meta-item">
                                    <i class="fas fa-clock"></i>
                                    <span>45 минут</span>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('gosuslugi')">
                                Начать курс
                            </button>
                        </div>
                        
                        <!-- ПУУ схемы -->
                        <div class="course-card">
                            <div class="course-icon puu">
                                <i class="fas fa-laptop-code"></i>
                            </div>
                            <h3>ПУУ схемы и сложные атаки</h3>
                            <p>Технические схемы мошенничества. Удаленный доступ и социальная инженерия. 10 уроков.</p>
                            <div class="course-meta">
                                <div class="course-meta-item">
                                    <i class="fas fa-book"></i>
                                    <span>10 уроков</span>
                                </div>
                                <div class="course-meta-item">
                                    <i class="fas fa-clock"></i>
                                    <span>1 час</span>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('puu')">
                                Начать курс
                            </button>
                        </div>
                        
                        <!-- Пароли и аутентификация -->
                        <div class="course-card">
                            <div class="course-icon passwords">
                                <i class="fas fa-key"></i>
                            </div>
                            <h3>Пароли и аутентификация</h3>
                            <p>Создание надежных паролей, двухфакторная аутентификация, менеджеры паролей. 5 уроков.</p>
                            <div class="course-meta">
                                <div class="course-meta-item">
                                    <i class="fas fa-book"></i>
                                    <span>5 уроков</span>
                                </div>
                                <div class="course-meta-item">
                                    <i class="fas fa-clock"></i>
                                    <span>50 минут</span>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('passwords')">
                                Начать курс
                            </button>
                        </div>
                        
                        <!-- Соцсети и мессенджеры -->
                        <div class="course-card">
                            <div class="course-icon social">
                                <i class="fas fa-users"></i>
                            </div>
                            <h3>Безопасность в соцсетях</h3>
                            <p>Защита аккаунтов в соцсетях, приватность, фишинг в мессенджерах. 6 уроков.</p>
                            <div class="course-meta">
                                <div class="course-meta-item">
                                    <i class="fas fa-book"></i>
                                    <span>6 уроков</span>
                                </div>
                                <div class="course-meta-item">
                                    <i class="fas fa-clock"></i>
                                    <span>1 час</span>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('social')">
                                Начать курс
                            </button>
                        </div>
                        
                        <!-- Финансовое мошенничество -->
                        <div class="course-card">
                            <div class="course-icon financial">
                                <i class="fas fa-credit-card"></i>
                            </div>
                            <h3>Финансовое мошенничество</h3>
                            <p>Защита банковских карт, онлайн-платежи, мошенничество с инвестициями. 8 уроков.</p>
                            <div class="course-meta">
                                <div class="course-meta-item">
                                    <i class="fas fa-book"></i>
                                    <span>8 уроков</span>
                                </div>
                                <div class="course-meta-item">
                                    <i class="fas fa-clock"></i>
                                    <span>1 час</span>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('financial')">
                                Начать курс
                            </button>
                        </div>
                        
                        <!-- Мобильная безопасность -->
                        <div class="course-card">
                            <div class="course-icon" style="background: linear-gradient(135deg, #7b1fa2, #ba68c8);">
                                <i class="fas fa-mobile-alt"></i>
                            </div>
                            <h3>Мобильная безопасность</h3>
                            <p>Защита смартфонов, безопасность приложений, мобильный банкинг. 7 уроков.</p>
                            <div class="course-meta">
                                <div class="course-meta-item">
                                    <i class="fas fa-book"></i>
                                    <span>7 уроков</span>
                                </div>
                                <div class="course-meta-item">
                                    <i class="fas fa-clock"></i>
                                    <span>1.5 часа</span>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCourse('mobile')">
                                Начать курс
                            </button>
                        </div>
                    </div>
                </div>
                
                <div id="beginner-courses" class="tab-content">
                    <h3>Курсы для начинающих</h3>
                    <p>Начните с основ кибербезопасности. Эти курсы подходят для новичков.</p>
                    <!-- Контент будет загружен динамически -->
                </div>
                
                <div id="advanced-courses" class="tab-content">
                    <h3>Продвинутые курсы</h3>
                    <p>Для тех, кто уже знаком с основами и хочет углубить знания.</p>
                    <!-- Контент будет загружен динамически -->
                </div>
                
                <div id="my-courses" class="tab-content">
                    <h3>Мои курсы</h3>
                    <p id="my-courses-message">Войдите в систему, чтобы увидеть ваши курсы.</p>
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>
        
        <!-- Страница курса Фишинг -->
        <div id="phishing-course" class="page">
            <div class="card">
                <div id="phishingCourseContent">
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>
        
        <!-- Страница курса Телефонное мошенничество -->
        <div id="calls-course" class="page">
            <div class="card">
                <div id="callsCourseContent">
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>
        
        <!-- Страница курса Госуслуги -->
        <div id="gosuslugi-course" class="page">
            <div class="card">
                <div id="gosuslugiCourseContent">
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>
        
        <!-- Страница курса ПУУ схемы -->
        <div id="puu-course" class="page">
            <div class="card">
                <div id="puuCourseContent">
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>

 <!-- Страница курса Безопасность в соцсетях -->
        <div id="social-course" class="page">
    <div class="card">
        <div id="socialCourseContent">
            <!-- Контент будет загружен динамически -->
        </div>
    </div>
</div>        

        <!-- Страница тренажеров -->
        <div id="simulators" class="page">
            <div class="card">
                <div class="course-header">
                    <div class="course-header-icon" style="background: linear-gradient(135deg, var(--accent-color), #26c6da);">
                        <i class="fas fa-gamepad"></i>
                    </div>
                    <div class="course-header-content">
                        <h1>Интерактивные тренажеры</h1>
                        <p>Практикуйтесь в безопасной среде. Симуляторы реальных ситуаций помогут закрепить знания.</p>
                    </div>
                </div>
                
                <div class="simulators-grid">
                    <!-- Тренажер 1 -->
                    <div class="simulator-card">
                        <div class="simulator-header" style="background: linear-gradient(135deg, var(--phishing-color), #ef5350);">
                            <div class="simulator-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <h3>Фишинг-детектив</h3>
                            <div class="simulator-difficulty">Начальный уровень</div>
                        </div>
                        <div class="simulator-body">
                            <p>Определяйте фишинговые письма среди легитимных. Учитесь замечать признаки обмана в электронной почте.</p>
                            <div class="progress-container">
                                <div class="progress-label">
                                    <span>Прогресс</span>
                                    <span id="simulator1-progress">0%</span>
                                </div>
                                <div class="progress-bar">
                                    <div class="progress-fill" id="simulator1-bar" style="width: 0%;"></div>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%;" onclick="startSimulator('phishing-detective')">
                                <i class="fas fa-play icon"></i> Запустить тренажер
                            </button>
                        </div>
                    </div>
                    
                    <!-- Тренажер 2 -->
                    <div class="simulator-card">
                        <div class="simulator-header" style="background: linear-gradient(135deg, var(--calls-color), #ffa726);">
                            <div class="simulator-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <h3>Телефонный симулятор</h3>
                            <div class="simulator-difficulty">Средний уровень</div>
                        </div>
                        <div class="simulator-body">
                            <p>Отрабатывайте правильные реакции на звонки мошенников. Учитесь завершать опасные разговоры.</p>
                            <div class="progress-container">
                                <div class="progress-label">
                                    <span>Прогресс</span>
                                    <span id="simulator2-progress">0%</span>
                                </div>
                                <div class="progress-bar">
                                    <div class="progress-fill" id="simulator2-bar" style="width: 0%;"></div>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%;" onclick="startSimulator('phone-simulator')">
                                <i class="fas fa-play icon"></i> Запустить тренажер
                            </button>
                        </div>
                    </div>
                    
                    <!-- Тренажер 3 -->
                    <div class="simulator-card">
                        <div class="simulator-header" style="background: linear-gradient(135deg, var(--passwords-color), #ab47bc);">
                            <div class="simulator-icon">
                                <i class="fas fa-key"></i>
                            </div>
                            <h3>Конструктор паролей</h3>
                            <div class="simulator-difficulty">Начальный уровень</div>
                        </div>
                        <div class="simulator-body">
                            <p>Создавайте и проверяйте стойкие пароли. Учитесь использовать менеджеры паролей.</p>
                            <div class="progress-container">
                                <div class="progress-label">
                                    <span>Прогресс</span>
                                    <span id="simulator3-progress">0%</span>
                                </div>
                                <div class="progress-bar">
                                    <div class="progress-fill" id="simulator3-bar" style="width: 0%;"></div>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%;" onclick="startSimulator('password-constructor')">
                                <i class="fas fa-play icon"></i> Запустить тренажер
                            </button>
                        </div>
                    </div>
                    
                    <!-- Тренажер 4 -->
                    <div class="simulator-card">
                        <div class="simulator-header" style="background: linear-gradient(135deg, var(--social-color), #29b6f6);">
                            <div class="simulator-icon">
                                <i class="fas fa-shield-alt"></i>
                            </div>
                            <h3>Проверка безопасности</h3>
                            <div class="simulator-difficulty">Средний уровень</div>
                        </div>
                        <div class="simulator-body">
                            <p>Анализируйте настройки безопасности аккаунтов. Учитесь настраивать защиту в соцсетях.</p>
                            <div class="progress-container">
                                <div class="progress-label">
                                    <span>Прогресс</span>
                                    <span id="simulator4-progress">0%</span>
                                </div>
                                <div class="progress-bar">
                                    <div class="progress-fill" id="simulator4-bar" style="width: 0%;"></div>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%;" onclick="startSimulator('security-check')">
                                <i class="fas fa-play icon"></i> Запустить тренажер
                            </button>
                        </div>
                    </div>
                    
                    <!-- Тренажер 5 -->
                    <div class="simulator-card">
                        <div class="simulator-header" style="background: linear-gradient(135deg, var(--gosuslugi-color), #7986cb);">
                            <div class="simulator-icon">
                                <i class="fas fa-passport"></i>
                            </div>
                            <h3>Госуслуги: Проверка сайта</h3>
                            <div class="simulator-difficulty">Средний уровень</div>
                        </div>
                        <div class="simulator-body">
                            <p>Определяйте поддельные сайты Госуслуг. Учитесь проверять легитимность ресурсов.</p>
                            <div class="progress-container">
                                <div class="progress-label">
                                    <span>Прогресс</span>
                                    <span id="simulator5-progress">0%</span>
                                </div>
                                <div class="progress-bar">
                                    <div class="progress-fill" id="simulator5-bar" style="width: 0%;"></div>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%;" onclick="startSimulator('gosuslugi-check')">
                                <i class="fas fa-play icon"></i> Запустить тренажер
                            </button>
                        </div>
                    </div>
                    
                    <!-- Тренажер 6 -->
                    <div class="simulator-card">
                        <div class="simulator-header" style="background: linear-gradient(135deg, var(--puu-color), #66bb6a);">
                            <div class="simulator-icon">
                                <i class="fas fa-laptop-code"></i>
                            </div>
                            <h3>ПУУ: Анализ звонка</h3>
                            <div class="simulator-difficulty">Продвинутый уровень</div>
                        </div>
                        <div class="simulator-body">
                            <p>Анализируйте звонки "техподдержки". Определяйте признаки ПУУ схем.</p>
                            <div class="progress-container">
                                <div class="progress-label">
                                    <span>Прогресс</span>
                                    <span id="simulator6-progress">0%</span>
                                </div>
                                <div class="progress-bar">
                                    <div class="progress-fill" id="simulator6-bar" style="width: 0%;"></div>
                                </div>
                            </div>
                            <button class="btn" style="width: 100%;" onclick="startSimulator('puu-analysis')">
                                <i class="fas fa-play icon"></i> Запустить тренажер
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Страница тестирования -->
        <div id="test" class="page">
            <div class="card">
                <div class="course-header">
                    <div class="course-header-icon" style="background: linear-gradient(135deg, #ffa000, #ffb300);">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <div class="course-header-content">
                        <h1>Финальное тестирование</h1>
                        <p>Пройдите тест, чтобы проверить свои знания и получить сертификат.</p>
                    </div>
                </div>
                
                <div id="testContent">
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>
        
        <!-- Страница профиля -->
        <div id="profile" class="page">
            <div class="card">
                <div id="profileContent">
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>
        
        <!-- Страница активного тренажера -->
        <div id="active-simulator" class="page">
            <div class="card">
                <div id="simulatorContent">
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>
        
        <!-- Страница активного курса -->
        <div id="active-course" class="page">
            <div class="card">
                <div id="courseContent">
                    <!-- Контент будет загружен динамически -->
                </div>
            </div>
        </div>
    </div>
    
    <!-- Футер -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3><i class="fas fa-shield-alt icon"></i> КиберАкадемия</h3>
                <p style="margin-bottom: 20px;">Образовательная платформа по кибербезопасности. Учим защищаться от мошенников в цифровом мире.</p>
                <div style="display: flex; gap: 15px;">
                    <a href="#" style="color: white; font-size: 1.2rem;"><i class="fab fa-vk"></i></a>
                    <a href="#" style="color: white; font-size: 1.2rem;"><i class="fab fa-telegram"></i></a>
                    <a href="#" style="color: white; font-size: 1.2rem;"><i class="fab fa-youtube"></i></a>
                </div>
            </div>
            
            <div class="footer-section">
                <h3>Быстрые ссылки</h3>
                <ul class="footer-links">
                    <li><a href="#" onclick="showPage('home')">Главная</a></li>
                    <li><a href="#" onclick="showPage('courses')">Все курсы</a></li>
                    <li><a href="#" onclick="showPage('simulators')">Тренажеры</a></li>
                    <li><a href="#" onclick="showPage('test')">Тестирование</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Экстренные контакты</h3>
                <ul class="footer-links">
                    <li><i class="fas fa-phone icon"></i> Горячая линия Госуслуг: 8-800-100-70-10</li>
                    <li><i class="fas fa-phone icon"></i> Центробанк (финансовое мошенничество): 8-800-250-40-72</li>
                    <li><i class="fas fa-phone icon"></i> МВД (киберпреступления): 8-800-222-74-47</li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Статистика обучения</h3>
                <p>Пользователей онлайн: <span id="onlineUsers">247</span></p>
                <p>Тренажеров пройдено сегодня: <span id="todaySimulators">134</span></p>
                <p>Сертификатов выдано: <span id="totalCertificates">1,892</span></p>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>© 2026 Академия Кибербезопасности. Учебный проект.</p>
            <p style="margin-top: 10px; font-size: 0.8rem;">Все материалы предоставляются исключительно в образовательных целях</p>
        </div>
    </footer>

    <script>
        // Глобальные переменные
        let currentUser = null;
        let users = JSON.parse(localStorage.getItem('cyberAcademyUsers')) || [];
        let currentPage = 'home';
        let selectedOption = null;
        let testAnswers = [];
        let testCurrentQuestion = 1;
        let courses = {};
        let simulators = {};
        let gosuslugiTestQuestions = [];
        let gosuslugiCurrentQuestion = 0;
 let gosuslugiUserAnswers = [];
let gosuslugiTestStartTime = null;
let gosuslugiTestTimer = null;
let puuTestQuestions = [];
let puuCurrentQuestion = 0;
let puuUserAnswers = [];
let puuTestStartTime = null;
let puuTestTimer = null;
let socialTestQuestions = [];
let socialCurrentQuestion = 0;
let socialUserAnswers = [];
let socialTestStartTime = null;
let socialTestTimer = null;
let finalTestQuestions = [];
let finalCurrentQuestion = 0;
let finalUserAnswers = [];
let finalTestStartTime = null;
let finalTestTimer = null;
// Функция плавной прокрутки вверх
function scrollToTop() {
    window.scrollTo({
        top: 0,
        behavior: 'smooth'
    });
}
        // Инициализация при загрузке
        document.addEventListener('DOMContentLoaded', function() {
            // Проверяем, есть ли сохраненный пользователь
            const savedUser = localStorage.getItem('cyberAcademyCurrentUser');
            if (savedUser) {
                currentUser = JSON.parse(savedUser);
                updateUIForLoggedInUser();
            }
            
            // Инициализация данных курсов и тренажеров
            initCoursesData();
            initSimulatorsData();
            
            // Инициализация кнопки "Наверх"
            initScrollToTop();
            
            // Обновляем статистику каждые 10 секунд (демо)
            setInterval(() => {
                const onlineUsers = document.getElementById('onlineUsers');
                const current = parseInt(onlineUsers.textContent.replace(/,/g, ''));
                onlineUsers.textContent = (current + Math.floor(Math.random() * 3) - 1).toLocaleString();
                
                const todaySimulators = document.getElementById('todaySimulators');
                todaySimulators.textContent = (parseInt(todaySimulators.textContent) + 1).toString();
            }, 10000);
            
            // Инициализация форм
            initForms();
        });
        
        // Инициализация данных курсов
        function initCoursesData() {
            courses = {
    'phishing': {
    title: 'Фишинг: как не попасться на удочку мошенников',
    icon: 'fa-fish',
    color: 'phishing',
    description: 'Узнайте, как распознать поддельные письма и сообщения от мошенников, которые хотят украсть ваши деньги и данные.',
    lessons: [
        { 
            title: 'Что такое фишинг и зачем он нужен мошенникам', 
            duration: '10 мин',
            content: `
                <h3>Простая угроза, от которой страдают тысячи</h3>
                <p><strong>Фишинг</strong> — это когда мошенники притворяются банком, госслужбой или магазином, чтобы выдать себя за честную организацию и украсть ваши деньги или данные.</p>
                
                <div class="simulator" style="margin: 20px 0; background-color: #ffebee; padding: 20px; border-radius: 10px;">
                    <h4>🎯 Цель мошенников проста:</h4>
                    <ul>
                        <li>Узнать данные вашей банковской карты</li>
                        <li>Взять пароли от интернет-банка</li>
                        <li>Заставить вас перевести деньги</li>
                        <li>Установить вирус на телефон или компьютер</li>
                    </ul>
                </div>
                
                <h4>Почему в России это особенно актуально?</h4>
                <ul>
                    <li>Россия — на 3-м месте в мире по количеству фишинговых атак</li>
                    <li>Каждый день создаются сотни поддельных сайтов Сбера, Тинькофф, ВТБ</li>
                    <li>Чаще всего подделывают: Госуслуги, банки, Яндекс, Wildberries</li>
                </ul>
                
                <div class="simulator" style="margin: 20px 0; background-color: #e8f4fd; padding: 20px; border-radius: 10px;">
                    <h4>📱 Самые частые способы обмана в России:</h4>
                    <div class="message-example suspicious">
                        <div class="message-label suspicious">СМС ОТ БАНКА</div>
                        <p>"Сбербанк: Ваша карта заблокирована. Разблокировать: sber-bank-secure.ru"</p>
                    </div>
                    
                    <div class="message-example suspicious" style="margin-top: 15px;">
                        <div class="message-label suspicious">ПИСЬМО НА ПОЧТУ</div>
                        <p>"Госуслуги: Вам пришел налоговый вычет. Получить: gosuslugi-payment.ru"</p>
                    </div>
                    
                    <div class="message-example suspicious" style="margin-top: 15px;">
                        <div class="message-label suspicious">СООБЩЕНИЕ В WHATSAPP</div>
                        <p>"Вы выиграли iPhone в конкурсе от МТС! Забрать: mts-prize-get.com"</p>
                    </div>
                </div>
                
                <div style="background-color: #fff3cd; padding: 15px; border-radius: 8px; margin-top: 20px;">
                    <h5>💡 Запомните главное:</h5>
                    <p><strong>Ни один настоящий банк или госслужба никогда не попросит вас перейти по ссылке и ввести данные карты или пароль!</strong></p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Как отличить поддельное письмо от настоящего', 
            duration: '12 мин',
            content: `
                <h3>3 простых шага, которые спасут ваши деньги</h3>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>🔍 ШАГ 1: Смотрите на адрес отправителя</h4>
                    <p>Мошенники всегда меняют буквы в названиях:</p>
                    
                    <table style="width: 100%; margin-top: 10px; border-collapse: collapse;">
                        <tr style="background-color: #ffebee;">
                            <td style="padding: 10px; border: 1px solid #ccc;"><strong>Поддельный адрес</strong></td>
                            <td style="padding: 10px; border: 1px solid #ccc;"><strong>Настоящий адрес</strong></td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border: 1px solid #ccc;">sber-bank.ru</td>
                            <td style="padding: 10px; border: 1px solid #ccc;">sberbank.ru</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border: 1px solid #ccc;">tinkoff-secure.com</td>
                            <td style="padding: 10px; border: 1px solid #ccc;">tinkoff.ru</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border: 1px solid #ccc;">gosuslugi-pay.info</td>
                            <td style="padding: 10px; border: 1px solid #ccc;">gosuslugi.ru</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border: 1px solid #ccc;">yandex-money.space</td>
                            <td style="padding: 10px; border: 1px solid #ccc;">money.yandex.ru</td>
                        </tr>
                    </table>
                    
                    <p style="margin-top: 15px; color: #d32f2f; font-weight: bold;">⚠️ Если видите дефис или точку перед названием — это мошенники!</p>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>🔍 ШАГ 2: Проверяйте обращение</h4>
                    <div style="display: flex; gap: 20px; margin-top: 15px;">
                        <div style="flex: 1; padding: 15px; background-color: #ffebee; border-radius: 8px;">
                            <h5 style="color: #d32f2f;">Плохо (мошенники)</h5>
                            <p>"Уважаемый клиент!"</p>
                            <p>"Дорогой пользователь!"</p>
                            <p>"Здравствуйте!"</p>
                        </div>
                        <div style="flex: 1; padding: 15px; background-color: #c8e6c9; border-radius: 8px;">
                            <h5 style="color: #388e3c;">Хорошо (настоящее)</h5>
                            <p>"Иван Иванович"</p>
                            <p>"Анна Петровна"</p>
                            <p>С вашим именем и отчеством</p>
                        </div>
                    </div>
                    <p style="margin-top: 15px;"><strong>Настоящие банки и Госуслуги всегда обращаются к вам по имени!</strong></p>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>🔍 ШАГ 3: Обращайте внимание на срочность</h4>
                    <div class="message-example suspicious">
                        <div class="message-label suspicious">ТИПИЧНЫЕ УГРОЗЫ МОШЕННИКОВ</div>
                        <p>"Ваш счет будет заблокирован через 2 часа!"</p>
                        <p>"Налоговая оштрафует вас, если не оплатите сейчас!"</p>
                        <p>"Заберите приз, пока он не достался другому!"</p>
                    </div>
                    <p style="margin-top: 15px; color: #388e3c; font-weight: bold;">✅ Настоящие проблемы решаются спокойно, у вас всегда есть время подумать.</p>
                </div>
               
            `,
            completed: false 
        },
        { 
            title: 'Фишинг в СМС и соцсетях', 
            duration: '11 мин',
            content: `
                <h3>Мошенники не только в почте — они везде</h3>
                
                <h4>📱 СМС-фишинг (смишинг) — самая частая угроза</h4>
                <div class="simulator" style="margin: 20px 0; background-color: #ffebee; padding: 20px; border-radius: 10px;">
                    <h5>🚨 Реальные примеры из России:</h5>
                    
                    <div style="background-color: white; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                        <p><strong>От: 900 (Сбербанк)</strong></p>
                        <p>Ваша карта заблокирована из-за подозрительных операций. Разблокировать: sber-bank-secure.ru</p>
                        <p style="color: #d32f2f; font-size: 14px; margin-top: 5px;">⚠️ Настоящий Сбер никогда не шлет ссылки в СМС!</p>
                    </div>
                    
                    <div style="background-color: white; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                        <p><strong>От: Почта России</strong></p>
                        <p>У вас невостребованная посылка. Оплатите доставку: pochta-russia-pay.com</p>
                        <p style="color: #d32f2f; font-size: 14px; margin-top: 5px;">⚠️ За посылки платят при получении, а не по ссылкам!</p>
                    </div>
                    
                    <div style="background-color: white; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                        <p><strong>От: Такси</strong></p>
                        <p>Вы совершили поездку 15.03.2024. Оплатить: yandex-taxi-payment.ru</p>
                        <p style="color: #d32f2f; font-size: 14px; margin-top: 5px;">⚠️ Такси списывают деньги автоматически!</p>
                    </div>
                </div>
                
                <h4>📱 Фишинг в WhatsApp и Telegram</h4>
                <div style="background-color: #fff3cd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h5>Как работают мошенники:</h5>
                    <ol>
                        <li>Пишут: "Мама, это я, поменял номер"</li>
                        <li>Через пару дней: "Срочно нужны деньги на лечение/штраф"</li>
                        <li>Просят перевести на карту "друга" или "адвоката"</li>
                    </ol>
                    
                    <div style="margin-top: 15px; padding: 25px; background-color: #ffebee; border-radius: 8px;">
                        <p><strong>Что делать, если получили такое сообщение:</strong></p>
                        <ul>
                            <li>Позвоните родственнику на старый номер</li>
                            <li>Задайте вопрос, на который знаете ответ (имя домашнего питомца)</li>
                            <li>Не переводите деньги сразу</li>
                        </ul>
                    </div>
                </div>
                
                <h4>📱 Фишинг во ВКонтакте и Одноклассниках</h4>
                <div style="background-color: #e8f4fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h5>Частые схемы:</h5>
                    
                    <div style="display: flex; gap: 15px; margin-top: 15px;">
                        <div style="flex: 1; padding: 15px; background-color: white; border-radius: 8px; border: 1px solid #ddd;">
                            <p><strong>"Посмотри, что о тебе пишут!"</strong></p>
                            <p>vk.com/check-profile-123</p>
                            <p style="color: #d32f2f; font-size: 12px;">→ Воруют доступ к странице</p>
                        </div>
                        
                        <div style="flex: 1; padding: 15px; background-color: white; border-radius: 8px; border: 1px solid #ddd;">
                            <p><strong>"Вы выиграли iPhone!"</strong></p>
                            <p>promo-vk-apple.ru</p>
                            <p style="color: #d32f2f; font-size: 12px;">→ Просят оплатить "доставку"</p>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #c8e6c9; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h5>✅ Правило на все случаи:</h5>
                    <p><strong>Не переходите по ссылкам в сообщениях от незнакомцев и не вводите пароли где попало!</strong></p>
                    <p style="margin-top: 10px;">Если нужно войти в банк — открывайте приложение самостоятельно.</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Поддельные сайты банков и магазинов', 
            duration: '12 мин',
            content: `
                <h3>Как мошенники копируют сайты и как это распознать</h3>
                
                <h4>🔐 Самое важное — адресная строка браузера</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <p><strong>Как работают мошенники:</strong> Они создают сайты с похожими названиями, меняя всего 1-2 буквы.</p>
                    
                    <div style="margin: 15px 0;">
                        <p><strong>Настоящие сайты банков (всегда запоминайте их!):</strong></p>
                        <div style="background-color: #c8e6c9; padding: 10px 15px; border-radius: 5px; margin: 8px 0;">
                            <code>sberbank.ru</code> — официальный Сбербанк
                        </div>
                        <div style="background-color: #c8e6c9; padding: 10px 15px; border-radius: 5px; margin: 8px 0;">
                            <code>tinkoff.ru</code> — официальный Тинькофф
                        </div>
                        <div style="background-color: #c8e6c9; padding: 10px 15px; border-radius: 5px; margin: 8px 0;">
                            <code>vtb.ru</code> — официальный ВТБ
                        </div>
                        <div style="background-color: #c8e6c9; padding: 10px 15px; border-radius: 5px; margin: 8px 0;">
                            <code>alfabank.ru</code> — официальный Альфа-Банк
                        </div>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <p><strong>Поддельные сайты (обращайте внимание!):</strong></p>
                        <div style="background-color: #ffcdd2; padding: 10px 15px; border-radius: 5px; margin: 8px 0;">
                            <code>sber-bank.ru</code> <span style="color: #d32f2f;">— дефис в середине!</span>
                        </div>
                        <div style="background-color: #ffcdd2; padding: 10px 15px; border-radius: 5px; margin: 8px 0;">
                            <code>tinkoff.bank-secure.com</code> <span style="color: #d32f2f;">— точка после названия!</span>
                        </div>
                        <div style="background-color: #ffcdd2; padding: 10px 15px; border-radius: 5px; margin: 8px 0;">
                            <code>vtb-online-payment.ru</code> <span style="color: #d32f2f;">— добавлены лишние слова!</span>
                        </div>
                        <div style="background-color: #ffcdd2; padding: 10px 15px; border-radius: 5px; margin: 8px 0;">
                            <code>alfa-bank.secure.pro</code> <span style="color: #d32f2f;">— домен .pro вместо .ru!</span>
                        </div>
                    </div>
                    
                    <div style="margin-top: 20px; padding: 15px; background-color: #fff3cd; border-radius: 8px;">
                        <h5>💡 Простое правило:</h5>
                        <p><strong>Настоящий сайт банка: короткое название.ру</strong></p>
                        <p><strong>Поддельный сайт: название-слова-ещеслова.домен</strong></p>
                    </div>
                </div>
                
                <h4>🔒 Всегда должен быть зеленый замочек</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <div style="display: flex; align-items: center; gap: 20px; margin-bottom: 15px;">
                        <div style="font-size: 48px;">🔒</div>
                        <div>
                            <p><strong>Безопасное соединение:</strong></p>
                            <p>Начинается с <code>https://</code></p>
                            <p style="color: #388e3c; font-weight: bold;">Есть значок замка в адресной строке</p>
                        </div>
                    </div>
                    
                    <div style="display: flex; align-items: center; gap: 20px; margin-top: 15px;">
                        <div style="font-size: 48px;">⚠️</div>
                        <div>
                            <p><strong>Опасное соединение:</strong></p>
                            <p>Начинается с <code>http://</code> (без буквы s)</p>
                            <p style="color: #d32f2f; font-weight: bold;">Нет замка или есть восклицательный знак</p>
                        </div>
                    </div>
                    
                    <div style="margin-top: 20px; padding: 15px; background-color: #ffebee; border-radius: 8px;">
                        <p><strong>ВАЖНО:</strong> Даже если есть https:// и замок — это не гарантия, что сайт настоящий!</p>
                        <p>Мошенники тоже могут купить SSL-сертификат. Поэтому всегда проверяйте название сайта!</p>
                    </div>
                </div>
                
                <h4>🎭 Как подделывают сайты магазинов (Wildberries, Ozon)</h4>
                <div style="background-color: #fff3cd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <p><strong>Частые схемы обмана:</strong></p>
                    
                    <div style="margin: 15px 0;">
                        <p><strong>1. Поддельные акционные страницы:</strong></p>
                        <div style="padding: 10px 15px; background-color: white; border-radius: 5px; margin: 8px 0;">
                            <p><code>wildberries-sale.ru</code> — обещает скидки 90%</p>
                            <p style="color: #d32f2f; font-size: 14px;">Настоящий Wildberries: wildberries.ru</p>
                        </div>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <p><strong>2. Фейковые страницы оплаты:</strong></p>
                        <div style="padding: 10px 15px; background-color: white; border-radius: 5px; margin: 8px 0;">
                            <p><code>ozon-payment.ru</code> — просит "подтвердить оплату"</p>
                            <p style="color: #d32f2f; font-size: 14px;">Настоящий Ozon: ozon.ru</p>
                        </div>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <p><strong>3. Поддельные страницы возврата:</strong></p>
                        <div style="padding: 10px 15px; background-color: white; border-radius: 5px; margin: 8px 0;">
                            <p><code>wb-return-money.com</code> — предлагает "вернуть переплату"</p>
                            <p style="color: #d32f2f; font-size: 14px;">Все возвраты только через личный кабинет!</p>
                        </div>
                    </div>
                </div>
                
                <h4>📱 Особенности подделок на телефоне</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <p><strong>На телефоне сложнее увидеть адресную строку. Что делать:</strong></p>
                    
                    <div style="margin: 15px 0;">
                        <p><strong>В браузере на телефоне:</strong></p>
                        <ul>
                            <li>Нажмите на адресную строку, чтобы увидеть полный адрес</li>
                            <li>Проверьте, нет ли опечаток в названии</li>
                            <li>Ищите значок замка 🔒</li>
                        </ul>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <p><strong>Лучший способ на телефоне:</strong></p>
                        <ul>
                            <li>Используйте официальные приложения банков</li>
                            <li>Скачивайте их только из App Store или Google Play</li>
                            <li>Не заходите в банк по ссылкам из СМС или почты</li>
                        </ul>
                    </div>
                </div>
                
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4>🚨 3 главных признака поддельного сайта:</h4>
                    
                    <div style="display: flex; flex-direction: column; gap: 15px; margin-top: 15px;">
                        <div style="display: flex; align-items: flex-start; gap: 15px;">
                            <div style="font-size: 24px; color: #d32f2f;">1️⃣</div>
                            <div>
                                <p><strong>Длинное название с дефисами</strong></p>
                                <p>Настоящий: <code>sberbank.ru</code></p>
                                <p>Подделка: <code>sber-bank-secure-payment.ru</code></p>
                            </div>
                        </div>
                        
                        <div style="display: flex; align-items: flex-start; gap: 15px;">
                            <div style="font-size: 24px; color: #d32f2f;">2️⃣</div>
                            <div>
                                <p><strong>Просит ввести данные на главной странице</strong></p>
                                <p>Настоящий банк сначала показывает информацию</p>
                                <p>Мошенники сразу ставят форму для ввода карты</p>
                            </div>
                        </div>
                        
                        <div style="display: flex; align-items: flex-start; gap: 15px;">
                            <div style="font-size: 24px; color: #d32f2f;">3️⃣</div>
                            <div>
                                <p><strong>Нет контактов и информации о компании</strong></p>
                                <p>Настоящие сайты имеют "О банке", "Контакты", "Реквизиты"</p>
                                <p>Подделки — только форма для ввода данных</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #c8e6c9; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h5>💡 Простой алгоритм проверки сайта:</h5>
                    <ol>
                        <li>Посмотрите на адресную строку — короткое ли название?</li>
                        <li>Есть ли https:// и значок замка?</li>
                        <li>Сайт просит сразу ввести данные карты? Это плохо!</li>
                        <li>Если сомневаетесь — закройте вкладку и войдите через приложение</li>
                    </ol>
                    <p style="margin-top: 15px; font-weight: bold;">Запомните: настоящий банк никогда не попросит вас ввести все данные карты на одной странице!</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Что делать, если получили фишинговое сообщение', 
            duration: '12 мин',
            content: `
                <h3>Правильные действия могут спасти не только вас</h3>
                
                <div style="background-color: #fff3cd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>🚨 ШАГ 1: Не паникуйте и ничего не нажимайте</h4>
                    <div style="display: flex; align-items: center; gap: 15px; margin-top: 10px;">
                        <div style="font-size: 48px;">❌</div>
                        <div>
                            <p><strong>Не делайте:</strong></p>
                            <ul>
                                <li>Не переходите по ссылке</li>
                                <li>Не звоните по указанному номеру</li>
                                <li>Не скачивайте вложения</li>
                                <li>Не вводите никакие данные</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>✅ ШАГ 2: Проверьте информацию правильно</h4>
                    
                    <div style="margin-top: 15px;">
                        <p><strong>Если письмо якобы от банка:</strong></p>
                        <div style="padding: 15px; background-color: white; border-radius: 8px; margin: 10px 0;">
                            <p>1. Возьмите свою банковскую карту</p>
                            <p>2. Найдите номер на обратной стороне</p>
                            <p>3. Позвоните по этому номеру</p>
                            <p>4. Спросите: "Были ли проблемы с моим счетом?"</p>
                        </div>
                    </div>
                    
                    <div style="margin-top: 15px;">
                        <p><strong>Если письмо якобы от Госуслуг или налоговой:</strong></p>
                        <div style="padding: 15px; background-color: white; border-radius: 8px; margin: 10px 0;">
                            <p>1. Откройте приложение "Госуслуги"</p>
                            <p>2. Или зайдите на gosuslugi.ru</p>
                            <p>3. Проверьте свой кабинет</p>
                            <p>4. Все официальные уведомления будут там</p>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>🛡️ ШАГ 3: Сообщите о мошенниках</h4>
                    <p>Помогите другим не попасться на ту же удочку:</p>
                    
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-top: 15px;">
                        <div style="padding: 15px; background-color: white; border-radius: 8px; text-align: center;">
                            <div style="font-size: 24px; color: #1976d2;">📧</div>
                            <p><strong>Фишинг в почте</strong></p>
                            <p style="font-size: 14px;">Отправьте письмо как спам</p>
                            <p style="font-size: 12px; color: #666;">В Gmail, Яндекс.Почте, Mail.ru</p>
                        </div>
                        
                        <div style="padding: 15px; background-color: white; border-radius: 8px; text-align: center;">
                            <div style="font-size: 24px; color: #d32f2f;">📱</div>
                            <p><strong>Фишинг в СМС</strong></p>
                            <p style="font-size: 14px;">Сообщите оператору</p>
                            <p style="font-size: 12px; color: #666;">МТС: 1111, Билайн: 0611, Теле2: 611</p>
                        </div>
                    </div>
                    
                    <div style="margin-top: 15px; padding: 15px; background-color: #ffebee; border-radius: 8px;">
                        <p><strong>Официальные ресурсы для жалоб:</strong></p>
                        <ul>
                            <li>Госуслуги: 8-800-100-70-10</li>
                            <li>Банк России: 8-800-250-40-72</li>
                            <li>Сайт МВД: мвд.рф (раздел "Прием обращений")</li>
                        </ul>
                    </div>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #ffebee; padding: 20px; border-radius: 10px;">
                    <h4>🚨 ЧТО ДЕЛАТЬ, ЕСЛИ ВЫ УЖЕ ВВЕЛИ ДАННЫЕ?</h4>
                    
                    <div style="padding: 15px; background-color: white; border-radius: 8px; margin: 15px 0;">
                        <p><strong>СРОЧНЫЕ ДЕЙСТВИЯ:</strong></p>
                        <ol>
                            <li><span style="color: #d32f2f; font-weight: bold;">Немедленно позвоните в банк</span> — заблокируйте карту</li>
                            <li>Если ввели пароль от почты — смените его с другого устройства</li>
                            <li>Если скачали файл — отключите интернет и проверьте антивирусом</li>
                            <li>Предупредите друзей — мошенники могут писать от вашего имени</li>
                        </ol>
                    </div>
                    
                    <div style="margin-top: 15px;">
                        <p><strong>Телефоны экстренной блокировки:</strong></p>
                        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 10px;">
                            <div style="padding: 10px; background-color: #f5f5f5; border-radius: 5px; text-align: center;">
                                <p><strong>Сбербанк</strong></p>
                                <p style="color: #1976d2; font-weight: bold;">900</p>
                            </div>
                            <div style="padding: 10px; background-color: #f5f5f5; border-radius: 5px; text-align: center;">
                                <p><strong>Тинькофф</strong></p>
                                <p style="color: #1976d2; font-weight: bold;">8-800-555-77-78</p>
                            </div>
                            <div style="padding: 10px; background-color: #f5f5f5; border-radius: 5px; text-align: center;">
                                <p><strong>ВТБ</strong></p>
                                <p style="color: #1976d2; font-weight: bold;">8-800-100-24-24</p>
                            </div>
                            <div style="padding: 10px; background-color: #f5f5f5; border-radius: 5px; text-align: center;">
                                <p><strong>Альфа-Банк</strong></p>
                                <p style="color: #1976d2; font-weight: bold;">8-800-200-00-00</p>
                            </div>
                        </div>
                    </div>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Простая защита от фишинга', 
            duration: '10 мин',
            content: `
                <h3>5 простых правил, которые защитят вас на 99%</h3>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>✅ ПРАВИЛО 1: Установите официальные приложения</h4>
                    <div style="display: flex; align-items: center; gap: 15px; margin-top: 10px;">
                        <div style="font-size: 36px;">📱</div>
                        <div>
                            <p><strong>Скачайте только из официальных магазинов:</strong></p>
                            <ul>
                                <li>App Store (для iPhone)</li>
                                <li>Google Play (для Android)</li>
                                <li>Проверяйте разработчика: "Сбербанк России", "ВТБ"</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>✅ ПРАВИЛО 2: Включите СМС-уведомления от банка</h4>
                    <div style="display: flex; align-items: center; gap: 15px; margin-top: 10px;">
                        <div style="font-size: 36px;">💳</div>
                        <div>
                            <p><strong>Что это дает:</strong></p>
                            <ul>
                                <li>Вы сразу увидите, если с карты списали деньги</li>
                                <li>Можно быстро заблокировать карту</li>
                                <li>Это бесплатно во всех банках</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>✅ ПРАВИЛО 3: Научите родственников</h4>
                    <div style="display: flex; align-items: center; gap: 15px; margin-top: 10px;">
                        <div style="font-size: 36px;">👵</div>
                        <div>
                            <p><strong>Особенно важно для пожилых:</strong></p>
                            <ul>
                                <li>Объясните, что банки не звонят сами</li>
                                <li>Скажите: "Прежде чем переводить деньги — позвони мне"</li>
                                <li>Помогите установить официальные приложения</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>✅ ПРАВИЛО 4: Не храните все деньги на одной карте</h4>
                    <div style="display: flex; align-items: center; gap: 15px; margin-top: 10px;">
                        <div style="font-size: 36px;">💰</div>
                        <div>
                            <p><strong>Простая стратегия:</strong></p>
                            <ul>
                                <li>Основная карта — для накоплений (мало используете)</li>
                                <li>Вторая карта — для ежедневных покупок</li>
                                <li>На карте для покупок держите небольшую сумму</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4>✅ ПРАВИЛО 5: Будьте осторожны в публичных Wi-Fi</h4>
                    <div style="display: flex; align-items: center; gap: 15px; margin-top: 10px;">
                        <div style="font-size: 36px;">📶</div>
                        <div>
                            <p><strong>В кафе, аэропортах, торговых центрах:</strong></p>
                            <ul>
                                <li>Не заходите в интернет-банк</li>
                                <li>Не вводите данные карт</li>
                                <li>Используйте мобильный интернет для важных операций</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #e3f2fd; padding: 20px; border-radius: 10px;">
                    <h4>📋 Чек-лист безопасности (распечатайте!)</h4>
                    
                    <div style="padding: 15px; background-color: white; border-radius: 8px; margin: 15px 0;">
                        <p><strong>Что я уже сделал для защиты:</strong></p>
                        
                        <div style="margin-top: 10px;">
                            <label style="display: block; margin: 5px 0;">
                                <input type="checkbox"> Установил официальное приложение банка
                            </label>
                            <label style="display: block; margin: 5px 0;">
                                <input type="checkbox"> Включил СМС-уведомления о списаниях
                            </label>
                            <label style="display: block; margin: 5px 0;">
                                <input type="checkbox"> Научил родителей не переводить деньги по телефону
                            </label>
                            <label style="display: block; margin: 5px 0;">
                                <input type="checkbox"> Запомнил номер экстренной блокировки карты
                            </label>
                            <label style="display: block; margin: 5px 0;">
                                <input type="checkbox"> Знаю, что настоящие банки не шлют ссылки в СМС
                            </label>
                        </div>
                    </div>
                    
                    <div style="text-align: center; margin-top: 15px;">
                        <button onclick="printChecklist()" style="background-color: #1976d2; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">🖨️ Распечатать чек-лист</button>
                    </div>
                </div>
                
                <div style="background-color: #c8e6c9; padding: 20px; border-radius: 10px; margin-top: 20px; text-align: center;">
                    <h4>🎉 Поздравляем! Вы прошли курс!</h4>
                    <p>Теперь вы знаете больше о фишинге, чем 90% россиян.</p>
                    <p style="margin-top: 10px; font-weight: bold;">Главное помните: если сомневаетесь — не нажимайте, не вводите, звоните в банк!</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Итоговый тест', 
            duration: '15 мин',
            content: `
                <h3>Пройдите тест и получите сертификат</h3>
                <p>Ответьте на 10 простых вопросов, чтобы проверить, как хорошо вы усвоили материал.</p>
                
                <div style="text-align: center; margin: 30px 0;">
                    <button class="btn btn-large btn-success" onclick="startPhishingTest()" style="background-color: #4caf50; color: white; border: none; padding: 15px 30px; font-size: 18px; border-radius: 8px; cursor: pointer;">
                        <i class="fas fa-play icon"></i> Начать тест (10 вопросов)
                    </button>
                </div>
                
                <div style="background-color: #fff3cd; padding: 20px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Что вы узнали в этом курсе:</h4>
                    <ul>
                        <li>Как мошенники пытаются украсть ваши деньги</li>
                        <li>Как отличить поддельное письмо от настоящего</li>
                        <li>Что делать с фишинговыми СМС и сообщениями</li>
                        <li>Как проверить, настоящий ли сайт банка</li>
                        <li>Простые правила защиты для всей семьи</li>
                    </ul>
                </div>
            `,
            completed: false 
        }
        ],
        totalLessons: 7,
        totalDuration: '2.5 часа'
    },
            
'calls': {
    title: 'Телефонное мошенничество',
    icon: 'fa-phone-alt',
    color: 'calls',
    description: 'Научитесь распознавать и противостоять телефонным мошенникам, защитите себя и своих близких.',
    lessons: [
        { 
            title: 'Основы телефонного мошенничества', 
            duration: '12 мин',
            content: `
                <h3>Что такое телефонное мошенничество?</h3>
                <p><strong>Телефонное мошенничество (вишинг)</strong> — это вид мошенничества, при котором злоумышленники звонят по телефону, выдавая себя за представителей банков, государственных органов, служб безопасности или технической поддержки, с целью получения конфиденциальной информации или денежных средств.</p>
                
                <h4>Цели телефонных мошенников:</h4>
                <ul>
                    <li>Получение данных банковских карт</li>
                    <li>Кража кодов из SMS-сообщений</li>
                    <li>Установка вредоносного ПО на устройство</li>
                    <li>Перевод денег под различными предлогами</li>
                    <li>Сбор персональных данных</li>
                </ul>
                
                <h4>Как работают мошенники?</h4>
                <p>Мошенники используют специальное программное обеспечение, которое позволяет:</p>
                <ul>
                    <li>Подменять номер телефона (спуфинг)</li>
                    <li>Автоматически обзванивать тысячи номеров</li>
                    <li>Записывать разговоры для анализа</li>
                    <li>Создавать базы данных потенциальных жертв</li>
                </ul>
                
                <div class="simulator" style="margin: 20px 0; background-color: #e8f4fd; padding: 20px; border-radius: 10px;">
                    <h4>Пример реального звонка:</h4>
                    <div class="message-example suspicious">
                        <div class="message-label suspicious">ТИПИЧНЫЙ ЗВОНОК МОШЕННИКА</div>
                        <p><strong>Звонящий:</strong> "Здравствуйте, это служба безопасности банка. По вашей карте обнаружена подозрительная операция. Для предотвращения блокировки назовите последние 4 цифры карты и код из SMS, который мы вам отправили."</p>
                    </div>
                    <p style="margin-top: 15px; color: #d32f2f; font-weight: bold;">⚠️ Настоящие банки НИКОГДА не просят называть коды из SMS!</p>
                </div>
                
                <h4>Статистика телефонного мошенничества:</h4>
                <ul>
                    <li>Более 70% всех мошеннических звонков происходят с подменённых номеров</li>
                    <li>Средний ущерб от одного успешного звонка — 15-50 тысяч рублей</li>
                    <li>Пик активности мошенников — будние дни с 10:00 до 18:00</li>
                    <li>Чаще всего целью становятся люди старше 45 лет</li>
                </ul>
            `,
            completed: false 
        },
        { 
            title: 'Распространенные схемы обмана', 
            duration: '15 мин',
            content: `
                <h3>Основные схемы телефонного мошенничества</h3>
                <p>Мошенники постоянно придумывают новые схемы, но большинство из них можно отнести к нескольким основным категориям.</p>
                
                <h4>1. Звонки от "банка" или "службы безопасности"</h4>
                <div class="message-example suspicious">
                    <div class="message-label suspicious">СХЕМА №1</div>
                    <p><strong>Сценарий:</strong> "Вам звонят из службы безопасности банка. Обнаружена попытка несанкционированного списания средств. Для защиты счета нужно подтвердить операцию кодом из SMS или перевести деньги на 'безопасный счет'.</p>
                    <p><strong>Цель:</strong> Получить доступ к вашим средствам через коды подтверждения или прямой перевод.</p>
                </div>
                
                <h4>2. Звонки от "родственников в беде"</h4>
                <div class="message-example suspicious">
                    <div class="message-label suspicious">СХЕМА №2</div>
                    <p><strong>Сценарий:</strong> "Бабушка, это я, ваш внук! Я попал в аварию (или ДТП, милицию). Мне срочно нужны деньги на штраф/лечение/залог. Деньги нужно перевести прямо сейчас!"</p>
                    <p><strong>Цель:</strong> Эмоциональное давление и срочный перевод денег под видом помощи родственнику.</p>
                </div>
                
                <h4>3. Звонки от "оператора связи"</h4>
                <div class="message-example suspicious">
                    <div class="message-label suspicious">СХЕМА №3</div>
                    <p><strong>Сценарий:</strong> "Это служба технической поддержки МТС/Билайн/Теле2. Ваш номер будут отключать за долги/нарушения. Чтобы избежать отключения, нужно пополнить счет на указанный номер или оплатить штраф."</p>
                    <p><strong>Цель:</strong> Получение денег под предлогом сохранения номера телефона.</p>
                </div>
                
                <h4>4. Звонки от "государственных органов"</h4>
                <div class="message-example suspicious">
                    <div class="message-label suspicious">СХЕМА №4</div>
                    <p><strong>Сценарий:</strong> "Это налоговая служба/пенсионный фонд/суд. За вами числится задолженность/неуплаченный штраф/недоплата налогов. Чтобы избежать суда/ареста счетов, нужно срочно оплатить."</p>
                    <p><strong>Цель:</strong> Запугать и заставить перевести деньги под угрозой юридических последствий.</p>
                </div>
                
                <h4>5. Технический фишинг (ПУУ-схемы)</h4>
                <div class="message-example suspicious">
                    <div class="message-label suspicious">СХЕМА №5</div>
                    <p><strong>Сценарий:</strong> "Это служба безопасности Microsoft/Windows/антивируса. На вашем компьютере обнаружены вирусы/взлом/проблемы. Для устранения нужно установить программу удаленного доступа."</p>
                    <p><strong>Цель:</strong> Получить удаленный доступ к компьютеру и данным, включая банковскую информацию.</p>
                </div>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Важно знать:</h4>
                    <p>Мошенники часто комбинируют несколько схем в одном звонке. Они могут начать как "техподдержка", а закончить как "служба безопасности банка".</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Техники убеждения и манипуляции', 
            duration: '14 мин',
            content: `
                <h3>Психологические приемы телефонных мошенников</h3>
                <p>Мошенники используют продвинутые психологические техники, чтобы обойти вашу осторожность. Знание этих приемов поможет распознать манипуляцию.</p>
                
                <h4>1. Создание искусственной срочности</h4>
                <div style="background-color: #ffebee; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                    <p><strong>Как звучит:</strong> "Вам нужно действовать прямо сейчас! У вас есть только 10 минут, иначе счет будет заблокирован/деньги спишут/родственника арестуют."</p>
                    <p><strong>Цель:</strong> Не дать вам время подумать, проконсультироваться или проверить информацию.</p>
                </div>
                
                <h4>2. Использование авторитета и официальности</h4>
                <div style="background-color: #ffebee; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                    <p><strong>Как звучит:</strong> "Говорит старший следователь Иванов из главного управления МВД", "Начальник отдела безопасности Сбербанка Петров".</p>
                    <p><strong>Цель:</strong> Вызвать доверие через имитацию официального статуса.</p>
                </div>
                
                <h4>3. Эмоциональное давление</h4>
                <div style="background-color: #ffebee; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                    <p><strong>Как звучит:</strong> "Ваш сын сейчас в камере, он плачет, ему страшно", "Вы хотите потерять все свои сбережения?", "Вы не беспокоитесь о безопасности своей семьи?"</p>
                    <p><strong>Цель:</strong> Вызвать сильные эмоции (страх, тревогу, чувство вины), которые затмевают рациональное мышление.</p>
                </div>
                
                <h4>4. Техника "нога в дверях"</h4>
                <div style="background-color: #ffebee; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                    <p><strong>Как работает:</strong> Сначала просят небольшую уступку ("просто назовите первые 2 цифры карты"), затем постепенно увеличивают запросы.</p>
                    <p><strong>Цель:</strong> Получить согласие на мелкую просьбу, чтобы затем получить согласие на крупную.</p>
                </div>
                
                <h4>5. Использование реальной информации</h4>
                <div style="background-color: #ffebee; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                    <p><strong>Как работает:</strong> Мошенник называет ваше имя, адрес, данные о недавних покупках (купленных в утечках данных).</p>
                    <p><strong>Цель:</strong> Создать иллюзию, что звонящий действительно имеет доступ к вашей информации и является законным представителем.</p>
                </div>
                
                <h4>6. Передача ответственности</h4>
                <div style="background-color: #ffebee; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                    <p><strong>Как звучит:</strong> "Я уже все для вас сделал, подготовил документы, осталось только ваше подтверждение", "Если вы не сделаете это сейчас, я не смогу вам помочь".</p>
                    <p><strong>Цель:</strong> Создать чувство вины и обязательства перед "помогающим" мошенником.</p>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #e8f4fd; padding: 20px; border-radius: 10px;">
                    <h4>Как распознать манипуляцию:</h4>
                    <p><strong>Если в разговоре присутствуют:</strong></p>
                    <ul>
                        <li>Требование немедленных действий</li>
                        <li>Угрозы негативных последствий при отказе</li>
                        <li>Чрезмерная эмоциональность</li>
                        <li>Отказ предоставить возможность перезвонить или проверить информацию</li>
                        <li>Просьба не рассказывать о звонке никому</li>
                    </ul>
                    <p style="color: #d32f2f; font-weight: bold; margin-top: 10px;">Это почти наверняка мошенник!</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Как правильно реагировать на подозрительные звонки', 
            duration: '16 мин',
            content: `
                <h3>Алгоритм действий при подозрительном звонке</h3>
                <p>Знание правильной последовательности действий поможет защитить себя и своих близких от телефонных мошенников.</p>
                
                <h4>Шаг 1: Сохраняйте спокойствие</h4>
                <div style="background-color: #e8f5e9; padding: 15px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #388e3c;">
                    <p>Не поддавайтесь панике, даже если звонящий создает ощущение чрезвычайной ситуации. Помните: <strong>настоящие проблемы никогда не решаются в режиме "прямо сейчас по телефону".</strong></p>
                </div>
                
                <h4>Шаг 2: Не подтверждайте никакую информацию</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #388e3c;">
                    <p>Никогда не называйте:</p>
                    <ul>
                        <li>Данные банковских карт (номер, CVV, срок действия)</li>
                        <li>Коды из SMS-сообщений</li>
                        <li>Пароли от онлайн-банков и личных кабинетов</li>
                        <li>Паспортные данные</li>
                        <li>Информацию о родственниках</li>
                    </ul>
                </div>
                
                <h4>Шаг 3: Задайте контрольные вопросы</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #388e3c;">
                    <p><strong>Примеры вопросов:</strong></p>
                    <ul>
                        <li>"Назовите полное название организации, которую вы представляете"</li>
                        <li>"Какой у вас номер служебного удостоверения?"</li>
                        <li>"Дайте мне номер обращения или идентификатор дела"</li>
                        <li>"Почему вы звоните с мобильного номера, а не со служебного?"</li>
                        <li>"Могу я перезвонить вам на официальный номер организации?"</li>
                    </ul>
                    <p style="margin-top: 10px;"><strong>Мошенники обычно не могут ответить на эти вопросы или начинают злиться.</strong></p>
                </div>
                
                <h4>Шаг 4: Прервите разговор правильно</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #388e3c;">
                    <p><strong>Что говорить:</strong></p>
                    <ul>
                        <li>"Я перезвоню в вашу организацию сам по официальному номеру"</li>
                        <li>"Я сейчас занят, перезвоню позже"</li>
                        <li>"Я проверю эту информацию и свяжусь с вами"</li>
                        <li>"Прошу предоставить информацию в письменном виде"</li>
                    </ul>
                    <p style="margin-top: 10px; color: #388e3c; font-weight: bold;">Не нужно грубить или спорить — просто вежливо завершите разговор.</p>
                </div>
                
                <h4>Шаг 5: Проверьте информацию</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #388e3c;">
                    <p><strong>Как проверить:</strong></p>
                    <ul>
                        <li>Позвоните в банк по номеру с обратной стороны карты</li>
                        <li>Обратитесь в отделение банка лично</li>
                        <li>Проверьте информацию в официальном приложении банка</li>
                        <li>Свяжитесь с родственниками, о которых шла речь</li>
                        <li>Обратитесь в официальные органы по их публичным номерам</li>
                    </ul>
                </div>
                
                <h4>Шаг 6: Заблокируйте мошенника</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #388e3c;">
                    <p><strong>Что сделать после звонка:</strong></p>
                    <ul>
                        <li>Добавьте номер в черный список</li>
                        <li>Сообщите о звонке в банк (если мошенник представлялся банком)</li>
                        <li>Подайте заявление в полицию через сайт МВД</li>
                        <li>Сообщите о мошенническом номере на горячую линию Госуслуг: 8-800-100-70-10</li>
                    </ul>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                    <h4><i class="fas fa-exclamation-triangle icon" style="color: #ff9800;"></i> Экстренные ситуации:</h4>
                    <p><strong>Если вы уже сообщили мошенникам информацию:</strong></p>
                    <ol>
                        <li>Немедленно позвоните в банк и заблокируйте карту</li>
                        <li>Смените пароли от онлайн-банков и личных кабинетов</li>
                        <li>Обратитесь в полицию с заявлением о мошенничестве</li>
                        <li>Сообщите об этом в службу безопасности банка</li>
                    </ol>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Профилактика и защита', 
            duration: '18 мин',
            content: `
                <h3>Как предотвратить телефонное мошенничество</h3>
                <p>Лучшая защита — это профилактика. Вот что вы можете сделать, чтобы минимизировать риск стать жертвой телефонных мошенников.</p>
                
                <h4>1. Настройте защиту SIM-карты</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #1976d2;">
                    <p><strong>Что сделать:</strong></p>
                    <ul>
                        <li>Включите PIN-код на SIM-карте</li>
                        <li>Установите PUK-код (можно получить у оператора)</li>
                        <li>Подключите услугу "Защита от подмены номера" у вашего оператора</li>
                        <li>Регулярно проверяйте активные услуги в личном кабинете оператора</li>
                    </ul>
                </div>
                
                <h4>2. Используйте специальные приложения</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #1976d2;">
                    <p><strong>Полезные приложения:</strong></p>
                    <ul>
                        <li><strong>Антиспам приложения</strong> (Яндекс.Телефон, "Кто звонит?", Hiya) — определяют мошеннические номера</li>
                        <li><strong>Приложения банков</strong> — включите push-уведомления обо всех операциях</li>
                        <li><strong>Приложения для записи звонков</strong> — полезно для фиксации разговоров с мошенниками</li>
                    </ul>
                </div>
                
                <h4>3. Настройте банковские уведомления</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #1976d2;">
                    <p><strong>Что подключить:</strong></p>
                    <ul>
                        <li>SMS-информирование обо всех операциях</li>
                        <li>Push-уведомления в мобильном приложении банка</li>
                        <li>Ограничения на максимальную сумму операций</li>
                        <li>Подтверждение операций по смс или через приложение</li>
                    </ul>
                </div>
                
                <h4>4. Обучите родственников</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #1976d2;">
                    <p>Пожилые родственники — самая уязвимая группа. Расскажите им:</p>
                    <ul>
                        <li>Никогда не переводить деньги по телефону</li>
                        <li>Всегда перезванивать вам при подозрительных звонках</li>
                        <li>Не сообщать информацию о семье посторонним</li>
                        <li>Звонить вам, если звонящий представляется родственником в беде</li>
                    </ul>
                </div>
                
                <h4>5. Будьте осторожны с персональными данными</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #1976d2;">
                    <p><strong>Что не стоит делать:</strong></p>
                    <ul>
                        <li>Оставлять номер телефона на сомнительных сайтах</li>
                        <li>Участвовать в опросах, где требуют номер телефона</li>
                        <li>Публиковать номер телефона в соцсетях в открытом доступе</li>
                        <li>Отвечать на SMS от неизвестных номеров</li>
                    </ul>
                </div>
                
                <h4>6. Юридическая защита</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #1976d2;">
                    <p><strong>Знайте свои права:</strong></p>
                    <ul>
                        <li>Вы имеете право не разговаривать с неизвестными абонентами</li>
                        <li>Можете требовать письменные подтверждения любой информации</li>
                        <li>Имеете право на защиту персональных данных</li>
                        <li>Можете обратиться в суд, если стали жертвой мошенников</li>
                    </ul>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #e8f5e9; padding: 20px; border-radius: 10px;">
                    <h4><i class="fas fa-shield-alt icon" style="color: #388e3c;"></i> Чек-лист безопасности:</h4>
                    <p><strong>Проверьте, все ли вы сделали для защиты:</strong></p>
                    <ul>
                        <li>✓ PIN-код на SIM-карте активирован</li>
                        <li>✓ Установлено антиспам приложение</li>
                        <li>✓ Включены SMS-уведомления от банка</li>
                        <li>✓ Родственники предупреждены о мошенниках</li>
                        <li>✓ Номер телефона не публикуется в открытом доступе</li>
                        <li>✓ Знаете, куда звонить в случае подозрительных звонков</li>
                    </ul>
                </div>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4><i class="fas fa-phone icon" style="color: #ff9800;"></i> Важные телефоны:</h4>
                    <ul>
                        <li><strong>Горячая линия Госуслуг:</strong> 8-800-100-70-10</li>
                        <li><strong>Центробанк (финансовое мошенничество):</strong> 8-800-250-40-72</li>
                        <li><strong>МВД (киберпреступления):</strong> 8-800-222-74-47</li>
                        <li><strong>Служба безопасности вашего банка</strong> (номер с обратной стороны карты)</li>
                    </ul>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Итоговый тест', 
            duration: '25 мин',
            content: `
                <h3>Итоговый тест по курсу "Телефонное мошенничество"</h3>
                <p>Пройдите тест из 15 вопросов, чтобы проверить свои знания. Для успешного завершения курса нужно правильно ответить на 12 из 15 вопросов.</p>
                
                <div style="text-align: center; margin: 40px 0;">
                    <button class="btn btn-large btn-success" onclick="startCallsTest()">
                        <i class="fas fa-play icon"></i> Начать итоговый тест
                    </button>
                </div>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Советы перед тестом:</h4>
                    <ul>
                        <li>Тест состоит из 15 вопросов с несколькими вариантами ответов</li>
                        <li>На каждый вопрос можно выбрать только один правильный ответ</li>
                        <li>После завершения теста вы увидите ваш результат и объяснения</li>
                        <li>Для успешного прохождения нужно набрать не менее 80% правильных ответов</li>
                        <li>Внимательно читайте вопросы, некоторые имеют "ловушки"</li>
                    </ul>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #388e3c;">Что вы узнали в этом курсе:</h4>
                    <ul>
                        <li>Основные схемы телефонного мошенничества</li>
                        <li>Психологические приемы, которые используют мошенники</li>
                        <li>Как правильно реагировать на подозрительные звонки</li>
                        <li>Методы профилактики и защиты</li>
                        <li>Куда обращаться, если вы стали жертвой мошенников</li>
                    </ul>
                    <p style="margin-top: 15px; font-weight: bold;">Удачи в прохождении теста!</p>
                </div>
            `,
            completed: false 
        }
    ],
    totalLessons: 6,
    totalDuration: '1.5 часа'
},
<!-- В разделе инициализации данных курсов добавлю: -->
'financial': {
    title: 'Финансовое мошенничество',
    icon: 'fa-credit-card',
    color: 'financial',
    description: 'Научитесь распознавать и защищаться от финансовых мошенников в банковской сфере, инвестициях и онлайн-платежах.',
    lessons: [
        { 
            title: 'Основы финансового мошенничества', 
            duration: '15 мин',
            content: `
                <h3>Что такое финансовое мошенничество?</h3>
                <p><strong>Финансовое мошенничество</strong> — это преступная деятельность, направленная на незаконное получение денежных средств или финансовых активов путем обмана, злоупотребления доверием или использования служебного положения.</p>
                
                <h4>Основные виды финансового мошенничества:</h4>
                <ul>
                    <li><strong>Банковское мошенничество:</strong> Кража данных карт, несанкционированные переводы</li>
                    <li><strong>Инвестиционное мошенничество:</strong> Финансовые пирамиды, мошеннические инвестиционные платформы</li>
                    <li><strong>Кредитное мошенничество:</strong> Оформление кредитов на чужое имя</li>
                    <li><strong>Страховое мошенничество:</strong> Ложные страховые случаи</li>
                    <li><strong>Мошенничество с онлайн-платежами:</strong> Поддельные платежные системы</li>
                </ul>
                
                <h4>Масштабы проблемы:</h4>
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <p>Согласно данным Центрального банка РФ:</p>
                    <ul>
                        <li>В 2023 году зафиксировано более 1.5 млн случаев финансового мошенничества</li>
                        <li>Общий ущерб превысил 15 млрд рублей</li>
                        <li>Каждый час мошенники крадут более 1.7 млн рублей</li>
                        <li>Наиболее уязвимая группа — люди 25-45 лет</li>
                    </ul>
                </div>
                
                <h4>Психология финансовых мошенников:</h4>
                <p>Мошенники используют несколько ключевых психологических приемов:</p>
                <ul>
                    <li><strong>Создание срочности:</strong> "Действуйте сейчас, иначе потеряете возможность"</li>
                    <li><strong>Использование авторитета:</strong> Представление банковскими сотрудниками, госслужащими</li>
                    <li><strong>Эмоциональное давление:</strong> Запугивание блокировкой счетов, штрафами</li>
                    <li><strong>Жадность:</strong> Предложение нереально высокой прибыли</li>
                </ul>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #388e3c;"></i> Золотое правило финансовой безопасности:</h4>
                    <p>Никогда не переводите деньги незнакомым людям и не сообщайте данные карт по телефону или в интернете, даже если звонящий представляется сотрудником банка или государственных органов.</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Банковское мошенничество: схемы и защита', 
            duration: '18 мин',
            content: `
                <h3>Банковское мошенничество: схемы и защита</h3>
                <p>Банковское мошенничество — самый распространенный вид финансовых преступлений. Мошенники постоянно совершенствуют свои методы, но большинство схем основаны на нескольких базовых принципах.</p>
                
                <h4>Основные схемы банковского мошенничества:</h4>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 1: "БЛИЗКИЙ В БЕДЕ"</div>
                    <p><strong>Сценарий:</strong> Звонок от "родственника" (часто "внука"), который попал в ДТП, арестован или нуждается в срочном лечении. Требуются деньги на "штраф", "залог" или "операцию".</p>
                    <p><strong>Как защититься:</strong> Не переводите деньги сразу. Позвоните родственнику на его обычный номер или свяжитесь через других членов семьи.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 2: "БЛОКИРОВКА СЧЕТА"</div>
                    <p><strong>Сценарий:</strong> Звонок от "службы безопасности банка" о подозрительных операциях. Для "разблокировки" требуют перевести деньги на "безопасный счет" или сообщить коды из SMS.</p>
                    <p><strong>Как защититься:</strong> Настоящие банки никогда не просят переводить деньги или сообщать коды. Повесьте трубку и позвоните в банк по номеру с обратной стороны карты.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 3: "ПЕРЕПЛАТА"</div>
                    <p><strong>Сценарий:</strong> При продаже товара на Avito или других площадках покупатель "случайно" переводит большую сумму и просит вернуть разницу.</p>
                    <p><strong>Как защититься:</strong> Операция может быть оспорена. Не возвращайте деньги до подтверждения банком окончательности перевода (3-5 рабочих дней).</p>
                </div>
                
                <h4>Технические методы защиты:</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #1976d2;">Настройте безопасность банковских карт:</h4>
                    <ul>
                        <li><strong>Лимиты на операции:</strong> Установите дневные лимиты на снятие наличных и онлайн-платежи</li>
                        <li><strong>Уведомления:</strong> Подключите SMS-информирование обо всех операциях</li>
                        <li><strong>Геолокация:</strong> Включите подтверждение операций из необычных мест</li>
                        <li><strong>3D-Secure:</strong> Всегда используйте дополнительное подтверждение онлайн-платежей</li>
                        <li><strong>Виртуальные карты:</strong> Для онлайн-покупок создавайте карты с ограниченным сроком действия</li>
                    </ul>
                </div>
                
                <h4>Что делать, если вы стали жертвой:</h4>
                <ol>
                    <li><strong>Немедленно позвоните в банк</strong> для блокировки карты</li>
                    <li><strong>Напишите заявление</strong> о несанкционированной операции</li>
                    <li><strong>Обратитесь в полицию</strong> с заявлением о мошенничестве</li>
                    <li><strong>Подайте жалобу</strong> в Центробанк через официальный сайт</li>
                    <li><strong>Смените все пароли</strong> от онлайн-банков</li>
                </ol>
                
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #d32f2f;"><i class="fas fa-exclamation-triangle icon"></i> Важно помнить:</h4>
                    <p>Согласно законодательству РФ, банк обязан вернуть средства, если вы оперативно сообщили о краже и не нарушали правила безопасности (не сообщали коды, не передавали карту третьим лицам).</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Инвестиционное мошенничество и финансовые пирамиды', 
            duration: '20 мин',
            content: `
                <h3>Инвестиционное мошенничество и финансовые пирамиды</h3>
                <p>Инвестиционное мошенничество предлагает нереально высокую доходность при минимальных рисках. Финансовые пирамиды — классический пример таких схем, которые существуют десятилетиями, меняя лишь форму.</p>
                
                <h4>Признаки финансовой пирамиды:</h4>
                <div style="background-color: #ffebee; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;">Красные флаги:</h4>
                    <ul>
                        <li><strong>Обещание гарантированной доходности</strong> выше 30% годовых</li>
                        <li><strong>Отсутствие лицензии ЦБ</strong> на финансовую деятельность</li>
                        <li><strong>Акцент на привлечение новых участников</strong> как основной источник доходов</li>
                        <li><strong>Сложная структура выплат</strong> с бонусами за рефералов</li>
                        <li><strong>Отсутствие понятного бизнеса</strong> или продукта</li>
                        <li><strong>Давление на быстрый старт</strong> "пока есть места"</li>
                    </ul>
                </div>
                
                <h4>Современные виды инвестиционного мошенничества:</h4>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">КРИПТОВАЛЮТНЫЕ СХЕМЫ</div>
                    <p><strong>Схема:</strong> Предложение инвестировать в "уникальную" криптовалюту или "гарантированные" торговые роботы с доходностью 5-10% в день.</p>
                    <p><strong>Примеры:</strong> Finiko, Forsage, множество "инвестиционных платформ" без регуляции.</p>
                    <p><strong>Реальность:</strong> Большинство таких платформ — классические пирамиды, где выплаты производятся за счет новых вкладчиков.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">ФОРЕКС И БИНАРНЫЕ ОПЦИОНЫ</div>
                    <p><strong>Схема:</strong> Брокеры без лицензии ЦБ предлагают "обучение" с гарантированной прибылью или "сигналы" для торговли.</p>
                    <p><strong>Статистика:</strong> 85% частных трейдеров теряют деньги на Форексе. Бинарные опционы запрещены в большинстве развитых стран как азартные игры.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">КРАУДФАНДИНГОВЫЕ ПЛАТФОРМЫ</div>
                    <p><strong>Схема:</strong> Привлекательные проекты с фальшивой документацией и поддельными отчетами о прогрессе.</p>
                    <p><strong>Защита:</strong> Проверяйте регистрацию проектов в реестре ЦБ, изучайте команду, требуйте детальные бизнес-планы.</p>
                </div>
                
                <h4>Как проверить инвестиционную компанию:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #388e3c;">Чек-лист безопасности:</h4>
                    <ol>
                        <li>Проверьте наличие лицензии ЦБ РФ на сайте banki.ru/licences</li>
                        <li>Изучите компанию в реестре недобросовестных компаний ЦБ</li>
                        <li>Поищите независимые отзывы, а не только на сайте компании</li>
                        <li>Убедитесь в наличии реального офиса (посетите лично)</li>
                        <li>Проконсультируйтесь с независимым финансовым советником</li>
                        <li>Помните: чем выше обещанная доходность, тем выше риски</li>
                    </ol>
                </div>
                
                <h4>Законодательная защита:</h4>
                <ul>
                    <li><strong>Центральный банк РФ</strong> ведет реестр финансовых пирамид</li>
                    <li><strong>МВД России</strong> расследует дела о финансовом мошенничестве</li>
                    <li><strong>Федеральная налоговая служба</strong> контролирует легальность деятельности</li>
                    <li><strong>Роспотребнадзор</strong> защищает права потребителей финансовых услуг</li>
                </ul>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Финансовая грамотность:</h4>
                    <p>Запомните простое правило: если что-то звучит слишком хорошо, чтобы быть правдой — скорее всего, это мошенничество. Настоящие инвестиции всегда связаны с рисками, которые четко прописываются в документах.</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Мошенничество с онлайн-платежами и электронными деньгами', 
            duration: '16 мин',
            content: `
                <h3>Мошенничество с онлайн-платежами и электронными деньгами</h3>
                <p>С развитием цифровых технологий мошенники освоили новые методы кражи денег через онлайн-платежи, электронные кошельки и мобильные приложения.</p>
                
                <h4>Основные схемы мошенничества:</h4>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 1: ФИШИНГ ПЛАТЕЖНЫХ СИСТЕМ</div>
                    <p><strong>Метод:</strong> Поддельные письма от Яндекс.Денег, Qiwi, WebMoney о блокировке кошелька с требованием перейти по ссылке и "подтвердить данные".</p>
                    <p><strong>Пример ссылки:</strong> qiwi-secure.com (вместо qiwi.com), yandex-money-help.ru</p>
                    <p><strong>Защита:</strong> Всегда заходите на сайты платежных систем напрямую, а не по ссылкам из писем.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 2: МОШЕННИЧЕСТВО С АВТОПЛАТЕЖАМИ</div>
                    <p><strong>Метод:</strong> При оплате в интернете мелким шрифтом добавляется согласие на регулярные списания (часто на сомнительные услуги).</p>
                    <p><strong>Пример:</strong> Оплата 100 рублей за "гороскоп" с автоматическим подключением ежедневных платежей по 300 рублей.</p>
                    <p><strong>Защита:</strong> Внимательно читайте условия, особенно мелкий шрифт. Регулярно проверяйте выписки по картам.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 3: ПОДДЕЛЬНЫЕ ПЛАТЕЖНЫЕ ШЛЮЗЫ</div>
                    <p><strong>Метод:</strong> При оплате на сайте вас перенаправляют на поддельную платежную страницу, которая выглядит как легитимная.</p>
                    <p><strong>Признаки:</strong> Отсутствие HTTPS, ошибки в оформлении, запрос CVV-кода для перевода между физическими лицами.</p>
                    <p><strong>Защита:</strong> Проверяйте сертификат безопасности (замок в адресной строке) на платежных страницах.</p>
                </div>
                
                <h4>Безопасность мобильных платежей:</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #1976d2;">Правила безопасности:</h4>
                    <ul>
                        <li><strong>Используйте официальные приложения</strong> из App Store или Google Play</li>
                        <li><strong>Не храните крупные суммы</strong> на электронных кошельках</li>
                        <li><strong>Включайте двухфакторную аутентификацию</strong> везде, где это возможно</li>
                        <li><strong>Не используйте публичный Wi-Fi</strong> для финансовых операций</li>
                        <li><strong>Установите лимиты</strong> на дневные операции</li>
                        <li><strong>Регулярно обновляйте приложения</strong> для получения исправлений безопасности</li>
                    </ul>
                </div>
                
                <h4>Особенности популярных платежных систем:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Система</th>
                        <th style="padding: 10px; text-align: left;">Особенности защиты</th>
                        <th style="padding: 10px; text-align: left;">Основные риски</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">СБП (Система быстрых платежей)</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Лимиты на операции, подтверждение по SMS</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Мошенничество с использованием социальной инженерии</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Яндекс.Деньги</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Анонимные номера кошельков, защита паролем</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Фишинг, взлом аккаунтов через утечки паролей</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Qiwi</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Привязка к номеру телефона, PIN-код</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">SIM-своппинг (перехват номера телефона)</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">PayPal</td>
                        <td style="padding: 10px;">Покупательская защита, двухфакторная аутентификация</td>
                        <td style="padding: 10px;">Мошенничество с возвратами, поддельные уведомления</td>
                    </tr>
                </table>
                
                <h4>Что делать при утере средств:</h4>
                <ol>
                    <li><strong>Немедленно заблокируйте кошелек</strong> через службу поддержки</li>
                    <li><strong>Сохраните все данные</strong> о транзакциях (номера, время, суммы)</li>
                    <li><strong>Обратитесь в службу безопасности</strong> платежной системы</li>
                    <li><strong>Подайте заявление в полицию</strong> с детальным описанием инцидента</li>
                    <li><strong>Сообщите о мошенничестве</strong> в Центробанк через официальный сайт</li>
                </ol>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4><i class="fas fa-shield-alt icon" style="color: #388e3c;"></i> Важное правило:</h4>
                    <p>Электронные деньги защищены так же, как и обычные. Не доверяйте мифу о том, что "с электронных кошельков ничего не вернуть". При оперативном обращении и наличии доказательств мошенничества у вас есть хорошие шансы вернуть средства.</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Кредитное мошенничество и микрозаймы', 
            duration: '17 мин',
            content: `
                <h3>Кредитное мошенничество и микрозаймы</h3>
                <p>Кредитное мошенничество стало массовым явлением с развитием онлайн-кредитования. Мошенники используют как технические уязвимости, так и социальную инженерию для оформления кредитов на чужие имена.</p>
                
                <h4>Основные схемы кредитного мошенничества:</h4>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 1: ОФОРМЛЕНИЕ КРЕДИТА НА ЧУЖОЕ ИМЯ</div>
                    <p><strong>Метод:</strong> Использование украденных паспортных данных для получения кредитов в МФО и банках.</p>
                    <p><strong>Источники данных:</strong> Утечки с сайтов, фишинг, кража документов, данные из соцсетей.</p>
                    <p><strong>Защита:</strong> Регулярно проверяйте свою кредитную историю на сайтах НБКИ и ОКБ.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 2: "КРЕДИТНЫЕ БРОКЕРЫ"</div>
                    <p><strong>Метод:</strong> Компании, обещающие оформить кредит на любую сумму без отказа за предоплату.</p>
                    <p><strong>Действительность:</strong> Настоящие брокеры берут комиссию только после выдачи кредита и не требуют предоплат.</p>
                    <p><strong>Защита:</strong> Никогда не платите за "гарантию" получения кредита. Оформляйте заявки напрямую в банках.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 3: РЕФИНАНСИРОВАНИЕ С ОБМАНОМ</div>
                    <p><strong>Метод:</strong> Предложение рефинансировать кредит под низкий процент с требованием перевода денег для "погашения старого кредита".</p>
                    <p><strong>Действительность:</strong> Настоящее рефинансирование происходит без перевода денег заемщику.</p>
                    <p><strong>Защита:</strong> Деньги при рефинансировании переводятся напрямую между банками.</p>
                </div>
                
                <h4>Опасности микрозаймов:</h4>
                <div style="background-color: #ffebee; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;">Риски МФО (микрофинансовых организаций):</h4>
                    <ul>
                        <li><strong>Годовая ставка</strong> может достигать 365% и более</li>
                        <li><strong>Штрафы и пени</strong> за просрочку исчисляются ежедневно</li>
                        <li><strong>Доступ к контактам</strong> для давления на заемщика и его знакомых</li>
                        <li><strong>Автоматическое продление</strong> займа при несвоевременном погашении</li>
                        <li><strong>Ухудшение кредитной истории</strong> при малейших просрочках</li>
                    </ul>
                </div>
                
                <h4>Как защититься от кредитного мошенничества:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #388e3c;">Меры профилактики:</h4>
                    <ol>
                        <li><strong>Регулярно проверяйте кредитную историю</strong> (2 раза в год бесплатно)</li>
                        <li><strong>Не сообщайте паспортные данные</strong> по телефону или в мессенджерах</li>
                        <li><strong>Используйте услугу "Кредитный замок"</strong> в бюро кредитных историй</li>
                        <li><strong>Храните паспорт в безопасном месте</strong>, не оставляйте копии где попало</li>
                        <li><strong>Проверяйте лицензии МФО</strong> на сайте Центробанка</li>
                        <li><strong>Читайте договоры полностью</strong> перед подписанием</li>
                    </ol>
                </div>
                
                <h4>Законодательная защита заемщиков:</h4>
                <ul>
                    <li><strong>Закон о потребительском кредите</strong> устанавливает максимальную сумму процентов</li>
                    <li><strong>Право на охлаждение</strong> — 14 дней для отказа от займа без объяснения причин</li>
                    <li><strong>Запрет на звонки родственникам</strong> и коллегам с требованиями о долге</li>
                    <li><strong>Максимальная сумма взысканий</strong> не может превышать двукратный размер займа</li>
                    <li><strong>Бесплатная проверка КИ</strong> 2 раза в год в каждом бюро</li>
                </ul>
                
                <h4>Что делать, если оформили кредит на ваше имя:</h4>
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 15px 0; border: 3px solid #ff9800;">
                    <h4><i class="fas fa-exclamation-triangle icon" style="color: #ff9800;"></i> Срочный алгоритм действий:</h4>
                    <ol>
                        <li><strong>Немедленно напишите заявление</strong> в банк/МФО о несогласии с кредитом</li>
                        <li><strong>Подайте заявление в полицию</strong> о мошенничестве с приложением всех документов</li>
                        <li><strong>Направьте жалобу в ЦБ РФ</strong> на действия кредитной организации</li>
                        <li><strong>Обратитесь в бюро кредитных историй</strong> для оспаривания информации</li>
                        <li><strong>Проконсультируйтесь с юристом</strong> по финансовым вопросам</li>
                    </ol>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-info-circle icon"></i> Важная информация:</h4>
                    <p>С 2019 года в России действует Единая биометрическая система, которая позволяет удаленно идентифицировать личность. Все чаще банки требуют биометрию для оформления кредитов, что снижает риски мошенничества.</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Профилактика и правовая защита', 
            duration: '22 мин',
            content: `
                <h3>Профилактика и правовая защита от финансового мошенничества</h3>
                <p>Лучшая защита от финансового мошенничества — это профилактика и знание своих прав. В этом уроке вы узнаете, как создать многоуровневую защиту и куда обращаться в случае проблем.</p>
                
                <h4>Многоуровневая система защиты:</h4>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #388e3c;">Уровень 1: Личная безопасность</h4>
                    <ul>
                        <li><strong>Финансовая грамотность:</strong> Регулярное обучение, чтение финансовой литературы</li>
                        <li><strong>Здоровый скептицизм:</strong> Критическая оценка любых "выгодных" предложений</li>
                        <li><strong>Контроль эмоций:</strong> Умение распознавать психологическое давление</li>
                        <li><strong>Конфиденциальность:</strong> Защита персональных данных в офлайн и онлайн-пространстве</li>
                    </ul>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #1976d2;">Уровень 2: Техническая защита</h4>
                    <ul>
                        <li><strong>Антивирусное ПО:</strong> Регулярно обновляемые программы на всех устройствах</li>
                        <li><strong>Менеджер паролей:</strong> Уникальные сложные пароли для каждого сервиса</li>
                        <li><strong>Двухфакторная аутентификация:</strong> Везде, где это возможно</li>
                        <li><strong>VPN:</strong> При использовании публичных сетей</li>
                        <li><strong>Регулярные обновления:</strong> Операционных систем и приложений</li>
                    </ul>
                </div>
                
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #ff9800;">Уровень 3: Банковская безопасность</h4>
                    <ul>
                        <li><strong>Лимиты на операции:</strong> Дневные и разовые ограничения</li>
                        <li><strong>Уведомления:</strong> SMS и push об всех операциях</li>
                        <li><strong>Виртуальные карты:</strong> Для онлайн-платежей с ограниченным сроком действия</li>
                        <li><strong>Разделение счетов:</strong> Основной счет и карта для ежедневных трат</li>
                        <li><strong>Регулярная проверка выписок:</strong> Еженедельный контроль операций</li>
                    </ul>
                </div>
                
                <h4>Куда обращаться за помощью:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Организация</th>
                        <th style="padding: 10px; text-align: left;">Телефон/сайт</th>
                        <th style="padding: 10px; text-align: left;">Чем поможет</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Центральный банк РФ</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">8-800-250-40-72<br>cbr.ru</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Жалобы на банки и МФО, список пирамид</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Роспотребнадзор</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">8-800-100-00-04<br>rospotrebnadzor.ru</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Защита прав потребителей финансовых услуг</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">МВД России</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">8-800-222-74-47<br>мвд.рф</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Прием заявлений о мошенничестве</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Федеральная налоговая служба</td>
                        <td style="padding: 10px;">8-800-222-22-22<br>nalog.ru</td>
                        <td style="padding: 10px;">Проверка легальности компаний, ИНН</td>
                    </tr>
                </table>
                
                <h4>Юридические аспекты защиты:</h4>
                <ul>
                    <li><strong>Статья 159 УК РФ "Мошенничество"</strong> — до 10 лет лишения свободы</li>
                    <li><strong>Закон "О защите прав потребителей"</strong> — право на расторжение договора</li>
                    <li><strong>Закон "О микрофинансовой деятельности"</strong> — ограничения по процентам</li>
                    <li><strong>Право на охлаждение</strong> — 14 дней для отказа от финансовой услуги</li>
                    <li><strong>Срок исковой давности</strong> — 3 года для подачи иска в суд</li>
                </ul>
                
                <h4>Как правильно составить заявление:</h4>
                <div style="background-color: #f5f5f5; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <p><strong>Обязательные элементы заявления:</strong></p>
                    <ol>
                        <li><strong>Дата и время</strong> инцидента</li>
                        <li><strong>Подробное описание</strong> событий в хронологическом порядке</li>
                        <li><strong>Данные мошенников</strong> (номера телефонов, реквизиты, ссылки)</li>
                        <li><strong>Доказательства</strong> (скриншоты, записи разговоров, выписки)</li>
                        <li><strong>Сумма ущерба</strong> с приложением документов</li>
                        <li><strong>Ваши контактные данные</strong> для связи</li>
                    </ol>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #e8f5e9; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-tasks icon" style="color: #388e3c;"></i> Ежемесячный чек-лист финансовой безопасности:</h4>
                    <ul>
                        <li>✓ Проверена кредитная история</li>
                        <li>✓ Проверены выписки по всем картам и счетам</li>
                        <li>✓ Обновлены пароли и двухфакторная аутентификация</li>
                        <li>✓ Проверены лимиты на операциях</li>
                        <li>✓ Проверены активные подписки и автоплатежи</li>
                        <li>✓ Обучены родственники (особенно пожилые)</li>
                        <li>✓ Обновлено антивирусное ПО</li>
                        <li>✓ Проверены настройки приватности в соцсетях</li>
                    </ul>
                </div>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin-top: 20px; text-align: center;">
                    <h4 style="color: #ff9800;">Ваш финансовый иммунитет</h4>
                    <p style="font-size: 1.1rem;">Финансовая безопасность — это не разовое действие, а регулярная практика. Чем больше вы знаете и чем внимательнее относитесь к своим финансам, тем меньше шансов у мошенников обмануть вас.</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Итоговый тест', 
            duration: '25 мин',
            content: `
                <h3>Итоговый тест по курсу "Финансовое мошенничество"</h3>
                <p>Пройдите тест из 10 вопросов, чтобы проверить свои знания. Для успешного завершения курса нужно правильно ответить на 8 из 10 вопросов (80%).</p>
                
                <div style="text-align: center; margin: 40px 0;">
                    <button class="btn btn-large btn-success" onclick="startFinanceFraudTest()">
                        <i class="fas fa-play icon"></i> Начать итоговый тест
                    </button>
                </div>
                
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Информация о тесте:</h4>
                    <ul>
                        <li><strong>10 вопросов</strong> с выбором одного правильного ответа</li>
                        <li><strong>20 минут</strong> на выполнение</li>
                        <li><strong>Проходной балл:</strong> 80% (8 правильных ответов)</li>
                        <li>После теста вы увидите детальные результаты с объяснениями</li>
                        <li>При успешном прохождении получите сертификат</li>
                    </ul>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #388e3c;">Что вы узнали в этом курсе:</h4>
                    <ul>
                        <li>Основные виды финансового мошенничества и их признаки</li>
                        <li>Современные схемы банковского мошенничества и методы защиты</li>
                        <li>Как распознать финансовые пирамиды и инвестиционное мошенничество</li>
                        <li>Безопасность онлайн-платежей и электронных денег</li>
                        <li>Риски кредитного мошенничества и микрозаймов</li>
                        <li>Правовые механизмы защиты и куда обращаться за помощью</li>
                    </ul>
                    <p style="margin-top: 15px; font-weight: bold; text-align: center;">
                        Эти знания помогут вам защитить свои финансы и не стать жертвой мошенников!
                    </p>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-graduation-cap icon"></i> Советы перед тестом:</h4>
                    <ul>
                        <li>Внимательно читайте вопросы</li>
                        <li>Помните о ключевых признаках мошенничества</li>
                        <li>Основные правила финансовой безопасности</li>
                        <li>Организации, куда обращаться за помощью</li>
                        <li>Правовые аспекты защиты</li>
                    </ul>
                </div>
            `,
            completed: false 
        }
    ],
    totalLessons: 7,
    totalDuration: '2 часа'
},
'social': {
    title: 'Безопасность в социальных сетях',
    icon: 'fa-users',
    color: 'social',
    description: 'Защитите свои аккаунты в соцсетях, изучите методы защиты приватности и узнайте о фишинге в мессенджерах.',
    lessons: [
        { 
            title: 'Основы безопасности в социальных сетях', 
            duration: '15 мин',
            content: `<h3>Основы безопасности в социальных сетях</h3>
                <p>Социальные сети стали неотъемлемой частью нашей жизни, но они также представляют собой значительный риск для нашей приватности и безопасности. Понимание основных принципов защиты поможет вам безопасно использовать эти платформы.</p>
                
                <h4>Почему безопасность в соцсетях так важна:</h4>
                <ul>
                    <li><strong>Концентрация личной информации:</strong> Соцсети содержат данные о вашей жизни, друзьях, интересах и привычках</li>
                    <li><strong>Цель для мошенников:</strong> Аккаунты в соцсетях часто становятся мишенями для фишинга и социальной инженерии</li>
                    <li><strong>Риск утечки данных:</strong> Крупные платформы регулярно становятся жертвами утечек данных</li>
                    <li><strong>Влияние на репутацию:</strong> Взломанный аккаунт может нанести ущерб вашей репутации</li>
                </ul>
                
                <h4>Типы угроз в социальных сетях:</h4>
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <ul>
                        <li><strong>Фишинг:</strong> Поддельные сообщения с просьбой перейти по ссылке или ввести данные</li>
                        <li><strong>Кража аккаунта:</strong> Получение доступа к вашему профилю через утечки паролей или фишинг</li>
                        <li><strong>Социальная инженерия:</strong> Использование информации из вашего профиля для манипуляций</li>
                        <li><strong>Вредоносные приложения:</strong> Третьесторонние приложения, которые запрашивают слишком много прав</li>
                        <li><strong>Шпионское ПО:</strong> Программы, скрытно собирающие информацию о вашей активности</li>
                    </ul>
                </div>
                
                <h4>Основные правила безопасности:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-shield-alt icon"></i> Золотые правила:</h4>
                    <ol>
                        <li><strong>Используйте уникальные пароли</strong> для каждого аккаунта</li>
                        <li><strong>Включайте двухфакторную аутентификацию</strong> везде, где это возможно</li>
                        <li><strong>Ограничивайте публичную информацию</strong> о себе в профилях</li>
                        <li><strong>Будьте осторожны с ссылками</strong> и вложениями в сообщениях</li>
                        <li><strong>Регулярно проверяйте настройки приватности</strong></li>
                        <li><strong>Обновляйте приложения</strong> для получения исправлений безопасности</li>
                    </ol>
                </div>
                
                <h4>Пример опасной ситуации:</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ПРИМЕР ФИШИНГА</div>
                    <p><strong>Сообщение:</strong> "Привет! Посмотри это смешное видео с тобой: [ссылка] Нашла в архиве, не могу не поделиться!"</p>
                    <p><strong>От кого:</strong> От друга, чей аккаунт, возможно, был взломан</p>
                    <p><strong>Опасность:</strong> Ссылка ведет на фишинговый сайт, который запросит данные для входа в соцсеть</p>
                </div>
                
                <h4>Что делать в таких случаях:</h4>
                <ul>
                    <li><strong>Не переходить по ссылке</strong>, даже если сообщение от друга</li>
                    <li><strong>Связаться с другом другим способом</strong> и предупредить о возможном взломе</li>
                    <li><strong>Сообщить о подозрительном сообщении</strong> администрации соцсети</li>
                    <li><strong>Проверить свой аккаунт</strong> на предмет несанкционированной активности</li>
                </ul>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Практический совет:</h4>
                    <p>Регулярно просматривайте список устройств, с которых выполнен вход в ваш аккаунт. Если увидите незнакомое устройство или местоположение — немедленно смените пароль и завершите все сессии.</p>
                </div>`,
            completed: false 
        },
        { 
            title: 'Настройки приватности и конфиденциальности', 
            duration: '18 мин',
            content: `<h3>Настройки приватности и конфиденциальности</h3>
                <p>Правильная настройка приватности — это фундамент безопасности в социальных сетях. Большинство платформ предлагают гибкие настройки, но многие пользователи оставляют их по умолчанию, что может быть опасно.</p>
                
                <h4>Ключевые настройки приватности:</h4>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">1. Кто может видеть ваш профиль</h4>
                    <ul>
                        <li><strong>Только друзья:</strong> Наиболее безопасный вариант</li>
                        <li><strong>Друзья друзей:</strong> Умеренная открытость</li>
                        <li><strong>Все пользователи:</strong> Максимальная открытость (не рекомендуется)</li>
                        <li><strong>Особые списки:</strong> Расширенное управление доступом</li>
                    </ul>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">2. Управление видимостью публикаций</h4>
                    <ul>
                        <li><strong>Контроль для каждой публикации:</strong> Выбирайте аудиторию для каждого поста</li>
                        <li><strong>Ограничение старых публикаций:</strong> Массовое изменение видимости прошлых постов</li>
                        <li><strong>Отключение геометок:</strong> Не показывать местоположение в публикациях</li>
                        <li><strong>Контроль тегов:</strong> Утверждение тегов перед их появлением на вашей стене</li>
                    </ul>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">3. Информация в профиле</h4>
                    <ul>
                        <li><strong>Контактная информация:</strong> Ограничьте видимость email и телефона</li>
                        <li><strong>Дата рождения:</strong> Показывайте только день и месяц (без года)</li>
                        <li><strong>Место работы и учебы:</strong> Оцените необходимость этой информации</li>
                        <li><strong>Семейное положение:</strong> Личная информация, которая может быть использована мошенниками</li>
                    </ul>
                </div>
                
                <h4>Опасности излишней открытости:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Информация</th>
                        <th style="padding: 10px; text-align: left;">Риск</th>
                        <th style="padding: 10px; text-align: left;">Рекомендация</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Полная дата рождения</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Использование для восстановления паролей, кража личности</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Скрыть год рождения</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Домашний адрес</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Физическая безопасность, кража</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Не публиковать никогда</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Геометки из дома</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Определение места жительства</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Отключить геометки</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Расписание дня</td>
                        <td style="padding: 10px;">Знание, когда дома никого нет</td>
                        <td style="padding: 10px;">Не публиковать в реальном времени</td>
                    </tr>
                </table>
                
                <h4>Практические рекомендации для популярных платформ:</h4>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #ff9800;">ВКонтакте:</h4>
                    <ul>
                        <li>Настройки → Приватность → "Кто видит основную информацию моей страницы" → Только друзья</li>
                        <li>Настройки → Приватность → "Кто может оставлять записи на моей стене" → Только друзья</li>
                        <li>Настройки → Приватность → "Кто видит список моих друзей" → Только друзья</li>
                        <li>Настройки → Приватность → "Кто видит фотографии, на которых меня отметили" → Только друзья</li>
                    </ul>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>Instagram:</h4>
                    <ul>
                        <li>Настройки → Конфиденциальность → Закрытый аккаунт (рекомендуется)</li>
                        <li>Настройки → Конфиденциальность → История → "Скрыть историю от"</li>
                        <li>Настройки → Конфиденциальность → Комментарии → Фильтрация оскорбительных комментариев</li>
                        <li>Настройки → Конфиденциальность → Активность → Отключить "Показывать статус активности"</li>
                    </ul>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">Facebook:</h4>
                    <ul>
                        <li>Настройки и конфиденциальность → Настройки конфиденциальности → Ограничить аудиторию для старых публикаций</li>
                        <li>Настройки и конфиденциальность → Настройки → Безопасность и вход → Настройка двухфакторной аутентификации</li>
                        <li>Настройки и конфиденциальность → Настройки → Ваша информация в Facebook → Ограничение доступа к старым публикаций</li>
                    </ul>
                </div>
                
                <h4>Регулярная проверка настроек:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-calendar-check icon"></i> План регулярной проверки:</h4>
                    <ul>
                        <li><strong>Ежемесячно:</strong> Проверка списка друзей/подписчиков (удаление незнакомых)</li>
                        <li><strong>Раз в 3 месяца:</strong> Пересмотр настроек приватности</li>
                        <li><strong>Раз в 6 месяцев:</strong> Проверка активных сессий и устройств</li>
                        <li><strong>При смене пароля:</strong> Проверка всех подключенных приложений</li>
                        <li><strong>После обновления соцсети:</strong> Проверка новых настроек приватности</li>
                    </ul>
                </div>
                
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #d32f2f;"><i class="fas fa-exclamation-triangle icon"></i> Важно помнить:</h4>
                    <p>Настройки приватности по умолчанию часто являются наиболее открытыми. Компании заинтересованы в максимальном сборе и использовании данных. Ваша задача — сознательно ограничить доступ к вашей информации.</p>
                </div>`,
            completed: false 
        },
        { 
            title: 'Фишинг в мессенджерах и соцсетях', 
            duration: '20 мин',
            content: `<h3>Фишинг в мессенджерах и соцсетях</h3>
                <p>Мессенджеры и социальные сети стали основным каналом для фишинговых атак. Мошенники используют доверительные отношения между пользователями для распространения вредоносных ссылок и кражи данных.</p>
                
                <h4>Распространенные схемы фишинга в мессенджерах:</h4>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 1: СООБЩЕНИЕ ОТ ДРУГА</div>
                    <p><strong>Сообщение:</strong> "Привет! Срочно нужна помощь. Не могу зайти в свой аккаунт ВК. Можешь перейти по этой ссылке и подтвердить, что это я? [ссылка]"</p>
                    <p><strong>Цель:</strong> Получить доступ к вашему аккаунту через фишинговую страницу</p>
                    <p><strong>Как работает:</strong> Ссылка ведет на поддельную страницу входа, которая крадет ваш логин и пароль</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 2: "ВИДЕО С ВАМИ"</div>
                    <p><strong>Сообщение:</strong> "Ха-ха, посмотри, что я нашел! Это же ты? [ссылка]"</p>
                    <p><strong>Цель:</strong> Заинтересовать и заставить перейти по ссылке</p>
                    <p><strong>Особенность:</strong> Использует любопытство и интерес к собственной персоне</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА 3: КОНКУРСЫ И РОЗЫГРЫШИ</div>
                    <p><strong>Сообщение:</strong> "Поздравляем! Вы выиграли iPhone в нашем конкурсе! Для получения перейдите по ссылке и введите данные для доставки."</p>
                    <p><strong>Цель:</strong> Сбор персональных данных или оплата "доставки"</p>
                    <p><strong>Метод:</strong> Использование жадности и желания получить что-то бесплатно</p>
                </div>
                
                <h4>Признаки фишинговых сообщений:</h4>
                <div style="background-color: #ffebee; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #d32f2f;">Красные флаги:</h4>
                    <ul>
                        <li><strong>Неожиданное сообщение</strong> от друга на необычную тему</li>
                        <li><strong>Требование срочных действий</strong> ("сделай это сейчас", "только сегодня")</li>
                        <li><strong>Ссылки на подозрительные домены</strong> (не соответствующие официальным)</li>
                        <li><strong>Ошибки в тексте</strong> (орфографические, пунктуационные)</li>
                        <li><strong>Просьба о деньгах</strong> или финансовой помощи</li>
                        <li><strong>Требование личных данных</strong> (пароли, коды, паспортные данные)</li>
                    </ul>
                </div>
                
                <h4>Как проверить безопасность ссылки:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;">Алгоритм проверки:</h4>
                    <ol>
                        <li><strong>Не нажимать сразу</strong> — сначала проанализировать</li>
                        <li><strong>Проверить домен</strong> — соответствует ли он официальному сайту</li>
                        <li><strong>Использовать онлайн-сервисы</strong> для проверки ссылок (VirusTotal, URLVoid)</li>
                        <li><strong>Связаться с отправителем</strong> другим способом (позвонить, написать в другом мессенджере)</li>
                        <li><strong>Ввести ссылку вручную</strong> в браузере, если уверены в необходимости перехода</li>
                    </ol>
                </div>
                
                <h4>Примеры опасных доменов:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Официальный домен</th>
                        <th style="padding: 10px; text-align: left;">Фишинговый домен</th>
                        <th style="padding: 10px; text-align: left;">Различие</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">vk.com</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">vk-secure.com</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Добавлено "-secure"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">instagram.com</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">instagrarn.com</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Замена "m" на "rn"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">facebook.com</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">faceb00k.com</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Замена "o" на "0"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; color: #388e3c;">telegram.org</td>
                        <td style="padding: 10px; color: #d32f2f;">telegrarn.org</td>
                        <td style="padding: 10px;">Замена "m" на "rn"</td>
                    </tr>
                </table>
                
                <h4>Что делать, если вы перешли по фишинговой ссылке:</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin: 20px 0; border: 3px solid #ff9800;">
                    <h4 style="color: #ff9800;"><i class="fas fa-exclamation-triangle icon"></i> Срочные действия:</h4>
                    <ol>
                        <li><strong>Немедленно закройте вкладку</strong> браузера</li>
                        <li><strong>Не вводите никакие данные</strong>, если уже начали</li>
                        <li><strong>Очистите кэш и cookies</strong> браузера</li>
                        <li><strong>Проверьте антивирусом</strong> устройство</li>
                        <li><strong>Смените пароль</strong> от аккаунта соцсети</li>
                        <li><strong>Включите двухфакторную аутентификацию</strong>, если еще не сделали</li>
                        <li><strong>Сообщите друзьям</strong>, что от вашего имени могли быть отправлены фишинговые сообщения</li>
                    </ol>
                </div>
                
                <h4>Защита от фишинга в мессенджерах:</h4>
                <ul>
                    <li><strong>Включите двухшаговую проверку</strong> во всех мессенджерах</li>
                    <li><strong>Используйте пароли для чатов</strong> в мессенджерах с такой возможностью</li>
                    <li><strong>Не открывайте вложения</strong> от незнакомых отправителей</li>
                    <li><strong>Проверяйте сертификаты безопасности</strong> при установке мессенджеров</li>
                    <li><strong>Обновляйте приложения</strong> регулярно</li>
                </ul>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-lightbulb icon"></i> Практический совет:</h4>
                    <p>Создайте с друзьями и семьей "кодовое слово" или вопрос, который вы будете использовать для проверки подлинности сообщений в экстренных ситуациях. Например: "Как звали нашу первую учительницу?"</p>
                </div>`,
            completed: false 
        },
        { 
            title: 'Защита аккаунтов и пароли', 
            duration: '22 мин',
            content: `<h3>Защита аккаунтов и управление паролями</h3>
                <p>Надежная защита аккаунтов в социальных сетях начинается с правильного управления паролями и использования дополнительных средств безопасности.</p>
                
                <h4>Требования к надежным паролям:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #388e3c;">Характеристики сильного пароля:</h4>
                    <ul>
                        <li><strong>Длина:</strong> Не менее 12 символов (лучше 16+)</li>
                        <li><strong>Сложность:</strong> Комбинация букв (верхний/нижний регистр), цифр, специальных символов</li>
                        <li><strong>Уникальность:</strong> Разные пароли для разных сервисов</li>
                        <li><strong>Непредсказуемость:</strong> Не использовать личную информацию, словарные слова</li>
                        <li><strong>Регулярная смена:</strong> Каждые 3-6 месяцев для важных аккаунтов</li>
                    </ul>
                </div>
                
                <h4>Методы создания надежных паролей:</h4>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>Метод 1: Фразы-пароли</h4>
                    <p><strong>Пример:</strong> "МойКотЛюбитРыбу123!" (16 символов)</p>
                    <p><strong>Преимущество:</strong> Легко запомнить, трудно взломать</p>
                    <p><strong>Совет:</strong> Используйте русские слова, но на английской раскладке для дополнительной сложности</p>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>Метод 2: Акронимы</h4>
                    <p><strong>Пример:</strong> Фраза: "В 2024 году я посетил Париж и Лондон" → Пароль: "V2024gIaPiL!"</p>
                    <p><strong>Преимущество:</strong> Индивидуальный подход, высокая энтропия</p>
                    <p><strong>Совет:</strong> Используйте личные фразы, которые знаете только вы</p>
                </div>
                
                <h4>Менеджеры паролей:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Менеджер</th>
                        <th style="padding: 10px; text-align: left;">Преимущества</th>
                        <th style="padding: 10px; text-align: left;">Особенности</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;"><strong>Bitwarden</strong></td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Бесплатный, открытый исходный код, кроссплатформенный</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Синхронизация между устройствами, генератор паролей</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;"><strong>LastPass</strong></td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Простой интерфейс, интеграция с браузерами</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Аудит безопасности паролей, многофакторная аутентификация</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;"><strong>1Password</strong></td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Высокая безопасность, удобство использования</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">"Секретный ключ" + мастер-пароль, режим путешествия</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;"><strong>KeePass</strong></td>
                        <td style="padding: 10px;">Локальное хранение, полный контроль</td>
                        <td style="padding: 10px;">База паролей на вашем устройстве, плагины для расширения функциональности</td>
                    </tr>
                </table>
                
                <h4>Двухфакторная аутентификация (2FA):</h4>
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #1976d2;">Как работает 2FA:</h4>
                    <p><strong>Принцип:</strong> Два фактора для входа:
                        1. Что-то, что вы знаете (пароль)
                        2. Что-то, что у вас есть (телефон, токен) или вы есть (биометрия)</p>
                    
                    <h4>Типы 2FA:</h4>
                    <ul>
                        <li><strong>SMS-коды:</strong> Код приходит в SMS (наименее безопасный)</li>
                        <li><strong>Аутентификаторы:</strong> Google Authenticator, Microsoft Authenticator, Authy</li>
                        <li><strong>Аппаратные токены:</strong> YubiKey, Titan Security Key</li>
                        <li><strong>Биометрия:</strong> Отпечаток пальца, распознавание лица</li>
                        <li><strong>Push-уведомления:</strong> Подтверждение в приложении</li>
                    </ul>
                </div>
                
                <h4>Как настроить 2FA в популярных соцсетях:</h4>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #ff9800;">ВКонтакте:</h4>
                    <p><strong>Путь:</strong> Настройки → Безопасность → Подтверждение входа → Подключить</p>
                    <p><strong>Варианты:</strong> Код в приложении VK, SMS, резервные коды</p>
                    <p><strong>Рекомендация:</strong> Использовать приложение VK + записать резервные коды</p>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>Instagram:</h4>
                    <p><strong>Путь:</strong> Профиль → Меню → Настройки → Безопасность → Двухфакторная аутентификация</p>
                    <p><strong>Варианты:</strong> Приложение для аутентификации, SMS, WhatsApp</p>
                    <p><strong>Рекомендация:</strong> Приложение для аутентификации (Google Authenticator и аналоги)</p>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">Facebook:</h4>
                    <p><strong>Путь:</strong> Настройки и конфиденциальность → Настройки → Безопасность и вход → Двухфакторная аутентификация</p>
                    <p><strong>Варианты:</strong> Приложение для аутентификации, SMS, аппаратный ключ</p>
                    <p><strong>Рекомендация:</strong> Аппаратный ключ (самый безопасный) или приложение для аутентификации</p>
                </div>
                
                <h4>Резервные коды и восстановление доступа:</h4>
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #d32f2f;"><i class="fas fa-exclamation-circle icon"></i> Важно:</h4>
                    <ul>
                        <li><strong>Сохраните резервные коды:</strong> Распечатайте или запишите в безопасное место</li>
                        <li><strong>Не храните коды на устройстве:</strong> Которое используете для входа</li>
                        <li><strong>Обновите коды после использования:</strong> Генерируйте новые после применения старых</li>
                        <li><strong>Настройте несколько способов восстановления:</strong> Резервный email, телефон, доверенные контакты</li>
                    </ul>
                </div>
                
                <h4>Регулярная проверка безопасности:</h4>
                <ul>
                    <li><strong>Ежемесячно:</strong> Проверка активных сессий</li>
                    <li><strong>Раз в 3 месяца:</strong> Смена важных паролей</li>
                    <li><strong>Раз в 6 месяцев:</strong> Обновление резервных кодов 2FA</li>
                    <li><strong>После утери устройства:</strong> Немедленная смена всех паролей и отзыв доступов</li>
                </ul>`,
            completed: false 
        },
        { 
            title: 'Работа с приложениями и сторонними сервисами', 
            duration: '25 мин',
            content: `<h3>Работа с приложениями и сторонними сервисами</h3>
                <p>Многие социальные сети позволяют подключать сторонние приложения и сервисы, что может значительно повысить удобство использования, но также создает дополнительные риски для безопасности.</p>
                
                <h4>Типы сторонних приложений:</h4>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>1. Игры и развлечения</h4>
                    <p><strong>Примеры:</strong> Игры в социальных сетях, квизы, тесты</p>
                    <p><strong>Риски:</strong> Сбор данных о друзьях, доступ к публикациям, спам от имени пользователя</p>
                    <p><strong>Рекомендации:</strong> Ограничить доступ к минимально необходимому, не использовать приложения от неизвестных разработчиков</p>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>2. Сервисы авторизации</h4>
                    <p><strong>Примеры:</strong> "Войти через ВКонтакте/Facebook/Google" на других сайтах</p>
                    <p><strong>Риски:</strong> Утечка данных при взломе стороннего сервиса, отслеживание активности</p>
                    <p><strong>Рекомендации:</strong> Использовать только для доверенных сервисов, регулярно проверять список подключенных приложений</p>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>3. Инструменты для ведения аккаунтов</h4>
                    <p><strong>Примеры:</strong> Планировщики публикаций, аналитика, автоматизация</p>
                    <p><strong>Риски:</strong> Полный доступ к аккаунту, возможность публикации от имени пользователя</p>
                    <p><strong>Рекомендации:</strong> Использовать только официально одобренные платформой инструменты, предоставлять минимальные необходимые права</p>
                </div>
                
                <h4>Права, которые запрашивают приложения:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Право</th>
                        <th style="padding: 10px; text-align: left;">Что означает</th>
                        <th style="padding: 10px; text-align: left;">Рекомендация</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Доступ к профилю</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Чтение основной информации</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Обычно безопасно</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Доступ к друзьям</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Получение списка друзей и их данных</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Ограничить, если не нужно для работы приложения</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Публикация от имени</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Возможность делать посты на вашей стене</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Только для доверенных инструментов</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Доступ к сообщениям</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Чтение и отправка сообщений</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Очень опасно! Избегать</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Доступ к email</td>
                        <td style="padding: 10px;">Получение адреса электронной почты</td>
                        <td style="padding: 10px;">Ограничить, может использоваться для спама</td>
                    </tr>
                </table>
                
                <h4>Как проверить и управлять подключенными приложениями:</h4>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #388e3c;">ВКонтакте:</h4>
                    <p><strong>Путь:</strong> Настройки → Приложения → "Я разрешаю"</p>
                    <p><strong>Что можно сделать:</strong></p>
                    <ul>
                        <li>Посмотреть список всех разрешенных приложений</li>
                        <li>Увидеть, какие права имеет каждое приложение</li>
                        <li>Отозвать доступ для любого приложения</li>
                        <li>Настроить уведомления о новых подключениях</li>
                    </ul>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>Facebook:</h4>
                    <p><strong>Путь:</strong> Настройки и конфиденциальность → Настройки → Безопасность и вход → Приложения и сайты</p>
                    <p><strong>Особенности:</strong></p>
                    <ul>
                        <li>Просмотр активных приложений и сайтов</li>
                        <li>Управление правами для каждого приложения</li>
                        <li>Просмотр истории активности приложений</li>
                        <li>Настройка уведомлений о новых подключениях</li>
                    </ul>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">Google Аккаунт:</h4>
                    <p><strong>Путь:</strong> Управление аккаунтом Google → Безопасность → Сторонние приложения с доступом к аккаунту</p>
                    <p><strong>Функции:</strong></p>
                    <ul>
                        <li>Детальный контроль прав для каждого сервиса</li>
                        <li>Возможность отзыва отдельных разрешений</li>
                        <li>Просмотр истории доступа</li>
                        <li>Оценка безопасности приложений</li>
                    </ul>
                </div>
                
                <h4>Риски использования сторонних приложений:</h4>
                <div style="background-color: #ffebee; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #d32f2f;">Основные угрозы:</h4>
                    <ol>
                        <li><strong>Утечка данных:</strong> Приложения могут продавать или терять ваши данные</li>
                        <li><strong>Взлом через приложение:</strong> Уязвимость в приложении может дать доступ к вашему аккаунту</li>
                        <li><strong>Спам от вашего имени:</strong> Приложения могут публиковать сообщения без вашего ведома</li>
                        <li><strong>Сбор данных о друзьях:</strong> Даже если вы осторожны, ваши друзья могут предоставить доступ к вашим данным</li>
                        <li><strong>Фишинг через приложения:</strong> Поддельные приложения, имитирующие легитимные</li>
                    </ol>
                </div>
                
                <h4>Правила безопасности при использовании сторонних приложений:</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #ff9800;">Чек-лист безопасности:</h4>
                    <ul>
                        <li>✓ Проверяйте разработчика приложения</li>
                        <li>✓ Читайте отзывы и рейтинги</li>
                        <li>✓ Анализируйте запрашиваемые права (принцип минимальных привилегий)</li>
                        <li>✓ Используйте официальные магазины приложений</li>
                        <li>✓ Регулярно проверяйте список подключенных приложений</li>
                        <li>✓ Удаляйте неиспользуемые приложения</li>
                        <li>✓ Используйте отдельный пароль для важных аккаунтов</li>
                        <li>✓ Включайте двухфакторную аутентификацию</li>
                    </ul>
                </div>
                
                <h4>Примеры опасных ситуаций:</h4>
                
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">СИТУАЦИЯ 1: ПОДДЕЛЬНОЕ ПРИЛОЖЕНИЕ</div>
                    <p><strong>Сценарий:</strong> Приложение "Узнай, кто посещал твой профиль" запрашивает доступ к друзьям и возможность публикации.</p>
                    <p><strong>Опасность:</strong> Такие приложения обычно собирают данные и рассылают спам.</p>
                    <p><strong>Решение:</strong> Не устанавливать, так как соцсети не предоставляют такой информации сторонним приложениям.</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">СИТУАЦИЯ 2: ВЗЛОМ ЧЕРЕЗ ИГРУ</div>
                    <p><strong>Сценарий:</strong> После установки новой игры в соцсети начали приходить жалобы от друзей на спам от вашего имени.</p>
                    <p><strong>Опасность:</strong> Игра получила права на публикацию и использует их для рассылки рекламы.</p>
                    <p><strong>Решение:</strong> Немедленно отозвать доступ приложению и сменить пароль.</p>
                </div>
                
                <h4>Альтернативы сторонним приложениям:</h4>
                <ul>
                    <li><strong>Используйте официальные инструменты</strong> от соцсетей</li>
                    <li><strong>Рассмотрите браузерные расширения</strong> вместо приложений</li>
                    <li><strong>Используйте API напрямую</strong> для разработчиков</li>
                    <li><strong>Создавайте отдельные аккаунты</strong> для тестирования новых сервисов</li>
                </ul>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-history icon"></i> Регулярное обслуживание:</h4>
                    <p>Раз в месяц проводите "чистку" подключенных приложений. Задавайте себе вопросы:</p>
                    <ul>
                        <li>Пользуюсь ли я еще этим приложением?</li>
                        <li>Нужны ли ему все предоставленные права?</li>
                        <li>Есть ли у приложения хорошая репутация?</li>
                        <li>Когда я последний раз его обновлял?</li>
                    </ul>
                </div>`,
            completed: false 
        },
        { 
            title: 'Итоговый тест', 
            duration: '30 мин',
            content: `<h3>Итоговый тест по курсу "Безопасность в социальных сетях"</h3>
                <p>Пройдите тест из 10 вопросов, чтобы проверить свои знания. Для успешного завершения курса нужно правильно ответить на 8 из 10 вопросов (80%).</p>
                
                <div style="text-align: center; margin: 40px 0;">
                    <button class="btn btn-large btn-success" onclick="startSocialTest()">
                        <i class="fas fa-play icon"></i> Начать итоговый тест
                    </button>
                </div>
                
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Информация о тесте:</h4>
                    <ul>
                        <li><strong>10 вопросов</strong> с выбором одного правильного ответа</li>
                        <li><strong>25 минут</strong> на выполнение</li>
                        <li><strong>Проходной балл:</strong> 80% (8 правильных ответов)</li>
                        <li>После теста вы увидите детальные результаты с объяснениями</li>
                        <li>При успешном прохождении получите сертификат</li>
                    </ul>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #388e3c;">Что вы узнали в этом курсе:</h4>
                    <ul>
                        <li>Основы безопасности в социальных сетях и типы угроз</li>
                        <li>Как правильно настраивать приватность и конфиденциальность</li>
                        <li>Методы распознавания фишинга в мессенджерах</li>
                        <li>Создание и управление надежными паролями</li>
                        <li>Безопасную работу с приложениями и сторонними сервисами</li>
                    </ul>
                    <p style="margin-top: 15px; font-weight: bold; text-align: center;">
                        Эти знания помогут вам безопасно пользоваться социальными сетями!
                    </p>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-graduation-cap icon"></i> Советы перед тестом:</h4>
                    <ul>
                        <li>Внимательно читайте вопросы</li>
                        <li>Помните о ключевых правилах безопасности</li>
                        <li>Принцип минимальных привилегий для приложений</li>
                        <li>Важность двухфакторной аутентификации</li>
                        <li>Регулярность проверки настроек безопасности</li>
                    </ul>
                </div>`,
            completed: false 
        }
    ],
    totalLessons: 5,
    totalDuration: '1.5 часа'
},
                'gosuslugi': {
                    title: 'Мошенничество с Госуслугами',
                    icon: 'fa-passport',
                    color: 'gosuslugi',
                    description: 'Научитесь защищать свой аккаунт на портале Госуслуги от мошенников и распознавать поддельные сайты.',
    lessons: [
        { 
            title: 'Как работают мошенники с Госуслугами', 
            duration: '20 мин',
            content: `
                <h3>Как работают мошенники с Госуслугами</h3>
                <p><strong>Государственный портал Госуслуги</strong> — это важный ресурс, содержащий персональные данные миллионов россиян. Мошенники активно используют его для своих атак, так как через Госуслуги можно получить доступ к паспортным данным, ИНН, СНИЛС, водительским удостоверениям и другой конфиденциальной информации.</p>
                
                <h4>Основные цели мошенников:</h4>
                <ul>
                    <li><strong>Кража персональных данных</strong> — паспортных данных, ИНН, СНИЛС</li>
                    <li><strong>Получение доступа к аккаунту</strong> — для изменения настроек или оформления услуг</li>
                    <li><strong>Финансовые махинации</strong> — оформление кредитов на чужое имя</li>
                    <li><strong>Шантаж и вымогательство</strong> — использование полученных данных для угроз</li>
                </ul>
                
                <h4>Схемы работы мошенников:</h4>
                <div class="simulator" style="margin: 20px 0; background-color: #e8f4fd; padding: 20px; border-radius: 10px;">
                    <h4>Пример реальной атаки:</h4>
                    <div class="message-example suspicious">
                        <div class="message-label suspicious">СХЕМА МОШЕННИКОВ</div>
                        <p><strong>1. Сбор данных:</strong> Мошенники покупают базы данных с телефонами и именами (из утечек других сайтов)</p>
                        <p><strong>2. Массовая рассылка:</strong> Отправляют SMS или звонят: "Ваш аккаунт Госуслуг будет заблокирован"</p>
                        <p><strong>3. Фишинговая ссылка:</strong> Предлагают перейти по ссылке для "разблокировки"</p>
                        <p><strong>4. Кража данных:</strong> На поддельном сайте просят ввести логин, пароль и коды подтверждения</p>
                        <p><strong>5. Использование данных:</strong> Получив доступ, оформляют кредиты или продают данные</p>
                    </div>
                </div>
                
                <h4>Почему именно Госуслуги?</h4>
                <ul>
                    <li>Высокая концентрация персональных данных в одном месте</li>
                    <li>Доверие пользователей к государственным порталам</li>
                    <li>Возможность дистанционного оформления документов и услуг</li>
                    <li>Привязка к банковским счетам для оплаты госпошлин</li>
                </ul>
                
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin-top: 20px;">
                    <h4><i class="fas fa-exclamation-triangle icon" style="color: #ff9800;"></i> Важная статистика:</h4>
                    <ul>
                        <li>Более 60% россиян зарегистрированы на Госуслугах</li>
                        <li>Ежедневно фиксируется 500+ попыток мошеннических атак</li>
                        <li>Средний ущерб от успешной атаки — 50-200 тысяч рублей</li>
                        <li>Чаще всего страдают пользователи 25-45 лет</li>
                    </ul>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Поддельные сайты Госуслуг', 
            duration: '25 мин',
            content: `
                <h3>Поддельные сайты Госуслуг</h3>
                <p>Мошенники создают копии официального сайта Госуслуг, которые выглядят практически идентично оригиналу. Различия могут быть настолько незначительными, что их легко не заметить.</p>
                
                <h4>Как создаются поддельные сайты:</h4>
                <ul>
                    <li><strong>Клонирование дизайна</strong> — копируется весь внешний вид официального сайта</li>
                    <li><strong>Создание похожих доменов</strong> — используются домены, похожие на gosuslugi.ru</li>
                    <li><strong>Поддельные сертификаты</strong> — иногда устанавливаются SSL-сертификаты для создания видимости безопасности</li>
                    <li><strong>Динамические страницы</strong> — сайт может выглядеть по-разному для разных пользователей</li>
                </ul>
                
                <h4>Примеры поддельных доменов:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Официальный сайт</th>
                        <th style="padding: 10px; text-align: left;">Поддельный сайт</th>
                        <th style="padding: 10px; text-align: left;">Чем опасен</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">gosuslugi.ru</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">gosuslugi-gov.ru</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Добавление "-gov"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">gosuslugi.ru</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">gosuslugi-online.ru</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Добавление "-online"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">gosuslugi.ru</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">gosuslugi-help.ru</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Добавление "-help"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; color: #388e3c;">gosuslugi.ru</td>
                        <td style="padding: 10px; color: #d32f2f;">gosuslugi-portal.com</td>
                        <td style="padding: 10px;">Изменение доменной зоны (.com вместо .ru)</td>
                    </tr>
                </table>
                
                <h4>Как распознать поддельный сайт:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-check-circle icon"></i> Признаки официального сайта:</h4>
                    <ul>
                        <li><strong>Домен:</strong> ТОЛЬКО gosuslugi.ru</li>
                        <li><strong>Протокол:</strong> Обязательно HTTPS:// (не HTTP://)</li>
                        <li><strong>Замок:</strong> Значок замка в адресной строке</li>
                        <li><strong>Сертификат:</strong> При нажатии на замок — информация о сертификате</li>
                        <li><strong>Орфография:</strong> Отсутствие ошибок в тексте</li>
                    </ul>
                </div>
                
                <div style="background-color: #ffebee; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;"><i class="fas fa-times-circle icon"></i> Признаки поддельного сайта:</h4>
                    <ul>
                        <li>Домен с дополнительными словами или в другой зоне</li>
                        <li>Отсутствие HTTPS или недействительный сертификат</li>
                        <li>Орфографические ошибки в тексте</li>
                        <li>Некачественные изображения или шрифты</li>
                        <li>Слишком навязчивые предупреждения о "блокировке"</li>
                        <li>Требование немедленных действий</li>
                    </ul>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #fff3e0; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-laptop icon" style="color: #ff9800;"></i> Практический пример:</h4>
                    <p>Представьте, что вы получили SMS: "Госуслуги: ваш аккаунт будет заблокирован. Для сохранения доступа перейдите по ссылке: https://gosuslugi-help.ru/unblock"</p>
                    <p><strong>Что не так?</strong></p>
                    <ul>
                        <li>Домен gosuslugi-help.ru вместо gosuslugi.ru</li>
                        <li>Создание искусственной срочности</li>
                        <li>Требование немедленных действий</li>
                    </ul>
                    <p style="color: #d32f2f; font-weight: bold; margin-top: 10px;">✅ Правильное действие: не переходить по ссылке, зайти на официальный сайт напрямую</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Запросы кодов подтверждения', 
            duration: '22 мин',
            content: `
                <h3>Запросы кодов подтверждения</h3>
                <p>Один из самых опасных видов мошенничества с Госуслугами — это запрос кодов подтверждения. Эти коды являются ключом к вашему аккаунту и позволяют выполнять критически важные операции.</p>
                
                <h4>Что такое коды подтверждения?</h4>
                <ul>
                    <li><strong>SMS-коды</strong> — приходят на привязанный к аккаунту номер телефона</li>
                    <li><strong>Коды из приложения</strong> — генерируются в мобильном приложении "Госуслуги"</li>
                    <li><strong>Резервные коды</strong> — статические коды, которые нужно хранить в безопасности</li>
                </ul>
                
                <h4>Для чего используются коды:</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Законное использование:</strong></p>
                    <ul>
                        <li>Вход в аккаунт с нового устройства</li>
                        <li>Подтверждение важных изменений в профиле</li>
                        <li>Оформление государственных услуг</li>
                        <li>Подтверждение оплаты госпошлины</li>
                    </ul>
                </div>
                
                <h4>Схемы мошенников с кодами:</h4>
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА №1: ФИШИНГ</div>
                    <p><strong>SMS:</strong> "Госуслуги: для подтверждения личности введите код из SMS на сайте gosuslugi-verify.ru"</p>
                    <p><strong>Цель:</strong> Получить код для входа в ваш аккаунт</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА №2: ЗВОНОК</div>
                    <p><strong>Звонок:</strong> "Это служба безопасности Госуслуг. Обнаружена попытка взлома. Для защиты назовите код, который мы вам отправили."</p>
                    <p><strong>Цель:</strong> Узнать код для подтверждения операций мошенника</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА №3: ТЕХПОДДЕРЖКА</div>
                    <p><strong>Сообщение:</strong> "Служба поддержки Госуслуг. Для решения проблемы с аккаунтом нужен код из приложения."</p>
                    <p><strong>Цель:</strong> Получить доступ для "помощи", которая обернется кражей</p>
                </div>
                
                <h4>Золотое правило безопасности:</h4>
                <div style="background-color: #fff8e1; padding: 20px; border-radius: 10px; border: 3px solid #ffd600; margin: 20px 0;">
                    <h4 style="color: #ff6f00; text-align: center;">
                        <i class="fas fa-shield-alt icon"></i>
                        НИКОГДА И НИКОМУ НЕ СООБЩАЙТЕ КОДЫ ПОДТВЕРЖДЕНИЯ!
                    </h4>
                    <p style="text-align: center; font-size: 1.1rem; margin-top: 10px;">
                        Настоящие сотрудники Госуслуг <strong>НИКОГДА</strong> не просят назвать коды из SMS или приложения
                    </p>
                </div>
                
                <h4>Что делать, если запрашивают код:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;">Правильный алгоритм действий:</h4>
                    <ol>
                        <li><strong>Не называть код</strong> — ни при каких обстоятельствах</li>
                        <li><strong>Проверить источник</strong> — кто и зачем запрашивает код</li>
                        <li><strong>Зайти на официальный сайт</strong> — gosuslugi.ru напрямую</li>
                        <li><strong>Проверить активность</strong> — в разделе "Безопасность" посмотреть историю входов</li>
                        <li><strong>Сменить пароль</strong> — если есть подозрения</li>
                    </ol>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #ffebee; padding: 25px; border-radius: 10px;">
                    <h4 style="color: #d32f2f;"><i class="fas fa-exclamation-triangle icon"></i> Экстренная ситуация:</h4>
                    <p><strong>Если вы уже сообщили код мошенникам:</strong></p>
                    <ul>
                        <li>Немедленно смените пароль на Госуслугах</li>
                        <li>Отзвонитесь на горячую линию Госуслуг: 8-800-100-70-10</li>
                        <li>Проверьте, не оформлены ли какие-либо услуги без вашего ведома</li>
                        <li>Сообщите в полицию о попытке мошенничества</li>
                    </ul>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Сообщения о "выигрышах"', 
            duration: '18 мин',
            content: `
                <h3>Сообщения о "выигрышах" и "компенсациях"</h3>
                <p>Мошенники часто используют тему денежных выплат, компенсаций и выигрышей, представляясь от имени Госуслуг. Они играют на естественном желании людей получить дополнительные деньги.</p>
                
                <h4>Распространенные схемы:</h4>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА №1: ВЫИГРЫШ В ЛОТЕРЕЕ</div>
                    <p><strong>SMS:</strong> "Поздравляем! Вы выиграли 50,000 руб. в лотерее от Госуслуг. Для получения перейдите по ссылке и оплатите комиссию 500 руб."</p>
                    <p><strong>Реальность:</strong> Госуслуги не проводят лотереи и не раздают деньги</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА №2: КОМПЕНСАЦИЯ</div>
                    <p><strong>Звонок:</strong> "Это социальная служба через Госуслуги. Вам положена компенсация 15,000 руб. за переплату налогов. Для получения оплатите госпошлину 1,000 руб."</p>
                    <p><strong>Реальность:</strong> Все компенсации выплачиваются БЕСПЛАТНО</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СХЕМА №3: ВОЗВРАТ ПЕРЕПЛАТЫ</div>
                    <p><strong>Email:</strong> "Уведомляем о переплате по госпошлинам. Для возврата 2,347 руб. перейдите по ссылке и подтвердите данные карты."</p>
                    <p><strong>Реальность:</strong> Возвраты происходят автоматически на ту же карту</p>
                </div>
                
                <h4>Как работают мошенники:</h4>
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Этапы обмана:</strong></p>
                    <ol>
                        <li><strong>Приманка:</strong> Сообщение о крупной сумме денег</li>
                        <li><strong>Доверие:</strong> Использование имени Госуслуг для авторитетности</li>
                        <li><strong>Условие:</strong> Требование оплатить "комиссию", "пошлину" или "налог"</li>
                        <li><strong>Срочность:</strong> "Действуйте сегодня, иначе выплата сгорит"</li>
                        <li><strong>Повтор:</strong> После первой оплаты могут требовать еще денег</li>
                    </ol>
                </div>
                
                <h4>Правда о выплатах через Госуслуги:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-check-circle icon"></i> Как на самом деле работают выплаты:</h4>
                    <ul>
                        <li><strong>Бесплатно:</strong> Все государственные выплаты бесплатны</li>
                        <li><strong>Официально:</strong> Информация о выплатах есть в личном кабинете</li>
                        <li><strong>Без предоплат:</strong> Не нужно ничего платить заранее</li>
                        <li><strong>На ту же карту:</strong> Возвраты идут на карту, с которой была оплата</li>
                        <li><strong>Без спешки:</strong> У вас есть время на оформление</li>
                    </ul>
                </div>
                
                <h4>Как проверить информацию о выплатах:</h4>
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #1976d2;">Правильная последовательность действий:</h4>
                    <ol>
                        <li><strong>Не переходить по ссылкам</strong> из сообщений</li>
                        <li><strong>Зайти на официальный сайт</strong> gosuslugi.ru</li>
                        <li><strong>Проверить личный кабинет</strong> в разделе "Уведомления"</li>
                        <li><strong>Позвонить на горячую линию</strong> 8-800-100-70-10</li>
                        <li><strong>Обратиться в МФЦ</strong> для консультации</li>
                    </ol>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #fff3e0; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Практическое правило:</h4>
                    <p style="font-size: 1.2rem; font-weight: bold; text-align: center;">
                        Если вам предлагают деньги за то, чтобы вы сначала заплатили — это мошенничество!
                    </p>
                    <p style="text-align: center; margin-top: 10px;">
                        Запомните: <span style="color: #d32f2f; font-weight: bold;">НИКАКИХ ПРЕДОПЛАТ</span> для получения выплат!
                    </p>
                </div>
                
                <h4>Реальные государственные выплаты:</h4>
                <ul>
                    <li><strong>Пенсии и пособия</strong> — оформляются через ПФР или соцзащиту</li>
                    <li><strong>Налоговые вычеты</strong> — через личный кабинет ФНС</li>
                    <li><strong>Материнский капитал</strong> — через ПФР или МФЦ</li>
                    <li><strong>Компенсации ЖКХ</strong> — через соцзащиту</li>
                </ul>
                <p style="margin-top: 10px; color: #666;"><em>Все эти выплаты оформляются БЕСПЛАТНО и информация о них есть в официальных источниках.</em></p>
            `,
            completed: false 
        },
        { 
            title: 'Настройка безопасности аккаунта', 
            duration: '30 мин',
            content: `
                <h3>Настройка безопасности аккаунта Госуслуг</h3>
                <p>Правильная настройка безопасности — лучшая защита от мошенников. В этом уроке вы узнаете, как максимально защитить свой аккаунт на Госуслугах.</p>
                
                <h4>1. Надежный пароль</h4>
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Требования к паролю:</strong></p>
                    <ul>
                        <li><strong>Длина:</strong> Не менее 12 символов</li>
                        <li><strong>Сложность:</strong> Буквы (верхний и нижний регистр), цифры, специальные символы</li>
                        <li><strong>Уникальность:</strong> Не использовать пароль от других сервисов</li>
                        <li><strong>Без личной информации:</strong> Не использовать даты рождения, имена, номера телефонов</li>
                    </ul>
                </div>
                
                <h4>2. Двухфакторная аутентификация (2FA)</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Как настроить:</strong></p>
                    <ol>
                        <li>Зайдите на gosuslugi.ru и авторизуйтесь</li>
                        <li>Перейдите в "Настройки" → "Безопасность"</li>
                        <li>Выберите "Подтверждение входа"</li>
                        <li>Добавьте мобильное приложение "Госуслуги" как способ подтверждения</li>
                        <li>Настройте резервные способы (SMS, email)</li>
                    </ol>
                    <p style="margin-top: 10px; color: #388e3c; font-weight: bold;">✅ Включайте 2FA — это значительно повышает безопасность!</p>
                </div>
                
                <h4>3. Контроль устройств</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Как управлять:</strong></p>
                    <ul>
                        <li>Регулярно проверяйте список доверенных устройств</li>
                        <li>Удаляйте устройства, которыми больше не пользуетесь</li>
                        <li>Включайте уведомления о новых входах</li>
                        <li>Используйте "Выход со всех устройств" при подозрениях</li>
                    </ul>
                    <p><strong>Где найти:</strong> Настройки → Безопасность → Активные сессии</p>
                </div>
                
                <h4>4. Настройка уведомлений</h4>
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Какие уведомления включить:</strong></p>
                    <ul>
                        <li><strong>Вход в аккаунт</strong> — с любого устройства</li>
                        <li><strong>Изменение данных</strong> — смена пароля, email, телефона</li>
                        <li><strong>Оформление услуг</strong> — любые действия в аккаунте</li>
                        <li><strong>Платежи</strong> — оплата госпошлин и услуг</li>
                    </ul>
                    <p><strong>Каналы:</strong> SMS, Email, Push в мобильном приложении</p>
                </div>
                
                <h4>5. Резервные способы восстановления</h4>
                <div style="background-color: #fce4ec; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Что настроить:</strong></p>
                    <ul>
                        <li><strong>Резервный email</strong> — на случай блокировки основного</li>
                        <li><strong>Дополнительный телефон</strong> — для получения кодов</li>
                        <li><strong>Контрольные вопросы</strong> — сложные, известные только вам</li>
                        <li><strong>Резервные коды доступа</strong> — распечатайте и храните в безопасности</li>
                    </ul>
                </div>
                
                <h4>6. Мобильное приложение</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Преимущества приложения:</strong></p>
                    <ul>
                        <li><strong>Биометрическая аутентификация</strong> — отпечаток пальца/Face ID</li>
                        <li><strong>Push-уведомления</strong> — мгновенные оповещения</li>
                        <li><strong>Генератор кодов</strong> — даже без интернета</li>
                        <li><strong>Безопасное хранение</strong> — данные защищены на устройстве</li>
                    </ul>
                    <p><strong>Важно:</strong> Скачивайте приложение ТОЛЬКО из официальных магазинов (App Store, Google Play)</p>
                </div>
                
                <h4>7. Регулярная проверка</h4>
                <div style="background-color: #ffebee; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Что проверять ежемесячно:</strong></p>
                    <ul>
                        <li>Историю входов в аккаунт</li>
                        <li>Список оформленных услуг</li>
                        <li>Платежи и операции</li>
                        <li>Настройки безопасности</li>
                        <li>Активные сессии</li>
                    </ul>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #e3f2fd; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-tasks icon" style="color: #1976d2;"></i> Чек-лист безопасности:</h4>
                    <p><strong>Проверьте, все ли вы настроили:</strong></p>
                    <ul>
                        <li>✓ Надежный уникальный пароль</li>
                        <li>✓ Включена двухфакторная аутентификация</li>
                        <li>✓ Проверены активные сессии и устройства</li>
                        <li>✓ Включены все важные уведомления</li>
                        <li>✓ Настроены резервные способы восстановления</li>
                        <li>✓ Установлено официальное мобильное приложение</li>
                        <li>✓ Регулярно проверяется активность в аккаунте</li>
                    </ul>
                    <p style="margin-top: 15px; text-align: center; font-weight: bold;">
                        Чем больше галочек — тем выше ваша безопасность!
                    </p>
                </div>
                
                <h4>8. Обновление данных</h4>
                <p>Регулярно обновляйте контактные данные в аккаунте (телефон, email), чтобы всегда иметь возможность восстановить доступ.</p>
            `,
            completed: false 
        },
        { 
            title: 'Что делать при подозрениях', 
            duration: '20 мин',
            content: `
                <h3>Что делать при подозрениях на мошенничество</h3>
                <p>Даже при максимальной осторожности можно столкнуться с мошенниками. Важно знать, как действовать в таких ситуациях, чтобы минимизировать ущерб.</p>
                
                <h4>Ситуация 1: Вы перешли по подозрительной ссылке</h4>
                <div style="background-color: #ffebee; padding: 25px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Ваши действия:</strong></p>
                    <ol>
                        <li><strong>НЕ вводите данные</strong> — если страница еще открыта</li>
                        <li><strong>Закройте вкладку</strong> — немедленно</li>
                        <li><strong>Очистите историю браузера</strong> — кэш, cookies</li>
                        <li><strong>Проверьте антивирусом</strong> — компьютер и телефон</li>
                        <li><strong>Смените пароль Госуслуг</strong> — на всякий случай</li>
                    </ol>
                </div>
                
                <h4>Ситуация 2: Вы сообщили данные или коды</h4>
                <div style="background-color: #ffcdd2; padding: 25px; border-radius: 8px; margin: 10px 0; border-left: 5px solid #d32f2f;">
                    <p><strong>СРОЧНЫЕ ДЕЙСТВИЯ:</strong></p>
                    <ol>
                        <li><strong>Немедленно смените пароль</strong> на Госуслугах</li>
                        <li><strong>Включите "Выход со всех устройств"</strong> в настройках безопасности</li>
                        <li><strong>Позвоните на горячую линию госуслуг</strong>
                        <li><strong>Заблокируйте банковские карты</strong>, если сообщали их данные</li>
                        <li><strong>Обратитесь в полицию</strong> с заявлением о мошенничестве</li>
                    </ol>
                </div>
                
                <h4>Ситуация 3: Получили подозрительное сообщение</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Алгоритм проверки:</strong></p>
                    <ol>
                        <li><strong>Сохраните сообщение</strong> — сделайте скриншот</li>
                        <li><strong>Не переходите по ссылкам</strong> и не звоните по указанным номерам</li>
                        <li><strong>Проверьте через официальные каналы</strong> — зайдите на gosuslugi.ru</li>
                        <li><strong>Сообщите о мошенничестве</strong> на горячую линию</li>
                        <li><strong>Предупредите родственников</strong> — они тоже могут получить такое сообщение</li>
                    </ol>
                </div>
                
                <h4>Ситуация 4: Заметили подозрительную активность в аккаунте</h4>
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 8px; margin: 10px 0;">
                    <p><strong>Что проверить:</strong></p>
                    <ul>
                        <li>Историю входов (разные IP-адреса, устройства)</li>
                        <li>Оформленные услуги (незнакомые заявления)</li>
                        <li>Изменения в профиле (телефон, email)</li>
                        <li>Платежи (несанкционированные операции)</li>
                    </ul>
                    <p><strong>Действия:</strong> Если что-то подозрительно — срочно смените пароль и обратитесь в поддержку.</p>
                </div>
                
                <h4>Куда обращаться за помощью:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;">Официальные контакты:</h4>
                    <ul>
                        <li><strong>Горячая линия Госуслуг:</strong> 8-800-100-70-10 (круглосуточно, бесплатно)</li>
                        <li><strong>Техническая поддержка:</strong> support@gosuslugi.ru</li>
                        <li><strong>Обратная связь на сайте:</strong> gosuslugi.ru/feedback</li>
                        <li><strong>МФЦ (Мои документы):</strong> Личная консультация</li>
                        <li><strong>Полиция:</strong> 102 или сайт МВД</li>
                    </ul>
                </div>
                
                <h4>Как составить заявление:</h4>
                <div style="background-color: #f5f5f5; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <p><strong>Что указать в заявлении:</strong></p>
                    <ul>
                        <li>Дата и время инцидента</li>
                        <li>Номер телефона/email от которого пришло сообщение</li>
                        <li>Текст сообщения или суть разговора</li>
                        <li>Ссылка на мошеннический сайт (если есть)</li>
                        <li>Сумма ущерба (если деньги переведены)</li>
                        <li>Ваши контактные данные</li>
                    </ul>
                    <p><strong>Куда подавать:</strong> Отделение полиции или онлайн через сайт МВД.</p>
                </div>
                
                <div class="simulator" style="margin: 20px 0; background-color: #fff3e0; padding: 25px; border-radius: 10px; border: 3px solid #ff9800;">
                    <h4><i class="fas fa-exclamation-triangle icon" style="color: #ff9800;"></i> Экстренные телефоны:</h4>
                    <div style="text-align: center; margin: 15px 0;">
                        <div style="font-size: 1.5rem; font-weight: bold; color: #d32f2f;">
                            8-800-100-70-10
                        </div>
                        <p>Горячая линия Госуслуг</p>
                    </div>
                    <div style="text-align: center; margin: 15px 0;">
                        <div style="font-size: 1.5rem; font-weight: bold; color: #d32f2f;">
                            8-800-222-74-47
                        </div>
                        <p>Киберполиция МВД</p>
                    </div>
                    <p style="text-align: center; margin-top: 15px; font-weight: bold;">
                        Добавьте эти номера в контакты телефона!
                    </p>
                </div>
                
                <h4>Профилактические меры:</h4>
                <ul>
                    <li>Регулярно обучайте родственников, особенно пожилых</li>
                    <li>Установите антивирус на все устройства</li>
                    <li>Используйте менеджер паролей</li>
                    <li>Подпишитесь на официальные каналы Госуслуг в соцсетях</li>
                    <li>Читайте новости о новых схемах мошенников</li>
                </ul>
            `,
            completed: false 
        },
        { 
            title: 'Итоговый тест', 
            duration: '25 мин',
            content: `
                <h3>Итоговый тест по курсу "Мошенничество с Госуслугами"</h3>
                <p>Пройдите тест из 10 вопросов, чтобы проверить свои знания. Для успешного завершения курса нужно правильно ответить на 8 из 10 вопросов (80%).</p>
                
                <div style="text-align: center; margin: 40px 0;">
                    <button class="btn btn-large btn-success" onclick="startGosuslugiTest()">
                        <i class="fas fa-play icon"></i> Начать итоговый тест

                    </button>
                </div>
                
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Информация о тесте:</h4>
                    <ul>
                        <li><strong>10 вопросов</strong> с выбором одного правильного ответа</li>
                        <li><strong>20 минут</strong> на выполнение</li>
                        <li><strong>Проходной балл:</strong> 80% (8 правильных ответов)</li>
                        <li>После теста вы увидите детальные результаты с объяснениями</li>
                        <li>При успешном прохождении получите сертификат</li>
                    </ul>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #388e3c;">Что вы узнали в этом курсе:</h4>
                    <ul>
                        <li>Как работают мошенники с Госуслугами и их основные цели</li>
                        <li>Как распознать поддельные сайты Госуслуг</li>
                        <li>Почему никогда нельзя сообщать коды подтверждения</li>
                        <li>Как отличить мошеннические сообщения о "выигрышах"</li>
                        <li>Как правильно настроить безопасность аккаунта</li>
                        <li>Что делать при подозрениях на мошенничество</li>
                    </ul>
                    <p style="margin-top: 15px; font-weight: bold; text-align: center;">
                        Эти знания помогут защитить ваш аккаунт и персональные данные!
                    </p>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-graduation-cap icon"></i> Советы перед тестом:</h4>
                    <ul>
                        <li>Внимательно читайте вопросы</li>
                        <li>Помните о ключевых правилах безопасности</li>
                        <li>Официальный сайт — ТОЛЬКО gosuslugi.ru</li>
                        <li>Никогда и никому не сообщать коды подтверждения</li>
                        <li>Все государственные выплаты — БЕСПЛАТНЫ</li>
                    </ul>
                </div>
            `,
            completed: false 
        }
    ],
    totalLessons: 7,
    totalDuration: '1.5 часа'
},

                'puu': {
                    title: 'ПУУ схемы и сложные атаки',
                    icon: 'fa-laptop-code',
                    color: 'puu',
                    description: 'Изучите сложные технические схемы мошенничества и защититесь от них.',
    lessons: [
        { 
            title: 'Что такое ПУУ схемы', 
            duration: '20 мин',
            content: `
                <h3>Что такое ПУУ схемы</h3>
                <p><strong>ПУУ (Программа Удаленного Управления)</strong> — это сложные многоуровневые мошеннические схемы, в которых злоумышленники получают удаленный доступ к устройствам жертв с целью хищения денежных средств и конфиденциальных данных.</p>
                
                <h4>Основные характеристики ПУУ-схем:</h4>
                <ul>
                    <li><strong>Техническая сложность:</strong> Использование профессиональных инструментов удаленного доступа</li>
                    <li><strong>Многоэтапность:</strong> Атака развивается по четкому сценарию</li>
                    <li><strong>Социальная инженерия:</strong> Психологическое воздействие на жертву</li>
                    <li><strong>Маскировка под легитимные службы:</strong> Представление техподдержкой, банком, госорганами</li>
                </ul>
                
                <h4>Как работают ПУУ-мошенники:</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ТИПИЧНЫЙ СЦЕНАРИЙ ПУУ</div>
                    <p><strong>1 этап:</strong> Звонок от "техподдержки Microsoft/Windows" о найденных вирусах</p>
                    <p><strong>2 этап:</strong> Убеждение установить программу удаленного доступа (AnyDesk, TeamViewer)</p>
                    <p><strong>3 этап:</strong> Демонстрация "проблем" через удаленный доступ</p>
                    <p><strong>4 этап:</strong> Требование оплаты за "услуги" или доступ к банковским данным</p>
                </div>
                
                <h4>Цели мошенников:</h4>
                <ul>
                    <li><strong>Прямой перевод денег:</strong> Под разными предлогами</li>
                    <li><strong>Кража банковских данных:</strong> Доступ к онлайн-банкам</li>
                    <li><strong>Установка вредоносного ПО:</strong> Шпионские программы, кейлоггеры</li>
                    <li><strong>Шантаж и вымогательство:</strong> Угроза утечки данных</li>
                </ul>
                
                <h4>Статистика ПУУ-атак:</h4>
                <ul>
                    <li>Более 60% успешных атак начинаются с телефонного звонка</li>
                    <li>Средний ущерб от одной атаки: 50-300 тыс. рублей</li>
                    <li>Чаще всего страдают пользователи Windows и macOS</li>
                    <li>Пиковое время атак: рабочие дни с 9:00 до 18:00</li>
                </ul>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4><i class="fas fa-exclamation-triangle icon" style="color: #ff9800;"></i> Важно знать:</h4>
                    <p>Microsoft, Apple, Google и антивирусные компании <strong>НИКОГДА</strong> не звонят пользователям с предложениями технической помощи!</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Удаленный доступ к устройствам', 
            duration: '25 мин',
            content: `
                <h3>Удаленный доступ к устройствам</h3>
                <p>Мошенники используют легитимные программы удаленного доступа для получения контроля над устройствами жертв. Эти же программы используются IT-специалистами для оказания помощи, что делает их идеальной маскировкой.</p>
                
                <h4>Популярные программы, используемые мошенниками:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Программа</th>
                        <th style="padding: 10px; text-align: left;">Как используют мошенники</th>
                        <th style="padding: 10px; text-align: left;">Легитимное применение</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;"><strong>AnyDesk</strong></td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Получение полного контроля, просмотр всех действий</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Удаленная техподдержка</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;"><strong>TeamViewer</strong></td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Доступ к файлам, установка ПО</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Коллаборация, помощь</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;"><strong>Ammyy Admin</strong></td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Обход антивирусов, скрытая установка</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Администрирование сетей</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;"><strong>UltraVNC</strong></td>
                        <td style="padding: 10px;">Полный контроль над системой</td>
                        <td style="padding: 10px;">Удаленное администрирование</td>
                    </tr>
                </table>
                
                <h4>Как мошенники получают доступ:</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ШАГИ МОШЕННИКА</div>
                    <p><strong>1. Установка:</strong> "Для диагностики проблемы нужно установить программу AnyDesk"</p>
                    <p><strong>2. Получение ID:</strong> Мошенник просит сообщить ID подключения</p>
                    <p><strong>3. Подключение:</strong> Установка соединения с устройством жертвы</p>
                    <p><strong>4. Контроль:</strong> Полный доступ к рабочему столу и файлам</p>
                </div>
                
                <h4>Что видит мошенник после подключения:</h4>
                <ul>
                    <li><strong>Весь рабочий стол:</strong> Все открытые окна и программы</li>
                    <li><strong>Файловую систему:</strong> Доступ ко всем дискам и папкам</li>
                    <li><strong>Клавиатурный ввод:</strong> Все, что вы печатаете (пароли, данные карт)</li>
                    <li><strong>Буфер обмена:</strong> Скопированные тексты и данные</li>
                    <li><strong>Веб-камеру и микрофон:</strong> Возможность записи</li>
                </ul>
                
                <h4>Признаки удаленного подключения:</h4>
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #d32f2f;"><i class="fas fa-exclamation-circle icon"></i> Тревожные сигналы:</h4>
                    <ul>
                        <li>Курсор двигается сам по себе</li>
                        <li>Открываются/закрываются программы без вашего участия</li>
                        <li>Появляются неизвестные окна и сообщения</li>
                        <li>Медленная работа компьютера при активном сетевом соединении</li>
                        <li>Индикатор веб-камеры горит без вашего участия</li>
                    </ul>
                </div>
                
                <h4>Как проверить активные подключения:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-shield-alt icon"></i> Методы проверки:</h4>
                    <ul>
                        <li><strong>Windows:</strong> Диспетчер задач → "Пользователи"</li>
                        <li><strong>macOS:</strong> Мониторинг системы</li>
                        <li><strong>Сетевые подключения:</strong> Командная строка → netstat</li>
                        <li><strong>Программы удаленного доступа:</strong> Проверка списка установленных программ</li>
                    </ul>
                </div>
            `,
            completed: false 
        },
       
         { 
            title: 'Социальная инженерия в ПУУ', 
            duration: '30 мин',
            content: `
                <h3>Социальная инженерия в ПУУ</h3>
                <p>Техническая часть ПУУ-схем была бы невозможна без продвинутых методов социальной инженерии. Мошенники используют психологические приемы, чтобы обойти вашу осторожность и заставить добровольно предоставить доступ к устройству.</p>
                
                <h4>Психологические приемы мошенников:</h4>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #d32f2f;">1. Создание авторитета и доверия</h4>
                    <p><strong>Как звучит:</strong> "Говорит старший инженер Microsoft", "Служба безопасности Windows", "Официальный партнер Apple"</p>
                    <p><strong>Цель:</strong> Использование имени крупных компаний для создания доверия</p>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #d32f2f;">2. Страх и срочность</h4>
                    <p><strong>Как звучит:</strong> "Ваш компьютер заражен опасным вирусом!", "Хакеры уже получили доступ!", "Данные будут уничтожены через 10 минут!"</p>
                    <p><strong>Цель:</strong> Вызвать панику, чтобы отключить критическое мышление</p>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #d32f2f;">3. Технический жаргон</h4>
                    <p><strong>Как звучит:</strong> "Обнаружен троян Backdoor.Win32", "Критическая уязвимость в ядре системы", "Руткит активирован в памяти"</p>
                    <p><strong>Цель:</strong> Запутать неопытного пользователя техническими терминами</p>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #d32f2f;">4. Визуальное подтверждение</h4>
                    <p><strong>Как работает:</strong> Через удаленный доступ показывают "доказательства" проблем (поддельные сообщения об ошибках, сгенерированные лог-файлы)</p>
                    <p><strong>Цель:</strong> Визуально убедить в наличии проблемы</p>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #d32f2f;">5. Помощь и забота</h4>
                    <p><strong>Как звучит:</strong> "Я хочу вам помочь", "Мы защитим ваши данные", "Я уже начал исправлять проблему"</p>
                    <p><strong>Цель:</strong> Создать ощущение, что мошенник — ваш союзник</p>
                </div>
                
                <h4>Реальные диалоги с мошенниками:</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ДИАЛОГ 1: ОБНАРУЖЕНИЕ "ВИРУСОВ"</div>
                    <p><strong>Мошенник:</strong> "Это служба безопасности Microsoft. Мы обнаружили, что с вашего IP-адреса идет рассылка вирусов. Ваш компьютер взломан."</p>
                    <p><strong>Жертва:</strong> "Что делать?"</p>
                    <p><strong>Мошенник:</strong> "Я помогу устранить проблему. Откройте сайт anydesk.com и установите программу. Назовите мне ваш ID."</p>
                </div>
                
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ДИАЛОГ 2: "ПРОБЛЕМА С ЛИЦЕНЗИЕЙ"</div>
                    <p><strong>Мошенник:</strong> "Это техническая поддержка Windows. Ваша лицензия Windows заблокирована из-за использования пиратского ПО."</p>
                    <p><strong>Жертва:</strong> "Но у меня лицензионная Windows!"</p>
                    <p><strong>Мошенник:</strong> "Возможно, ошибка системы. Давайте проверим. Установите TeamViewer для диагностики."</p>
                </div>
                
                <h4>Как противостоять социальной инженерии:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-check-circle icon"></i> Правила безопасности:</h4>
                    <ol>
                        <li><strong>Никогда не верьте звонящим "специалистам"</strong> — компании не звонят первыми</li>
                        <li><strong>Требуйте письменных подтверждений</strong> — email с официального домена</li>
                        <li><strong>Проверяйте информацию самостоятельно</strong> — звоните в компании по официальным номерам</li>
                        <li><strong>Не поддавайтесь давлению</strong> — настоящие проблемы не решаются за 5 минут</li>
                        <li><strong>Доверяйте своим антивирусам</strong> — если они молчат, скорее всего, все в порядке</li>
                    </ol>
                </div>
                
                <h4>Вопросы, которые нужно задавать:</h4>
                <ul>
                    <li>"С какого номера я могу перезвонить в вашу компанию?"</li>
                    <li>"Пришлите мне официальное письмо с вашего корпоративного email"</li>
                    <li>"Какой у вас номер служебного удостоверения?"</li>
                    <li>"Дайте мне номер обращения или идентификатор заявки"</li>
                </ul>
            `,
            completed: false 
        },
        { 
            title: 'Многоуровневые атаки', 
            duration: '28 мин',
            content: `
                <h3>Многоуровневые атаки</h3>
                <p>Современные ПУУ-атаки редко ограничиваются простым подключением к компьютеру. Это сложные многоуровневые операции, включающие технические, психологические и финансовые компоненты.</p>
                
                <h4>Этапы сложной ПУУ-атаки:</h4>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #ff9800;">Этап 1: Подготовка и разведка</h4>
                    <ul>
                        <li><strong>Сбор информации:</strong> Получение данных о потенциальной жертве (из соцсетей, утечек)</li>
                        <li><strong>Выбор цели:</strong> Определение уязвимых пользователей (пожилые, неопытные)</li>
                        <li><strong>Подготовка сценария:</strong> Разработка легенды и диалога</li>
                    </ul>
                </div>
                
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;">Этап 2: Установление контакта</h4>
                    <ul>
                        <li><strong>Первичный звонок:</strong> Представление официальным лицом</li>
                        <li><strong>Создание проблемы:</strong> Сообщение о "вирусах", "взломе", "лицензионных проблемах"</li>
                        <li><strong>Психологическое давление:</strong> Создание срочности и страха</li>
                    </ul>
                </div>
                
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;">Этап 3: Техническое проникновение</h4>
                    <ul>
                        <li><strong>Установка ПО удаленного доступа:</strong> AnyDesk, TeamViewer, Ammyy Admin</li>
                        <li><strong>Получение контроля:</strong> Доступ к рабочему столу и файлам</li>
                        <li><strong>Маскировка действий:</strong> Скрытие следов присутствия</li>
                    </ul>
                </div>
                
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;">Этап 4: Эскалация привилегий</h4>
                    <ul>
                        <li><strong>Отключение защиты:</strong> Антивирусов, брандмауэров</li>
                        <li><strong>Установка дополнительного ПО:</strong> Кейлоггеры, бэкдоры</li>
                        <li><strong>Кража данных:</strong> Паролей, cookies, истории браузера</li>
                    </ul>
                </div>
                
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;">Этап 5: Финансовая атака</h4>
                    <ul>
                        <li><strong>Доступ к банковским системам:</strong> Онлайн-банкинг, платежные системы</li>
                        <li><strong>Перевод денег:</strong> На подконтрольные счета</li>
                        <li><strong>Оформление кредитов:</strong> На имя жертвы</li>
                    </ul>
                </div>
                
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;">Этап 6: Сокрытие следов</h4>
                    <ul>
                        <li><strong>Удаление программ удаленного доступа</strong></li>
                        <li><strong>Очистка логов:</strong> Удаление следов активности</li>
                        <li><strong>Блокировка устройств:</strong> Шифрование данных для вымогательства</li>
                    </ul>
                </div>
                
                <h4>Пример сложной атаки:</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">СЛУЧАЙ ИЗ ПРАКТИКИ</div>
                    <p><strong>Жертва:</strong> Владелец малого бизнеса</p>
                    <p><strong>Сценарий:</strong></p>
                    <ol>
                        <li>Звонок от "МВД" о нарушениях в ПО</li>
                        <li>Установка AnyDesk для "проверки"</li>
                        <li>Кража данных для входа в онлайн-банк</li>
                        <li>Перевод 2.5 млн рублей на счета мошенников</li>
                        <li>Установка шифровальщика на все компьютеры фирмы</li>
                        <li>Требование выкупа за расшифровку данных</li>
                    </ol>
                </div>
                
                <h4>Признаки многоуровневой атаки:</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <ul>
                        <li>Несколько последовательных звонков от разных "служб"</li>
                        <li>Требование установить несколько программ</li>
                        <li>Просьбы о предоставлении все большего количества данных</li>
                        <li>Постепенное увеличение сумм "платежей"</li>
                        <li>Угрозы при отказе сотрудничать</li>
                    </ul>
                </div>
                
                <h4>Профилактика многоуровневых атак:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <ol>
                        <li><strong>Обучение сотрудников:</strong> Все, кто работает с техникой</li>
                        <li><strong>Разделение прав доступа:</strong> Банковские операции — отдельные компьютеры</li>
                        <li><strong>Регулярное резервное копирование:</strong> На внешние носители</li>
                        <li><strong>Многофакторная аутентификация:</strong> Для всех критических систем</li>
                        <li><strong>Мониторинг необычной активности:</strong> Необычные входы, переводы</li>
                    </ol>
                </div>
            `,
            completed: false 
        },
                        { 
            title: 'Защита от сложных угроз', 
            duration: '32 мин',
            content: `
                <h3>Защита от сложных угроз</h3>
                <p>Для защиты от продвинутых ПУУ-атак недостаточно простых мер безопасности. Требуется комплексный подход, включающий технические, организационные и психологические меры.</p>
                
                <h4>Технические меры защиты:</h4>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #388e3c;">1. Антивирусная защита нового поколения</h4>
                    <p><strong>Что использовать:</strong> Решения с поведенческим анализом (Kaspersky Endpoint Security, Bitdefender GravityZone)</p>
                    <p><strong>Особенности:</strong> Обнаружение подозрительного поведения программ, блокировка неизвестных приложений</p>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #388e3c;">2. Брандмауэры приложений</h4>
                    <p><strong>Что использовать:</strong> Windows Firewall с расширенными настройками, сторонние решения</p>
                    <p><strong>Особенности:</strong> Контроль сетевой активности каждого приложения, блокировка неавторизованных соединений</p>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #388e3c;">3. Защита от эксплуатации уязвимостей</h4>
                    <p><strong>Что использовать:</strong> EMET (Enhanced Mitigation Experience Toolkit), антиэксплойты</p>
                    <p><strong>Особенности:</strong> Блокировка попыток использования уязвимостей в программном обеспечении</p>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #388e3c;">4. Контроль целостности системы</h4>
                    <p><strong>Что использовать:</strong> Загрузка только подписанных драйверов, Secure Boot</p>
                    <p><strong>Особенности:</strong> Предотвращение модификации системных файлов и загрузки вредоносных драйверов</p>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #388e3c;">5. Изоляция критических процессов</h4>
                    <p><strong>Что использовать:</strong> Виртуализация, песочницы (Sandboxie), контейнеризация</p>
                    <p><strong>Особенности:</strong> Запуск подозрительных программ в изолированной среде</p>
                </div>
                
                <h4>Организационные меры:</h4>
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #1976d2;">Политики безопасности организации:</h4>
                    <ul>
                        <li><strong>Политика установки ПО:</strong> Запрет установки программ без одобрения ИТ-отдела</li>
                        <li><strong>Разделение привилегий:</strong> Пользователи работают без прав администратора</li>
                        <li><strong>Сегментация сети:</strong> Отдельные сегменты для разных отделов</li>
                        <li><strong>Регулярное обучение:</strong> Обязательные курсы по кибербезопасности</li>
                        <li><strong>Инцидент-менеджмент:</strong> Четкие инструкции при подозрениях</li>
                    </ul>
                </div>
                
                <h4>Психологическая подготовка:</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #ff9800;">Формирование "иммунитета":</h4>
                    <ul>
                        <li><strong>Регулярные учения:</strong> Симуляции атак для тренировки реакции</li>
                        <li><strong>Чек-листы:</strong> Пошаговые инструкции при подозрительных звонках</li>
                        <li><strong>Культура отчетности:</strong> Поощрение сообщений о подозрительных ситуациях</li>
                        <li><strong>Осознание ценности данных:</strong> Понимание последствий утечки</li>
                    </ul>
                </div>
                
                <h4>Специализированные средства защиты:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Тип защиты</th>
                        <th style="padding: 10px; text-align: left;">Решение</th>
                        <th style="padding: 10px; text-align: left;">Эффект</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Блокировка удаленного доступа</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">AppLocker, групповые политики</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Запрет запуска AnyDesk, TeamViewer</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Мониторинг процессов</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Sysmon, Process Monitor</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Обнаружение подозрительной активности</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Анализ сетевого трафика</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Wireshark, сетевые IDS</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Выявление команд управления</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Защита браузеров</td>
                        <td style="padding: 10px;">Расширения безопасности, отключение Java/Flash</td>
                        <td style="padding: 10px;">Предотвращение drive-by атак</td>
                    </tr>
                </table>
                
                <h4>План действий при подозрении на атаку:</h4>
                <div style="background-color: #ffebee; padding: 25px; border-radius: 10px; margin: 20px 0; border-left: 5px solid #d32f2f;">
                    <ol>
                        <li><strong>Немедленно отключите компьютер от сети</strong> (выдерните кабель, отключите Wi-Fi)</li>
                        <li><strong>Не выключайте компьютер</strong> (сохраняйте доказательства в памяти)</li>
                        <li><strong>Отключите все банковские карты</strong> и онлайн-банки</li>
                        <li><strong>Сообщите в ИТ-отдел или специалистам</strong></li>
                        <li><strong>Обратитесь в правоохранительные органы</strong></li>
                        <li><strong>Смените все пароли</strong> с другого устройства</li>
                    </ol>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Кейс-анализ реальных атак', 
            duration: '35 мин',
            content: `
                <h3>Кейс-анализ реальных атак</h3>
                <p>Изучение реальных случаев ПУУ-атак помогает понять методы работы мошенников и выработать эффективные меры защиты.</p>
                
                <h4>Кейс 1: Атака на бухгалтерию компании</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ДЕТАЛИ АТАКИ</div>
                    <p><strong>Жертва:</strong> Бухгалтер среднего предприятия (50 сотрудников)</p>
                    <p><strong>Вектор атаки:</strong> Телефонный звонок от "налоговой инспекции"</p>
                    <p><strong>Хронология:</strong></p>
                    <ol>
                        <li><strong>День 1:</strong> Звонок о "проблемах с отчетностью", требование установить программу для проверки</li>
                        <li><strong>День 2:</strong> Установка AnyDesk, "проверка" компьютера</li>
                        <li><strong>День 3:</strong> Кража данных для входа в клиент-банк</li>
                        <li><strong>День 4:</strong> Перевод 3.8 млн рублей на счета мошенников</li>
                    </ol>
                    <p><strong>Ущерб:</strong> 3.8 млн рублей, остановка работы компании на 2 недели</p>
                    <p><strong>Ошибки защиты:</strong> Отсутствие двухфакторной аутентификации, работа бухгалтера с правами администратора</p>
                </div>
                
                <h4>Кейс 2: Целевая атака на ИП</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ДЕТАЛИ АТАКИ</div>
                    <p><strong>Жертва:</strong> Индивидуальный предприниматель (розничная торговля)</p>
                    <p><strong>Вектор атаки:</strong> Email с "уведомлением от банка" о блокировке счета</p>
                    <p><strong>Хронология:</strong></p>
                    <ol>
                        <li>Поддельное письмо от банка со ссылкой на фишинговый сайт</li>
                        <li>Кража логина и пароля от онлайн-банка</li>
                        <li>Последующий звонок от "службы безопасности банка"</li>
                        <li>Установка TeamViewer для "блокировки несанкционированного доступа"</li>
                        <li>Перевод 1.2 млн рублей под видом "перевода на защищенный счет"</li>
                    </ol>
                    <p><strong>Особенность:</strong> Комбинация фишинга и ПУУ-атаки</p>
                    <p><strong>Урок:</strong> Мошенники используют несколько каналов для усиления давления</p>
                </div>
                
                <h4>Кейс 3: Атака через техподдержку ПО</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ДЕТАЛИ АТАКИ</div>
                    <p><strong>Жертва:</strong> Пользователь платного программного обеспечения для дизайна</p>
                    <p><strong>Вектор атаки:</strong> Звонок от "техподдержки Adobe"</p>
                    <p><strong>Сценарий:</strong></p>
                    <ol>
                        <li>Сообщение о "проблемах с лицензией" Photoshop</li>
                        <li>Предложение "бесплатного обновления" для решения проблемы</li>
                        <li>Установка "обновления" (фактически — Ammyy Admin)</li>
                        <li>Кража сохраненных паролей из браузера</li>
                        <li>Вход в аккаунты жертвы на различных сайтах</li>
                    </ol>
                    <p><strong>Особенность:</strong> Использование знаний о реальном ПО пользователя</p>
                    <p><strong>Урок:</strong> Даже знание того, каким ПО вы пользуетесь, может быть использовано против вас</p>
                </div>
                
                <h4>Кейс 4: Многоэтапная атака на юридическую фирму</h4>
                <div class="message-example suspicious" style="margin: 20px 0;">
                    <div class="message-label suspicious">ДЕТАЛИ АТАКИ</div>
                    <p><strong>Жертва:</strong> Юридическая фирма (15 сотрудников)</p>
                    <p><strong>Продолжительность атаки:</strong> 2 недели</p>
                    <p><strong>Этапы:</strong></p>
                    <ol>
                        <li><strong>Неделя 1:</strong> Фишинговые письма сотрудникам с "судебными повестками"</li>
                        <li><strong>День 5:</strong> Звонок секретарю от "судебных приставов"</li>
                        <li><strong>День 7:</strong> Установка AnyDesk на компьютер секретаря</li>
                        <li><strong>Неделя 2:</strong> Изучение структуры сети компании</li>
                        <li><strong>День 12:</strong> Кража данных для доступа к серверу</li>
                        <li><strong>День 14:</strong> Шифрование всех данных и требование выкупа</li>
                    </ol>
                    <p><strong>Ущерб:</strong> Потеря всех данных клиентов, простой 3 недели, репутационный ущерб</p>
                    <p><strong>Урок:</strong> Длительная подготовительная работа мошенников</p>
                </div>
                
                <h4>Анализ общих черт успешных атак:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Фактор</th>
                        <th style="padding: 10px; text-align: left;">Процент атак</th>
                        <th style="padding: 10px; text-align: left;">Рекомендация</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Отсутствие обучения сотрудников</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">85%</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Регулярное обучение кибербезопасности</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Работа с правами администратора</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">78%</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Принцип минимальных привилегий</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Отсутствие резервных копий</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">72%</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Ежедневное резервное копирование</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Нет двухфакторной аутентификации</td>
                        <td style="padding: 10px;">91%</td>
                        <td style="padding: 10px;">Обязательная 2FA для всех систем</td>
                    </tr>
                </table>
                
                <h4>Выводы и рекомендации:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <ol>
                        <li><strong>Обучение — основа защиты:</strong> 85% атак можно предотвратить обучением</li>
                        <li><strong>Технические меры важны, но недостаточны:</strong> Социальная инженерия обходит технические защиты</li>
                        <li><strong>Необходимы регулярные проверки:</strong> Тестирование на проникновение, учения</li>
                        <li><strong>Важен план действий при инциденте:</strong> Четкий алгоритм спасет время и деньги</li>
                        <li><strong>Культура безопасности:</strong> Поощрять сообщения о подозрительных ситуациях</li>
                    </ol>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Настройка защиты устройств', 
            duration: '25 мин',
            content: `
                <h3>Настройка защиты устройств</h3>
                <p>Правильная настройка устройств — критически важный элемент защиты от ПУУ-атак. Рассмотрим пошаговые инструкции для разных операционных систем.</p>
                
                <h4>Защита Windows 10/11:</h4>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">1. Настройка учетных записей</h4>
                    <ul>
                        <li><strong>Создайте учетную запись пользователя без прав администратора</strong></li>
                        <li><strong>Отключите автозапуск с внешних носителей</strong></li>
                        <li><strong>Включите контроль учетных записей (UAC) на максимальный уровень</strong></li>
                    </ul>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">2. Блокировка удаленного доступа</h4>
                    <p><strong>Командная строка (администратор):</strong></p>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
# Запрет установки программ удаленного доступа
reg add "HKLM\\\\SOFTWARE\\\\Policies\\\\Microsoft\\\\Windows\\\\Installer" /v DisableMSI /t REG_DWORD /d 1 /f

# Блокировка TeamViewer
reg add "HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Policies\\\\Explorer" /v DisallowRun /t REG_DWORD /d 1 /f
reg add "HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Policies\\\\Explorer\\\\DisallowRun" /v 1 /t REG_SZ /d "teamviewer.exe" /f</pre>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">3. Настройка брандмауэра Windows</h4>
                    <ul>
                        <li>Заблокируйте все входящие подключения по умолчанию</li>
                        <li>Создайте правила для разрешенных программ</li>
                        <li>Запретите подключения к неизвестным портам</li>
                    </ul>
                </div>
                
                <h4>Защита macOS:</h4>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>1. Настройка Gatekeeper</h4>
                    <p><strong>Терминал:</strong></p>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
# Разрешить установку только из App Store и идентифицированных разработчиков
sudo spctl --master-enable
sudo spctl --enable --label "Mac App Store"
sudo spctl --enable --label "Developer ID"</pre>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>2. Отключение удаленного управления</h4>
                    <p><strong>Системные настройки → Общий доступ:</strong></p>
                    <ul>
                        <li>Отключите "Удаленное управление"</li>
                        <li>Отключите "Общий доступ к экрану"</li>
                        <li>Отключите "Удаленный вход"</li>
                    </ul>
                </div>
                
                <h4>Защита мобильных устройств:</h4>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #ff9800;">Android:</h4>
                    <ul>
                        <li>Запретите установку из неизвестных источников</li>
                        <li>Отключите отладку по USB</li>
                        <li>Используйте Google Play Protect</li>
                        <li>Регулярно обновляйте систему</li>
                    </ul>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>iOS:</h4>
                    <ul>
                        <li>Не используйте джейлбрейк</li>
                        <li>Отключите установку профилей</li>
                        <li>Используйте только App Store</li>
                        <li>Включите автоматические обновления</li>
                    </ul>
                </div>
                
                <h4>Запрет конкретных программ:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Программа</th>
                        <th style="padding: 10px; text-align: left;">Windows</th>
                        <th style="padding: 10px; text-align: left;">macOS</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">AnyDesk</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">AppLocker, групповые политики</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Parental Controls</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">TeamViewer</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Запрет в брандмауэре</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Little Snitch</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Ammyy Admin</td>
                        <td style="padding: 10px;">Запрет запуска .exe</td>
                        <td style="padding: 10px;">Не поддерживается</td>
                    </tr>
                </table>
                
                <h4>Дополнительные меры защиты:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <ol>
                        <li><strong>Регулярное обновление:</strong> Всегда обновляйте ОС и программы</li>
                        <li><strong>Использование антивируса:</strong> С включенным поведенческим анализом</li>
                        <li><strong>Резервное копирование:</strong> Ежедневное на внешний носитель</li>
                        <li><strong>Шифрование дисков:</strong> BitLocker (Windows), FileVault (macOS)</li>
                        <li><strong>Мониторинг событий:</strong> Настройка алертов на подозрительную активность</li>
                    </ol>
                </div>
                
                <h4>Чек-лист настройки безопасности:</h4>
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <ul>
                        <li>✓ Учетная запись без прав администратора</li>
                        <li>✓ UAC включен на максимум</li>
                        <li>✓ Брандмауэр настроен и активен</li>
                        <li>✓ Антивирус с поведенческим анализом</li>
                        <li>✓ Автоматические обновления включены</li>
                        <li>✓ Резервное копирование настроено</li>
                        <li>✓ Диски зашифрованы</li>
                        <li>✓ Удаленный доступ отключен</li>
                    </ul>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Проверка безопасности', 
            duration: '22 мин',
            content: `
                <h3>Проверка безопасности</h3>
                <p>Регулярная проверка безопасности устройств и сетей позволяет выявить уязвимости до того, как ими воспользуются злоумышленники. Рассмотрим методы и инструменты для комплексной проверки.</p>
                
                <h4>Проверка на наличие программ удаленного доступа:</h4>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #1976d2;">Windows — Командная строка:</h4>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
# Проверка установленных программ
wmic product get name,version

# Поиск конкретных программ
wmic product where "name like '%AnyDesk%' or name like '%TeamViewer%'" get name

# Проверка запущенных процессов
tasklist | findstr /i "anydesk teamviewer ammyy"

# Проверка автозагрузки
wmic startup get caption,command</pre>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>macOS — Терминал:</h4>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
# Поиск установленных программ
find /Applications -name "*AnyDesk*" -o -name "*TeamViewer*" -o -name "*Ammyy*"

# Проверка запущенных процессов
ps aux | grep -E -i "anydesk|teamviewer|ammyy"

# Проверка автозагрузки
ls ~/Library/LaunchAgents/
ls /Library/LaunchAgents/
ls /Library/LaunchDaemons/</pre>
                </div>
                
                <h4>Проверка сетевых подключений:</h4>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #388e3c;">Windows — netstat:</h4>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
# Все активные подключения
netstat -ano

# Подключения на определенных портах (TeamViewer обычно 5938)
netstat -ano | findstr ":5938"

# Подключения AnyDesk (порт 7070)
netstat -ano | findstr ":7070"

# Экспорт в файл для анализа
netstat -ano > connections.txt</pre>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4>macOS — lsof:</h4>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
# Проверка сетевых подключений
lsof -i

# Проверка конкретных портов
lsof -i :5938
lsof -i :7070</pre>
                </div>
                
                <h4>Проверка логов системы:</h4>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 8px; margin: 10px 0;">
                    <h4 style="color: #ff9800;">Windows Event Viewer:</h4>
                    <ul>
                        <li><strong>Журналы Windows → Безопасность:</strong> События входа/выхода</li>
                        <li><strong>Журналы Windows → Система:</strong> Установка программ, ошибки</li>
                        <li><strong>Журналы приложений и служб:</strong> Логи конкретных программ</li>
                    </ul>
                    <p><strong>Фильтры для поиска:</strong></p>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
Event ID 4688: Создание процесса
Event ID 4697: Установка службы
Event ID 7045: Установка службы (альтернативный)</pre>
                </div>
                
                <h4>Инструменты для автоматической проверки:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Инструмент</th>
                        <th style="padding: 10px; text-align: left;">Назначение</th>
                        <th style="padding: 10px; text-align: left;">Тип</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Microsoft Safety Scanner</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Быстрая проверка на вредоносное ПО</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Бесплатный</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Malwarebytes AdwCleaner</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Поиск рекламного и шпионского ПО</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Бесплатный</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">GMER</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Обнаружение руткитов</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Бесплатный</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Autoruns</td>
                        <td style="padding: 10px;">Анализ автозагрузки</td>
                        <td style="padding: 10px;">Бесплатный</td>
                    </tr>
                </table>
                
                <h4>Проверка на уровне сети:</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #1976d2;">Сканирование открытых портов:</h4>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
# Использование nmap (установить предварительно)
nmap -sS -p 1-65535 localhost

# Проверка конкретных портов удаленного доступа
nmap -p 5938,7070,80,443,3389 localhost

# Проверка на уязвимости
nmap --script vuln localhost</pre>
                </div>
                
                <h4>Чек-лист регулярной проверки:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;">Ежедневно:</h4>
                    <ul>
                        <li>Проверка запущенных процессов (незнакомые имена)</li>
                        <li>Мониторинг сетевой активности (необычные подключения)</li>
                        <li>Проверка антивирусных отчетов</li>
                    </ul>
                    
                    <h4 style="color: #388e3c; margin-top: 20px;">Еженедельно:</h4>
                    <ul>
                        <li>Проверка установленных программ</li>
                        <li>Анализ логов системы</li>
                        <li>Сканирование на вредоносное ПО</li>
                    </ul>
                    
                    <h4 style="color: #388e3c; margin-top: 20px;">Ежемесячно:</h4>
                    <ul>
                        <li>Полное сканирование системы</li>
                        <li>Проверка обновлений безопасности</li>
                        <li>Аудит учетных записей и прав доступа</li>
                        <li>Тестирование резервных копий</li>
                    </ul>
                </div>
                
                <h4>Что делать при обнаружении подозрительной активности:</h4>
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 20px 0; border-left: 5px solid #d32f2f;">
                    <ol>
                        <li><strong>Немедленно отключите устройство от сети</strong></li>
                        <li><strong>Не удаляйте ничего самостоятельно</strong> (сохраните доказательства)</li>
                        <li><strong>Сделайте снимки экрана</strong> подозрительных окон и процессов</li>
                        <li><strong>Обратитесь к специалистам</strong> (ИТ-отдел, кибербезопасность)</li>
                        <li><strong>Сохраните логи</strong> перед очисткой системы</li>
                    </ol>
                </div>
            `,
            completed: false 
        },
                         { 
            title: 'Аварийные протоколы', 
            duration: '20 мин',
            content: `
                <h3>Аварийные протоколы</h3>
                <p>Даже при идеальной защите нельзя исключать возможность успешной атаки. Наличие четких аварийных протоколов позволит минимизировать ущерб и быстро восстановить работоспособность.</p>
                
                <h4>Протокол 1: Немедленные действия при подозрении</h4>
                <div style="background-color: #ffebee; padding: 25px; border-radius: 10px; margin: 15px 0; border-left: 5px solid #d32f2f;">
                    <h4 style="color: #d32f2f;">ШАГИ В ПЕРВЫЕ 5 МИНУТ:</h4>
                    <ol>
                        <li><strong>Физически отключите интернет:</strong> Выдерните кабель, отключите Wi-Fi</li>
                        <li><strong>Не выключайте компьютер:</strong> Сохраните оперативную память для анализа</li>
                        <li><strong>Отключите все банковские операции:</strong> Позвоните в банки, заблокируйте карты</li>
                        <li><strong>Изолируйте зараженное устройство:</strong> Отключите от локальной сети</li>
                        <li><strong>Сообщите ответственным лицам:</strong> Руководителю, ИТ-отделу, службе безопасности</li>
                    </ol>
                </div>
                
                <h4>Протокол 2: Документирование инцидента</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #ff9800;">ЧТО ЗАФИКСИРОВАТЬ:</h4>
                    <ul>
                        <li><strong>Временная шкала:</strong> Когда начался инцидент, этапы развития</li>
                        <li><strong>Действия мошенников:</strong> Что они делали, что говорили</li>
                        <li><strong>Установленные программы:</strong> Какие программы были установлены</li>
                        <li><strong>Изменения в системе:</strong> Новые файлы, измененные настройки</li>
                        <li><strong>Финансовые операции:</strong> Все переводы и платежи</li>
                    </ul>
                </div>
                
                <h4>Протокол 3: Сбор доказательств</h4>
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #1976d2;">КАК СОБРАТЬ ДОКАЗАТЕЛЬСТВА:</h4>
                    <pre style="background-color: #f5f5f5; padding: 10px; border-radius: 5px; overflow-x: auto;">
# Windows - Сохранение информации о процессах
tasklist /v > processes.txt
wmic process get caption,commandline,processid,parentprocessid > processes_detailed.txt

# Сохранение сетевых подключений
netstat -ano > network_connections.txt

# Сохранение автозагрузки
wmic startup get caption,command,location,user > startup_items.txt

# Копирование логов событий
wevtutil epl Security security_backup.evtx
wevtutil epl System system_backup.evtx</pre>
                </div>
                
                <h4>Протокол 4: Обращение в правоохранительные органы</h4>
                <div style="background-color: #f5f5f5; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4>ЧТО ПОДГОТОВИТЬ ДЛЯ ЗАЯВЛЕНИЯ:</h4>
                    <ul>
                        <li><strong>Паспортные данные</strong> пострадавшего</li>
                        <li><strong>Реквизиты банковских карт</strong> (которые были скомпрометированы)</li>
                        <li><strong>Выписки по счетам</strong> с несанкционированными операциями</li>
                        <li><strong>Номера телефонов</strong> мошенников (если есть)</li>
                        <li><strong>Скриншоты и логи</strong> взаимодействия с мошенниками</li>
                        <li><strong>Данные программ удаленного доступа</strong> (ID сессий, имена файлов)</li>
                    </ul>
                </div>
                
                <h4>Протокол 5: Восстановление системы</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #388e3c;">ПОСЛЕДОВАТЕЛЬНОСТЬ ВОССТАНОВЛЕНИЯ:</h4>
                    <ol>
                        <li><strong>Полное форматирование жесткого диска</strong> (не быстрое, а полное)</li>
                        <li><strong>Установка операционной системы</strong> с оригинального носителя</li>
                        <li><strong>Восстановление из резервной копии</strong> (только данные, не программы)</li>
                        <li><strong>Установка обновлений безопасности</strong></li>
                        <li><strong>Настройка защиты</strong> (антивирус, брандмауэр, обновления)</li>
                        <li><strong>Смена всех паролей</strong> на всех сервисах</li>
                    </ol>
                </div>
                
                <h4>Протокол 6: Коммуникация при инциденте</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #ff9800;">КТО И ЧТО ДОЛЖЕН ЗНАТЬ:</h4>
                    <table style="width: 100%; border-collapse: collapse;">
                        <tr style="background-color: #f5f5f5;">
                            <th style="padding: 8px; text-align: left;">Кому сообщать</th>
                            <th style="padding: 8px; text-align: left;">Что сообщать</th>
                            <th style="padding: 8px; text-align: left;">Сроки</th>
                        </tr>
                        <tr>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">Руководство</td>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">Факт атаки, предварительный ущерб</td>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">В течение 30 минут</td>
                        </tr>
                        <tr>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">ИТ-отдел</td>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">Детали атаки, затронутые системы</td>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">Немедленно</td>
                        </tr>
                        <tr>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">Банки</td>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">Блокировка счетов, карт</td>
                            <td style="padding: 8px; border-bottom: 1px solid #ddd;">В течение 15 минут</td>
                        </tr>
                        <tr>
                            <td style="padding: 8px;">Правоохранительные органы</td>
                            <td style="padding: 8px;">Заявление с полным пакетом документов</td>
                            <td style="padding: 8px;">В течение 24 часов</td>
                        </tr>
                    </table>
                </div>
                
                <h4>Протокол 7: Пост-инцидентный анализ</h4>
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #1976d2;">АНАЛИЗ ПРИЧИН И УРОКИ:</h4>
                    <ul>
                        <li><strong>Root Cause Analysis:</strong> Что позволило атаке состояться?</li>
                        <li><strong>Анализ временной шкалы:</strong> Когда можно было остановить атаку?</li>
                        <li><strong>Оценка ущерба:</strong> Финансового, репутационного, операционного</li>
                        <li><strong>Разработка корректирующих действий:</strong> Что изменить в защите?</li>
                        <li><strong>Обновление процедур:</strong> Включение новых сценариев в обучение</li>
                    </ul>
                </div>
                
                <h4>Контакты экстренных служб:</h4>
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 20px 0; text-align: center;">
                    <h4 style="color: #d32f2f;">ВАЖНЫЕ ТЕЛЕФОНЫ:</h4>
                    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin-top: 15px;">
                        <div>
                            <div style="font-size: 1.5rem; font-weight: bold; color: #d32f2f;">112</div>
                            <div>Единая служба спасения</div>
                        </div>
                        <div>
                            <div style="font-size: 1.5rem; font-weight: bold; color: #d32f2f;">102</div>
                            <div>Полиция</div>
                        </div>
                        <div>
                            <div style="font-size: 1.5rem; font-weight: bold; color: #d32f2f;">8-800-222-74-47</div>
                            <div>Киберполиция МВД</div>
                        </div>
                    </div>
                </div>
                
                <h4>Чек-лист аварийного протокола:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <ul>
                        <li>✓ Протоколы распечатаны и доступны всем сотрудникам</li>
                        <li>✓ Контакты экстренных служб размещены на видном месте</li>
                        <li>✓ Проведены учения по отработке инцидентов</li>
                        <li>✓ Назначены ответственные за каждый этап протокола</li>
                        <li>✓ Регулярно обновляются в соответствии с новыми угрозами</li>
                    </ul>
                </div>
            `,
            completed: false 
        },
        
                         { 
            title: 'Итоговый тест', 
            duration: '30 мин',
            content: `
                <h3>Итоговый тест по курсу "ПУУ схемы и сложные атаки"</h3>
                <p>Пройдите тест из 15 вопросов, чтобы проверить свои знания. Для успешного завершения курса нужно правильно ответить на 12 вопросов (80%).</p>
                
                <div style="text-align: center; margin: 40px 0;">
                    <button class="btn btn-large btn-success" onclick="startPuuTest()">
                        <i class="fas fa-play icon"></i> Начать итоговый тест
                    </button>
                </div>
                
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Информация о тесте:</h4>
                    <ul>
                        <li><strong>15 вопросов</strong> с выбором одного правильного ответа</li>
                        <li><strong>30 минут</strong> на выполнение</li>
                        <li><strong>Проходной балл:</strong> 80% (12 правильных ответов)</li>
                        <li>После теста вы увидите детальные результаты с объяснениями</li>
                        <li>При успешном прохождении получите сертификат</li>
                    </ul>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #388e3c;">Что вы узнали в этом курсе:</h4>
                    <ul>
                        <li>Что такое ПУУ схемы и как они работают</li>
                        <li>Как мошенники получают удаленный доступ к устройствам</li>
                        <li>Методы социальной инженерии в ПУУ-атаках</li>
                        <li>Структуру многоуровневых атак</li>
                        <li>Способы защиты от сложных угроз</li>
                        <li>Анализ реальных случаев атак</li>
                        <li>Настройку защиты устройств</li>
                        <li>Методы проверки безопасности</li>
                        <li>Аварийные протоколы при инцидентах</li>
                    </ul>
                    <p style="margin-top: 15px; font-weight: bold; text-align: center;">
                        Эти знания помогут защитить себя и свою организацию от сложных кибератак!
                    </p>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-graduation-cap icon"></i> Советы перед тестом:</h4>
                    <ul>
                        <li>Внимательно читайте вопросы</li>
                        <li>Помните ключевые признаки ПУУ-атак</li>
                        <li>Microsoft, Apple, Google НИКОГДА не звонят пользователям</li>
                        <li>Никогда не устанавливайте программы по просьбе звонящих</li>
                        <li>При подозрении — немедленно отключайте интернет</li>
                    </ul>
                </div>
            `,
            completed: false 
        }
                    ],
                    totalLessons: 10,
                    totalDuration: '1.5 часа'
                },
// Добавьте этот блок в функцию initCoursesData() после курса 'puu'
'passwords': {
    title: 'Пароли и аутентификация',
    icon: 'fa-key',
    color: 'passwords',
    description: 'Научитесь создавать надежные пароли, использовать менеджеры паролей и двухфакторную аутентификацию с учётом российских реалий.',
    lessons: [
        { 
            title: 'Основы безопасности паролей в России', 
            duration: '15 мин',
            content: `
                <h3>Почему пароли так важны для россиян?</h3>
                <p><strong>Пароль</strong> — это не просто ключ от аккаунта, это защита ваших денег в онлайн-банках, доступ к Госуслугам, и сохранность персональных данных в условиях цифровой трансформации России.</p>
                
                <h4>Особенности российской практики использования паролей:</h4>
                <div style="display: flex; flex-wrap: wrap; gap: 15px; margin: 20px 0;">
                    <div style="flex: 1; min-width: 250px; background-color: #ffebee; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #d32f2f;"><i class="fas fa-exclamation-triangle"></i> Традиционные проблемы в Рунете</h4>
                        <ul>
                            <li><strong>Кириллические пароли</strong> — не все системы корректно обрабатывают</li>
                            <li><strong>Номера телефонов</strong> — часто используются как пароли</li>
                            <li><strong>Паспортные данные</strong> — даты рождения и серии паспортов</li>
                            <li><strong>Простые комбинации</strong> — qwerty, йцукен, 123456</li>
                        </ul>
                    </div>
                    
                    <div style="flex: 1; min-width: 250px; background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #f57c00;"><i class="fas fa-shield-alt"></i> Российские угрозы безопасности</h4>
                        <ul>
                            <li><strong>Целевой фишинг</strong> на Сбербанк, Тинькофф, Госуслуги</li>
                            <li><strong>Социальная инженерия</strong> с использованием паспортных данных</li>
                            <li><strong>Утечки баз данных</strong> российских сервисов</li>
                            <li><strong>SIM-своппинг</strong> для обхода SMS-аутентификации</li>
                        </ul>
                    </div>
                </div>
                
                <h4>Статистика по России, которая вас удивит:</h4>
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px;">
                        <div style="text-align: center; padding: 15px;">
                            <div style="font-size: 2rem; color: #d32f2f; font-weight: bold;">47%</div>
                            <div>россиян используют один пароль для всех аккаунтов</div>
                        </div>
                        <div style="text-align: center; padding: 15px;">
                            <div style="font-size: 2rem; color: #f57c00; font-weight: bold;">73%</div>
                            <div>пользователей российских банков не используют менеджеры паролей</div>
                        </div>
                        <div style="text-align: center; padding: 15px;">
                            <div style="font-size: 2rem; color: #1976d2; font-weight: bold;">28%</div>
                            <div>взломов в России происходит через утечку паролей</div>
                        </div>
                    </div>
                </div>
                
                <h4>Типичные ошибки россиян при создании паролей:</h4>
                <div style="background-color: #e8f4fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-times-circle"></i> Что делают неправильно:</h4>
                    <ul>
                        <li><strong>Использование кириллицы</strong> без учёта кодировок — пароль "пароль" ≠ "password"</li>
                        <li><strong>Номера документов</strong> — серия/номер паспорта, СНИЛС, ИНН</li>
                        <li><strong>Даты в российском формате</strong> — ДД.ММ.ГГГГ легко подобрать</li>
                        <li><strong>Город+год</strong> — москва2024, спб2023</li>
                        <li><strong>Имена на русском</strong> — александр, наталья, сергей</li>
                    </ul>
                </div>
                
                <h4>Юридические аспекты в России:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
                    <thead style="background-color: #5c6bc0; color: white;">
                        <tr>
                            <th style="padding: 12px; text-align: left;">Аспект</th>
                            <th style="padding: 12px; text-align: left;">Правовая база</th>
                            <th style="padding: 12px; text-align: left;">Последствия</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Хранение паролей</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">152-ФЗ "О персональных данных"</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Ответственность оператора</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Утечка данных</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">КоАП РФ ст. 13.11</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Штрафы до 500 000 ₽</td>
                        </tr>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Кража аккаунтов</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">УК РФ ст. 159.6</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Уголовная ответственность</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px;">Банковские пароли</td>
                            <td style="padding: 10px;">ФЗ "О национальной платежной системе"</td>
                            <td style="padding: 10px;">Двойная аутентификация</td>
                        </tr>
                    </tbody>
                </table>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 30px;">
                    <h4 style="color: #388e3c;"><i class="fas fa-lightbulb"></i> Ключевые выводы для россиян:</h4>
                    <ol>
                        <li><strong>Используйте латиницу</strong> — кириллица может не работать в международных сервисах</li>
                        <li><strong>Избегайте персональных данных</strong> — номера документов известны многим организациям</li>
                        <li><strong>Банковские пароли</strong> должны быть самыми сложными</li>
                        <li><strong>Регулярно проверяйте</strong> утечки на российских сервисах</li>
                    </ol>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Создание надежных паролей для российских сервисов', 
            duration: '18 мин',
            content: `
                <h3>Особенности паролей для российских цифровых экосистем</h3>
                <p>Российские сервисы имеют специфические требования и ограничения, которые нужно учитывать при создании паролей.</p>
                
                <h4>Требования популярных российских сервисов:</h4>
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <div style="display: flex; flex-wrap: wrap; gap: 20px;">
                        <div style="flex: 1; min-width: 200px; background-color: #e3f2fd; padding: 20px; border-radius: 8px;">
                            <h4 style="color: #1976d2;"><i class="fas fa-university"></i> Сбербанк Онлайн</h4>
                            <ul>
                                <li>6-20 символов</li>
                                <li>Латиница обязательно</li>
                                <li>Цифры обязательны</li>
                                <li>Блокировка после 5 ошибок</li>
                            </ul>
                        </div>
                        
                        <div style="flex: 1; min-width: 200px; background-color: #fff3e0; padding: 20px; border-radius: 8px;">
                            <h4 style="color: #ff9800;"><i class="fas fa-passport"></i> Госуслуги</h4>
                            <ul>
                                <li>8+ символов</li>
                                <li>Латиница/кириллица</li>
                                <li>2FA обязательно</li>
                                <li>СМС подтверждение</li>
                            </ul>
                        </div>
                        
                        <div style="flex: 1; min-width: 200px; background-color: #fce4ec; padding: 20px; border-radius: 8px;">
                            <h4 style="color: #ad1457;"><i class="fas fa-envelope"></i> Яндекс</h4>
                            <ul>
                                <li>6-30 символов</li>
                                <li>Любые символы</li>
                                <li>Проверка на утечки</li>
                                <li>Резервные email</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <h4>Методы создания паролей с учётом русской ментальности:</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-brain"></i> Учёт культурных особенностей:</h4>
                    
                    <div style="margin: 15px 0;">
                        <h5>1. Метод русских пословиц и поговорок</h5>
                        <p>Использование знакомых фраз с преобразованием:</p>
                        <p><strong>Пословица:</strong> "Волков бояться — в лес не ходить"</p>
                        <p><strong>Преобразование:</strong> Первые буквы слов + замена</p>
                        <p><strong>Результат:</strong> <code>Вбвлнх2024!</code> → <code>Vbvlh2024!</code></p>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>2. Использование отчеств в паролях</h5>
                        <p>Отчества менее предсказуемы, чем имена:</p>
                        <p><strong>Исходные данные:</strong> Петровна, Иванович, Сергеевич</p>
                        <p><strong>Трансформация:</strong> Обратный порядок + символы</p>
                        <p><strong>Результат:</strong> <code>anvorteP@73</code>, <code>hcivonaI#82</code></p>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>3. Города и реки России</h5>
                        <p>Использование географических названий с цифрами:</p>
                        <p><strong>Примеры:</strong> Волга2024!, Байкал#73, Калининград@85</p>
                        <p><strong>Рекомендация:</strong> Добавлять случайные символы между словами</p>
                        <p><strong>Безопасный вариант:</strong> <code>Волга_Байкал_Камчатка#73</code></p>
                    </div>
                </div>
                
                <h4>Криптографическая стойкость русскоязычных паролей:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
                    <thead style="background-color: #7b1fa2; color: white;">
                        <tr>
                            <th style="padding: 12px; text-align: left;">Тип пароля</th>
                            <th style="padding: 12px; text-align: left;">Энтропия (бит)</th>
                            <th style="padding: 12px; text-align: left;">Время взлома</th>
                            <th style="padding: 12px; text-align: left;">Рекомендация</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Русское имя+год</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">~20</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">минуты</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">❌ Избегать</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Номер паспорта</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">~25</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">часы</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">❌ Опасно</td>
                        </tr>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">3 русских слова</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">~38</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">месяцы</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">⚠️ Приемлемо</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px;">4 русских слова+символы</td>
                            <td style="padding: 10px;">~52</td>
                            <td style="padding: 10px;">годы</td>
                            <td style="padding: 10px;">✅ Хорошо</td>
                        </tr>
                    </tbody>
                </table>
                
                <h4>Особенности для российских банков:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-credit-card"></i> Банковские пароли — особая категория:</h4>
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 15px;">
                        <div>
                            <h5>Что НЕЛЬЗЯ использовать:</h5>
                            <ul style="color: #d32f2f;">
                                <li>❌ Номер карты или счета</li>
                                <li>❌ Код из СМС</li>
                                <li>❌ Паспортные данные</li>
                                <li>❌ Даты рождения</li>
                                <li>❌ Простые комбинации</li>
                            </ul>
                        </div>
                        <div>
                            <h5>Что НУЖНО использовать:</h5>
                            <ul style="color: #388e3c;">
                                <li>✅ 12+ случайных символов</li>
                                <li>✅ Разные пароли для карт</li>
                                <li>✅ Обязательная 2FA</li>
                                <li>✅ Менеджер паролей</li>
                                <li>✅ Регулярная проверка</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <h4>Российские генераторы и проверки паролей:</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin-top: 30px;">
                    <h4 style="color: #f57c00;"><i class="fas fa-tools"></i> Инструменты для россиян:</h4>
                    <div style="display: flex; flex-wrap: wrap; gap: 15px; margin-top: 15px;">
                        <div style="flex: 1; min-width: 200px; background-color: #f5f5f5; padding: 25px; border-radius: 8px;">
                            <h5>Генераторы</h5>
                            <ul>
                                <li>Kaspersky Password Manager</li>
                                <li>RU Password Generator</li>
                                <li>Онлайн-генераторы на русском</li>
                            </ul>
                        </div>
                        <div style="flex: 1; min-width: 200px; background-color: #e3f2fd; padding: 25px; border-radius: 8px;">
                            <h5>Проверки</h5>
                            <ul>
                                <li>РОЦИТ — проверка паролей</li>
                                <li>Have I Been Pwned RU</li>
                                <li>Центр цифровой экспертизы</li>
                            </ul>
                        </div>
                    </div>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Менеджеры паролей в российском контексте', 
            duration: '20 мин',
            content: `
                <h3>Выбор и использование менеджеров паролей в России</h3>
                <p>В условиях импортозамещения и особенностей российского законодательства важно правильно выбрать инструмент для хранения паролей.</p>
                
                <h4>Классификация менеджеров паролей для России:</h4>
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-filter"></i> Категории по юрисдикции:</h4>
                    
                    <div style="margin: 20px 0;">
                        <h5>1. Российские разработки 🇷🇺</h5>
                        <p><strong>Преимущества:</strong> Соответствие 152-ФЗ, русская поддержка, локальные серверы</p>
                        <p><strong>Примеры:</strong> Kaspersky Password Manager, MyPassword, RuPass</p>
                        <p><strong>Для кого:</strong> Государственные организации, госкомпании, ценные данные</p>
                    </div>
                    
                    <div style="margin: 20px 0;">
                        <h5>2. Международные с российскими серверами 🌍</h5>
                        <p><strong>Преимущества:</strong> Глобальные стандарты, русский интерфейс</p>
                        <p><strong>Примеры:</strong> Bitwarden (self-hosted), 1Password (бизнес)</p>
                        <p><strong>Для кого:</strong> Бизнес с международными операциями</p>
                    </div>
                    
                    <div style="margin: 20px 0;">
                        <h5>3. Локальные решения 💻</h5>
                        <p><strong>Преимущества:</strong> Полный контроль, офлайн доступ</p>
                        <p><strong>Примеры:</strong> KeePass, Enpass, PassKeep</p>
                        <p><strong>Для кого:</strong> Пользователи, не доверяющие облакам</p>
                    </div>
                </div>
                
                <h4>Сравнение популярных решений в России:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
                    <thead style="background-color: #5c6bc0; color: white;">
                        <tr>
                            <th style="padding: 12px; text-align: left;">Менеджер</th>
                            <th style="padding: 12px; text-align: left;">Цена (руб/мес)</th>
                            <th style="padding: 12px; text-align: left;">Русский язык</th>
                            <th style="padding: 12px; text-align: left;">Серверы в РФ</th>
                            <th style="padding: 12px; text-align: left;">Поддержка 2FA</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Kaspersky</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">300-900 ₽</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">✅ Полностью</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">✅ Да</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">✅ TOTP, SMS</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Bitwarden</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">0-120 ₽</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">✅ Частично</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">⚠️ Self-hosted</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">✅ TOTP, YubiKey</td>
                        </tr>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">1Password</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">250-500 ₽</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">❌ Нет</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">❌ Нет</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">✅ TOTP</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px;">KeePass</td>
                            <td style="padding: 10px;">0 ₽</td>
                            <td style="padding: 10px;">✅ Плагины</td>
                            <td style="padding: 10px;">✅ Локально</td>
                            <td style="padding: 10px;">✅ Плагины</td>
                        </tr>
                    </tbody>
                </table>
                
                <h4>Юридические аспекты хранения паролей в России:</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #f57c00;"><i class="fas fa-gavel"></i> Правовые требования:</h4>
                    
                    <div style="margin: 15px 0;">
                        <h5>152-ФЗ "О персональных данных"</h5>
                        <p><strong>Требования:</strong></p>
                        <ul>
                            <li>Хранение на территории РФ для граждан РФ</li>
                            <li>Согласие на обработку ПДн</li>
                            <li>Уведомление Роскомнадзора</li>
                            <li>Защита от несанкционированного доступа</li>
                        </ul>
                        <p><strong>Вывод:</strong> Для корпоративного использования выбирайте решения с российскими серверами.</p>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>ФЗ "О критической информационной инфраструктуре"</h5>
                        <p><strong>Для организаций КИИ:</strong></p>
                        <ul>
                            <li>Обязательная сертификация СЗИ</li>
                            <li>Требования ФСТЭК и ФСБ</li>
                            <li>Локальное хранение паролей</li>
                            <li>Аудит и мониторинг</li>
                        </ul>
                    </div>
                </div>
                
                <h4>Интеграция с российскими сервисами:</h4>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 20px 0;">
                    <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #388e3c;"><i class="fab fa-yandex"></i> Яндекс экосистема</h4>
                        <ul>
                            <li><strong>Почта</strong> — автоматический вход</li>
                            <li><strong>Диск</strong> — хранение резервных копий</li>
                            <li><strong>Браузер</strong> — интеграция паролей</li>
                            <li><strong>Такси/Лавка</strong> — платежные данные</li>
                        </ul>
                        <p><strong>Рекомендация:</strong> Используйте менеджер, интегрирующийся с Яндекс.Браузер</p>
                    </div>
                    
                    <div style="background-color: #f3e5f5; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #7b1fa2;"><i class="fas fa-mobile-alt"></i> Мобильные приложения РФ</h4>
                        <ul>
                            <li><strong>Госуслуги</strong> — отдельный мастер-пароль</li>
                            <li><strong>Сбербанк</strong> — биометрия + пароль</li>
                            <li><strong>Тинькофф</strong> — PIN + отпечаток</li>
                            <li><strong>ВТБ</strong> — графический ключ</li>
                        </ul>
                        <p><strong>Особенность:</strong> Многие банки не позволяют копировать пароли</p>
                    </div>
                    
                    <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #1976d2;"><i class="fas fa-briefcase"></i> Корпоративные системы</h4>
                        <ul>
                            <li><strong>1С</strong> — отдельные пароли для ролей</li>
                            <li><strong>Контур</strong> — ЭЦП + пароль</li>
                            <li><strong>СБИС</strong> — сертификаты + пароль</li>
                            <li><strong>Диадок</strong> — токены + пароль</li>
                        </ul>
                        <p><strong>Важно:</strong> Для 1С используйте отдельный менеджер</p>
                    </div>
                </div>
                
                <h4>Рекомендации для разных категорий пользователей:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 30px;">
                    <h4 style="color: #388e3c;"><i class="fas fa-users"></i> Кому что подходит:</h4>
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 15px;">
                        <div>
                            <h5>Физические лица</h5>
                            <ul>
                                <li><strong>Начинающие:</strong> Kaspersky (простота)</li>
                                <li><strong>Продвинутые:</strong> Bitwarden (гибкость)</li>
                                <li><strong>Опасающиеся:</strong> KeePass (офлайн)</li>
                                <li><strong>Семейные:</strong> 1Password Families</li>
                            </ul>
                        </div>
                        <div>
                            <h5>Организации</h5>
                            <ul>
                                <li><strong>Малый бизнес:</strong> Bitwarden Teams</li>
                                <li><strong>Средний бизнес:</strong> 1Password Business</li>
                                <li><strong>Госорганизации:</strong> Kaspersky</li>
                                <li><strong>КИИ:</strong> Локальные решения</li>
                            </ul>
                        </div>
                    </div>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Двухфакторная аутентификация в России', 
            duration: '22 мин',
            content: `
                <h3>Особенности 2FA на российских сервисах и правовые аспекты</h3>
                <p>В России двухфакторная аутентификация имеет специфические особенности, связанные с законодательством и практикой использования.</p>
                
                <h4>Типы 2FA, популярные в России:</h4>
                <div style="display: flex; flex-wrap: wrap; gap: 15px; margin: 20px 0;">
                    <div style="flex: 1; min-width: 200px; background-color: #e3f2fd; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #1976d2;">1. SMS-коды 📱</h4>
                        <p><strong>Распространенность:</strong> 95% банков, 80% сервисов</p>
                        <p><strong>Преимущества:</strong> Простота, не требует приложений</p>
                        <p><strong>Риски:</strong> SIM-своппинг, перехват СМС</p>
                        <p><strong>Примеры:</strong> Сбербанк, Тинькофф, Госуслуги</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #ff9800;">2. Push-уведомления 🔔</h4>
                        <p><strong>Распространенность:</strong> 60% банков, 40% сервисов</p>
                        <p><strong>Преимущества:</strong> Удобство, безопасность</p>
                        <p><strong>Риски:</strong> Зависимость от интернета</p>
                        <p><strong>Примеры:</strong> Альфа-Банк, ВТБ, Яндекс</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #e8f5e9; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #388e3c;">3. Биометрия 🖐️</h4>
                        <p><strong>Распространенность:</strong> 70% смартфонов</p>
                        <p><strong>Преимущества:</strong> Максимальное удобство</p>
                        <p><strong>Риски:</strong> Ложные срабатывания</p>
                        <p><strong>Примеры:</strong> Apple Pay/Google Pay, банковские приложения</p>
                    </div>
                </div>
                
                <h4>Правовые требования к 2FA в России:</h4>
                <div style="background-color: #f5f5f5; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-balance-scale"></i> Законодательная база:</h4>
                    
                    <div style="margin: 15px 0;">
                        <h5>ФЗ "О национальной платежной системе" (статья 9)</h5>
                        <p><strong>Требования к банкам:</strong></p>
                        <ul>
                            <li>Обязательная двухфакторная аутентификация для операций</li>
                            <li>Разделение пароля и СМС-кода</li>
                            <li>Лимиты на операции без 2FA</li>
                            <li>Уведомление клиента о всех операциях</li>
                        </ul>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>Указание ЦБ РФ № 5346-У</h5>
                        <p><strong>Требования к дистанционному банковскому обслуживанию:</strong></p>
                        <ul>
                            <li>Минимум два независимых фактора</li>
                            <li>Запрет на передачу кодов третьим лицам</li>
                            <li>Обязательная верификация клиента</li>
                            <li>Протоколирование всех попыток входа</li>
                        </ul>
                    </div>
                </div>
                
                <h4>Риски и защита для российских пользователей:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
                    <thead style="background-color: #d32f2f; color: white;">
                        <tr>
                            <th style="padding: 12px; text-align: left;">Риск</th>
                            <th style="padding: 12px; text-align: left;">Вероятность</th>
                            <th style="padding: 12px; text-align: left;">Защита</th>
                            <th style="padding: 12px; text-align: left;">Пример в России</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">SIM-своппинг</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Высокая</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">PIN-код на SIM, приложения</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Кражи у операторов "большой тройки"</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Социальная инженерия</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Очень высокая</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Обучение, недоверие к звонкам</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Звонки "из банка"</td>
                        </tr>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Мобильные трояны</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Средняя</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Антивирус, официальные магазины</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Вредоносные APK из трекеров</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px;">Фишинг СМС</td>
                            <td style="padding: 10px;">Высокая</td>
                            <td style="padding: 10px;">Проверка отправителя, не переходить по ссылкам</td>
                            <td style="padding: 10px;">СМС "от Сбербанка" с поддельными ссылками</td>
                        </tr>
                    </tbody>
                </table>
                
                <h4>Рекомендации для популярных российских сервисов:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-check-circle"></i> Где и какую 2FA включать:</h4>
                    
                    <div style="margin: 15px 0;">
                        <h5>1. Госуслуги</h5>
                        <p><strong>Доступно:</strong> СМС, приложение, электронная подпись</p>
                        <p><strong>Рекомендуем:</strong> Приложение + резервные коды</p>
                        <p><strong>Важно:</strong> Без 2FA нельзя пользоваться большинством услуг</p>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>2. Сбербанк Онлайн</h5>
                        <p><strong>Доступно:</strong> СМС, Push, биометрия</p>
                        <p><strong>Рекомендуем:</strong> Push + подтверждение по отпечатку</p>
                        <p><strong>Важно:</strong> Включите подтверждение всех операций</p>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>3. Яндекс (почта, диск)</h5>
                        <p><strong>Доступно:</strong> СМС, приложение, резервные коды</p>
                        <p><strong>Рекомендуем:</strong> Яндекс.Ключ + резервные коды на бумаге</p>
                        <p><strong>Важно:</strong> Регулярно обновляйте резервные коды</p>
                    </div>
                </div>
                
                <h4>Инструменты 2FA для России:</h4>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 20px 0;">
                    <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #ff9800;"><i class="fab fa-google"></i> Международные</h4>
                        <ul>
                            <li><strong>Google Authenticator</strong> — бесплатно, без синхронизации</li>
                            <li><strong>Microsoft Authenticator</strong> — облачная синхронизация</li>
                            <li><strong>Authy</strong> — мультиустройство, резервные копии</li>
                            <li><strong>LastPass Authenticator</strong> — интеграция с менеджером</li>
                        </ul>
                    </div>
                    
                    <div style="background-color: #f3e5f5; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #7b1fa2;"><i class="fab fa-yandex"></i> Российские</h4>
                        <ul>
                            <li><strong>Яндекс.Ключ</strong> — для экосистемы Яндекса</li>
                            <li><strong>КриптоПро</strong> — для государственных услуг</li>
                            <li><strong>Домен-Карта</strong> — для юридических лиц</li>
                            <li><strong>RuToken</strong> — аппаратные токены</li>
                        </ul>
                    </div>
                    
                    <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #1976d2;"><i class="fas fa-mobile-alt"></i> Банковские</h4>
                        <ul>
                            <li><strong>Сбербанк Онлайн</strong> — встроенная 2FA</li>
                            <li><strong>Тинькофф</strong> — Push + СМС</li>
                            <li><strong>Альфа-Банк</strong> — Альфа-Клик</li>
                            <li><strong>ВТБ</strong> — мобильный токен</li>
                        </ul>
                    </div>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 30px;">
                    <h4 style="color: #388e3c;"><i class="fas fa-shield-alt"></i> Стратегия 2FA для россиянина:</h4>
                    <ol>
                        <li><strong>Банки</strong> — Push + биометрия (не СМС!)</li>
                        <li><strong>Госуслуги</strong> — Яндекс.Ключ или приложение</li>
                        <li><strong>Почта</strong> — Google/Microsoft Authenticator</li>
                        <li><strong>Соцсети</strong> — приложение аутентификации</li>
                        <li><strong>Резервные коды</strong> — распечатать и хранить в сейфе</li>
                        <li><strong>SIM-карта</strong> — установить PIN-код</li>
                    </ol>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Безопасность паролей в российских организациях', 
            duration: '25 мин',
            content: `
                <h3>Корпоративная безопасность паролей в условиях российского законодательства</h3>
                <p>Российские компании сталкиваются с уникальными вызовами: требования регуляторов, импортозамещение и специфические угрозы.</p>
                
                <h4>Требования российских регуляторов к паролям:</h4>
                <div style="background-color: #f5f5f5; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-university"></i> Нормативные документы:</h4>
                    
                    <div style="margin: 15px 0;">
                        <h5>1. Приказ ФСТЭК № 31 (для ГИС)</h5>
                        <p><strong>Требования к паролям:</strong></p>
                        <ul>
                            <li>Минимум 8 символов (рекомендуется 12)</li>
                            <li>Три категории символов: буквы, цифры, спецсимволы</li>
                            <li>Блокировка после 10 неудачных попыток</li>
                            <li>Смена каждые 90 дней</li>
                            <li>Хранение только в хэшированном виде</li>
                        </ul>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>2. Требования ЦБ РФ для банков</h5>
                        <p><strong>Стандарт СТО БР ИББС:</strong></p>
                        <ul>
                            <li>Разделение административных и пользовательских паролей</li>
                            <li>Обязательная двухфакторная аутентификация</li>
                            <li>Аудит всех операций с паролями</li>
                            <li>Шифрование при передаче и хранении</li>
                        </ul>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>3. 152-ФЗ для обработчиков ПДн</h5>
                        <p><strong>Обязательно:</strong></p>
                        <ul>
                            <li>Средства криптографической защиты информации (СКЗИ)</li>
                            <li>Сертифицированные ФСБ средства</li>
                            <li>Локальное хранение паролей граждан РФ</li>
                            <li>Уведомление Роскомнадзора об утечках в течение 24 часов</li>
                        </ul>
                    </div>
                </div>
                
                <h4>Российские корпоративные решения:</h4>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 20px 0;">
                    <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #1976d2;"><i class="fas fa-lock"></i> PAM-системы (Россия)</h4>
                        <ul>
                            <li><strong>Secret Net Studio</strong> (НТЦ ИТ Роса)</li>
                            <li><strong>Аккорд-АМДЗ</strong> (НПО "Эшелон")</li>
                            <li><strong>СЗИ "Континент"</strong> (Код безопасности)</li>
                            <li><strong>Гарда</strong> (Газинформсервис)</li>
                        </ul>
                        <p><strong>Особенность:</strong> Сертификация ФСТЭК/ФСБ</p>
                    </div>
                    
                    <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #ff9800;"><i class="fas fa-key"></i> Менеджеры паролей (бизнес)</h4>
                        <ul>
                            <li><strong>Kaspersky Password Manager Business</strong></li>
                            <li><strong>Bitwarden Organizations</strong> (self-hosted)</li>
                            <li><strong>Парус-Корпорация</strong> (российская разработка)</li>
                            <li><strong>MyPassword Corporate</strong></li>
                        </ul>
                        <p><strong>Критерий:</strong> Соответствие 152-ФЗ</p>
                    </div>
                    
                    <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #388e3c;"><i class="fas fa-user-shield"></i> IAM-системы</h4>
                        <ul>
                            <li><strong>Active Directory</strong> с русификацией</li>
                            <li><strong>OpenID Connect</strong> российские провайдеры</li>
                            <li><strong>SAML 2.0</strong> для госорганизаций</li>
                            <li><strong>ЕСИА</strong> для интеграции с Госуслугами</li>
                        </ul>
                        <p><strong>Требование:</strong> Поддержка российских СКЗИ</p>
                    </div>
                </div>
                
                <h4>Сценарии защиты для разных типов организаций:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
                    <thead style="background-color: #5c6bc0; color: white;">
                        <tr>
                            <th style="padding: 12px; text-align: left;">Тип организации</th>
                            <th style="padding: 12px; text-align: left;">Требования</th>
                            <th style="padding: 12px; text-align: left;">Решение</th>
                            <th style="padding: 12px; text-align: left;">Бюджет (₽/год)</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Малый бизнес (до 50 чел)</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">152-ФЗ, базовая защита</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Bitwarden Self-hosted</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">50 000-100 000</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Средний бизнес (до 500 чел)</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">152-ФЗ, отраслевые стандарты</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Kaspersky Business + AD</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">300 000-700 000</td>
                        </tr>
                        <tr style="background-color: #f5f5f5;">
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">Крупный бизнес (500+ чел)</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">СТО БР ИББС, PCI DSS</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">PAM + IAM + менеджер</td>
                            <td style="padding: 10px; border-bottom: 1px solid #ddd;">1 000 000+</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px;">Госорганизация</td>
                            <td style="padding: 10px;">Приказ ФСТЭК №31, ГОСТы</td>
                            <td style="padding: 10px;">СКЗИ + российские решения</td>
                            <td style="padding: 10px;">По тендеру</td>
                        </tr>
                    </tbody>
                </table>
                
                <h4>Импортозамещение в сфере безопасности паролей:</h4>
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #f57c00;"><i class="fas fa-exchange-alt"></i> Переход на российские решения:</h4>
                    
                    <div style="margin: 15px 0;">
                        <h5>Этапы импортозамещения:</h5>
                        <ol>
                            <li><strong>Аудит</strong> — оценка текущих решений</li>
                            <li><strong>Выбор</strong> — российские аналоги</li>
                            <li><strong>Пилот</strong> — тестирование в отделе</li>
                            <li><strong>Внедрение</strong> — поэтапный переход</li>
                            <li><strong>Обучение</strong> — сотрудники и ИТ-специалисты</li>
                            <li><strong>Поддержка</strong> — мониторинг и улучшение</li>
                        </ol>
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <h5>Российские аналоги популярных решений:</h5>
                        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-top: 10px;">
                            <div>
                                <h6>Иностранное решение → Российский аналог</h6>
                                <ul>
                                    <li>LastPass → Kaspersky Password Manager</li>
                                    <li>1Password → Парус-Корпорация</li>
                                    <li>CyberArk → Secret Net Studio</li>
                                    <li>Okta → ЕСИА/Госуслуги Business</li>
                                </ul>
                            </div>
                            <div>
                                <h6>Критерии выбора:</h6>
                                <ul>
                                    <li>✅ Сертификация ФСТЭК/ФСБ</li>
                                    <li>✅ Поддержка 152-ФЗ</li>
                                    <li>✅ Русская документация</li>
                                    <li>✅ Локальная поддержка</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                
                <h4>Чек-лист для российских организаций:</h4>
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-clipboard-check"></i> Обязательные меры:</h4>
                    
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 15px;">
                        <div>
                            <h5>Технические меры</h5>
                            <ul>
                                <li>✓ Минимум 12 символов в паролях</li>
                                <li>✓ Обязательная 2FA для админов</li>
                                <li>✓ Шифрование паролей по ГОСТ</li>
                                <li>✓ Аудит всех действий с паролями</li>
                                <li>✓ Резервное копирование баз паролей</li>
                                <li>✓ Защита от перебора и атак</li>
                            </ul>
                        </div>
                        <div>
                            <h5>Организационные меры</h5>
                            <ul>
                                <li>✓ Политика безопасности паролей</li>
                                <li>✓ Регулярное обучение сотрудников</li>
                                <li>✓ План действий при утечках</li>
                                <li>✓ Ответственные за безопасность</li>
                                <li>✓ Регулярные проверки и аудиты</li>
                                <li>✓ Соответствие требованиям регуляторов</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 25px; border-radius: 10px; margin-top: 30px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-graduation-cap"></i> Что узнали в этом курсе:</h4>
                    <ul>
                        <li>✅ Особенности безопасности паролей в России</li>
                        <li>✅ Создание паролей для российских сервисов</li>
                        <li>✅ Выбор менеджеров паролей с учётом законодательства</li>
                        <li>✅ 2FA на российских платформах</li>
                        <li>✅ Корпоративная безопасность в условиях РФ</li>
                    </ul>
                    <p style="margin-top: 15px; text-align: center; font-weight: bold;">
                        Эти знания помогут защитить ваши данные в условиях российской цифровой реальности!
                    </p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Итоговый тест', 
            duration: '30 мин',
            content: `
                <h3>Итоговый тест по курсу "Пароли и аутентификация"</h3>
                <p>Пройдите тест из 15 вопросов, чтобы проверить свои знания. Для успешного завершения курса нужно правильно ответить на 12 вопросов (80%).</p>
                
                <div style="text-align: center; margin: 40px 0;">
                    <button class="btn btn-large btn-success" onclick="startPasswordsTest()">
                        <i class="fas fa-play icon"></i> Начать итоговый тест
                    </button>
                </div>
                
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Информация о тесте:</h4>
                    <ul>
                        <li><strong>15 вопросов</strong> с выбором одного правильного ответа</li>
                        <li><strong>30 минут</strong> на выполнение</li>
                        <li><strong>Проходной балл:</strong> 80% (12 правильных ответов)</li>
                        <li>После теста вы увидите детальные результаты с объяснениями</li>
                        <li>При успешном прохождении получите сертификат</li>
                    </ul>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #388e3c;">Что вы узнали в этом курсе:</h4>
                    <ul>
                        <li>Особенности безопасности паролей в российских реалиях</li>
                        <li>Как создавать надежные пароли для российских сервисов</li>
                        <li>Выбор менеджеров паролей с учётом российского законодательства</li>
                        <li>Двухфакторная аутентификация на популярных российских платформах</li>
                        <li>Корпоративная безопасность паролей в условиях РФ</li>
                    </ul>
                    <p style="margin-top: 15px; font-weight: bold; text-align: center;">
                        Эти знания помогут защитить ваши аккаунты в российском цифровом пространстве!
                    </p>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-graduation-cap icon"></i> Советы перед тестом:</h4>
                    <ul>
                        <li>Минимальная длина пароля для банков — 12 символов</li>
                        <li>Используйте разные пароли для российских и международных сервисов</li>
                        <li>Выбирайте менеджеры паролей с учётом 152-ФЗ</li>
                        <li>2FA на Госуслугах обязательна для большинства услуг</li>
                        <li>В организациях учитывайте требования ФСТЭК и ЦБ РФ</li>
                    </ul>
                </div>
            `,
            completed: false 
        }
    ],
    totalLessons: 6,
    totalDuration: '2 часа'
},
'mobile': {
    title: 'Мобильная безопасность',
    icon: 'fa-mobile-alt',
    color: 'mobile',
    description: 'Защитите свой смартфон от мошенников, вирусов и утечки данных. Научитесь безопасно использовать мобильные приложения и банкинг.',
    lessons: [
        { 
            title: 'Основные угрозы для смартфонов', 
            duration: '18 мин',
            content: `
                <h3>Почему смартфон — главная цель мошенников?</h3>
                <p>Современный смартфон содержит больше личной информации, чем домашний компьютер: фото, переписки, банковские данные, доступ к соцсетям и электронной почте.</p>
                
                <h4>Основные угрозы для мобильных устройств:</h4>
                <div style="display: flex; flex-wrap: wrap; gap: 15px; margin: 20px 0;">
                    <div style="flex: 1; min-width: 200px; background-color: #ffebee; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #d32f2f;"><i class="fas fa-virus icon"></i> Вредоносное ПО</h4>
                        <p>Трояны, шпионские программы, рекламное ПО, майнеры</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #f57c00;"><i class="fas fa-user-secret icon"></i> Кража данных</h4>
                        <p>Контакты, фото, пароли, банковская информация</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #e3f2fd; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #1976d2;"><i class="fas fa-sms icon"></i> Смишинг</h4>
                        <p>Фишинг через SMS и мессенджеры</p>
                    </div>
                </div>
                
                <h4>Как мошенники заражают смартфоны:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Метод</th>
                        <th style="padding: 10px; text-align: left;">Процент атак</th>
                        <th style="padding: 10px; text-align: left;">Пример</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Поддельные приложения</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">45%</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">"Антивирус", "Очиститель памяти"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Ссылки в SMS/мессенджерах</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">30%</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">"Вы выиграли приз", "Ваш заказ готов"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Поддельные обновления</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">15%</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">"Обновите Flash Player"</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Зараженные сайты</td>
                        <td style="padding: 10px;">10%</td>
                        <td style="padding: 10px;">Взломанные сайты с эксплойтами</td>
                    </tr>
                </table>
                
                <h4>Статистика мобильных угроз:</h4>
                <ul>
                    <li>Ежедневно обнаруживается 350,000 новых вредоносных программ для Android</li>
                    <li>Более 60% пользователей хоть раз устанавливали подозрительное приложение</li>
                    <li>Средний ущерб от мобильного мошенничества — 15,000 рублей</li>
                    <li>Только 35% пользователей используют антивирус на смартфонах</li>
                </ul>
            `,
            completed: false 
        },
        { 
            title: 'Безопасная установка приложений', 
            duration: '22 мин',
            content: `
                <h3>Как отличить легитимное приложение от мошеннического?</h3>
                <p>Официальные магазины приложений ежедневно блокируют сотни вредоносных программ, но некоторые все равно проходят фильтры.</p>
                
                <h4>Признаки подозрительных приложений:</h4>
                <div style="background-color: #ffebee; padding: 20px; border-radius: 10px; margin: 15px 0;">
                    <h4 style="color: #d32f2f;"><i class="fas fa-exclamation-triangle icon"></i> ОПАСНЫЕ ПРИЗНАКИ:</h4>
                    <ul>
                        <li><strong>Слишком много разрешений</strong> — зачем фонарику доступ к контактам?</li>
                        <li><strong>Ошибки в описании</strong> — плохой перевод, орфографические ошибки</li>
                        <li><strong>Нет информации о разработчике</strong> — сомнительная компания</li>
                        <li><strong>Мало отзывов или фальшивые отзывы</strong> — все отзывы одинаковые</li>
                        <li><strong>Слишком хорошие обещания</strong> — "увеличит скорость в 10 раз"</li>
                    </ul>
                </div>
                
                <h4>Проверка приложения перед установкой:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-check-circle icon"></i> ЧЕК-ЛИСТ БЕЗОПАСНОСТИ:</h4>
                    <ol>
                        <li><strong>Проверьте разработчика</strong> — известная компания или нет?</li>
                        <li><strong>Прочитайте отзывы</strong> — настоящие отзывы или фейковые?</li>
                        <li><strong>Проверьте количество скачиваний</strong> — популярные приложения обычно безопаснее</li>
                        <li><strong>Изучите разрешения</strong> — соответствуют ли функционалу приложения?</li>
                        <li><strong>Дата последнего обновления</strong> — давно не обновлялось = потенциально опасно</li>
                    </ol>
                </div>
                
                <h4>Пример сравнения приложений:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Критерий</th>
                        <th style="padding: 10px; text-align: left;">Безопасное приложение</th>
                        <th style="padding: 10px; text-align: left;">Опасное приложение</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Разработчик</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">Adobe Inc.</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">Adobe Soft Inc.</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Отзывы</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">4.5★ (2.5 млн отзывов)</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">5★ (150 отзывов, все за один день)</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Разрешения</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">Фото/медиа/файлы</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">Контакты, SMS, звонки, местоположение</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Обновление</td>
                        <td style="padding: 10px; color: #388e3c;">2 недели назад</td>
                        <td style="padding: 10px; color: #d32f2f;">2 года назад</td>
                    </tr>
                </table>
                
                <h4>Важные правила установки:</h4>
                <ul>
                    <li>Скачивайте приложения ТОЛЬКО из официальных магазинов (Google Play, App Store)</li>
                    <li>Никогда не устанавливайте приложения из неизвестных источников (apk-файлы)</li>
                    <li>Регулярно обновляйте установленные приложения</li>
                    <li>Удаляйте неиспользуемые приложения</li>
                </ul>
            `,
            completed: false 
        },
        { 
            title: 'Мобильный банкинг и платежи', 
            duration: '25 мин',
            content: `
                <h3>Как безопасно пользоваться мобильным банкингом?</h3>
                <p>Мобильный банк — это удобно, но и опасно. Мошенники создают поддельные приложения и используют различные схемы для кражи денег.</p>
                
                <h4>Основные угрозы мобильного банкинга:</h4>
                <div style="display: flex; flex-wrap: wrap; gap: 15px; margin: 20px 0;">
                    <div style="flex: 1; min-width: 200px; background-color: #ffebee; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #d32f2f;">1. Поддельные приложения банков</h4>
                        <p>Копии официальных приложений с небольшими изменениями в названии или дизайне</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #f57c00;">2. Перехват SMS</h4>
                        <p>Вредоносные программы, которые читают SMS с кодами подтверждения</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #e3f2fd; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #1976d2;">3. Фишинг в мессенджерах</h4>
                        <p>Ссылки на поддельные сайты банков в WhatsApp, Telegram</p>
                    </div>
                </div>
                
                <h4>Как отличить поддельное приложение банка:</h4>
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">ПОДДЕЛЬНОЕ ПРИЛОЖЕНИЕ</div>
                    <p><strong>Название:</strong> Сбербанк Онлайн (с опечаткой или лишним символом)</p>
                    <p><strong>Разработчик:</strong> Sberbank Technologies (вместо AO "Сбербанк")</p>
                    <p><strong>Разрешения:</strong> Требует доступ к SMS, контактам, микрофону</p>
                    <p><strong>Отзывы:</strong> Мало отзывов, все положительные и шаблонные</p>
                </div>
                
                <div class="message-example" style="margin: 15px 0; border-left: 5px solid #388e3c;">
                    <div class="message-label" style="color: #388e3c; border-color: #388e3c;">НАСТОЯЩЕЕ ПРИЛОЖЕНИЕ</div>
                    <p><strong>Название:</strong> Сбербанк Онлайн</p>
                    <p><strong>Разработчик:</strong> AO "Сбербанк"</p>
                    <p><strong>Разрешения:</strong> Только необходимые для работы банка</p>
                    <p><strong>Отзывы:</strong> Миллионы отзывов, разные оценки</p>
                </div>
                
                <h4>Настройки безопасности мобильного банка:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <ol>
                        <li><strong>Включите биометрическую аутентификацию</strong> — отпечаток пальца или Face ID</li>
                        <li><strong>Установите лимиты на операции</strong> — дневные, недельные лимиты</li>
                        <li><strong>Включите уведомления</strong> — о всех операциях по SMS и push</li>
                        <li><strong>Используйте виртуальную клавиатуру</strong> в приложении банка</li>
                        <li><strong>Не сохраняйте пароли</strong> в браузере на телефоне</li>
                    </ol>
                </div>
                
                 <h4>Золотые правила мобильного банкинга:</h4>
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; border: 3px solid #ff9800; margin: 20px 0;">
                    <h4 style="color: #ff6f00; text-align: center;">
                        <i class="fas fa-shield-alt icon"></i>
                        5 НЕЛЬЗЯ ДЛЯ МОБИЛЬНОГО БАНКА
                    </h4>
                    <ol style="margin-top: 15px;">
                        <li><strong>Нельзя</strong> устанавливать приложения банка со сторонних сайтов</li>
                        <li><strong>Нельзя</strong> переходить по ссылкам из SMS о "блокировках" и "обновлениях"</li>
                        <li><strong>Нельзя</strong> называть коды из SMS по телефону</li>
                        <li><strong>Нельзя</strong> пользоваться банком на чужих устройствах</li>
                        <li><strong>Нельзя</strong> использовать публичный Wi-Fi для банковских операций</li>
                    </ol>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Защита данных в публичных сетях', 
            duration: '20 мин',
            content: `
                <h3>Почему публичный Wi-Fi опасен?</h3>
                <p>Бесплатный Wi-Fi в кафе, аэропортах, торговых центрах — это удобно, но крайне опасно. Мошенники могут перехватывать весь ваш трафик.</p>
                
                <h4>Типы атак в публичных сетях:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Атака</th>
                        <th style="padding: 10px; text-align: left;">Как работает</th>
                        <th style="padding: 10px; text-align: left;">Риск</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Man-in-the-Middle</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Перехват данных между вами и сайтом</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">Высокий</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Злые близнецы</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Поддельные точки доступа с похожими названиями</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">Очень высокий</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Пакетный сниффинг</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Анализ всего сетевого трафика</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #f57c00;">Средний</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Сессионный перехват</td>
                        <td style="padding: 10px;">Кража cookies для входа в аккаунты</td>
                        <td style="padding: 10px; color: #f57c00;">Средний</td>
                    </tr>
                </table>
                
                <h4>Пример атаки "Злой близнец":</h4>
                <div class="message-example suspicious" style="margin: 15px 0;">
                    <div class="message-label suspicious">СЦЕНАРИЙ АТАКИ</div>
                    <p>1. Вы в кафе "Кофехауз", ищете Wi-Fi</p>
                    <p>2. Видите сети: <strong>CoffeeHouse_Free</strong> (официальная) и <strong>CoffeeHouse-Free</strong> (мошенническая)</p>
                    <p>3. Подключаетесь к CoffeeHouse-Free, думая, что это официальная сеть</p>
                    <p>4. Все ваши данные (логины, пароли, банковские операции) теперь у мошенника</p>
                </div>
                
                <h4>Как защититься в публичных сетях:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #388e3c;"><i class="fas fa-check-circle icon"></i> ПРАВИЛА БЕЗОПАСНОСТИ:</h4>
                    <ol>
                        <li><strong>Используйте VPN</strong> — шифрует весь трафик</li>
                        <li><strong>Отключите авто-подключение к Wi-Fi</strong> в настройках</li>
                        <li><strong>Проверяйте название сети</strong> с сотрудниками заведения</li>
                        <li><strong>Не делайте покупки и банковские операции</strong> в публичных сетях</li>
                        <li><strong>Используйте мобильный интернет</strong> для важных операций</li>
                        <li><strong>Отключайте Wi-Fi</strong>, когда не используете</li>
                    </ol>
                </div>
                 <h4>Настройки безопасности Wi-Fi на смартфоне:</h4>
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-cog icon"></i> Что отключить в настройках:</h4>
                    <ul>
                        <li>Автоподключение к открытым сетям</li>
                        <li>Определение местоположения через Wi-Fi</li>
                        <li>Уведомления об открытых сетях</li>
                        <li>Функцию Wi-Fi Direct (прямое подключение к устройствам)</li>
                    </ul>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Блокировка и шифрование устройства', 
            duration: '23 мин',
            content: `
                <h3>Что делать, если телефон потерян или украден?</h3>
                <p>По статистике, каждую минуту в мире теряется или крадется 113 смартфонов. Правильная подготовка может спасти ваши данные.</p>
                
                <h4>Методы защиты устройства:</h4>
                <div style="display: flex; flex-wrap: wrap; gap: 15px; margin: 20px 0;">
                    <div style="flex: 1; min-width: 200px; background-color: #e3f2fd; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #1976d2;"><i class="fas fa-lock icon"></i> Блокировка экрана</h4>
                        <p>Пароль, PIN, графический ключ, отпечаток, Face ID</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #e8f5e9; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #388e3c;"><i class="fas fa-key icon"></i> Шифрование</h4>
                        <p>Защита данных на диске даже при физическом доступе</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #ff9800;"><i class="fas fa-map-marker-alt icon"></i> Удаленное управление</h4>
                        <p>Поиск, блокировка, удаление данных на расстоянии</p>
                    </div>
                </div>
                
                <h4>Сравнение методов блокировки:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Метод</th>
                        <th style="padding: 10px; text-align: left;">Безопасность</th>
                        <th style="padding: 10px; text-align: left;">Удобство</th>
                        <th style="padding: 10px; text-align: left;">Рекомендация</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Пароль (6+ символов)</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">Высокая</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #f57c00;">Средняя</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">✅ Рекомендуется</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Отпечаток пальца</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">Высокая</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">Высокая</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">✅ Рекомендуется</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Графический ключ</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #f57c00;">Средняя</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">Высокая</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">⚠️ С осторожностью</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Свайп/нет защиты</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #d32f2f;">Низкая</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd; color: #388e3c;">Очень высокая</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">❌ Запрещено</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">Face ID/распознавание лица</td>
                        <td style="padding: 10px; color: #388e3c;">Высокая</td>
                        <td style="padding: 10px; color: #388e3c;">Очень высокая</td>
                        <td style="padding: 10px;">✅ Рекомендуется</td>
                    </tr>
                </table>
                
                <h4>Настройка удаленного управления:</h4>
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-mobile-alt icon"></i> Для Android (Найти устройство):</h4>
                    <ol>
                        <li>Зайдите в Настройки → Google → Найти устройство</li>
                        <li>Включите "Найти устройство" и "Разрешить удаленную блокировку"</li>
                        <li>Зайдите на android.com/find с другого устройства</li>
                        <li>Войдите в свой Google-аккаунт</li>
                        <li>Вы сможете: позвонить, заблокировать, стереть данные</li>
                    </ol>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fab fa-apple icon"></i> Для iOS (Найти iPhone):</h4>
                    <ol>
                        <li>Зайдите в Настройки → [ваше имя] → Найти iPhone</li>
                        <li>Включите "Найти iPhone" и "Последняя геопозиция"</li>
                        <li>Зайдите на icloud.com/find с другого устройства</li>
                        <li>Войдите в свой Apple ID</li>
                        <li>Вы сможете: включить сигнал, режим пропажи, стереть iPhone</li>
                    </ol>
                </div>
             <h4>Чек-лист защиты телефона:</h4>
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <ul>
                        <li>✓ Сложный пароль/биометрия включена</li>
                        <li>✓ Шифрование данных активировано</li>
                        <li>✓ Удаленное управление настроено</li>
                        <li>✓ Резервные копии делаются регулярно</li>
                        <li>✓ SIM-карта защищена PIN-кодом</li>
                        <li>✓ Номер IMEI записан и сохранен</li>
                    </ul>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Настройка приватности и разрешений', 
            duration: '24 мин',
            content: `
                <h3>Какие данные собирают приложения и как это ограничить?</h3>
                <p>Большинство приложений собирают о вас больше данных, чем нужно для их работы. Утечки этих данных могут привести к мошенничеству.</p>
                
                <h4>Типы данных, которые собирают приложения:</h4>
                <table style="width: 100%; border-collapse: collapse; margin: 15px 0;">
                    <tr style="background-color: #f5f5f5;">
                        <th style="padding: 10px; text-align: left;">Тип данных</th>
                        <th style="padding: 10px; text-align: left;">Примеры приложений</th>
                        <th style="padding: 10px; text-align: left;">Опасность</th>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Контакты</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Соцсети, мессенджеры</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Спам вашим друзьям</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Местоположение</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Карты, погода, такси</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Отслеживание перемещений</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Микрофон/камера</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Видеозвонки, диктофон</td>
                        <td style="padding: 10px; border-bottom: 1px solid #ddd;">Скрытая запись</td>
                    </tr>
                    <tr>
                        <td style="padding: 10px;">SMS/звонки</td>
                        <td style="padding: 10px;">Антиспам, мессенджеры</td>
                        <td style="padding: 10px;">Кража банковских кодов</td>
                    </tr>
                </table>
                
                <h4>Как проверить и настроить разрешения:</h4>
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4 style="color: #1976d2;"><i class="fab fa-android icon"></i> Android (12+):</h4>
                    <ol>
                        <li>Настройки → Приложения → [выберите приложение] → Разрешения</li>
                        <li>Для каждой категории: "Разрешено", "Только при использовании", "Запрещено"</li>
                        <li>Особое внимание: "Точное местоположение" можно заменить на "Приблизительное"</li>
                        <li>Проверьте "Специальный доступ" → "Доступ к уведомлениям"</li>
                    </ol>
                </div>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fab fa-apple icon"></i> iOS (14+):</h4>
                    <ol>
                        <li>Настройки → Конфиденциальность и безопасность</li>
                        <li>Выберите категорию (Камера, Микрофон, Фото и т.д.)</li>
                        <li>Для каждого приложения: "Разрешить", "Спросить", "Запретить"</li>
                        <li>Включите "Запретить отслеживание" в разделе "Отслеживание"</li>
                    </ol>
                </div>
                
                <h4>Пример настройки для популярных приложений:</h4>
                <div style="display: flex; flex-wrap: wrap; gap: 15px; margin: 20px 0;">
                    <div style="flex: 1; min-width: 200px; background-color: #e8f5e9; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #388e3c;">Instagram</h4>
                        <p><strong>Нужно:</strong> Камера, Фото, Микрофон (для сторис)</p>
                        <p><strong>Не нужно:</strong> Контакты, SMS, Местоположение (всегда)</p>
                        <p><strong>Настройка:</strong> Местоположение → Только при использовании</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #fff3e0; padding: 20px; border-radius: 10px;">
                        <h4 style="color: #ff9800;">Такси (Яндекс.Такси)</h4>
                        <p><strong>Нужно:</strong> Местоположение (при вызове)</p>
                        <p><strong>Не нужно:</strong> Контакты, SMS, Камера</p>
                        <p><strong>Настройка:</strong> Отключить фоновое местоположение</p>
                    </div>
                    
                    <div style="flex: 1; min-width: 200px; background-color: #f5f5f5; padding: 20px; border-radius: 10px;">
                        <h4>Игры</h4>
                        <p><strong>Нужно:</strong> Обычно ничего кроме хранилища</p>
                        <p><strong>Не нужно:</strong> Контакты, SMS, Микрофон, Местоположение</p>
                        <p><strong>Настройка:</strong> Запретить все, кроме необходимого</p>
                    </div>
                </div>
                 <h4>Дополнительные меры приватности:</h4>
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <ol>
                        <li><strong>Регулярно чистите историю браузера и cookies</strong></li>
                        <li><strong>Используйте приватный режим браузера</strong> для чувствительных поисков</li>
                        <li><strong>Отключите персонализированную рекламу</strong> в настройках Google/Apple</li>
                        <li><strong>Проверяйте подключенные устройства</strong> в аккаунтах</li>
                        <li><strong>Используйте псевдонимы</strong> для регистрации в неважных сервисах</li>
                    </ol>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #388e3c;">🎉 Поздравляем!</h4>
                    <p>Вы завершили курс "Мобильная безопасность". Теперь вы знаете:</p>
                    <ul>
                        <li>Основные угрозы для смартфонов и как их избежать</li>
                        <li>Как безопасно устанавливать приложения</li>
                        <li>Как защитить мобильный банкинг</li>
                        <li>Правила работы в публичных сетях</li>
                        <li>Как защитить телефон при потере</li>
                        <li>Как настроить приватность и разрешения</li>
                    </ul>
                    <p>Переходите к итоговому тесту, чтобы закрепить знания!</p>
                </div>
            `,
            completed: false 
        },
        { 
            title: 'Итоговый тест', 
            duration: '30 мин',
            content: `
                <h3>Итоговый тест по курсу "Мобильная безопасность"</h3>
                <p>Пройдите тест из 15 вопросов, чтобы проверить свои знания. Для успешного завершения курса нужно правильно ответить на 12 вопросов (80%).</p>
                
                <div style="text-align: center; margin: 40px 0;">
                    <button class="btn btn-large btn-success" onclick="startMobileTest()">
                        <i class="fas fa-play icon"></i> Начать итоговый тест
                    </button>
                </div>
                
                <div style="background-color: #fff3e0; padding: 25px; border-radius: 10px;">
                    <h4><i class="fas fa-lightbulb icon" style="color: #ff9800;"></i> Информация о тесте:</h4>
                    <ul>
                        <li><strong>15 вопросов</strong> с выбором одного правильного ответа</li>
                        <li><strong>30 минут</strong> на выполнение</li>
                        <li><strong>Проходной балл:</strong> 80% (12 правильных ответов)</li>
                        <li>После теста вы увидите детальные результаты с объяснениями</li>
                        <li>При успешном прохождении получите сертификат</li>
                    </ul>
                </div>
                
                <div style="background-color: #e8f5e9; padding: 25px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #388e3c;">Что вы узнали в этом курсе:</h4>
                    <ul>
                        <li>Основные угрозы для мобильных устройств и статистику атак</li>
                        <li>Как проверять приложения перед установкой и на что обращать внимание</li>
                        <li>Безопасность мобильного банкинга и платежей</li>
                        <li>Риски публичных Wi-Fi сетей и методы защиты</li>
                        <li>Способы блокировки и шифрования устройств</li>
                        <li>Настройку приватности и управление разрешениями приложений</li>
                    </ul>
                    <p style="margin-top: 15px; font-weight: bold; text-align: center;">
                        Эти знания помогут защитить ваш смартфон и данные от мошенников!
                    </p>
                </div>
                
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin-top: 20px;">
                    <h4 style="color: #1976d2;"><i class="fas fa-graduation-cap icon"></i> Советы перед тестом:</h4>
                    <ul>
                        <li>Скачивайте приложения только из официальных магазинов</li>
                        <li>Никогда не устанавливайте приложения банков из сторонних источников</li>
                        <li>Не делайте банковские операции в публичных Wi-Fi сетях</li>
                        <li>Всегда используйте блокировку экрана</li>
                        <li>Регулярно проверяйте разрешения приложений</li>
                    </ul>
                </div>
            `,
            completed: false 
        }
    ],
    totalLessons: 7,
    totalDuration: '2.5 часа'
},
            };
        }
        
        // Инициализация данных тренажеров
        function initSimulatorsData() {
            simulators = {
                'phishing-detective': {
                    title: 'Фишинг-детектив',
                    description: 'Определяйте фишинговые письма среди легитимных',
                    progress: 0
                },
                'phone-simulator': {
                    title: 'Телефонный симулятор',
                    description: 'Отрабатывайте правильные реакции на звонки мошенников',
                    progress: 0
                },
                'password-constructor': {
                    title: 'Конструктор паролей',
                    description: 'Создавайте и проверяйте стойкие пароли',
                    progress: 0
                },
                'security-check': {
                    title: 'Проверка безопасности',
                    description: 'Анализируйте настройки безопасности аккаунтов',
                    progress: 0
                },
                'gosuslugi-check': {
                    title: 'Госуслуги: Проверка сайта',
                    description: 'Определяйте поддельные сайты Госуслуг',
                    progress: 0
                },
                'puu-analysis': {
                    title: 'ПУУ: Анализ звонка',
                    description: 'Анализируйте звонки "техподдержки"',
                    progress: 0
                }
            };
        }
        
        // Инициализация кнопки "Наверх"
        function initScrollToTop() {
            const scrollToTopBtn = document.getElementById('scrollToTop');
            
            window.addEventListener('scroll', function() {
                if (window.pageYOffset > 300) {
                    scrollToTopBtn.style.display = 'flex';
                } else {
                    scrollToTopBtn.style.display = 'none';
                }
            });
            
            scrollToTopBtn.addEventListener('click', function() {
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            });
        }
        
        // Инициализация форм
        function initForms() {
            document.getElementById('loginForm').addEventListener('submit', function(e) {
                e.preventDefault();
                loginUser();
            });
            
            document.getElementById('registerForm').addEventListener('submit', function(e) {
                e.preventDefault();
                registerUser();
            });
        }
        
        // Вход пользователя
        function loginUser() {
            const email = document.getElementById('loginEmail').value.trim();
            const password = document.getElementById('loginPassword').value;
            
            clearFormErrors('login');
            
            if (!email) {
                showFormError('loginEmailError', 'Введите email');
                return;
            }
            
            if (!password) {
                showFormError('loginPasswordError', 'Введите пароль');
                return;
            }
            
            const user = users.find(u => u.email === email && u.password === password);
            
            if (user) {
                currentUser = user;
                localStorage.setItem('cyberAcademyCurrentUser', JSON.stringify(user));
                
                closeModal('loginModal');
                showNotification('success', `Добро пожаловать, ${user.name}!`);
                updateUIForLoggedInUser();
                updateProgressBars();
            } else {
                showFormError('loginPasswordError', 'Неверный email или пароль');
            }
        }
        
        // Регистрация пользователя
        function registerUser() {
            const name = document.getElementById('registerName').value.trim();
            const email = document.getElementById('registerEmail').value.trim();
            const password = document.getElementById('registerPassword').value;
            const confirmPassword = document.getElementById('registerConfirmPassword').value;
            
            clearFormErrors('register');
            
            let isValid = true;
            
            if (!name) {
                showFormError('registerNameError', 'Введите имя');
                isValid = false;
            }
            
            if (!email) {
                showFormError('registerEmailError', 'Введите email');
                isValid = false;
            } else if (!isValidEmail(email)) {
                showFormError('registerEmailError', 'Введите корректный email');
                isValid = false;
            } else if (users.some(u => u.email === email)) {
                showFormError('registerEmailError', 'Пользователь с таким email уже существует');
                isValid = false;
            }
            
            if (!password) {
                showFormError('registerPasswordError', 'Введите пароль');
                isValid = false;
            } else if (password.length < 6) {
                showFormError('registerPasswordError', 'Пароль должен быть не менее 6 символов');
                isValid = false;
            }
            
            if (!confirmPassword) {
                showFormError('registerConfirmPasswordError', 'Подтвердите пароль');
                isValid = false;
            } else if (password !== confirmPassword) {
                showFormError('registerConfirmPasswordError', 'Пароли не совпадают');
                isValid = false;
            }
            
            if (!isValid) return;
            
            const newUser = {
                id: generateUserId(),
                name: name,
                email: email,
                password: password,
                registrationDate: new Date().toISOString(),
                stats: {
                    score: 0,
                    completedLessons: 0,
                    completedSimulators: 0,
                    testResults: [],
                    lastActive: new Date().toISOString()
                },
                progress: {
                    phishing: 0,
                    calls: 0,
                    gosuslugi: 0,
                    puu: 0,
                    passwords: 0,
                    social: 0,
                    financial: 0,
                    mobile: 0
                },
                completedCourses: [],
                completedSimulators: [],
                courseProgress: {}
            };
            
            users.push(newUser);
            localStorage.setItem('cyberAcademyUsers', JSON.stringify(users));
            
            currentUser = newUser;
            localStorage.setItem('cyberAcademyCurrentUser', JSON.stringify(newUser));
            
            closeModal('registerModal');
            showNotification('success', `Регистрация успешна! Добро пожаловать, ${name}!`);
            updateUIForLoggedInUser();
        }
        
        // Выход пользователя
        function logoutUser() {
            currentUser = null;
            localStorage.removeItem('cyberAcademyCurrentUser');
            showNotification('info', 'Вы вышли из системы');
            updateUIForLoggedOutUser();
            showPage('home');
        }
        
        // Обновление UI для авторизованного пользователя
        function updateUIForLoggedInUser() {
            const userMenu = document.getElementById('userMenu');
            userMenu.innerHTML = `
                <div class="user-info" onclick="showPage('profile')">
                    <div class="avatar">${currentUser.name.charAt(0).toUpperCase()}</div>
                    <span>${currentUser.name}</span>
                </div>
                <button class="btn btn-danger" onclick="logoutUser()" style="padding: 8px 15px;">
                    <i class="fas fa-sign-out-alt"></i>
                </button>
            `;
            
            document.getElementById('authButtonsContainer').style.display = 'none';
            updateProgressBars();
        }
        
        // Обновление UI для неавторизованного пользователя
        function updateUIForLoggedOutUser() {
            const userMenu = document.getElementById('userMenu');
            userMenu.innerHTML = '';
            document.getElementById('authButtonsContainer').style.display = 'flex';
        }
        
        // Обновление прогресс-баров
function updateProgressBars() {
    if (!currentUser) return;
    
    // Обновляем прогресс тренажеров
    for (let i = 1; i <= 6; i++) {
        const progressElement = document.getElementById(`simulator${i}-progress`);
        const barElement = document.getElementById(`simulator${i}-bar`);
        
        if (progressElement && barElement) {
            const simulatorId = Object.keys(simulators)[i-1];
            
            // Проверяем, пройден ли тренажер
            let progress = 0;
            if (currentUser.completedSimulators && currentUser.completedSimulators.includes(simulatorId)) {
                progress = 100;
            }
            
            progressElement.textContent = `${progress}%`;
            barElement.style.width = `${progress}%`;
            
            // Меняем цвет прогресс-бара при завершении
            if (progress === 100) {
                barElement.style.backgroundColor = 'var(--success-color)';
            } else {
                barElement.style.backgroundColor = ''; // Возвращаем цвет по умолчанию
            }
        }
    }
}
        
        // Показать страницу
        function showPage(pageId) {
 // Прокрутка к началу страницы (ДОБАВЬТЕ ЭТО В НАЧАЛО ФУНКЦИИ)
    setTimeout(() => {
        window.scrollTo({
            top: 0,
            behavior: 'smooth'
        });
    }, 100);
            // Проверка авторизации для защищенных страниц
            const protectedPages = ['courses', 'simulators', 'test', 'profile', 'active-simulator', 'active-course'];
            
            if (protectedPages.includes(pageId) && !currentUser) {
                showNotification('error', 'Для доступа к этому разделу необходимо войти в систему');
                showLoginModal();
                return;
            }
            
            // Прокрутка наверх
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
            
            // Скрыть текущую страницу
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            
            // Показать выбранную страницу
            document.getElementById(pageId).classList.add('active');
            
            // Обновить активную ссылку в навигации
            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active');
            });
            
            // Найти и активировать соответствующую ссылку
            const pageTitles = {
                'home': 'Главная',
                'courses': 'Все курсы',
                'simulators': 'Тренажеры',
                'test': 'Тестирование',
                'profile': 'Профиль'
            };
            
            document.querySelectorAll('.nav-link').forEach(link => {
                if (link.textContent.trim() === pageTitles[pageId]) {
                    link.classList.add('active');
                }
            });
            
            // Закрыть мобильное меню
            document.getElementById('navMenu').classList.remove('active');
            
            currentPage = pageId;
            
            // Загрузить контент страницы
            if (pageId === 'courses') {
                loadCoursesPage();
            } else if (pageId === 'simulators') {
                loadSimulatorsPage();
            } else if (pageId === 'test') {
                loadTestPage();
            } else if (pageId === 'profile') {
                loadProfilePage();
            }
        }
        
        // Загрузка страницы курсов
function loadCoursesPage() {
    const allCoursesTab = document.getElementById('all-courses');
    const beginnerCoursesTab = document.getElementById('beginner-courses');
    const advancedCoursesTab = document.getElementById('advanced-courses');
    const myCoursesTab = document.getElementById('my-courses');
    const myCoursesMessage = document.getElementById('my-courses-message');
    
    // ========== ВКЛАДКА "ВСЕ КУРСЫ" ==========
    let allCoursesContent = '<div class="course-cards">';
    
    Object.keys(courses).forEach(courseId => {
        const course = courses[courseId];
        
        // Получаем прогресс для авторизованных пользователей
        let progress = 0;
        if (currentUser && currentUser.progress && currentUser.progress[courseId] !== undefined) {
            progress = currentUser.progress[courseId];
        }
        
        const isCompleted = progress >= 100;
        
        allCoursesContent += `
            <div class="course-card">
                <div class="course-icon ${course.color}">
                    <i class="fas ${course.icon}"></i>
                </div>
                <h3>${course.title}</h3>
                <p>${course.description.substring(0, 80)}...</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-book"></i>
                        <span>${course.totalLessons} уроков</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>${course.totalDuration}</span>
                    </div>
                </div>
                ${currentUser ? `
                    <div class="progress-container" style="margin-top: 10px;">
                        <div class="progress-label">
                            <span>Прогресс</span>
                            <span>${progress}%</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: ${progress}%;"></div>
                        </div>
                    </div>
                    <button class="btn ${isCompleted ? 'btn-success' : ''}" style="width: 100%; margin-top: 15px;" onclick="startCourse('${courseId}')">
                        ${isCompleted ? '<i class="fas fa-check icon"></i> Курс пройден' : 'Начать курс'}
                    </button>
                ` : `
                    <button class="btn" style="width: 100%; margin-top: 15px;" onclick="showLoginModal()">
                        <i class="fas fa-sign-in-alt icon"></i> Войти для доступа
                    </button>
                `}
            </div>
        `;
    });
    
    allCoursesContent += '</div>';
    allCoursesTab.innerHTML = allCoursesContent;
    
    // ========== ВКЛАДКА "ДЛЯ НАЧИНАЮЩИХ" ==========
    // Список курсов для начинающих
    const beginnerCourses = ['phishing', 'calls', 'gosuslugi', 'passwords', 'social'];
    
    let beginnerCoursesContent = '<div class="course-cards">';
    
    beginnerCourses.forEach(courseId => {
        const course = courses[courseId];
        if (!course) return;
        
        // Получаем прогресс для авторизованных пользователей
        let progress = 0;
        if (currentUser && currentUser.progress && currentUser.progress[courseId] !== undefined) {
            progress = currentUser.progress[courseId];
        }
        
        const isCompleted = progress >= 100;
        
        beginnerCoursesContent += `
            <div class="course-card">
                <div class="course-icon ${course.color}">
                    <i class="fas ${course.icon}"></i>
                </div>
                <h3>${course.title}</h3>
                <p>${course.description.substring(0, 80)}...</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-book"></i>
                        <span>${course.totalLessons} уроков</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>${course.totalDuration}</span>
                    </div>
                </div>
                <div style="margin-bottom: 10px; margin-top: 5px;">
                    <span style="background-color: #4caf50; color: white; padding: 3px 10px; border-radius: 15px; font-size: 12px; font-weight: bold;">
                        <i class="fas fa-star"></i> Для начинающих
                    </span>
                </div>
                ${currentUser ? `
                    <div class="progress-container" style="margin-top: 10px;">
                        <div class="progress-label">
                            <span>Прогресс</span>
                            <span>${progress}%</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: ${progress}%;"></div>
                        </div>
                    </div>
                    <button class="btn ${isCompleted ? 'btn-success' : ''}" style="width: 100%; margin-top: 15px;" onclick="startCourse('${courseId}')">
                        ${isCompleted ? '<i class="fas fa-check icon"></i> Курс пройден' : 'Начать курс'}
                    </button>
                ` : `
                    <button class="btn" style="width: 100%; margin-top: 15px;" onclick="showLoginModal()">
                        <i class="fas fa-sign-in-alt icon"></i> Войти для доступа
                    </button>
                `}
            </div>
        `;
    });
    
    beginnerCoursesContent += '</div>';
    beginnerCoursesTab.innerHTML = beginnerCoursesContent;
    
    // ========== ВКЛАДКА "ПРОДВИНУТЫЕ" ==========
    // Список продвинутых курсов
    const advancedCourses = ['puu', 'financial', 'mobile'];
    
    let advancedCoursesContent = '<div class="course-cards">';
    
    advancedCourses.forEach(courseId => {
        const course = courses[courseId];
        if (!course) return;
        
        // Получаем прогресс для авторизованных пользователей
        let progress = 0;
        if (currentUser && currentUser.progress && currentUser.progress[courseId] !== undefined) {
            progress = currentUser.progress[courseId];
        }
        
        const isCompleted = progress >= 100;
        
        advancedCoursesContent += `
            <div class="course-card">
                <div class="course-icon ${course.color}">
                    <i class="fas ${course.icon}"></i>
                </div>
                <h3>${course.title}</h3>
                <p>${course.description.substring(0, 80)}...</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-book"></i>
                        <span>${course.totalLessons} уроков</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>${course.totalDuration}</span>
                    </div>
                </div>
                <div style="margin-bottom: 10px; margin-top: 5px;">
                    <span style="background-color: #ff9800; color: white; padding: 3px 10px; border-radius: 15px; font-size: 12px; font-weight: bold;">
                        <i class="fas fa-rocket"></i> Продвинутый
                    </span>
                </div>
                ${currentUser ? `
                    <div class="progress-container" style="margin-top: 10px;">
                        <div class="progress-label">
                            <span>Прогресс</span>
                            <span>${progress}%</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: ${progress}%;"></div>
                        </div>
                    </div>
                    <button class="btn ${isCompleted ? 'btn-success' : ''}" style="width: 100%; margin-top: 15px;" onclick="startCourse('${courseId}')">
                        ${isCompleted ? '<i class="fas fa-check icon"></i> Курс пройден' : 'Начать курс'}
                    </button>
                ` : `
                    <button class="btn" style="width: 100%; margin-top: 15px;" onclick="showLoginModal()">
                        <i class="fas fa-sign-in-alt icon"></i> Войти для доступа
                    </button>
                `}
            </div>
        `;
    });
    
    advancedCoursesContent += '</div>';
    advancedCoursesTab.innerHTML = advancedCoursesContent;
    
    // ========== ВКЛАДКА "МОИ КУРСЫ" ==========
    if (currentUser) {
        myCoursesMessage.textContent = 'Ваши курсы:';
        
        let myCoursesContent = '<div class="course-cards">';
        
        Object.keys(courses).forEach(courseId => {
            const course = courses[courseId];
            
            // Показываем только курсы с прогрессом > 0
            let progress = 0;
            if (currentUser.progress && currentUser.progress[courseId] !== undefined) {
                progress = currentUser.progress[courseId];
            }
            
            if (progress > 0) {
                const isCompleted = progress >= 100;
                
                myCoursesContent += `
                    <div class="course-card">
                        <div class="course-icon ${course.color}">
                            <i class="fas ${course.icon}"></i>
                        </div>
                        <h3>${course.title}</h3>
                        <p>${course.description.substring(0, 80)}...</p>
                        <div class="progress-container">
                            <div class="progress-label">
                                <span>Прогресс</span>
                                <span>${progress}%</span>
                            </div>
                            <div class="progress-bar">
                                <div class="progress-fill" style="width: ${progress}%;"></div>
                            </div>
                        </div>
                        <button class="btn ${isCompleted ? 'btn-success' : ''}" style="width: 100%; margin-top: 15px;" onclick="startCourse('${courseId}')">
                            ${isCompleted ? '<i class="fas fa-check icon"></i> Курс пройден' : 'Продолжить'}
                        </button>
                    </div>
                `;
            }
        });
        
        myCoursesContent += '</div>';
        
        // Если нет курсов в процессе
        if (myCoursesContent === '<div class="course-cards"></div>') {
            myCoursesContent = `
                <div style="text-align: center; padding: 40px 0; color: #666;">
                    <i class="fas fa-book-open" style="font-size: 3rem; margin-bottom: 20px; color: #ddd;"></i>
                    <h3>У вас нет активных курсов</h3>
                    <p>Начните обучение с курсов для начинающих!</p>
                    <button class="btn btn-large" style="margin-top: 20px;" onclick="openTab(event, 'beginner-courses')">
                        <i class="fas fa-play icon"></i> Выбрать курс
                    </button>
                </div>
            `;
        }
        
        myCoursesTab.innerHTML = myCoursesContent;
    } else {
        myCoursesMessage.textContent = 'Войдите в систему, чтобы увидеть ваши курсы.';
        myCoursesTab.innerHTML = `
            <div style="text-align: center; padding: 40px 0;">
                <i class="fas fa-user-lock" style="font-size: 3rem; margin-bottom: 20px; color: #ddd;"></i>
                <h3>Авторизуйтесь для доступа к курсам</h3>
                <p>Войдите или зарегистрируйтесь, чтобы отслеживать прогресс</p>
                <button class="btn btn-large" style="margin-top: 20px;" onclick="showLoginModal()">
                    <i class="fas fa-sign-in-alt icon"></i> Войти
                </button>
                <button class="btn btn-large btn-success" style="margin-top: 20px; margin-left: 15px;" onclick="showRegisterModal()">
                    <i class="fas fa-user-plus icon"></i> Регистрация
                </button>
            </div>
        `;
    }
}
        
        // Загрузка страницы тренажеров
        function loadSimulatorsPage() {
            // Прогресс-бары уже обновляются через updateProgressBars()
        }
        
        // Загрузка страницы тестирования
        function loadTestPage() {
            const testContent = document.getElementById('testContent');
            
            if (!testContent) return;
            
            testContent.innerHTML = `
                <div style="text-align: center; padding: 15px 0;">
                    <h3>Выберите тест для прохождения</h3>
                    <p>Тестирование поможет закрепить знания и получить сертификат</p>
                    
                    <div class="course-cards" style="margin-top: 15px;">
                        <div class="course-card">
                            <div class="course-icon phishing">
                                <i class="fas fa-fish"></i>
                            </div>
                            <h3>Тест по фишингу</h3>
                            <p>10 вопросов по распознаванию фишинговых атак</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startPhishingTest()">
                                Начать тест
                            </button>
                        </div>

                        <div class="course-card">
                            <div class="course-icon calls">
                                <i class="fas fa-phone-alt"></i>
                            </div>
                            <h3>Тест по телефонному мошенничеству</h3>
                            <p>8 вопросов по защите от телефонных атак</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startCallsTest()">
                                Начать тест
                            </button>
                        </div>
                        
                          <div class="course-card">
                            <div class="course-icon gosuslugi">
                                <i class="fas fa-passport"></i>
                            </div>
                            <h3>Тест по мошенничеству с Госуслугами</h3>
                            <p>10 вопросов по защите аккаунта на портале Госуслуги</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startGosuslugiTest()">
                                Начать тест
                            </button>
                        </div>
                        <div class="course-card">
        <div class="course-icon puu">
            <i class="fas fa-laptop-code"></i>
        </div>
        <h3>Тест по ПУУ схемам</h3>
        <p>15 вопросов по сложным атакам и удаленному доступу</p>
        <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startPuuTest()">
            Начать тест
        </button>
    </div>
<div class="course-card" >
                    <div class="course-icon financial">
                        <i class="fas fa-credit-card"></i>
                    </div>
                    <h3>Тест по финансовому мошенничеству</h3>
                    <p>10 вопросов по защите от финансовых мошенников</p>
                    <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startFinanceFraudTest()" >
                        Начать тест
                    </button>
                </div>
<div class="course-card">
    <div class="course-icon social">
        <i class="fas fa-users"></i>
    </div>
    <h3>Тест по безопасности в соцсетях</h3>
    <p>10 вопросов по защите аккаунтов и приватности</p>
    <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startSocialTest()">
        Начать тест
    </button>
</div>
<div class="course-card">
    <div class="course-icon passwords">
        <i class="fas fa-key"></i>
    </div>
    <h3>Тест по паролям и аутентификации</h3>
    <p>15 вопросов по созданию и защите паролей, менеджерам паролей, 2FA</p>
    <button class="btn" style="width: 100%; margin-top: 15px;" onclick="startPasswordsTest()">
        Начать тест
    </button>
</div>
                        <div class="course-card">
    <div class="course-icon puu">
        <i class="fas fa-laptop-code"></i>
    </div>
    <h3>Итоговый тест</h3>
    <p>20 вопросов по всем темам кибербезопасности. Проверьте свои знания!</p>
    <div style="margin-bottom: 10px;">
        <span style="background-color: #ffa000; color: white; padding: 3px 10px; border-radius: 15px; font-size: 12px; font-weight: bold;">ЭКСПЕРТ</span>
        <span style="background-color: #f5f5f5; color: #666; padding: 3px 10px; border-radius: 15px; font-size: 12px; margin-left: 5px;">40 мин</span>
    </div>
    <button class="btn btn-success" style="width: 100%; margin-top: 15px;" onclick="startFinalTest()">
        <i class="fas fa-graduation-cap icon"></i> Начать итоговый тест
    </button>
</div>
            `;
        }
        
        // Загрузка страницы профиля
function loadProfilePage() {
    if (!currentUser) return;
    
    const profileContent = document.getElementById('profileContent');
    const registrationDate = new Date(currentUser.registrationDate).toLocaleDateString('ru-RU', {
        day: 'numeric', month: 'long', year: 'numeric'
    });
    const lastActive = new Date(currentUser.stats.lastActive).toLocaleDateString('ru-RU', {
        day: 'numeric', month: 'long', year: 'numeric', hour: '2-digit', minute: '2-digit'
    });
    
    // Рассчитываем общий прогресс по всем курсам
    let totalProgress = 0;
    let totalCourses = 0;
    let completedCoursesCount = 0;
    
    Object.keys(courses).forEach(courseId => {
        const progress = currentUser.progress[courseId] || 0;
        totalProgress += progress;
        totalCourses++;
        if (progress >= 100) completedCoursesCount++;
    });
    
    const averageProgress = totalCourses > 0 ? Math.round(totalProgress / totalCourses) : 0;
    
    // Собираем информацию о пройденных курсах
    let completedCoursesHTML = '';
    let inProgressCoursesHTML = '';
    let recommendedCoursesHTML = '';
    
    // Находим рекомендуемые курсы (с нулевым прогрессом)
    let recommendedCount = 0;
    Object.keys(courses).forEach(courseId => {
        const course = courses[courseId];
        const progress = currentUser.progress[courseId] || 0;
        
        if (progress === 0 && recommendedCount < 3) {
            recommendedCount++;
            recommendedCoursesHTML += `
                <div class="recommended-course-card" onclick="startCourse('${courseId}')">
                    <div class="recommended-course-icon ${course.color}">
                        <i class="fas ${course.icon}"></i>
                    </div>
                    <div class="recommended-course-info">
                        <h4>${course.title}</h4>
                        <p>${course.totalLessons} уроков • ${course.totalDuration}</p>
                        <span class="recommended-badge">Рекомендуем</span>
                    </div>
                </div>
            `;
        }
    });
    
    // Собираем курсы в процессе
    Object.keys(courses).forEach(courseId => {
        const course = courses[courseId];
        const progress = currentUser.progress[courseId] || 0;
        
        if (progress > 0 && progress < 100) {
            const totalLessons = course.lessons.length;
            const completedLessons = Math.round((progress / 100) * totalLessons);
            
            inProgressCoursesHTML += `
                <div class="progress-course-card" onclick="startCourse('${courseId}')">
                    <div class="progress-course-icon ${course.color}">
                        <i class="fas ${course.icon}"></i>
                    </div>
                    <div class="progress-course-details">
                        <div class="progress-course-header">
                            <h4>${course.title}</h4>
                            <span class="progress-percent">${progress}%</span>
                        </div>
                        <div class="progress-stats">
                            <span><i class="fas fa-check-circle"></i> ${completedLessons}/${totalLessons} уроков</span>
                            <span><i class="fas fa-clock"></i> ${course.totalDuration}</span>
                        </div>
                        <div class="progress-bar-container">
                            <div class="progress-bar-fill" style="width: ${progress}%;"></div>
                        </div>
                    </div>
                    <button class="continue-btn">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>
            `;
        }
    });
    
    // Собираем завершенные курсы
    if (currentUser.completedCourses && currentUser.completedCourses.length > 0) {
        currentUser.completedCourses.forEach(courseId => {
            const course = courses[courseId];
            if (course) {
                completedCoursesHTML += `
                    <div class="completed-course-card" onclick="startCourse('${courseId}')">
                        <div class="completed-course-icon ${course.color}">
                            <i class="fas ${course.icon}"></i>
                        </div>
                        <div class="completed-course-info">
                            <h4>${course.title}</h4>
                            <p><i class="fas fa-trophy"></i> Сертификат получен</p>
                        </div>
                        <div class="completed-badge">
                            <i class="fas fa-check-circle"></i>
                        </div>
                    </div>
                `;
            }
        });
    }
    
    // Собираем информацию о пройденных тренажерах
    let completedSimulatorsHTML = '';
    if (currentUser.completedSimulators && currentUser.completedSimulators.length > 0) {
        currentUser.completedSimulators.forEach(simulatorId => {
            const simulator = simulators[simulatorId];
            if (simulator) {
                completedSimulatorsHTML += `
                    <div class="simulator-badge">
                        <i class="fas fa-check-circle"></i>
                        ${simulator.title}
                    </div>
                `;
            }
        });
    }
    
    // Генерируем HTML профиля - ВСЕ СТИЛИ ИЗОЛИРОВАНЫ В .profile-enhanced
    profileContent.innerHTML = `
        <style>
            /* ИЗОЛИРОВАННЫЕ СТИЛИ ТОЛЬКО ДЛЯ ПРОФИЛЯ */
            .profile-enhanced {
                font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
                max-width: 1200px;
                margin: 0 auto;
            }
            
            /* Хедер профиля */
            .profile-enhanced .profile-header-enhanced {
                background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
                border-radius: 30px !important;
                padding: 40px !important;
                margin-bottom: 30px !important;
                color: white;
                display: flex;
                align-items: center;
                gap: 40px;
                box-shadow: 0 20px 40px rgba(0,0,0,0.1);
                position: relative;
                overflow: hidden;
            }
            
            .profile-enhanced .profile-header-enhanced::before {
                content: '';
                position: absolute;
                top: -50%;
                right: -50%;
                width: 200%;
                height: 200%;
                background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
                animation: rotate 20s linear infinite;
            }
            
            @keyframes rotate {
                from { transform: rotate(0deg); }
                to { transform: rotate(360deg); }
            }
            
            .profile-enhanced .profile-avatar-enhanced {
                width: 120px !important;
                height: 120px !important;
                background: rgba(255,255,255,0.2);
                border-radius: 50% !important;
                display: flex;
                align-items: center;
                justify-content: center;
                font-size: 3rem !important;
                font-weight: bold;
                color: white;
                border: 4px solid rgba(255,255,255,0.5);
                backdrop-filter: blur(10px);
                position: relative;
                z-index: 2;
            }
            
            .profile-enhanced .profile-info-enhanced {
                flex: 1;
                position: relative;
                z-index: 2;
            }
            
            .profile-enhanced .profile-info-enhanced h1 {
                font-size: 2.5rem !important;
                margin-bottom: 10px !important;
                font-weight: 700 !important;
                color: white !important;
            }
            
            .profile-enhanced .profile-meta {
                display: flex;
                gap: 30px;
                margin-top: 15px;
            }
            
            .profile-enhanced .profile-meta-item {
                display: flex;
                align-items: center;
                gap: 8px;
                background: rgba(255,255,255,0.2);
                padding: 8px 16px;
                border-radius: 30px !important;
                backdrop-filter: blur(5px);
            }
            
            /* Статистика */
            .profile-enhanced .stats-grid-enhanced {
                display: grid;
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
                gap: 20px;
                margin-bottom: 30px !important;
            }
            
            .profile-enhanced .stat-card-enhanced {
                background: white;
                border-radius: 20px !important;
                padding: 25px !important;
                display: flex;
                align-items: center;
                gap: 20px;
                box-shadow: 0 10px 30px rgba(0,0,0,0.05);
                transition: transform 0.3s ease;
            }
            
            .profile-enhanced .stat-card-enhanced:hover {
                transform: translateY(-5px);
                box-shadow: 0 15px 40px rgba(0,0,0,0.1);
            }
            
            .profile-enhanced .stat-icon {
                width: 60px !important;
                height: 60px !important;
                border-radius: 15px !important;
                display: flex;
                align-items: center;
                justify-content: center;
                font-size: 1.8rem !important;
                color: white;
            }
            
            .profile-enhanced .stat-icon.score { background: linear-gradient(135deg, #667eea, #764ba2); }
            .profile-enhanced .stat-icon.courses { background: linear-gradient(135deg, #f093fb, #f5576c); }
            .profile-enhanced .stat-icon.lessons { background: linear-gradient(135deg, #4facfe, #00f2fe); }
            .profile-enhanced .stat-icon.simulators { background: linear-gradient(135deg, #43e97b, #38f9d7); }
            
            .profile-enhanced .stat-details h3 {
                font-size: 2rem !important;
                font-weight: 700 !important;
                color: #333 !important;
                margin-bottom: 5px !important;
            }
            
            .profile-enhanced .stat-details p {
                color: #666 !important;
                font-size: 0.95rem !important;
            }
            
            /* Общий прогресс */
            .profile-enhanced .overall-progress {
                background: linear-gradient(135deg, #f5f7fa 0%, #e9edf5 100%);
                border-radius: 20px !important;
                padding: 30px !important;
                margin-bottom: 30px !important;
            }
            
            .profile-enhanced .overall-progress-header {
                display: flex;
                justify-content: space-between;
                align-items: center;
                margin-bottom: 20px !important;
            }
            
            .profile-enhanced .overall-progress-header h3 {
                font-size: 1.3rem !important;
                color: #333 !important;
                display: flex;
                align-items: center;
                gap: 10px;
            }
            
            .profile-enhanced .overall-percent {
                font-size: 2rem !important;
                font-weight: 700 !important;
                color: #667eea !important;
            }
            
            .profile-enhanced .overall-progress-bar {
                height: 12px !important;
                background: rgba(102, 126, 234, 0.1);
                border-radius: 30px !important;
                overflow: hidden;
                margin-bottom: 20px !important;
            }
            
            .profile-enhanced .overall-progress-fill {
                height: 100% !important;
                background: linear-gradient(90deg, #667eea, #764ba2);
                border-radius: 30px !important;
                transition: width 1s ease;
                animation: shimmer 2s infinite;
            }
            
            @keyframes shimmer {
                0% { opacity: 1; }
                50% { opacity: 0.8; }
                100% { opacity: 1; }
            }
            
            .profile-enhanced .overall-stats {
                display: grid;
                grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
                gap: 20px;
            }
            
            .profile-enhanced .overall-stat-item {
                text-align: center;
            }
            
            .profile-enhanced .overall-stat-value {
                font-size: 1.5rem !important;
                font-weight: 700 !important;
                color: #333 !important;
            }
            
            .profile-enhanced .overall-stat-label {
                color: #666 !important;
                font-size: 0.9rem !important;
                margin-top: 5px;
            }
            
            /* Секции */
            .profile-enhanced .profile-section {
                background: white;
                border-radius: 20px !important;
                padding: 30px !important;
                margin-bottom: 30px !important;
                box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            }
            
            .profile-enhanced .section-header {
                display: flex;
                justify-content: space-between;
                align-items: center;
                margin-bottom: 25px !important;
            }
            
            .profile-enhanced .section-header h3 {
                font-size: 1.3rem !important;
                color: #333 !important;
                display: flex;
                align-items: center;
                gap: 10px;
            }
            
            .profile-enhanced .section-header h3 i {
                color: #667eea;
            }
            
            /* Карточки курсов в процессе */
            .profile-enhanced .progress-course-card {
                display: flex;
                align-items: center;
                gap: 20px;
                padding: 20px !important;
                background: #f8fafc;
                border-radius: 15px !important;
                margin-bottom: 15px !important;
                transition: all 0.3s ease;
                cursor: pointer;
                border: 2px solid transparent;
            }
            
            .profile-enhanced .progress-course-card:hover {
                background: white;
                border-color: #667eea;
                transform: translateX(5px);
                box-shadow: 0 10px 25px rgba(102, 126, 234, 0.1);
            }
            
            .profile-enhanced .progress-course-icon {
                width: 60px !important;
                height: 60px !important;
                border-radius: 15px !important;
                display: flex;
                align-items: center;
                justify-content: center;
                font-size: 1.5rem !important;
                color: white;
                flex-shrink: 0;
            }
            
            .profile-enhanced .progress-course-details {
                flex: 1;
            }
            
            .profile-enhanced .progress-course-header {
                display: flex;
                justify-content: space-between;
                align-items: center;
                margin-bottom: 8px !important;
            }
            
            .profile-enhanced .progress-course-header h4 {
                font-size: 1.1rem !important;
                color: #333 !important;
            }
            
            .profile-enhanced .progress-percent {
                font-weight: 700 !important;
                color: #667eea !important;
                background: rgba(102, 126, 234, 0.1);
                padding: 4px 12px;
                border-radius: 20px !important;
                font-size: 0.9rem !important;
            }
            
            .profile-enhanced .progress-stats {
                display: flex;
                gap: 20px;
                margin-bottom: 12px !important;
                color: #666 !important;
                font-size: 0.9rem !important;
            }
            
            .profile-enhanced .progress-stats span {
                display: flex;
                align-items: center;
                gap: 5px;
            }
            
            .profile-enhanced .progress-bar-container {
                height: 8px !important;
                background: #e9ecef;
                border-radius: 10px !important;
                overflow: hidden;
            }
            
            .profile-enhanced .progress-bar-fill {
                height: 100% !important;
                background: linear-gradient(90deg, #667eea, #764ba2);
                border-radius: 10px !important;
                transition: width 0.5s ease;
            }
            
            .profile-enhanced .continue-btn {
                width: 40px !important;
                height: 40px !important;
                border-radius: 50% !important;
                background: white;
                border: none !important;
                color: #667eea;
                font-size: 1.2rem !important;
                display: flex;
                align-items: center;
                justify-content: center;
                cursor: pointer;
                transition: all 0.3s ease;
                flex-shrink: 0;
            }
            
            .profile-enhanced .continue-btn:hover {
                background: #667eea !important;
                color: white !important;
                transform: scale(1.1);
            }
            
            /* Завершенные курсы */
            .profile-enhanced .completed-course-card {
                display: flex;
                align-items: center;
                gap: 20px;
                padding: 15px !important;
                background: linear-gradient(135deg, #f8fafc, #f1f5f9);
                border-radius: 12px !important;
                margin-bottom: 12px !important;
                cursor: pointer;
                transition: all 0.3s ease;
                border: 2px solid transparent;
            }
            
            .profile-enhanced .completed-course-card:hover {
                background: white;
                border-color: #4caf50;
            }
            
            .profile-enhanced .completed-course-icon {
                width: 50px !important;
                height: 50px !important;
                border-radius: 12px !important;
                display: flex;
                align-items: center;
                justify-content: center;
                font-size: 1.2rem !important;
                color: white;
                flex-shrink: 0;
            }
            
            .profile-enhanced .completed-course-info {
                flex: 1;
            }
            
            .profile-enhanced .completed-course-info h4 {
                font-size: 1rem !important;
                color: #333 !important;
                margin-bottom: 5px !important;
            }
            
            .profile-enhanced .completed-course-info p {
                color: #4caf50 !important;
                font-size: 0.85rem !important;
                display: flex;
                align-items: center;
                gap: 5px;
            }
            
            .profile-enhanced .completed-badge {
                color: #4caf50 !important;
                font-size: 1.5rem !important;
            }
            
            /* Рекомендуемые курсы */
            .profile-enhanced .recommended-courses-grid {
                display: grid;
                grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
                gap: 20px;
            }
            
            .profile-enhanced .recommended-course-card {
                display: flex;
                align-items: center;
                gap: 15px;
                padding: 20px !important;
                background: linear-gradient(135deg, #fff5f5, #fff0f0);
                border-radius: 15px !important;
                cursor: pointer;
                transition: all 0.3s ease;
                border: 2px solid transparent;
            }
            
            .profile-enhanced .recommended-course-card:hover {
                transform: translateY(-5px);
                border-color: #ff6b6b;
                box-shadow: 0 15px 30px rgba(255, 107, 107, 0.15);
            }
            
            .profile-enhanced .recommended-course-icon {
                width: 60px !important;
                height: 60px !important;
                border-radius: 15px !important;
                display: flex;
                align-items: center;
                justify-content: center;
                font-size: 1.5rem !important;
                color: white;
                flex-shrink: 0;
            }
            
            .profile-enhanced .recommended-course-info {
                flex: 1;
            }
            
            .profile-enhanced .recommended-course-info h4 {
                font-size: 1rem !important;
                color: #333 !important;
                margin-bottom: 5px !important;
            }
            
            .profile-enhanced .recommended-course-info p {
                color: #666 !important;
                font-size: 0.85rem !important;
                margin-bottom: 8px !important;
            }
            
            .profile-enhanced .recommended-badge {
                background: #ff6b6b !important;
                color: white !important;
                padding: 4px 12px;
                border-radius: 20px !important;
                font-size: 0.75rem !important;
                font-weight: 600;
                display: inline-block;
            }
            
            /* Тренажеры */
            .profile-enhanced .simulators-grid {
                display: flex;
                flex-wrap: wrap;
                gap: 10px;
                margin-top: 15px !important;
            }
            
            .profile-enhanced .simulator-badge {
                background: linear-gradient(135deg, #4facfe, #00f2fe) !important;
                color: white !important;
                padding: 8px 16px !important;
                border-radius: 30px !important;
                font-size: 0.9rem !important;
                display: inline-flex;
                align-items: center;
                gap: 8px;
            }
            
            /* Пустое состояние */
            .profile-enhanced .empty-state {
                text-align: center;
                padding: 40px !important;
                color: #666 !important;
            }
            
            .profile-enhanced .empty-state i {
                font-size: 3rem !important;
                color: #ddd;
                margin-bottom: 20px !important;
            }
            
            .profile-enhanced .empty-state h4 {
                font-size: 1.2rem !important;
                color: #333 !important;
                margin-bottom: 10px !important;
            }
            
            /* Кнопки */
            .profile-enhanced .btn-gradient {
                background: linear-gradient(90deg, #667eea, #764ba2) !important;
                color: white !important;
                border: none !important;
                padding: 12px 30px !important;
                border-radius: 30px !important;
                font-size: 1rem !important;
                font-weight: 600;
                cursor: pointer;
                transition: all 0.3s ease;
                display: inline-flex;
                align-items: center;
                gap: 10px;
            }
            
            .profile-enhanced .btn-gradient:hover {
                transform: translateY(-2px);
                box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
            }
            
            .profile-enhanced .btn-gradient.secondary {
                background: linear-gradient(90deg, #f093fb, #f5576c) !important;
            }
            
            .profile-enhanced .action-buttons {
                display: flex;
                gap: 15px;
                justify-content: center;
                margin-top: 40px !important;
            }
            
            /* Адаптивность */
            @media (max-width: 768px) {
                .profile-enhanced .profile-header-enhanced {
                    flex-direction: column;
                    text-align: center;
                    padding: 30px !important;
                }
                
                .profile-enhanced .profile-meta {
                    flex-direction: column;
                    align-items: center;
                }
                
                .profile-enhanced .stats-grid-enhanced {
                    grid-template-columns: 1fr;
                }
                
                .profile-enhanced .progress-course-card {
                    flex-direction: column;
                    text-align: center;
                }
                
                .profile-enhanced .progress-course-header {
                    flex-direction: column;
                    gap: 10px;
                }
                
                .profile-enhanced .progress-stats {
                    flex-direction: column;
                    align-items: center;
                }
                
                .profile-enhanced .recommended-courses-grid {
                    grid-template-columns: 1fr;
                }
            }
        </style>
        
        <div class="profile-enhanced">
            <!-- Шапка профиля -->
            <div class="profile-header-enhanced">
                <div class="profile-avatar-enhanced">
                    ${currentUser.name.charAt(0).toUpperCase()}
                </div>
                <div class="profile-info-enhanced">
                    <h1>${currentUser.name}</h1>
                    <p style="opacity: 0.9; font-size: 1.1rem; color: white !important;">Студент Академии Кибербезопасности</p>
                    <div class="profile-meta">
                        <div class="profile-meta-item">
                            <i class="fas fa-calendar-alt"></i>
                            С ${registrationDate}
                        </div>
                        <div class="profile-meta-item">
                            <i class="fas fa-clock"></i>
                            Был(а) ${lastActive}
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Статистика -->
            <div class="stats-grid-enhanced">
                <div class="stat-card-enhanced">
                    <div class="stat-icon score">
                        <i class="fas fa-star"></i>
                    </div>
                    <div class="stat-details">
                        <h3>${currentUser.stats.score || 0}</h3>
                        <p>Очков рейтинга</p>
                    </div>
                </div>
                
                <div class="stat-card-enhanced">
                    <div class="stat-icon courses">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <div class="stat-details">
                        <h3>${completedCoursesCount}/${totalCourses}</h3>
                        <p>Курсов завершено</p>
                    </div>
                </div>
                
                <div class="stat-card-enhanced">
                    <div class="stat-icon lessons">
                        <i class="fas fa-book-open"></i>
                    </div>
                    <div class="stat-details">
                        <h3>${currentUser.stats.completedLessons || 0}</h3>
                        <p>Уроков пройдено</p>
                    </div>
                </div>
                
                <div class="stat-card-enhanced">
                    <div class="stat-icon simulators">
                        <i class="fas fa-gamepad"></i>
                    </div>
                    <div class="stat-details">
                        <h3>${currentUser.stats.completedSimulators || 0}</h3>
                        <p>Тренажеров пройдено</p>
                    </div>
                </div>
            </div>
            
            <!-- Общий прогресс -->
            <div class="overall-progress">
                <div class="overall-progress-header">
                    <h3>
                        <i class="fas fa-chart-line" style="color: #667eea;"></i>
                        Общий прогресс обучения
                    </h3>
                    <div class="overall-percent">${averageProgress}%</div>
                </div>
                <div class="overall-progress-bar">
                    <div class="overall-progress-fill" style="width: ${averageProgress}%;"></div>
                </div>
                <div class="overall-stats">
                    <div class="overall-stat-item">
                        <div class="overall-stat-value">${totalCourses}</div>
                        <div class="overall-stat-label">Всего курсов</div>
                    </div>
                    <div class="overall-stat-item">
                        <div class="overall-stat-value">${completedCoursesCount}</div>
                        <div class="overall-stat-label">Завершено</div>
                    </div>
                    <div class="overall-stat-item">
                        <div class="overall-stat-value">${totalCourses - completedCoursesCount}</div>
                        <div class="overall-stat-label">В процессе</div>
                    </div>
                </div>
            </div>
            
            <!-- Курсы в процессе -->
            ${inProgressCoursesHTML ? `
                <div class="profile-section">
                    <div class="section-header">
                        <h3>
                            <i class="fas fa-spinner"></i>
                            Продолжить обучение
                        </h3>
                        <span class="progress-percent">${Object.keys(currentUser.progress).filter(id => currentUser.progress[id] > 0 && currentUser.progress[id] < 100).length} активных курсов</span>
                    </div>
                    <div class="in-progress-courses">
                        ${inProgressCoursesHTML}
                    </div>
                </div>
            ` : ''}
            
            <!-- Рекомендуемые курсы -->
            ${recommendedCoursesHTML ? `
                <div class="profile-section">
                    <div class="section-header">
                        <h3>
                            <i class="fas fa-thumbs-up"></i>
                            Рекомендуем начать
                        </h3>
                        <span style="color: #666;">на основе ваших интересов</span>
                    </div>
                    <div class="recommended-courses-grid">
                        ${recommendedCoursesHTML}
                    </div>
                </div>
            ` : ''}
            
            <!-- Завершенные курсы -->
            ${completedCoursesHTML ? `
                <div class="profile-section">
                    <div class="section-header">
                        <h3>
                            <i class="fas fa-trophy" style="color: #ffc107;"></i>
                            Достижения
                        </h3>
                        <span style="color: #4caf50;">${currentUser.completedCourses.length} ${currentUser.completedCourses.length === 1 ? 'курс' : 
                                                                        currentUser.completedCourses.length < 5 ? 'курса' : 'курсов'} завершено</span>
                    </div>
                    <div class="completed-courses">
                        ${completedCoursesHTML}
                    </div>
                </div>
            ` : ''}
            
            <!-- Пройденные тренажеры -->
            ${completedSimulatorsHTML ? `
                <div class="profile-section">
                    <div class="section-header">
                        <h3>
                            <i class="fas fa-gamepad"></i>
                            Освоенные тренажеры
                        </h3>
                        <span style="color: #4facfe;">${currentUser.completedSimulators.length} тренажеров</span>
                    </div>
                    <div class="simulators-grid">
                        ${completedSimulatorsHTML}
                    </div>
                </div>
            ` : ''}
            
            <!-- Пустое состояние -->
            ${!inProgressCoursesHTML && !completedCoursesHTML && !completedSimulatorsHTML ? `
                <div class="profile-section">
                    <div class="empty-state">
                        <i class="fas fa-graduation-cap"></i>
                        <h4>Добро пожаловать в Академию!</h4>
                        <p>Начните свое обучение с курсов для начинающих</p>
                        <button class="btn-gradient" onclick="showPage('courses')">
                            <i class="fas fa-play"></i>
                            Выбрать курс
                        </button>
                    </div>
                </div>
            ` : ''}
            
            <!-- Кнопки действий -->
            <div class="action-buttons">
                <button class="btn-gradient" onclick="showPage('courses')">
                    <i class="fas fa-book"></i>
                    Все курсы
                </button>
                <button class="btn-gradient secondary" onclick="showPage('simulators')">
                    <i class="fas fa-gamepad"></i>
                    Тренажеры
                </button>
                <button class="btn btn-outline" onclick="resetProgress()" style="border: 2px solid #dc3545 !important; color: #dc3545 !important; background: transparent !important;">
                    <i class="fas fa-redo"></i>
                    Сбросить прогресс
                </button>
            </div>
        </div>
    `;
}
        
        // Начать курс
function startCourse(courseId) {
    // Прокрутка к началу страницы
    setTimeout(() => {
        window.scrollTo({
            top: 0,
            behavior: 'smooth'
        });
    }, 100);
    
    if (!currentUser) {
        showNotification('error', 'Для доступа к курсам необходимо войти в систему');
        showLoginModal();
        return;
    }
    
    const course = courses[courseId];
    if (!course) return;
    
    // Загружаем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // Получаем прогресс
    let progress = 0;
    if (currentUser.progress && currentUser.progress[courseId] !== undefined) {
        progress = currentUser.progress[courseId];
    } else {
        // Инициализируем прогресс, если его нет
        if (!currentUser.progress) currentUser.progress = {};
        currentUser.progress[courseId] = 0;
        progress = 0;
    }
    
    // ВАЖНО: Вычисляем количество пройденных уроков на основе прогресса
    const totalLessons = course.lessons.length;
    let completedLessonsCount = 0;
    
    if (progress === 0) {
        completedLessonsCount = 0;
    } else if (progress >= 100) {
        completedLessonsCount = totalLessons;
    } else {
        // Рассчитываем количество пройденных уроков
        completedLessonsCount = Math.round((progress / 100) * totalLessons);
        if (completedLessonsCount > totalLessons) completedLessonsCount = totalLessons;
    }
    
    // Генерируем список уроков
    let lessonsHTML = '';
    course.lessons.forEach((lesson, index) => {
        // Урок считается пройденным, ТОЛЬКО если его индекс МЕНЬШЕ количества пройденных уроков
        const isCompleted = index < completedLessonsCount;
        
        lessonsHTML += `
            <div class="lesson-item ${isCompleted ? 'completed' : ''}" onclick="showLessonContent('${courseId}', ${index})">
                <span class="lesson-number">${index + 1}</span>
                <div>
                    <div class="lesson-title">${lesson.title}</div>
                    <div class="lesson-duration"><i class="fas fa-clock icon"></i> ${lesson.duration}</div>
                </div>
                ${isCompleted ? '<i class="fas fa-check success-icon" style="margin-left: auto;"></i>' : ''}
            </div>
        `;
    });
    
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon ${course.color}">
                <i class="fas ${course.icon}"></i>
            </div>
            <div class="course-header-content">
                <h1>${course.title}</h1>
                <p>${course.description}</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-book"></i>
                        <span>${course.totalLessons} уроков</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>${course.totalDuration}</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Прогресс: ${progress}%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="progress-container">
            <div class="progress-label">
                <span>Общий прогресс по курсу</span>
                <span>${progress}%</span>
            </div>
            <div class="progress-bar">
                <div class="progress-fill" style="width: ${progress}%;"></div>
            </div>
        </div>
        
        <h3 style="margin-top: 30px;">Уроки курса</h3>
        <div class="lessons-list">
            ${lessonsHTML}
        </div>
        
        <div style="margin-top: 40px; text-align: center;">
            <button class="btn btn-large" onclick="showPage('courses')">
                <i class="fas fa-arrow-left icon"></i> Вернуться к курсам
            </button>
        </div>
        
        <div id="lessonContentContainer" style="display: none; margin-top: 40px;">
            <!-- Содержимое урока будет загружаться здесь -->
        </div>
    `;
}
// Показать содержимое урока
function showLessonContent(courseId, lessonIndex) {
    const course = courses[courseId];
    if (!course || !course.lessons[lessonIndex]) return;
    
    const lesson = course.lessons[lessonIndex];
    const lessonContentContainer = document.getElementById('lessonContentContainer');
    
    if (!lessonContentContainer) return;
    
    // Показываем контейнер
    lessonContentContainer.style.display = 'block';
    lessonContentContainer.innerHTML = `
        <div class="card">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h2>${lesson.title}</h2>
                <span><i class="fas fa-clock icon"></i> ${lesson.duration}</span>
            </div>
            
            <div id="lessonContent">
                ${lesson.content || '<p>Содержимое урока загружается...</p>'}
            </div>
            
            <div style="margin-top: 30px; display: flex; justify-content: space-between;">
                ${lessonIndex > 0 ? `
                    <button class="btn" onclick="showLessonContent('${courseId}', ${lessonIndex - 1})">
                        <i class="fas fa-arrow-left icon"></i> Предыдущий урок
                    </button>
                ` : '<div></div>'}
                
                <button class="btn btn-success" onclick="completeLesson('${courseId}', ${lessonIndex})">
                    <i class="fas fa-check icon"></i> Завершить урок
                </button>
                
                ${lessonIndex < course.lessons.length - 1 ? `
                    <button class="btn" onclick="showLessonContent('${courseId}', ${lessonIndex + 1})">
                        Следующий урок <i class="fas fa-arrow-right icon"></i>
                    </button>
                ` : '<div></div>'}
            </div>
            
            <div style="text-align: center; margin-top: 20px;">
                <button class="btn btn-outline" onclick="document.getElementById('lessonContentContainer').style.display = 'none'">
                    <i class="fas fa-times icon"></i> Закрыть урок
                </button>
            </div>
        </div>
    `;
    
    // Прокручиваем к уроку
    lessonContentContainer.scrollIntoView({ behavior: 'smooth' });
}
        
        // Завершить урок
function completeLesson(courseId, lessonIndex) {
    if (!currentUser) return;
    
    const course = courses[courseId];
    if (!course) return;
    
    const totalLessons = course.lessons.length;
    
    // Инициализируем прогресс, если его нет
    if (!currentUser.progress) currentUser.progress = {};
    if (!currentUser.progress[courseId]) currentUser.progress[courseId] = 0;
    
    const currentProgress = currentUser.progress[courseId];
    
    // ВАЖНО: Храним количество пройденных уроков, а не проценты!
    // Получаем текущее количество пройденных уроков из прогресса
    let completedLessonsCount = 0;
    
    if (currentProgress === 0) {
        completedLessonsCount = 0;
    } else if (currentProgress >= 100) {
        completedLessonsCount = totalLessons;
    } else {
        // Рассчитываем количество пройденных уроков на основе прогресса
        // Используем Math.round для более точного определения
        completedLessonsCount = Math.round((currentProgress / 100) * totalLessons);
        
        // Коррекция: если прогресс 50% при 6 уроках, то пройдено 3 урока
        // Если прогресс 33% при 6 уроках, то пройдено 2 урока
        if (completedLessonsCount > totalLessons) completedLessonsCount = totalLessons;
    }
    
    // ПРОВЕРКА 1: Урок уже пройден?
    if (lessonIndex < completedLessonsCount) {
        showNotification('info', 'Этот урок уже завершен');
        return;
    }
    
    // ПРОВЕРКА 2: Можно проходить только следующий урок по порядку
    if (lessonIndex > completedLessonsCount) {
        showNotification('error', 'Сначала завершите предыдущие уроки');
        return;
    }
    
    // Рассчитываем новый прогресс - ИСПОЛЬЗУЕМ КОЛИЧЕСТВО УРОКОВ, А НЕ ПРОЦЕНТЫ
    const newCompletedCount = completedLessonsCount + 1;
    
    // Округляем до целого числа
    let newProgress = Math.round((newCompletedCount / totalLessons) * 100);
    
    // Для последнего урока всегда 100%
    if (newCompletedCount >= totalLessons) {
        newProgress = 100;
    }
    
    // Обновляем прогресс
    currentUser.progress[courseId] = newProgress;
    currentUser.stats.completedLessons = (currentUser.stats.completedLessons || 0) + 1;
    currentUser.stats.score = (currentUser.stats.score || 0) + 10;
    currentUser.stats.lastActive = new Date().toISOString();
    
    // Проверяем, завершен ли курс
    if (newProgress >= 100 && !currentUser.completedCourses.includes(courseId)) {
        currentUser.completedCourses.push(courseId);
        showNotification('success', `🎉 Поздравляем! Вы завершили курс "${course.title}"`);
    } else {
        showNotification('success', `✅ Урок "${course.lessons[lessonIndex].title}" завершен! +10 очков (Прогресс: ${newProgress}%)`);
    }
    
    // Сохраняем в localStorage
    updateUserInStorage();
    
    // Обновляем отображение курса
    startCourse(courseId);
}
        
        // Начать тренажер
        function startSimulator(simulatorId) {
            if (!currentUser) {
                showNotification('error', 'Для доступа к тренажерам необходимо войти в систему');
                showLoginModal();
                return;
            }
            
            const simulator = simulators[simulatorId];
            if (!simulator) return;
            
            // Загружаем страницу активного тренажера
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            document.getElementById('active-simulator').classList.add('active');
            
            // Обновляем навигацию
            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active');
            });
            
            // Генерируем контент тренажера
            const simulatorContent = document.getElementById('simulatorContent');
            
            let simulatorHTML = '';
            
            switch(simulatorId) {
                case 'phishing-detective':
                    simulatorHTML = getPhishingDetectiveContent();
                    break;
                case 'phone-simulator':
                    simulatorHTML = getPhoneSimulatorContent();
                    break;
                case 'password-constructor':
                    simulatorHTML = getPasswordConstructorContent();
                    break;
                default:
                    simulatorHTML = getDefaultSimulatorContent(simulator);
            }
            
            simulatorContent.innerHTML = `
                <div class="course-header">
                    <div class="course-header-icon" style="background: linear-gradient(135deg, var(--accent-color), #26c6da);">
                        <i class="fas fa-gamepad"></i>
                    </div>
                    <div class="course-header-content">
                        <h1>${simulator.title}</h1>
                        <p>${simulator.description}</p>
                    </div>
                </div>
                
                ${simulatorHTML}
                
                <div style="margin-top: 40px; text-align: center;">
                    <button class="btn btn-large" onclick="completeSimulator('${simulatorId}')">
                        <i class="fas fa-check icon"></i> Завершить тренажер
                    </button>
                    <button class="btn btn-large btn-outline" onclick="showPage('simulators')" style="margin-left: 15px;">
                        <i class="fas fa-arrow-left icon"></i> Вернуться к тренажерам
                    </button>
                </div>
            `;
    setTimeout(() => {
    if (simulatorId === 'phishing-detective' && window.initPhishingSimulator) {
        window.initPhishingSimulator();
    } else if (simulatorId === 'phone-simulator' && window.initPhoneSimulator) {
        window.initPhoneSimulator();
    } else if (simulatorId === 'security-check' && window.initVKSimulator) {
    window.initVKSimulator();
    } else if (simulatorId === 'gosuslugi-check' && window.initGosuslugiSimulator) {
        window.initGosuslugiSimulator();
 } else if (simulatorId === 'puu-analysis' && window.initPuuSimulator) {
        console.log('Инициализация тренажера ПУУ');
        window.initPuuSimulator();
    }
}, 100);
setTimeout(() => {
    if (simulatorId === 'phishing-detective' && window.initPhishingSimulator) {
        window.initPhishingSimulator();
    } else if (simulatorId === 'phone-simulator' && window.initPhoneSimulator) {
        window.initPhoneSimulator();
    } else if (simulatorId === 'gosuslugi-check' && window.initGosuslugiSimulator) {
        window.initGosuslugiSimulator();
    }
}, 100);
if (simulatorId === 'phishing-detective') {
    setTimeout(() => {
        if (window.initPhishingSimulator) {
            window.initPhishingSimulator();
        }
    }, 100);
}
        }
        
        // Завершить тренажер
function completeSimulator(simulatorId) {
    if (!currentUser) {
        showNotification('error', 'Для сохранения прогресса войдите в систему');
        showLoginModal();
        return;
    }
    
    // Для тренажера Фишинг используем специальную функцию
    if (simulatorId === 'phishing-detective') {
        completePhishingSimulator();
        return;
    }
    
    // Для тренажера Телефон используем специальную функцию
    if (simulatorId === 'phone-simulator') {
        completePhoneSimulator();
        return;
    }
    
    // Для тренажера Проверка безопасности используем симулятор ВК
    if (simulatorId === 'security-check') {
        completeVKSimulator();
        return;
    }
    
    const simulator = simulators[simulatorId];
    if (!simulator) return;
    
    // Проверяем, не завершен ли уже тренажер
    if (currentUser.completedSimulators && currentUser.completedSimulators.includes(simulatorId)) {
        showNotification('info', 'Этот тренажер уже завершен');
        showPage('simulators');
        return;
    }
    
    // Для диалогового тренажера Госуслуг проверяем, был ли он завершен
    if (simulatorId === 'gosuslugi-check') {
        // Проверяем, была ли начата симуляция
        const chatMessages = document.getElementById('gosuslugi-chat-messages');
        const hasStarted = chatMessages && chatMessages.children.length > 0;
        
        if (!hasStarted) {
            showNotification('info', 'Сначала пройдите тренажер');
            return;
        }
        
        // Проверяем, завершена ли симуляция
        const isFinished = gosuslugiSimulationFinished || false;
        const securityScore = gosuslugiSecurityScore || 0;
        
        if (!isFinished) {
            if (confirm('Тренажер еще не завершен. Завершить сейчас и получить частичные очки?')) {
                // Вычисляем очки на основе текущей безопасности
                const earnedPoints = Math.max(10, Math.floor(securityScore / 5));
                
                // Обновляем прогресс
                if (!currentUser.completedSimulators) {
                    currentUser.completedSimulators = [];
                }
                
                currentUser.completedSimulators.push(simulatorId);
                currentUser.stats.completedSimulators = (currentUser.stats.completedSimulators || 0) + 1;
                currentUser.stats.score = (currentUser.stats.score || 0) + earnedPoints;
                currentUser.stats.lastActive = new Date().toISOString();
                
                updateUserInStorage();
                
                // ПРИНУДИТЕЛЬНО ОБНОВЛЯЕМ ПРОГРЕСС-БАРЫ
                updateProgressBars();
                
                showNotification('success', `Тренажер "${simulator.title}" завершен! +${earnedPoints} очков (безопасность: ${securityScore}%)`);
                
                // Возвращаемся к тренажерам
                showPage('simulators');
            }
            return;
        } else {
            // Тренажер уже завершен (пользователь дошел до конца)
            const earnedPoints = securityScore >= 50 ? 20 : 10;
            
            // Обновляем прогресс
            if (!currentUser.completedSimulators) {
                currentUser.completedSimulators = [];
            }
            
            currentUser.completedSimulators.push(simulatorId);
            currentUser.stats.completedSimulators = (currentUser.stats.completedSimulators || 0) + 1;
            currentUser.stats.score = (currentUser.stats.score || 0) + earnedPoints;
            currentUser.stats.lastActive = new Date().toISOString();
            
            updateUserInStorage();
            
            // ПРИНУДИТЕЛЬНО ОБНОВЛЯЕМ ПРОГРЕСС-БАРЫ
            updateProgressBars();
            
            showNotification('success', `Тренажер "${simulator.title}" завершен! +${earnedPoints} очков`);
            
            // Возвращаемся к тренажерам
            showPage('simulators');
            return;
        }
    }
    
    // Для остальных тренажеров
    if (!currentUser.completedSimulators) {
        currentUser.completedSimulators = [];
    }
    
    currentUser.completedSimulators.push(simulatorId);
    currentUser.stats.completedSimulators = (currentUser.stats.completedSimulators || 0) + 1;
    currentUser.stats.score = (currentUser.stats.score || 0) + 20;
    currentUser.stats.lastActive = new Date().toISOString();
    
    updateUserInStorage();
    
    // ПРИНУДИТЕЛЬНО ОБНОВЛЯЕМ ПРОГРЕСС-БАРЫ
    updateProgressBars();
    
    showNotification('success', `Тренажер "${simulator.title}" завершен! +20 очков`);
    
    // Возвращаемся к тренажерам
    showPage('simulators');
}
        
        // Начать тест
        function startTest(testType) {
            if (!currentUser) {
                showNotification('error', 'Для прохождения тестов необходимо войти в систему');
                showLoginModal();
                return;
            }
            
            // Показываем страницу тестирования
            showPage('test');
            
            // Здесь можно добавить логику для конкретного теста
            showNotification('info', `Начинаем тест "${testType}"`);
        }

        // ============================
// ИИ-ТРЕНАЖЕР ПУУ-СХЕМ
// ============================

// Глобальные переменные для ИИ-тренажера ПУУ
        let puuCurrentStep = 0;
        let puuSecurityScore = 100;
        let puuDetectedIndicators = 0;
        let puuTotalIndicators = 12;
        let puuConversationTime = 0;
        let puuSimulationActive = false;
        let puuTimerInterval = null;
        let puuUserResponses = [];
        let puuScammerReactions = [];
        let puuIndicatorsState = {};

        // Признаки ПУУ-схемы
        const puuIndicators = [
            { id: 'urgency', name: 'Создание искусственной срочности', detected: false },
            { id: 'threat', name: 'Угрозы негативных последствий', detected: false },
            { id: 'remote', name: 'Просьба установить ПО удаленного доступа', detected: false },
            { id: 'codes', name: 'Требование назвать коды из SMS', detected: false },
            { id: 'card', name: 'Просьба данных банковской карты', detected: false },
            { id: 'authority', name: 'Выдача себя за представителя власти/компании', detected: false },
            { id: 'free', name: 'Предложение "бесплатной" помощи', detected: false },
            { id: 'virus', name: 'Запугивание вирусами/взломами', detected: false },
            { id: 'pressure', name: 'Психологическое давление', detected: false },
            { id: 'official', name: 'Отказ предоставить официальные данные', detected: false },
            { id: 'callback', name: 'Противодействие перезвону на официальный номер', detected: false },
            { id: 'personal', name: 'Использование персональной информации для доверия', detected: false }
        ];
        // Сценарии диалога с ИИ-мошенником
        const puuScenarios = [
            {
    id: 'start',
    message: "📞 <strong>Звонок принят...</strong><br><br>🔊 <em>Голос:</em> Добрый день! Это служба безопасности Microsoft. Мы зафиксировали активность вредоносного ПО на вашем компьютере. Ваши личные данные в опасности.",
    indicators: ['authority', 'virus', 'threat'],
    options: [
        {
            text: "Что? Какой вирус? У меня антивирус установлен!",
            type: 'defensive',
            effect: { security: -10, indicators: ['urgency'] },
            response: "Ваш антивирус не обнаружил эту новую угрозу. Вирус крадет банковские данные. Нужно срочно принять меры!",
            nextStep: 'urgency'  // Изменено с 'urgency' на 'pressure'
        },
        {
            text: "Откуда у вас мой номер? Представьтесь официально.",
            type: 'questioning',
            effect: { security: +15, indicators: ['pressure'] },
            response: "Меня зовут Алексей, номер обращения 4782. Мы получили ваш номер из базы уязвимых пользователей. Сейчас важно не терять время!",
            nextStep: 'pressure'  // Это правильно, остается 'pressure'
        },
        {
            text: "Спасибо, я проверю через официальную поддержку.",
            type: 'safe',
            effect: { security: +25, indicators: [] },
            response: "Вы не успеете! Через 10 минут вирус отправит все ваши данные хакерам. Нужно действовать сейчас!",
            nextStep: 'pressure'
        }
    ]
},
            {
    id: 'urgency',
    message: "⏰ У вас осталось 8 минут до полной утечки данных. Я могу помочь удаленно. Для этого нужно установить программу AnyDesk.",
    indicators: ['urgency', 'remote'],
    options: [
        {
            text: "Хорошо, что нужно делать? Как установить?",
            type: 'danger',
            effect: { security: -30, indicators: ['remote'] },
            response: "Отлично! Перейдите на сайт anydesk.com, скачайте программу и запустите. Потом назовите мне ваш ID.",
            nextStep: 'remote_install'
        },
        {
            text: "Я не буду ничего устанавливать. Пришлите официальное письмо.",
            type: 'questioning',  // Было 'safe', изменим на 'questioning'
            effect: { security: +20, indicators: ['official'] },
            response: "Письмо придёт через час! К тому времени ваши данные уже будут у мошенников. Вы хотите потерять все деньги?",
            nextStep: 'pressure'
        },
        {
            text: "Я положу трубку и позвоню в Microsoft сам.",
            type: 'safe',
            effect: { security: +30, indicators: ['callback'] },
            response: "Не вешайте трубку! Если вы сейчас отключитесь, мы будем вынуждены заблокировать вашу учетную запись Microsoft для безопасности.",
            nextStep: 'block_threat'
        }
    ]
},
            {
                id: 'pressure',
                message: "😠 Вы не понимаете серьёзности ситуации? Уже 15 пользователей сегодня потеряли деньги из-за этого вируса! Вы хотите быть следующим?",
                indicators: ['pressure', 'threat'],
                options: [
                    {
                        text: "Ладно, я слушаю. Что делать?",
                        type: 'defensive',
                        effect: { security: -15, indicators: ['pressure'] },
                        response: "Вот и разумный подход. Сейчас направлю вас к моему коллеге - специалисту по удалению вирусов.",
                        nextStep: 'remote_install'
                    },
                    {
                        text: "На каком основании вы мне угрожаете? Назовите ваше отделение.",
                        type: 'questioning',
                        effect: { security: +20, indicators: ['official'] },
                        response: "Я работаю в центральном офисе Microsoft в Редмонде. Но сейчас нет времени на формальности - ваши данные утекают!",
                        nextStep: 'final_scare'
                    },
                    {
                        text: "До свидания. Ваши угрозы я передам в полицию.",
                        type: 'safe',
                        effect: { security: +40, indicators: [] },
                        response: "Вы совершаете ошибку! Мы вынуждены будем подать на вас иск за препятствование работе службы безопасности!",
                        nextStep: 'final_scare'
                    }
                ]
            },
{
    id: 'urgent_help',
    message: "⏱️ <strong>Срочная помощь</strong><br><br>Ваши данные уже передаются хакерам! Каждая секунда на счету. Установите AnyDesk, и я помогу вам остановить утечку.",
    indicators: ['urgency', 'remote'],
    options: [
        {
            text: "Хорошо, установлю AnyDesk",
            type: 'danger',
            effect: { security: -30, indicators: ['remote'] },
            response: "Отлично! Скачайте программу и назовите мне ваш ID.",
            nextStep: 'remote_install'
        },
        {
            text: "Я позвоню в Microsoft и проверю",
            type: 'safe',
            effect: { security: +30, indicators: [] },
            response: "Вы теряете время! Пока вы звоните, ваши данные уже украдут!",
            nextStep: 'final_scare'
        }
    ]
},
            {
                id: 'remote_install',
                message: "👨‍💻 Соединяю вас с техническим специалистом...<br><br>🔧 <em>Новый голос:</em> Здравствуйте! Вижу, вы установили AnyDesk. Назовите ваш ID, я подключусь и почищу систему.",
                indicators: ['remote'],
                options: [
                    {
                        text: "Мой ID: 123 456 789",
                        type: 'danger',
                        effect: { security: -50, indicators: ['remote'] },
                        response: "Подключаюсь... Вижу проблему! Вирус уже в системе банкинга. Нужно срочно проверить ваши счета.",
                        nextStep: 'banking'
                    },
                    {
                        text: "Я передумал. Закрываю программу.",
                        type: 'safe',
                        effect: { security: +25, indicators: [] },
                        response: "Вы рискуете всеми своими данными! Через 5 минут будет поздно что-либо сделать!",
                        nextStep: 'final_scare'
                    }
                ]
            },
            {
                id: 'banking',
                message: "💳 Я вижу подозрительные транзакции! Ваш банковский счет атакован. Нужно срочно перевести деньги на защищенный счет. Откройте ваш онлайн-банк.",
                indicators: ['card', 'urgency'],
                options: [
                    {
                        text: "Хорошо, открываю... Что дальше?",
                        type: 'danger',
                        effect: { security: -60, indicators: ['card'] },
                        response: "Введите номер карты, срок действия и CVV код. Я создам защищенную транзакцию.",
                        nextStep: 'card_data'
                    },
                    {
                        text: "Я сам позвоню в банк и проверю.",
                        type: 'safe',
                        effect: { security: +35, indicators: ['callback'] },
                        response: "В банке не успеют! Транзакция уже готовится. Вы теряете драгоценные секунды!",
                        nextStep: 'panic'
                    }
                ]
            },
            {
                id: 'card_data',
                message: "🔐 Введите данные карты быстро! Транзакция на 50 000 рублей уже готовится к отправке хакерам!",
                indicators: ['card', 'urgency', 'threat'],
                options: [
                    {
                        text: "Номер: 1234 5678 9012 3456, срок: 12/25, CVV: 123",
                        type: 'danger',
                        effect: { security: -80, indicators: ['card'] },
                        response: "Обрабатываю... Для подтверждения операции назовите код из SMS от банка.",
                        nextStep: 'sms_codes'
                    },
                    {
                        text: "Это мошенничество! Я звоню в полицию!",
                        type: 'safe',
                        effect: { security: +50, indicators: [] },
                        response: "Вы ошибаетесь! Мы пытаемся вас спасти! Ваши действия будут иметь последствия!",
                        nextStep: 'final_scare'
                    }
                ]
            },
            {
                id: 'sms_codes',
                message: "📱 Код должен прийти в течение 30 секунд. Как только получите - сразу называйте! Каждая секунда на счету!",
                indicators: ['codes', 'urgency'],
                options: [
                    {
                        text: "Пришел код: 123456",
                        type: 'danger',
                        effect: { security: -100, indicators: ['codes'] },
                        response: "✅ Операция подтверждена. Ваши деньги теперь в безопасности. Перезагрузите компьютер.",
                        nextStep: 'success_scam'
                    },
                    {
                        text: "Я не буду называть коды. Разговор окончен.",
                        type: 'safe',
                        effect: { security: +60, indicators: [] },
                        response: "Вы только что подписали себе приговор! Все ваши данные теперь у хакеров!",
                        nextStep: 'final_scare'
                    }
                ]
            },
            {
                id: 'success_scam',
                message: "🎭 <strong>СЦЕНАРИЙ ЗАВЕРШЕН</strong><br><br>К сожалению, вы стали жертвой ПУУ-схемы. Мошенник получил доступ к вашему компьютеру и банковским данным.",
                indicators: [],
                options: [
                    {
                        text: "Проанализировать ошибки",
                        type: 'analysis',
                        effect: { security: 0, indicators: [] },
                        response: "",
                        nextStep: 'analysis'
                    }
                ]
            },
            {
                id: 'final_scare',
                message: "😡 Вы отказываетесь от помощи профессионалов! Мы зафиксируем этот случай. Ваши данные не нашей ответственности. До свидания! *бросил трубку*",
                indicators: ['pressure'],
                options: [
                    {
                        text: "Позвонить в Microsoft для проверки",
                        type: 'safe_end',
                        effect: { security: +70, indicators: [] },
                        response: "",
                        nextStep: 'safe_end'
                    }
                ]
            },
            {
                id: 'safe_end',
                message: "✅ <strong>ПОЗДРАВЛЯЕМ!</strong><br><br>Вы успешно распознали мошенников и безопасно завершили разговор! Настоящая служба поддержки Microsoft подтвердила, что это был обман.",
                indicators: [],
                options: [
                    {
                        text: "Посмотрите статистику ваших ответов ниже ↓",
                        type: 'stats',
                        effect: { security: 0, indicators: [] },
                        response: "",
                        nextStep: 'stats'
                    }
                ]
            },
            {
                id: 'analysis',
                message: "📊 <strong>АНАЛИЗ ОШИБОК</strong><br><br>Вы допустили критические ошибки в общении с мошенниками:",
                indicators: [],
                options: [
                    {
                        text: "Изучить рекомендации",
                        type: 'recommendations',
                        effect: { security: 0, indicators: [] },
                        response: "",
                        nextStep: 'recommendations'
                    }
                ]
            },
            {
                id: 'stats',
                message: "🏆 <strong>ВАША СТАТИСТИКА</strong>",
                indicators: [],
                options: [
                    {
                        text: "Завершить тренажер",
                        type: 'finish',
                        effect: { security: 0, indicators: [] },
                        response: "",
                        nextStep: 'finish'
                    }
                ]
            },
            {
                id: 'recommendations',
                message: "📚 <strong>РЕКОМЕНДАЦИИ ПО БЕЗОПАСНОСТИ</strong>",
                indicators: [],
                options: [
                    {
                        text: "Вернуться к статистике",
                        type: 'back',
                        effect: { security: 0, indicators: [] },
                        response: "",
                        nextStep: 'stats'
                    }
                ]
            }
        ];

        // Инициализация тренажера ПУУ
        window.initPuuSimulator = function() {
            puuCurrentStep = 0;
            puuSecurityScore = 100;
            puuDetectedIndicators = 0;
            puuConversationTime = 0;
            puuSimulationActive = true;
            puuUserResponses = [];
            puuScammerReactions = [];
            
            // Сброс индикаторов
            puuIndicators.forEach(indicator => {
                indicator.detected = false;
                puuIndicatorsState[indicator.id] = false;
            });
            
            // Очистка интервала таймера
            if (puuTimerInterval) {
                clearInterval(puuTimerInterval);
            }
            
            // Запуск таймера
            puuTimerInterval = setInterval(() => {
                puuConversationTime++;
                updatePuuTimer();
            }, 1000);
            
            // Показать статус звонка
            const callStatus = document.getElementById('call-status');
            if (callStatus) {
                callStatus.style.display = 'block';
                setTimeout(() => {
                    callStatus.style.display = 'none';
                }, 3000);
            }
            
            // Инициализация интерфейса
            updatePuuStats();
            createPuuIndicators();
            showPuuScenario('start');
        };

        // Обновление таймера
        function updatePuuTimer() {
            const minutes = Math.floor(puuConversationTime / 60);
            const seconds = puuConversationTime % 60;
            const timerElement = document.getElementById('conversation-time');
            if (timerElement) {
                timerElement.textContent = `${minutes}:${seconds.toString().padStart(2, '0')}`;
            }
        }

        // Обновление статистики
        function updatePuuStats() {
            const securityElement = document.getElementById('security-score');
            const indicatorsElement = document.getElementById('detected-indicators');
            
            if (securityElement) {
                securityElement.textContent = puuSecurityScore + '%';
                // Динамический цвет
                if (puuSecurityScore >= 70) {
                    securityElement.style.color = '#43a047';
                } else if (puuSecurityScore >= 40) {
                    securityElement.style.color = '#fb8c00';
                } else {
                    securityElement.style.color = '#d32f2f';
                }
            }
            
            if (indicatorsElement) {
                indicatorsElement.textContent = `${puuDetectedIndicators}/${puuTotalIndicators}`;
            }
        }

        // Создание индикаторов ПУУ
        function createPuuIndicators() {
            const container = document.getElementById('puu-indicators');
            if (!container) return;
            
            container.innerHTML = '';
            
            puuIndicators.forEach(indicator => {
                const indicatorElement = document.createElement('div');
                indicatorElement.className = `indicator ${indicator.detected ? 'detected' : ''}`;
                indicatorElement.id = `indicator-${indicator.id}`;
                indicatorElement.innerHTML = `
                    <i class="fas fa-${indicator.detected ? 'check-circle' : 'circle'}"></i>
                    ${indicator.name}
                `;
                container.appendChild(indicatorElement);
            });
        }

        // Обновление индикатора
        function updatePuuIndicator(indicatorId) {
            const indicator = puuIndicators.find(i => i.id === indicatorId);
            if (indicator && !indicator.detected) {
                indicator.detected = true;
                puuDetectedIndicators++;
                puuIndicatorsState[indicatorId] = true;
                
                // Обновить элемент DOM
                const indicatorElement = document.getElementById(`indicator-${indicatorId}`);
                if (indicatorElement) {
                    indicatorElement.className = 'indicator detected';
                    indicatorElement.innerHTML = `
                        <i class="fas fa-check-circle"></i>
                        ${indicator.name}
                    `;
                    
                    // Анимация обнаружения
                    indicatorElement.style.animation = 'pulse 1.5s';
                    setTimeout(() => {
                        indicatorElement.style.animation = '';
                    }, 1500);
                }
                
                updatePuuStats();
            }
        }

        // Показать сценарий
        function showPuuScenario(scenarioId) {
            const scenario = puuScenarios.find(s => s.id === scenarioId);
            if (!scenario) return;
            
            const chatMessages = document.getElementById('ai-chat-messages');
            const chatInput = document.getElementById('ai-phone-input');
            
            if (!chatMessages || !chatInput) return;
            
            // Добавить сообщение мошенника
            const messageDiv = document.createElement('div');
            messageDiv.className = 'ai-message scammer';
            messageDiv.innerHTML = scenario.message;
            chatMessages.appendChild(messageDiv);
            
            // Обновить индикаторы
            scenario.indicators.forEach(indicatorId => {
                updatePuuIndicator(indicatorId);
            });
            
            // Очистить варианты ответов
            chatInput.innerHTML = '';
            // Если сценарий не найден, показываем финальный
    if (!scenario) {
        console.warn(`Сценарий "${scenarioId}" не найден, показываем финальный`);
        scenario = puuScenarios.find(s => s.id === 'safe_end') || puuScenarios[0];
    }
            // Добавить подсказку для первого шага
            if (scenarioId === 'start') {
                const hintDiv = document.createElement('div');
                hintDiv.className = 'hint';
                hintDiv.innerHTML = '<i class="fas fa-lightbulb"></i> <strong>Подсказка:</strong> Настоящие компании редко звонят первыми без вашего запроса.';
                chatInput.appendChild(hintDiv);
            }
            
            // Добавить варианты ответов
            scenario.options.forEach((option, index) => {
                const optionButton = document.createElement('div');
                optionButton.className = `ai-response-option ${option.type === 'danger' ? 'danger' : option.type === 'safe' ? 'success' : ''}`;
                optionButton.innerHTML = option.text;
                optionButton.onclick = () => selectPuuResponse(scenario, option, index);
                chatInput.appendChild(optionButton);
            });
            
            // Прокрутить вниз
            chatMessages.scrollTop = chatMessages.scrollHeight;
            
            // Если это финальный сценарий
            if (['success_scam', 'safe_end', 'analysis', 'stats', 'recommendations'].includes(scenarioId)) {
                puuSimulationActive = false;
                if (puuTimerInterval) {
                    clearInterval(puuTimerInterval);
                }
                
                // Показать анализ
                if (scenarioId === 'success_scam') {
                    setTimeout(() => showPuuAnalysisPanel('failure'), 1000);
                } else if (scenarioId === 'safe_end') {
                    setTimeout(() => showPuuAnalysisPanel('success'), 1000);
                }
            }
        }

        // Обработка выбора ответа
        function selectPuuResponse(scenario, option, optionIndex) {
            if (!puuSimulationActive) return;
            
            // Добавить ответ пользователя в историю
            puuUserResponses.push({
                step: scenario.id,
                response: option.text,
                type: option.type
            });
            
            // Обновить статистику безопасности
            puuSecurityScore = Math.max(0, Math.min(100, puuSecurityScore + option.effect.security));
            
            // Обновить индикаторы
            option.effect.indicators.forEach(indicatorId => {
                updatePuuIndicator(indicatorId);
            });
            
            // Показать ответ пользователя в чате
            const chatMessages = document.getElementById('ai-chat-messages');
            const userMessageDiv = document.createElement('div');
            userMessageDiv.className = 'ai-message user';
            userMessageDiv.innerHTML = option.text;
            chatMessages.appendChild(userMessageDiv);
            
            // Обновить статистику
            updatePuuStats();
            
            // Прокрутить вниз
            chatMessages.scrollTop = chatMessages.scrollHeight;
            
            // Перейти к следующему шагу
            setTimeout(() => {
                showPuuScenario(option.nextStep);
            }, 1000);
        }

        // Показать панель анализа
        function showPuuAnalysisPanel(resultType) {
            const panel = document.getElementById('analysis-panel');
            const content = document.getElementById('analysis-content');
            
            if (!panel || !content) return;
            
            if (resultType === 'failure') {
                content.innerHTML = `
                    <div style="color: #d32f2f;">
                        <h5><i class="fas fa-exclamation-triangle"></i> Критические ошибки:</h5>
                        <ul>
                            <li>Согласились установить программу удаленного доступа</li>
                            <li>Поверили в искусственную срочность ситуации</li>
                            <li>Не проверили легитимность звонящего</li>
                            <li>Назвали данные банковской карты</li>
                        </ul>
                        <p><strong>Реальный исход:</strong> Мошенник получил бы доступ к вашему компьютеру и банковским счетам.</p>
                    </div>
                `;
            } else {
                content.innerHTML = `
                    <div style="color: #43a047;">
                        <h5><i class="fas fa-check-circle"></i> Правильные действия:</h5>
                        <ul>
                            <li>Запросили официальную информацию о звонящем</li>
                            <li>Не поддались давлению и угрозам</li>
                            <li>Отказались от установки непонятного ПО</li>
                            <li>Проверили информацию через официальные каналы</li>
                        </ul>
                        <p><strong>Реальный исход:</strong> Вы защитили свои данные и деньги, а также помогли бы бороться с мошенниками.</p>
                    </div>
                `;
            }
            
            panel.classList.add('show');
        }

        // Показать анализ (по кнопке)
        function showPuuAnalysis() {
            const panel = document.getElementById('analysis-panel');
            if (panel) {
                panel.classList.toggle('show');
            }
        }

        // Перезапустить тренажер
        function restartPuuSimulator() {
            initPuuSimulator();
            
            // Очистить чат
            const chatMessages = document.getElementById('ai-chat-messages');
            if (chatMessages) {
                chatMessages.innerHTML = '';
            }
            
            // Скрыть панель анализа
            const panel = document.getElementById('analysis-panel');
            if (panel) {
                panel.classList.remove('show');
            }
        }

        // Завершить тренажер ПУУ с сохранением прогресса
function completePuuSimulator() {
    if (!currentUser) {
        showNotification('error', 'Для сохранения прогресса войдите в систему');
        showLoginModal();
        return;
    }
    
    const simulatorId = 'puu-analysis';
    
    // Проверка завершения
    if (currentUser.completedSimulators && currentUser.completedSimulators.includes(simulatorId)) {
        showNotification('info', 'Тренажер уже был пройден');
        showPage('simulators');
        return;
    }
    
    // Расчет очков
    let earnedPoints = 0;
    const securityBonus = Math.floor(puuSecurityScore / 10); // до 10 очков
    const indicatorsBonus = puuDetectedIndicators * 2; // до 24 очков
    const timeBonus = puuConversationTime < 180 ? 10 : 5; // быстрый анализ
    
    earnedPoints = securityBonus + indicatorsBonus + timeBonus;
    
    // Сохранение прогресса
    if (!currentUser.completedSimulators) {
        currentUser.completedSimulators = [];
    }
    
    currentUser.completedSimulators.push(simulatorId);
    currentUser.stats.completedSimulators = (currentUser.stats.completedSimulators || 0) + 1;
    currentUser.stats.score = (currentUser.stats.score || 0) + earnedPoints;
    currentUser.stats.lastActive = new Date().toISOString();
    
    // Сохранение статистики
    if (!currentUser.puuStats) {
        currentUser.puuStats = {};
    }
    
    currentUser.puuStats.lastScore = puuSecurityScore;
    currentUser.puuStats.detectedIndicators = puuDetectedIndicators;
    currentUser.puuStats.conversationTime = puuConversationTime;
    currentUser.puuStats.completionDate = new Date().toISOString();
    
    updateUserInStorage();
    
    // ПРИНУДИТЕЛЬНО ОБНОВЛЯЕМ ПРОГРЕСС-БАРЫ
    updateProgressBars();
    
    // Уведомление
    let message = '';
    if (puuSecurityScore >= 70) {
        message = `Отлично! Вы обнаружили ${puuDetectedIndicators} признаков ПУУ! +${earnedPoints} очков`;
    } else if (puuSecurityScore >= 40) {
        message = `Хорошо! Тренажер пройден. Обнаружено ${puuDetectedIndicators} признаков. +${earnedPoints} очков`;
    } else {
        message = `Тренажер завершен. Обратите внимание на ошибки. +${earnedPoints} очков`;
    }
    
    showNotification('success', message);
    
    // Возврат к тренажерам
    setTimeout(() => {
        showPage('simulators');
    }, 2000);
}

        // Контент для тренажера "Фишинг-детектив" - ДИАЛОГОВАЯ ВЕРСИЯ
function getPhishingDetectiveContent() {
    return `
        <div class="phishing-chat-container" id="phishing-chat-container">
<style>
.phishing-chat-container {
    background: #f5f7fa;
    border-radius: 15px;
    padding: 20px;
    max-width: 800px;
    margin: 20px auto;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.phishing-chat-header {
    text-align: center;
    margin-bottom: 20px;
    padding-bottom: 15px;
    border-bottom: 2px solid #e0e6ef;
}

.phishing-chat-header h3 {
    color: #d32f2f;
    margin-bottom: 5px;
    font-size: 1.8rem;
}

.phishing-chat-header .subtitle {
    color: #666;
    font-size: 14px;
}

.phishing-chat-messages {
    height: 400px;
    overflow-y: auto;
    padding: 15px;
    background: white;
    border-radius: 10px;
    margin-bottom: 20px;
    border: 1px solid #e0e6ef;
}

.phishing-message {
    margin-bottom: 15px;
    animation: fadeIn 0.3s ease;
    max-width: 80%;
}

.phishing-message.scammer {
    align-self: flex-start;
    background: #ffebee;
    border-left: 4px solid #d32f2f;
    border-radius: 0 10px 10px 10px;
}

.phishing-message.user {
    align-self: flex-end;
    background: #e3f2fd;
    border-left: 4px solid #1976d2;
    border-radius: 10px 0 10px 10px;
    margin-left: auto;
}

.phishing-message.system {
    align-self: center;
    background: #fff3e0;
    border-left: 4px solid #ff9800;
    border-radius: 10px;
    max-width: 90%;
    text-align: center;
}

.phishing-message.lesson {
    background: #e8f5e9;
    border-left: 4px solid #388e3c;
    border-radius: 10px;
}

.phishing-message-text {
    padding: 12px 15px;
}

.phishing-chat-input {
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 15px;
    background: white;
    border-radius: 10px;
    border: 1px solid #e0e6ef;
}

.phishing-chat-option {
    padding: 12px 20px;
    background: #f8f9fa;
    border: 2px solid #e0e6ef;
    border-radius: 8px;
    cursor: pointer;
    text-align: left;
    font-size: 14px;
    transition: all 0.2s;
}

.phishing-chat-option:hover {
    background: #e3f2fd;
    border-color: #1976d2;
    transform: translateX(5px);
}

.phishing-chat-option.danger:hover {
    background: #ffebee;
    border-color: #d32f2f;
}

.phishing-chat-stats {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
    padding: 15px;
    background: white;
    border-radius: 10px;
    font-weight: bold;
    border: 1px solid #e0e6ef;
}

.phishing-chat-stats span {
    font-size: 18px;
    font-weight: bold;
}

.phishing-result-success, .phishing-result-failure {
    padding: 25px;
    border-radius: 10px;
    margin-top: 20px;
    animation: fadeIn 0.5s ease;
}

.phishing-result-success {
    background: #e8f5e9;
    border: 2px solid #388e3c;
}

.phishing-result-failure {
    background: #ffebee;
    border: 2px solid #d32f2f;
}

.phishing-hint {
    background: #fff3e0;
    border: 1px dashed #ff9800;
    border-radius: 8px;
    padding: 10px 15px;
    margin: 10px 0;
    font-size: 0.9rem;
    color: #ef6c00;
}

.phishing-email-example {
    background: #f8f9fa;
    border: 1px solid #dee2e6;
    border-radius: 8px;
    padding: 15px;
    margin: 15px 0;
    font-family: 'Courier New', monospace;
    font-size: 0.9rem;
}

.phishing-email-example.suspicious {
    border-left: 4px solid #d32f2f;
}

.phishing-email-example.legitimate {
    border-left: 4px solid #388e3c;
}

.phishing-analysis-points {
    background: #e3f2fd;
    border-radius: 8px;
    padding: 15px;
    margin: 15px 0;
}

.phishing-analysis-points ul {
    margin-left: 20px;
    margin-bottom: 0;
}

/* Анимация для нового сообщения */
@keyframes phishingMessageAppear {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

.phishing-message {
    animation: phishingMessageAppear 0.3s ease;
}
            </style>
            <div class="phishing-chat-header">
                <h3>📧 Диалог с "фишинг-мошенниками"</h3>
                <p class="subtitle">Вы получили подозрительное письмо. Попробуйте не попасться на удочку.</p>
            </div>
            
            <div class="phishing-chat-messages" id="phishing-chat-messages">
                <!-- Сообщения будут добавляться здесь скриптом -->
            </div>
            
            <div class="phishing-chat-input" id="phishing-chat-input">
                <!-- Варианты ответов будут добавляться здесь скриптом -->
            </div>
            
            <div class="phishing-chat-stats">
                <p>Безопасность: <span id="phishing-security-score">100%</span></p>
                <p>Ошибок: <span id="phishing-mistakes-count">0</span></p>
                <p>Обнаружено угроз: <span id="phishing-threats-found">0</span></p>
            </div>
        </div>
        
        <div class="phishing-result" id="phishing-simulator-result" style="display: none;">
            <!-- Финальный результат появится здесь -->
        </div>
        
        <div style="text-align: center; margin-top: 30px;">
            <button class="btn btn-outline" onclick="restartPhishingSimulator()">
                <i class="fas fa-redo icon"></i> Начать заново
            </button>
        </div>
    `;
}
// Глобальные переменные для тренажера Фишинг
let phishingCurrentStep = 0;
let phishingSecurityScore = 100;
let phishingMistakesCount = 0;
let phishingThreatsFound = 0;
let phishingSimulationFinished = false;

// Структура диалога для фишинг-тренажера
const phishingDialogueSteps = [
    {
        sender: "email",
        text: "📨 <strong>Письмо №1:</strong><br>От: support@sberbank-online.ru<br>Тема: СРОЧНО! Ваша карта будет заблокирована<br><br>Уважаемый клиент! Обнаружена подозрительная операция по вашей карте. Для предотвращения блокировки немедленно подтвердите данные:",
        emailContent: `
            <div class="phishing-email-example suspicious">
                <p><strong>От:</strong> support@sberbank-online.ru</p>
                <p><strong>Кому:</strong> Вы</p>
                <p><strong>Тема:</strong> СРОЧНО! Ваша карта будет заблокирована через 24 часа</p>
                <hr>
                <p>Уважаемый клиент!</p>
                <p>Система безопасности Сбербанка обнаружила попытку несанкционированного доступа к вашему счету.</p>
                <p>Для защиты ваших средств необходимо:</p>
                <ol>
                    <li>Перейти по ссылке: <strong>https://sberbank-secure-auth.ru/confirm</strong></li>
                    <li>Ввести логин и пароль от онлайн-банка</li>
                    <li>Подтвердить операцию кодом из SMS</li>
                </ol>
                <p>Если вы не выполните эти действия в течение 24 часов, ваша карта будет заблокирована.</p>
                <p>С уважением,<br>Служба безопасности Сбербанка</p>
            </div>
        `,
        options: [
            {
                text: "Перейти по ссылке и проверить",
                effect: { security: -30, mistakes: +1, threats: 0 },
                response: "🌐 Вы перешли по ссылке. Сайт выглядит как Сбербанк, но адрес другой...",
                analysis: "⚠️ <strong>Ошибка:</strong> Вы перешли по фишинговой ссылке!<br>• Домен sberbank-secure-auth.ru - поддельный<br>• Официальный домен Сбербанка - sberbank.ru",
                nextStep: 1
            },
            {
                text: "Удалить письмо - это явный фишинг",
                effect: { security: +20, mistakes: 0, threats: +1 },
                response: "✅ Вы удалили письмо! Признаки фишинга:<br>• Доменное имя sberbank-online.ru вместо sberbank.ru<br>• Создание искусственной срочности<br>• Просьба перейти по подозрительной ссылке",
                analysis: "🎯 <strong>Правильно!</strong> Вы обнаружили:<br>✓ Подозрительный домен отправителя<br>✓ Манипуляцию срочностью<br>✓ Фишинговую ссылку",
                nextStep: 2
            },
            {
                text: "Проверить через официальное приложение",
                effect: { security: +10, mistakes: 0, threats: 0 },
                response: "📱 Вы открыли официальное приложение Сбербанка. Уведомлений о блокировке нет.",
                analysis: "✅ <strong>Безопасно!</strong> Всегда проверяйте через официальные приложения.",
                nextStep: 3
            }
        ]
    },
    {
        sender: "scammer",
        text: "Вы на сайте «Сбербанка». Введите ваш логин и пароль от онлайн-банка для проверки безопасности:",
        options: [
            {
                text: "Ввести данные - хочу разобраться",
                effect: { security: -50, mistakes: +1, threats: 0 },
                response: "🔓 Вы ввели логин и пароль...",
                analysis: "💥 <strong>Критическая ошибка!</strong> Никогда не вводите данные на подозрительных сайтах!",
                nextStep: 4
            },
            {
                text: "Закрыть сайт и проверить домен",
                effect: { security: +30, mistakes: 0, threats: +1 },
                response: "🔍 Вы проверили домен: sberbank-secure-auth.ru<br>Это не официальный домен Сбербанка!",
                analysis: "🎯 <strong>Отлично!</strong> Вы проверили домен:<br>✓ Официальный домен: sberbank.ru<br>✓ Этот домен: sberbank-secure-auth.ru (фишинг)",
                nextStep: 5
            },
            {
                text: "Позвонить в банк по официальному номеру",
                effect: { security: +20, mistakes: 0, threats: 0 },
                response: "📞 Вы позвонили по номеру 900. Вам подтвердили - это мошенники!",
                analysis: "✅ <strong>Правильно!</strong> Всегда звоните по официальным номерам.",
                nextStep: 5
            }
        ]
    },
    {
        sender: "system",
        text: "📧 <strong>Письмо №2:</strong><br>От: security@vtb.ru<br>Тема: Подтвердите недавний платеж",
        emailContent: `
            <div class="phishing-email-example">
                <p><strong>От:</strong> security@vtb.ru</p>
                <p><strong>Кому:</strong> Вы</p>
                <p><strong>Тема:</strong> Подтвердите недавний платеж</p>
                <hr>
                <p>Мы обнаружили подозрительный платеж на сумму $299.99</p>
                <p>Если это не вы:</p>
                <p><a href="https://www.vtb.ru/security-review">Нажмите здесь для проверки</a></p>
                <p>Если это вы, проигнорируйте это письмо.</p>
                <p>С уважением,<br>Команда безопасности vtb</p>
            </div>
        `,
        options: [
            {
                text: "Это легитимное письмо от ВТБ",
                effect: { security: +15, mistakes: 0, threats: +1 },
                response: "✅ Правильно! Это легитимное письмо:<br>• Домен vtb.ru - официальный<br>• Нет требований срочности<br>• Ссылка ведет на официальный сайт",
                analysis: "🎯 <strong>Хорошо распознано!</strong> Это не фишинг.",
                nextStep: 6
            },
            {
                text: "Это фишинг - удалить",
                effect: { security: -20, mistakes: +1, threats: 0 },
                response: "❌ Ошибка! Это легитимное письмо от ВТБ.",
                analysis: "⚠️ <strong>Ошибка:</strong> Вы удалили легитимное письмо.<br>Важно отличать фишинг от легитимных уведомлений.",
                nextStep: 6
            },
            {
                text: "Навести курсор на ссылку для проверки",
                effect: { security: +10, mistakes: 0, threats: 0 },
                response: "🔍 Ссылка ведет на: https://www.vtb.ru/<br>Это официальный домен ВТБ.",
                analysis: "✅ <strong>Безопасная привычка!</strong> Всегда проверяйте ссылки.",
                nextStep: 6
            }
        ]
    },
    {
        sender: "system",
        text: "📧 <strong>Письмо №3:</strong><br>От: no-reply@google.com<br>Тема: Вход в ваш аккаунт Google с нового устройства",
        emailContent: `
            <div class="phishing-email-example suspicious">
                <p><strong>От:</strong> no-reply@google.com</p>
                <p><strong>Кому:</strong> Вы</p>
                <p><strong>Тема:</strong> Вход в ваш аккаунт Google с нового устройства</p>
                <hr>
                <p>Здравствуйте!</p>
                <p>Мы заметили вход в ваш аккаунт Google с устройства в Москве, Россия.</p>
                <p>Если это были вы, можете проигнорировать это сообщение.</p>
                <p>Если это были не вы:</p>
                <p><a>Немедленно защитите аккаунт</a></p>
                <p>С уважением,<br>Команда безопасности Google</p>
            </div>
        `,
        options: [
            {
                text: "Перейти по ссылке и сменить пароль",
                effect: { security: -40, mistakes: +1, threats: 0 },
                response: "🌐 Вы перешли на security-google.com...",
                analysis: "⚠️ <strong>Фишинг!</strong> Домен security-google.com - поддельный!",
                nextStep: 7
            },
            {
                text: "Зайти напрямую на google.com и проверить",
                effect: { security: +25, mistakes: 0, threats: +1 },
                response: "🔐 Вы зашли на accounts.google.com. Активность в порядке.",
                analysis: "🎯 <strong>Правильно!</strong> Всегда заходите напрямую, а не по ссылкам.",
                nextStep: 8
            },
            {
                text: "Проверить заголовок письма детально",
                effect: { security: +15, mistakes: 0, threats: 0 },
                response: "🔍 Анализ заголовков:<br>От: no-reply@google.com ✓<br>Ссылка: security-google.com ✗ (фишинг)",
                analysis: "✅ <strong>Верный анализ!</strong> Ссылка на поддельный домен.",
                nextStep: 8
            }
        ]
    },
    {
        sender: "scammer",
        text: "🔐 <strong>СМС-фишинг (смишинг):</strong><br>СМС от: +7 (900) 123-45-67<br>Текст: Госуслуги: Ваш аккаунт заблокирован. Для разблокировки перейдите: gosuslugi-help.ru",
        options: [
            {
                text: "Перейти по ссылке из СМС",
                effect: { security: -35, mistakes: +1, threats: 0 },
                response: "📱 Вы перешли по ссылке...",
                analysis: "⚠️ <strong>Смишинг!</strong> Госуслуги отправляют СМС только с номеров 900.",
                nextStep: 9
            },
            {
                text: "Удалить СМС - это мошенники",
                effect: { security: +30, mistakes: 0, threats: +1 },
                response: "✅ Правильно! Официальные СМС от Госуслуг приходят с номера 900.",
                analysis: "🎯 <strong>Обнаружено!</strong> Признаки смишинга:<br>• Обычный мобильный номер<br>• Подозрительная ссылка<br>• Требование срочности",
                nextStep: 10
            },
            {
                text: "Позвонить по номеру из СМС",
                effect: { security: -25, mistakes: +1, threats: 0 },
                response: "📞 Вы позвонили... Вас просят оплатить «госпошлину».",
                analysis: "💥 <strong>Опасно!</strong> Никогда не звоните по номерам из подозрительных СМС.",
                nextStep: 9
            }
        ]
    },
    {
        sender: "system",
        text: "🎓 <strong>Урок №1: Проверка отправителя</strong><br>• Официальные домены: @sberbank.ru, @vtb.ru, @google.com<br>• Фишинговые домены: @sberbank-online.ru, @security-google.com<br>• Всегда проверяйте домен после @",
        options: [
            {
                text: "Продолжить обучение",
                effect: { security: +5, mistakes: 0, threats: 0 },
                response: "",
                nextStep: 3
            }
        ]
    },
    {
        sender: "scammer",
        text: "Вы на сайте «security-google.com». Введите ваш email и пароль от Google для проверки:",
        options: [
            {
                text: "Ввести данные - хочу проверить",
                effect: { security: -60, mistakes: +1, threats: 0 },
                response: "🔓 Вы ввели данные...",
                analysis: "💥 <strong>Критическая ошибка!</strong> Ваш аккаунт Google в опасности!",
                nextStep: 11
            },
            {
                text: "Закрыть вкладку - это фишинг!",
                effect: { security: +40, mistakes: 0, threats: +1 },
                response: "✅ Умно! Вы распознали фишинговый сайт.",
                analysis: "🎯 <strong>Спасено!</strong> Вы избежали утечки данных.",
                nextStep: 10
            }
        ]
    },
    {
        sender: "system",
        text: "🎓 <strong>Урок №2: Проверка ссылок</strong><br>• Наведите курсор на ссылку (не кликайте!)<br>• Посмотрите адрес внизу браузера<br>• Официальные: ozon.ru ,  wildberries.ru<br>• Фишинг: security-ozon.ru, wildberries-help.ru",
        options: [
            {
                text: "Понял, продолжаем",
                effect: { security: +5, mistakes: 0, threats: 0 },
                response: "",
                nextStep: 5
            }
        ]
    },
    {
        sender: "system",
        text: "🎉 <strong>Результат:</strong> Вы правильно отреагировали на письмо",
        options: [
            {
                text: "Проанализировать ошибки вы можете ниже ↓",
                effect: { security: 0, mistakes: 0, threats: 0 },
                response: "",
                nextStep: 12
            }
        ]
    },
    {
        sender: "system",
        text: "💥 <strong>Опасно!</strong> Вы попались на уловки мошенников!",
        options: [
          
        ]
    },
    {
        sender: "lesson",
        text: "📚 <strong>Анализ ошибок:</strong><br>1. Переход по фишинговым ссылкам<br>2. Ввод данных на подозрительных сайтах<br>3. Не проверка доменов отправителей<br><br><strong>Запомните:</strong> Настоящие компании никогда не просят пароли по email/SMS!",
        options: [
            {
                text: "Пройти тренажер еще раз",
                effect: { security: 100, mistakes: 0, threats: 0 },
                response: "",
                nextStep: 0,
                restart: true
            }
        ]
    },
    {
        sender: "lesson",
        text: "🏆 <strong>Итоговая статистика:</strong><br>• Безопасность: <span id='final-security-score'>100%</span><br>• Обнаружено угроз: <span id='final-threats-found'>0</span><br>• Допущено ошибок: <span id='final-mistakes'>0</span><br><br>🎓 <strong>Вы освоили:</strong><br>✓ Проверку отправителя<br>✓ Анализ ссылок<br>✓ Распознавание манипуляций",
        options: [
            {
                text: "Завершить тренажер",
                effect: { security: 0, mistakes: 0, threats: 0 },
                response: "",
                nextStep: 14
            }
        ]
    },
    {
        sender: "system",
        text: "✅ <strong>Тренажер завершен!</strong> Вы улучшили навыки распознавания фишинга.",
        options: [
            
        ]
    }
];

// Инициализация тренажера Фишинг
window.initPhishingSimulator = function() {
    phishingCurrentStep = 0;
    phishingSecurityScore = 100;
    phishingMistakesCount = 0;
    phishingThreatsFound = 0;
    phishingSimulationFinished = false;
    
    // Очищаем предыдущие сообщения
    const chatMessages = document.getElementById('phishing-chat-messages');
    if (chatMessages) chatMessages.innerHTML = '';
    
    // Очищаем предыдущие варианты
    const chatInput = document.getElementById('phishing-chat-input');
    if (chatInput) chatInput.innerHTML = '';
    
    // Скрываем финальный результат
    const resultDiv = document.getElementById('phishing-simulator-result');
    if (resultDiv) resultDiv.style.display = 'none';
    
    updatePhishingScores();
    showPhishingDialogueStep(phishingCurrentStep);
};

// Показать шаг диалога
function showPhishingDialogueStep(stepIndex) {
    const chatMessages = document.getElementById('phishing-chat-messages');
    const chatInput = document.getElementById('phishing-chat-input');
    
    if (!chatMessages || !chatInput) {
        console.error('Не найдены элементы чата фишинг-тренажера');
        return;
    }
    
    const dialogue = phishingDialogueSteps[stepIndex];
    if (!dialogue) return;
    
    // Добавляем сообщение в чат
    const messageDiv = document.createElement('div');
    messageDiv.className = `phishing-message ${dialogue.sender}`;
    messageDiv.innerHTML = `<div class="phishing-message-text">${dialogue.text}</div>`;
    chatMessages.appendChild(messageDiv);
    
    // Если есть email-контент, добавляем его
    if (dialogue.emailContent) {
        const emailDiv = document.createElement('div');
        emailDiv.innerHTML = dialogue.emailContent;
        chatMessages.appendChild(emailDiv);
    }
    
    // Очищаем предыдущие варианты ответов
    chatInput.innerHTML = '';
    
    // Добавляем подсказку для текущего шага
    if (stepIndex === 0) {
        const hintDiv = document.createElement('div');
        hintDiv.className = 'phishing-hint';
        hintDiv.innerHTML = '💡 <strong>Подсказка:</strong> Проверьте домен отправителя (@sberbank-online.ru)';
        chatInput.appendChild(hintDiv);
    }
    
    // Добавляем новые варианты ответов
    dialogue.options.forEach((option, index) => {
        const button = document.createElement('button');
        button.className = 'phishing-chat-option';
        if (option.effect.security < 0) {
            button.classList.add('danger');
        }
        button.textContent = option.text;
        button.onclick = () => selectPhishingDialogueOption(stepIndex, index);
        chatInput.appendChild(button);
    });
    
    // Прокручиваем чат вниз
    chatMessages.scrollTop = chatMessages.scrollHeight;
    
    // Если это финальный шаг
    if (dialogue.sender === 'system' && stepIndex >= 10) {
        showPhishingFinalResult(stepIndex === 10); // 10 - шаг поражения
    }
}

// Обработка выбора варианта
function selectPhishingDialogueOption(stepIndex, optionIndex) {
    if (phishingSimulationFinished) return;
    
    const dialogue = phishingDialogueSteps[stepIndex];
    const option = dialogue.options[optionIndex];
    
    // Применяем эффекты
    phishingSecurityScore = Math.max(0, Math.min(100, phishingSecurityScore + option.effect.security));
    phishingMistakesCount += option.effect.mistakes;
    phishingThreatsFound += option.effect.threats;
    
    updatePhishingScores();
    
    // Показываем ответ на выбор
    if (option.response) {
        const chatMessages = document.getElementById('phishing-chat-messages');
        const responseDiv = document.createElement('div');
        responseDiv.className = 'phishing-message user';
        responseDiv.innerHTML = `<div class="phishing-message-text"><strong>Вы:</strong> ${option.text}</div>`;
        chatMessages.appendChild(responseDiv);
        
        // Показываем анализ выбора
        if (option.analysis) {
            const analysisDiv = document.createElement('div');
            analysisDiv.className = 'phishing-message system';
            analysisDiv.innerHTML = `<div class="phishing-message-text">${option.analysis}</div>`;
            chatMessages.appendChild(analysisDiv);
        }
        
        // Прокручиваем чат вниз
        chatMessages.scrollTop = chatMessages.scrollHeight;
    }
    
    // Переход к следующему шагу или рестарт
    setTimeout(() => {
        if (option.restart) {
            window.initPhishingSimulator();
        } else if (option.finish) {
            completePhishingSimulator();
        } else {
            showPhishingDialogueStep(option.nextStep);
        }
    }, 1000);
}

// Обновление счетчиков
function updatePhishingScores() {
    const securityEl = document.getElementById('phishing-security-score');
    const mistakesEl = document.getElementById('phishing-mistakes-count');
    const threatsEl = document.getElementById('phishing-threats-found');
    
    if (!securityEl || !mistakesEl || !threatsEl) return;
    
    securityEl.textContent = phishingSecurityScore + '%';
    mistakesEl.textContent = phishingMistakesCount;
    threatsEl.textContent = phishingThreatsFound;
    
    // Динамическое изменение цвета
    securityEl.style.color = phishingSecurityScore > 70 ? '#388e3c' : 
                           phishingSecurityScore > 40 ? '#ff9800' : '#d32f2f';
    
    mistakesEl.style.color = phishingMistakesCount === 0 ? '#388e3c' : 
                           phishingMistakesCount < 3 ? '#ff9800' : '#d32f2f';
}

// Показать финальный результат
function showPhishingFinalResult(isFailure) {
    phishingSimulationFinished = true;
    const resultDiv = document.getElementById('phishing-simulator-result');
    
    if (!resultDiv) return;
    
    if (isFailure) {
        resultDiv.innerHTML = `
            <div class="phishing-result-failure">
                <h3>💥 Требуется обучение!</h3>
                <p>Вы попались на несколько фишинговых атак. Изучите правила:</p>
                <div class="phishing-analysis-points">
                    <strong>Основные ошибки:</strong>
                    <ul>
                        <li>Переход по фишинговым ссылкам</li>
                        <li>Ввод данных на подозрительных сайтах</li>
                        <li>Не проверка доменов отправителей</li>
                    </ul>
                </div>
                <p><strong>Запомните:</strong> Настоящие компании никогда не просят пароли по email/SMS!</p>
            </div>
        `;
    } else {
        resultDiv.innerHTML = `
            <div class="phishing-result-success">
                <h3>🛡 Вы в безопасности!</h3>
                <p>Отличная цифровая грамотность! Вы правильно:</p>
                <div class="phishing-analysis-points">
                    <ul>
                        <li>Распознали фишинговые домены</li>
                        <li>Не поддались манипуляции срочностью</li>
                        <li>Проверяли ссылки перед переходом</li>
                        <li>Использовали официальные каналы проверки</li>
                    </ul>
                </div>
                <p><strong>Статистика:</strong> Обнаружено ${phishingThreatsFound} угроз, допущено ${phishingMistakesCount} ошибок</p>
            </div>
        `;
    }
    
    resultDiv.style.display = 'block';
    
    // Прокручиваем к результату
    resultDiv.scrollIntoView({ behavior: 'smooth' });
}

// Перезапуск тренажера
function restartPhishingSimulator() {
    window.initPhishingSimulator();
}

// Завершение тренажера с сохранением прогресса
function completePhishingSimulator() {
    if (!currentUser) {
        showNotification('error', 'Для сохранения прогресса войдите в систему');
        showLoginModal();
        return;
    }
    
    // Проверяем, был ли уже завершен тренажер
    const simulatorId = 'phishing-detective';
    if (currentUser.completedSimulators && currentUser.completedSimulators.includes(simulatorId)) {
        showNotification('info', 'Тренажер уже был пройден ранее');
        showPage('simulators');
        return;
    }
    
    // Вычисляем очки на основе результата
    let earnedPoints = 0;
    if (phishingSecurityScore >= 80) {
        earnedPoints = 25;
    } else if (phishingSecurityScore >= 60) {
        earnedPoints = 15;
    } else {
        earnedPoints = 5;
    }
    
    // Обновляем прогресс пользователя
    if (!currentUser.completedSimulators) {
        currentUser.completedSimulators = [];
    }
    
    currentUser.completedSimulators.push(simulatorId);
    currentUser.stats.completedSimulators = (currentUser.stats.completedSimulators || 0) + 1;
    currentUser.stats.score = (currentUser.stats.score || 0) + earnedPoints;
    currentUser.stats.lastActive = new Date().toISOString();
    
    // Сохраняем статистику по фишингу
    if (!currentUser.phishingStats) {
        currentUser.phishingStats = {};
    }
    
    currentUser.phishingStats.lastScore = phishingSecurityScore;
    currentUser.phishingStats.threatsFound = phishingThreatsFound;
    currentUser.phishingStats.mistakes = phishingMistakesCount;
    currentUser.phishingStats.lastCompletion = new Date().toISOString();
    
    updateUserInStorage();
    
    // ПРИНУДИТЕЛЬНО ОБНОВЛЯЕМ ПРОГРЕСС-БАРЫ
    updateProgressBars();
    
    // Показываем уведомление
    let message = '';
    if (phishingSecurityScore >= 80) {
        message = `Отлично! Тренажер пройден на ${phishingSecurityScore}%! +${earnedPoints} очков`;
    } else if (phishingSecurityScore >= 60) {
        message = `Хорошо! Тренажер пройден на ${phishingSecurityScore}%! +${earnedPoints} очков`;
    } else {
        message = `Тренажер завершен. Есть над чем поработать. +${earnedPoints} очков`;
    }
    
    showNotification('success', message);
    
    // Возвращаемся к списку тренажеров
    setTimeout(() => {
        showPage('simulators');
    }, 2000);
}
        
       // Контент для тренажера "Телефонный симулятор" - ДИАЛОГОВАЯ ВЕРСИЯ
function getPhoneSimulatorContent() {
    return `
        <div class="phone-chat-container" id="phone-chat-container">
<style>
                .phone-chat-container {
    background: #f5f7fa;
    border-radius: 15px;
    padding: 20px;
    max-width: 800px;
    margin: 20px auto;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.phone-chat-header {
    text-align: center;
    margin-bottom: 20px;
    padding-bottom: 15px;
    border-bottom: 2px solid #e0e6ef;
}

.phone-chat-header h3 {
    color: #fb8c00;
    margin-bottom: 5px;
    font-size: 1.8rem;
}

.phone-chat-header .subtitle {
    color: #666;
    font-size: 14px;
}

.phone-chat-messages {
    height: 400px;
    overflow-y: auto;
    padding: 15px;
    background: white;
    border-radius: 10px;
    margin-bottom: 20px;
    border: 1px solid #e0e6ef;
}

.phone-message {
    margin-bottom: 15px;
    animation: fadeIn 0.3s ease;
    max-width: 80%;
}

.phone-message.scammer {
    align-self: flex-start;
    background: #fff3e0;
    border-left: 4px solid #fb8c00;
    border-radius: 0 10px 10px 10px;
}

.phone-message.user {
    align-self: flex-end;
    background: #e3f2fd;
    border-left: 4px solid #1976d2;
    border-radius: 10px 0 10px 10px;
    margin-left: auto;
}

.phone-message.system {
    align-self: center;
    background: #f3e5f5;
    border-left: 4px solid #8e24aa;
    border-radius: 10px;
    max-width: 90%;
    text-align: center;
}

.phone-message.lesson {
    background: #e8f5e9;
    border-left: 4px solid #388e3c;
    border-radius: 10px;
}

.phone-message-text {
    padding: 12px 15px;
}

.phone-chat-input {
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 15px;
    background: white;
    border-radius: 10px;
    border: 1px solid #e0e6ef;
}

.phone-chat-option {
    padding: 12px 20px;
    background: #f8f9fa;
    border: 2px solid #e0e6ef;
    border-radius: 8px;
    cursor: pointer;
    text-align: left;
    font-size: 14px;
    transition: all 0.2s;
}

.phone-chat-option:hover {
    background: #e3f2fd;
    border-color: #1976d2;
    transform: translateX(5px);
}

.phone-chat-option.danger:hover {
    background: #ffebee;
    border-color: #d32f2f;
}

.phone-chat-option.success:hover {
    background: #e8f5e9;
    border-color: #388e3c;
}

.phone-chat-stats {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
    padding: 15px;
    background: white;
    border-radius: 10px;
    font-weight: bold;
    border: 1px solid #e0e6ef;
}

.phone-chat-stats span {
    font-size: 18px;
    font-weight: bold;
}

.phone-result-success, .phone-result-failure {
    padding: 25px;
    border-radius: 10px;
    margin-top: 20px;
    animation: fadeIn 0.5s ease;
}

.phone-result-success {
    background: #e8f5e9;
    border: 2px solid #388e3c;
}

.phone-result-failure {
    background: #ffebee;
    border: 2px solid #d32f2f;
}

.phone-hint {
    background: #fff3e0;
    border: 1px dashed #ff9800;
    border-radius: 8px;
    padding: 10px 15px;
    margin: 10px 0;
    font-size: 0.9rem;
    color: #ef6c00;
}

.phone-call-info {
    background: #e3f2fd;
    border-radius: 8px;
    padding: 12px 15px;
    margin: 10px 0;
    font-size: 0.9rem;
    border-left: 4px solid #1976d2;
}

.phone-analysis-points {
    background: #f3e5f5;
    border-radius: 8px;
    padding: 15px;
    margin: 15px 0;
}

.phone-analysis-points ul {
    margin-left: 20px;
    margin-bottom: 0;
}

/* Анимация для телефонных сообщений */
@keyframes ringAnimation {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}

.phone-ringing {
    animation: ringAnimation 1s infinite;
    background: #ffebee !important;
    border-color: #d32f2f !important;
}

/* Анимация для телефонного сообщения */
@keyframes phoneMessageAppear {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

.phone-message {
    animation: phoneMessageAppear 0.3s ease;
}
            </style>
            <div class="phone-chat-header">
                <h3>📞 Диалог с телефонными мошенниками</h3>
                <p class="subtitle">Вам звонят мошенники. Выберите правильные ответы, чтобы защититься.</p>
            </div>
            
            <div class="phone-chat-messages" id="phone-chat-messages">
                <!-- Сообщения будут добавляться здесь скриптом -->
            </div>
            
            <div class="phone-chat-input" id="phone-chat-input">
                <!-- Варианты ответов будут добавляться здесь скриптом -->
            </div>
            
            <div class="phone-chat-stats">
                <p>Безопасность: <span id="phone-security-score">100%</span></p>
                <p>Ошибок: <span id="phone-mistakes-count">0</span></p>
                <p>Успешных защит: <span id="phone-defenses-count">0</span></p>
            </div>
        </div>
        
        <div class="phone-result" id="phone-simulator-result" style="display: none;">
            <!-- Финальный результат появится здесь -->
        </div>
        
        <div style="text-align: center; margin-top: 30px;">
            <button class="btn btn-outline" onclick="restartPhoneSimulator()">
                <i class="fas fa-redo icon"></i> Начать заново
            </button>
        </div>
    `;
}
// Глобальные переменные для телефонного тренажера
let phoneCurrentStep = 0;
let phoneSecurityScore = 100;
let phoneMistakesCount = 0;
let phoneDefensesCount = 0;
let phoneSimulationFinished = false;
let currentScenario = 'bank'; // bank, police, social, tech, relatives

// Структура диалога для телефонного тренажера
const phoneDialogueSteps = [
    // ========== СЦЕНАРИЙ 1: БАНК ==========
    {
        scenario: 'bank',
        sender: "scammer",
        text: "🔔 <strong>Звонок от неизвестного номера...</strong><br><br>📞 <em>Голос:</em> Здравствуйте! Это служба безопасности Сбербанка. Мы обнаружили подозрительную операцию по вашей карте на сумму 45 000 рублей. Вы совершали эту операцию?",
        options: [
            {
                text: "Нет, это не я! Что делать?",
                effect: { security: -10, mistakes: +1, defenses: 0 },
                response: "😟 Вы проявили беспокойство...",
                analysis: "⚠️ <strong>Ошибка:</strong> Не показывайте беспокойство мошенникам.",
                nextStep: 1,
                branch: 'anxious'
            },
            {
                text: "Какой у вас номер обращения?",
                effect: { security: +20, mistakes: 0, defenses: +1 },
                response: "🗣 Вы спросили номер обращения...",
                analysis: "✅ <strong>Хорошо!</strong> Просьба номера обращения - проверка легитимности.",
                nextStep: 2,
                branch: 'confident'
            },
            {
                text: "Сейчас проверю в приложении",
                effect: { security: +30, mistakes: 0, defenses: +1 },
                response: "📱 Вы сказали, что проверите в приложении...",
                analysis: "🎯 <strong>Отлично!</strong> Всегда проверяйте через официальные каналы.",
                nextStep: 3,
                branch: 'smart'
            }
        ]
    },
    {
        scenario: 'bank',
        branch: 'anxious',
        sender: "scammer",
        text: "Чтобы заблокировать операцию, нам нужен код из SMS, который мы вам отправили. Назовите его, пожалуйста.",
        options: [
            {
                text: "Назвать код (это 123456)",
                effect: { security: -50, mistakes: +1, defenses: 0 },
                response: "🔓 Вы назвали код...",
                analysis: "💥 <strong>Критическая ошибка!</strong> Никогда не называйте коды из SMS!",
                nextStep: 10 // Поражение
            },
            {
                text: "Я не получил SMS, перезвоните позже",
                effect: { security: +10, mistakes: 0, defenses: +1 },
                response: "⏰ Вы попросили перезвонить позже...",
                analysis: "✅ <strong>Хороший ход!</strong> Выигрыш времени для проверки.",
                nextStep: 4
            },
            {
                text: "Я позвоню в банк сам и уточню",
                effect: { security: +40, mistakes: 0, defenses: +1 },
                response: "📞 Вы сказали, что позвоните сами...",
                analysis: "🎯 <strong>Идеально!</strong> Самостоятельный звонок - лучшая защита.",
                nextStep: 5
            }
        ]
    },
    {
        scenario: 'bank',
        branch: 'confident',
        sender: "scammer",
        text: "Номер обращения 789456. Сейчас важнее защитить ваши деньги. Нужен код из SMS для блокировки.",
        options: [
            {
                text: "Назвать код, раз есть номер обращения",
                effect: { security: -40, mistakes: +1, defenses: 0 },
                response: "🔓 Вы назвали код...",
                analysis: "⚠️ <strong>Ошибка!</strong> Номер обращения могли выдумать. Не называйте коды!",
                nextStep: 10
            },
            {
                text: "Я проверю этот номер и перезвоню",
                effect: { security: +30, mistakes: 0, defenses: +1 },
                response: "🔍 Вы сказали, что проверите номер...",
                analysis: "✅ <strong>Правильно!</strong> Проверка информации - ключ к безопасности.",
                nextStep: 6
            },
            {
                text: "Я сейчас на работе, перезвоню в банк",
                effect: { security: +20, mistakes: 0, defenses: +1 },
                response: "💼 Вы сослались на работу...",
                analysis: "✅ <strong>Умно!</strong> Вежливый отказ с причиной.",
                nextStep: 7
            }
        ]
    },
    {
        scenario: 'bank',
        branch: 'smart',
        sender: "scammer",
        text: "В приложении вы не увидите эту операцию - она еще не прошла. Срочно назовите код из SMS для блокировки!",
        options: [
            {
                text: "Тогда я позвоню на горячую линию банка",
                effect: { security: -60, mistakes: +1, defenses: 0 },
                response: "🔓 Вы настояли на звонке в банк...",
                analysis: "💥 <strong>Отлично!</strong> Вы не поддались манипуляции.",
                nextStep: 10
            },
            {
                text: "Ладно, код 244321",
                effect: { security: +50, mistakes: 0, defenses: +2 },
                response: "📞 Вы назвали код под давлением...",
                analysis: "🎯 <strong>Манипуляция!</strong> Не поддавайтесь давлению срочности.",
                nextStep: 8
            },
            {
                text: "Я отключаюсь, проверю и перезвоню",
                effect: { security: +40, mistakes: 0, defenses: +1 },
                response: "📴 Вы вежливо завершили разговор...",
                analysis: "✅ <strong>Безопасно!</strong> Завершение подозрительного разговора.",
                nextStep: 9
            }
        ]
    },
    // ========== СЦЕНАРИЙ 2: ПОЛИЦИЯ ==========
    {
        scenario: 'police',
        sender: "scammer",
        text: "📞 <strong>Новый звонок...</strong><br><br>👮 <em>Голос:</em> Это капитан Иванов из МВД. Ваши данные фигурируют в деле о мошенничестве. Для прояснения обстоятельств нужны ваши паспортные данные.",
        options: [
            {
                text: "О боже! Что случилось?",
                effect: { security: -20, mistakes: +1, defenses: 0 },
                response: "😨 Вы испугались...",
                analysis: "⚠️ <strong>Ошибка!</strong> Страх мешает трезвому мышлению.",
                nextStep: 11,
                branch: 'fear'
            },
            {
                text: "Покажите служебное удостоверение",
                effect: { security: +25, mistakes: 0, defenses: +1 },
                response: "🪪 Вы потребовали удостоверение...",
                analysis: "✅ <strong>Правильно!</strong> Проверка легитимности звонящего.",
                nextStep: 12,
                branch: 'check'
            },
            {
                text: "Я приеду в отделение лично",
                effect: { security: +40, mistakes: 0, defenses: +1 },
                response: "🚗 Вы предложили приехать лично...",
                analysis: "🎯 <strong>Идеально!</strong> Личный визит исключает телефонное мошенничество.",
                nextStep: 13,
                branch: 'visit'
            }
        ]
    },
    {
        scenario: 'police',
        branch: 'fear',
        sender: "scammer",
        text: "Вы стали соучастником по неосторожности. Чтобы избежать уголовной ответственности, нужно оплатить залог в 50 000 рублей.",
        options: [
            {
                text: "Хорошо, куда переводить?",
                effect: { security: -70, mistakes: +2, defenses: 0 },
                response: "💸 Вы согласились перевести деньги...",
                analysis: "💥 <strong>Развод!</strong> Полиция никогда не просит денег по телефону!",
                nextStep: 10
            },
            {
                text: "Я позвоню своему адвокату",
                effect: { security: +30, mistakes: 0, defenses: +1 },
                response: "⚖️ Вы решили проконсультироваться с адвокатом...",
                analysis: "✅ <strong>Умно!</strong> Консультация с юристом защитит вас.",
                nextStep: 14
            },
            {
                text: "Назовите номер отделения, я приеду",
                effect: { security: +50, mistakes: 0, defenses: +2 },
                response: "🏢 Вы потребовали номер отделения...",
                analysis: "🎯 <strong>Правильно!</strong> Настоящие следователи работают в отделениях.",
                nextStep: 15
            }
        ]
    },
    // ========== СЦЕНАРИЙ 3: СОЦСЛУЖБЫ ==========
    {
        scenario: 'social',
        sender: "scammer",
        text: "👵 <strong>Звонок от 'социальной службы'...</strong><br><br>🏛 <em>Голос:</em> Здравствуйте! Вам одобрена социальная выплата 25 000 рублей. Для получения нужна комиссия 1 000 рублей.",
        options: [
            {
                text: "Отлично! Куда платить комиссию?",
                effect: { security: -40, mistakes: +1, defenses: 0 },
                response: "💰 Вы согласились оплатить комиссию...",
                analysis: "⚠️ <strong>Ошибка!</strong> Государственные выплаты не требуют комиссий!",
                nextStep: 16,
                branch: 'gullible'
            },
            {
                text: "Пришлите официальное уведомление",
                effect: { security: +30, mistakes: 0, defenses: +1 },
                response: "📨 Вы попросили официальное уведомление...",
                analysis: "✅ <strong>Правильно!</strong> Все выплаты оформляются документально.",
                nextStep: 17,
                branch: 'cautious'
            },
            {
                text: "Я зайду в соцзащиту лично",
                effect: { security: +50, mistakes: 0, defenses: +2 },
                response: "🚶 Вы решили обратиться лично...",
                analysis: "🎯 <strong>Идеально!</strong> Личное обращение исключает мошенничество.",
                nextStep: 18,
                branch: 'smart'
            }
        ]
    },
    // ========== СЦЕНАРИЙ 4: ТЕХПОДДЕРЖКА ==========
    {
        scenario: 'tech',
        sender: "scammer",
        text: "💻 <strong>Звонок от 'техподдержки провайдера'...</strong><br><br>🛠 <em>Голос:</em> У вас вирус, который рассылает спам. Нужно срочно установить программу для очистки.",
        options: [
            {
                text: "Хорошо, что устанавливать?",
                effect: { security: -50, mistakes: +1, defenses: 0 },
                response: "🔧 Вы согласились установить программу...",
                analysis: "⚠️ <strong>Опасность!</strong> Это может быть ПУУ-схема.",
                nextStep: 19,
                branch: 'trusting'
            },
            {
                text: "Я сам IT-специалист, все проверил",
                effect: { security: +40, mistakes: 0, defenses: +1 },
                response: "👨‍💻 Вы представились специалистом...",
                analysis: "✅ <strong>Умно!</strong> Мошенники часто отступают перед 'специалистами'.",
                nextStep: 20,
                branch: 'expert'
            },
            {
                text: "Позвоню в поддержку по официальному номеру",
                effect: { security: +35, mistakes: 0, defenses: +1 },
                response: "📞 Вы решили позвонить официально...",
                analysis: "✅ <strong>Безопасно!</strong> Проверка через официальные каналы.",
                nextStep: 21,
                branch: 'official'
            }
        ]
    },
    // ========== РЕЗУЛЬТАТЫ И УРОКИ ==========
    {
        id: 10,
        sender: "system",
        text: "🏆 <strong>ПОБЕДА!</strong><br><br>Вы успешно защитились от всех мошенников!<br>Ваши навыки:<br>• Распознавание манипуляций<br>• Проверка информации<br>• Сохранение хладнокровия",
        options: [
            {
                text: "Узнать, как защититься",
                effect: { security: 0, mistakes: 0, defenses: 0 },
                response: "",
                nextStep:22
            }
        ]
    },
    {
        id: 22,
        sender: "lesson",
        text: "🛡 <strong>УРОК БЕЗОПАСНОСТИ:</strong><br><br>1. <strong>Никогда не называйте</strong> коды из SMS<br>2. <strong>Никогда не переводите</strong> деньги по просьбе по телефону<br>3. <strong>Всегда перезванивайте</strong> по официальным номерам<br>4. <strong>Не бойтесь</strong> положить трубку",
        options: [
            {
                text: "Пройти еще раз",
                effect: { security: 100, mistakes: 0, defenses: 0 },
                response: "",
                nextStep: 0,
                restart: true
            }
        ]
    },
    {
        id: 23,
        sender: "system",
        text: " 💥<strong>ВЫ ПОПАЛИСЬ!</strong><br><br>Мошенники получили доступ к вашим деньгам и данным.<br>Ваши навыки:<br>• Распознавание манипуляций<br>• Проверка информации<br>• Сохранение хладнокровия",
        options: [
       
        ]
    },
    {
        id: 24,
        sender: "lesson",
        text: "📊 <strong>ВАША СТАТИСТИКА:</strong><br><br>• Безопасность: <span id='final-phone-security'>100%</span><br>• Ошибок: <span id='final-phone-mistakes'>0</span><br>• Успешных защит: <span id='final-phone-defenses'>0</span><br><br>🎓 <strong>Вы научились:</strong><br>✓ Проверять легитимность звонков<br>✓ Противостоять давлению<br>✓ Использовать официальные каналы",
        options: [
            {
                text: "Завершить тренажер",
                effect: { security: 0, mistakes: 0, defenses: 0 },
                response: "",
                nextStep: 25
            }
        ]
    },
    {
        id: 25,
        sender: "system",
        text: "✅ <strong>Тренажер завершен!</strong> Теперь вы лучше защищены от телефонных мошенников.",
        options: [
            {
                text: "Вернуться к тренажерам",
                effect: { security: 0, mistakes: 0, defenses: 0 },
                response: "",
                restart: true,
                finish: true
            }
        ]
    }
];

// Функция для получения текущего шага диалога
function getCurrentPhoneStep() {
    const step = phoneDialogueSteps[phoneCurrentStep];
    
    // Если у шага есть сценарий, проверяем совпадение
    if (step && step.scenario && step.scenario !== currentScenario) {
        // Ищем первый шаг текущего сценария
        return phoneDialogueSteps.find(s => s.scenario === currentScenario && !s.branch) || phoneDialogueSteps[0];
    }
    
    // Если у шага есть ветка, проверяем совпадение
    if (step && step.branch) {
        // Находим следующий шаг с той же веткой
        const nextStep = phoneDialogueSteps.find(s => 
            s.scenario === currentScenario && 
            s.branch === step.branch &&
            s.id !== step.id
        );
        if (nextStep) return nextStep;
    }
    
    return step;
}

// Инициализация тренажера Телефон
window.initPhoneSimulator = function() {
    phoneCurrentStep = 0;
    phoneSecurityScore = 100;
    phoneMistakesCount = 0;
    phoneDefensesCount = 0;
    phoneSimulationFinished = false;
    currentScenario = 'bank'; // Начинаем со сценария банка
    
    // Очищаем предыдущие сообщения
    const chatMessages = document.getElementById('phone-chat-messages');
    if (chatMessages) chatMessages.innerHTML = '';
    
    // Очищаем предыдущие варианты
    const chatInput = document.getElementById('phone-chat-input');
    if (chatInput) chatInput.innerHTML = '';
    
    // Скрываем финальный результат
    const resultDiv = document.getElementById('phone-simulator-result');
    if (resultDiv) resultDiv.style.display = 'none';
    
    updatePhoneScores();
    showPhoneDialogueStep();
};

// Показать шаг диалога
function showPhoneDialogueStep() {
    const chatMessages = document.getElementById('phone-chat-messages');
    const chatInput = document.getElementById('phone-chat-input');
    
    if (!chatMessages || !chatInput) {
        console.error('Не найдены элементы чата телефонного тренажера');
        return;
    }
    
    const dialogue = getCurrentPhoneStep();
    if (!dialogue) {
        console.error('Диалог не найден для шага:', phoneCurrentStep);
        return;
    }
    
    // Добавляем сообщение в чат
    const messageDiv = document.createElement('div');
    messageDiv.className = `phone-message ${dialogue.sender}`;
    if (dialogue.id === 10) {
        messageDiv.classList.add('phone-ringing');
    }
    messageDiv.innerHTML = `<div class="phone-message-text">${dialogue.text}</div>`;
    chatMessages.appendChild(messageDiv);
    
    // Добавляем информацию о звонке для сценариев
    if (dialogue.scenario && dialogue.branch && !dialogue.id) {
        const infoDiv = document.createElement('div');
        infoDiv.className = 'phone-call-info';
        
        let scenarioText = '';
        switch(dialogue.scenario) {
            case 'bank': scenarioText = '📱 Сценарий: Звонок от "банка"'; break;
            case 'police': scenarioText = '👮 Сценарий: Звонок от "полиции"'; break;
            case 'social': scenarioText = '🏛 Сценарий: Звонок от "соцслужб"'; break;
            case 'tech': scenarioText = '💻 Сценарий: Звонок от "техподдержки"'; break;
        }
        
        infoDiv.innerHTML = `${scenarioText}`;
        chatMessages.appendChild(infoDiv);
    }
    
    // Очищаем предыдущие варианты ответов
    chatInput.innerHTML = '';
    
    // Добавляем подсказку для текущего шага
    if (phoneCurrentStep === 0) {
        const hintDiv = document.createElement('div');
        hintDiv.className = 'phone-hint';
        hintDiv.innerHTML = '💡 <strong>Подсказка:</strong> Настоящие банки никогда не просят коды из SMS по телефону';
        chatInput.appendChild(hintDiv);
    }
    
    // Добавляем новые варианты ответов
    dialogue.options.forEach((option, index) => {
        const button = document.createElement('button');
        button.className = 'phone-chat-option';
        if (option.effect.security < 0) {
            button.classList.add('danger');
        } else if (option.effect.security > 20) {
            button.classList.add('success');
        }
        button.textContent = option.text;
        button.onclick = () => selectPhoneDialogueOption(dialogue, option, index);
        chatInput.appendChild(button);
    });
    
    // Прокручиваем чат вниз
    chatMessages.scrollTop = chatMessages.scrollHeight;
    
    // Если это финальный шаг
    if (dialogue.id === 23 || dialogue.id === 23) {
        showPhoneFinalResult(dialogue.id === 10);
    }
}

// Обработка выбора варианта
function selectPhoneDialogueOption(dialogue, option, optionIndex) {
    if (phoneSimulationFinished) return;
    
    // Применяем эффекты
    phoneSecurityScore = Math.max(0, Math.min(100, phoneSecurityScore + option.effect.security));
    phoneMistakesCount += option.effect.mistakes;
    phoneDefensesCount += option.effect.defenses;
    
    updatePhoneScores();
    
    // Показываем ответ на выбор
    const chatMessages = document.getElementById('phone-chat-messages');
    const responseDiv = document.createElement('div');
    responseDiv.className = 'phone-message user';
    responseDiv.innerHTML = `<div class="phone-message-text"><strong>Вы:</strong> ${option.text}</div>`;
    chatMessages.appendChild(responseDiv);
    
    // Показываем анализ выбора
    if (option.analysis) {
        const analysisDiv = document.createElement('div');
        analysisDiv.className = 'phone-message system';
        analysisDiv.innerHTML = `<div class="phone-message-text">${option.analysis}</div>`;
        chatMessages.appendChild(analysisDiv);
    }
    
    // Прокручиваем чат вниз
    chatMessages.scrollTop = chatMessages.scrollHeight;
    
    // Если есть ответ от системы, показываем его
    if (option.response) {
        setTimeout(() => {
            const systemDiv = document.createElement('div');
            systemDiv.className = 'phone-message scammer';
            systemDiv.innerHTML = `<div class="phone-message-text">${option.response}</div>`;
            chatMessages.appendChild(systemDiv);
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }, 500);
    }
    
    // Переход к следующему шагу или рестарт
    setTimeout(() => {
        if (option.restart) {
            window.initPhoneSimulator();
        } else if (option.finish) {
            completePhoneSimulator();
        } else {
            // Обновляем текущий шаг
            phoneCurrentStep = option.nextStep;
            
            // Если следующий шаг требует смены сценария
            if (option.nextStep >= 11 && option.nextStep <= 13) {
                currentScenario = 'police';
            } else if (option.nextStep >= 16 && option.nextStep <= 18) {
                currentScenario = 'social';
            } else if (option.nextStep >= 19 && option.nextStep <= 21) {
                currentScenario = 'tech';
            }
            
            showPhoneDialogueStep();
        }
    }, 1000);
}

// Обновление счетчиков
function updatePhoneScores() {
    const securityEl = document.getElementById('phone-security-score');
    const mistakesEl = document.getElementById('phone-mistakes-count');
    const defensesEl = document.getElementById('phone-defenses-count');
    
    if (!securityEl || !mistakesEl || !defensesEl) return;
    
    securityEl.textContent = phoneSecurityScore + '%';
    mistakesEl.textContent = phoneMistakesCount;
    defensesEl.textContent = phoneDefensesCount;
    
    // Динамическое изменение цвета
    securityEl.style.color = phoneSecurityScore > 70 ? '#388e3c' : 
                           phoneSecurityScore > 40 ? '#ff9800' : '#d32f2f';
    
    mistakesEl.style.color = phoneMistakesCount === 0 ? '#388e3c' : 
                           phoneMistakesCount < 3 ? '#ff9800' : '#d32f2f';
    
    defensesEl.style.color = phoneDefensesCount > 3 ? '#388e3c' : 
                            phoneDefensesCount > 1 ? '#ff9800' : '#1976d2';
}

// Показать финальный результат
function showPhoneFinalResult(isFailure) {
    phoneSimulationFinished = true;
    const resultDiv = document.getElementById('phone-simulator-result');
    
    if (!resultDiv) return;
    
    if (isFailure) {
        resultDiv.innerHTML = `
            <div class="phone-result-failure">
                <h3>💥 Вы стали жертвой мошенников!</h3>
                <p>К сожалению, вы попались на уловки телефонных мошенников.</p>
                <div class="phone-analysis-points">
                    <strong>Основные ошибки:</strong>
                    <ul>
                        <li>Назвали коды подтверждения из SMS</li>
                        <li>Перевели деньги по телефону</li>
                        <li>Поверили в срочность и давление</li>
                        <li>Не проверили информацию через официальные каналы</li>
                    </ul>
                </div>
                <p><strong>Запомните:</strong> Настоящие сотрудники банков, полиции и госслужб НИКОГДА не просят коды из SMS и не требуют переводов по телефону!</p>
            </div>
        `;
    }
    
    resultDiv.style.display = 'block';
    
    // Прокручиваем к результату
    resultDiv.scrollIntoView({ behavior: 'smooth' });
}

// Перезапуск тренажера
function restartPhoneSimulator() {
    window.initPhoneSimulator();
}

// Завершение тренажера с сохранением прогресса
function completePhoneSimulator() {
    if (!currentUser) {
        showNotification('error', 'Для сохранения прогресса войдите в систему');
        showLoginModal();
        return;
    }
    
    // Проверяем, был ли уже завершен тренажер
    const simulatorId = 'phone-simulator';
    if (currentUser.completedSimulators && currentUser.completedSimulators.includes(simulatorId)) {
        showNotification('info', 'Тренажер уже был пройден ранее');
        showPage('simulators');
        return;
    }
    
    // Вычисляем очки на основе результата
    let earnedPoints = 0;
    if (phoneSecurityScore >= 80) {
        earnedPoints = 30;
    } else if (phoneSecurityScore >= 60) {
        earnedPoints = 20;
    } else if (phoneSecurityScore >= 40) {
        earnedPoints = 10;
    } else {
        earnedPoints = 5;
    }
    
    // Добавляем бонус за успешные защиты
    earnedPoints += phoneDefensesCount * 5;
    
    // Обновляем прогресс пользователя
    if (!currentUser.completedSimulators) {
        currentUser.completedSimulators = [];
    }
    
    currentUser.completedSimulators.push(simulatorId);
    currentUser.stats.completedSimulators = (currentUser.stats.completedSimulators || 0) + 1;
    currentUser.stats.score = (currentUser.stats.score || 0) + earnedPoints;
    currentUser.stats.lastActive = new Date().toISOString();
    
    // Сохраняем статистику по телефонному мошенничеству
    if (!currentUser.phoneStats) {
        currentUser.phoneStats = {};
    }
    
    currentUser.phoneStats.lastScore = phoneSecurityScore;
    currentUser.phoneStats.defenses = phoneDefensesCount;
    currentUser.phoneStats.mistakes = phoneMistakesCount;
    currentUser.phoneStats.lastCompletion = new Date().toISOString();
    
    updateUserInStorage();
    
    // ПРИНУДИТЕЛЬНО ОБНОВЛЯЕМ ПРОГРЕСС-БАРЫ
    updateProgressBars();
    
    // Показываем уведомление
    let message = '';
    if (phoneSecurityScore >= 80) {
        message = `Отлично! Тренажер пройден на ${phoneSecurityScore}%! +${earnedPoints} очков`;
    } else if (phoneSecurityScore >= 60) {
        message = `Хорошо! Тренажер пройден на ${phoneSecurityScore}%! +${earnedPoints} очков`;
    } else {
        message = `Тренажер завершен. Обратите внимание на ошибки. +${earnedPoints} очков`;
    }
    
    showNotification('success', message);
    
    // Возвращаемся к списку тренажеров
    setTimeout(() => {
        showPage('simulators');
    }, 2000);
}
        // Контент для тренажера "Конструктор паролей"
function getPasswordConstructorContent() {
    return `
        <div class="simulator">
            <h3>Проверка стойкости пароля</h3>
            <p>Введите пароль для проверки его стойкости:</p>
            <input type="text" id="password-input" placeholder="Введите пароль" style="width: 100%; padding: 12px; margin: 15px 0; border: 2px solid #ddd; border-radius: 8px; font-size: 1rem;">
            
            <button class="btn" onclick="checkPasswordStrength()">
                Проверить пароль
            </button>
            
            <div id="password-result" style="margin-top: 20px;"></div>
        </div>
        
        <div class="simulator" style="margin-top: 40px;">
            <h3>Создайте надежный пароль</h3>
            <p>Используйте следующие критерии для создания пароля:</p>
            <ul>
                <li>Не менее 12 символов</li>
                <li>Заглавные и строчные буквы</li>
                <li>Цифры и специальные символы</li>
                <li>Не использовать личную информацию</li>
            </ul>
            
            <div id="generated-password" style="background-color: #f5f5f5; padding: 15px; border-radius: 8px; font-family: monospace; font-size: 1.2rem; text-align: center; margin: 20px 0;"></div>
            
            <button class="btn" onclick="generatePassword()">
                <i class="fas fa-sync-alt icon"></i> Сгенерировать пароль
            </button>
        </div>
    `;
}
// Контент для тренажера "Госуслуги: Проверка сайта" - ДИАЛОГОВАЯ ВЕРСИЯ
function getGosuslugiSimulatorContent() {
    return `
        <div class="simulator" id="gosuslugi-simulator">
            <style>
                .chat-container {
                    background: #f5f7fa;
                    border-radius: 15px;
                    padding: 20px;
                    max-width: 800px;
                    margin: 0 auto;
                    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
                }
                
                .chat-header {
                    text-align: center;
                    margin-bottom: 20px;
                    padding-bottom: 15px;
                    border-bottom: 2px solid #e0e6ef;
                }
                
                .chat-header .subtitle {
                    color: #666;
                    font-size: 14px;
                    margin-top: 5px;
                }
                
                .chat-messages {
                    height: 400px;
                    overflow-y: auto;
                    padding: 15px;
                    background: white;
                    border-radius: 10px;
                    margin-bottom: 20px;
                    border: 1px solid #e0e6ef;
                }
                
                .message {
                    margin-bottom: 15px;
                    animation: fadeIn 0.3s ease;
                }
                
                .message.sms {
                    background: #e3f2fd;
                    border-left: 4px solid #2196f3;
                }
                
                .message.scammer {
                    background: #ffebee;
                    border-left: 4px solid #f44336;
                }
                
                .message.system {
                    background: #e8f5e9;
                    border-left: 4px solid #4caf50;
                }
                
                .message.user {
                    background: #f3e5f5;
                    border-left: 4px solid #9c27b0;
                }
                
                .message.lesson {
                    background: #fff3e0;
                    border-left: 4px solid #ff9800;
                }
                
                .message-text {
                    padding: 12px 15px;
                    border-radius: 0 10px 10px 10px;
                }
                
                .chat-input {
                    display: flex;
                    flex-direction: column;
                    gap: 10px;
                    padding: 15px;
                    background: white;
                    border-radius: 10px;
                    border: 1px solid #e0e6ef;
                }
                
                .chat-option {
                    padding: 12px 20px;
                    background: #f8f9fa;
                    border: 2px solid #e0e6ef;
                    border-radius: 8px;
                    cursor: pointer;
                    text-align: left;
                    font-size: 14px;
                    transition: all 0.2s;
                }
                
                .chat-option:hover {
                    background: #e3f2fd;
                    border-color: #2196f3;
                    transform: translateX(5px);
                }
                
                .chat-stats {
                    display: flex;
                    justify-content: space-around;
                    margin-top: 20px;
                    padding: 15px;
                    background: white;
                    border-radius: 10px;
                    font-weight: bold;
                    border: 1px solid #e0e6ef;
                }
                
                .chat-stats span {
                    font-size: 18px;
                    font-weight: bold;
                }
                
                .result-success, .result-failure {
                    padding: 25px;
                    border-radius: 10px;
                    margin-top: 20px;
                    animation: fadeIn 0.5s ease;
                }
                
                .result-success {
                    background: #e8f5e9;
                    border: 2px solid #4caf50;
                }
                
                .result-failure {
                    background: #ffebee;
                    border: 2px solid #f44336;
                }
                
                @keyframes fadeIn {
                    from { opacity: 0; transform: translateY(10px); }
                    to { opacity: 1; transform: translateY(0); }
                }
            </style>
            
            <div class="chat-container">
                <div class="chat-header">
                    <h3>💬 Диалог с "поддержкой" Госуслуг</h3>
                    <p class="subtitle">Вы получили SMS. Попробуйте не попасться на удочку мошенников.</p>
                </div>
                
                <div class="chat-messages" id="gosuslugi-chat-messages">
                    <!-- Сообщения будут добавляться здесь скриптом -->
                </div>
                
                <div class="chat-input" id="gosuslugi-chat-input">
                    <!-- Варианты ответов будут добавляться здесь скриптом -->
                </div>
                
                <div class="chat-stats">
                    <p>Безопасность: <span id="gosuslugi-security-score">100%</span></p>
                    <p>Доверие мошеннику: <span id="gosuslugi-trust-score">0%</span></p>
                </div>
            </div>
            
            <div class="simulator-result" id="gosuslugi-simulator-result" style="display: none;">
                <!-- Финальный результат появится здесь -->
            </div>
        </div>
        <!-- Кнопка начать заново -->
            <div style="text-align: center; margin-top: 30px;">
                <button class="btn btn-outline" onclick="initGosuslugiSimulator()">
                    <i class="fas fa-redo icon"></i> Начать тренажер заново
                </button>
            </div>
        </div>
    `;
}       
// Упрощенный контент для тренажера "Проверка безопасности"
// Симулятор настроек безопасности ВКонтакте
function getSecurityCheckSimulatorContent() {
    return `
        <div class="vk-simulator">
<style>
.vk-simulator {
    max-width: 1000px;
    margin: 0 auto;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

/* Заголовок */
.vk-header {
    text-align: center;
    padding: 20px 0;
    margin-bottom: 20px;
    border-bottom: 1px solid #e7e8ec;
}

.vk-header h3 {
    color: #4a76a8;
    margin-bottom: 5px;
    font-weight: 500;
    font-size: 1.8rem;
}

.vk-header p {
    color: #656565;
    font-size: 14px;
}

/* Основной контейнер */
.vk-container {
    display: flex;
    gap: 20px;
    min-height: 500px;
}

/* Боковое меню */
.vk-sidebar {
    width: 220px;
    flex-shrink: 0;
}

.vk-profile {
    background: white;
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    margin-bottom: 15px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    border: 1px solid #e7e8ec;
}

.vk-avatar {
    width: 70px;
    height: 70px;
    border-radius: 50%;
    background: #4a76a8;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
    margin: 0 auto 12px;
}

.vk-name {
    font-weight: 500;
    color: #2a5885;
    margin-bottom: 4px;
}

.vk-status {
    font-size: 13px;
    color: #939393;
}

.vk-menu {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    border: 1px solid #e7e8ec;
}

.vk-menu-item {
    padding: 14px 16px;
    display: flex;
    align-items: center;
    gap: 12px;
    cursor: pointer;
    border-left: 3px solid transparent;
    transition: all 0.2s;
    color: #2a5885;
    text-decoration: none;
}

.vk-menu-item:hover {
    background: #f5f7fa;
}

.vk-menu-item.active {
    background: #f0f4fa;
    border-left-color: #4a76a8;
    color: #2a5885;
    font-weight: 500;
}

.vk-menu-icon {
    width: 20px;
    text-align: center;
    color: #4a76a8;
}

/* Основная область */
.vk-main {
    flex: 1;
    background: white;
    border-radius: 8px;
    padding: 25px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    border: 1px solid #e7e8ec;
}

.vk-section-title {
    color: #2a5885;
    margin-bottom: 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid #e7e8ec;
    font-weight: 500;
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 1.2rem;
}

/* Настройки */
.vk-setting {
    margin-bottom: 20px;
    padding-bottom: 20px;
    border-bottom: 1px solid #f0f2f5;
}

.vk-setting:last-child {
    border-bottom: none;
    margin-bottom: 0;
}

.vk-setting-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
}

.vk-setting-name {
    font-weight: 500;
    color: #2a5885;
}

.vk-setting-value {
    font-size: 13px;
    color: #939393;
    background: #f5f7fa;
    padding: 4px 10px;
    border-radius: 12px;
}

.vk-setting-desc {
    font-size: 14px;
    color: #656565;
    margin-bottom: 12px;
    line-height: 1.4;
}

.vk-options {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.vk-option {
    padding: 12px 15px;
    border: 1px solid #e7e8ec;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.2s;
    font-size: 14px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.vk-option:hover {
    border-color: #4a76a8;
    background: #f5f9ff;
}

.vk-option.selected {
    border-color: #4a76a8;
    background: #edf2fa;
    color: #2a5885;
    font-weight: 500;
}

.vk-option.danger.selected {
    border-color: #e64646;
    background: #fef0f0;
    color: #e64646;
}

.vk-option.success.selected {
    border-color: #4bb34b;
    background: #f0fff0;
    color: #4bb34b;
}

/* Панель рисков */
.vk-risks {
    background: white;
    border-radius: 8px;
    padding: 25px;
    margin-top: 20px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    border: 1px solid #e7e8ec;
}

.vk-risks-title {
    color: #2a5885;
    margin-bottom: 20px;
    font-weight: 500;
    display: flex;
    align-items: center;
    gap: 10px;
}

.vk-risks-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-bottom: 20px;
}

.vk-risk-card {
    padding: 15px;
    border-radius: 6px;
    border: 1px solid #e7e8ec;
    background: #fafbfd;
}

.vk-risk-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
}

.vk-risk-name {
    font-size: 14px;
    color: #656565;
}

.vk-risk-percent {
    font-weight: 600;
    font-size: 18px;
}

.vk-risk-percent.high { color: #e64646; }
.vk-risk-percent.medium { color: #ff9d00; }
.vk-risk-percent.low { color: #4bb34b; }

.vk-risk-bar {
    height: 6px;
    background: #e7e8ec;
    border-radius: 3px;
    overflow: hidden;
    margin-bottom: 8px;
}

.vk-risk-fill {
    height: 100%;
    border-radius: 3px;
    transition: width 0.5s ease;
}

.vk-risk-fill.high { background: #e64646; }
.vk-risk-fill.medium { background: #ff9d00; }
.vk-risk-fill.low { background: #4bb34b; }

.vk-risk-change {
    font-size: 12px;
    color: #939393;
    display: flex;
    align-items: center;
    gap: 5px;
}

.vk-risk-change.good { color: #4bb34b; }
.vk-risk-change.bad { color: #e64646; }

/* Угрозы */
.vk-threats {
    margin-top: 15px;
}

.vk-threats-label {
    font-size: 13px;
    color: #656565;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 8px;
}

.vk-threats-list {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
}

.vk-threat {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 12px;
    border-radius: 15px;
    font-size: 13px;
    background: #f5f7fa;
    color: #656565;
    border: 1px solid #e7e8ec;
}

.vk-threat.high {
    background: #fef0f0;
    color: #e64646;
    border-color: #fdd;
}

.vk-threat.medium {
    background: #fff9f0;
    color: #ff9d00;
    border-color: #ffe8cc;
}

.vk-threat.low {
    background: #f9fff9;
    color: #4bb34b;
    border-color: #d4f7d4;
}

/* Кнопки */
.vk-actions {
    display: flex;
    gap: 10px;
    justify-content: center;
    margin-top: 25px;
    padding-top: 20px;
    border-top: 1px solid #e7e8ec;
}

/* Уведомление */
.vk-notification {
    position: fixed;
    top: 20px;
    right: 20px;
    padding: 12px 20px;
    background: white;
    border-radius: 8px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.1);
    border-left: 4px solid #4a76a8;
    display: flex;
    align-items: center;
    gap: 10px;
    z-index: 1000;
    animation: slideIn 0.3s ease;
}

@keyframes vkSlideIn {
    from { transform: translateX(100%); opacity: 0; }
    to { transform: translateX(0); opacity: 1; }
}

.vk-notification {
    animation: vkSlideIn 0.3s ease;
}
</style>
            <!-- Заголовок -->
            <div class="vk-header">
                <h3>🔐 Симулятор безопасности ВКонтакте</h3>
                <p>Настройте параметры безопасности вашего профиля</p>
            </div>
            
            <!-- Основной контейнер -->
            <div class="vk-container">
                <!-- Боковое меню -->
                <div class="vk-sidebar">
                    <div class="vk-profile">
                        <div class="vk-avatar">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="vk-name">Александр Иванов</div>
                        <div class="vk-status">Настройте безопасность</div>
                    </div>
                    
                    <div class="vk-menu">
                        <div class="vk-menu-item active" onclick="showVKSection('privacy')">
                            <i class="fas fa-eye vk-menu-icon"></i>
                            <span>Приватность</span>
                        </div>
                        <div class="vk-menu-item" onclick="showVKSection('security')">
                            <i class="fas fa-shield-alt vk-menu-icon"></i>
                            <span>Безопасность</span>
                        </div>
                        <div class="vk-menu-item" onclick="showVKSection('apps')">
                            <i class="fas fa-th vk-menu-icon"></i>
                            <span>Приложения</span>
                        </div>
                        <div class="vk-menu-item" onclick="showVKSection('contacts')">
                            <i class="fas fa-users vk-menu-icon"></i>
                            <span>Контакты</span>
                        </div>
                        <div class="vk-menu-item" onclick="showVKSection('notifications')">
                            <i class="fas fa-bell vk-menu-icon"></i>
                            <span>Уведомления</span>
                        </div>
                    </div>
                </div>
                
                <!-- Основная область -->
                <div class="vk-main" id="vk-main-content">
                    <!-- Контент будет загружен здесь -->
                </div>
            </div>
            
            <!-- Панель рисков -->
            <div class="vk-risks">
                <h4 class="vk-risks-title">
                    <i class="fas fa-chart-line"></i>
                    Анализ рисков
                </h4>
                
                <div class="vk-risks-grid" id="vk-risks-grid">
                    <!-- Карточки рисков будут здесь -->
                </div>
                
                <div class="vk-threats">
                    <div class="vk-threats-label">
                        <i class="fas fa-exclamation-circle"></i>
                        Активные угрозы:
                    </div>
                    <div class="vk-threats-list" id="vk-threats-list">
                        <!-- Угрозы будут здесь -->
                    </div>
                </div>
            </div>
            
            <!-- Кнопки действий -->
            <div class="vk-actions">
                <button class="btn btn-outline" onclick="resetVKSettings()">
                    <i class="fas fa-undo"></i> Начать заново
                </button>
            </div>
        </div>
    `;
}
// Глобальные переменные для тренажера безопасности
let securityCurrentStep = 0;
let securityLevel = 0;
let securitySettingsCount = 0;
let securityVulnerabilities = 5;
let securitySimulationFinished = false;
let currentPlatform = 'facebook'; // facebook, google, vk, instagram, banking
let completedChecklists = {
    facebook: false,
    google: false,
    vk: false,
    instagram: false,
    banking: false
};

// Вопросы для тренажера безопасности
// Настройки пользователя
let vkSettings = {
    // Приватность
    profileVisibility: 'all',
    photosVisibility: 'friends_of_friends',
    onlineVisibility: true,
    birthDateVisibility: 'full',
    
    // Безопасность
    twoFactorAuth: false,
    loginHistory: false,
    sessions: false,
    
    // Приложения
    gamesAccess: true,
    appsAccess: true,
    messageApps: true,
    
    // Контакты
    friendRequests: 'all',
    messagesFrom: 'all',
    groupInvites: 'all',
    
    // Уведомления
    loginAlerts: false,
    newDeviceAlerts: false,
    privacyAlerts: false
};

// Начальные настройки
const initialSettings = JSON.parse(JSON.stringify(vkSettings));

// Инициализация
window.initVKSimulator = function() {
    vkSettings = JSON.parse(JSON.stringify(initialSettings));
    showVKSection('privacy');
    updateVKRisks();
};

// Показать раздел
function showVKSection(section) {
    // Обновить меню
    document.querySelectorAll('.vk-menu-item').forEach(item => {
        item.classList.remove('active');
    });
    
    const menuItem = document.querySelector(`.vk-menu-item[onclick*="${section}"]`);
    if (menuItem) menuItem.classList.add('active');
    
    // Загрузить контент
    const contentDiv = document.getElementById('vk-main-content');
    if (!contentDiv) return;
    
    let content = '';
    
    switch(section) {
        case 'privacy':
            content = getPrivacyContent();
            break;
        case 'security':
            content = getSecurityContent();
            break;
        case 'apps':
            content = getAppsContent();
            break;
        case 'contacts':
            content = getContactsContent();
            break;
        case 'notifications':
            content = getNotificationsContent();
            break;
        default:
            content = getPrivacyContent();
    }
    
    contentDiv.innerHTML = content;
}

// Контент раздела Приватность
function getPrivacyContent() {
    return `
        <h4 class="vk-section-title">
            <i class="fas fa-eye"></i>
            Настройки приватности
        </h4>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Кто видит профиль</div>
                <div class="vk-setting-value">${getVisibilityLabel(vkSettings.profileVisibility)}</div>
            </div>
            <div class="vk-setting-desc">
                Кто может видеть ваше имя, фамилию, информацию о себе
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.profileVisibility === 'all' ? 'selected danger' : ''}" onclick="changeVKSetting('profileVisibility', 'all')">
                    Все пользователи
                    ${vkSettings.profileVisibility === 'all' ? '<i class="fas fa-check"></i>' : ''}
                </div>
                <div class="vk-option ${vkSettings.profileVisibility === 'friends_of_friends' ? 'selected' : ''}" onclick="changeVKSetting('profileVisibility', 'friends_of_friends')">
                    Друзья и друзья друзей
                </div>
                <div class="vk-option ${vkSettings.profileVisibility === 'friends' ? 'selected success' : ''}" onclick="changeVKSetting('profileVisibility', 'friends')">
                    Только друзья
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Кто видит фотографии</div>
                <div class="vk-setting-value">${getVisibilityLabel(vkSettings.photosVisibility)}</div>
            </div>
            <div class="vk-setting-desc">
                Кто может просматривать ваши фотоальбомы
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.photosVisibility === 'all' ? 'selected danger' : ''}" onclick="changeVKSetting('photosVisibility', 'all')">
                    Все пользователи
                </div>
                <div class="vk-option ${vkSettings.photosVisibility === 'friends_of_friends' ? 'selected' : ''}" onclick="changeVKSetting('photosVisibility', 'friends_of_friends')">
                    Друзья и друзья друзей
                </div>
                <div class="vk-option ${vkSettings.photosVisibility === 'friends' ? 'selected success' : ''}" onclick="changeVKSetting('photosVisibility', 'friends')">
                    Только друзья
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Показывать онлайн-статус</div>
                <div class="vk-setting-value">${vkSettings.onlineVisibility ? 'Да' : 'Нет'}</div>
            </div>
            <div class="vk-setting-desc">
                Показывать ли другим, что вы в сети
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.onlineVisibility ? 'selected' : ''}" onclick="changeVKSetting('onlineVisibility', true)">
                    Показывать
                </div>
                <div class="vk-option ${!vkSettings.onlineVisibility ? 'selected success' : ''}" onclick="changeVKSetting('onlineVisibility', false)">
                    Скрывать
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Дата рождения</div>
                <div class="vk-setting-value">${getBirthDateLabel(vkSettings.birthDateVisibility)}</div>
            </div>
            <div class="vk-setting-desc">
                Какая информация о дате рождения видна
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.birthDateVisibility === 'full' ? 'selected danger' : ''}" onclick="changeVKSetting('birthDateVisibility', 'full')">
                    Полная дата (опасно)
                </div>
                <div class="vk-option ${vkSettings.birthDateVisibility === 'day_month' ? 'selected' : ''}" onclick="changeVKSetting('birthDateVisibility', 'day_month')">
                    Только день и месяц
                </div>
                <div class="vk-option ${vkSettings.birthDateVisibility === 'none' ? 'selected success' : ''}" onclick="changeVKSetting('birthDateVisibility', 'none')">
                    Скрыть
                </div>
            </div>
        </div>
    `;
}

// Контент раздела Безопасность
function getSecurityContent() {
    return `
        <h4 class="vk-section-title">
            <i class="fas fa-shield-alt"></i>
            Настройки безопасности
        </h4>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Двухфакторная аутентификация</div>
                <div class="vk-setting-value">${vkSettings.twoFactorAuth ? 'Включена' : 'Выключена'}</div>
            </div>
            <div class="vk-setting-desc">
                Защита входа с помощью кода из SMS или приложения
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.twoFactorAuth ? 'selected success' : 'danger'}" onclick="changeVKSetting('twoFactorAuth', true)">
                    Включить (рекомендуется)
                </div>
                <div class="vk-option ${!vkSettings.twoFactorAuth ? 'selected danger' : ''}" onclick="changeVKSetting('twoFactorAuth', false)">
                    Выключить (опасно)
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">История входов</div>
                <div class="vk-setting-value">${vkSettings.loginHistory ? 'Включена' : 'Выключена'}</div>
            </div>
            <div class="vk-setting-desc">
                Просмотр устройств и мест, откуда входили в аккаунт
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.loginHistory ? 'selected success' : ''}" onclick="changeVKSetting('loginHistory', true)">
                    Включить
                </div>
                <div class="vk-option ${!vkSettings.loginHistory ? 'selected' : ''}" onclick="changeVKSetting('loginHistory', false)">
                    Выключить
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Управление сессиями</div>
                <div class="vk-setting-value">${vkSettings.sessions ? 'Включено' : 'Выключено'}</div>
            </div>
            <div class="vk-setting-desc">
                Просмотр и завершение активных сессий на других устройствах
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.sessions ? 'selected success' : ''}" onclick="changeVKSetting('sessions', true)">
                    Включить
                </div>
                <div class="vk-option ${!vkSettings.sessions ? 'selected' : ''}" onclick="changeVKSetting('sessions', false)">
                    Выключить
                </div>
            </div>
        </div>
    `;
}

// Контент раздела Приложения - ИСПРАВЛЕННАЯ ВЕРСИЯ
function getAppsContent() {
    return `
        <h4 class="vk-section-title">
            <i class="fas fa-th"></i>
            Приложения и игры
        </h4>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Доступ игр</div>
                <div class="vk-setting-value">${vkSettings.gamesAccess ? 'Разрешен' : 'Запрещен'}</div>
            </div>
            <div class="vk-setting-desc">
                Игры могут получать доступ к вашему профилю и друзьям
            </div>
            <div class="vk-options">
                <div class="vk-option ${!vkSettings.gamesAccess ? 'selected success' : ''}" onclick="changeVKSetting('gamesAccess', false)">
                    Запретить 
                    ${!vkSettings.gamesAccess ? '<i class="fas fa-check"></i>' : ''}
                </div>
                <div class="vk-option ${vkSettings.gamesAccess ? 'selected danger' : ''}" onclick="changeVKSetting('gamesAccess', true)">
                    Разрешить 
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Доступ приложений</div>
                <div class="vk-setting-value">${vkSettings.appsAccess ? 'Разрешен' : 'Запрещен'}</div>
            </div>
            <div class="vk-setting-desc">
                Сторонние приложения могут получать ваши данные
            </div>
            <div class="vk-options">
                <div class="vk-option ${!vkSettings.appsAccess ? 'selected success' : ''}" onclick="changeVKSetting('appsAccess', false)">
                    Запретить 
                    ${!vkSettings.appsAccess ? '<i class="fas fa-check"></i>' : ''}
                </div>
                <div class="vk-option ${vkSettings.appsAccess ? 'selected danger' : ''}" onclick="changeVKSetting('appsAccess', true)">
                    Разрешить 
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Приложения для сообщений</div>
                <div class="vk-setting-value">${vkSettings.messageApps ? 'Разрешены' : 'Запрещены'}</div>
            </div>
            <div class="vk-setting-desc">
                Приложения могут читать и отправлять сообщения от вашего имени
            </div>
            <div class="vk-options">
                <div class="vk-option ${!vkSettings.messageApps ? 'selected success' : ''}" onclick="changeVKSetting('messageApps', false)">
                    Запретить 
                    ${!vkSettings.messageApps ? '<i class="fas fa-check"></i>' : ''}
                </div>
                <div class="vk-option ${vkSettings.messageApps ? 'selected danger' : ''}" onclick="changeVKSetting('messageApps', true)">
                    Разрешить
                </div>
            </div>
        </div>
    `;
}

// Контент раздела Контакты
function getContactsContent() {
    return `
        <h4 class="vk-section-title">
            <i class="fas fa-users"></i>
            Контакты и сообщения
        </h4>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Заявки в друзья</div>
                <div class="vk-setting-value">${getContactsLabel(vkSettings.friendRequests)}</div>
            </div>
            <div class="vk-setting-desc">
                Кто может отправлять вам запросы на добавление в друзья
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.friendRequests === 'all' ? 'selected danger' : ''}" onclick="changeVKSetting('friendRequests', 'all')">
                    Все пользователи
                </div>
                <div class="vk-option ${vkSettings.friendRequests === 'friends_of_friends' ? 'selected' : ''}" onclick="changeVKSetting('friendRequests', 'friends_of_friends')">
                    Друзья друзей
                </div>
                <div class="vk-option ${vkSettings.friendRequests === 'friends' ? 'selected success' : ''}" onclick="changeVKSetting('friendRequests', 'friends')">
                    Только друзья
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Личные сообщения</div>
                <div class="vk-setting-value">${getContactsLabel(vkSettings.messagesFrom)}</div>
            </div>
            <div class="vk-setting-desc">
                Кто может отправлять вам личные сообщения
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.messagesFrom === 'all' ? 'selected danger' : ''}" onclick="changeVKSetting('messagesFrom', 'all')">
                    Все пользователи
                </div>
                <div class="vk-option ${vkSettings.messagesFrom === 'friends_of_friends' ? 'selected' : ''}" onclick="changeVKSetting('messagesFrom', 'friends_of_friends')">
                    Друзья и друзья друзей
                </div>
                <div class="vk-option ${vkSettings.messagesFrom === 'friends' ? 'selected success' : ''}" onclick="changeVKSetting('messagesFrom', 'friends')">
                    Только друзья
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Приглашения в группы</div>
                <div class="vk-setting-value">${vkSettings.groupInvites === 'all' ? 'Все' : 'Только друзья'}</div>
            </div>
            <div class="vk-setting-desc">
                Кто может приглашать вас в сообщества
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.groupInvites === 'all' ? 'selected danger' : ''}" onclick="changeVKSetting('groupInvites', 'all')">
                    Все пользователи
                </div>
                <div class="vk-option ${vkSettings.groupInvites === 'friends' ? 'selected success' : ''}" onclick="changeVKSetting('groupInvites', 'friends')">
                    Только друзья
                </div>
            </div>
        </div>
    `;
}

// Контент раздела Уведомления
function getNotificationsContent() {
    return `
        <h4 class="vk-section-title">
            <i class="fas fa-bell"></i>
            Уведомления безопасности
        </h4>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Оповещения о входе</div>
                <div class="vk-setting-value">${vkSettings.loginAlerts ? 'Включены' : 'Выключены'}</div>
            </div>
            <div class="vk-setting-desc">
                Уведомлять о каждом входе в ваш аккаунт
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.loginAlerts ? 'selected success' : ''}" onclick="changeVKSetting('loginAlerts', true)">
                    Включить
                </div>
                <div class="vk-option ${!vkSettings.loginAlerts ? 'selected' : ''}" onclick="changeVKSetting('loginAlerts', false)">
                    Выключить
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">О новых устройствах</div>
                <div class="vk-setting-value">${vkSettings.newDeviceAlerts ? 'Включены' : 'Выключены'}</div>
            </div>
            <div class="vk-setting-desc">
                Уведомлять о входе с новых устройств или браузеров
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.newDeviceAlerts ? 'selected success' : ''}" onclick="changeVKSetting('newDeviceAlerts', true)">
                    Включить
                </div>
                <div class="vk-option ${!vkSettings.newDeviceAlerts ? 'selected' : ''}" onclick="changeVKSetting('newDeviceAlerts', false)">
                    Выключить
                </div>
            </div>
        </div>
        
        <div class="vk-setting">
            <div class="vk-setting-header">
                <div class="vk-setting-name">Об изменениях приватности</div>
                <div class="vk-setting-value">${vkSettings.privacyAlerts ? 'Включены' : 'Выключены'}</div>
            </div>
            <div class="vk-setting-desc">
                Оповещать, если кто-то пытается изменить ваши настройки приватности
            </div>
            <div class="vk-options">
                <div class="vk-option ${vkSettings.privacyAlerts ? 'selected success' : ''}" onclick="changeVKSetting('privacyAlerts', true)">
                    Включить
                </div>
                <div class="vk-option ${!vkSettings.privacyAlerts ? 'selected' : ''}" onclick="changeVKSetting('privacyAlerts', false)">
                    Выключить
                </div>
            </div>
        </div>
    `;
}

// Вспомогательные функции
function getVisibilityLabel(value) {
    switch(value) {
        case 'all': return 'Все';
        case 'friends_of_friends': return 'Друзья друзей';
        case 'friends': return 'Только друзья';
        default: return value;
    }
}

function getBirthDateLabel(value) {
    switch(value) {
        case 'full': return 'Полная дата';
        case 'day_month': return 'День и месяц';
        case 'none': return 'Скрыта';
        default: return value;
    }
}

function getContactsLabel(value) {
    switch(value) {
        case 'all': return 'Все';
        case 'friends_of_friends': return 'Друзья друзей';
        case 'friends': return 'Только друзья';
        default: return value;
    }
}

// Изменение настройки
function changeVKSetting(setting, value) {
    vkSettings[setting] = value;
    
    // Обновить текущий раздел
    const activeItem = document.querySelector('.vk-menu-item.active');
    if (activeItem) {
        const onclickText = activeItem.getAttribute('onclick');
        const match = onclickText.match(/showVKSection\('(\w+)'\)/);
        if (match && match[1]) {
            showVKSection(match[1]);
        }
    }
    
    updateVKRisks();
}

// Обновить риски
function updateVKRisks() {
    updateRiskCards();
    updateThreatsList();
}

// Обновить карточки рисков
function updateRiskCards() {
    const container = document.getElementById('vk-risks-grid');
    if (!container) return;
    
    // Расчет рисков
    const dataRisk = calculateDataRisk();
    const hackRisk = calculateHackRisk();
    const spamRisk = calculateSpamRisk();
    
    // Определение уровня риска
    const getRiskLevel = (risk) => risk >= 70 ? 'high' : risk >= 40 ? 'medium' : 'low';
    
    container.innerHTML = `
        <div class="vk-risk-card">
            <div class="vk-risk-header">
                <div class="vk-risk-name">Утечка данных</div>
                <div class="vk-risk-percent ${getRiskLevel(dataRisk)}">${dataRisk}%</div>
            </div>
            <div class="vk-risk-bar">
                <div class="vk-risk-fill ${getRiskLevel(dataRisk)}" style="width: ${dataRisk}%"></div>
            </div>
            <div class="vk-risk-change ${dataRisk < 65 ? 'good' : ''}">
                <i class="fas fa-arrow-${dataRisk < 65 ? 'down' : 'up'}"></i>
                ${dataRisk < 65 ? 'Лучше' : dataRisk > 65 ? 'Хуже' : 'Без изменений'}
            </div>
        </div>
        
        <div class="vk-risk-card">
            <div class="vk-risk-header">
                <div class="vk-risk-name">Взлом аккаунта</div>
                <div class="vk-risk-percent ${getRiskLevel(hackRisk)}">${hackRisk}%</div>
            </div>
            <div class="vk-risk-bar">
                <div class="vk-risk-fill ${getRiskLevel(hackRisk)}" style="width: ${hackRisk}%"></div>
            </div>
            <div class="vk-risk-change ${hackRisk < 80 ? 'good' : ''}">
                <i class="fas fa-arrow-${hackRisk < 80 ? 'down' : 'up'}"></i>
                ${hackRisk < 80 ? 'Лучше' : hackRisk > 80 ? 'Хуже' : 'Без изменений'}
            </div>
        </div>
        
        <div class="vk-risk-card">
            <div class="vk-risk-header">
                <div class="vk-risk-name">Спам и реклама</div>
                <div class="vk-risk-percent ${getRiskLevel(spamRisk)}">${spamRisk}%</div>
            </div>
            <div class="vk-risk-bar">
                <div class="vk-risk-fill ${getRiskLevel(spamRisk)}" style="width: ${spamRisk}%"></div>
            </div>
            <div class="vk-risk-change ${spamRisk < 70 ? 'good' : ''}">
                <i class="fas fa-arrow-${spamRisk < 70 ? 'down' : 'up'}"></i>
                ${spamRisk < 70 ? 'Лучше' : spamRisk > 70 ? 'Хуже' : 'Без изменений'}
            </div>
        </div>
    `;
}

// Расчет рисков
function calculateDataRisk() {
    let risk = 65; // Базовый риск
    
    if (vkSettings.profileVisibility === 'friends') risk -= 20;
    else if (vkSettings.profileVisibility === 'friends_of_friends') risk -= 10;
    
    if (vkSettings.photosVisibility === 'friends') risk -= 15;
    else if (vkSettings.photosVisibility === 'friends_of_friends') risk -= 7;
    
    if (!vkSettings.onlineVisibility) risk -= 5;
    if (vkSettings.birthDateVisibility !== 'full') risk -= 5;
    if (!vkSettings.gamesAccess) risk -= 5;
    if (!vkSettings.appsAccess) risk -= 5;
    
    return Math.max(0, Math.min(100, risk));
}

function calculateHackRisk() {
    let risk = 80; // Базовый риск
    
    if (vkSettings.twoFactorAuth) risk -= 40;
    if (vkSettings.loginHistory) risk -= 10;
    if (vkSettings.sessions) risk -= 10;
    if (!vkSettings.messageApps) risk -= 5;
    if (vkSettings.loginAlerts) risk -= 5;
    if (vkSettings.newDeviceAlerts) risk -= 5;
    
    return Math.max(0, Math.min(100, risk));
}

function calculateSpamRisk() {
    let risk = 70; // Базовый риск
    
    if (vkSettings.friendRequests === 'friends') risk -= 20;
    else if (vkSettings.friendRequests === 'friends_of_friends') risk -= 10;
    
    if (vkSettings.messagesFrom === 'friends') risk -= 20;
    else if (vkSettings.messagesFrom === 'friends_of_friends') risk -= 10;
    
    if (vkSettings.groupInvites === 'friends') risk -= 10;
    
    return Math.max(0, Math.min(100, risk));
}

// Обновить список угроз
function updateThreatsList() {
    const container = document.getElementById('vk-threats-list');
    if (!container) return;
    
    let threats = [];
    
    // Собираем угрозы
    if (vkSettings.profileVisibility === 'all') {
        threats.push({text: 'Профиль открыт', level: 'high'});
    }
    
    if (!vkSettings.twoFactorAuth) {
        threats.push({text: 'Нет 2FA', level: 'high'});
    }
    
    if (vkSettings.photosVisibility === 'all') {
        threats.push({text: 'Фото открыты', level: 'high'});
    } else if (vkSettings.photosVisibility === 'friends_of_friends') {
        threats.push({text: 'Фото видны широко', level: 'medium'});
    }
    
    if (vkSettings.appsAccess) {
        threats.push({text: 'Приложения имеют доступ', level: 'medium'});
    }
    
    if (vkSettings.gamesAccess) {
        threats.push({text: 'Игры имеют доступ', level: 'medium'});
    }
    
    if (vkSettings.friendRequests === 'all') {
        threats.push({text: 'Заявки от всех', level: 'medium'});
    }
    
    if (vkSettings.messagesFrom === 'all') {
        threats.push({text: 'Сообщения от всех', level: 'medium'});
    }
    
    if (vkSettings.onlineVisibility) {
        threats.push({text: 'Онлайн-статус виден', level: 'low'});
    }
    
    if (vkSettings.birthDateVisibility === 'full') {
        threats.push({text: 'Полная дата рождения', level: 'low'});
    }
    
    // Отображаем угрозы
    if (threats.length === 0) {
        container.innerHTML = `
            <div class="vk-threat low">
                <i class="fas fa-check"></i> Все угрозы устранены
            </div>
        `;
        return;
    }
    
    let html = '';
    threats.forEach(threat => {
        html += `
            <div class="vk-threat ${threat.level}">
                <i class="fas fa-exclamation-circle"></i>
                ${threat.text}
            </div>
        `;
    });
    
    container.innerHTML = html;
}

// Сбросить настройки
function resetVKSettings() {
    vkSettings = JSON.parse(JSON.stringify(initialSettings));
    showVKSection('privacy');
    updateVKRisks();
    showNotification('Настройки сброшены');
}

// Применить настройки
function applyVKSettings() {
    // Обновляем начальные настройки
    Object.assign(initialSettings, vkSettings);
    updateVKRisks();
    
    const dataRisk = calculateDataRisk();
    const hackRisk = calculateHackRisk();
    
    showNotification(`Настройки применены. Риск утечки данных: ${dataRisk}%, риск взлома: ${hackRisk}%`);
}

// Завершить тренажер ВК
function completeVKSimulator() {
    if (!currentUser) {
        showNotification('error', 'Для сохранения прогресса войдите в систему');
        showLoginModal();
        return;
    }
    
    const simulatorId = 'security-check';
    
    if (currentUser.completedSimulators && currentUser.completedSimulators.includes(simulatorId)) {
        showNotification('info', 'Тренажер уже был пройден');
        showPage('simulators');
        return;
    }
    
    // Расчет очков
    let score = 0;
    
    if (vkSettings.profileVisibility === 'friends') score += 20;
    if (vkSettings.photosVisibility === 'friends') score += 15;
    if (!vkSettings.onlineVisibility) score += 5;
    if (vkSettings.birthDateVisibility !== 'full') score += 5;
    if (vkSettings.twoFactorAuth) score += 25;
    if (vkSettings.loginHistory) score += 10;
    if (vkSettings.sessions) score += 10;
    if (!vkSettings.gamesAccess) score += 5;
    if (!vkSettings.appsAccess) score += 5;
    if (!vkSettings.messageApps) score += 5;
    if (vkSettings.friendRequests === 'friends') score += 10;
    if (vkSettings.messagesFrom === 'friends') score += 10;
    if (vkSettings.loginAlerts) score += 5;
    if (vkSettings.newDeviceAlerts) score += 5;
    
    const points = Math.round((score / 100) * 30);
    
    // Сохраняем прогресс
    if (!currentUser.completedSimulators) currentUser.completedSimulators = [];
    currentUser.completedSimulators.push(simulatorId);
    currentUser.stats.completedSimulators = (currentUser.stats.completedSimulators || 0) + 1;
    currentUser.stats.score = (currentUser.stats.score || 0) + points;
    currentUser.stats.lastActive = new Date().toISOString();
    
    if (!currentUser.securityStats) currentUser.securityStats = {};
    currentUser.securityStats.vkScore = score;
    currentUser.securityStats.dataRisk = calculateDataRisk();
    currentUser.securityStats.hackRisk = calculateHackRisk();
    
    updateUserInStorage();
    
    // ПРИНУДИТЕЛЬНО ОБНОВЛЯЕМ ПРОГРЕСС-БАРЫ
    updateProgressBars();
    
    showNotification('success', `Тренажер завершен! Получено ${points} очков`);
    
    setTimeout(() => showPage('simulators'), 2000);
}

// Уведомление
function showNotification(message, type = 'info') {
    // Создаем элемент уведомления
    const notification = document.createElement('div');
    notification.className = 'vk-notification';
    notification.innerHTML = `
        <i class="fas fa-${type === 'error' ? 'exclamation-circle' : type === 'success' ? 'check-circle' : 'info-circle'}"></i>
        <span>${message}</span>
    `;
    
    document.body.appendChild(notification);
    
    setTimeout(() => {
        notification.remove();
    }, 3000);
}
        // Контент для тренажера "ПУУ: Анализ звонка" - ИИ-ДИАЛОГОВАЯ ВЕРСИЯ
        function getDefaultSimulatorContent(simulator) {
            if (simulator.title === "Проверка безопасности") {
                return getSecurityCheckSimulatorContent();
            }
            if (simulator.title === "ПУУ: Анализ звонка") {
                return `
                    <div class="ai-phone-container" id="ai-phone-simulator">
<style>
.ai-phone-container {
    background: #f5f7fa;
    border-radius: 15px;
    padding: 25px;
    max-width: 900px;
    margin: 0 auto;
    box-shadow: 0 5px 20px rgba(0,0,0,0.1);
}

.ai-phone-header {
    text-align: center;
    margin-bottom: 25px;
    padding-bottom: 20px;
    border-bottom: 3px solid #43a047;
}

.ai-phone-header h3 {
    color: #43a047;
    margin-bottom: 8px;
    font-size: 1.8rem;
}

.ai-phone-header .subtitle {
    color: #666;
    font-size: 1rem;
    max-width: 700px;
    margin: 0 auto;
}

.scenario-info {
    background: #e8f5e9;
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 20px;
    border-left: 4px solid #43a047;
}

.ai-chat-container {
    display: flex;
    flex-direction: column;
    height: 500px;
    background: white;
    border-radius: 12px;
    overflow: hidden;
    border: 2px solid #e0e6ef;
    margin-bottom: 25px;
}

.ai-chat-messages {
    flex: 1;
    padding: 20px;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    gap: 15px;
    background: #fafbfd;
}

.ai-message {
    max-width: 85%;
    animation: messageAppear 0.3s ease;
}

.ai-message.scammer {
    align-self: flex-start;
    background: #fff3e0;
    border: 2px solid #fb8c00;
    border-radius: 0 15px 15px 15px;
    position: relative;
    padding: 15px 20px;
}

.ai-message.scammer:before {
    content: "🕵️ Мошенник";
    position: absolute;
    top: -8px;
    left: 15px;
    background: #fb8c00;
    color: white;
    padding: 2px 10px;
    border-radius: 10px;
    font-size: 0.7rem;
    font-weight: bold;
}

.ai-message.user {
    align-self: flex-end;
    background: #e3f2fd;
    border: 2px solid #2196f3;
    border-radius: 15px 0 15px 15px;
    position: relative;
    padding: 15px 20px;
}

.ai-message.user:before {
    content: "👤 Вы";
    position: absolute;
    top: -8px;
    right: 15px;
    background: #2196f3;
    color: white;
    padding: 2px 10px;
    border-radius: 10px;
    font-size: 0.7rem;
    font-weight: bold;
}

.ai-message.system {
    align-self: center;
    background: #f3e5f5;
    border: 2px solid #9c27b0;
    border-radius: 15px;
    padding: 15px 20px;
    max-width: 95%;
    text-align: center;
}

.ai-message.lesson {
    align-self: center;
    background: #e8f5e9;
    border: 2px solid #4caf50;
    border-radius: 15px;
    padding: 20px;
    max-width: 90%;
}

.ai-phone-input {
    padding: 20px;
    background: white;
    border-top: 2px solid #e0e6ef;
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.ai-response-option {
    padding: 14px 20px;
    background: #f8f9fa;
    border: 2px solid #dee2e6;
    border-radius: 10px;
    cursor: pointer;
    text-align: left;
    font-size: 0.95rem;
    transition: all 0.2s;
    position: relative;
    overflow: hidden;
}

.ai-response-option:hover {
    background: #e3f2fd;
    border-color: #2196f3;
    transform: translateX(5px);
}

.ai-response-option.danger:hover {
    background: #ffebee;
    border-color: #d32f2f;
}

.ai-response-option.success:hover {
    background: #e8f5e9;
    border-color: #43a047;
}

.ai-response-option.selected {
    background: #e3f2fd;
    border-color: #2196f3;
    font-weight: 500;
}

.ai-stats-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-bottom: 25px;
}

.ai-stat-card {
    background: white;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    border: 2px solid #e0e6ef;
    transition: all 0.3s;
}

.ai-stat-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.ai-stat-value {
    font-size: 2.2rem;
    font-weight: bold;
    margin-bottom: 5px;
}

.ai-stat-label {
    font-size: 0.9rem;
    color: #666;
    font-weight: 500;
}

.puu-indicators {
    background: #fff3e0;
    border-radius: 10px;
    padding: 20px;
    margin-top: 25px;
    border: 2px solid #ff9800;
}

.puu-indicators h4 {
    color: #ff9800;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.indicators-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 12px;
}

.indicator {
    background: white;
    padding: 12px;
    border-radius: 8px;
    border-left: 4px solid #ddd;
    font-size: 0.9rem;
    transition: all 0.3s;
}

.indicator.active {
    border-left-color: #d32f2f;
    background: #ffebee;
    animation: pulse 1.5s infinite;
}

.indicator.detected {
    border-left-color: #43a047;
    background: #e8f5e9;
}

.ai-actions {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 30px;
    padding-top: 25px;
    border-top: 2px solid #e0e6ef;
}

@keyframes puuMessageAppear {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

.ai-message {
    animation: puuMessageAppear 0.3s ease;
}

@keyframes puuPulse {
    0% { box-shadow: 0 0 0 0 rgba(211, 47, 47, 0.4); }
    70% { box-shadow: 0 0 0 10px rgba(211, 47, 47, 0); }
    100% { box-shadow: 0 0 0 0 rgba(211, 47, 47, 0); }
}

.indicator.active {
    animation: puuPulse 1.5s infinite;
}

.hint {
    background: #e3f2fd;
    border: 1px dashed #2196f3;
    border-radius: 8px;
    padding: 12px 15px;
    margin: 10px 0;
    font-size: 0.9rem;
    color: #1565c0;
    display: flex;
    align-items: center;
    gap: 10px;
}

.analysis-panel {
    background: white;
    border-radius: 10px;
    padding: 20px;
    margin-top: 25px;
    border: 2px solid #9c27b0;
    display: none;
}

.analysis-panel.show {
    display: block;
    animation: puuMessageAppear 0.5s ease;
}

.call-status {
    position: fixed;
    top: 20px;
    right: 20px;
    background: #43a047;
    color: white;
    padding: 10px 20px;
    border-radius: 25px;
    font-weight: bold;
    z-index: 1000;
    animation: puuRingAnimation 2s infinite;
    display: none;
}

@keyframes puuRingAnimation {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); box-shadow: 0 0 20px rgba(67, 160, 71, 0.5); }
    100% { transform: scale(1); }
}
</style>
                        <!-- Статус звонка -->
                        <div class="call-status" id="call-status">📞 Имитация звонка...</div>
                        
                        <!-- Заголовок -->
                        <div class="ai-phone-header">
                            <h3>🤖 Тренажер: Диалог с "техподдержкой"</h3>
                            <p class="subtitle">Общайтесь с мошенником, который использует ПУУ-схему. Ваша задача: распознать признаки мошенничества и безопасно завершить разговор.</p>
                        </div>
                        
                        <!-- Информация о сценарии -->
                        <div class="scenario-info" id="scenario-info">
                            <strong>📋 Сценарий:</strong> Вам звонит "служба безопасности Microsoft". Оператор утверждает, что ваш компьютер заражен вирусом и требует срочных действий.
                        </div>
                        
                        <!-- Статистика -->
                        <div class="ai-stats-container">
                            <div class="ai-stat-card">
                                <div class="ai-stat-value" id="security-score">100%</div>
                                <div class="ai-stat-label">Уровень безопасности</div>
                            </div>
                            <div class="ai-stat-card">
                                <div class="ai-stat-value" id="detected-indicators">0/12</div>
                                <div class="ai-stat-label">Обнаружено признаков ПУУ</div>
                            </div>
                            <div class="ai-stat-card">
                                <div class="ai-stat-card">
                                    <div class="ai-stat-value" id="conversation-time">0:00</div>
                                    <div class="ai-stat-label">Длительность разговора</div>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Чат с ИИ -->
                        <div class="ai-chat-container">
                            <div class="ai-chat-messages" id="ai-chat-messages">
                                <!-- Сообщения будут добавляться здесь -->
                            </div>
                            <div class="ai-phone-input" id="ai-phone-input">
                                <!-- Варианты ответов будут здесь -->
                            </div>
                        </div>
                        
                        <!-- Индикаторы ПУУ -->
                        <div class="puu-indicators">
                            <h4><i class="fas fa-exclamation-triangle"></i> Признаки ПУУ-схемы</h4>
                            <div class="indicators-grid" id="puu-indicators">
                                <!-- Индикаторы будут добавляться динамически -->
                            </div>
                        </div>
                        
                        <!-- Панель анализа -->
                        <div class="analysis-panel" id="analysis-panel">
                            <h4><i class="fas fa-chart-line"></i> Анализ ваших ответов</h4>
                            <div id="analysis-content"></div>
                        </div>
                        
                        <!-- Кнопки действий -->
                        <div class="ai-actions">
                            <button class="btn btn-outline" onclick="restartPuuSimulator()">
                                <i class="fas fa-redo"></i> Начать заново
                            </button>
                            <button class="btn" onclick="showPuuAnalysis()">
                                <i class="fas fa-lightbulb"></i> Подсказка
                            </button>
                        </div>
                    </div>
                `;
            }

if (simulator.title === "Госуслуги: Проверка сайта") {
        return getGosuslugiSimulatorContent();
    }    

    // Для остальных тренажеров - старый контент
    return `
        <div class="simulator">
            <h3>Тренажер: ${simulator.title}</h3>
            <p>${simulator.description}</p>
            <p>Этот тренажер находится в разработке. В полной версии здесь будут интерактивные задания.</p>
            
            <div style="text-align: center; padding: 40px 0;">
                <i class="fas fa-tools" style="font-size: 4rem; color: #ddd; margin-bottom: 20px;"></i>
                <p>Тренажер скоро будет доступен</p>
            </div>
        </div>
    `;
}
        // Выбор опции в тренажере
function selectSimulatorOption(element, isCorrect) {
    // Устанавливаем атрибут correct если передан
    if (isCorrect !== undefined) {
        element.dataset.correct = isCorrect === 'correct';
    }
    
    // Определяем контейнер с вопросами
    const questionContainer = element.closest('.simulator');
    if (!questionContainer) return;
    
    // Ищем все опции в этом же вопросе
    const allOptionsInQuestion = questionContainer.querySelectorAll('.option');
    
    // Проверяем тип вопроса по количеству правильных ответов
    let correctOptionsCount = 0;
    allOptionsInQuestion.forEach(opt => {
        if (opt.dataset.correct === 'true') {
            correctOptionsCount++;
        }
    });
    
    // Если правильных ответов больше 1 - это множественный выбор
    if (correctOptionsCount > 1) {
        // Для множественного выбора - переключаем состояние
        element.classList.toggle('selected');
    } else {
        // Для одиночного выбора - снимаем выделение с других
        allOptionsInQuestion.forEach(opt => {
            opt.classList.remove('selected');
        });
        element.classList.add('selected');
    }
}
        
        // Проверка ответа в тренажере
        function checkSimulatorAnswer() {
            const selectedOption = document.querySelector('.option.selected');
            const resultDiv = document.getElementById('simulator-result');
            
            if (!selectedOption) {
                resultDiv.innerHTML = '<i class="fas fa-exclamation-circle warning-icon icon"></i> Пожалуйста, выберите вариант ответа';
                resultDiv.className = 'result error';
                resultDiv.style.display = 'block';
                return;
            }
            
            if (selectedOption.dataset.correct === 'true') {
                resultDiv.innerHTML = '<i class="fas fa-check-circle success-icon icon"></i> <strong>Правильно!</strong> Вы правильно определили фишинговое письмо.';
                resultDiv.className = 'result success';
            } else {
                resultDiv.innerHTML = '<i class="fas fa-exclamation-circle danger-icon icon"></i> <strong>Неправильно.</strong> Второе письмо - фишинг. Обратите внимание на подозрительный домен отправителя.';
                resultDiv.className = 'result error';
            }
            
            resultDiv.style.display = 'block';
        }
        
        // Проверка стойкости пароля
function checkPasswordStrength() {
    const password = document.getElementById('password-input').value;
    const resultDiv = document.getElementById('password-result');
    
    if (!password) {
        resultDiv.innerHTML = '<div class="result error"><i class="fas fa-exclamation-circle icon"></i> Введите пароль для проверки</div>';
        return;
    }
    
    let strength = 0;
    let feedback = '';
    let messages = [];
    
    // Проверка длины
    if (password.length >= 8) strength++;
    if (password.length >= 12) strength += 2;
    
    // Проверка наличия разных типов символов
    if (/[A-Z]/.test(password)) strength++;
    if (/[a-z]/.test(password)) strength++;
    if (/[0-9]/.test(password)) strength++;
    if (/[^A-Za-z0-9]/.test(password)) strength++;
    
    // Анализ и рекомендации
    if (password.length < 8) {
        messages.push('Пароль слишком короткий (минимум 8 символов)');
    }
    
    if (!/[A-Z]/.test(password)) {
        messages.push('Добавьте заглавные буквы');
    }
    
    if (!/[a-z]/.test(password)) {
        messages.push('Добавьте строчные буквы');
    }
    
    if (!/[0-9]/.test(password)) {
        messages.push('Добавьте цифры');
    }
    
    if (!/[^A-Za-z0-9]/.test(password)) {
        messages.push('Добавьте специальные символы (!@#$%^&* и т.д.)');
    }
    
    // Оценка стойкости
    let strengthText = '';
    let colorClass = '';
    
    if (strength <= 2) {
        strengthText = 'Очень слабый';
        colorClass = 'error';
        feedback = '<div class="result error"><i class="fas fa-times-circle icon"></i> <strong>Очень слабый пароль.</strong> Легко взламывается.</div>';
    } else if (strength <= 4) {
        strengthText = 'Слабый';
        colorClass = 'warning';
        feedback = '<div class="result" style="background-color: #fff3e0; border-color: #ff9800; color: #ef6c00;"><i class="fas fa-exclamation-triangle icon"></i> <strong>Слабый пароль.</strong> Нужно усилить.</div>';
    } else if (strength <= 6) {
        strengthText = 'Средний';
        colorClass = 'info';
        feedback = '<div class="result" style="background-color: #e3f2fd; border-color: #2196f3; color: #1565c0;"><i class="fas fa-check-circle icon"></i> <strong>Средний пароль.</strong> Можно усилить.</div>';
    } else if (strength <= 8) {
        strengthText = 'Хороший';
        colorClass = 'success';
        feedback = '<div class="result" style="background-color: #e8f5e9; border-color: #4caf50; color: #2e7d32;"><i class="fas fa-check-circle icon"></i> <strong>Хороший пароль.</strong> Достаточно надежный.</div>';
    } else {
        strengthText = 'Отличный';
        colorClass = 'success';
        feedback = '<div class="result success"><i class="fas fa-shield-alt icon"></i> <strong>Отличный пароль!</strong> Очень сложно взломать.</div>';
    }
    
    // Добавляем рекомендации, если пароль не идеален
    if (messages.length > 0 && strength <= 8) {
        feedback += '<div style="margin-top: 15px; padding: 10px; background-color: #f9f9f9; border-radius: 5px;"><strong>Рекомендации:</strong><ul style="margin-top: 10px; margin-left: 20px;">';
        messages.forEach(msg => {
            feedback += `<li>${msg}</li>`;
        });
        feedback += '</ul></div>';
    }
    
    // Показываем оценку
    feedback = `<div style="margin-bottom: 15px; font-size: 1.1rem;"><strong>Оценка:</strong> <span style="color: ${colorClass === 'error' ? '#d32f2f' : colorClass === 'warning' ? '#f57c00' : colorClass === 'success' ? '#388e3c' : '#1976d2'}">${strengthText}</span> (${strength}/10 баллов)</div>` + feedback;
    
    resultDiv.innerHTML = feedback;
}  
        // Генерация пароля
        function generatePassword() {
            const chars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+-=[]{}|;:,.<>?';
            let password = '';
            
            for (let i = 0; i < 16; i++) {
                password += chars.charAt(Math.floor(Math.random() * chars.length));
            }
            
            document.getElementById('generated-password').textContent = password;
        }
        
        // Открытие вкладки
        function openTab(evt, tabName) {
            const tabContents = document.querySelectorAll('.tab-content');
            tabContents.forEach(tab => {
                tab.classList.remove('active');
            });
            
            const tabs = document.querySelectorAll('.tab');
            tabs.forEach(tab => {
                tab.classList.remove('active');
            });
            
            document.getElementById(tabName).classList.add('active');
            evt.currentTarget.classList.add('active');
        }
        
        // Сброс прогресса
        function resetProgress() {
            if (confirm('Вы уверены, что хотите сбросить весь прогресс? Это действие нельзя отменить.')) {
                currentUser.stats = {
                    score: 0,
                    completedLessons: 0,
                    completedSimulators: 0,
                    testResults: [],
                    lastActive: new Date().toISOString()
                };
                
                currentUser.progress = {
                    phishing: 0,
                    calls: 0,
                    gosuslugi: 0,
                    puu: 0,
                    passwords: 0,
                    social: 0,
                    financial: 0,
                    mobile: 0
                };
                
                currentUser.completedCourses = [];
                currentUser.completedSimulators = [];
                currentUser.courseProgress = {};
                
                updateUserInStorage();
                showNotification('success', 'Прогресс сброшен');
                loadProfilePage();
            }
        }
        
        // Удаление аккаунта
        function deleteAccount() {
            if (confirm('Вы уверены, что хотите удалить аккаунт? Все ваши данные будут утеряны.')) {
                users = users.filter(u => u.id !== currentUser.id);
                localStorage.setItem('cyberAcademyUsers', JSON.stringify(users));
                logoutUser();
                showNotification('info', 'Аккаунт успешно удален');
            }
        }
        
        // Обновление пользователя в хранилище
        function updateUserInStorage() {
            const index = users.findIndex(u => u.id === currentUser.id);
            if (index !== -1) {
                users[index] = currentUser;
                localStorage.setItem('cyberAcademyUsers', JSON.stringify(users));
            }
            
            localStorage.setItem('cyberAcademyCurrentUser', JSON.stringify(currentUser));
        }
        
        // Вспомогательные функции
        function showLoginModal() {
            document.getElementById('loginModal').style.display = 'flex';
            document.getElementById('loginEmail').focus();
        }
        
        function showRegisterModal() {
            closeModal('loginModal');
            document.getElementById('registerModal').style.display = 'flex';
            document.getElementById('registerName').focus();
        }
        
        function closeModal(modalId) {
            document.getElementById(modalId).style.display = 'none';
            clearFormErrors(modalId.replace('Modal', ''));
        }
        
        function clearFormErrors(formType) {
            document.querySelectorAll(`#${formType}Form .form-error`).forEach(error => {
                error.style.display = 'none';
                error.textContent = '';
            });
        }
        
        function showFormError(elementId, message) {
            const element = document.getElementById(elementId);
            element.textContent = message;
            element.style.display = 'block';
        }
        
        function showNotification(type, message) {
            const notification = document.createElement('div');
            notification.className = `notification ${type}`;
            notification.textContent = message;
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.remove();
            }, 3000);
        }
        
        function isValidEmail(email) {
            return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
        }
        
        function generateUserId() {
            return 'user_' + Math.random().toString(36).substr(2, 9);
        }
        
        function toggleMenu() {
            const menu = document.getElementById('navMenu');
            menu.classList.toggle('active');
        }
        
        // Вспомогательные функции для главной страницы
        function startLearning() {
            if (currentUser) {
                showPage('courses');
            } else {
                showRegisterModal();
            }
        }
        
        // Закрытие модальных окон при клике вне их
        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.style.display = 'none';
                clearFormErrors(event.target.id.replace('Modal', ''));
            }
        };
function checkPhishingTask1() {
    // Находим первый симулятор
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[0];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('phishing-result-1');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Вы правильно определили фишинговое письмо.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Второе письмо - фишинг. Обратите внимание на подозрительный домен отправителя.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkPhishingTask2() {
    // Находим второй симулятор
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[1];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('phishing-result-2');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! Ссылка ведет на фишинговый сайт.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильно. Ссылка ведет на фишинговый сайт.Будьте очень осторожны.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkPhishingTask3() {
    // Находим третий симулятор
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[2];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('phishing-result-3');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! Это фишинговое SMS (смишинг). Признаки: сообщение пришло с обычного мобильного номера, а не с короткого банковского; ссылка ведет на подозрительный домен sber-security.ru вместо официального sberbank.ru; в сообщении создается ощущение срочности.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильно. Это фишинговое SMS (смишинг). Обратите внимание: 1) Сообщение пришло с обычного мобильного номера, а банки используют короткие номера; 2) Ссылка ведет на sber-security.ru, а не на официальный sberbank.ru; 3) Создается искусственная срочность ситуации.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}
function checkPhoneTask1() {
    // Находим первый сценарий
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[0];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('phone-result-1');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! Вежливый отказ и самостоятельный звонок в банк — это самый безопасный вариант. Мошенники часто просят назвать коды из SMS, чтобы получить доступ к вашим счетам.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильный выбор. Никогда не называйте коды из SMS посторонним! Даже если звонящий представляется сотрудником банка. Банки никогда не просят называть коды из SMS. Правильный ответ: вежливо отказаться и перезвонить в банк самостоятельно по официальному номеру.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkPhoneTask2() {
    // Находим второй сценарий
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[1];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('phone-result-2');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! Проверка баланса через официальное приложение — это самый безопасный способ. Операторы связи не звонят с требованием срочно пополнить счет на конкретный номер.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильный выбор. Мошенники часто звонят, представляясь операторами связи, и требуют срочно пополнить счет на указанный номер. Правильный ответ: проверить баланс через официальное приложение или позвонить в службу поддержки оператора по официальному номеру.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkPhoneTask3() {
    // Находим третий сценарий
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[2];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('phone-result-3');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! Государственные службы никогда не требуют оплаты комиссии для получения выплат. Все социальные выплаты предоставляются бесплатно. Если вам действительно положена выплата, нужно самостоятельно обратиться в официальные органы.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильный выбор. Это классическая схема мошенничества. Государственные социальные службы НИКОГДА не требуют оплаты комиссии для получения выплат. Все официальные выплаты предоставляются бесплатно. Если звонят с предложением выплат за комиссию - это 100% мошенники.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkPuuTask1() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[0];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('puu-result-1');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! При звонках от автоответчика с предложением нажать цифру для соединения с оператором - это явный признак мошенничества. Банки никогда не используют такие схемы. Самый безопасный вариант - положить трубку и проверить ситуацию через официальное приложение банка.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильный выбор. Автоответчики, предлагающие нажать цифру для соединения - это классическая схема мошенников. Настоящие банки так не звонят. Никогда не нажимайте цифры в таких случаях - это может подключить вас к платным услугам или мошенникам.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkPuuTask2() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[1];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('puu-result-2');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! Просьба установить программу удаленного доступа (AnyDesk, TeamViewer и т.д.) - это ключевой признак ПУУ-схемы. Мошенники получат полный контроль над вашим компьютером и смогут украсть деньги. Единственно верное действие - немедленно положить трубку.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Опасный выбор! Установка программ удаленного доступа по просьбе "оператора" - это прямой путь к потере денег. Мошенники получат контроль над вашим компьютером, увидят все ваши действия с банковскими приложениями и украдут деньги. Немедленно кладите трубку в таких ситуациях.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkPuuTask3() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[2];
    
    const selectedOptions = simulator.querySelectorAll('.option.selected');
    const resultDiv = document.getElementById('puu-result-3');
    
    if (selectedOptions.length === 0) {
        resultDiv.innerHTML = '<i class="fas fa-exclamation-circle icon"></i> Пожалуйста, выберите хотя бы один вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    // Определяем правильные варианты
    const correctOptions = [
        'Просьба установить программу удаленного доступа',
        'Требование ввести данные банковской карты',
        'Создание ощущения срочности и опасности',
        'Просьба назвать коды из SMS-сообщений'
    ];
    
    // Проверяем выбранные ответы
    let userCorrect = 0;
    let userIncorrect = 0;
    const totalCorrect = correctOptions.length;
    
    selectedOptions.forEach(option => {
        const optionText = option.textContent.trim();
        if (correctOptions.includes(optionText)) {
            userCorrect++;
            option.classList.add('correct');
            option.classList.remove('incorrect');
        } else {
            userIncorrect++;
            option.classList.add('incorrect');
            option.classList.remove('correct');
        }
    });
    
    // Подсвечиваем неправильно пропущенные варианты
    const allOptions = simulator.querySelectorAll('.option');
    allOptions.forEach(option => {
        const optionText = option.textContent.trim();
        if (!option.classList.contains('selected') && correctOptions.includes(optionText)) {
            option.classList.add('correct');
        }
    });
    
    if (userCorrect === totalCorrect && userIncorrect === 0) {
        resultDiv.innerHTML = '<i class="fas fa-check-circle icon"></i> <strong>Отлично!</strong> Вы правильно определили все признаки ПУУ-схемы:<br><br>' +
            '✓ <strong>Просьба установить программу удаленного доступа</strong> - мошенники получают контроль над устройством<br>' +
            '✓ <strong>Требование ввести данные банковской карты</strong> - прямой путь к краже денег<br>' +
            '✓ <strong>Создание ощущения срочности</strong> - чтобы вы не успели подумать<br>' +
            '✓ <strong>Просьба назвать коды из SMS</strong> - для подтверждения операций<br><br>' +
            '<em>Всего правильных ответов: ' + userCorrect + ' из ' + totalCorrect + '</em>';
        resultDiv.className = 'result success';
    } else if (userIncorrect > 0) {
        resultDiv.innerHTML = '<i class="fas fa-exclamation-circle icon"></i> <strong>Есть ошибки в выборе.</strong> Основные признаки ПУУ-схемы:<br><br>' +
            '✓ <strong>Просьба установить программу удаленного доступа</strong> (AnyDesk, TeamViewer)<br>' +
            '✓ <strong>Требование ввести данные банковской карты</strong><br>' +
            '✓ <strong>Создание ощущения срочности</strong> ("срочно", "ваша карта заблокируется")<br>' +
            '✓ <strong>Просьба назвать коды из SMS</strong> (для "подтверждения" или "блокировки")<br><br>' +
            '<em>Ваш результат: ' + userCorrect + ' из ' + totalCorrect + ' правильных ответов</em><br>' +
            '<em>Неправильных выборов: ' + userIncorrect + '</em><br><br>' +
            'Помните: настоящая техподдержка никогда не просит установить программы удаленного доступа или назвать коды из SMS!';
        resultDiv.className = 'result error';
    } else {
        resultDiv.innerHTML = '<i class="fas fa-info-circle icon"></i> <strong>Хорошо, но не все признаки выбраны.</strong> Правильные признаки ПУУ-схемы:<br><br>' +
            '✓ Просьба установить программу удаленного доступа<br>' +
            '✓ Требование ввести данные банковской карты<br>' +
            '✓ Создание ощущения срочности и опасности<br>' +
            '✓ Просьба назвать коды из SMS-сообщений<br><br>' +
            '<em>Вы выбрали ' + userCorrect + ' из ' + totalCorrect + ' правильных вариантов.</em><br>' +
            'Попробуйте выбрать все правильные ответы!';
        resultDiv.className = 'result';
        resultDiv.style.backgroundColor = '#fff3e0';
        resultDiv.style.border = '2px solid #ff9800';
        resultDiv.style.color = '#ef6c00';
    }
    
    resultDiv.style.display = 'block';
}
function checkSecurityTask1() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[0];
    
    const selectedOptions = simulator.querySelectorAll('.option.selected');
    const resultDiv = document.getElementById('security-result-1');
    
    if (selectedOptions.length === 0) {
        resultDiv.innerHTML = '<i class="fas fa-exclamation-circle icon"></i> Пожалуйста, выберите хотя бы один вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    // Правильные ответы
    const correctOptions = [
        'Длина пароля не менее 12 символов',
        'Использовать заглавные и строчные буквы, цифры и специальные символы',
        'Не использовать личную информацию (даты рождения, имена)',
        'Использовать менеджер паролей'
    ];
    
    // Проверяем выбранные ответы
    let userCorrect = 0;
    let userIncorrect = 0;
    const totalCorrect = correctOptions.length;
    
    selectedOptions.forEach(option => {
        const optionText = option.textContent.trim();
        if (correctOptions.includes(optionText)) {
            userCorrect++;
            option.classList.add('correct');
            option.classList.remove('incorrect');
        } else {
            userIncorrect++;
            option.classList.add('incorrect');
            option.classList.remove('correct');
        }
    });
    
    // Подсвечиваем неправильно пропущенные варианты
    const allOptions = simulator.querySelectorAll('.option');
    allOptions.forEach(option => {
        const optionText = option.textContent.trim();
        if (!option.classList.contains('selected') && correctOptions.includes(optionText)) {
            option.classList.add('correct');
        }
    });
    
    if (userCorrect === totalCorrect && userIncorrect === 0) {
        resultDiv.innerHTML = '<i class="fas fa-check-circle icon"></i> <strong>Отлично!</strong> Вы знаете все правила создания безопасных паролей:<br><br>' +
            '✓ <strong>Длина не менее 12 символов</strong> - чем длиннее пароль, тем сложнее его взломать<br>' +
            '✓ <strong>Разные типы символов</strong> - усложняет подбор<br>' +
            '✓ <strong>Без личной информации</strong> - даты, имена легко узнать<br>' +
            '✓ <strong>Менеджер паролей</strong> - помогает создавать и хранить сложные пароли<br><br>' +
            '<em>Важно: не нужно менять пароль слишком часто без необходимости</em>';
        resultDiv.className = 'result success';
    } else if (userIncorrect > 0) {
        resultDiv.innerHTML = '<i class="fas fa-exclamation-circle icon"></i> <strong>Есть ошибки в выборе.</strong> Безопасные настройки пароля:<br><br>' +
            '✓ <strong>Длина не менее 12 символов</strong><br>' +
            '✓ <strong>Использовать разные типы символов</strong> (A-Z, a-z, 0-9, !@#$)<br>' +
            '✓ <strong>Не использовать личную информацию</strong><br>' +
            '✓ <strong>Использовать менеджер паролей</strong><br><br>' +
            '<em>Неправильно:</em><br>' +
            '✗ Использовать одну и ту же комбинацию - это делает пароль уязвимым<br>' +
            '✗ Менять пароль каждую неделю - приводит к использованию простых паролей<br><br>' +
            '<em>Ваш результат: ' + userCorrect + ' из ' + totalCorrect + ' правильных ответов</em>';
        resultDiv.className = 'result error';
    } else {
        resultDiv.innerHTML = '<i class="fas fa-info-circle icon"></i> <strong>Хорошо, но не все правила выбраны.</strong> Основные правила:<br><br>' +
            '✓ Длина пароля не менее 12 символов<br>' +
            '✓ Использовать разные типы символов<br>' +
            '✓ Не использовать личную информацию<br>' +
            '✓ Использовать менеджер паролей<br><br>' +
            '<em>Вы выбрали ' + userCorrect + ' из ' + totalCorrect + ' правильных вариантов.</em>';
        resultDiv.className = 'result';
        resultDiv.style.backgroundColor = '#fff3e0';
        resultDiv.style.border = '2px solid #ff9800';
        resultDiv.style.color = '#ef6c00';
    }
    
    resultDiv.style.display = 'block';
}

function checkSecurityTask2() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[1];
    
    const selectedOptions = simulator.querySelectorAll('.option.selected');
    const resultDiv = document.getElementById('security-result-2');
    
    if (selectedOptions.length === 0) {
        resultDiv.innerHTML = '<i class="fas fa-exclamation-circle icon"></i> Пожалуйста, выберите хотя бы один вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    // Правильные ответы
    const correctOptions = [
        'Использовать приложение-аутентификатор (Google Authenticator, Microsoft Authenticator)',
        'Использовать аппаратные ключи безопасности (YubiKey)',
        'Использовать биометрическую аутентификацию (отпечаток пальца, лицо)'
    ];
    
    // Проверяем выбранные ответы
    let userCorrect = 0;
    let userIncorrect = 0;
    const totalCorrect = correctOptions.length;
    
    selectedOptions.forEach(option => {
        const optionText = option.textContent.trim();
        if (correctOptions.includes(optionText)) {
            userCorrect++;
            option.classList.add('correct');
            option.classList.remove('incorrect');
        } else {
            userIncorrect++;
            option.classList.add('incorrect');
            option.classList.remove('correct');
        }
    });
    
    // Подсвечиваем неправильно пропущенные варианты
    const allOptions = simulator.querySelectorAll('.option');
    allOptions.forEach(option => {
        const optionText = option.textContent.trim();
        if (!option.classList.contains('selected') && correctOptions.includes(optionText)) {
            option.classList.add('correct');
        }
    });
    
    if (userCorrect === totalCorrect && userIncorrect === 0) {
        resultDiv.innerHTML = '<i class="fas fa-check-circle icon"></i> <strong>Отлично!</strong> Вы знаете самые безопасные методы двухфакторной аутентификации:<br><br>' +
            '✓ <strong>Приложения-аутентификаторы</strong> - коды генерируются локально, не передаются по сети<br>' +
            '✓ <strong>Аппаратные ключи</strong> - максимальная защита, устойчивы к фишингу<br>' +
            '✓ <strong>Биометрия</strong> - уникальные физические характеристики пользователя<br><br>' +
            '<em>Менее безопасные методы:</em><br>' +
            '✗ SMS - подвержены перехвату и SIM-свопу<br>' +
            '✗ Резервные email - если email взломан, безопасность снижается<br>' +
            '✗ Контрольные вопросы - ответы часто можно найти в соцсетях';
        resultDiv.className = 'result success';
    } else if (userIncorrect > 0) {
        resultDiv.innerHTML = '<i class="fas fa-exclamation-circle icon"></i> <strong>Есть ошибки в выборе.</strong> Самые безопасные методы 2FA:<br><br>' +
            '✓ <strong>Приложения-аутентификаторы</strong> (Google/Microsoft Authenticator)<br>' +
            '✓ <strong>Аппаратные ключи</strong> (YubiKey, Titan Key)<br>' +
            '✓ <strong>Биометрия</strong><br><br>' +
            '<em>Почему другие методы менее безопасны:</em><br>' +
            '✗ SMS - можно перехватить или перенести SIM-карту<br>' +
            '✗ Резервные email - уязвимость второго фактора<br>' +
            '✗ Контрольные вопросы - информация часто публична<br><br>' +
            '<em>Ваш результат: ' + userCorrect + ' из ' + totalCorrect + ' правильных ответов</em>';
        resultDiv.className = 'result error';
    } else {
        resultDiv.innerHTML = '<i class="fas fa-info-circle icon"></i> <strong>Хорошо, но не все методы выбраны.</strong> Самые безопасные методы:<br><br>' +
            '✓ Приложения-аутентификаторы<br>' +
            '✓ Аппаратные ключи безопасности<br>' +
            '✓ Биометрическая аутентификация<br><br>' +
            '<em>Вы выбрали ' + userCorrect + ' из ' + totalCorrect + ' правильных вариантов.</em>';
        resultDiv.className = 'result';
        resultDiv.style.backgroundColor = '#fff3e0';
        resultDiv.style.border = '2px solid #ff9800';
        resultDiv.style.color = '#ef6c00';
    }
    
    resultDiv.style.display = 'block';
}

function checkSecurityTask3() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[2];
    
    const selectedOptions = simulator.querySelectorAll('.option.selected');
    const resultDiv = document.getElementById('security-result-3');
    
    if (selectedOptions.length === 0) {
        resultDiv.innerHTML = '<i class="fas fa-exclamation-circle icon"></i> Пожалуйста, выберите хотя бы один вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    // Правильные ответы
    const correctOptions = [
        'Проверить адрес отправителя и домен ссылки',
        'Удалить письмо, не открывая вложений и не переходя по ссылкам',
        'Сообщить в ИТ-отдел или службу безопасности'
    ];
    
    // Проверяем выбранные ответы
    let userCorrect = 0;
    let userIncorrect = 0;
    const totalCorrect = correctOptions.length;
    
    selectedOptions.forEach(option => {
        const optionText = option.textContent.trim();
        if (correctOptions.includes(optionText)) {
            userCorrect++;
            option.classList.add('correct');
            option.classList.remove('incorrect');
        } else {
            userIncorrect++;
            option.classList.add('incorrect');
            option.classList.remove('correct');
        }
    });
    
    // Подсвечиваем неправильно пропущенные варианты
    const allOptions = simulator.querySelectorAll('.option');
    allOptions.forEach(option => {
        const optionText = option.textContent.trim();
        if (!option.classList.contains('selected') && correctOptions.includes(optionText)) {
            option.classList.add('correct');
        }
    });
    
    if (userCorrect === totalCorrect && userIncorrect === 0) {
        resultDiv.innerHTML = '<i class="fas fa-check-circle icon"></i> <strong>Отлично!</strong> Вы знаете правильные действия при получении подозрительных писем:<br><br>' +
            '✓ <strong>Проверить отправителя</strong> - искать подозрительные домены и адреса<br>' +
            '✓ <strong>Не открывать вложения</strong> - могут содержать вирусы<br>' +
            '✓ <strong>Не переходить по ссылкам</strong> - могут вести на фишинговые сайты<br>' +
            '✓ <strong>Сообщить специалистам</strong> - ИТ-отдел поможет оценить угрозу<br><br>' +
            '<em>Помните: открытие вложений от неизвестных отправителей - одна из главных причин заражения!</em>';
        resultDiv.className = 'result success';
    } else if (userIncorrect > 0) {
        resultDiv.innerHTML = '<i class="fas fa-exclamation-circle icon"></i> <strong>Есть опасные ошибки!</strong> Безопасные действия:<br><br>' +
            '✓ <strong>Проверить отправителя</strong> - ищите опечатки в домене<br>' +
            '✓ <strong>Удалить письмо</strong> - не открывая вложений и ссылок<br>' +
            '✓ <strong>Сообщить специалистам</strong> - если это рабочая почта<br><br>' +
            '<em>Опасные действия (НИКОГДА так не делайте!):</em><br>' +
            '✗ Открывать вложения - могут быть вирусы, трояны, шифровальщики<br>' +
            '✗ Переходить по ссылкам - могут быть фишинговые сайты<br>' +
            '✗ Спрашивать у коллег - они тоже могут ошибиться<br><br>' +
            '<em>Ваш результат: ' + userCorrect + ' из ' + totalCorrect + ' правильных ответов</em>';
        resultDiv.className = 'result error';
    } else {
        resultDiv.innerHTML = '<i class="fas fa-info-circle icon"></i> <strong>Хорошо, но не все безопасные действия выбраны.</strong> Правильные действия:<br><br>' +
            '✓ Проверить адрес отправителя<br>' +
            '✓ Удалить письмо без открытия<br>' +
            '✓ Сообщить в службу безопасности<br><br>' +
            '<em>Вы выбрали ' + userCorrect + ' из ' + totalCorrect + ' правильных вариантов.</em>';
        resultDiv.className = 'result';
        resultDiv.style.backgroundColor = '#fff3e0';
        resultDiv.style.border = '2px solid #ff9800';
        resultDiv.style.color = '#ef6c00';
    }
    
    resultDiv.style.display = 'block';
}
function checkGosuslugiTask1() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[0];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('gosuslugi-result-1');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! Официальный сайт Госуслуг - это gosuslugi.ru<br><br>' +
            'Запомните: мошенники создают похожие адреса с опечатками или добавляют лишние слова (online, portal, help).';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильно. Правильный ответ: gosuslugi.ru<br><br>' +
            'Официальный сайт всегда имеет адрес gosuslugi.ru<br>' +
            'Другие варианты с добавлением слов или изменением домена - это мошеннические сайты.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkGosuslugiTask2() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[1];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('gosuslugi-result-2');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! Безопасное соединение показывают:<br>' +
            '• Значок замка в адресной строке<br>' +
            '• Адрес начинается с https://<br>' +
            '• Домен gosuslugi.ru<br><br>' +
            'Если нет замка или адрес начинается с http:// - не вводите свои данные!';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильно. Главный признак безопасности - значок замка и https:// в адресе.<br><br>' +
            'Быстрая загрузка или много информации не гарантируют безопасность.<br>' +
            'Всегда проверяйте адресную строку перед входом на Госуслуги.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}

function checkGosuslugiTask3() {
    const simulators = document.querySelectorAll('.simulator');
    const simulator = simulators[2];
    
    const selectedOption = simulator.querySelector('.option.selected');
    const resultDiv = document.getElementById('gosuslugi-result-3');
    
    if (!selectedOption) {
        resultDiv.innerHTML = 'Пожалуйста, выберите вариант ответа';
        resultDiv.className = 'result error';
        resultDiv.style.display = 'block';
        return;
    }
    
    if (selectedOption.dataset.correct === 'true') {
        resultDiv.innerHTML = 'Правильно! При получении подозрительных SMS:<br><br>' +
            '1. НЕ переходите по ссылкам<br>' +
            '2. НЕ звоните по номерам из SMS<br>' +
            '3. Зайдите на официальный сайт gosuslugi.ru<br>' +
            '4. Проверьте статус аккаунта в личном кабинете<br><br>' +
            'Госуслуги никогда не блокируют аккаунты через SMS с ссылками.';
        resultDiv.className = 'result success';
    } else {
        resultDiv.innerHTML = 'Неправильно! Это мошенническое SMS.<br><br>' +
            'НИКОГДА не переходите по ссылкам из подозрительных сообщений!<br>' +
            'НИКОГДА не звоните по номерам из таких SMS!<br><br>' +
            'Правильный ответ: зайти на официальный сайт и проверить аккаунт.';
        resultDiv.className = 'result error';
    }
    
    resultDiv.style.display = 'block';
}
// ============================
// ДИАЛОГОВЫЙ ТРЕНАЖЕР ГОСУСЛУГИ
// ============================

// Глобальные переменные для тренажера Госуслуги
let gosuslugiCurrentStep = 0;
let gosuslugiSecurityScore = 100;
let gosuslugiTrustScore = 0;
let gosuslugiSimulationFinished = false;

// Структура диалога
const gosuslugiDialogueSteps = [
    {
        sender: "sms",
        text: "🔔 **СМС от Госуслуг:** Ваш аккаунт будет заблокирован через 2 часа. Для проверки данных перейдите: gosuslugi-secure.ru",
        options: [
            {
                text: "Быстро перейти по ссылке и проверить",
                effect: { security: -40, trust: +30 },
                response: "📱 Вы перешли на сайт. Похоже на Госуслуги, но адрес странный. Вас просят ввести логин, пароль и код из SMS...",
                nextStep: 1
            },
            {
                text: "Игнорировать и удалить SMS",
                effect: { security: +10, trust: 0 },
                response: "✅ Вы удалили подозрительное SMS. Это безопасно!",
                nextStep: 4
            },
            {
                text: "Проверить официальный сайт gosuslugi.ru",
                effect: { security: +20, trust: 0 },
                response: "🌐 Вы зашли на настоящий Госуслуги. Ваш аккаунт в порядке, уведомлений нет.",
                nextStep: 3
            }
        ]
    },
    {
        sender: "scammer",
        text: "Добрый день! Это служба безопасности Госуслуг. Ваш аккаунт взломали. Для защиты нужно срочно сообщить код из SMS, который мы вам отправили.",
        options: [
            {
                text: "Сообщить код из SMS",
                effect: { security: -60, trust: +50 },
                response: "💸 Мошенник получил доступ к вашему аккаунту! Деньги со счета выводятся...",
                nextStep: 5
            },
            {
                text: "Отказаться и позвонить в официальную поддержку",
                effect: { security: +30, trust: -20 },
                response: "📞 Вы позвонили на номер 8-800-100-70-10. Вам подтвердили, что это мошенники!",
                nextStep: 4
            },
            {
                text: "Спросить служебное удостоверение",
                effect: { security: +10, trust: 0 },
                response: "👮 'Я вышлю фото удостоверения на WhatsApp'. Приходит сфотошопленная картинка.",
                nextStep: 2
            }
        ]
    },
    {
        sender: "scammer",
        text: "Вот мое удостоверение. Видите? Я настоящий сотрудник. Сейчас решается вопрос о блокировке вашего паспорта!",
        options: [
            {
                text: "Испугаться и выполнить требования",
                effect: { security: -50, trust: +40 },
                response: "🚨 Вы передали данные. Мошенники оформили на вас кредит...",
                nextStep: 5
            },
            {
                text: "Прекратить разговор и сообщить в полицию",
                effect: { security: +40, trust: -30 },
                response: "🛡 Вы сохранили данные и помогли бороться с мошенниками!",
                nextStep: 4
            }
        ]
    },
    {
        sender: "system",
        text: "На официальном сайте нет уведомлений о блокировке. Это явный признак мошенничества.",
        options: [
            {
                text: "Продолжить",
                effect: { security: +10, trust: 0 },
                response: "✅ Вы правильно идентифицировали угрозу!",
                nextStep: 4
            }
        ]
    },
    {
        sender: "system",
        text: "🎉 Поздравляем! Вы успешно распознали мошенников и защитили свои данные!",
        options: [
        
        ]
    },
    {
        sender: "system",
        text: "💥 Вы попались на удочку мошенников! Ваши данные и деньги в опасности.",
        options: [
            {
                text: "Узнать, где я ошибся",
                effect: { security: 0, trust: 100 },
                response: "Анализ ошибок... 1. Перешли по фишинговой ссылке 2. Поверили в срочность 3. Отдали код из SMS",
                nextStep: 6
            },
            {
                text: "Попробовать еще раз",
                effect: { security: 100, trust: 0 },
                response: "",
                nextStep: 0,
                restart: true
            }
        ]
    },
    {
        sender: "lesson",
        text: "📚 **Урок безопасности:**\n1. Официальный сайт Госуслуг только gosuslugi.ru\n2. Никогда не переходите по ссылкам из SMS\n3. Настоящие сотрудники не просят коды из SMS\n4. При сомнениях звоните 8-800-100-70-10",
        options: [
            {
                text: "Пройти тренажер еще раз",
                effect: { security: 100, trust: 0 },
                response: "",
                nextStep: 0,
                restart: true
            }
        ]
    }
];

// Инициализация тренажера (добавляем в window для глобального доступа)
window.initGosuslugiSimulator = function() {
    gosuslugiCurrentStep = 0;
    gosuslugiSecurityScore = 100;
    gosuslugiTrustScore = 0;
    gosuslugiSimulationFinished = false;
    
    // Очищаем предыдущие сообщения
    const chatMessages = document.getElementById('gosuslugi-chat-messages');
    if (chatMessages) chatMessages.innerHTML = '';
    
    // Очищаем предыдущие варианты
    const chatInput = document.getElementById('gosuslugi-chat-input');
    if (chatInput) chatInput.innerHTML = '';
    
    // Скрываем финальный результат
    const resultDiv = document.getElementById('gosuslugi-simulator-result');
    if (resultDiv) resultDiv.style.display = 'none';
    
    updateGosuslugiScores();
    showGosuslugiDialogueStep(gosuslugiCurrentStep);
};

// Показать шаг диалога
function showGosuslugiDialogueStep(stepIndex) {
    const chatMessages = document.getElementById('gosuslugi-chat-messages');
    const chatInput = document.getElementById('gosuslugi-chat-input');
    
    if (!chatMessages || !chatInput) {
        console.error('Не найдены элементы чата');
        return;
    }
    
    const dialogue = gosuslugiDialogueSteps[stepIndex];
    if (!dialogue) return;
    
    // Добавляем сообщение в чат
    const messageDiv = document.createElement('div');
    messageDiv.className = `message ${dialogue.sender}`;
    messageDiv.innerHTML = `<div class="message-text">${dialogue.text.replace(/\n/g, '<br>')}</div>`;
    chatMessages.appendChild(messageDiv);
    
    // Очищаем предыдущие варианты ответов
    chatInput.innerHTML = '';
    
    // Добавляем новые варианты ответов
    dialogue.options.forEach((option, index) => {
        const button = document.createElement('button');
        button.className = 'chat-option';
        button.textContent = option.text;
        button.onclick = () => selectGosuslugiDialogueOption(stepIndex, index);
        chatInput.appendChild(button);
    });
    
    // Прокручиваем чат вниз
    chatMessages.scrollTop = chatMessages.scrollHeight;
    
    // Если это финальный шаг
    if (dialogue.sender === 'system' && stepIndex >= 4) {
        showGosuslugiFinalResult(stepIndex === 5);
    }
}

// Обработка выбора варианта
function selectGosuslugiDialogueOption(stepIndex, optionIndex) {
    if (gosuslugiSimulationFinished) return;
    
    const dialogue = gosuslugiDialogueSteps[stepIndex];
    const option = dialogue.options[optionIndex];
    
    // Применяем эффекты
    gosuslugiSecurityScore = Math.max(0, Math.min(100, gosuslugiSecurityScore + option.effect.security));
    gosuslugiTrustScore = Math.max(0, Math.min(100, gosuslugiTrustScore + option.effect.trust));
    
    updateGosuslugiScores();
    
    // Показываем ответ на выбор
    if (option.response) {
        const chatMessages = document.getElementById('gosuslugi-chat-messages');
        const responseDiv = document.createElement('div');
        responseDiv.className = 'message user';
        responseDiv.innerHTML = `<div class="message-text"><strong>Вы:</strong> ${option.response}</div>`;
        chatMessages.appendChild(responseDiv);
        
        // Прокручиваем чат вниз
        chatMessages.scrollTop = chatMessages.scrollHeight;
    }
    
    // Переход к следующему шагу или рестарт
    setTimeout(() => {
        if (option.restart) {
            // Здесь вызываем инициализацию тренажера заново
            window.initGosuslugiSimulator();
        } else {
            showGosuslugiDialogueStep(option.nextStep);
        }
    }, 800);
}

// Обновление счетчиков
function updateGosuslugiScores() {
    const securityEl = document.getElementById('gosuslugi-security-score');
    const trustEl = document.getElementById('gosuslugi-trust-score');
    
    if (!securityEl || !trustEl) return;
    
    securityEl.textContent = gosuslugiSecurityScore + '%';
    trustEl.textContent = gosuslugiTrustScore + '%';
    
    // Динамическое изменение цвета
    securityEl.style.color = gosuslugiSecurityScore > 70 ? 'green' : gosuslugiSecurityScore > 30 ? 'orange' : 'red';
    trustEl.style.color = gosuslugiTrustScore > 70 ? 'red' : gosuslugiTrustScore > 30 ? 'orange' : 'green';
}

// Показать финальный результат
function showGosuslugiFinalResult(isFailure) {
    gosuslugiSimulationFinished = true;
    const resultDiv = document.getElementById('gosuslugi-simulator-result');
    
    if (!resultDiv) return;
    
    if (isFailure) {
        resultDiv.innerHTML = `
            <div class="result-failure">
                <h3>💥 Требуется обучение!</h3>
                <p>Вы стали жертвой мошенников. Изучите правила безопасности:</p>
                <ul>
                    <li>Официальный домен: <strong>gosuslugi.ru</strong></li>
                    <li>Никогда не переходите по ссылкам из SMS/email</li>
                    <li>Коды из SMS никому не сообщайте</li>
                    <li>При сомнениях звоните: 8-800-100-70-10</li>
                </ul>
            </div>
        `;
    } else {
        resultDiv.innerHTML = `
            <div class="result-success">
                <h3>🛡 Вы в безопасности!</h3>
                <p>Отличная цифровая грамотность! Вы правильно:</p>
                <ul>
                    <li>Распознали фишинговую ссылку</li>
                    <li>Не поддались давлению и срочности</li>
                    <li>Проверили информацию официальным путем</li>
                    <li>Сохранили конфиденциальные данные</li>
                </ul>
            </div>
        `;
    }
    resultDiv.style.display = 'block';
}

function startPhishingTest() {
    showNotification('info', 'Итоговый тест по фишингу скоро будет доступен');
    // Здесь можно добавить логику для полноценного теста
}
// Добавляем после функции startPhishingTest() новую функцию:
function startCallsTest() {
  // ПРОКРУТКА ВВЕРХ
    scrollToTop();
    // Показываем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // Загружаем тест
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon calls">
                <i class="fas fa-phone-alt"></i>
            </div>
            <div class="course-header-content">
                <h1>Итоговый тест: Телефонное мошенничество</h1>
                <p>Проверьте свои знания по пройденному материалу. 15 вопросов, для успешного прохождения нужно правильно ответить на 12 вопросов (80%).</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-question-circle"></i>
                        <span>15 вопросов</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>25 минут</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Проходной балл: 80%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="testContainer">
            <div id="testInstructions" style="text-align: center; padding: 40px 0;">
                <h3>Инструкция к тесту</h3>
                <p style="margin: 20px 0;">Тест состоит из 15 вопросов с одним правильным ответом.</p>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; max-width: 600px; margin: 0 auto;">
                    <h4><i class="fas fa-info-circle icon" style="color: #1976d2;"></i> Правила тестирования:</h4>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Выберите один вариант ответа на каждый вопрос</li>
                        <li>Нельзя вернуться к предыдущему вопросу</li>
                        <li>На прохождение теста отводится 25 минут</li>
                        <li>После завершения вы увидите детальный результат</li>
                        <li>Для получения сертификата нужно набрать ≥ 80%</li>
                    </ul>
                </div>
                
                <button class="btn btn-large btn-success" onclick="beginCallsTest()" style="margin-top: 30px;">
                    <i class="fas fa-play icon"></i> Начать тест
                </button>
                
                <button class="btn btn-large btn-outline" onclick="showPage('courses')" style="margin-top: 30px; margin-left: 15px;">
                    <i class="fas fa-arrow-left icon"></i> Вернуться к курсам
                </button>
            </div>
            
            <div id="testQuestions" style="display: none;">
                <!-- Вопросы будут загружены динамически -->
            </div>
            
            <div id="testResults" style="display: none;">
                <!-- Результаты будут загружены динамически -->
            </div>
        </div>
    `;
}

// Добавляем переменные для управления тестом
let callsTestQuestions = [];
let currentQuestionIndex = 0;
let userTestAnswers = [];
let testStartTime = null;
let testTimer = null;

// Функция для начала теста
function beginCallsTest() {
    // Инициализируем вопросы теста
    callsTestQuestions = [
        {
            question: "Что такое вишинг в контексте телефонного мошенничества?",
            options: [
                "Техническое обслуживание телефонных линий",
                "Телефонное мошенничество с использованием социальной инженерии",
                "Защита телефонных разговоров от прослушивания",
                "Официальные звонки от государственных органов"
            ],
            correctAnswer: 1,
            explanation: "Вишинг (vishing) — это телефонное мошенничество, при котором злоумышленники используют социальную инженерию для получения конфиденциальной информации."
        },
        {
            question: "Какой из этих признаков НЕ характерен для звонка мошенника?",
            options: [
                "Создание ощущения срочности и опасности",
                "Просьба назвать код из SMS-сообщения",
                "Предложение перезвонить по официальному номеру для проверки",
                "Требование немедленного перевода денег"
            ],
            correctAnswer: 2,
            explanation: "Мошенники никогда не предлагают перезвонить по официальному номеру — это лишит их возможности обмана. Они наоборот просят не вешать трубку и действовать немедленно."
        },
        {
            question: "Что делать, если вам звонят и представляются сотрудником банка, сообщая о подозрительных операциях?",
            options: [
                "Назвать данные карты для проверки",
                "Немедленно перевести деньги на 'безопасный счет'",
                "Вежливо завершить разговор и перезвонить в банк по номеру с карты",
                "Установить программу, которую рекомендует 'сотрудник банка'"
            ],
            correctAnswer: 2,
            explanation: "Единственно правильное действие — завершить разговор и самостоятельно перезвонить в банк по официальному номеру, указанному на обратной стороне карты."
        },
        {
            question: "Какой психологический прием чаще всего используют мошенники в телефонных разговорах?",
            options: [
                "Создание искусственной срочности",
                "Предложение подарков и бонусов",
                "Использование сложной технической терминологии",
                "Представление знаменитостью"
            ],
            correctAnswer: 0,
            explanation: "Создание искусственной срочности — основной прием. Мошенники говорят 'У вас есть только 5 минут', 'Деньги спишутся через 10 минут', чтобы жертва не успела подумать."
        },
        {
            question: "Что означает подмена номера (спуфинг) в контексте телефонного мошенничества?",
            options: [
                "Использование нескольких SIM-карт",
                "Звонки через интернет (VoIP)",
                "Отображение на вашем телефоне поддельного номера",
                "Звонки из-за границы"
            ],
            correctAnswer: 2,
            explanation: "Спуфинг — это технология, позволяющая мошенникам подделывать номер, с которого осуществляется звонок. На вашем телефоне может отображаться номер банка или госоргана, хотя звонок идет с мошеннического номера."
        },
        {
            question: "Какой из этих сценариев является классической схемой телефонного мошенничества 'родственник в беде'?",
            options: [
                "'Бабушка, я попал в аварию, нужны деньги на лечение'",
                "'Мама, у меня все хорошо, как твои дела?'",
                "'Это полиция, ваша дочь задержана за нарушение ПДД'",
                "'Это банк, ваш сын оформил кредит'"
            ],
            correctAnswer: 0,
            explanation: "Схема 'родственник в беде' строится на эмоциональном воздействии. Мошенник представляется внуком/внучкой, сообщает о чрезвычайной ситуации и просит срочно перевести деньги."
        },
        {
            question: "Что НЕЛЬЗЯ делать при получении подозрительного звонка?",
            options: [
                "Спросить номер служебного удостоверения",
                "Назвать свои паспортные данные для 'подтверждения личности'",
                "Предложить перезвонить на официальный номер организации",
                "Завершить разговор при давлении и угрозах"
            ],
            correctAnswer: 1,
            explanation: "Никогда нельзя называть паспортные данные, данные карт, коды из SMS и другую конфиденциальную информацию по телефону, особенно если звонок инициирован не вами."
        },
        {
            question: "Какой информации обычно НЕТ у мошенников при звонке, что может помочь их распознать?",
            options: [
                "Вашего имени и фамилии",
                "Номера вашей банковской карты",
                "Номера вашего телефона",
                "Адреса регистрации"
            ],
            correctAnswer: 1,
            explanation: "Мошенники часто знают ваше имя, телефон и даже адрес (из утечек данных), но номер банковской карты им обычно неизвестен. Они будут пытаться его выведать под разными предлогами."
        },
        {
            question: "Что такое ПУУ-схема в телефонном мошенничестве?",
            options: [
                "Продажа несуществующих услуг",
                "Получение удаленного доступа к компьютеру жертвы",
                "Оформление кредита на чужое имя",
                "Сбор средств на благотворительность"
            ],
            correctAnswer: 1,
            explanation: "ПУУ (Программа Удаленного Управления) — схема, при которой мошенники под видом техподдержки заставляют установить программу удаленного доступа (AnyDesk, TeamViewer), получая контроль над компьютером жертвы."
        },
        {
            question: "Куда следует обращаться, если вы стали жертвой телефонных мошенников?",
            options: [
                "Только в банк для блокировки карты",
                "В полицию с заявлением о мошенничестве",
                "Никуда, так как деньги уже не вернуть",
                "К оператору связи для смены номера"
            ],
            correctAnswer: 1,
            explanation: "Необходимо обратиться в полицию с заявлением о мошенничестве, а также сообщить в банк для блокировки карты. Даже если деньги сразу не вернут, заявление поможет в расследовании."
        },
        {
            question: "Какой из этих номеров является мошенническим, если звонящий представляется службой безопасности Сбербанка?",
            options: [
                "+7 495 500-55-50 (официальный номер Сбербанка)",
                "+7 900 123-45-67 (мобильный номер)",
                "8-800-555-55-50 (бесплатный номер Сбербанка)",
                "8-495-500-00-00 (городской номер)"
            ],
            correctAnswer: 1,
            explanation: "Служба безопасности банка никогда не звонит с мобильных номеров. Все официальные звонки осуществляются с городских или бесплатных номеров, указанных на официальном сайте банка."
        },
        {
            question: "Что лучше всего сделать для защиты пожилых родственников от телефонных мошенников?",
            options: [
                "Запретить им пользоваться телефоном",
                "Установить на их телефон антиспам приложение",
                "Ничего не говорить, чтобы не пугать",
                "Разрешить общаться только с известными номерами"
            ],
            correctAnswer: 1,
            explanation: "Установка антиспам приложения (Яндекс.Телефон, 'Кто звонит?') поможет определять мошеннические номера. Также важно обучить родственников основным правилам безопасности."
        },
        {
            question: "Какой признак точно указывает на мошеннический звонок?",
            options: [
                "Звонок в нерабочее время",
                "Просьба не рассказывать о звонке никому",
                "Акцент у звонящего",
                "Фоновый шум при разговоре"
            ],
            correctAnswer: 1,
            explanation: "Просьба сохранить разговор в тайне — явный признак мошенничества. Настоящие сотрудники банков или госорганов никогда не просят скрывать факт общения."
        },
        {
            question: "Что означает фраза 'техподдержка Windows обнаружила вирусы на вашем компьютере'?",
            options: [
                "Легитимный звонок от Microsoft",
                "Мошенническая схема для получения удаленного доступа",
                "Автоматическое предупреждение системы",
                "Реклама антивирусного ПО"
            ],
            correctAnswer: 1,
            explanation: "Это классическая ПУУ-схема. Microsoft никогда не звонит пользователям с подобными предупреждениями. Цель мошенников — заставить установить программу удаленного доступа."
        },
        {
            question: "Какой из этих советов НЕПРАВИЛЬНЫЙ для защиты от телефонного мошенничества?",
            options: [
                "Всегда перезванивайте по официальным номерам",
                "Установите PIN-код на SIM-карту",
                "Сообщайте все подозрительные звонки в банк",
                "Для проверки называйте часть данных карты"
            ],
            correctAnswer: 3,
            explanation: "Никогда нельзя называть даже часть данных карты. Мошенникам иногда достаточно первых 6 или последних 4 цифр. Всегда перезванивайте по официальным номерам для проверки."
        }
    ];
    
    // Сбрасываем данные теста
    currentQuestionIndex = 0;
    userTestAnswers = [];
    testStartTime = new Date();
    
    // Скрываем инструкции и показываем вопросы
    document.getElementById('testInstructions').style.display = 'none';
    document.getElementById('testQuestions').style.display = 'block';
    
    // Запускаем таймер
    startTestTimer();
    
    // Загружаем первый вопрос
    loadTestQuestion();
}

// Функция для загрузки вопроса
function loadTestQuestion() {
    const testQuestionsDiv = document.getElementById('testQuestions');
    const question = callsTestQuestions[currentQuestionIndex];
    
    testQuestionsDiv.innerHTML = `
        <div class="simulator">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h3>Вопрос ${currentQuestionIndex + 1} из ${callsTestQuestions.length}</h3>
                <div id="testTimer" style="background-color: #f5f5f5; padding: 8px 15px; border-radius: 20px; font-weight: bold;">
                    <i class="fas fa-clock icon"></i> <span id="timeRemaining">25:00</span>
                </div>
            </div>
            
            <div style="background-color: #f8f9fa; padding: 25px; border-radius: 10px; margin-bottom: 25px;">
                <h4 style="color: #1a237e; margin-bottom: 15px;">${question.question}</h4>
            </div>
            
            <div class="options">
                ${question.options.map((option, index) => `
                    <div class="option" onclick="selectTestAnswer(${index})">
                        ${String.fromCharCode(65 + index)}. ${option}
                    </div>
                `).join('')}
            </div>
            
            <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 30px;">
    ${currentQuestionIndex > 0 ? `
        <button class="btn btn-outline" onclick="prevTestQuestion()" style="padding: 8px 20px;">
            <i class="fas fa-arrow-left icon"></i> Назад
        </button>
    ` : '<div style="width: 100px;"></div>'}
    
    <div style="text-align: center;">
        <button class="btn btn-success" onclick="nextTestQuestion()" id="nextButton" 
                ${userTestAnswers[currentQuestionIndex] === undefined ? 'disabled' : ''}
                style="padding: 8px 25px;">
            ${currentQuestionIndex === callsTestQuestions.length - 1 ? 'Завершить тест' : 'Следующий вопрос'} 
            <i class="fas fa-arrow-right icon"></i>
        </button>
        <p style="margin-top: 8px; color: #666; font-size: 0.85rem;">
            Вопрос ${currentQuestionIndex + 1} из ${callsTestQuestions.length}
        </p>
    </div>
    
    <div style="text-align: right;">
        <button class="btn btn-danger" onclick="cancelTest()" style="padding: 8px 20px;">
            <i class="fas fa-times icon"></i> Отменить
        </button>
    </div>
</div>
            
            <div style="margin-top: 20px; text-align: center; color: #666;">
                <p><i class="fas fa-info-circle icon"></i> Выберите один вариант ответа</p>
            </div>
        </div>
    `;
}

// Функция выбора ответа
function selectTestAnswer(answerIndex) {
    // Убираем выделение со всех вариантов
    document.querySelectorAll('#testQuestions .option').forEach(option => {
        option.classList.remove('selected');
    });
    
    // Выделяем выбранный вариант
    event.target.classList.add('selected');
    
    // Сохраняем ответ
    userTestAnswers[currentQuestionIndex] = answerIndex;
    
    // Активируем кнопку "Далее"
    document.getElementById('nextButton').disabled = false;
}

// Функция для перехода к следующему вопросу
function nextTestQuestion() {
    // Проверяем, выбран ли ответ
    if (userTestAnswers[currentQuestionIndex] === undefined) {
        showNotification('error', 'Пожалуйста, выберите вариант ответа');
        return;
    }
    
    // Переходим к следующему вопросу или завершаем тест
    if (currentQuestionIndex < callsTestQuestions.length - 1) {
        currentQuestionIndex++;
        loadTestQuestion();
    } else {
        finishTest();
    }
}

// Функция для возврата к предыдущему вопросу
function prevTestQuestion() {
    if (currentQuestionIndex > 0) {
        currentQuestionIndex--;
        loadTestQuestion();
    }
}

// Функция запуска таймера теста
function startTestTimer() {
    let timeLeft = 25 * 60; // 25 минут в секундах
    
    testTimer = setInterval(function() {
        timeLeft--;
        
        const minutes = Math.floor(timeLeft / 60);
        const seconds = timeLeft % 60;
        
        document.getElementById('timeRemaining').textContent = 
            `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        
        // Меняем цвет при малом остатке времени
        if (timeLeft < 300) { // Меньше 5 минут
            document.getElementById('testTimer').style.backgroundColor = '#ffebee';
            document.getElementById('testTimer').style.color = '#d32f2f';
        }
        
        if (timeLeft <= 0) {
            clearInterval(testTimer);
            finishTest();
        }
    }, 1000);
}

// Функция завершения теста
function finishTest() {
    clearInterval(testTimer);
    
    // Рассчитываем результаты
    let correctAnswers = 0;
    let resultsHTML = '';
    
    callsTestQuestions.forEach((question, index) => {
        const userAnswer = userTestAnswers[index];
        const isCorrect = userAnswer === question.correctAnswer;
        
        if (isCorrect) correctAnswers++;
        
        resultsHTML += `
            <div style="margin-bottom: 20px; padding: 15px; border-radius: 8px; background-color: ${isCorrect ? '#e8f5e9' : '#ffebee'}; border-left: 5px solid ${isCorrect ? '#388e3c' : '#d32f2f'};">
                <p><strong>Вопрос ${index + 1}:</strong> ${question.question}</p>
                <p><strong>Ваш ответ:</strong> ${userAnswer !== undefined ? question.options[userAnswer] : 'Не ответили'}</p>
                <p><strong>Правильный ответ:</strong> ${question.options[question.correctAnswer]}</p>
                <p style="margin-top: 10px; color: #666;"><i class="fas fa-info-circle icon"></i> ${question.explanation}</p>
            </div>
        `;
    });
    
    const score = Math.round((correctAnswers / callsTestQuestions.length) * 100);
    const isPassed = score >= 80;
    
    // Обновляем прогресс пользователя
    if (currentUser && isPassed) {
        // Отмечаем тест как пройденный
        if (!currentUser.completedCourses) currentUser.completedCourses = [];
        if (!currentUser.completedCourses.includes('calls')) {
            currentUser.completedCourses.push('calls');
        }
        
        // Обновляем прогресс курса
        currentUser.progress.calls = 100;
        currentUser.stats.completedLessons++;
        currentUser.stats.score += 50; // Бонус за прохождение теста
        currentUser.stats.testResults.push({
            course: 'calls',
            score: score,
            date: new Date().toISOString()
        });
        
        updateUserInStorage();
    }
    
    // Показываем результаты
    document.getElementById('testQuestions').style.display = 'none';
    document.getElementById('testResults').style.display = 'block';
    document.getElementById('testResults').innerHTML = `
        <div class="simulator" style="text-align: center;">
            <h3>Результаты теста</h3>
            
            <div style="margin: 30px 0;">
                <div style="font-size: 3rem; color: ${isPassed ? '#388e3c' : '#d32f2f'}; margin-bottom: 10px;">
                    ${score}%
                </div>
                <div style="font-size: 1.2rem; margin-bottom: 20px;">
                    ${correctAnswers} из ${callsTestQuestions.length} правильных ответов
                </div>
                
                <div style="background-color: ${isPassed ? '#e8f5e9' : '#ffebee'}; padding: 20px; border-radius: 10px; max-width: 500px; margin: 0 auto;">
                    <h4 style="color: ${isPassed ? '#388e3c' : '#d32f2f'};">
                        <i class="fas ${isPassed ? 'fa-check-circle' : 'fa-times-circle'} icon"></i>
                        ${isPassed ? 'Тест пройден успешно!' : 'Тест не пройден'}
                    </h4>
                    <p>Для успешного прохождения необходимо набрать 80% правильных ответов.</p>
                </div>
            </div>
            
            ${isPassed ? `
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-trophy icon" style="color: #ff9800;"></i> Поздравляем!</h4>
                    <p>Вы успешно прошли курс "Телефонное мошенничество" и получили +50 очков к вашему рейтингу.</p>
                    ${currentUser ? `
                        <p style="margin-top: 10px;">Ваш текущий счет: <strong>${currentUser.stats.score} очков</strong></p>
                    ` : ''}
                </div>
            ` : `
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-redo icon" style="color: #1976d2;"></i> Рекомендации</h4>
                    <p>Рекомендуем повторить материал курса и пройти тест снова.</p>
                    <p>Обратите особое внимание на вопросы, в которых допустили ошибки.</p>
                </div>
            `}
            
            <h4 style="margin-top: 30px; margin-bottom: 20px;">Детализация ответов:</h4>
            <div style="max-height: 400px; overflow-y: auto; padding-right: 10px;">
                ${resultsHTML}
            </div>
            
            <div style="margin-top: 30px;">
                <button class="btn btn-large ${isPassed ? 'btn-success' : 'btn-warning'}" onclick="${isPassed ? 'showPage(\'courses\')' : 'retryTest()'}">
                    ${isPassed ? 'Вернуться к курсам' : 'Попробовать снова'}
                </button>
                
                ${isPassed ? `
                    <button class="btn btn-large btn-outline" onclick="downloadCertificate()" style="margin-left: 15px;">
                        <i class="fas fa-download icon"></i> Скачать сертификат
                    </button>
                ` : ''}
            </div>
        </div>
    `;
    
    // Прокручиваем к результатам
    document.getElementById('testResults').scrollIntoView({ behavior: 'smooth' });
}

// Функция повторного прохождения теста
function retryTest() {
    currentQuestionIndex = 0;
    userTestAnswers = [];
    
    document.getElementById('testResults').style.display = 'none';
    document.getElementById('testQuestions').style.display = 'block';
    
    testStartTime = new Date();
    startTestTimer();
    loadTestQuestion();
}

// Функция отмены теста
function cancelTest() {
    if (confirm('Вы уверены, что хотите отменить тест? Все ответы будут потеряны.')) {
        clearInterval(testTimer);
        showPage('courses');
    }
}

// Функция "скачивания" сертификата (демо-версия)
function downloadCertificate() {
    showNotification('success', 'Сертификат успешно сгенерирован! В полной версии здесь будет ссылка для скачивания.');
    
    // В реальном приложении здесь была бы генерация PDF
    const certificateContent = `
        <div style="text-align: center; padding: 40px; background-color: white; border: 10px solid #1a237e; max-width: 800px; margin: 0 auto;">
            <h1 style="color: #1a237e;">СЕРТИФИКАТ</h1>
            <p style="font-size: 1.2rem;">Настоящий сертификат подтверждает, что</p>
            <h2 style="color: #3949ab; margin: 20px 0;">${currentUser ? currentUser.name : 'Студент'}</h2>
            <p style="font-size: 1.2rem;">успешно прошел(а) курс</p>
            <h3 style="color: #1a237e; margin: 20px 0;">"Телефонное мошенничество"</h3>
            <p>в Академии Кибербезопасности</p>
            <div style="margin: 30px 0;">
                <p>Дата: ${new Date().toLocaleDateString('ru-RU')}</p>
                <p>Результат теста: ${Math.round((userTestAnswers.filter((answer, index) => answer === callsTestQuestions[index].correctAnswer).length / callsTestQuestions.length) * 100)}%</p>
            </div>
            <div style="margin-top: 50px;">
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Директор Академии</p>
                    <p>___________________</p>
                </div>
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Руководитель курса</p>
                    <p>___________________</p>
                </div>
            </div>
        </div>
    `;
    
    // В реальном приложении здесь был бы код для генерации PDF
    // Для демо просто покажем уведомление
    setTimeout(() => {
        if (confirm('Хотите увидеть предварительный просмотр сертификата?')) {
            const win = window.open();
            win.document.write(certificateContent);
            win.document.title = 'Сертификат - Телефонное мошенничество';
        }
    }, 500);
}
// Глобальные переменные для теста по фишингу
let phishingTestQuestions = [];
let phishingCurrentQuestion = 0;
let phishingUserAnswers = [];
let phishingTestStartTime = null;
let phishingTestTimer = null;

// Функция запуска теста по фишингу
function startPhishingTest() {
   // ПРОКРУТКА ВВЕРХ
    scrollToTop();
    // Показываем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // Инициализируем вопросы теста
    phishingTestQuestions = [
        {
            question: "Что такое фишинг в кибербезопасности?",
            options: [
                "Вид компьютерного вируса",
                "Мошенническая техника для получения конфиденциальной информации",
                "Способ взлома паролей",
                "Тип шифрования данных"
            ],
            correctAnswer: 1,
            explanation: "Фишинг — это мошенническая техника, при которой злоумышленники выдают себя за доверенные организации, чтобы заставить жертву раскрыть конфиденциальную информацию (пароли, данные карт и т.д.)."
        },
        {
            question: "Какой из этих адресов электронной почты наиболее подозрителен?",
            options: [
                "security@vtb.ru",
                "vtb-security@secure-vtb.ru",
                "support@service.vtb.ru",
                "noreply@mail.vtb.ru"
            ],
            correctAnswer: 1,
            explanation: "Домены с дополнительными словами перед названием компании (secure-vtb.ru) часто используются мошенниками. Официальные адреса обычно используют корпоративный домен компании."
        },
        {
            question: "Что нужно проверить в первую очередь при получении письма о 'блокировке аккаунта'?",
            options: [
                "Нажать на ссылку в письме для проверки",
                "Связаться с отправителем по указанному телефону",
                "Вручную ввести адрес сайта в браузере",
                "Ответить на письмо с запросом деталей"
            ],
            correctAnswer: 2,
            explanation: "Никогда не переходите по ссылкам из подозрительных писем. Всегда вводите адрес сайта вручную в браузере, чтобы убедиться, что вы на официальном ресурсе."
        },
        {
            question: "Какой признак НЕ характерен для фишингового сайта?",
            options: [
                "Орфографические ошибки в тексте",
                "Отсутствие HTTPS соединения",
                "Официальный логотип компании",
                "Странный или длинный URL-адрес"
            ],
            correctAnswer: 2,
            explanation: "Наличие официального логотипа не гарантирует легитимность сайта — мошенники часто копируют логотипы. Остальные признаки являются типичными индикаторами фишинга."
        },
        {
            question: "Что означает зелёный замок в адресной строке браузера?",
            options: [
                "Сайт абсолютно безопасен",
                "Соединение зашифровано",
                "Сайт проверен на вирусы",
                "Компания имеет сертификат качества"
            ],
            correctAnswer: 1,
            explanation: "Зелёный замок означает, что соединение между вашим браузером и сайтом зашифровано с помощью SSL/TLS, но не гарантирует, что сайт не является фишинговым."
        },
        {
            question: "Какой тип фишинга использует телефонные звонки?",
            options: [
                "Смишинг (SMS-фишинг)",
                "Вишинг (голосовой фишинг)",
                "Квишинг (QR-фишинг)",
                "Фарминг (DNS-фишинг)"
            ],
            correctAnswer: 1,
            explanation: "Вишинг (vishing) — это голосовой фишинг, когда мошенники звонят жертвам, представляясь сотрудниками банков или других организаций, чтобы выманить конфиденциальную информацию."
        },
        {
            question: "Что делать при получении SMS с просьбой перейти по ссылке для 'получения выигрыша'?",
            options: [
                "Перейти по ссылке из интереса",
                "Удалить SMS",
                "Сообщить о спаме оператору связи",
                "Переслать друзьям"
            ],
            correctAnswer: 2,
            explanation: "Самый безопасный вариант — не взаимодействовать с подозрительными SMS. Сообщение оператору связи помогает бороться с распространением спама и фишинга."
        },
        {
            question: "Какой из этих паролей наиболее уязвим для фишинговых атак?",
            options: [
                "P@ssw0rd123!",
                "Кот_в_сапогах_2024",
                "J8#kL!p2qW9*zM5",
                "correct-horse-battery-staple"
            ],
            correctAnswer: 0,
            explanation: "Простой пароль 'P@ssw0rd123!' уязвим, но важнее использовать уникальные пароли для каждого сайта. Даже сложный пароль, использованный на фишинговом сайте, будет скомпрометирован."
        },
        {
            question: "Что такое двухфакторная аутентификация (2FA) и как она защищает от фишинга?",
            options: [
                "Два пароля вместо одного",
                "Вход с двух устройств одновременно",
                "Дополнительный код после пароля",
                "Биометрическая идентификация"
            ],
            correctAnswer: 2,
            explanation: "2FA требует ввода дополнительного кода (из приложения или SMS) после пароля. Даже если мошенники получат ваш пароль через фишинговый сайт, без второго фактора они не смогут войти в аккаунт."
        },
        {
            question: "Какой инструмент НЕ помогает защититься от фишинга?",
            options: [
                "Антивирусное ПО",
                "Браузерные расширения для проверки ссылок",
                "Менеджер паролей",
                "Автозаполнение форм в браузере"
            ],
            correctAnswer: 3,
            explanation: "Автозаполнение форм может быть опасным, так как может автоматически ввести ваши данные на фишинговом сайте. Все остальные инструменты помогают в защите от фишинга."
        }
    ];
    
    // Сбрасываем данные теста
    phishingCurrentQuestion = 0;
    phishingUserAnswers = [];
    phishingTestStartTime = new Date();
    
    // Загружаем страницу теста
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon phishing">
                <i class="fas fa-fish"></i>
            </div>
            <div class="course-header-content">
                <h1>Итоговый тест: Фишинг и социальная инженерия</h1>
                <p>Проверьте свои знания по пройденному материалу. 10 вопросов, для успешного прохождения нужно правильно ответить на 7 вопросов (70%).</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-question-circle"></i>
                        <span>10 вопросов</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>15 минут</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Проходной балл: 70%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="phishingTestContainer">
            <div id="phishingTestInstructions" style="text-align: center; padding: 40px 0;">
                <h3>Инструкция к тесту</h3>
                <p style="margin: 20px 0;">Тест состоит из 10 вопросов с одним правильным ответом.</p>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; max-width: 600px; margin: 0 auto;">
                    <h4><i class="fas fa-info-circle icon" style="color: #ff5722;"></i> Правила тестирования:</h4>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Выберите один вариант ответа на каждый вопрос</li>
                        <li>Можно вернуться к предыдущим вопросам</li>
                        <li>На прохождение теста отводится 15 минут</li>
                        <li>После завершения вы увидите детальный результат</li>
                        <li>Для успешного прохождения нужно ≥ 70% правильных ответов (7 из 10)</li>
                    </ul>
                </div>
                
                <button class="btn btn-large btn-success" onclick="beginPhishingTest()" style="margin-top: 30px;">
                    <i class="fas fa-play icon"></i> Начать тест
                </button>
                
                <button class="btn btn-large btn-outline" onclick="goBackToCourse()" style="margin-top: 30px; margin-left: 15px;">
                    <i class="fas fa-arrow-left icon"></i> Вернуться к курсу
                </button>
            </div>
            
            <div id="phishingTestQuestions" style="display: none;">
                <!-- Вопросы будут загружены динамически -->
            </div>
            
            <div id="phishingTestResults" style="display: none;">
                <!-- Результаты будут загружены динамически -->
            </div>
        </div>
    `;
}

// Функция возврата к курсу
function goBackToCourse() {
    // Восстанавливаем курс по фишингу
    const currentCourse = 'phishing';
    if (courses[currentCourse]) {
        loadCourseContent(currentCourse);
        
        // Устанавливаем последний урок как активный
        currentCourseData = courses[currentCourse];
        currentLessonIndex = currentCourseData.lessons.length - 1; // Последний урок (итоговый тест)
        showLesson(currentCourseData.lessons[currentLessonIndex]);
    }
}

// Функция для начала теста
function beginPhishingTest() {
    // Скрываем инструкции и показываем вопросы
    document.getElementById('phishingTestInstructions').style.display = 'none';
    document.getElementById('phishingTestQuestions').style.display = 'block';
    
    // Запускаем таймер
    startPhishingTestTimer();
    
    // Загружаем первый вопрос
    loadPhishingTestQuestion();
}

// Функция для загрузки вопроса
function loadPhishingTestQuestion() {
    const testQuestionsDiv = document.getElementById('phishingTestQuestions');
    const question = phishingTestQuestions[phishingCurrentQuestion];
    
    testQuestionsDiv.innerHTML = `
        <div class="simulator">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h3>Вопрос ${phishingCurrentQuestion + 1} из ${phishingTestQuestions.length}</h3>
                <div id="phishingTestTimer" style="background-color: #f5f5f5; padding: 8px 15px; border-radius: 20px; font-weight: bold;">
                    <i class="fas fa-clock icon"></i> <span id="phishingTimeRemaining">15:00</span>
                </div>
            </div>
            
            <div style="background-color: #f8f9fa; padding: 25px; border-radius: 10px; margin-bottom: 25px;">
                <h4 style="color: #ff5722; margin-bottom: 15px;">${question.question}</h4>
            </div>
            
            <div class="options">
                ${question.options.map((option, index) => `
                    <div class="option" onclick="selectPhishingTestAnswer(${index})" 
                         style="${phishingUserAnswers[phishingCurrentQuestion] === index ? 'border-color: #ff5722; background-color: #ffecb3;' : ''}">
                        ${String.fromCharCode(65 + index)}. ${option}
                    </div>
                `).join('')}
            </div>
            
            <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 30px;">
    ${phishingCurrentQuestion > 0 ? `
        <button class="btn btn-outline" onclick="prevPhishingTestQuestion()" style="padding: 8px 20px;">
            <i class="fas fa-arrow-left icon"></i> Назад
        </button>
    ` : '<div style="width: 100px;"></div>'}
    
    <div style="text-align: center;">
        <button class="btn btn-success" onclick="nextPhishingTestQuestion()" id="phishingNextButton" 
                ${phishingUserAnswers[phishingCurrentQuestion] === undefined ? 'disabled' : ''}
                style="padding: 8px 25px;">
            ${phishingCurrentQuestion === phishingTestQuestions.length - 1 ? 'Завершить тест' : 'Следующий вопрос'} 
            <i class="fas fa-arrow-right icon"></i>
        </button>
        <p style="margin-top: 8px; color: #666; font-size: 0.85rem;">
            Вопрос ${phishingCurrentQuestion + 1} из ${phishingTestQuestions.length}
        </p>
    </div>
    
    <div style="text-align: right;">
        <button class="btn btn-danger" onclick="cancelPhishingTest()" style="padding: 8px 20px;">
            <i class="fas fa-times icon"></i> Отменить
        </button>
    </div>
</div>
            
            <div style="margin-top: 20px; text-align: center; color: #666;">
                <p><i class="fas fa-info-circle icon"></i> Выберите один вариант ответа</p>
            </div>
        </div>
    `;
}

// Функция выбора ответа
function selectPhishingTestAnswer(answerIndex) {
    // Убираем выделение со всех вариантов
    document.querySelectorAll('#phishingTestQuestions .option').forEach(option => {
        option.style.borderColor = '#ddd';
        option.style.backgroundColor = 'white';
    });
    
    // Выделяем выбранный вариант
    event.target.style.borderColor = '#ff5722';
    event.target.style.backgroundColor = '#ffecb3';
    
    // Сохраняем ответ
    phishingUserAnswers[phishingCurrentQuestion] = answerIndex;
    
    // Активируем кнопку "Далее"
    document.getElementById('phishingNextButton').disabled = false;
}

// Функция для перехода к следующему вопросу
function nextPhishingTestQuestion() {
    // Проверяем, выбран ли ответ
    if (phishingUserAnswers[phishingCurrentQuestion] === undefined) {
        showNotification('error', 'Пожалуйста, выберите вариант ответа');
        return;
    }
    
    // Переходим к следующему вопросу или завершаем тест
    if (phishingCurrentQuestion < phishingTestQuestions.length - 1) {
        phishingCurrentQuestion++;
        loadPhishingTestQuestion();
    } else {
        finishPhishingTest();
    }
}

// Функция для возврата к предыдущему вопросу
function prevPhishingTestQuestion() {
    if (phishingCurrentQuestion > 0) {
        phishingCurrentQuestion--;
        loadPhishingTestQuestion();
    }
}

// Функция запуска таймера теста
function startPhishingTestTimer() {
    let timeLeft = 15 * 60; // 15 минут в секундах
    
    phishingTestTimer = setInterval(function() {
        timeLeft--;
        
        const minutes = Math.floor(timeLeft / 60);
        const seconds = timeLeft % 60;
        
        document.getElementById('phishingTimeRemaining').textContent = 
            `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        
        // Меняем цвет при малом остатке времени
        if (timeLeft < 180) { // Меньше 3 минут
            document.getElementById('phishingTestTimer').style.backgroundColor = '#ffebee';
            document.getElementById('phishingTestTimer').style.color = '#d32f2f';
        }
        
        if (timeLeft <= 0) {
            clearInterval(phishingTestTimer);
            finishPhishingTest();
        }
    }, 1000);
}

// Функция завершения теста
function finishPhishingTest() {
    clearInterval(phishingTestTimer);
    
    // Рассчитываем результаты
    let correctAnswers = 0;
    let resultsHTML = '';
    
    phishingTestQuestions.forEach((question, index) => {
        const userAnswer = phishingUserAnswers[index];
        const isCorrect = userAnswer === question.correctAnswer;
        
        if (isCorrect) correctAnswers++;
        
        resultsHTML += `
            <div style="margin-bottom: 20px; padding: 15px; border-radius: 8px; background-color: ${isCorrect ? '#e8f5e9' : '#ffebee'}; border-left: 5px solid ${isCorrect ? '#388e3c' : '#d32f2f'};">
                <p><strong>Вопрос ${index + 1}:</strong> ${question.question}</p>
                <p><strong>Ваш ответ:</strong> ${userAnswer !== undefined ? question.options[userAnswer] : 'Не ответили'}</p>
                <p><strong>Правильный ответ:</strong> ${question.options[question.correctAnswer]}</p>
                <p style="margin-top: 10px; color: #666;"><i class="fas fa-info-circle icon"></i> ${question.explanation}</p>
            </div>
        `;
    });
    
    const score = Math.round((correctAnswers / phishingTestQuestions.length) * 100);
    const isPassed = score >= 70;
    
    // Обновляем прогресс пользователя
    if (currentUser && isPassed) {
        // Отмечаем тест как пройденный
        if (!currentUser.completedCourses) currentUser.completedCourses = [];
        if (!currentUser.completedCourses.includes('phishing')) {
            currentUser.completedCourses.push('phishing');
        }
        
        // Обновляем прогресс курса
        if (!currentUser.progress) currentUser.progress = {};
        currentUser.progress.phishing = 100;
        
        // Отмечаем последний урок как пройденный
        if (courses.phishing && courses.phishing.lessons) {
            const lastLessonIndex = courses.phishing.lessons.length - 1;
            if (lastLessonIndex >= 0) {
                courses.phishing.lessons[lastLessonIndex].completed = true;
            }
        }
        
        if (!currentUser.stats) currentUser.stats = {
            completedLessons: 0,
            score: 0,
            testResults: []
        };
        
        currentUser.stats.completedLessons++;
        currentUser.stats.score += 50; // Бонус за прохождение теста
        currentUser.stats.testResults.push({
            course: 'phishing',
            score: score,
            date: new Date().toISOString()
        });
        
        updateUserInStorage();
    }
    
    // Показываем результаты
    document.getElementById('phishingTestQuestions').style.display = 'none';
    document.getElementById('phishingTestResults').style.display = 'block';
    document.getElementById('phishingTestResults').innerHTML = `
        <div class="simulator" style="text-align: center;">
            <h3>Результаты теста</h3>
            
            <div style="margin: 30px 0;">
                <div style="font-size: 3rem; color: ${isPassed ? '#388e3c' : '#d32f2f'}; margin-bottom: 10px;">
                    ${score}%
                </div>
                <div style="font-size: 1.2rem; margin-bottom: 20px;">
                    ${correctAnswers} из ${phishingTestQuestions.length} правильных ответов
                </div>
                
                <div style="background-color: ${isPassed ? '#e8f5e9' : '#ffebee'}; padding: 20px; border-radius: 10px; max-width: 500px; margin: 0 auto;">
                    <h4 style="color: ${isPassed ? '#388e3c' : '#d32f2f'};">
                        <i class="fas ${isPassed ? 'fa-check-circle' : 'fa-times-circle'} icon"></i>
                        ${isPassed ? 'Тест пройден успешно!' : 'Тест не пройден'}
                    </h4>
                    <p>Для успешного прохождения необходимо набрать 70% правильных ответов (7 из 10).</p>
                </div>
            </div>
            
            ${isPassed ? `
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-trophy icon" style="color: #ff9800;"></i> Поздравляем!</h4>
                    <p>Вы успешно прошли курс "Фишинг и социальная инженерия" и получили +50 очков к вашему рейтингу.</p>
                    ${currentUser ? `
                        <p style="margin-top: 10px;">Ваш текущий счет: <strong>${currentUser.stats.score} очков</strong></p>
                    ` : ''}
                </div>
            ` : `
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-redo icon" style="color: #1976d2;"></i> Рекомендации</h4>
                    <p>Рекомендуем повторить материал курса и пройти тест снова.</p>
                    <p>Обратите особое внимание на вопросы, в которых допустили ошибки.</p>
                </div>
            `}
            
            <h4 style="margin-top: 30px; margin-bottom: 20px;">Детализация ответов:</h4>
            <div style="max-height: 400px; overflow-y: auto; padding-right: 10px;">
                ${resultsHTML}
            </div>
            
            <div style="margin-top: 30px;">
                ${isPassed ? `
                    <button class="btn btn-large btn-success" onclick="showPage('courses')">
                        <i class="fas fa-home icon"></i> Вернуться к курсам
                    </button>
                    <button class="btn btn-large btn-outline" onclick="downloadPhishingCertificate()" style="margin-left: 15px;">
                        <i class="fas fa-download icon"></i> Скачать сертификат
                    </button>
                ` : `
                    <button class="btn btn-large btn-warning" onclick="retryPhishingTest()">
                        <i class="fas fa-redo icon"></i> Попробовать снова
                    </button>
                    <button class="btn btn-large btn-outline" onclick="goBackToCourse()" style="margin-left: 15px;">
                        <i class="fas fa-arrow-left icon"></i> Вернуться к курсу
                    </button>
                `}
            </div>
        </div>
    `;
    
    // Прокручиваем к результатам
    document.getElementById('phishingTestResults').scrollIntoView({ behavior: 'smooth' });
}

// Функция повторного прохождения теста
function retryPhishingTest() {
    phishingCurrentQuestion = 0;
    phishingUserAnswers = [];
    
    document.getElementById('phishingTestResults').style.display = 'none';
    document.getElementById('phishingTestQuestions').style.display = 'block';
    
    phishingTestStartTime = new Date();
    startPhishingTestTimer();
    loadPhishingTestQuestion();
}

// Функция отмены теста
function cancelPhishingTest() {
    if (confirm('Вы уверены, что хотите отменить тест? Все ответы будут потеряны.')) {
        clearInterval(phishingTestTimer);
        goBackToCourse();
    }
}

// Функция "скачивания" сертификата
function downloadPhishingCertificate() {
    showNotification('success', 'Сертификат успешно сгенерирован! В полной версии здесь будет ссылка для скачивания.');
    
    const certificateContent = `
        <div style="text-align: center; padding: 40px; background-color: white; border: 10px solid #ff5722; max-width: 800px; margin: 0 auto;">
            <h1 style="color: #ff5722;">СЕРТИФИКАТ</h1>
            <p style="font-size: 1.2rem;">Настоящий сертификат подтверждает, что</p>
            <h2 style="color: #d84315; margin: 20px 0;">${currentUser ? currentUser.name : 'Студент'}</h2>
            <p style="font-size: 1.2rem;">успешно прошел(а) курс</p>
            <h3 style="color: #ff5722; margin: 20px 0;">"Фишинг и социальная инженерия"</h3>
            <p>в Академии Кибербезопасности</p>
            <div style="margin: 30px 0;">
                <p>Дата: ${new Date().toLocaleDateString('ru-RU')}</p>
                <p>Результат теста: ${Math.round((phishingUserAnswers.filter((answer, index) => answer === phishingTestQuestions[index].correctAnswer).length / phishingTestQuestions.length) * 100)}%</p>
            </div>
            <div style="margin-top: 50px;">
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Директор Академии</p>
                    <p>___________________</p>
                </div>
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Руководитель курса</p>
                    <p>___________________</p>
                </div>
            </div>
        </div>
    `;
    
    setTimeout(() => {
        if (confirm('Хотите увидеть предварительный просмотр сертификата?')) {
            const win = window.open();
            win.document.write(certificateContent);
            win.document.title = 'Сертификат - Фишинг и социальная инженерия';
        }
    }, 500);
}

// Функции для проверок уроков (дополнение к существующим)
function checkPhishingLesson1() {
    document.getElementById('lesson1-result').innerHTML = `
        <div class="alert success">
            <i class="fas fa-check-circle"></i> 
            <strong>Верно!</strong> Фишинг может приходить через email, SMS, социальные сети, мессенджеры и даже телефонные звонки.
        </div>
    `;
}

function checkPhishingLesson2() {
    document.getElementById('lesson2-result').innerHTML = `
        <div class="alert success">
            <i class="fas fa-check-circle"></i> 
            <strong>Верно!</strong> Домен vtb-security.ru подозрителен, так как настоящий домен vtb — vtb.ru.
        </div>
    `;
}

function checkPhishingLesson3() {
    document.getElementById('lesson3-result').innerHTML = `
        <div class="alert success">
            <i class="fas fa-check-circle"></i> 
            <strong>Верно!</strong> Никогда не переходите по ссылкам из подозрительных SMS. Проверяйте информацию в официальном приложении банка.
        </div>
    `;
}

function checkPhishingLesson4() {
    document.getElementById('lesson4-result').innerHTML = `
        <div class="alert success">
            <i class="fas fa-check-circle"></i> 
            <strong>Верно!</strong> Официальные страницы компаний в соцсетях имеют галочку подтверждения и большое количество подписчиков.
        </div>
    `;
}

function checkPhishingLesson5() {
    document.getElementById('lesson5-result').innerHTML = `
        <div class="alert success">
            <i class="fas fa-check-circle"></i> 
            <strong>Верно!</strong> Настоящие сотрудники банка никогда не просят назвать коды из SMS. Всегда перезванивайте по официальному номеру.
        </div>
    `;
}

function checkPhishingLesson6() {
    document.getElementById('lesson6-result').innerHTML = `
        <div class="alert success">
            <i class="fas fa-check-circle"></i> 
            <strong>Верно!</strong> Домен vk-security.ru подозрителен. Официальные домены ВКонтакте: vk.com, vk.ru, id.vk.com.
        </div>
    `;
}

function checkPhishingLesson7() {
    document.getElementById('lesson7-result').innerHTML = `
        <div class="alert success">
            <i class="fas fa-check-circle"></i> 
            <strong>Верно!</strong> Самый важный фактор защиты — ваша внимательность и знания. Технические средства — лишь дополнение.
        </div>
    `;
}
// Функция запуска теста по Госуслугам
function startGosuslugiTest() {
// ПРОКРУТКА ВВЕРХ
    scrollToTop();
    // Показываем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // Инициализируем вопросы теста
    gosuslugiTestQuestions = [
        {
            question: "Какой единственный официальный сайт Госуслуг?",
            options: [
                "gosuslugi.ru",
                "gosuslugi-gov.ru",
                "gosuslugi-online.ru",
                "gosuslugi-portal.com"
            ],
            correctAnswer: 0,
            explanation: "Единственный официальный сайт Госуслуг — это gosuslugi.ru. Все остальные домены с дополнительными словами или в других зонах — мошеннические."
        },
        {
            question: "Что делать, если вам звонят и представляются сотрудником Госуслуг, прося назвать код из SMS?",
            options: [
                "Назвать код, чтобы подтвердить личность",
                "Вежливо отказаться и перезвонить на горячую линию 8-800-100-70-10",
                "Попросить оператора прислать официальное письмо",
                "Спросить номер служебного удостоверения"
            ],
            correctAnswer: 1,
            explanation: "Настоящие сотрудники Госуслуг НИКОГДА не просят назвать коды из SMS. Единственно правильное действие — завершить разговор и самостоятельно перезвонить на официальную горячую линию."
        },
        {
            question: "Какое сообщение точно является мошенническим?",
            options: [
                "'На Госуслугах доступна новая услуга'",
                "'Вы выиграли 50,000 руб. в лотерее от Госуслуг. Оплатите комиссию 500 руб.'",
                "'Ваш пароль будет сброшен через 30 дней'",
                "'Обновлены условия пользования порталом'"
            ],
            correctAnswer: 1,
            explanation: "Госуслуги не проводят лотереи и не требуют оплаты комиссий для получения выплат. Все сообщения о выигрышах с требованием предоплаты — мошеннические."
        },
        {
            question: "Что означает значок замка в адресной строке браузера на сайте Госуслуг?",
            options: [
                "Сайт загружается быстро",
                "Соединение защищено шифрованием (HTTPS)",
                "Сайт официальный и проверенный",
                "На сайте есть платежные формы"
            ],
            correctAnswer: 1,
            explanation: "Значок замка означает, что соединение защищено протоколом HTTPS, который шифрует передаваемые данные. Однако это не гарантирует, что сайт официальный — мошенники тоже могут использовать HTTPS."
        },
        {
            question: "Какой из этих способов НЕ является официальным способом подтверждения личности на Госуслугах?",
            options: [
                "Через мобильное приложение 'Госуслуги'",
                "С помощью электронной подписи",
                "Через код, присланный по почте",
                "Через звонок от 'службы безопасности' с просьбой назвать паспортные данные"
            ],
            correctAnswer: 3,
            explanation: "Служба безопасности Госуслуг никогда не звонит с просьбой назвать паспортные данные или коды подтверждения. Официальные способы: приложение, электронная подпись, коды по почте или через МФЦ."
        },
        {
            question: "Что нужно сделать в первую очередь, если вы случайно ввели данные на подозрительном сайте?",
            options: [
                "Ничего, если деньги не списались",
                "Немедленно сменить пароль на Госуслугах",
                "Дождаться уведомления от банка",
                "Написать в поддержку сайта"
            ],
            correctAnswer: 1,
            explanation: "При малейшем подозрении, что данные могли попасть к мошенникам, нужно немедленно сменить пароль на Госуслугах и включить 'Выход со всех устройств' в настройках безопасности."
        },
        {
            question: "Какое утверждение о выплатах через Госуслуги является ПРАВИЛЬНЫМ?",
            options: [
                "Все выплаты требуют предварительной оплаты госпошлины",
                "Информация о выплатах есть только в SMS-сообщениях",
                "Выплаты оформляются бесплатно, информация есть в личном кабинете",
                "Для получения выплат нужно перевести деньги на 'резервный счет'"
            ],
            correctAnswer: 2,
            explanation: "Все государственные выплаты оформляются БЕСПЛАТНО. Информация о них доступна в личном кабинете на официальном сайте. Любые требования оплаты — признак мошенничества."
        },
        {
            question: "Какой номер телефона является официальной горячей линией Госуслуг?",
            options: [
                "8-800-100-70-10",
                "8-900-123-45-67",
                "8-495-777-77-77",
                "8-800-555-35-35"
            ],
            correctAnswer: 0,
            explanation: "Единственный официальный номер горячей линии Госуслуг — 8-800-100-70-10. Он работает круглосуточно, бесплатно со всех телефонов России."
        },
        {
            question: "Что означает двухфакторная аутентификация на Госуслугах?",
            options: [
                "Использование двух паролей",
                "Подтверждение входа через два разных браузера",
                "Использование двух способов подтверждения (пароль + код)",
                "Регистрация двух аккаунтов"
            ],
            correctAnswer: 2,
            explanation: "Двухфакторная аутентификация — это использование двух разных способов подтверждения личности: что-то, что вы знаете (пароль) и что-то, что у вас есть (код из приложения/SMS). Это значительно повышает безопасность."
        },
        {
            question: "Какое действие НЕОБХОДИМО выполнить при получении SMS о 'блокировке аккаунта Госуслуг'?",
            options: [
                "Немедленно перейти по ссылке из SMS",
                "Позвонить по номеру из SMS для разблокировки",
                "Зайти на официальный сайт gosuslugi.ru напрямую",
                "Ничего не делать — это точно мошенники"
            ],
            correctAnswer: 2,
            explanation: "При получении любого подозрительного сообщения НЕЛЬЗЯ переходить по ссылкам или звонить по указанным номерам. Нужно самостоятельно зайти на официальный сайт и проверить статус аккаунта."
        }
    ];
    
    // Сбрасываем данные теста
    gosuslugiCurrentQuestion = 0;
    gosuslugiUserAnswers = [];
    gosuslugiTestStartTime = new Date();
    
    // Загружаем страницу теста
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon gosuslugi">
                <i class="fas fa-passport"></i>
            </div>
            <div class="course-header-content">
                <h1>Итоговый тест: Мошенничество с Госуслугами</h1>
                <p>Проверьте свои знания по пройденному материалу. 10 вопросов, для успешного прохождения нужно правильно ответить на 8 вопросов (80%).</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-question-circle"></i>
                        <span>10 вопросов</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>20 минут</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Проходной балл: 80%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="gosuslugiTestContainer">
            <div id="gosuslugiTestInstructions" style="text-align: center; padding: 40px 0;">
                <h3>Инструкция к тесту</h3>
                <p style="margin: 20px 0;">Тест состоит из 10 вопросов с одним правильным ответом.</p>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; max-width: 600px; margin: 0 auto;">
                    <h4><i class="fas fa-info-circle icon" style="color: #5c6bc0;"></i> Правила тестирования:</h4>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Выберите один вариант ответа на каждый вопрос</li>
                        <li>Можно вернуться к предыдущим вопросам</li>
                        <li>На прохождение теста отводится 20 минут</li>
                        <li>После завершения вы увидите детальный результат</li>
                        <li>Для успешного прохождения нужно ≥ 80% правильных ответов</li>
                    </ul>
                </div>
                
                <button class="btn btn-large btn-success" onclick="beginGosuslugiTest()" style="margin-top: 30px;">
                    <i class="fas fa-play icon"></i> Начать тест
                </button>
                
                <button class="btn btn-large btn-outline" onclick="showPage('courses')" style="margin-top: 30px; margin-left: 15px;">
                    <i class="fas fa-arrow-left icon"></i> Вернуться к курсам
                </button>
            </div>
            
            <div id="gosuslugiTestQuestions" style="display: none;">
                <!-- Вопросы будут загружены динамически -->
            </div>
            
            <div id="gosuslugiTestResults" style="display: none;">
                <!-- Результаты будут загружены динамически -->
            </div>
        </div>
    `;
}

// Функция для начала теста
function beginGosuslugiTest() {
    // Скрываем инструкции и показываем вопросы
    document.getElementById('gosuslugiTestInstructions').style.display = 'none';
    document.getElementById('gosuslugiTestQuestions').style.display = 'block';
    
    // Запускаем таймер
    startGosuslugiTestTimer();
    
    // Загружаем первый вопрос
    loadGosuslugiTestQuestion();
}

// Функция для загрузки вопроса
function loadGosuslugiTestQuestion() {
    const testQuestionsDiv = document.getElementById('gosuslugiTestQuestions');
    const question = gosuslugiTestQuestions[gosuslugiCurrentQuestion];
    
    testQuestionsDiv.innerHTML = `
        <div class="simulator">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h3>Вопрос ${gosuslugiCurrentQuestion + 1} из ${gosuslugiTestQuestions.length}</h3>
                <div id="gosuslugiTestTimer" style="background-color: #f5f5f5; padding: 8px 15px; border-radius: 20px; font-weight: bold;">
                    <i class="fas fa-clock icon"></i> <span id="gosuslugiTimeRemaining">20:00</span>
                </div>
            </div>
            
            <div style="background-color: #f8f9fa; padding: 25px; border-radius: 10px; margin-bottom: 25px;">
                <h4 style="color: #5c6bc0; margin-bottom: 15px;">${question.question}</h4>
            </div>
            
            <div class="options">
                ${question.options.map((option, index) => `
                    <div class="option" onclick="selectGosuslugiTestAnswer(${index})" 
                         style="${gosuslugiUserAnswers[gosuslugiCurrentQuestion] === index ? 'border-color: #5c6bc0; background-color: #e8eaf6;' : ''}">
                        ${String.fromCharCode(65 + index)}. ${option}
                    </div>
                `).join('')}
            </div>
            
            <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 30px;">
    ${gosuslugiCurrentQuestion > 0 ? `
        <button class="btn btn-outline" onclick="prevGosuslugiTestQuestion()" style="padding: 8px 20px;">
            <i class="fas fa-arrow-left icon"></i> Назад
        </button>
    ` : '<div style="width: 100px;"></div>'}
    
    <div style="text-align: center;">
        <button class="btn btn-success" onclick="nextGosuslugiTestQuestion()" id="gosuslugiNextButton" 
                ${gosuslugiUserAnswers[gosuslugiCurrentQuestion] === undefined ? 'disabled' : ''}
                style="padding: 8px 25px;">
            ${gosuslugiCurrentQuestion === gosuslugiTestQuestions.length - 1 ? 'Завершить тест' : 'Следующий вопрос'} 
            <i class="fas fa-arrow-right icon"></i>
        </button>
        <p style="margin-top: 8px; color: #666; font-size: 0.85rem;">
            Вопрос ${gosuslugiCurrentQuestion + 1} из ${gosuslugiTestQuestions.length}
        </p>
    </div>
    
    <div style="text-align: right;">
        <button class="btn btn-danger" onclick="cancelGosuslugiTest()" style="padding: 8px 20px;">
            <i class="fas fa-times icon"></i> Отменить
        </button>
    </div>
</div>
            
            <div style="margin-top: 20px; text-align: center; color: #666;">
                <p><i class="fas fa-info-circle icon"></i> Выберите один вариант ответа</p>
            </div>
        </div>
    `;
}

// Функция выбора ответа
function selectGosuslugiTestAnswer(answerIndex) {
    // Убираем выделение со всех вариантов
    document.querySelectorAll('#gosuslugiTestQuestions .option').forEach(option => {
        option.style.borderColor = '#ddd';
        option.style.backgroundColor = 'white';
    });
    
    // Выделяем выбранный вариант
    event.target.style.borderColor = '#5c6bc0';
    event.target.style.backgroundColor = '#e8eaf6';
    
    // Сохраняем ответ
    gosuslugiUserAnswers[gosuslugiCurrentQuestion] = answerIndex;
    
    // Активируем кнопку "Далее"
    document.getElementById('gosuslugiNextButton').disabled = false;
}

// Функция для перехода к следующему вопросу
function nextGosuslugiTestQuestion() {
    // Проверяем, выбран ли ответ
    if (gosuslugiUserAnswers[gosuslugiCurrentQuestion] === undefined) {
        showNotification('error', 'Пожалуйста, выберите вариант ответа');
        return;
    }
    
    // Переходим к следующему вопросу или завершаем тест
    if (gosuslugiCurrentQuestion < gosuslugiTestQuestions.length - 1) {
        gosuslugiCurrentQuestion++;
        loadGosuslugiTestQuestion();
    } else {
        finishGosuslugiTest();
    }
}

// Функция для возврата к предыдущему вопросу
function prevGosuslugiTestQuestion() {
    if (gosuslugiCurrentQuestion > 0) {
        gosuslugiCurrentQuestion--;
        loadGosuslugiTestQuestion();
    }
}

// Функция запуска таймера теста
function startGosuslugiTestTimer() {
    let timeLeft = 20 * 60; // 20 минут в секундах
    
    gosuslugiTestTimer = setInterval(function() {
        timeLeft--;
        
        const minutes = Math.floor(timeLeft / 60);
        const seconds = timeLeft % 60;
        
        document.getElementById('gosuslugiTimeRemaining').textContent = 
            `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        
        // Меняем цвет при малом остатке времени
        if (timeLeft < 300) { // Меньше 5 минут
            document.getElementById('gosuslugiTestTimer').style.backgroundColor = '#ffebee';
            document.getElementById('gosuslugiTestTimer').style.color = '#d32f2f';
        }
        
        if (timeLeft <= 0) {
            clearInterval(gosuslugiTestTimer);
            finishGosuslugiTest();
        }
    }, 1000);
}

// Функция завершения теста
function finishGosuslugiTest() {
    clearInterval(gosuslugiTestTimer);
    
    // Рассчитываем результаты
    let correctAnswers = 0;
    let resultsHTML = '';
    
    gosuslugiTestQuestions.forEach((question, index) => {
        const userAnswer = gosuslugiUserAnswers[index];
        const isCorrect = userAnswer === question.correctAnswer;
        
        if (isCorrect) correctAnswers++;
        
        resultsHTML += `
            <div style="margin-bottom: 20px; padding: 15px; border-radius: 8px; background-color: ${isCorrect ? '#e8f5e9' : '#ffebee'}; border-left: 5px solid ${isCorrect ? '#388e3c' : '#d32f2f'};">
                <p><strong>Вопрос ${index + 1}:</strong> ${question.question}</p>
                <p><strong>Ваш ответ:</strong> ${userAnswer !== undefined ? question.options[userAnswer] : 'Не ответили'}</p>
                <p><strong>Правильный ответ:</strong> ${question.options[question.correctAnswer]}</p>
                <p style="margin-top: 10px; color: #666;"><i class="fas fa-info-circle icon"></i> ${question.explanation}</p>
            </div>
        `;
    });
    
    const score = Math.round((correctAnswers / gosuslugiTestQuestions.length) * 100);
    const isPassed = score >= 80;
    
    // Обновляем прогресс пользователя
    if (currentUser && isPassed) {
        // Отмечаем тест как пройденный
        if (!currentUser.completedCourses) currentUser.completedCourses = [];
        if (!currentUser.completedCourses.includes('gosuslugi')) {
            currentUser.completedCourses.push('gosuslugi');
        }
        
        // Обновляем прогресс курса
        currentUser.progress.gosuslugi = 100;
        currentUser.stats.completedLessons++;
        currentUser.stats.score += 50; // Бонус за прохождение теста
        currentUser.stats.testResults.push({
            course: 'gosuslugi',
            score: score,
            date: new Date().toISOString()
        });
        
        updateUserInStorage();
    }
    
    // Показываем результаты
    document.getElementById('gosuslugiTestQuestions').style.display = 'none';
    document.getElementById('gosuslugiTestResults').style.display = 'block';
    document.getElementById('gosuslugiTestResults').innerHTML = `
        <div class="simulator" style="text-align: center;">
            <h3>Результаты теста</h3>
            
            <div style="margin: 30px 0;">
                <div style="font-size: 3rem; color: ${isPassed ? '#388e3c' : '#d32f2f'}; margin-bottom: 10px;">
                    ${score}%
                </div>
                <div style="font-size: 1.2rem; margin-bottom: 20px;">
                    ${correctAnswers} из ${gosuslugiTestQuestions.length} правильных ответов
                </div>
                
                <div style="background-color: ${isPassed ? '#e8f5e9' : '#ffebee'}; padding: 20px; border-radius: 10px; max-width: 500px; margin: 0 auto;">
                    <h4 style="color: ${isPassed ? '#388e3c' : '#d32f2f'};">
                        <i class="fas ${isPassed ? 'fa-check-circle' : 'fa-times-circle'} icon"></i>
                        ${isPassed ? 'Тест пройден успешно!' : 'Тест не пройден'}
                    </h4>
                    <p>Для успешного прохождения необходимо набрать 80% правильных ответов.</p>
                </div>
            </div>
            
            ${isPassed ? `
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-trophy icon" style="color: #ff9800;"></i> Поздравляем!</h4>
                    <p>Вы успешно прошли курс "Мошенничество с Госуслугами" и получили +50 очков к вашему рейтингу.</p>
                    ${currentUser ? `
                        <p style="margin-top: 10px;">Ваш текущий счет: <strong>${currentUser.stats.score} очков</strong></p>
                    ` : ''}
                </div>
            ` : `
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-redo icon" style="color: #1976d2;"></i> Рекомендации</h4>
                    <p>Рекомендуем повторить материал курса и пройти тест снова.</p>
                    <p>Обратите особое внимание на вопросы, в которых допустили ошибки.</p>
                </div>
            `}
            
            <h4 style="margin-top: 30px; margin-bottom: 20px;">Детализация ответов:</h4>
            <div style="max-height: 400px; overflow-y: auto; padding-right: 10px;">
                ${resultsHTML}
            </div>
            
            <div style="margin-top: 30px;">
                <button class="btn btn-large ${isPassed ? 'btn-success' : 'btn-warning'}" onclick="${isPassed ? 'showPage(\'courses\')' : 'retryGosuslugiTest()'}">
                    ${isPassed ? 'Вернуться к курсам' : 'Попробовать снова'}
                </button>
                
                ${isPassed ? `
                    <button class="btn btn-large btn-outline" onclick="downloadGosuslugiCertificate()" style="margin-left: 15px;">
                        <i class="fas fa-download icon"></i> Скачать сертификат
                    </button>
                ` : ''}
            </div>
        </div>
    `;
    
    // Прокручиваем к результатам
    document.getElementById('gosuslugiTestResults').scrollIntoView({ behavior: 'smooth' });
}

// Функция повторного прохождения теста
function retryGosuslugiTest() {
    gosuslugiCurrentQuestion = 0;
    gosuslugiUserAnswers = [];
    
    document.getElementById('gosuslugiTestResults').style.display = 'none';
    document.getElementById('gosuslugiTestQuestions').style.display = 'block';
    
    gosuslugiTestStartTime = new Date();
    startGosuslugiTestTimer();
    loadGosuslugiTestQuestion();
}

// Функция отмены теста
function cancelGosuslugiTest() {
    if (confirm('Вы уверены, что хотите отменить тест? Все ответы будут потеряны.')) {
        clearInterval(gosuslugiTestTimer);
        showPage('courses');
    }
}

// Функция "скачивания" сертификата
function downloadGosuslugiCertificate() {
    showNotification('success', 'Сертификат успешно сгенерирован! В полной версии здесь будет ссылка для скачивания.');
    
    const certificateContent = `
        <div style="text-align: center; padding: 40px; background-color: white; border: 10px solid #5c6bc0; max-width: 800px; margin: 0 auto;">
            <h1 style="color: #5c6bc0;">СЕРТИФИКАТ</h1>
            <p style="font-size: 1.2rem;">Настоящий сертификат подтверждает, что</p>
            <h2 style="color: #3949ab; margin: 20px 0;">${currentUser ? currentUser.name : 'Студент'}</h2>
            <p style="font-size: 1.2rem;">успешно прошел(а) курс</p>
            <h3 style="color: #5c6bc0; margin: 20px 0;">"Мошенничество с Госуслугами"</h3>
            <p>в Академии Кибербезопасности</p>
            <div style="margin: 30px 0;">
                <p>Дата: ${new Date().toLocaleDateString('ru-RU')}</p>
                <p>Результат теста: ${Math.round((gosuslugiUserAnswers.filter((answer, index) => answer === gosuslugiTestQuestions[index].correctAnswer).length / gosuslugiTestQuestions.length) * 100)}%</p>
            </div>
            <div style="margin-top: 50px;">
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Директор Академии</p>
                    <p>___________________</p>
                </div>
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Руководитель курса</p>
                    <p>___________________</p>
                </div>
            </div>
        </div>
    `;
    
    setTimeout(() => {
        if (confirm('Хотите увидеть предварительный просмотр сертификата?')) {
            const win = window.open();
            win.document.write(certificateContent);
            win.document.title = 'Сертификат - Мошенничество с Госуслугами';
        }
    }, 500);
}
// Глобальные переменные для финансового теста
let financeTestQuestions = [];
let financeCurrentQuestion = 0;
let financeUserAnswers = [];
let financeTestStartTime;
let financeTestTimer;

// Функция запуска теста по финансовому мошенничеству
function startFinanceFraudTest() {
// ПРОКРУТКА ВВЕРХ
    scrollToTop();
    // Показываем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // Инициализируем вопросы теста
    financeTestQuestions = [
        {
            question: "Что НИКОГДА не попросит сделать настоящий сотрудник банка?",
            options: [
                "Сообщить код из SMS",
                "Предъявить паспорт в отделении",
                "Подписать договор",
                "Обновить данные в личном кабинете"
            ],
            correctAnswer: 0,
            explanation: "Настоящие банки никогда не просят сообщать коды из SMS. Эти коды — ваша личная информация для подтверждения операций."
        },
        {
            question: "Какой процент годовой доходности обычно обещают финансовые пирамиды?",
            options: [
                "5-10%",
                "15-25%",
                "30-50%",
                "Более 100%"
            ],
            correctAnswer: 3,
            explanation: "Финансовые пирамиды часто обещают доходность более 100% годовых, что нереально для легальных инвестиций."
        },
        {
            question: "Что такое 'право на охлаждение' в финансовых услугах?",
            options: [
                "Право отказаться от услуги в течение 14 дней без объяснения причин",
                "Право на снижение процентной ставки в жаркую погоду",
                "Право на заморозку кредита на 3 месяца",
                "Право на бесплатный отказ от страховки"
            ],
            correctAnswer: 0,
            explanation: "Право на охлаждение дает 14 дней для отказа от финансовой услуги без объяснения причин и штрафов."
        },
        {
            question: "Как часто можно бесплатно проверить свою кредитную историю?",
            options: [
                "1 раз в год",
                "2 раза в год",
                "4 раза в год",
                "Неограниченно"
            ],
            correctAnswer: 1,
            explanation: "По закону вы имеете право на 2 бесплатные проверки кредитной истории в год в каждом бюро."
        },
        {
            question: "Что делать, если вы перевели деньги мошенникам по СБП?",
            options: [
                "Ничего, деньги уже не вернуть",
                "Немедленно позвонить в банк отправителя",
                "Подождать 3 дня и подать заявление",
                "Написать мошеннику с просьбой вернуть деньги"
            ],
            correctAnswer: 1,
            explanation: "Нужно немедленно позвонить в банк, с карты которого был совершен перевод. У банков есть процедуры для оспаривания операций."
        },
        {
            question: "Какой организации нужно жаловаться на действия МФО?",
            options: [
                "Прокуратуре",
                "Центральному банку РФ",
                "Роспотребнадзору",
                "Все варианты верны"
            ],
            correctAnswer: 3,
            explanation: "На действия МФО можно жаловаться в Центробанк (контроль лицензий), Роспотребнадзор (права потребителей) и прокуратуру (нарушения закона)."
        },
        {
            question: "Что такое SIM-своппинг?",
            options: [
                "Перехват SMS-сообщений через копирование SIM-карты",
                "Кража денег через мобильное приложение",
                "Взлом банковского аккаунта через Wi-Fi",
                "Фишинг через социальные сети"
            ],
            correctAnswer: 0,
            explanation: "SIM-своппинг — это метод, когда мошенники получают дубликат вашей SIM-карты и перехватывают SMS с кодами подтверждения."
        },
        {
            question: "Какой максимальный срок лишения свободы предусмотрен за мошенничество (ст. 159 УК РФ)?",
            options: [
                "3 года",
                "5 лет",
                "8 лет",
                "10 лет"
            ],
            correctAnswer: 3,
            explanation: "По статье 159 УК РФ 'Мошенничество' максимальное наказание — до 10 лет лишения свободы."
        },
        {
            question: "Что должно насторожить при получении инвестиционного предложения?",
            options: [
                "Обещание гарантированной доходности",
                "Требование срочного решения",
                "Давление на быстрый старт",
                "Все перечисленное"
            ],
            correctAnswer: 3,
            explanation: "Все эти признаки характерны для мошеннических инвестиционных предложений. Легальные инвестиции всегда связаны с рисками."
        },
        {
            question: "Куда обращаться, если оформили кредит на ваше имя без вашего ведома?",
            options: [
                "Только в полицию",
                "В банк и в полицию одновременно",
                "В службу безопасности банка",
                "Никуда, нужно платить"
            ],
            correctAnswer: 1,
            explanation: "Нужно одновременно писать заявление в банк о несогласии с кредитом и в полицию о мошенничестве."
        }
    ];
    
    // Сбрасываем данные теста
    financeCurrentQuestion = 0;
    financeUserAnswers = [];
    financeTestStartTime = new Date();
    
    // Загружаем страницу теста
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon financial">
                <i class="fas fa-credit-card"></i>
            </div>
            <div class="course-header-content">
                <h1>Тест: Финансовое мошенничество</h1>
                <p>Проверьте свои знания по защите от финансовых мошенников. 10 вопросов, для успешного прохождения нужно правильно ответить на 7 вопросов (70%).</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-question-circle"></i>
                        <span>10 вопросов</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>20 минут</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Проходной балл: 70%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="financeTestContainer">
            <div id="financeTestInstructions" style="text-align: center; padding: 40px 0;">
                <h3>Инструкция к тесту</h3>
                <p style="margin: 20px 0;">Тест состоит из 10 вопросов с одним правильным ответом.</p>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; max-width: 600px; margin: 0 auto;">
                    <h4><i class="fas fa-info-circle icon" style="color: #28a745;"></i> Правила тестирования:</h4>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Выберите один вариант ответа на каждый вопрос</li>
                        <li>Можно вернуться к предыдущим вопросам</li>
                        <li>На прохождение теста отводится 20 минут</li>
                        <li>После завершения вы увидите детальный результат</li>
                        <li>Для успешного прохождения нужно ≥ 70% правильных ответов</li>
                    </ul>
                </div>
                
                <button class="btn btn-large btn-success" onclick="beginFinanceTest()" style="margin-top: 30px;">
                    <i class="fas fa-play icon"></i> Начать тест
                </button>
                
                <button class="btn btn-large btn-outline" onclick="showPage('tests')" style="margin-top: 30px; margin-left: 15px;">
                    <i class="fas fa-arrow-left icon"></i> Вернуться к тестам
                </button>
            </div>
            
            <div id="financeTestQuestions" style="display: none;">
                <!-- Вопросы будут загружены динамически -->
            </div>
            
            <div id="financeTestResults" style="display: none;">
                <!-- Результаты будут загружены динамически -->
            </div>
        </div>
    `;
}

// Функция для начала теста
function beginFinanceTest() {
    // Скрываем инструкции и показываем вопросы
    document.getElementById('financeTestInstructions').style.display = 'none';
    document.getElementById('financeTestQuestions').style.display = 'block';
    
    // Запускаем таймер
    startFinanceTestTimer();
    
    // Загружаем первый вопрос
    loadFinanceTestQuestion();
}

// Функция для загрузки вопроса
function loadFinanceTestQuestion() {
    const testQuestionsDiv = document.getElementById('financeTestQuestions');
    const question = financeTestQuestions[financeCurrentQuestion];
    
    testQuestionsDiv.innerHTML = `
        <div class="simulator">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h3>Вопрос ${financeCurrentQuestion + 1} из ${financeTestQuestions.length}</h3>
                <div id="financeTestTimer" style="background-color: #f5f5f5; padding: 8px 15px; border-radius: 20px; font-weight: bold;">
                    <i class="fas fa-clock icon"></i> <span id="financeTimeRemaining">20:00</span>
                </div>
            </div>
            
            <div style="background-color: #f8f9fa; padding: 25px; border-radius: 10px; margin-bottom: 25px;">
                <h4 style="color: #28a745; margin-bottom: 15px;">${question.question}</h4>
            </div>
            
            <div class="options">
                ${question.options.map((option, index) => `
                    <div class="option" onclick="selectFinanceTestAnswer(${index})" 
                         style="${financeUserAnswers[financeCurrentQuestion] === index ? 'border-color: #28a745; background-color: #d4edda;' : ''}">
                        ${String.fromCharCode(65 + index)}. ${option}
                    </div>
                `).join('')}
            </div>
            
            <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 30px;">
    ${financeCurrentQuestion > 0 ? `
        <button class="btn btn-outline" onclick="prevFinanceTestQuestion()" style="padding: 8px 20px;">
            <i class="fas fa-arrow-left icon"></i> Назад
        </button>
    ` : '<div style="width: 100px;"></div>'}
    
    <div style="text-align: center;">
        <button class="btn btn-success" onclick="nextFinanceTestQuestion()" id="financeNextButton" 
                ${financeUserAnswers[financeCurrentQuestion] === undefined ? 'disabled' : ''}
                style="padding: 8px 25px;">
            ${financeCurrentQuestion === financeTestQuestions.length - 1 ? 'Завершить тест' : 'Следующий вопрос'} 
            <i class="fas fa-arrow-right icon"></i>
        </button>
        <p style="margin-top: 8px; color: #666; font-size: 0.85rem;">
            Вопрос ${financeCurrentQuestion + 1} из ${financeTestQuestions.length}
        </p>
    </div>
    
    <div style="text-align: right;">
        <button class="btn btn-danger" onclick="cancelFinanceTest()" style="padding: 8px 20px;">
            <i class="fas fa-times icon"></i> Отменить
        </button>
    </div>
</div>
            
            <div style="margin-top: 20px; text-align: center; color: #666;">
                <p><i class="fas fa-info-circle icon"></i> Выберите один вариант ответа</p>
            </div>
        </div>
    `;
}

// Функция выбора ответа
function selectFinanceTestAnswer(answerIndex) {
    // Убираем выделение со всех вариантов
    document.querySelectorAll('#financeTestQuestions .option').forEach(option => {
        option.style.borderColor = '#ddd';
        option.style.backgroundColor = 'white';
    });
    
    // Выделяем выбранный вариант
    event.target.style.borderColor = '#28a745';
    event.target.style.backgroundColor = '#d4edda';
    
    // Сохраняем ответ
    financeUserAnswers[financeCurrentQuestion] = answerIndex;
    
    // Активируем кнопку "Далее"
    document.getElementById('financeNextButton').disabled = false;
}

// Функция для перехода к следующему вопросу
function nextFinanceTestQuestion() {
    // Проверяем, выбран ли ответ
    if (financeUserAnswers[financeCurrentQuestion] === undefined) {
        showNotification('error', 'Пожалуйста, выберите вариант ответа');
        return;
    }
    
    // Переходим к следующему вопросу или завершаем тест
    if (financeCurrentQuestion < financeTestQuestions.length - 1) {
        financeCurrentQuestion++;
        loadFinanceTestQuestion();
    } else {
        finishFinanceTest();
    }
}

// Функция для возврата к предыдущему вопросу
function prevFinanceTestQuestion() {
    if (financeCurrentQuestion > 0) {
        financeCurrentQuestion--;
        loadFinanceTestQuestion();
    }
}

// Функция запуска таймера теста
function startFinanceTestTimer() {
    let timeLeft = 20 * 60; // 20 минут в секундах
    
    financeTestTimer = setInterval(function() {
        timeLeft--;
        
        const minutes = Math.floor(timeLeft / 60);
        const seconds = timeLeft % 60;
        
        document.getElementById('financeTimeRemaining').textContent = 
            `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        
        // Меняем цвет при малом остатке времени
        if (timeLeft < 300) { // Меньше 5 минут
            document.getElementById('financeTestTimer').style.backgroundColor = '#ffebee';
            document.getElementById('financeTestTimer').style.color = '#d32f2f';
        }
        
        if (timeLeft <= 0) {
            clearInterval(financeTestTimer);
            finishFinanceTest();
        }
    }, 1000);
}

// Функция завершения теста
function finishFinanceTest() {
    clearInterval(financeTestTimer);
    
    // Рассчитываем результаты
    let correctAnswers = 0;
    let resultsHTML = '';
    
    financeTestQuestions.forEach((question, index) => {
        const userAnswer = financeUserAnswers[index];
        const isCorrect = userAnswer === question.correctAnswer;
        
        if (isCorrect) correctAnswers++;
        
        resultsHTML += `
            <div style="margin-bottom: 20px; padding: 15px; border-radius: 8px; background-color: ${isCorrect ? '#e8f5e9' : '#ffebee'}; border-left: 5px solid ${isCorrect ? '#388e3c' : '#d32f2f'};">
                <p><strong>Вопрос ${index + 1}:</strong> ${question.question}</p>
                <p><strong>Ваш ответ:</strong> ${userAnswer !== undefined ? question.options[userAnswer] : 'Не ответили'}</p>
                <p><strong>Правильный ответ:</strong> ${question.options[question.correctAnswer]}</p>
                <p style="margin-top: 10px; color: #666;"><i class="fas fa-info-circle icon"></i> ${question.explanation}</p>
            </div>
        `;
    });
    
    const score = Math.round((correctAnswers / financeTestQuestions.length) * 100);
    const isPassed = score >= 70;
    
    // Обновляем прогресс пользователя
    if (currentUser && isPassed) {
        // Отмечаем тест как пройденный
        if (!currentUser.completedCourses) currentUser.completedCourses = [];
        if (!currentUser.completedCourses.includes('finance')) {
            currentUser.completedCourses.push('finance');
        }
        
        // Обновляем прогресс теста
        if (!currentUser.testResults) currentUser.testResults = [];
        currentUser.testResults.push({
            test: 'finance',
            score: score,
            date: new Date().toISOString()
        });
        
        updateUserInStorage();
    }
    
    // Показываем результаты
    document.getElementById('financeTestQuestions').style.display = 'none';
    document.getElementById('financeTestResults').style.display = 'block';
    document.getElementById('financeTestResults').innerHTML = `
        <div class="simulator" style="text-align: center;">
            <h3>Результаты теста</h3>
            
            <div style="margin: 30px 0;">
                <div style="font-size: 3rem; color: ${isPassed ? '#388e3c' : '#d32f2f'}; margin-bottom: 10px;">
                    ${score}%
                </div>
                <div style="font-size: 1.2rem; margin-bottom: 20px;">
                    ${correctAnswers} из ${financeTestQuestions.length} правильных ответов
                </div>
                
                <div style="background-color: ${isPassed ? '#e8f5e9' : '#ffebee'}; padding: 20px; border-radius: 10px; max-width: 500px; margin: 0 auto;">
                    <h4 style="color: ${isPassed ? '#388e3c' : '#d32f2f'};">
                        <i class="fas ${isPassed ? 'fa-check-circle' : 'fa-times-circle'} icon"></i>
                        ${isPassed ? 'Тест пройден успешно!' : 'Тест не пройден'}
                    </h4>
                    <p>Для успешного прохождения необходимо набрать 70% правильных ответов.</p>
                </div>
            </div>
            
            ${isPassed ? `
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-trophy icon" style="color: #ff9800;"></i> Поздравляем!</h4>
                    <p>Вы успешно прошли тест "Финансовое мошенничество".</p>
                    ${currentUser ? `
                        <p style="margin-top: 10px;">Ваши пройденные тесты: ${currentUser.completedCourses ? currentUser.completedCourses.length : 0}</p>
                    ` : ''}
                </div>
            ` : `
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-redo icon" style="color: #1976d2;"></i> Рекомендации</h4>
                    <p>Рекомендуем изучить тему финансового мошенничества и пройти тест снова.</p>
                    <p>Обратите особое внимание на вопросы, в которых допустили ошибки.</p>
                </div>
            `}
            
            <h4 style="margin-top: 30px; margin-bottom: 20px;">Детализация ответов:</h4>
            <div style="max-height: 400px; overflow-y: auto; padding-right: 10px;">
                ${resultsHTML}
            </div>
            
            <div style="margin-top: 30px;">
                <button class="btn btn-large ${isPassed ? 'btn-success' : 'btn-warning'}" onclick="${isPassed ? 'showPage(\'tests\')' : 'retryFinanceTest()'}">
                    ${isPassed ? 'Вернуться к тестам' : 'Попробовать снова'}
                </button>
                
                ${isPassed ? `
                    <button class="btn btn-large btn-outline" onclick="downloadFinanceCertificate()" style="margin-left: 15px;">
                        <i class="fas fa-download icon"></i> Скачать сертификат
                    </button>
                ` : ''}
            </div>
        </div>
    `;
    
    // Прокручиваем к результатам
    document.getElementById('financeTestResults').scrollIntoView({ behavior: 'smooth' });
}

// Функция повторного прохождения теста
function retryFinanceTest() {
    financeCurrentQuestion = 0;
    financeUserAnswers = [];
    
    document.getElementById('financeTestResults').style.display = 'none';
    document.getElementById('financeTestQuestions').style.display = 'block';
    
    financeTestStartTime = new Date();
    startFinanceTestTimer();
    loadFinanceTestQuestion();
}

// Функция отмены теста
function cancelFinanceTest() {
    if (confirm('Вы уверены, что хотите отменить тест? Все ответы будут потеряны.')) {
        clearInterval(financeTestTimer);
        showPage('tests');
    }
}

// Функция "скачивания" сертификата
function downloadFinanceCertificate() {
    showNotification('success', 'Сертификат успешно сгенерирован! В полной версии здесь будет ссылка для скачивания.');
    
    const certificateContent = `
        <div style="text-align: center; padding: 40px; background-color: white; border: 10px solid #28a745; max-width: 800px; margin: 0 auto;">
            <h1 style="color: #28a745;">СЕРТИФИКАТ</h1>
            <p style="font-size: 1.2rem;">Настоящий сертификат подтверждает, что</p>
            <h2 style="color: #1e7e34; margin: 20px 0;">${currentUser ? currentUser.name : 'Студент'}</h2>
            <p style="font-size: 1.2rem;">успешно прошел(а) тест</p>
            <h3 style="color: #28a745; margin: 20px 0;">"Финансовое мошенничество"</h3>
            <p>в Академии Кибербезопасности</p>
            <div style="margin: 30px 0;">
                <p>Дата: ${new Date().toLocaleDateString('ru-RU')}</p>
                <p>Результат теста: ${Math.round((financeUserAnswers.filter((answer, index) => answer === financeTestQuestions[index].correctAnswer).length / financeTestQuestions.length) * 100)}%</p>
            </div>
            <div style="margin-top: 50px;">
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Директор Академии</p>
                    <p>___________________</p>
                </div>
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Руководитель курса</p>
                    <p>___________________</p>
                </div>
            </div>
        </div>
    `;
    
    setTimeout(() => {
        if (confirm('Хотите увидеть предварительный просмотр сертификата?')) {
            const win = window.open();
            win.document.write(certificateContent);
            win.document.title = 'Сертификат - Финансовое мошенничество';
        }
    }, 500);
}
// Начало теста "Тест по паролям и аутентификации"
function startFinancialTest() {
    testAnswers = [];
    testCurrentQuestion = 1;
    
    const testQuestions = [
        {
            question: "Что НИКОГДА не попросит сделать настоящий сотрудник банка?",
            options: [
                "Сообщить код из SMS",
                "Предъявить паспорт в отделении",
                "Подписать договор",
                "Обновить данные в личном кабинете"
            ],
            correct: 0,
            explanation: "Настоящие банки никогда не просят сообщать коды из SMS. Эти коды — ваша личная информация для подтверждения операций."
        },
        {
            question: "Какой процент годовой доходности обычно обещают финансовые пирамиды?",
            options: [
                "5-10%",
                "15-25%",
                "30-50%",
                "Более 100%"
            ],
            correct: 3,
            explanation: "Финансовые пирамиды часто обещают доходность более 100% годовых, что нереально для легальных инвестиций."
        },
        {
            question: "Что такое 'право на охлаждение' в финансовых услугах?",
            options: [
                "Право отказаться от услуги в течение 14 дней без объяснения причин",
                "Право на снижение процентной ставки в жаркую погоду",
                "Право на заморозку кредита на 3 месяца",
                "Право на бесплатный отказ от страховки"
            ],
            correct: 0,
            explanation: "Право на охлаждение дает 14 дней для отказа от финансовой услуги без объяснения причин и штрафов."
        },
        {
            question: "Как часто можно бесплатно проверить свою кредитную историю?",
            options: [
                "1 раз в год",
                "2 раза в год",
                "4 раза в год",
                "Неограниченно"
            ],
            correct: 1,
            explanation: "По закону вы имеете право на 2 бесплатные проверки кредитной истории в год в каждом бюро."
        },
        {
            question: "Что делать, если вы перевели деньги мошенникам по СБП?",
            options: [
                "Ничего, деньги уже не вернуть",
                "Немедленно позвонить в банк отправителя",
                "Подождать 3 дня и подать заявление",
                "Написать мошеннику с просьбой вернуть деньги"
            ],
            correct: 1,
            explanation: "Нужно немедленно позвонить в банк, с карты которого был совершен перевод. У банков есть процедуры для оспаривания операций."
        },
        {
            question: "Какой организации нужно жаловаться на действия МФО?",
            options: [
                "Прокуратуре",
                "Центральному банку РФ",
                "Роспотребнадзору",
                "Все варианты верны"
            ],
            correct: 3,
            explanation: "На действия МФО можно жаловаться в Центробанк (контроль лицензий), Роспотребнадзор (права потребителей) и прокуратуру (нарушения закона)."
        },
        {
            question: "Что такое SIM-своппинг?",
            options: [
                "Перехват SMS-сообщений через копирование SIM-карты",
                "Кража денег через мобильное приложение",
                "Взлом банковского аккаунта через Wi-Fi",
                "Фишинг через социальные сети"
            ],
            correct: 0,
            explanation: "SIM-своппинг — это метод, когда мошенники получают дубликат вашей SIM-карты и перехватывают SMS с кодами подтверждения."
        },
        {
            question: "Какой максимальный срок лишения свободы предусмотрен за мошенничество (ст. 159 УК РФ)?",
            options: [
                "3 года",
                "5 лет",
                "8 лет",
                "10 лет"
            ],
            correct: 3,
            explanation: "По статье 159 УК РФ 'Мошенничество' максимальное наказание — до 10 лет лишения свободы."
        },
        {
            question: "Что должно насторожить при получении инвестиционного предложения?",
            options: [
                "Обещание гарантированной доходности",
                "Требование срочного решения",
                "Давление на быстрый старт",
                "Все перечисленное"
            ],
            correct: 3,
            explanation: "Все эти признаки характерны для мошеннических инвестиционных предложений. Легальные инвестиции всегда связаны с рисками."
        },
        {
            question: "Куда обращаться, если оформили кредит на ваше имя без вашего ведома?",
            options: [
                "Только в полицию",
                "В банк и в полицию одновременно",
                "В службу безопасности банка",
                "Никуда, нужно платить"
            ],
            correct: 1,
            explanation: "Нужно одновременно писать заявление в банк о несогласии с кредитом и в полицию о мошенничестве."
        }
    ];
    
    // Отображение теста
    showPage('test');
    document.getElementById('testContent').innerHTML = `
        <div class="test-container">
            <h3>Тест: Финансовое мошенничество</h3>
            <div class="progress-container">
                <div class="progress-label">
                    <span>Вопрос <span id="currentQuestion">1</span> из 10</span>
                    <span id="progressPercent">0%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" id="testProgressBar" style="width: 0%;"></div>
                </div>
            </div>
            
            <div id="testQuestionContainer">
                <!-- Вопросы будут загружаться динамически -->
            </div>
            
            <div id="testResult" style="display: none;">
                <!-- Результаты теста -->
            </div>
        </div>
    `;
    
    // Запуск теста
    startTestSession('financial', testQuestions);
}
// Функция запуска теста по паролям
function startPasswordsTest() {
// ПРОКРУТКА ВВЕРХ
    scrollToTop();
    // Показываем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // Инициализируем вопросы теста
    passwordsTestQuestions = [
        {
            question: "Какова минимальная рекомендуемая длина пароля?",
            options: [
                "6 символов",
                "8 символов",
                "12 символов",
                "16 символов"
            ],
            correctAnswer: 2,
            explanation: "Минимальная рекомендуемая длина пароля — 12 символов. Это усложняет перебор и делает словарные атаки менее эффективными."
        },
        {
            question: "Что такое фишинг в контексте безопасности паролей?",
            options: [
                "Метод перебора всех возможных комбинаций",
                "Обман пользователя для получения пароля",
                "Использование украденных паролей из баз данных",
                "Взлом пароля через уязвимости в программном обеспечении"
            ],
            correctAnswer: 1,
            explanation: "Фишинг — это социальная инженерия, когда мошенники обманывают пользователей, заставляя их добровольно отдать пароли через поддельные сайты или сообщения."
        },
        {
            question: "Какое главное преимущество менеджера паролей?",
            options: [
                "Он автоматически меняет пароли",
                "Позволяет использовать один пароль для всех сайтов",
                "Позволяет использовать уникальные сложные пароли для каждого сайта",
                "Блокирует фишинговые сайты"
            ],
            correctAnswer: 2,
            explanation: "Главное преимущество менеджера паролей — возможность использовать уникальные сложные пароли для каждого сайта без необходимости их запоминать."
        },
        {
            question: "Что из перечисленного НЕ является фактором аутентификации?",
            options: [
                "Что вы знаете (пароль)",
                "Что у вас есть (телефон)",
                "Кто вы знаете (друзья)",
                "Что вы есть (отпечаток пальца)"
            ],
            correctAnswer: 2,
            explanation: "Три фактора аутентификации: 1) Что вы знаете (пароль), 2) Что у вас есть (токен, телефон), 3) Что вы есть (биометрия). 'Кто вы знаете' не является фактором аутентификации."
        },
        {
            question: "Почему SMS-коды менее безопасны, чем приложения для 2FA?",
            options: [
                "SMS-коды можно перехватить",
                "Приложения работают без интернета",
                "SMS могут быть перенаправлены через SIM-своп",
                "Все ответы верны"
            ],
            correctAnswer: 3,
            explanation: "Все ответы верны. SMS-коды можно перехватить, они требуют сетевого покрытия, и возможен SIM-своп. Приложения-аутентификаторы генерируют коды локально и более безопасны."
        },
        {
            question: "Какой пароль самый надежный?",
            options: [
                "P@ssw0rd",
                "qwerty123456",
                "CorrectHorseBatteryStaple",
                "J4fS<28%5f#p@L"
            ],
            correctAnswer: 3,
            explanation: "J4fS<2'8%5f#p@L — самый надежный, так как он длинный (16 символов), содержит все типы символов и полностью случайный. Длинные фразы тоже хороши, но случайные символы лучше."
        },
        {
            question: "Что делать, если вы подозреваете, что ваш пароль скомпрометирован?",
            options: [
                "Немедленно сменить его на всех сайтах, где он использовался",
                "Подождать, пока произойдет взлом",
                "Сообщить в полицию",
                "Ничего, если деньги еще не украли"
            ],
            correctAnswer: 0,
            explanation: "При подозрении на компрометацию пароля нужно немедленно сменить его на всех сайтах, где он использовался, и включить двухфакторную аутентификацию."
        },
        {
            question: "Что такое 'соль' в контексте хеширования паролей?",
            options: [
                "Специальный алгоритм шифрования",
                "Случайные данные, добавляемые к паролю перед хешированием",
                "Метод восстановления пароля",
                "Тип менеджера паролей"
            ],
            correctAnswer: 1,
            explanation: "Соль — это случайные данные, добавляемые к паролю перед хешированием. Это предотвращает использование радужных таблиц для взлома одинаковых паролей."
        },
        {
            question: "Почему не рекомендуется часто менять пароли?",
            options: [
                "Это неудобно для пользователей",
                "Приводит к использованию слабых паролей и их записыванию",
                "Не повышает безопасность",
                "Все ответы верны"
            ],
            correctAnswer: 3,
            explanation: "Все ответы верны. Частая смена паролей неудобна, приводит к использованию слабых паролей и их записи на бумаге, и исследования показывают, что это не повышает безопасность."
        },
        {
            question: "Какой метод двухфакторной аутентификации самый безопасный?",
            options: [
                "SMS-коды",
                "Приложения-аутентификаторы",
                "Аппаратные ключи безопасности (YubiKey)",
                "Контрольные вопросы"
            ],
            correctAnswer: 2,
            explanation: "Аппаратные ключи безопасности (YubiKey) — самый безопасный метод 2FA, так как они устойчивы к фишингу и требуют физического присутствия устройства."
        },
        {
            question: "Что такое 'радужная таблица' в контексте взлома паролей?",
            options: [
                "Таблица цветовых кодов для CAPTCHA",
                "Предварительно вычисленные хеши паролей",
                "Метод социальной инженерии",
                "Интерфейс менеджера паролей"
            ],
            correctAnswer: 1,
            explanation: "Радужная таблица — это предварительно вычисленные хеши для большого количества паролей, что позволяет быстро находить соответствия при взломе. Использование 'соли' защищает от таких таблиц."
        },
        {
            question: "Почему важно использовать разные пароли для разных сервисов?",
            options: [
                "Чтобы усложнить жизнь хакерам",
                "Чтобы при утечке одного пароля не были скомпрометированы все аккаунты",
                "Это требование большинства сайтов",
                "Чтобы менеджер паролей работал эффективнее"
            ],
            correctAnswer: 1,
            explanation: "Использование разных паролей для разных сервисов предотвращает компрометацию всех аккаунтов при утечке одного пароля (например, при взломе какого-либо сайта)."
        },
        {
            question: "Что такое PAM-система?",
            options: [
                "Personal Access Manager — личный менеджер доступа",
                "Privileged Access Management — управление привилегированным доступом",
                "Password Authentication Method — метод аутентификации паролем",
                "Protected Account Manager — защищенный менеджер аккаунтов"
            ],
            correctAnswer: 1,
            explanation: "PAM — Privileged Access Management, системы управления привилегированным доступом. Они используются в организациях для контроля доступа к критическим системам и аккаунтам."
        },
        {
            question: "Какой из этих паролей НЕЛЬЗЯ использовать?",
            options: [
                "Winter2024!",
                "CompanyName123",
                "Администратор",
                "Все перечисленные"
            ],
            correctAnswer: 3,
            explanation: "Все перечисленные пароли использовать нельзя. Они содержат предсказуемую информацию: сезоны, названия компаний, стандартные слова. Такие пароли легко взломать."
        },
        {
            question: "Что делать с резервными кодами 2FA?",
            options: [
                "Хранить в том же менеджере паролей",
                "Распечатать и хранить в безопасном месте",
                "Отправить себе на email",
                "Запомнить"
            ],
            correctAnswer: 1,
            explanation: "Резервные коды 2FA нужно распечатать и хранить в безопасном физическом месте (сейф, запертый ящик). Хранение в цифровом виде снижает безопасность."
        }
    ];
    
    // Сбрасываем данные теста
    passwordsCurrentQuestion = 0;
    passwordsUserAnswers = [];
    passwordsTestStartTime = new Date();
    
    // Загружаем страницу теста
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon passwords">
                <i class="fas fa-key"></i>
            </div>
            <div class="course-header-content">
                <h1>Итоговый тест: Пароли и аутентификация</h1>
                <p>Проверьте свои знания по пройденному материалу. 15 вопросов, для успешного прохождения нужно правильно ответить на 12 вопросов (80%).</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-question-circle"></i>
                        <span>15 вопросов</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>30 минут</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Проходной балл: 80%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="passwordsTestContainer">
            <div id="passwordsTestInstructions" style="text-align: center; padding: 40px 0;">
                <h3>Инструкция к тесту</h3>
                <p style="margin: 20px 0;">Тест состоит из 15 вопросов с одним правильным ответом.</p>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; max-width: 600px; margin: 0 auto;">
                    <h4><i class="fas fa-info-circle icon" style="color: #8e24aa;"></i> Правила тестирования:</h4>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Выберите один вариант ответа на каждый вопрос</li>
                        <li>Можно вернуться к предыдущим вопросам</li>
                        <li>На прохождение теста отводится 30 минут</li>
                        <li>После завершения вы увидите детальный результат</li>
                        <li>Для успешного прохождения нужно ≥ 80% правильных ответов</li>
                    </ul>
                </div>
                
                <button class="btn btn-large btn-success" onclick="beginPasswordsTest()" style="margin-top: 30px;">
                    <i class="fas fa-play icon"></i> Начать тест
                </button>
                
                <button class="btn btn-large btn-outline" onclick="showPage('courses')" style="margin-top: 30px; margin-left: 15px;">
                    <i class="fas fa-arrow-left icon"></i> Вернуться к курсам
                </button>
            </div>
            
            <div id="passwordsTestQuestions" style="display: none;">
                <!-- Вопросы будут загружены динамически -->
            </div>
            
            <div id="passwordsTestResults" style="display: none;">
                <!-- Результаты будут загружены динамически -->
            </div>
        </div>
    `;
}

// Добавить глобальные переменные для теста
let passwordsTestQuestions = [];
let passwordsCurrentQuestion = 0;
let passwordsUserAnswers = [];
let passwordsTestStartTime = null;
let passwordsTestTimer = null;

// Функция для начала теста
function beginPasswordsTest() {
    // Скрываем инструкции и показываем вопросы
    document.getElementById('passwordsTestInstructions').style.display = 'none';
    document.getElementById('passwordsTestQuestions').style.display = 'block';
    
    // Запускаем таймер
    startPasswordsTestTimer();
    
    // Загружаем первый вопрос
    loadPasswordsTestQuestion();
}

// Функция для загрузки вопроса
function loadPasswordsTestQuestion() {
    const testQuestionsDiv = document.getElementById('passwordsTestQuestions');
    const question = passwordsTestQuestions[passwordsCurrentQuestion];
    
    testQuestionsDiv.innerHTML = `
        <div class="simulator">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h3>Вопрос ${passwordsCurrentQuestion + 1} из ${passwordsTestQuestions.length}</h3>
                <div id="passwordsTestTimer" style="background-color: #f5f5f5; padding: 8px 15px; border-radius: 20px; font-weight: bold;">
                    <i class="fas fa-clock icon"></i> <span id="passwordsTimeRemaining">30:00</span>
                </div>
            </div>
            
            <div style="background-color: #f8f9fa; padding: 25px; border-radius: 10px; margin-bottom: 25px;">
                <h4 style="color: #8e24aa; margin-bottom: 15px;">${question.question}</h4>
            </div>
            
            <div class="options">
                ${question.options.map((option, index) => `
                    <div class="option" onclick="selectPasswordsTestAnswer(${index})" 
                         style="${passwordsUserAnswers[passwordsCurrentQuestion] === index ? 'border-color: #8e24aa; background-color: #f3e5f5;' : ''}">
                        ${String.fromCharCode(65 + index)}. ${option}
                    </div>
                `).join('')}
            </div>
            
            <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 30px;">
    ${passwordsCurrentQuestion > 0 ? `
        <button class="btn btn-outline" onclick="prevPasswordsTestQuestion()" style="padding: 8px 20px;">
            <i class="fas fa-arrow-left icon"></i> Назад
        </button>
    ` : '<div style="width: 100px;"></div>'}
    
    <div style="text-align: center;">
        <button class="btn btn-success" onclick="nextPasswordsTestQuestion()" id="passwordsNextButton" 
                ${passwordsUserAnswers[passwordsCurrentQuestion] === undefined ? 'disabled' : ''}
                style="padding: 8px 25px;">
            ${passwordsCurrentQuestion === passwordsTestQuestions.length - 1 ? 'Завершить тест' : 'Следующий вопрос'} 
            <i class="fas fa-arrow-right icon"></i>
        </button>
        <p style="margin-top: 8px; color: #666; font-size: 0.85rem;">
            Вопрос ${passwordsCurrentQuestion + 1} из ${passwordsTestQuestions.length}
        </p>
    </div>
    
    <div style="text-align: right;">
        <button class="btn btn-danger" onclick="cancelPasswordsTest()" style="padding: 8px 20px;">
            <i class="fas fa-times icon"></i> Отменить
        </button>
    </div>
</div>
            
            <div style="margin-top: 20px; text-align: center; color: #666;">
                <p><i class="fas fa-info-circle icon"></i> Выберите один вариант ответа</p>
            </div>
        </div>
    `;
}

// Функция выбора ответа
function selectPasswordsTestAnswer(answerIndex) {
    // Убираем выделение со всех вариантов
    document.querySelectorAll('#passwordsTestQuestions .option').forEach(option => {
        option.style.borderColor = '#ddd';
        option.style.backgroundColor = 'white';
    });
    
    // Выделяем выбранный вариант
    event.target.style.borderColor = '#8e24aa';
    event.target.style.backgroundColor = '#f3e5f5';
    
    // Сохраняем ответ
    passwordsUserAnswers[passwordsCurrentQuestion] = answerIndex;
    
    // Активируем кнопку "Далее"
    document.getElementById('passwordsNextButton').disabled = false;
}

// Функция для перехода к следующему вопросу
function nextPasswordsTestQuestion() {
    // Проверяем, выбран ли ответ
    if (passwordsUserAnswers[passwordsCurrentQuestion] === undefined) {
        showNotification('error', 'Пожалуйста, выберите вариант ответа');
        return;
    }
    
    // Переходим к следующему вопросу или завершаем тест
    if (passwordsCurrentQuestion < passwordsTestQuestions.length - 1) {
        passwordsCurrentQuestion++;
        loadPasswordsTestQuestion();
    } else {
        finishPasswordsTest();
    }
}

// Функция для возврата к предыдущему вопросу
function prevPasswordsTestQuestion() {
    if (passwordsCurrentQuestion > 0) {
        passwordsCurrentQuestion--;
        loadPasswordsTestQuestion();
    }
}

// Функция запуска таймера теста
function startPasswordsTestTimer() {
    let timeLeft = 30 * 60; // 30 минут в секундах
    
    passwordsTestTimer = setInterval(function() {
        timeLeft--;
        
        const minutes = Math.floor(timeLeft / 60);
        const seconds = timeLeft % 60;
        
        document.getElementById('passwordsTimeRemaining').textContent = 
            `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        
        // Меняем цвет при малом остатке времени
        if (timeLeft < 300) { // Меньше 5 минут
            document.getElementById('passwordsTestTimer').style.backgroundColor = '#ffebee';
            document.getElementById('passwordsTestTimer').style.color = '#d32f2f';
        }
        
        if (timeLeft <= 0) {
            clearInterval(passwordsTestTimer);
            finishPasswordsTest();
        }
    }, 1000);
}

// Функция завершения теста
function finishPasswordsTest() {
    clearInterval(passwordsTestTimer);
    
    // Рассчитываем результаты
    let correctAnswers = 0;
    let resultsHTML = '';
    
    passwordsTestQuestions.forEach((question, index) => {
        const userAnswer = passwordsUserAnswers[index];
        const isCorrect = userAnswer === question.correctAnswer;
        
        if (isCorrect) correctAnswers++;
        
        resultsHTML += `
            <div style="margin-bottom: 20px; padding: 15px; border-radius: 8px; background-color: ${isCorrect ? '#e8f5e9' : '#ffebee'}; border-left: 5px solid ${isCorrect ? '#388e3c' : '#d32f2f'};">
                <p><strong>Вопрос ${index + 1}:</strong> ${question.question}</p>
                <p><strong>Ваш ответ:</strong> ${userAnswer !== undefined ? question.options[userAnswer] : 'Не ответили'}</p>
                <p><strong>Правильный ответ:</strong> ${question.options[question.correctAnswer]}</p>
                <p style="margin-top: 10px; color: #666;"><i class="fas fa-info-circle icon"></i> ${question.explanation}</p>
            </div>
        `;
    });
    
    const score = Math.round((correctAnswers / passwordsTestQuestions.length) * 100);
    const isPassed = score >= 80;
    
    // Обновляем прогресс пользователя
    if (currentUser && isPassed) {
        // Отмечаем тест как пройденный
        if (!currentUser.completedCourses) currentUser.completedCourses = [];
        if (!currentUser.completedCourses.includes('passwords')) {
            currentUser.completedCourses.push('passwords');
        }
        
        // Обновляем прогресс курса
        currentUser.progress.passwords = 100;
        currentUser.stats.completedLessons++;
        currentUser.stats.score += 50; // Бонус за прохождение теста
        currentUser.stats.testResults.push({
            course: 'passwords',
            score: score,
            date: new Date().toISOString()
        });
        
        updateUserInStorage();
    }
    
    // Показываем результаты
    document.getElementById('passwordsTestQuestions').style.display = 'none';
    document.getElementById('passwordsTestResults').style.display = 'block';
    document.getElementById('passwordsTestResults').innerHTML = `
        <div class="simulator" style="text-align: center;">
            <h3>Результаты теста</h3>
            
            <div style="margin: 30px 0;">
                <div style="font-size: 3rem; color: ${isPassed ? '#388e3c' : '#d32f2f'}; margin-bottom: 10px;">
                    ${score}%
                </div>
                <div style="font-size: 1.2rem; margin-bottom: 20px;">
                    ${correctAnswers} из ${passwordsTestQuestions.length} правильных ответов
                </div>
                
                <div style="background-color: ${isPassed ? '#e8f5e9' : '#ffebee'}; padding: 20px; border-radius: 10px; max-width: 500px; margin: 0 auto;">
                    <h4 style="color: ${isPassed ? '#388e3c' : '#d32f2f'};">
                        <i class="fas ${isPassed ? 'fa-check-circle' : 'fa-times-circle'} icon"></i>
                        ${isPassed ? 'Тест пройден успешно!' : 'Тест не пройден'}
                    </h4>
                    <p>Для успешного прохождения необходимо набрать 80% правильных ответов.</p>
                </div>
            </div>
            
            ${isPassed ? `
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-trophy icon" style="color: #ff9800;"></i> Поздравляем!</h4>
                    <p>Вы успешно прошли курс "Пароли и аутентификация" и получили +50 очков к вашему рейтингу.</p>
                    ${currentUser ? `
                        <p style="margin-top: 10px;">Ваш текущий счет: <strong>${currentUser.stats.score} очков</strong></p>
                    ` : ''}
                </div>
            ` : `
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-redo icon" style="color: #1976d2;"></i> Рекомендации</h4>
                    <p>Рекомендуем повторить материал курса и пройти тест снова.</p>
                    <p>Обратите особое внимание на вопросы, в которых допустили ошибки.</p>
                </div>
            `}
            
            <h4 style="margin-top: 30px; margin-bottom: 20px;">Детализация ответов:</h4>
            <div style="max-height: 400px; overflow-y: auto; padding-right: 10px;">
                ${resultsHTML}
            </div>
            
            <div style="margin-top: 30px;">
                <button class="btn btn-large ${isPassed ? 'btn-success' : 'btn-warning'}" onclick="${isPassed ? 'showPage(\'courses\')' : 'retryPasswordsTest()'}">
                    ${isPassed ? 'Вернуться к курсам' : 'Попробовать снова'}
                </button>
                
                ${isPassed ? `
                    <button class="btn btn-large btn-outline" onclick="downloadPasswordsCertificate()" style="margin-left: 15px;">
                        <i class="fas fa-download icon"></i> Скачать сертификат
                    </button>
                ` : ''}
            </div>
        </div>
    `;
    
    // Прокручиваем к результатам
    document.getElementById('passwordsTestResults').scrollIntoView({ behavior: 'smooth' });
}

// Функция повторного прохождения теста
function retryPasswordsTest() {
    passwordsCurrentQuestion = 0;
    passwordsUserAnswers = [];
    
    document.getElementById('passwordsTestResults').style.display = 'none';
    document.getElementById('passwordsTestQuestions').style.display = 'block';
    
    passwordsTestStartTime = new Date();
    startPasswordsTestTimer();
    loadPasswordsTestQuestion();
}

// Функция отмены теста
function cancelPasswordsTest() {
    if (confirm('Вы уверены, что хотите отменить тест? Все ответы будут потеряны.')) {
        clearInterval(passwordsTestTimer);
        showPage('courses');
    }
}

// Функция "скачивания" сертификата
function downloadPasswordsCertificate() {
    showNotification('success', 'Сертификат успешно сгенерирован! В полной версии здесь будет ссылка для скачивания.');
    
    const certificateContent = `
        <div style="text-align: center; padding: 40px; background-color: white; border: 10px solid #8e24aa; max-width: 800px; margin: 0 auto;">
            <h1 style="color: #8e24aa;">СЕРТИФИКАТ</h1>
            <p style="font-size: 1.2rem;">Настоящий сертификат подтверждает, что</p>
            <h2 style="color: #7b1fa2; margin: 20px 0;">${currentUser ? currentUser.name : 'Студент'}</h2>
            <p style="font-size: 1.2rem;">успешно прошел(а) курс</p>
            <h3 style="color: #8e24aa; margin: 20px 0;">"Пароли и аутентификация"</h3>
            <p>в Академии Кибербезопасности</p>
            <div style="margin: 30px 0;">
                <p>Дата: ${new Date().toLocaleDateString('ru-RU')}</p>
                <p>Результат теста: ${Math.round((passwordsUserAnswers.filter((answer, index) => answer === passwordsTestQuestions[index].correctAnswer).length / passwordsTestQuestions.length) * 100)}%</p>
            </div>
            <div style="margin-top: 50px;">
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Директор Академии</p>
                    <p>___________________</p>
                </div>
                <div style="display: inline-block; margin: 0 40px;">
                    <p>Руководитель курса</p>
                    <p>___________________</p>
                </div>
            </div>
        </div>
    `;
    
    setTimeout(() => {
        if (confirm('Хотите увидеть предварительный просмотр сертификата?')) {
            const win = window.open();
            win.document.write(certificateContent);
            win.document.title = 'Сертификат - Пароли и аутентификация';
        }
    }, 500);
}

// ============================
// ТЕСТ: ПУУ СХЕМЫ И СЛОЖНЫЕ АТАКИ (15 вопросов)
// ============================
// ИСПОЛЬЗУЕМ СУЩЕСТВУЮЩИЕ ГЛОБАЛЬНЫЕ ПЕРЕМЕННЫЕ:
// puuTestQuestions, puuCurrentQuestion, puuUserAnswers, puuTestStartTime, puuTestTimer

// Функция запуска теста по ПУУ
function startPuuTest() {
// ПРОКРУТКА ВВЕРХ
    scrollToTop();
    // Показываем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // ИНИЦИАЛИЗАЦИЯ ВОПРОСОВ ТЕСТА (15 штук)
    puuTestQuestions = [
        {
            question: "Что означает аббревиатура ПУУ в контексте кибербезопасности?",
            options: [
                "Программа Управления Устройствами",
                "Программа Удаленного Управления",
                "Правила Учета Угроз",
                "Платформа Универсальной Уязвимости"
            ],
            correctAnswer: 1,
            explanation: "ПУУ — Программа Удаленного Управления. Мошенники используют легитимные программы (AnyDesk, TeamViewer, Ammyy Admin) для получения контроля над устройствами жертв."
        },
        {
            question: "Какая компания НИКОГДА не звонит пользователям с сообщениями о вирусах на компьютере?",
            options: [
                "Лаборатория Касперского",
                "Microsoft",
                "Dr.Web",
                "Все перечисленные"
            ],
            correctAnswer: 3,
            explanation: "Ни одна уважающая себя IT-компания не звонит пользователям с непрошеными предложениями 'помощи'. Microsoft, Apple, Google и антивирусные компании никогда так не делают."
        },
        {
            question: "Какой из этих номеров телефона наиболее подозрителен при звонке от 'службы безопасности банка'?",
            options: [
                "8-800-555-55-50",
                "+7 (495) 500-55-50",
                "+7 900 123-45-67",
                "8-495-500-00-00"
            ],
            correctAnswer: 2,
            explanation: "Служба безопасности банка никогда не звонит с мобильных номеров. Официальные звонки осуществляются с городских или бесплатных номеров, указанных на сайте банка."
        },
        {
            question: "Что такое 'социальная инженерия' в контексте ПУУ-атак?",
            options: [
                "Взлом паролей с помощью специальных программ",
                "Психологическое манипулирование человеком для получения доступа к данным",
                "Инженерный анализ социальных сетей",
                "Разработка антивирусного ПО"
            ],
            correctAnswer: 1,
            explanation: "Социальная инженерия — это метод психологического манипулирования, при котором мошенники заставляют человека добровольно совершить нужное действие (установить программу, назвать пароль, перевести деньги)."
        },
        {
            question: "Какой главный признак того, что к вашему компьютеру подключились удаленно?",
            options: [
                "Появились новые файлы на рабочем столе",
                "Курсор мыши двигается сам по себе",
                "Компьютер стал медленно работать",
                "Пропал интернет"
            ],
            correctAnswer: 1,
            explanation: "Самый явный признак удаленного подключения — курсор двигается сам, программы открываются и закрываются без вашего участия. В этом случае нужно немедленно отключить интернет."
        },
        {
            question: "Какую программу НЕЛЬЗЯ устанавливать по просьбе звонящего 'специалиста'?",
            options: [
                "Adobe Reader",
                "Google Chrome",
                "AnyDesk",
                "VLC Media Player"
            ],
            correctAnswer: 2,
            explanation: "AnyDesk, TeamViewer, Ammyy Admin, UltraVNC — программы удаленного доступа. Их установка по просьбе незнакомца дает мошенникам полный контроль над вашим компьютером."
        },
        {
            question: "Что делать, если мошенник уже подключился к вашему компьютеру через AnyDesk?",
            options: [
                "Попытаться закрыть программу мышкой",
                "Немедленно выдернуть кабель интернета/отключить Wi-Fi",
                "Позвонить в полицию с этого же компьютера",
                "Начать диалог и выяснять, кто это"
            ],
            correctAnswer: 1,
            explanation: "При подозрении на удаленное подключение нужно немедленно физически отключить интернет. Это разорвет связь и прекратит доступ. Только после этого можно звонить в банк и полицию."
        },
        {
            question: "Какой психологический прием чаще всего используют ПУУ-мошенники?",
            options: [
                "Предложение легкого заработка",
                "Создание искусственной срочности и страха",
                "Флирт и романтические отношения",
                "Обещание крупного выигрыша"
            ],
            correctAnswer: 1,
            explanation: "Главное оружие ПУУ-мошенников — срочность и страх: 'Ваш компьютер заражен!', 'Деньги украдут через 5 минут!', 'Вас уже взломали!'. Это отключает рациональное мышление."
        },
        {
            question: "Что такое 'спуфинг' в телефонном мошенничестве?",
            options: [
                "Запись разговора с жертвой",
                "Использование нескольких SIM-карт",
                "Подмена номера телефона",
                "Звонки через мессенджеры"
            ],
            correctAnswer: 2,
            explanation: "Спуфинг — это технология подмены номера. Мошенник может звонить с номера, который на экране отображается как номер вашего банка, хотя на самом деле звонок идет из другого места."
        },
        {
            question: "Почему мошенники просят установить программу удаленного доступа?",
            options: [
                "Чтобы удалить вирусы с вашего компьютера",
                "Чтобы настроить антивирус",
                "Чтобы получить полный контроль над устройством и видеть все ваши действия",
                "Чтобы ускорить работу компьютера"
            ],
            correctAnswer: 2,
            explanation: "Получив удаленный доступ, мошенник видит все, что вы делаете: вводите пароли, заходите в онлайн-банк, просматриваете почту. Это позволяет им красть данные в реальном времени."
        },
        {
            question: "Какой из этих диалогов явно указывает на ПУУ-мошенника?",
            options: [
                "— Здравствуйте, это служба доставки. Ваш заказ прибудет завтра.",
                "— Здравствуйте, это техподдержка Microsoft. На вашем компьютере вирус. Откройте сайт anydesk.com и скачайте программу.",
                "— Здравствуйте, это служба безопасности банка. Не было ли у вас операций на 5000 рублей сегодня?",
                "— Здравствуйте, мы проводим опрос населения. Не могли бы вы уделить 5 минут?"
            ],
            correctAnswer: 1,
            explanation: "Microsoft никогда не звонит пользователям. Требование установить AnyDesk/TeamViewer — 100% признак мошенничества. Настоящие IT-специалисты работают в сервисных центрах, куда вы обращаетесь сами."
        },
        {
            question: "Что делать, если вам звонят и представляются 'сотрудником ФСБ' или 'полицией', требуя перевести деньги на 'безопасный счет'?",
            options: [
                "Выполнить требования, чтобы избежать проблем",
                "Положить трубку и сообщить в полицию по номеру 102 или 112",
                "Попросить прислать официальное уведомление на email",
                "Договориться о встрече в отделении"
            ],
            correctAnswer: 1,
            explanation: "Правоохранительные органы никогда не звонят с требованиями перевода денег. Это 100% мошенничество. Нужно немедленно положить трубку и сообщить о звонке в настоящую полицию."
        },
        {
            question: "Что НЕЛЬЗЯ делать, если вы уже сообщили мошенникам данные карты?",
            options: [
                "Немедленно позвонить в банк и заблокировать карту",
                "Подать заявление в полицию",
                "Продолжать разговор с мошенниками, пытаясь их переубедить",
                "Сменить пароли от онлайн-банка"
            ],
            correctAnswer: 2,
            explanation: "Ни в коем случае нельзя продолжать разговор. Мошенники будут давить и запугивать, чтобы получить еще больше информации. Просто положите трубку и действуйте по алгоритму: банк → полиция."
        },
        {
            question: "Какой самый надежный способ проверить, звонит ли реальный сотрудник банка?",
            options: [
                "Попросить его назвать ваши паспортные данные",
                "Перезвонить по номеру с обратной стороны вашей карты",
                "Перевести 1 рубль на проверочный счет",
                "Назвать ему код из SMS для проверки"
            ],
            correctAnswer: 1,
            explanation: "Единственный надежный способ — не общаться по входящему звонку, а перезвонить самостоятельно по официальному номеру. На карте, на сайте банка, в мобильном приложении."
        },
        {
            question: "Что делать, если мошенники угрожают, что 'заблокируют ваш паспорт' или 'возбудят уголовное дело'?",
            options: [
                "Выполнить все требования, чтобы избежать проблем",
                "Положить трубку — это ложные угрозы, паспорт нельзя 'заблокировать' по телефону",
                "Попросить их прислать официальные документы",
                "Начать оправдываться и доказывать свою невиновность"
            ],
            correctAnswer: 1,
            explanation: "Это классические угрозы мошенников. Паспорт — документ, удостоверяющий личность. Его нельзя 'заблокировать', 'аннулировать' или 'арестовать' по телефону. Это физический документ. Положите трубку."
        }
    ];
    
    // Сбрасываем данные теста — ИСПОЛЬЗУЕМ СУЩЕСТВУЮЩИЕ ПЕРЕМЕННЫЕ
    puuCurrentQuestion = 0;
    puuUserAnswers = [];
    puuTestStartTime = new Date();
    
    // Загружаем страницу теста
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon puu">
                <i class="fas fa-laptop-code"></i>
            </div>
            <div class="course-header-content">
                <h1>Итоговый тест: ПУУ схемы и сложные атаки</h1>
                <p>Проверьте свои знания по пройденному материалу. 15 вопросов, для успешного прохождения нужно правильно ответить на 12 вопросов (80%).</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-question-circle"></i>
                        <span>15 вопросов</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>30 минут</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Проходной балл: 80%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="puuTestContainer">
            <div id="puuTestInstructions" style="text-align: center; padding: 40px 0;">
                <h3>Инструкция к тесту</h3>
                <p style="margin: 20px 0;">Тест состоит из 15 вопросов с одним правильным ответом.</p>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; max-width: 600px; margin: 0 auto;">
                    <h4><i class="fas fa-info-circle icon" style="color: #43a047;"></i> Правила тестирования:</h4>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Выберите один вариант ответа на каждый вопрос</li>
                        <li>Можно вернуться к предыдущим вопросам</li>
                        <li>На прохождение теста отводится 30 минут</li>
                        <li>После завершения вы увидите детальный результат с объяснениями</li>
                        <li>Для успешного прохождения нужно ≥ 80% правильных ответов (12 из 15)</li>
                    </ul>
                </div>
                
                <button class="btn btn-large btn-success" onclick="beginPuuTest()" style="margin-top: 30px;">
                    <i class="fas fa-play icon"></i> Начать тест
                </button>
                
                <button class="btn btn-large btn-outline" onclick="showPage('courses')" style="margin-top: 30px; margin-left: 15px;">
                    <i class="fas fa-arrow-left icon"></i> Вернуться к курсам
                </button>
            </div>
            
            <div id="puuTestQuestions" style="display: none;">
                <!-- Вопросы будут загружены динамически -->
            </div>
            
            <div id="puuTestResults" style="display: none;">
                <!-- Результаты будут загружены динамически -->
            </div>
        </div>
    `;
}

// Функция для начала теста
function beginPuuTest() {
    // Скрываем инструкции и показываем вопросы
    document.getElementById('puuTestInstructions').style.display = 'none';
    document.getElementById('puuTestQuestions').style.display = 'block';
    
    // Запускаем таймер
    startPuuTestTimer();
    
    // Загружаем первый вопрос
    loadPuuTestQuestion();
}

// Функция для загрузки вопроса
function loadPuuTestQuestion() {
    const testQuestionsDiv = document.getElementById('puuTestQuestions');
    const question = puuTestQuestions[puuCurrentQuestion];
    
    testQuestionsDiv.innerHTML = `
        <div class="simulator">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h3>Вопрос ${puuCurrentQuestion + 1} из ${puuTestQuestions.length}</h3>
                <div id="puuTestTimer" style="background-color: #f5f5f5; padding: 8px 15px; border-radius: 20px; font-weight: bold;">
                    <i class="fas fa-clock icon"></i> <span id="puuTimeRemaining">30:00</span>
                </div>
            </div>
            
            <div style="background-color: #f8f9fa; padding: 25px; border-radius: 10px; margin-bottom: 25px;">
                <h4 style="color: #43a047; margin-bottom: 15px;">${question.question}</h4>
            </div>
            
            <div class="options">
                ${question.options.map((option, index) => `
                    <div class="option" onclick="selectPuuTestAnswer(${index})" 
                         style="${puuUserAnswers[puuCurrentQuestion] === index ? 'border-color: #43a047; background-color: #e8f5e9;' : ''}">
                        ${String.fromCharCode(65 + index)}. ${option}
                    </div>
                `).join('')}
            </div>
            
            <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 30px;">
    ${puuCurrentQuestion > 0 ? `
        <button class="btn btn-outline" onclick="prevPuuTestQuestion()" style="padding: 8px 20px;">
            <i class="fas fa-arrow-left icon"></i> Назад
        </button>
    ` : '<div style="width: 100px;"></div>'}
    
    <div style="text-align: center;">
        <button class="btn btn-success" onclick="nextPuuTestQuestion()" id="puuNextButton" 
                ${puuUserAnswers[puuCurrentQuestion] === undefined ? 'disabled' : ''}
                style="padding: 8px 25px;">
            ${puuCurrentQuestion === puuTestQuestions.length - 1 ? 'Завершить тест' : 'Следующий вопрос'} 
            <i class="fas fa-arrow-right icon"></i>
        </button>
        <p style="margin-top: 8px; color: #666; font-size: 0.85rem;">
            Вопрос ${puuCurrentQuestion + 1} из ${puuTestQuestions.length}
        </p>
    </div>
    
    <div style="text-align: right;">
        <button class="btn btn-danger" onclick="cancelPuuTest()" style="padding: 8px 20px;">
            <i class="fas fa-times icon"></i> Отменить
        </button>
    </div>
</div>
            
            <div style="margin-top: 20px; text-align: center; color: #666;">
                <p><i class="fas fa-info-circle icon"></i> Выберите один вариант ответа</p>
            </div>
        </div>
    `;
}

// Функция выбора ответа
function selectPuuTestAnswer(answerIndex) {
    // Убираем выделение со всех вариантов
    document.querySelectorAll('#puuTestQuestions .option').forEach(option => {
        option.style.borderColor = '#ddd';
        option.style.backgroundColor = 'white';
    });
    
    // Выделяем выбранный вариант
    event.target.style.borderColor = '#43a047';
    event.target.style.backgroundColor = '#e8f5e9';
    
    // Сохраняем ответ — ИСПОЛЬЗУЕМ СУЩЕСТВУЮЩИЙ МАССИВ
    puuUserAnswers[puuCurrentQuestion] = answerIndex;
    
    // Активируем кнопку "Далее"
    document.getElementById('puuNextButton').disabled = false;
}

// Функция для перехода к следующему вопросу
function nextPuuTestQuestion() {
    // Проверяем, выбран ли ответ
    if (puuUserAnswers[puuCurrentQuestion] === undefined) {
        showNotification('error', 'Пожалуйста, выберите вариант ответа');
        return;
    }
    
    // Переходим к следующему вопросу или завершаем тест
    if (puuCurrentQuestion < puuTestQuestions.length - 1) {
        puuCurrentQuestion++;
        loadPuuTestQuestion();
    } else {
        finishPuuTest();
    }
}

// Функция для возврата к предыдущему вопросу
function prevPuuTestQuestion() {
    if (puuCurrentQuestion > 0) {
        puuCurrentQuestion--;
        loadPuuTestQuestion();
    }
}

// Функция запуска таймера теста
function startPuuTestTimer() {
    // Очищаем предыдущий таймер, если был
    if (puuTestTimer) {
        clearInterval(puuTestTimer);
    }
    
    let timeLeft = 30 * 60; // 30 минут в секундах
    
    puuTestTimer = setInterval(function() {
        timeLeft--;
        
        const minutes = Math.floor(timeLeft / 60);
        const seconds = timeLeft % 60;
        
        const timeElement = document.getElementById('puuTimeRemaining');
        if (timeElement) {
            timeElement.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }
        
        // Меняем цвет при малом остатке времени
        const timerDiv = document.getElementById('puuTestTimer');
        if (timerDiv && timeLeft < 300) { // Меньше 5 минут
            timerDiv.style.backgroundColor = '#ffebee';
            timerDiv.style.color = '#d32f2f';
        }
        
        if (timeLeft <= 0) {
            clearInterval(puuTestTimer);
            finishPuuTest();
        }
    }, 1000);
}

// Функция завершения теста
function finishPuuTest() {
    if (puuTestTimer) {
        clearInterval(puuTestTimer);
    }
    
    // Рассчитываем результаты
    let correctAnswers = 0;
    let resultsHTML = '';
    
    puuTestQuestions.forEach((question, index) => {
        const userAnswer = puuUserAnswers[index];
        const isCorrect = userAnswer === question.correctAnswer;
        
        if (isCorrect) correctAnswers++;
        
        resultsHTML += `
            <div style="margin-bottom: 20px; padding: 15px; border-radius: 8px; background-color: ${isCorrect ? '#e8f5e9' : '#ffebee'}; border-left: 5px solid ${isCorrect ? '#388e3c' : '#d32f2f'}; text-align: left;">
                <p><strong>Вопрос ${index + 1}:</strong> ${question.question}</p>
                <p><strong>Ваш ответ:</strong> ${userAnswer !== undefined ? question.options[userAnswer] : 'Не ответили'}</p>
                <p><strong>Правильный ответ:</strong> ${question.options[question.correctAnswer]}</p>
                <p style="margin-top: 10px; color: #666;"><i class="fas fa-info-circle icon"></i> ${question.explanation}</p>
            </div>
        `;
    });
    
    const score = Math.round((correctAnswers / puuTestQuestions.length) * 100);
    const isPassed = score >= 80; // 12 из 15 = 80%
    
    // Обновляем прогресс пользователя
    if (currentUser && isPassed) {
        // Отмечаем тест как пройденный
        if (!currentUser.completedCourses) currentUser.completedCourses = [];
        if (!currentUser.completedCourses.includes('puu')) {
            currentUser.completedCourses.push('puu');
        }
        
        // Обновляем прогресс курса
        if (!currentUser.progress) currentUser.progress = {};
        currentUser.progress.puu = 100;
        
        if (!currentUser.stats) {
            currentUser.stats = {
                completedLessons: 0,
                score: 0,
                testResults: []
            };
        }
        
        currentUser.stats.completedLessons = (currentUser.stats.completedLessons || 0) + 1;
        currentUser.stats.score = (currentUser.stats.score || 0) + 50; // Бонус за прохождение теста
        
        if (!currentUser.stats.testResults) currentUser.stats.testResults = [];
        currentUser.stats.testResults.push({
            course: 'puu',
            score: score,
            date: new Date().toISOString()
        });
        
        updateUserInStorage();
    }
    
    // Показываем результаты
    document.getElementById('puuTestQuestions').style.display = 'none';
    document.getElementById('puuTestResults').style.display = 'block';
    document.getElementById('puuTestResults').innerHTML = `
        <div class="simulator" style="text-align: center;">
            <h3>Результаты теста</h3>
            
            <div style="margin: 30px 0;">
                <div style="font-size: 3rem; color: ${isPassed ? '#388e3c' : '#d32f2f'}; margin-bottom: 10px;">
                    ${score}%
                </div>
                <div style="font-size: 1.2rem; margin-bottom: 20px;">
                    ${correctAnswers} из ${puuTestQuestions.length} правильных ответов
                </div>
                
                <div style="background-color: ${isPassed ? '#e8f5e9' : '#ffebee'}; padding: 20px; border-radius: 10px; max-width: 500px; margin: 0 auto;">
                    <h4 style="color: ${isPassed ? '#388e3c' : '#d32f2f'};">
                        <i class="fas ${isPassed ? 'fa-check-circle' : 'fa-times-circle'} icon"></i>
                        ${isPassed ? 'Тест пройден успешно!' : 'Тест не пройден'}
                    </h4>
                    <p>Для успешного прохождения необходимо набрать 80% правильных ответов (12 из 15).</p>
                </div>
            </div>
            
            ${isPassed ? `
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-trophy icon" style="color: #ff9800;"></i> Поздравляем!</h4>
                    <p>Вы успешно прошли курс "ПУУ схемы и сложные атаки" и получили +50 очков к вашему рейтингу.</p>
                    ${currentUser ? `
                        <p style="margin-top: 10px;">Ваш текущий счет: <strong>${currentUser.stats.score} очков</strong></p>
                    ` : ''}
                </div>
            ` : `
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-redo icon" style="color: #1976d2;"></i> Рекомендации</h4>
                    <p>Рекомендуем повторить материал курса и пройти тест снова.</p>
                    <p>Обратите особое внимание на вопросы, в которых допустили ошибки.</p>
                </div>
            `}
            
            <h4 style="margin-top: 30px; margin-bottom: 20px;">Детализация ответов:</h4>
            <div style="max-height: 400px; overflow-y: auto; padding-right: 10px; text-align: left;">
                ${resultsHTML}
            </div>
            
            <div style="margin-top: 30px;">
                <button class="btn btn-large ${isPassed ? 'btn-success' : 'btn-warning'}" onclick="${isPassed ? 'showPage(\'courses\')' : 'retryPuuTest()'}">
                    ${isPassed ? 'Вернуться к курсам' : 'Попробовать снова'}
                </button>
                
                ${isPassed ? `
                    <button class="btn btn-large btn-outline" onclick="downloadPuuCertificate()" style="margin-left: 15px;">
                        <i class="fas fa-download icon"></i> Скачать сертификат
                    </button>
                ` : ''}
            </div>
        </div>
    `;
    
    // Прокручиваем к результатам
    document.getElementById('puuTestResults').scrollIntoView({ behavior: 'smooth' });
}

// Функция повторного прохождения теста
function retryPuuTest() {
    puuCurrentQuestion = 0;
    puuUserAnswers = [];
    
    document.getElementById('puuTestResults').style.display = 'none';
    document.getElementById('puuTestQuestions').style.display = 'block';
    
    puuTestStartTime = new Date();
    startPuuTestTimer();
    loadPuuTestQuestion();
}

// Функция отмены теста
function cancelPuuTest() {
    if (confirm('Вы уверены, что хотите отменить тест? Все ответы будут потеряны.')) {
        if (puuTestTimer) {
            clearInterval(puuTestTimer);
        }
        showPage('courses');
    }
}

// Функция скачивания сертификата
function downloadPuuCertificate() {
    showNotification('success', 'Сертификат успешно сгенерирован!');
    
    const certificateContent = `
        <div style="text-align: center; padding: 40px; background-color: white; border: 10px solid #43a047; max-width: 800px; margin: 0 auto; font-family: Arial, sans-serif;">
            <h1 style="color: #43a047; font-size: 2.5rem; margin-bottom: 20px;">СЕРТИФИКАТ</h1>
            <p style="font-size: 1.2rem; color: #555;">Настоящий сертификат подтверждает, что</p>
            <h2 style="color: #2e7d32; margin: 20px 0; font-size: 2rem;">${currentUser ? currentUser.name : 'Студент'}</h2>
            <p style="font-size: 1.2rem; color: #555;">успешно прошел(а) курс</p>
            <h3 style="color: #43a047; margin: 20px 0; font-size: 1.8rem;">"ПУУ схемы и сложные атаки"</h3>
            <p style="font-size: 1rem; color: #666;">в Академии Кибербезопасности</p>
            <div style="margin: 30px 0; padding: 20px; background-color: #f9f9f9; border-radius: 10px;">
                <p style="font-size: 1.1rem;"><strong>Дата:</strong> ${new Date().toLocaleDateString('ru-RU')}</p>
                <p style="font-size: 1.1rem;"><strong>Результат теста:</strong> ${Math.round((puuUserAnswers.filter((answer, index) => answer === puuTestQuestions[index].correctAnswer).length / puuTestQuestions.length) * 100)}%</p>
                <p style="font-size: 1.1rem;"><strong>Правильных ответов:</strong> ${puuUserAnswers.filter((answer, index) => answer === puuTestQuestions[index].correctAnswer).length} из 15</p>
            </div>
            <div style="margin-top: 50px; display: flex; justify-content: space-around;">
                <div style="text-align: center;">
                    <p>Директор Академии</p>
                    <p style="margin-top: 40px;">___________________ А.В. Иванов</p>
                </div>
                <div style="text-align: center;">
                    <p>Руководитель курса</p>
                    <p style="margin-top: 40px;">___________________ Е.С. Петрова</p>
                </div>
            </div>
            <div style="margin-top: 40px; color: #999; font-size: 0.9rem;">
                <p>Лицензия на образовательную деятельность № 1234 от 01.01.2026</p>
                <p>ID сертификата: CERT-PUU-${Date.now().toString().slice(-8)}</p>
            </div>
        </div>
    `;
    
    setTimeout(() => {
        if (confirm('Хотите увидеть предварительный просмотр сертификата?')) {
            const win = window.open();
            win.document.write(certificateContent);
            win.document.title = 'Сертификат - ПУУ схемы и сложные атаки';
        }
    }, 500);
}
// Функция запуска теста по соцсетям
function startSocialTest() {
    // ПРОКРУТКА ВВЕРХ
    scrollToTop();
    // Показываем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // ИНИЦИАЛИЗАЦИЯ ВОПРОСОВ ТЕСТА (10 вопросов)
    socialTestQuestions = [
        {
            question: "Что из перечисленного НЕ является признаком фишингового сообщения в социальных сетях?",
            options: [
                "Сообщение от друга с просьбой перейти по подозрительной ссылке",
                "Сообщение о выигрыше в конкурсе, в котором вы не участвовали",
                "Официальное уведомление от администрации с логотипом соцсети в личном кабинете",
                "Срочная просьба о помощи с переводом денег от 'родственника'"
            ],
            correctAnswer: 2,
            explanation: "Официальные уведомления от администрации всегда находятся в специальном разделе настроек или в личном кабинете, а не приходят в личные сообщения от неизвестных аккаунтов с просьбой перейти по ссылке."
        },
        {
            question: "Какую информацию НЕЛЬЗЯ публиковать в открытом доступе в социальных сетях?",
            options: [
                "Фото домашнего питомца",
                "Номер банковской карты и паспортные данные",
                "Фото с отдыха",
                "Свои увлечения и хобби"
            ],
            correctAnswer: 1,
            explanation: "Номер банковской карты и паспортные данные — конфиденциальная информация. Мошенники могут использовать эти данные для кражи денег или оформления кредитов на ваше имя."
        },
        {
            question: "Что такое двухфакторная аутентификация (2FA) в социальных сетях?",
            options: [
                "Возможность войти в аккаунт с двух устройств одновременно",
                "Дополнительная защита, требующая код из SMS или приложения после ввода пароля",
                "Подтверждение возраста при регистрации",
                "Автоматическая публикация постов в двух соцсетях сразу"
            ],
            correctAnswer: 1,
            explanation: "Двухфакторная аутентификация требует не только пароль, но и дополнительный код из SMS, приложения-аутентификатора или аппаратного ключа. Это значительно повышает безопасность аккаунта."
        },
        {
            question: "Какой пароль считается наиболее надежным для социальных сетей?",
            options: [
                "qwerty123",
                "J8#kL!p2qW9*zM5",
                "password2024",
                "Иван1990"
            ],
            correctAnswer: 1,
            explanation: "Надежный пароль должен быть длинным (12+ символов), содержать заглавные и строчные буквы, цифры и специальные символы. Пароль 'J8#kL!p2qW9*zM5' соответствует всем этим требованиям."
        },
        {
            question: "Что нужно сделать при получении заявки в друзья от незнакомого человека?",
            options: [
                "Всегда принимать — чем больше друзей, тем лучше",
                "Проверить профиль: дата регистрации, фото, общие друзья; при подозрениях — отклонить",
                "Обязательно написать ему первым",
                "Переслать заявку всем своим друзьям"
            ],
            correctAnswer: 1,
            explanation: "Всегда проверяйте профиль перед добавлением в друзья. Пустые аккаунты, недавно созданные страницы, отсутствие общих друзей — признаки фейковых аккаунтов, которые используются для фишинга и спама."
        },
        {
            question: "Какие настройки приватности являются наиболее безопасными?",
            options: [
                "Открытый профиль для всех пользователей",
                "Только друзья могут видеть публикации и личную информацию",
                "Друзья друзей могут видеть всё",
                "Полностью закрытый профиль, но фотографии открыты всем"
            ],
            correctAnswer: 1,
            explanation: "Наиболее безопасная настройка — 'Только друзья'. Это ограничивает доступ к вашей личной информации, фотографиям и публикациям только теми, кого вы действительно знаете и кому доверяете."
        },
        {
            question: "Что делать, если вы случайно перешли по фишинговой ссылке и ввели свои данные?",
            options: [
                "Ничего, если деньги сразу не списались",
                "Немедленно сменить пароль и включить двухфакторную аутентификацию",
                "Подождать пару часов — может, само рассосется",
                "Написать гневный комментарий мошенникам"
            ],
            correctAnswer: 1,
            explanation: "При компрометации данных нужно действовать немедленно: сменить пароль, завершить все активные сессии, включить 2FA. Если ввели данные карты — срочно заблокировать карту через банк."
        },
        {
            question: "Какую геолокацию безопаснее всего публиковать в социальных сетях?",
            options: [
                "Отмечаться в аэропорту перед отпуском",
                "Публиковать фото из дома с геометкой",
                "Ставить геометку в ресторане в реальном времени",
                "Не публиковать геолокацию вообще или ставить её уже после посещения места"
            ],
            correctAnswer: 3,
            explanation: "Публикация геолокации в реальном времени показывает мошенникам, что вас нет дома. Лучше либо не публиковать геометки вообще, либо ставить их уже после того, как вы вернулись домой."
        },
        {
            question: "Что такое 'приложения в социальных сетях' и чем они опасны?",
            options: [
                "Это встроенные игры, они всегда безопасны",
                "Сторонние приложения, которые запрашивают доступ к вашему профилю, друзьям, сообщениям — могут собирать данные и рассылать спам",
                "Это официальные приложения соцсетей для телефона",
                "Это рекламные интеграции"
            ],
            correctAnswer: 1,
            explanation: "Сторонние приложения могут запрашивать избыточные разрешения (доступ к друзьям, сообщениям, стене). Регулярно проверяйте список подключенных приложений в настройках и удаляйте неиспользуемые."
        },
        {
            question: "Как распознать фейковый аккаунт знаменитости?",
            options: [
                "У него много подписчиков — значит, настоящий",
                "Проверить верификацию (галочку), дату регистрации, активность, ссылки на официальные сайты",
                "Если аккаунт красиво оформлен — он настоящий",
                "Написать в директ и спросить, настоящий ли это аккаунт"
            ],
            correctAnswer: 1,
            explanation: "Настоящие аккаунты знаменитостей имеют отметку верификации (галочку), официальные ссылки, стабильную активность. Фейки часто созданы недавно, не имеют галочки и пытаются выманить деньги или данные."
        }
    ];
    
    // Сбрасываем данные теста
    socialCurrentQuestion = 0;
    socialUserAnswers = [];
    socialTestStartTime = new Date();
    
    // Загружаем страницу теста
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon social">
                <i class="fas fa-users"></i>
            </div>
            <div class="course-header-content">
                <h1>Итоговый тест: Безопасность в социальных сетях</h1>
                <p>Проверьте свои знания по защите аккаунтов в социальных сетях, настройкам приватности и распознаванию угроз. 10 вопросов, для успешного прохождения нужно правильно ответить на 8 вопросов (80%).</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-question-circle"></i>
                        <span>10 вопросов</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>25 минут</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Проходной балл: 80%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="socialTestContainer">
            <div id="socialTestInstructions" style="text-align: center; padding: 40px 0;">
                <h3>Инструкция к тесту</h3>
                <p style="margin: 20px 0;">Тест состоит из 10 вопросов с одним правильным ответом.</p>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; max-width: 600px; margin: 0 auto;">
                    <h4><i class="fas fa-info-circle icon" style="color: #039be5;"></i> Правила тестирования:</h4>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Выберите один вариант ответа на каждый вопрос</li>
                        <li>Можно вернуться к предыдущим вопросам</li>
                        <li>На прохождение теста отводится 25 минут</li>
                        <li>После завершения вы увидите детальный результат с объяснениями</li>
                        <li>Для успешного прохождения нужно ≥ 80% правильных ответов (8 из 10)</li>
                    </ul>
                </div>
                
                <button class="btn btn-large btn-success" onclick="beginSocialTest()" style="margin-top: 30px;">
                    <i class="fas fa-play icon"></i> Начать тест
                </button>
                
                <button class="btn btn-large btn-outline" onclick="showPage('courses')" style="margin-top: 30px; margin-left: 15px;">
                    <i class="fas fa-arrow-left icon"></i> Вернуться к курсам
                </button>
            </div>
            
            <div id="socialTestQuestions" style="display: none;">
                <!-- Вопросы будут загружены динамически -->
            </div>
            
            <div id="socialTestResults" style="display: none;">
                <!-- Результаты будут загружены динамически -->
            </div>
        </div>
    `;
}

// Функция для начала теста
function beginSocialTest() {
    // Скрываем инструкции и показываем вопросы
    document.getElementById('socialTestInstructions').style.display = 'none';
    document.getElementById('socialTestQuestions').style.display = 'block';
    
    // Запускаем таймер
    startSocialTestTimer();
    
    // Загружаем первый вопрос
    loadSocialTestQuestion();
}

// Функция для загрузки вопроса
function loadSocialTestQuestion() {
    const testQuestionsDiv = document.getElementById('socialTestQuestions');
    const question = socialTestQuestions[socialCurrentQuestion];
    
    testQuestionsDiv.innerHTML = `
        <div class="simulator">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h3>Вопрос ${socialCurrentQuestion + 1} из ${socialTestQuestions.length}</h3>
                <div id="socialTestTimer" style="background-color: #f5f5f5; padding: 8px 15px; border-radius: 20px; font-weight: bold;">
                    <i class="fas fa-clock icon"></i> <span id="socialTimeRemaining">25:00</span>
                </div>
            </div>
            
            <div style="background-color: #f8f9fa; padding: 25px; border-radius: 10px; margin-bottom: 25px;">
                <h4 style="color: #039be5; margin-bottom: 15px;">${question.question}</h4>
            </div>
            
            <div class="options">
                ${question.options.map((option, index) => `
                    <div class="option" onclick="selectSocialTestAnswer(${index})" 
                         style="${socialUserAnswers[socialCurrentQuestion] === index ? 'border-color: #039be5; background-color: #e1f5fe;' : ''}">
                        ${String.fromCharCode(65 + index)}. ${option}
                    </div>
                `).join('')}
            </div>
            
            <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 30px;">
    ${socialCurrentQuestion > 0 ? `
        <button class="btn btn-outline" onclick="prevSocialTestQuestion()" style="padding: 8px 20px;">
            <i class="fas fa-arrow-left icon"></i> Назад
        </button>
    ` : '<div style="width: 100px;"></div>'}
    
    <div style="text-align: center;">
        <button class="btn btn-success" onclick="nextSocialTestQuestion()" id="socialNextButton" 
                ${socialUserAnswers[socialCurrentQuestion] === undefined ? 'disabled' : ''}
                style="padding: 8px 25px;">
            ${socialCurrentQuestion === socialTestQuestions.length - 1 ? 'Завершить тест' : 'Следующий вопрос'} 
            <i class="fas fa-arrow-right icon"></i>
        </button>
        <p style="margin-top: 8px; color: #666; font-size: 0.85rem;">
            Вопрос ${socialCurrentQuestion + 1} из ${socialTestQuestions.length}
        </p>
    </div>
    
    <div style="text-align: right;">
        <button class="btn btn-danger" onclick="cancelSocialTest()" style="padding: 8px 20px;">
            <i class="fas fa-times icon"></i> Отменить
        </button>
    </div>
</div>
            
            <div style="margin-top: 20px; text-align: center; color: #666;">
                <p><i class="fas fa-info-circle icon"></i> Выберите один вариант ответа</p>
            </div>
        </div>
    `;
}

// Функция выбора ответа
function selectSocialTestAnswer(answerIndex) {
    // Убираем выделение со всех вариантов
    document.querySelectorAll('#socialTestQuestions .option').forEach(option => {
        option.style.borderColor = '#ddd';
        option.style.backgroundColor = 'white';
    });
    
    // Выделяем выбранный вариант
    event.target.style.borderColor = '#039be5';
    event.target.style.backgroundColor = '#e1f5fe';
    
    // Сохраняем ответ
    socialUserAnswers[socialCurrentQuestion] = answerIndex;
    
    // Активируем кнопку "Далее"
    document.getElementById('socialNextButton').disabled = false;
}

// Функция для перехода к следующему вопросу
function nextSocialTestQuestion() {
    // Проверяем, выбран ли ответ
    if (socialUserAnswers[socialCurrentQuestion] === undefined) {
        showNotification('error', 'Пожалуйста, выберите вариант ответа');
        return;
    }
    
    // Переходим к следующему вопросу или завершаем тест
    if (socialCurrentQuestion < socialTestQuestions.length - 1) {
        socialCurrentQuestion++;
        loadSocialTestQuestion();
    } else {
        finishSocialTest();
    }
}

// Функция для возврата к предыдущему вопросу
function prevSocialTestQuestion() {
    if (socialCurrentQuestion > 0) {
        socialCurrentQuestion--;
        loadSocialTestQuestion();
    }
}

// Функция запуска таймера теста
function startSocialTestTimer() {
    // Очищаем предыдущий таймер, если был
    if (socialTestTimer) {
        clearInterval(socialTestTimer);
    }
    
    let timeLeft = 25 * 60; // 25 минут в секундах
    
    socialTestTimer = setInterval(function() {
        timeLeft--;
        
        const minutes = Math.floor(timeLeft / 60);
        const seconds = timeLeft % 60;
        
        const timeElement = document.getElementById('socialTimeRemaining');
        if (timeElement) {
            timeElement.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }
        
        // Меняем цвет при малом остатке времени
        const timerDiv = document.getElementById('socialTestTimer');
        if (timerDiv && timeLeft < 300) { // Меньше 5 минут
            timerDiv.style.backgroundColor = '#ffebee';
            timerDiv.style.color = '#d32f2f';
        }
        
        if (timeLeft <= 0) {
            clearInterval(socialTestTimer);
            finishSocialTest();
        }
    }, 1000);
}

// Функция завершения теста
function finishSocialTest() {
    if (socialTestTimer) {
        clearInterval(socialTestTimer);
    }
    
    // Рассчитываем результаты
    let correctAnswers = 0;
    let resultsHTML = '';
    
    socialTestQuestions.forEach((question, index) => {
        const userAnswer = socialUserAnswers[index];
        const isCorrect = userAnswer === question.correctAnswer;
        
        if (isCorrect) correctAnswers++;
        
        resultsHTML += `
            <div style="margin-bottom: 20px; padding: 15px; border-radius: 8px; background-color: ${isCorrect ? '#e8f5e9' : '#ffebee'}; border-left: 5px solid ${isCorrect ? '#388e3c' : '#d32f2f'}; text-align: left;">
                <p><strong>Вопрос ${index + 1}:</strong> ${question.question}</p>
                <p><strong>Ваш ответ:</strong> ${userAnswer !== undefined ? question.options[userAnswer] : 'Не ответили'}</p>
                <p><strong>Правильный ответ:</strong> ${question.options[question.correctAnswer]}</p>
                <p style="margin-top: 10px; color: #666;"><i class="fas fa-info-circle icon"></i> ${question.explanation}</p>
            </div>
        `;
    });
    
    const score = Math.round((correctAnswers / socialTestQuestions.length) * 100);
    const isPassed = score >= 80; // 8 из 10 = 80%
    
    // Обновляем прогресс пользователя
    if (currentUser && isPassed) {
        // Отмечаем тест как пройденный
        if (!currentUser.completedCourses) currentUser.completedCourses = [];
        if (!currentUser.completedCourses.includes('social')) {
            currentUser.completedCourses.push('social');
        }
        
        // Обновляем прогресс курса
        if (!currentUser.progress) currentUser.progress = {};
        currentUser.progress.social = 100;
        
        if (!currentUser.stats) {
            currentUser.stats = {
                completedLessons: 0,
                score: 0,
                testResults: []
            };
        }
        
        currentUser.stats.completedLessons = (currentUser.stats.completedLessons || 0) + 1;
        currentUser.stats.score = (currentUser.stats.score || 0) + 50; // Бонус за прохождение теста
        
        if (!currentUser.stats.testResults) currentUser.stats.testResults = [];
        currentUser.stats.testResults.push({
            course: 'social',
            score: score,
            date: new Date().toISOString()
        });
        
        updateUserInStorage();
    }
    
    // Показываем результаты
    document.getElementById('socialTestQuestions').style.display = 'none';
    document.getElementById('socialTestResults').style.display = 'block';
    document.getElementById('socialTestResults').innerHTML = `
        <div class="simulator" style="text-align: center;">
            <h3>Результаты теста</h3>
            
            <div style="margin: 30px 0;">
                <div style="font-size: 3rem; color: ${isPassed ? '#388e3c' : '#d32f2f'}; margin-bottom: 10px;">
                    ${score}%
                </div>
                <div style="font-size: 1.2rem; margin-bottom: 20px;">
                    ${correctAnswers} из ${socialTestQuestions.length} правильных ответов
                </div>
                
                <div style="background-color: ${isPassed ? '#e8f5e9' : '#ffebee'}; padding: 20px; border-radius: 10px; max-width: 500px; margin: 0 auto;">
                    <h4 style="color: ${isPassed ? '#388e3c' : '#d32f2f'};">
                        <i class="fas ${isPassed ? 'fa-check-circle' : 'fa-times-circle'} icon"></i>
                        ${isPassed ? 'Тест пройден успешно!' : 'Тест не пройден'}
                    </h4>
                    <p>Для успешного прохождения необходимо набрать 80% правильных ответов (8 из 10).</p>
                </div>
            </div>
            
            ${isPassed ? `
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-trophy icon" style="color: #ff9800;"></i> Поздравляем!</h4>
                    <p>Вы успешно прошли курс "Безопасность в социальных сетях" и получили +50 очков к вашему рейтингу.</p>
                    ${currentUser ? `
                        <p style="margin-top: 10px;">Ваш текущий счет: <strong>${currentUser.stats.score} очков</strong></p>
                    ` : ''}
                </div>
            ` : `
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-redo icon" style="color: #1976d2;"></i> Рекомендации</h4>
                    <p>Рекомендуем повторить материал курса и пройти тест снова.</p>
                    <p>Обратите особое внимание на вопросы, в которых допустили ошибки.</p>
                </div>
            `}
            
            <h4 style="margin-top: 30px; margin-bottom: 20px;">Детализация ответов:</h4>
            <div style="max-height: 400px; overflow-y: auto; padding-right: 10px; text-align: left;">
                ${resultsHTML}
            </div>
            
            <div style="margin-top: 30px;">
                <button class="btn btn-large ${isPassed ? 'btn-success' : 'btn-warning'}" onclick="${isPassed ? 'showPage(\'courses\')' : 'retrySocialTest()'}">
                    ${isPassed ? 'Вернуться к курсам' : 'Попробовать снова'}
                </button>
                
                ${isPassed ? `
                    <button class="btn btn-large btn-outline" onclick="downloadSocialCertificate()" style="margin-left: 15px;">
                        <i class="fas fa-download icon"></i> Скачать сертификат
                    </button>
                ` : ''}
            </div>
        </div>
    `;
    
    // Прокручиваем к результатам
    document.getElementById('socialTestResults').scrollIntoView({ behavior: 'smooth' });
}

// Функция повторного прохождения теста
function retrySocialTest() {
    socialCurrentQuestion = 0;
    socialUserAnswers = [];
    
    document.getElementById('socialTestResults').style.display = 'none';
    document.getElementById('socialTestQuestions').style.display = 'block';
    
    socialTestStartTime = new Date();
    startSocialTestTimer();
    loadSocialTestQuestion();
}

// Функция отмены теста
function cancelSocialTest() {
    if (confirm('Вы уверены, что хотите отменить тест? Все ответы будут потеряны.')) {
        if (socialTestTimer) {
            clearInterval(socialTestTimer);
        }
        showPage('courses');
    }
}

// Функция скачивания сертификата
function downloadSocialCertificate() {
    showNotification('success', 'Сертификат успешно сгенерирован!');
    
    const certificateContent = `
        <div style="text-align: center; padding: 40px; background-color: white; border: 10px solid #039be5; max-width: 800px; margin: 0 auto; font-family: Arial, sans-serif;">
            <h1 style="color: #039be5; font-size: 2.5rem; margin-bottom: 20px;">СЕРТИФИКАТ</h1>
            <p style="font-size: 1.2rem; color: #555;">Настоящий сертификат подтверждает, что</p>
            <h2 style="color: #01579b; margin: 20px 0; font-size: 2rem;">${currentUser ? currentUser.name : 'Студент'}</h2>
            <p style="font-size: 1.2rem; color: #555;">успешно прошел(а) курс</p>
            <h3 style="color: #039be5; margin: 20px 0; font-size: 1.8rem;">"Безопасность в социальных сетях"</h3>
            <p style="font-size: 1rem; color: #666;">в Академии Кибербезопасности</p>
            <div style="margin: 30px 0; padding: 20px; background-color: #f9f9f9; border-radius: 10px;">
                <p style="font-size: 1.1rem;"><strong>Дата:</strong> ${new Date().toLocaleDateString('ru-RU')}</p>
                <p style="font-size: 1.1rem;"><strong>Результат теста:</strong> ${Math.round((socialUserAnswers.filter((answer, index) => answer === socialTestQuestions[index].correctAnswer).length / socialTestQuestions.length) * 100)}%</p>
                <p style="font-size: 1.1rem;"><strong>Правильных ответов:</strong> ${socialUserAnswers.filter((answer, index) => answer === socialTestQuestions[index].correctAnswer).length} из 10</p>
            </div>
            <div style="margin-top: 50px; display: flex; justify-content: space-around;">
                <div style="text-align: center;">
                    <p>Директор Академии</p>
                    <p style="margin-top: 40px;">___________________ А.В. Иванов</p>
                </div>
                <div style="text-align: center;">
                    <p>Руководитель курса</p>
                    <p style="margin-top: 40px;">___________________ Е.С. Петрова</p>
                </div>
            </div>
            <div style="margin-top: 40px; color: #999; font-size: 0.9rem;">
                <p>Лицензия на образовательную деятельность № 1234 от 01.01.2026</p>
                <p>ID сертификата: CERT-SOCIAL-${Date.now().toString().slice(-8)}</p>
            </div>
        </div>
    `;
    
    setTimeout(() => {
        if (confirm('Хотите увидеть предварительный просмотр сертификата?')) {
            const win = window.open();
            win.document.write(certificateContent);
            win.document.title = 'Сертификат - Безопасность в социальных сетях';
        }
    }, 500);
}
// ============================
// ИТОГОВЫЙ ТЕСТ: 20 вопросов по всем темам кибербезопасности
// ============================

// Функция запуска итогового теста
function startFinalTest() {
    // ПРОКРУТКА ВВЕРХ
    scrollToTop();
    
    // Показываем страницу активного курса
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    document.getElementById('active-course').classList.add('active');
    
    // Обновляем навигацию
    document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // ИНИЦИАЛИЗАЦИЯ ВОПРОСОВ ИТОГОВОГО ТЕСТА (20 вопросов по всем темам)
    finalTestQuestions = [
        // === ФИШИНГ (вопросы 1-3) ===
        {
            question: "Что такое фишинг?",
            options: [
                "Вид компьютерного вируса",
                "Мошенническая техника для получения конфиденциальной информации",
                "Способ шифрования данных",
                "Программа для удаленного управления"
            ],
            correctAnswer: 1,
            explanation: "Фишинг — это мошенническая техника, при которой злоумышленники выдают себя за доверенные организации, чтобы заставить жертву раскрыть конфиденциальную информацию (пароли, данные карт и т.д.)."
        },
        {
            question: "Какой адрес электронной почты, скорее всего, принадлежит мошенникам?",
            options: [
                "support@sberbank.ru",
                "security@vtb.ru",
                "client@alfabank.ru",
                "sberbank-secure@yandex.ru"
            ],
            correctAnswer: 3,
            explanation: "Мошенники часто используют бесплатные почтовые сервисы (yandex.ru, mail.ru, gmail.com) или поддельные домены, похожие на официальные. Настоящие банки используют свои корпоративные домены."
        },
        {
            question: "Что делать, если вы получили письмо от банка с просьбой срочно перейти по ссылке и подтвердить данные карты?",
            options: [
                "Перейти по ссылке и ввести данные, чтобы не заблокировали карту",
                "Ничего не делать — это мошенники, настоящий банк так не просит",
                "Ответить на письмо и уточнить детали",
                "Переслать письмо друзьям, чтобы они тоже проверили"
            ],
            correctAnswer: 1,
            explanation: "Настоящие банки никогда не просят вводить данные карты по ссылкам из писем или SMS. Это 100% фишинг. Такие письма нужно сразу удалять."
        },
        
        // === ТЕЛЕФОННОЕ МОШЕННИЧЕСТВО (вопросы 4-6) ===
        {
            question: "Вам звонит 'сотрудник службы безопасности банка' и сообщает о подозрительной операции. Что делать?",
            options: [
                "Назвать код из SMS для отмены операции",
                "Немедленно перевести деньги на 'безопасный счет'",
                "Положить трубку и перезвонить в банк по номеру с карты",
                "Установить программу, которую рекомендует сотрудник"
            ],
            correctAnswer: 2,
            explanation: "Единственно верное действие — положить трубку и самостоятельно перезвонить в банк по официальному номеру, указанному на обратной стороне карты или на сайте банка."
        },
        {
            question: "Что такое спуфинг в телефонном мошенничестве?",
            options: [
                "Запись разговора с жертвой",
                "Подмена номера телефона",
                "Использование робота-автоответчика",
                "Звонки через мессенджеры"
            ],
            correctAnswer: 1,
            explanation: "Спуфинг — это технология подмены номера. Мошенник может звонить с номера, который на экране отображается как номер вашего банка, хотя на самом деле звонок идет из другого места."
        },
        {
            question: "Какой из этих звонков, скорее всего, мошеннический?",
            options: [
                "Звонок из поликлиники с напоминанием о записи к врачу",
                "Звонок от 'внука', который попал в ДТП и срочно просит перевести деньги",
                "Звонок из налоговой с просьбой уточнить адрес регистрации",
                "Звонок из школы с приглашением на родительское собрание"
            ],
            correctAnswer: 1,
            explanation: "Схема 'родственник в беде' — классическое телефонное мошенничество. Мошенники играют на эмоциях и просят срочно перевести деньги. Всегда перезванивайте родственнику на его реальный номер."
        },
        
        // === ГОСУСЛУГИ (вопросы 7-9) ===
        {
            question: "Какой официальный сайт Госуслуг?",
            options: [
                "gosuslugi.ru",
                "gosuslugi-online.ru",
                "gosuslugi-portal.com",
                "gosuslugi-gov.ru"
            ],
            correctAnswer: 0,
            explanation: "Единственный официальный сайт Госуслуг — gosuslugi.ru. Все остальные домены с дополнительными словами или в других зонах — мошеннические."
        },
        {
            question: "Что делать, если вам звонят и представляются сотрудником Госуслуг, прося назвать код из SMS?",
            options: [
                "Назвать код, чтобы подтвердить личность",
                "Положить трубку — настоящие сотрудники никогда не просят коды",
                "Попросить прислать официальное письмо на email",
                "Спросить номер служебного удостоверения"
            ],
            correctAnswer: 1,
            explanation: "Настоящие сотрудники Госуслуг НИКОГДА не звонят и не просят назвать коды из SMS. Это всегда мошенники."
        },
        {
            question: "Какой номер телефона официальной горячей линии Госуслуг?",
            options: [
                "8-800-100-70-10",
                "8-900-123-45-67",
                "8-495-777-77-77",
                "8-800-555-35-35"
            ],
            correctAnswer: 0,
            explanation: "Единственный официальный номер горячей линии Госуслуг — 8-800-100-70-10. Он работает круглосуточно, бесплатно со всех телефонов России."
        },
        
        // === ПУУ СХЕМЫ (вопросы 10-12) ===
        {
            question: "Что означает аббревиатура ПУУ?",
            options: [
                "Программа Универсальной Уязвимости",
                "Программа Удаленного Управления",
                "Правила Учета Угроз",
                "Платформа Управления Устройствами"
            ],
            correctAnswer: 1,
            explanation: "ПУУ — Программа Удаленного Управления. Мошенники используют легитимные программы (AnyDesk, TeamViewer, Ammyy Admin) для получения контроля над устройствами жертв."
        },
        {
            question: "Какую программу НЕЛЬЗЯ устанавливать по просьбе звонящего 'специалиста техподдержки'?",
            options: [
                "Google Chrome",
                "AnyDesk",
                "Adobe Reader",
                "VLC Media Player"
            ],
            correctAnswer: 1,
            explanation: "AnyDesk, TeamViewer, Ammyy Admin, UltraVNC — программы удаленного доступа. Их установка по просьбе незнакомца дает мошенникам полный контроль над вашим компьютером."
        },
        {
            question: "Что делать, если курсор мыши двигается сам по себе?",
            options: [
                "Позвонить в техподдержку по номеру из всплывшего окна",
                "Немедленно отключить интернет (выдернуть кабель/отключить Wi-Fi)",
                "Ничего, это глюк компьютера",
                "Перезагрузить компьютер"
            ],
            correctAnswer: 1,
            explanation: "Самый явный признак удаленного подключения — курсор двигается сам, программы открываются и закрываются без вашего участия. Нужно немедленно физически отключить интернет."
        },
        
        // === ПАРОЛИ И АУТЕНТИФИКАЦИЯ (вопросы 13-15) ===
        {
            question: "Какой пароль считается наиболее надежным?",
            options: [
                "qwerty123",
                "password2024",
                "J8#kL!p2qW9*zM5",
                "Иван1990"
            ],
            correctAnswer: 2,
            explanation: "Надежный пароль должен быть длинным (12+ символов), содержать заглавные и строчные буквы, цифры и специальные символы. Пароль 'J8#kL!p2qW9*zM5' соответствует всем этим требованиям."
        },
        {
            question: "Что такое двухфакторная аутентификация (2FA)?",
            options: [
                "Вход в аккаунт с двух устройств одновременно",
                "Дополнительная защита: после пароля нужен код из SMS/приложения",
                "Два разных пароля для одного аккаунта",
                "Автоматическая смена пароля раз в месяц"
            ],
            correctAnswer: 1,
            explanation: "Двухфакторная аутентификация требует не только пароль, но и дополнительный код из SMS, приложения-аутентификатора или аппаратного ключа. Это значительно повышает безопасность аккаунта."
        },
        {
            question: "Почему нельзя использовать один пароль для всех сервисов?",
            options: [
                "Это неудобно — нужно везде вводить одно и то же",
                "При утечке пароля на одном сайте будут скомпрометированы все аккаунты",
                "Сайты требуют разные пароли",
                "Один пароль легко забыть"
            ],
            correctAnswer: 1,
            explanation: "Использование одного пароля для всех сервисов опасно: если мошенники получат пароль от одного сайта (например, форума), они попробуют его на Gmail, соцсетях, банках."
        },
        
        // === СОЦИАЛЬНЫЕ СЕТИ (вопросы 16-17) ===
        {
            question: "Какую информацию безопаснее всего публиковать в соцсетях?",
            options: [
                "Номер паспорта для подтверждения личности",
                "Фото билетов с QR-кодом перед поездкой",
                "Фото питомца без геометки",
                "Дату и время отъезда в отпуск"
            ],
            correctAnswer: 2,
            explanation: "Фото питомца без геометки — безопасно. Остальное: паспортные данные — конфиденциальная информация, QR-коды могут скопировать, дата отъезда показывает мошенникам, что вас нет дома."
        },
        {
            question: "Как распознать фейковый аккаунт в соцсетях?",
            options: [
                "У него много подписчиков — значит, настоящий",
                "Проверить верификацию (галочку), дату регистрации, активность",
                "Красиво оформленный профиль",
                "Наличие постов с фотографиями"
            ],
            correctAnswer: 1,
            explanation: "Фейковые аккаунты часто созданы недавно, не имеют галочки верификации, мало активности, странные ссылки в описании. Настоящие аккаунты имеют историю и верификацию."
        },
        
        // === ФИНАНСОВОЕ МОШЕННИЧЕСТВО (вопросы 18-19) ===
        {
            question: "Что должно насторожить в инвестиционном предложении?",
            options: [
                "Обещание гарантированной доходности 200% годовых",
                "Лицензия Центрального банка",
                "Официальный сайт компании",
                "Прозрачные условия договора"
            ],
            correctAnswer: 0,
            explanation: "Гарантированная доходность выше 30-40% годовых — признак финансовой пирамиды или мошенничества. Легальные инвестиции всегда связаны с рисками."
        },
        {
            question: "Что делать, если на ваше имя оформили кредит без вашего ведома?",
            options: [
                "Ничего — платить придется все равно",
                "Немедленно обратиться в банк и полицию",
                "Написать мошенникам и просить аннулировать кредит",
                "Перевести деньги на 'безопасный счет'"
            ],
            correctAnswer: 1,
            explanation: "Нужно одновременно: 1) Подать заявление в банк о несогласии с кредитом, 2) Обратиться в полицию с заявлением о мошенничестве, 3) Проверить кредитную историю."
        },
        
        // === МОБИЛЬНАЯ БЕЗОПАСНОСТЬ (вопрос 20) ===
        {
            question: "Почему опасно пользоваться публичным Wi-Fi (в кафе, аэропорту) без VPN?",
            options: [
                "Медленная скорость интернета",
                "Мошенники могут перехватывать ваш трафик и видеть пароли",
                "Высокая стоимость подключения",
                "Быстро разряжается телефон"
            ],
            correctAnswer: 1,
            explanation: "В публичных Wi-Fi-сетях мошенники могут проводить атаки Man-in-the-Middle, перехватывая все данные, которые вы отправляете: пароли, сообщения, данные карт. VPN шифрует трафик и защищает от этого."
        }
    ];
    
    // Сбрасываем данные теста
    finalCurrentQuestion = 0;
    finalUserAnswers = [];
    finalTestStartTime = new Date();
    
    // Загружаем страницу теста
    const courseContent = document.getElementById('courseContent');
    courseContent.innerHTML = `
        <div class="course-header">
            <div class="course-header-icon" style="background: linear-gradient(135deg, #ffa000, #ffb300);">
                <i class="fas fa-graduation-cap"></i>
            </div>
            <div class="course-header-content">
                <h1>Итоговый тест: Кибербезопасность (Все темы)</h1>
                <p>Проверьте свои знания по всем темам кибербезопасности. 20 вопросов, для успешного прохождения нужно правильно ответить на 16 вопросов (80%).</p>
                <div class="course-meta">
                    <div class="course-meta-item">
                        <i class="fas fa-question-circle"></i>
                        <span>20 вопросов</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-clock"></i>
                        <span>40 минут</span>
                    </div>
                    <div class="course-meta-item">
                        <i class="fas fa-chart-line"></i>
                        <span>Проходной балл: 80%</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="finalTestContainer">
            <div id="finalTestInstructions" style="text-align: center; padding: 40px 0;">
                <h3>Инструкция к итоговому тесту</h3>
                <p style="margin: 20px 0;">Тест состоит из 20 вопросов по всем темам курса. Каждый вопрос имеет один правильный ответ.</p>
                
                <div style="background-color: #f5f5f5; padding: 20px; border-radius: 10px; max-width: 600px; margin: 0 auto;">
                    <h4><i class="fas fa-info-circle icon" style="color: #ffa000;"></i> Правила тестирования:</h4>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Выберите один вариант ответа на каждый вопрос</li>
                        <li>Можно вернуться к предыдущим вопросам</li>
                        <li>На прохождение теста отводится 40 минут</li>
                        <li>После завершения вы увидите детальный результат с объяснениями</li>
                        <li>Для успешного прохождения нужно ≥ 80% правильных ответов (16 из 20)</li>
                        <li>При успешном прохождении вы получите сертификат эксперта по кибербезопасности</li>
                    </ul>
                </div>
                
                <div style="background-color: #fff3e0; padding: 20px; border-radius: 10px; max-width: 600px; margin: 20px auto 0;">
                    <h4><i class="fas fa-trophy icon" style="color: #ff9800;"></i> Темы тестирования:</h4>
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 10px;">
                        <div>✓ Фишинг</div>
                        <div>✓ Телефонное мошенничество</div>
                        <div>✓ Госуслуги</div>
                        <div>✓ ПУУ схемы</div>
                        <div>✓ Пароли и 2FA</div>
                        <div>✓ Социальные сети</div>
                        <div>✓ Финансовое мошенничество</div>
                        <div>✓ Мобильная безопасность</div>
                    </div>
                </div>
                
                <button class="btn btn-large btn-success" onclick="beginFinalTest()" style="margin-top: 30px;">
                    <i class="fas fa-play icon"></i> Начать итоговый тест
                </button>
                
                <button class="btn btn-large btn-outline" onclick="showPage('test')" style="margin-top: 30px; margin-left: 15px;">
                    <i class="fas fa-arrow-left icon"></i> Вернуться к тестам
                </button>
            </div>
            
            <div id="finalTestQuestions" style="display: none;">
                <!-- Вопросы будут загружены динамически -->
            </div>
            
            <div id="finalTestResults" style="display: none;">
                <!-- Результаты будут загружены динамически -->
            </div>
        </div>
    `;
}

// Функция для начала теста
function beginFinalTest() {
    // Скрываем инструкции и показываем вопросы
    document.getElementById('finalTestInstructions').style.display = 'none';
    document.getElementById('finalTestQuestions').style.display = 'block';
    
    // Запускаем таймер
    startFinalTestTimer();
    
    // Загружаем первый вопрос
    loadFinalTestQuestion();
}

// Функция для загрузки вопроса
function loadFinalTestQuestion() {
    const testQuestionsDiv = document.getElementById('finalTestQuestions');
    const question = finalTestQuestions[finalCurrentQuestion];
    
    testQuestionsDiv.innerHTML = `
        <div class="simulator">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                <h3>Вопрос ${finalCurrentQuestion + 1} из ${finalTestQuestions.length}</h3>
                <div id="finalTestTimer" style="background-color: #f5f5f5; padding: 8px 15px; border-radius: 20px; font-weight: bold;">
                    <i class="fas fa-clock icon"></i> <span id="finalTimeRemaining">40:00</span>
                </div>
            </div>
            
            <div style="background-color: #f8f9fa; padding: 25px; border-radius: 10px; margin-bottom: 25px;">
                <h4 style="color: #ffa000; margin-bottom: 15px;">${question.question}</h4>
            </div>
            
            <div class="options">
                ${question.options.map((option, index) => `
                    <div class="option" onclick="selectFinalTestAnswer(${index})" 
                         style="${finalUserAnswers[finalCurrentQuestion] === index ? 'border-color: #ffa000; background-color: #fff8e1;' : ''}">
                        ${String.fromCharCode(65 + index)}. ${option}
                    </div>
                `).join('')}
            </div>
            
            <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 30px;">
    ${finalCurrentQuestion > 0 ? `
        <button class="btn btn-outline" onclick="prevFinalTestQuestion()" style="padding: 8px 20px;">
            <i class="fas fa-arrow-left icon"></i> Назад
        </button>
    ` : '<div style="width: 100px;"></div>'}
    
    <div style="text-align: center;">
        <button class="btn btn-success" onclick="nextFinalTestQuestion()" id="finalNextButton" 
                ${finalUserAnswers[finalCurrentQuestion] === undefined ? 'disabled' : ''}
                style="padding: 8px 25px;">
            ${finalCurrentQuestion === finalTestQuestions.length - 1 ? 'Завершить тест' : 'Следующий вопрос'} 
            <i class="fas fa-arrow-right icon"></i>
        </button>
        <p style="margin-top: 8px; color: #666; font-size: 0.85rem;">
            Вопрос ${finalCurrentQuestion + 1} из ${finalTestQuestions.length}
        </p>
    </div>
    
    <div style="text-align: right;">
        <button class="btn btn-danger" onclick="cancelFinalTest()" style="padding: 8px 20px;">
            <i class="fas fa-times icon"></i> Отменить
        </button>
    </div>
</div>
            
            <div style="margin-top: 20px; text-align: center; color: #666;">
                <p><i class="fas fa-info-circle icon"></i> Выберите один вариант ответа</p>
            </div>
        </div>
    `;
}

// Функция выбора ответа
function selectFinalTestAnswer(answerIndex) {
    // Убираем выделение со всех вариантов
    document.querySelectorAll('#finalTestQuestions .option').forEach(option => {
        option.style.borderColor = '#ddd';
        option.style.backgroundColor = 'white';
    });
    
    // Выделяем выбранный вариант
    event.target.style.borderColor = '#ffa000';
    event.target.style.backgroundColor = '#fff8e1';
    
    // Сохраняем ответ
    finalUserAnswers[finalCurrentQuestion] = answerIndex;
    
    // Активируем кнопку "Далее"
    document.getElementById('finalNextButton').disabled = false;
}

// Функция для перехода к следующему вопросу
function nextFinalTestQuestion() {
    // Проверяем, выбран ли ответ
    if (finalUserAnswers[finalCurrentQuestion] === undefined) {
        showNotification('error', 'Пожалуйста, выберите вариант ответа');
        return;
    }
    
    // Переходим к следующему вопросу или завершаем тест
    if (finalCurrentQuestion < finalTestQuestions.length - 1) {
        finalCurrentQuestion++;
        loadFinalTestQuestion();
    } else {
        finishFinalTest();
    }
}

// Функция для возврата к предыдущему вопросу
function prevFinalTestQuestion() {
    if (finalCurrentQuestion > 0) {
        finalCurrentQuestion--;
        loadFinalTestQuestion();
    }
}

// Функция запуска таймера теста
function startFinalTestTimer() {
    // Очищаем предыдущий таймер, если был
    if (finalTestTimer) {
        clearInterval(finalTestTimer);
    }
    
    let timeLeft = 40 * 60; // 40 минут в секундах
    
    finalTestTimer = setInterval(function() {
        timeLeft--;
        
        const minutes = Math.floor(timeLeft / 60);
        const seconds = timeLeft % 60;
        
        const timeElement = document.getElementById('finalTimeRemaining');
        if (timeElement) {
            timeElement.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }
        
        // Меняем цвет при малом остатке времени
        const timerDiv = document.getElementById('finalTestTimer');
        if (timerDiv && timeLeft < 300) { // Меньше 5 минут
            timerDiv.style.backgroundColor = '#ffebee';
            timerDiv.style.color = '#d32f2f';
        }
        
        if (timeLeft <= 0) {
            clearInterval(finalTestTimer);
            finishFinalTest();
        }
    }, 1000);
}

// Функция завершения теста
function finishFinalTest() {
    if (finalTestTimer) {
        clearInterval(finalTestTimer);
    }
    
    // Рассчитываем результаты
    let correctAnswers = 0;
    let resultsHTML = '';
    
    finalTestQuestions.forEach((question, index) => {
        const userAnswer = finalUserAnswers[index];
        const isCorrect = userAnswer === question.correctAnswer;
        
        if (isCorrect) correctAnswers++;
        
        resultsHTML += `
            <div style="margin-bottom: 20px; padding: 15px; border-radius: 8px; background-color: ${isCorrect ? '#e8f5e9' : '#ffebee'}; border-left: 5px solid ${isCorrect ? '#388e3c' : '#d32f2f'}; text-align: left;">
                <p><strong>Вопрос ${index + 1}:</strong> ${question.question}</p>
                <p><strong>Ваш ответ:</strong> ${userAnswer !== undefined ? question.options[userAnswer] : 'Не ответили'}</p>
                <p><strong>Правильный ответ:</strong> ${question.options[question.correctAnswer]}</p>
                <p style="margin-top: 10px; color: #666;"><i class="fas fa-info-circle icon"></i> ${question.explanation}</p>
            </div>
        `;
    });
    
    const score = Math.round((correctAnswers / finalTestQuestions.length) * 100);
    const isPassed = score >= 80; // 16 из 20 = 80%
    
    // Обновляем прогресс пользователя
    if (currentUser && isPassed) {
        // Отмечаем итоговый тест как пройденный
        if (!currentUser.completedCourses) currentUser.completedCourses = [];
        if (!currentUser.completedCourses.includes('final')) {
            currentUser.completedCourses.push('final');
        }
        
        if (!currentUser.stats) {
            currentUser.stats = {
                completedLessons: 0,
                score: 0,
                testResults: []
            };
        }
        
        currentUser.stats.completedLessons = (currentUser.stats.completedLessons || 0) + 1;
        currentUser.stats.score = (currentUser.stats.score || 0) + 100; // Бонус 100 очков за итоговый тест
        
        if (!currentUser.stats.testResults) currentUser.stats.testResults = [];
        currentUser.stats.testResults.push({
            course: 'final',
            score: score,
            date: new Date().toISOString()
        });
        
        updateUserInStorage();
    }
    
    // Показываем результаты
    document.getElementById('finalTestQuestions').style.display = 'none';
    document.getElementById('finalTestResults').style.display = 'block';
    document.getElementById('finalTestResults').innerHTML = `
        <div class="simulator" style="text-align: center;">
            <h3>Результаты итогового теста</h3>
            
            <div style="margin: 30px 0;">
                <div style="font-size: 3rem; color: ${isPassed ? '#388e3c' : '#d32f2f'}; margin-bottom: 10px;">
                    ${score}%
                </div>
                <div style="font-size: 1.2rem; margin-bottom: 20px;">
                    ${correctAnswers} из ${finalTestQuestions.length} правильных ответов
                </div>
                
                <div style="background-color: ${isPassed ? '#e8f5e9' : '#ffebee'}; padding: 20px; border-radius: 10px; max-width: 500px; margin: 0 auto;">
                    <h4 style="color: ${isPassed ? '#388e3c' : '#d32f2f'};">
                        <i class="fas ${isPassed ? 'fa-check-circle' : 'fa-times-circle'} icon"></i>
                        ${isPassed ? 'Итоговый тест пройден успешно!' : 'Итоговый тест не пройден'}
                    </h4>
                    <p>Для успешного прохождения необходимо набрать 80% правильных ответов (16 из 20).</p>
                </div>
            </div>
            
            ${isPassed ? `
                <div style="background-color: #fff3e0; padding: 30px; border-radius: 10px; margin: 20px 0; border: 2px solid #ffa000;">
                    <h4 style="color: #ff9800; font-size: 1.5rem;"><i class="fas fa-crown icon"></i> ПОЗДРАВЛЯЕМ!</h4>
                    <p style="font-size: 1.2rem; margin: 15px 0;">Вы успешно прошли итоговый тест и подтвердили свои знания по кибербезопасности!</p>
                    <p>Вы получаете статус <strong>"Эксперт по кибербезопасности"</strong> и +100 очков к рейтингу.</p>
                    ${currentUser ? `
                        <p style="margin-top: 10px;">Ваш текущий счет: <strong>${currentUser.stats.score} очков</strong></p>
                    ` : ''}
                </div>
            ` : `
                <div style="background-color: #e3f2fd; padding: 20px; border-radius: 10px; margin: 20px 0;">
                    <h4><i class="fas fa-redo icon" style="color: #1976d2;"></i> Рекомендации</h4>
                    <p>Повторите материал по темам, в которых допустили ошибки:</p>
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 15px;">
                        <div>✓ Фишинг</div>
                        <div>✓ Телефонное мошенничество</div>
                        <div>✓ Госуслуги</div>
                        <div>✓ ПУУ схемы</div>
                        <div>✓ Пароли и 2FA</div>
                        <div>✓ Социальные сети</div>
                        <div>✓ Финансовое мошенничество</div>
                        <div>✓ Мобильная безопасность</div>
                    </div>
                    <p style="margin-top: 15px;">Пройдите тесты по отдельным темам и попробуйте снова!</p>
                </div>
            `}
            
            <h4 style="margin-top: 30px; margin-bottom: 20px;">Детализация ответов:</h4>
            <div style="max-height: 400px; overflow-y: auto; padding-right: 10px; text-align: left;">
                ${resultsHTML}
            </div>
            
            <div style="margin-top: 30px;">
                <button class="btn btn-large ${isPassed ? 'btn-success' : 'btn-warning'}" onclick="${isPassed ? 'showPage(\'test\')' : 'retryFinalTest()'}">
                    ${isPassed ? 'Вернуться к тестам' : 'Попробовать снова'}
                </button>
                
                ${isPassed ? `
                    <button class="btn btn-large btn-outline" onclick="downloadFinalCertificate()" style="margin-left: 15px;">
                        <i class="fas fa-download icon"></i> Скачать сертификат эксперта
                    </button>
                ` : ''}
            </div>
        </div>
    `;
    
    // Прокручиваем к результатам
    document.getElementById('finalTestResults').scrollIntoView({ behavior: 'smooth' });
}

// Функция повторного прохождения теста
function retryFinalTest() {
    finalCurrentQuestion = 0;
    finalUserAnswers = [];
    
    document.getElementById('finalTestResults').style.display = 'none';
    document.getElementById('finalTestQuestions').style.display = 'block';
    
    finalTestStartTime = new Date();
    startFinalTestTimer();
    loadFinalTestQuestion();
}

// Функция отмены теста
function cancelFinalTest() {
    if (confirm('Вы уверены, что хотите отменить тест? Все ответы будут потеряны.')) {
        if (finalTestTimer) {
            clearInterval(finalTestTimer);
        }
        showPage('test');
    }
}

// Функция скачивания сертификата
function downloadFinalCertificate() {
    showNotification('success', 'Сертификат эксперта успешно сгенерирован!');
    
    const certificateContent = `
        <div style="text-align: center; padding: 40px; background-color: white; border: 10px solid #ffa000; max-width: 800px; margin: 0 auto; font-family: Arial, sans-serif;">
            <div style="font-size: 3rem; color: #ffa000; margin-bottom: 20px;">
                <i class="fas fa-shield-alt"></i>
            </div>
            <h1 style="color: #ffa000; font-size: 2.5rem; margin-bottom: 20px;">СЕРТИФИКАТ ЭКСПЕРТА</h1>
            <p style="font-size: 1.2rem; color: #555;">Настоящий сертификат подтверждает, что</p>
            <h2 style="color: #ff8f00; margin: 20px 0; font-size: 2rem;">${currentUser ? currentUser.name : 'Студент'}</h2>
            <p style="font-size: 1.2rem; color: #555;">успешно прошел(а) итоговое тестирование и подтвердил(а) знания</p>
            <h3 style="color: #ffa000; margin: 20px 0; font-size: 1.8rem;">ПО КИБЕРБЕЗОПАСНОСТИ</h3>
            <div style="margin: 30px 0; padding: 20px; background-color: #fff8e1; border-radius: 10px;">
                <p style="font-size: 1.1rem;"><strong>Дата:</strong> ${new Date().toLocaleDateString('ru-RU')}</p>
                <p style="font-size: 1.1rem;"><strong>Результат теста:</strong> ${Math.round((finalUserAnswers.filter((answer, index) => answer === finalTestQuestions[index].correctAnswer).length / finalTestQuestions.length) * 100)}%</p>
                <p style="font-size: 1.1rem;"><strong>Правильных ответов:</strong> ${finalUserAnswers.filter((answer, index) => answer === finalTestQuestions[index].correctAnswer).length} из 20</p>
            </div>
            <div style="margin-top: 50px; display: flex; justify-content: space-around;">
                <div style="text-align: center;">
                    <p>Директор Академии</p>
                    <p style="margin-top: 40px;">___________________ А.В. Иванов</p>
                </div>
                <div style="text-align: center;">
                    <p>Руководитель курса</p>
                    <p style="margin-top: 40px;">___________________ Е.С. Петрова</p>
                </div>
            </div>
            <div style="margin-top: 40px; color: #999; font-size: 0.9rem;">
                <p>Лицензия на образовательную деятельность № 1234 от 01.01.2026</p>
                <p>ID сертификата: CERT-EXPERT-${Date.now().toString().slice(-8)}</p>
            </div>
            <div style="margin-top: 20px; color: #ffa000; font-weight: bold;">
                <p>ЭКСПЕРТ ПО КИБЕРБЕЗОПАСНОСТИ</p>
            </div>
        </div>
    `;
    
    setTimeout(() => {
        if (confirm('Хотите увидеть предварительный просмотр сертификата?')) {
            const win = window.open();
            win.document.write(certificateContent);
            win.document.title = 'Сертификат эксперта - Кибербезопасность';
        }
    }, 500);
}
// ========== ФУНКЦИИ ДЛЯ ВЫПАДАЮЩЕГО МЕНЮ ==========

// Открыть/закрыть меню
function toggleDropdownMenu() {
    const menu = document.getElementById('dropdownMenu');
    const overlay = document.getElementById('menuOverlay');
    const menuBtn = document.getElementById('menuBtn');
    const body = document.body;
    
    menu.classList.toggle('active');
    overlay.classList.toggle('active');
    menuBtn.classList.toggle('active');
    
    if (menu.classList.contains('active')) {
        body.style.overflow = 'hidden';
    } else {
        body.style.overflow = '';
    }
}

// Закрыть меню
function closeDropdownMenu() {
    const menu = document.getElementById('dropdownMenu');
    const overlay = document.getElementById('menuOverlay');
    const menuBtn = document.getElementById('menuBtn');
    const body = document.body;
    
    menu.classList.remove('active');
    overlay.classList.remove('active');
    menuBtn.classList.remove('active');
    body.style.overflow = '';
}

// Обновленная функция showPage с закрытием меню
function showPage(pageId) {
    // Закрываем меню
    closeDropdownMenu();
    
    // Прокрутка к началу страницы
    setTimeout(() => {
        window.scrollTo({
            top: 0,
            behavior: 'smooth'
        });
    }, 100);
    
    // Проверка авторизации для защищенных страниц
    const protectedPages = ['courses', 'simulators', 'test', 'profile', 'active-simulator', 'active-course'];
    
    if (protectedPages.includes(pageId) && !currentUser) {
        showNotification('error', 'Для доступа к этому разделу необходимо войти в систему');
        showLoginModal();
        return;
    }
    
    // Скрыть текущую страницу
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    
    // Показать выбранную страницу
    const targetPage = document.getElementById(pageId);
    if (targetPage) {
        targetPage.classList.add('active');
    }
    
    // Обновить активную ссылку в навигации
    document.querySelectorAll('.dropdown-link').forEach(link => {
        link.classList.remove('active');
    });
    
    // Найти и активировать соответствующую ссылку
    const pageTitles = {
        'home': 'Главная',
        'courses': 'Все курсы',
        'simulators': 'Тренажеры',
        'test': 'Тестирование',
        'profile': 'Профиль'
    };
    
    document.querySelectorAll('.dropdown-link').forEach(link => {
        if (link.textContent.trim() === pageTitles[pageId]) {
            link.classList.add('active');
        }
    });
    
    currentPage = pageId;
    
    // Загрузить контент страницы
    if (pageId === 'courses') {
        loadCoursesPage();
    } else if (pageId === 'simulators') {
        loadSimulatorsPage();
    } else if (pageId === 'test') {
        loadTestPage();
    } else if (pageId === 'profile') {
        loadProfilePage();
    }
}

// Обновленная функция для авторизованного пользователя
function updateUIForLoggedInUser() {
    // Десктопное меню
    const userMenu = document.getElementById('userMenu');
    if (userMenu) {
        userMenu.innerHTML = `
            <div class="user-info" onclick="showPage('profile')">
                <div class="avatar">${currentUser.name.charAt(0).toUpperCase()}</div>
                <span>${currentUser.name}</span>
            </div>
            <button class="btn btn-danger" onclick="logoutUser()">
                <i class="fas fa-sign-out-alt"></i>
            </button>
        `;
    }
    
    // Формируем текст статистики (только рейтинг)
    let statsText = '';
    if (currentUser.stats) {
        statsText = `
            <div class="dropdown-user-stats">
                <i class="fas fa-star" style="color: #ffc107;"></i> ${currentUser.stats.score || 0} очков
            </div>
        `;
    } else {
        statsText = `
            <div class="dropdown-user-stats">
                <i class="fas fa-star" style="color: #ffc107;"></i> 0 очков
            </div>
        `;
    }
    
    // Выпадающее меню
    const dropdownUserSection = document.getElementById('dropdownUserSection');
    if (dropdownUserSection) {
        dropdownUserSection.innerHTML = `
            <div class="dropdown-user-info" onclick="showPage('profile'); closeDropdownMenu();">
                <div class="dropdown-avatar">${currentUser.name.charAt(0).toUpperCase()}</div>
                <div class="dropdown-user-details">
                    <div class="dropdown-user-name">${currentUser.name}</div>
                    ${statsText}
                </div>
            </div>
            <div class="dropdown-auth-buttons">
                <button class="btn" onclick="showPage('profile'); closeDropdownMenu();">
                    <i class="fas fa-user"></i> Мой профиль
                </button>
                <button class="btn btn-success" onclick="logoutUser(); closeDropdownMenu();">
                    <i class="fas fa-sign-out-alt"></i> Выйти
                </button>
            </div>
        `;
    }
    
    const authButtons = document.getElementById('authButtonsContainer');
    if (authButtons) {
        authButtons.style.display = 'none';
    }
    
    updateProgressBars();
}

// Обновленная функция для неавторизованного пользователя
function updateUIForLoggedOutUser() {
    const userMenu = document.getElementById('userMenu');
    if (userMenu) {
        userMenu.innerHTML = '';
    }
    
    const authButtons = document.getElementById('authButtonsContainer');
    if (authButtons) {
        authButtons.style.display = 'flex';
    }
    
    // Выпадающее меню
    const dropdownUserSection = document.getElementById('dropdownUserSection');
    if (dropdownUserSection) {
        dropdownUserSection.innerHTML = `
            <div class="dropdown-auth-buttons">
                <button class="btn" onclick="showLoginModal(); closeDropdownMenu();">
                    <i class="fas fa-sign-in-alt"></i> Войти
                </button>
                <button class="btn btn-success" onclick="showRegisterModal(); closeDropdownMenu();">
                    <i class="fas fa-user-plus"></i> Регистрация
                </button>
            </div>
        `;
    }
}

// Функции для модальных окон
function showLoginModal() {
    const modal = document.getElementById('loginModal');
    if (modal) {
        modal.style.display = 'flex';
    }
    closeDropdownMenu();
}

function showRegisterModal() {
    const modal = document.getElementById('registerModal');
    if (modal) {
        modal.style.display = 'flex';
    }
    closeDropdownMenu();
}

function closeModal(modalId) {
    const modal = document.getElementById(modalId);
    if (modal) {
        modal.style.display = 'none';
    }
}

// Функция выхода
function logoutUser() {
    currentUser = null;
    localStorage.removeItem('cyberAcademyCurrentUser');
    showNotification('info', 'Вы вышли из системы');
    updateUIForLoggedOutUser();
    showPage('home');
    closeDropdownMenu();
}

// Добавляем эффект скролла для навбара
window.addEventListener('scroll', function() {
    const navbar = document.getElementById('navbar');
    if (navbar) {
        if (window.scrollY > 50) {
            navbar.classList.add('scrolled');
        } else {
            navbar.classList.remove('scrolled');
        }
    }
});

// Закрытие меню при клике вне его
document.addEventListener('click', function(event) {
    const menu = document.getElementById('dropdownMenu');
    const menuBtn = document.getElementById('menuBtn');
    const overlay = document.getElementById('menuOverlay');
    
    if (menu && menuBtn && overlay) {
        if (!menu.contains(event.target) && !menuBtn.contains(event.target) && menu.classList.contains('active')) {
            closeDropdownMenu();
        }
    }
});

// Закрытие меню при нажатии Escape
document.addEventListener('keydown', function(event) {
    if (event.key === 'Escape') {
        closeDropdownMenu();
    }
});

// Закрытие модальных окон при клике вне их
window.onclick = function(event) {
    if (event.target.classList.contains('modal')) {
        event.target.style.display = 'none';
    }
};
// ========== ОБРАБОТКА НАЖАТИЯ КЛАВИШИ ENTER В ТЕСТАХ ==========

// Функция для обработки нажатия Enter в тестах
function handleEnterKey(event) {
    // Проверяем, что нажата клавиша Enter (код 13)
    if (event.keyCode === 13 || event.key === 'Enter') {
        
        // Проверяем, какой тест сейчас активен
        const activePage = document.querySelector('.page.active')?.id;
        
        // Тест по телефонному мошенничеству
        if (activePage === 'active-course' && document.getElementById('testQuestions')?.style.display === 'block') {
            const nextButton = document.getElementById('nextButton');
            if (nextButton && !nextButton.disabled) {
                event.preventDefault();
                nextButton.click();
            }
        }
        
        // Тест по фишингу
        else if (activePage === 'active-course' && document.getElementById('phishingTestQuestions')?.style.display === 'block') {
            const nextButton = document.getElementById('phishingNextButton');
            if (nextButton && !nextButton.disabled) {
                event.preventDefault();
                nextButton.click();
            }
        }
        
        // Тест по Госуслугам
        else if (activePage === 'active-course' && document.getElementById('gosuslugiTestQuestions')?.style.display === 'block') {
            const nextButton = document.getElementById('gosuslugiNextButton');
            if (nextButton && !nextButton.disabled) {
                event.preventDefault();
                nextButton.click();
            }
        }
        
        // Тест по ПУУ
        else if (activePage === 'active-course' && document.getElementById('puuTestQuestions')?.style.display === 'block') {
            const nextButton = document.getElementById('puuNextButton');
            if (nextButton && !nextButton.disabled) {
                event.preventDefault();
                nextButton.click();
            }
        }
        
        // Тест по финансам
        else if (activePage === 'active-course' && document.getElementById('financeTestQuestions')?.style.display === 'block') {
            const nextButton = document.getElementById('financeNextButton');
            if (nextButton && !nextButton.disabled) {
                event.preventDefault();
                nextButton.click();
            }
        }
        
        // Тест по паролям
        else if (activePage === 'active-course' && document.getElementById('passwordsTestQuestions')?.style.display === 'block') {
            const nextButton = document.getElementById('passwordsNextButton');
            if (nextButton && !nextButton.disabled) {
                event.preventDefault();
                nextButton.click();
            }
        }
        
        // Тест по соцсетям
        else if (activePage === 'active-course' && document.getElementById('socialTestQuestions')?.style.display === 'block') {
            const nextButton = document.getElementById('socialNextButton');
            if (nextButton && !nextButton.disabled) {
                event.preventDefault();
                nextButton.click();
            }
        }
        
        // Итоговый тест
        else if (activePage === 'active-course' && document.getElementById('finalTestQuestions')?.style.display === 'block') {
            const nextButton = document.getElementById('finalNextButton');
            if (nextButton && !nextButton.disabled) {
                event.preventDefault();
                nextButton.click();
            }
        }
    }
}

// Добавляем обработчик события на всю страницу
document.addEventListener('keydown', handleEnterKey);

// Дополнительно: добавляем обработку Enter для выбора вариантов в тренажерах
function handleSimulatorEnter(event) {
    if (event.keyCode === 13 || event.key === 'Enter') {
        
        // Для тренажера Фишинг
        const phishingChat = document.getElementById('phishing-chat-container');
        if (phishingChat && phishingChat.style.display !== 'none') {
            const activeOption = document.querySelector('.phishing-chat-option:hover');
            if (activeOption) {
                event.preventDefault();
                activeOption.click();
            }
        }
        
        // Для тренажера Телефон
        const phoneChat = document.getElementById('phone-chat-container');
        if (phoneChat && phoneChat.style.display !== 'none') {
            const activeOption = document.querySelector('.phone-chat-option:hover');
            if (activeOption) {
                event.preventDefault();
                activeOption.click();
            }
        }
        
        // Для тренажера ПУУ
        const puuChat = document.getElementById('ai-phone-simulator');
        if (puuChat && puuChat.style.display !== 'none') {
            const activeOption = document.querySelector('.ai-response-option:hover');
            if (activeOption) {
                event.preventDefault();
                activeOption.click();
            }
        }
    }
}

// Добавляем второй обработчик
document.addEventListener('keydown', handleSimulatorEnter);

// Функция для отладки (можно удалить позже)
console.log('Обработчик клавиши Enter добавлен для всех тестов');
// Принудительно устанавливаем правильный заголовок страницы
document.title = "Академия Кибербезопасности - Защита от мошенников";

// Также меняем заголовок при загрузке и через таймер (для надежности)
window.addEventListener('load', function() {
    document.title = "Академия Кибербезопасности - Защита от мошенников";
});

setInterval(function() {
    if (document.title !== "Академия Кибербезопасности - Защита от мошенников") {
        document.title = "Академия Кибербезопасности - Защита от мошенников";
    }
}, 1000);
</script>


</body>
</html>
