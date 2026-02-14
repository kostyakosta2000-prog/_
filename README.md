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
