# My-Web
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的个人空间</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <!-- 导航栏 -->
    <header>
        <nav>
            <div class="logo">
                <i class="fas fa-user-astronaut"></i>
                <span>我的空间</span>
            </div>
            <ul class="nav-links">
                <li><a href="#home" class="active"><i class="fas fa-home"></i> 首页</a></li>
                <li><a href="#games"><i class="fas fa-gamepad"></i> 游戏</a></li>
                <li><a href="#stories"><i class="fas fa-book-open"></i> 我的故事</a></li>
                <li><a href="#novels"><i class="fas fa-pen-fancy"></i> 我的小说</a></li>
                <li><a href="#scenery"><i class="fas fa-camera"></i> 美景</a></li>
            </ul>
            <div class="burger">
                <div class="line1"></div>
                <div class="line2"></div>
                <div class="line3"></div>
            </div>
        </nav>
    </header>

    <!-- 主要内容区域 -->
    <main>
        <!-- 首页部分 -->
        <section id="home" class="section active">
            <div class="hero">
                <h1>欢迎来到我的个人空间</h1>
                <p>探索我的创作世界</p>
                <div class="scroll-down">
                    <span>向下滚动</span>
                    <i class="fas fa-chevron-down"></i>
                </div>
            </div>
            
            <div class="intro-cards">
                <div class="card" data-target="#games">
                    <i class="fas fa-gamepad"></i>
                    <h3>游戏作品</h3>
                    <p>我开发的游戏和游戏设计分享</p>
                </div>
                <div class="card" data-target="#stories">
                    <i class="fas fa-book-open"></i>
                    <h3>我的故事</h3>
                    <p>生活中的点滴记录与回忆</p>
                </div>
                <div class="card" data-target="#novels">
                    <i class="fas fa-pen-fancy"></i>
                    <h3>我的小说</h3>
                    <p>原创小说与文学创作</p>
                </div>
                <div class="card" data-target="#scenery">
                    <i class="fas fa-camera"></i>
                    <h3>美景分享</h3>
                    <p>旅行中拍摄的美丽风景</p>
                </div>
            </div>
        </section>

        <!-- 游戏部分 -->
        <section id="games" class="section">
            <h2 class="section-title">我的游戏作品</h2>
            <div class="games-container">
                <!-- 游戏将通过JavaScript动态加载 -->
            </div>
        </section>

        <!-- 故事部分 -->
        <section id="stories" class="section">
            <h2 class="section-title">我的故事</h2>
            <div class="story-container">
                <div class="story-timeline">
                    <!-- 时间线将通过JavaScript动态加载 -->
                </div>
            </div>
        </section>

        <!-- 小说部分 -->
        <section id="novels" class="section">
            <h2 class="section-title">我的小说</h2>
            <div class="novel-filter">
                <button class="filter-btn active" data-filter="all">全部</button>
                <button class="filter-btn" data-filter="fantasy">奇幻</button>
                <button class="filter-btn" data-filter="sci-fi">科幻</button>
                <button class="filter-btn" data-filter="romance">爱情</button>
            </div>
            <div class="novels-container">
                <!-- 小说将通过JavaScript动态加载 -->
            </div>
        </section>

        <!-- 美景部分 -->
        <section id="scenery" class="section">
            <h2 class="section-title">美景分享</h2>
            <div class="gallery-container">
                <!-- 图片将通过JavaScript动态加载 -->
            </div>
            <div class="lightbox">
                <span class="close-btn">&times;</span>
                <img class="lightbox-content" id="lightbox-img">
                <div class="caption"></div>
                <a class="prev">&#10094;</a>
                <a class="next">&#10095;</a>
            </div>
        </section>
    </main>

    <!-- 页脚 -->
    <footer>
        <div class="social-links">
            <a href="#"><i class="fab fa-weibo"></i></a>
            <a href="#"><i class="fab fa-github"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
        </div>
        <p>&copy; 2023 我的个人空间. 保留所有权利.</p>
    </footer>

    <!-- 返回顶部按钮 -->
    <button id="back-to-top" title="返回顶部"><i class="fas fa-arrow-up"></i></button>

    <script src="js/script.js"></script>
</body>
</html>
/* 基础样式重置 */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --primary-color: #3498db;
    --secondary-color: #2c3e50;
    --accent-color: #e74c3c;
    --light-color: #ecf0f1;
    --dark-color: #2c3e50;
    --text-color: #333;
    --text-light: #7f8c8d;
    --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    --transition: all 0.3s ease;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: var(--text-color);
    background-color: #f9f9f9;
    overflow-x: hidden;
}

/* 导航栏样式 */
header {
    background-color: var(--secondary-color);
    color: white;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
    box-shadow: var(--shadow);
    transition: var(--transition);
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.logo {
    display: flex;
    align-items: center;
    font-size: 1.5rem;
    font-weight: bold;
}

.logo i {
    margin-right: 0.5rem;
    color: var(--primary-color);
}

.nav-links {
    display: flex;
    list-style: none;
}

.nav-links li {
    margin-left: 2rem;
}

.nav-links a {
    color: white;
    text-decoration: none;
    font-weight: 500;
    display: flex;
    align-items: center;
    transition: var(--transition);
}

.nav-links a i {
    margin-right: 0.5rem;
}

.nav-links a:hover, .nav-links a.active {
    color: var(--primary-color);
}

.burger {
    display: none;
    cursor: pointer;
}

.burger div {
    width: 25px;
    height: 3px;
    background-color: white;
    margin: 5px;
    transition: var(--transition);
}

/* 主要内容区域 */
main {
    margin-top: 70px;
    min-height: calc(100vh - 70px);
}

.section {
    padding: 4rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
    display: none;
}

.section.active {
    display: block;
    animation: fadeIn 0.5s ease;
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

.section-title {
    text-align: center;
    margin-bottom: 3rem;
    font-size: 2.5rem;
    color: var(--secondary-color);
    position: relative;
}

.section-title::after {
    content: '';
    display: block;
    width: 80px;
    height: 4px;
    background-color: var(--primary-color);
    margin: 1rem auto;
}

/* 首页样式 */
.hero {
    height: 80vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('images/hero-bg.jpg') no-repeat center center/cover;
    color: white;
    border-radius: 10px;
    margin-bottom: 2rem;
}

.hero h1 {
    font-size: 3.5rem;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.5rem;
    margin-bottom: 2rem;
}

.scroll-down {
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    animation: bounce 2s infinite;
}

@keyframes bounce {
    0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
    40% { transform: translateY(-20px); }
    60% { transform: translateY(-10px); }
}

.intro-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-top: 3rem;
}

.card {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    text-align: center;
    box-shadow: var(--shadow);
    transition: var(--transition);
    cursor: pointer;
}

.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.card i {
    font-size: 3rem;
    color: var(--primary-color);
    margin-bottom: 1.5rem;
}

.card h3 {
    margin-bottom: 1rem;
    color: var(--secondary-color);
}

/* 游戏部分样式 */
.games-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
}

.game-card {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: var(--shadow);
    transition: var(--transition);
}

.game-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.game-img {
    height: 200px;
    overflow: hidden;
}

.game-img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: var(--transition);
}

.game-card:hover .game-img img {
    transform: scale(1.1);
}

.game-info {
    padding: 1.5rem;
}

.game-info h3 {
    margin-bottom: 0.5rem;
    color: var(--secondary-color);
}

.game-info p {
    color: var(--text-light);
    margin-bottom: 1rem;
}

.game-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1rem;
}

.tag {
    background-color: var(--light-color);
    color: var(--secondary-color);
    padding: 0.3rem 0.8rem;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: 500;
}

.play-btn {
    display: inline-block;
    background-color: var(--primary-color);
    color: white;
    padding: 0.6rem 1.2rem;
    border-radius: 5px;
    text-decoration: none;
    font-weight: 500;
    transition: var(--transition);
    border: none;
    cursor: pointer;
}

.play-btn:hover {
    background-color: #2980b9;
}

/* 故事部分样式 */
.story-container {
    position: relative;
    max-width: 800px;
    margin: 0 auto;
    padding: 0 1rem;
}

.story-timeline {
    position: relative;
    padding: 2rem 0;
}

.story-timeline::before {
    content: '';
    position: absolute;
    left: 50%;
    top: 0;
    bottom: 0;
    width: 2px;
    background-color: var(--primary-color);
    transform: translateX(-50%);
}

.story-item {
    position: relative;
    margin-bottom: 2rem;
    width: 100%;
    display: flex;
    justify-content: flex-end;
    padding-right: 3rem;
}

.story-item:nth-child(even) {
    justify-content: flex-start;
    padding-left: 3rem;
    padding-right: 0;
}

.story-content {
    background: white;
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: var(--shadow);
    width: calc(50% - 2rem);
    position: relative;
}

.story-item:nth-child(even) .story-content::before {
    content: '';
    position: absolute;
    right: -10px;
    top: 20px;
    width: 0;
    height: 0;
    border-top: 10px solid transparent;
    border-bottom: 10px solid transparent;
    border-left: 10px solid white;
}

.story-item:nth-child(odd) .story-content::before {
    content: '';
    position: absolute;
    left: -10px;
    top: 20px;
    width: 0;
    height: 0;
    border-top: 10px solid transparent;
    border-bottom: 10px solid transparent;
    border-right: 10px solid white;
}

.story-date {
    position: absolute;
    top: 20px;
    width: 100px;
    background-color: var(--primary-color);
    color: white;
    padding: 0.3rem 0.6rem;
    border-radius: 20px;
    text-align: center;
    font-weight: 500;
}

.story-item:nth-child(odd) .story-date {
    left: -120px;
}

.story-item:nth-child(even) .story-date {
    right: -120px;
}

.story-content h3 {
    margin-bottom: 0.5rem;
    color: var(--secondary-color);
}

/* 小说部分样式 */
.novel-filter {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 1rem;
    margin-bottom: 2rem;
}

.filter-btn {
    background-color: var(--light-color);
    color: var(--secondary-color);
    border: none;
    padding: 0.6rem 1.2rem;
    border-radius: 20px;
    cursor: pointer;
    transition: var(--transition);
    font-weight: 500;
}

.filter-btn:hover, .filter-btn.active {
    background-color: var(--primary-color);
    color: white;
}

.novels-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 2rem;
}

.novel-card {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: var(--shadow);
    transition: var(--transition);
}

.novel-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.novel-cover {
    height: 300px;
    overflow: hidden;
}

.novel-cover img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.novel-info {
    padding: 1.5rem;
}

.novel-info h3 {
    margin-bottom: 0.5rem;
    color: var(--secondary-color);
}

.novel-meta {
    display: flex;
    justify-content: space-between;
    color: var(--text-light);
    font-size: 0.9rem;
    margin-bottom: 1rem;
}

.read-btn {
    display: inline-block;
    background-color: var(--primary-color);
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    text-decoration: none;
    font-weight: 500;
    transition: var(--transition);
}

.read-btn:hover {
    background-color: #2980b9;
}

/* 美景部分样式 */
.gallery-container {
    columns: 3 250px;
    gap: 1rem;
}

.gallery-item {
    margin-bottom: 1rem;
    break-inside: avoid;
    position: relative;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: var(--shadow);
    transition: var(--transition);
}

.gallery-item:hover {
    transform: scale(1.02);
}

.gallery-item img {
    width: 100%;
    height: auto;
    display: block;
    cursor: pointer;
}

.image-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: linear-gradient(transparent, rgba(0, 0, 0, 0.7));
    color: white;
    padding: 1rem;
    transform: translateY(100%);
    transition: var(--transition);
}

.gallery-item:hover .image-caption {
    transform: translateY(0);
}

/* 灯箱样式 */
.lightbox {
    display: none;
    position: fixed;
    z-index: 2000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.9);
    overflow: auto;
}

.lightbox-content {
    display: block;
    margin: 60px auto;
    max-width: 80%;
    max-height: 80%;
    animation: zoom 0.3s;
}

@keyframes zoom {
    from { transform: scale(0.8); }
    to { transform: scale(1); }
}

.close-btn {
    position: absolute;
    top: 20px;
    right: 30px;
    color: white;
    font-size: 40px;
    font-weight: bold;
    cursor: pointer;
    transition: var(--transition);
}

.close-btn:hover {
    color: var(--primary-color);
}

.caption {
    color: white;
    text-align: center;
    padding: 10px 0;
    font-size: 1.2rem;
}

.prev, .next {
    cursor: pointer;
    position: absolute;
    top: 50%;
    width: auto;
    padding: 16px;
    margin-top: -50px;
    color: white;
    font-weight: bold;
    font-size: 30px;
    transition: var(--transition);
    user-select: none;
}

.next {
    right: 0;
    border-radius: 3px 0 0 3px;
}

.prev {
    left: 0;
    border-radius: 0 3px 3px 0;
}

.prev:hover, .next:hover {
    background-color: rgba(0, 0, 0, 0.8);
}

/* 页脚样式 */
footer {
    background-color: var(--secondary-color);
    color: white;
    text-align: center;
    padding: 2rem;
    margin-top: 2rem;
}

.social-links {
    display: flex;
    justify-content: center;
    gap: 1.5rem;
    margin-bottom: 1.5rem;
}

.social-links a {
    color: white;
    font-size: 1.5rem;
    transition: var(--transition);
}

.social-links a:hover {
    color: var(--primary-color);
    transform: translateY(-5px);
}

/* 返回顶部按钮 */
#back-to-top {
    display: none;
    position: fixed;
    bottom: 20px;
    right: 20px;
    z-index: 99;
    border: none;
    outline: none;
    background-color: var(--primary-color);
    color: white;
    cursor: pointer;
    padding: 15px;
    border-radius: 50%;
    font-size: 1.2rem;
    width: 50px;
    height: 50px;
    transition: var(--transition);
    box-shadow: var(--shadow);
}

#back-to-top:hover {
    background-color: #2980b9;
    transform: translateY(-5px);
}

/* 响应式设计 */
@media (max-width: 768px) {
    nav {
        padding: 1rem;
    }
    
    .nav-links {
        position: absolute;
        right: 0;
        top: 70px;
        background-color: var(--secondary-color);
        width: 100%;
        flex-direction: column;
        align-items: center;
        padding: 1rem 0;
        clip-path: circle(0px at 90% -10%);
        transition: all 0.5s ease-out;
    }
    
    .nav-links.active {
        clip-path: circle(1000px at 90% -10%);
    }
    
    .nav-links li {
        margin: 1rem 0;
    }
    
    .burger {
        display: block;
    }
    
    .burger.active .line1 {
        transform: rotate(-45deg) translate(-5px, 6px);
    }
    
    .burger.active .line2 {
        opacity: 0;
    }
    
    .burger.active .line3 {
        transform: rotate(45deg) translate(-5px, -6px);
    }
    
    .hero h1 {
        font-size: 2.5rem;
    }
    
    .hero p {
        font-size: 1.2rem;
    }
    
    .story-timeline::before {
        left: 30px;
    }
    
    .story-item, .story-item:nth-child(even) {
        justify-content: flex-start;
        padding-left: 3rem;
        padding-right: 0;
    }
    
    .story-content {
        width: 100%;
    }
    
    .story-item:nth-child(odd) .story-date,
    .story-item:nth-child(even) .story-date {
        left: -120px;
        right: auto;
    }
    
    .story-item:nth-child(odd) .story-content::before,
    .story-item:nth-child(even) .story-content::before {
        left: -10px;
        right: auto;
        border-right: 10px solid white;
        border-left: none;
    }
}

@media (max-width: 480px) {
    .intro-cards {
        grid-template-columns: 1fr;
    }
    
    .section {
        padding: 2rem 1rem;
    }
    
    .section-title {
        font-size: 2rem;
    }
}
document.addEventListener('DOMContentLoaded', function() {
    // 导航栏切换
    const burger = document.querySelector('.burger');
    const navLinks = document.querySelector('.nav-links');
    const navItems = document.querySelectorAll('.nav-links li a');
    
    burger.addEventListener('click', () => {
        navLinks.classList.toggle('active');
        burger.classList.toggle('active');
    });
    
    // 平滑滚动和部分切换
    navItems.forEach(item => {
        item.addEventListener('click', (e) => {
            e.preventDefault();
            
            // 更新活动导航项
            navItems.forEach(link => link.classList.remove('active'));
            item.classList.add('active');
            
            // 关闭移动菜单
            navLinks.classList.remove('active');
            burger.classList.remove('active');
            
            // 获取目标部分
            const targetId = item.getAttribute('href');
            const targetSection = document.querySelector(targetId);
            
            // 隐藏所有部分
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('active');
            });
            
            // 显示目标部分
            targetSection.classList.add('active');
            
            // 平滑滚动到顶部
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
    });
    
    // 首页卡片点击事件
    const introCards = document.querySelectorAll('.intro-cards .card');
    introCards.forEach(card => {
        card.addEventListener('click', () => {
            const targetId = card.getAttribute('data-target');
            const targetSection = document.querySelector(targetId);
            
            // 更新活动导航项
            navItems.forEach(link => link.classList.remove('active'));
            document.querySelector(`.nav-links a[href="${targetId}"]`).classList.add('active');
            
            // 隐藏所有部分
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('active');
            });
            
            // 显示目标部分
            targetSection.classList.add('active');
            
            // 平滑滚动到顶部
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
    });
    
    // 返回顶部按钮
    const backToTopBtn = document.getElementById('back-to-top');
    window.addEventListener('scroll', () => {
        if (window.pageYOffset > 300) {
            backToTopBtn.style.display = 'block';
        } else {
            backToTopBtn.style.display = 'none';
        }
    });
    
    backToTopBtn.addEventListener('click', () => {
        window.scrollTo({
            top: 0,
            behavior: 'smooth'
        });
    });
    
    // 游戏数据加载
    const gamesData = [
        {
            id: 1,
            title: "太空冒险",
            description: "一个关于探索宇宙的2D平台游戏",
            image: "images/game1.jpg",
            tags: ["平台", "冒险", "2D"],
            link: "#"
        },
        {
            id: 2,
            title: "迷宫逃脱",
            description: "在迷宫中寻找出口的解谜游戏",
            image: "images/game2.jpg",
            tags: ["解谜", "策略", "3D"],
            link: "#"
        },
        {
            id: 3,
            title: "赛车竞速",
            description: "高速驾驶体验的赛车游戏",
            image: "images/game3.jpg",
            tags: ["竞速", "体育", "3D"],
            link: "#"
        },
        {
            id: 4,
            title: "农场物语",
            description: "经营自己的农场，种植作物和饲养动物",
            image: "images/game4.jpg",
            tags: ["模拟", "经营", "休闲"],
            link: "#"
        }
    ];
    
    const gamesContainer = document.querySelector('.games-container');
    
    function loadGames() {
        gamesContainer.innerHTML = '';
        
        gamesData.forEach(game => {
            const gameCard = document.createElement('div');
            gameCard.className = 'game-card';
            
            gameCard.innerHTML = `
                <div class="game-img">
                    <img src="${game.image}" alt="${game.title}">
                </div>
                <div class="game-info">
                    <h3>${game.title}</h3>
                    <p>${game.description}</p>
                    <div class="game-tags">
                        ${game.tags.map(tag => `<span class="tag">${tag}</span>`).join('')}
                    </div>
                    <button class="play-btn" data-game-id="${game.id}">试玩游戏</button>
                </div>
            `;
            
            gamesContainer.appendChild(gameCard);
        });
        
        // 添加游戏按钮事件
        document.querySelectorAll('.play-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const gameId = this.getAttribute('data-game-id');
                alert(`即将加载游戏ID: ${gameId}`);
                // 实际应用中这里会加载游戏iframe或跳转到游戏页面
            });
        });
    }
    
    // 故事数据加载
    const storiesData = [
        {
            date: "2023年6月",
            title: "毕业季",
            content: "大学四年的时光转瞬即逝，毕业典礼上看着熟悉的校园和同学，心中充满不舍和对未来的期待。"
        },
        {
            date: "2022年12月",
            title: "第一次滑雪",
            content: "冬天和朋友一起去滑雪场，虽然摔了很多次，但终于学会了基础的滑雪技巧，非常有趣的体验。"
        },
        {
            date: "2021年8月",
            title: "独自旅行",
            content: "第一次一个人背包旅行，去了云南大理和丽江，认识了很多有趣的人，看到了美丽的风景。"
        },
        {
            date: "2020年3月",
            title: "疫情居家",
            content: "因为疫情开始在家上网课，学会了做饭和很多新技能，也有了更多时间思考人生。"
        }
    ];
    
    const storyTimeline = document.querySelector('.story-timeline');
    
    function loadStories() {
        storyTimeline.innerHTML = '';
        
        storiesData.forEach((story, index) => {
            const storyItem = document.createElement('div');
            storyItem.className = `story-item ${index % 2 === 0 ? '' : 'even'}`;
            
            storyItem.innerHTML = `
                <div class="story-content">
                    <h3>${story.title}</h3>
                    <p>${story.content}</p>
                </div>
                <div class="story-date">${story.date}</div>
            `;
            
            storyTimeline.appendChild(storyItem);
        });
    }
    
    // 小说数据加载
    const novelsData = [
        {
            id: 1,
            title: "星辰大海",
            cover: "images/novel1.jpg",
            genre: "sci-fi",
            author: "我",
            chapters: 12,
            description: "一个关于星际探索和人类未来的科幻故事。"
        },
        {
            id: 2,
            title: "魔法学院",
            cover: "images/novel2.jpg",
            genre: "fantasy",
            author: "我",
            chapters: 8,
            description: "年轻魔法师在魔法学院的成长与冒险。"
        },
        {
            id: 3,
            title: "夏日恋歌",
            cover: "images/novel3.jpg",
            genre: "romance",
            author: "我",
            chapters: 5,
            description: "发生在海边的青春爱情故事。"
        },
        {
            id: 4,
            title: "未来战争",
            cover: "images/novel4.jpg",
            genre: "sci-fi",
            author: "我",
            chapters: 15,
            description: "人工智能与人类之间的终极对抗。"
        },
        {
            id: 5,
            title: "精灵王国",
            cover: "images/novel5.jpg",
            genre: "fantasy",
            author: "我",
            chapters: 10,
            description: "精灵与人类共同对抗黑暗势力的史诗故事。"
        },
        {
            id: 6,
            title: "城市月光",
            cover: "images/novel6.jpg",
            genre: "romance",
            author: "我",
            chapters: 7,
            description: "都市职场中的浪漫邂逅与成长。"
        }
    ];
    
    const novelsContainer = document.querySelector('.novels-container');
    const filterButtons = document.querySelectorAll('.filter-btn');
    
    function loadNovels(filter = 'all') {
        novelsContainer.innerHTML = '';
        
        const filteredNovels = filter === 'all' 
            ? novelsData 
            : novelsData.filter(novel => novel.genre === filter);
        
        filteredNovels.forEach(novel => {
            const novelCard = document.createElement('div');
            novelCard.className = 'novel-card';
            
            novelCard.innerHTML = `
                <div class="novel-cover">
                    <img src="${novel.cover}" alt="${novel.title}">
                </div>
                <div class="novel-info">
                    <h3>${novel.title}</h3>
                    <div class="novel-meta">
                        <span>${novel.author}</span>
                        <span>${novel.chapters}章</span>
                    </div>
                    <p>${novel.description}</p>
                    <a href="#" class="read-btn" data-novel-id="${novel.id}">阅读</a>
                </div>
            `;
            
            novelsContainer.appendChild(novelCard);
        });
        
        // 添加阅读按钮事件
        document.querySelectorAll('.read-btn').forEach(btn => {
            btn.addEventListener('click', function(e) {
                e.preventDefault();
                const novelId = this.getAttribute('data-novel-id');
                alert(`即将打开小说ID: ${novelId}`);
                // 实际应用中这里会跳转到小说阅读页面
            });
        });
    }
    
    // 小说筛选按钮事件
    filterButtons.forEach(button => {
        button.addEventListener('click', function() {
            // 更新活动按钮
            filterButtons.forEach(btn => btn.classList.remove('active'));
            this.classList.add('active');
            
            // 加载筛选后的小说
            const filter = this.getAttribute('data-filter');
            loadNovels(filter);
        });
    });
    
    // 美景图片数据加载
    const galleryData = [
        {
            id: 1,
            image: "images/scenery1.jpg",
            title: "雪山日出",
            location: "西藏"
        },
        {
            id: 2,
            image: "images/scenery2.jpg",
            title: "湖边日落",
            location: "青海湖"
        },
        {
            id: 3,
            image: "images/scenery3.jpg",
            title: "森林小径",
            location: "长白山"
        },
        {
            id: 4,
            image: "images/scenery4.jpg",
            title: "海边沙滩",
            location: "三亚"
        },
        {
            id: 5,
            image: "images/scenery5.jpg",
            title: "城市夜景",
            location: "上海"
        },
        {
            id: 6,
            image: "images/scenery6.jpg",
            title: "梯田风光",
            location: "云南"
        },
        {
            id: 7,
            image: "images/scenery7.jpg",
            title: "沙漠星空",
            location: "敦煌"
        },
        {
            id: 8,
            image: "images/scenery8.jpg",
            title: "古镇小巷",
            location: "乌镇"
        },
        {
            id: 9,
            image: "images/scenery9.jpg",
            title: "高山湖泊",
            location: "天山"
        }
    ];
    
    const galleryContainer = document.querySelector('.gallery-container');
    const lightbox = document.querySelector('.lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    const captionText = document.querySelector('.caption');
    const closeBtn = document.querySelector('.close-btn');
    const prevBtn = document.querySelector('.prev');
    const nextBtn = document.querySelector('.next');
    let currentImageIndex = 0;
    
    function loadGallery() {
        galleryContainer.innerHTML = '';
        
        galleryData.forEach((item, index) => {
            const galleryItem = document.createElement('div');
            galleryItem.className = 'gallery-item';
            
            galleryItem.innerHTML = `
                <img src="${item.image}" alt="${item.title}" data-index="${index}">
                <div class="image-caption">
                    <h4>${item.title}</h4>
                    <p>${item.location}</p>
                </div>
            `;
            
            galleryContainer.appendChild(galleryItem);
        });
        
        // 添加图片点击事件
        document.querySelectorAll('.gallery-item img').forEach(img => {
            img.addEventListener('click', function() {
                currentImageIndex = parseInt(this.getAttribute('data-index'));
                openLightbox(currentImageIndex);
            });
        });
    }
    
    function openLightbox(index) {
        lightbox.style.display = 'block';
        lightboxImg.src = galleryData[index].image;
        captionText.innerHTML = `<strong>${galleryData[index].title}</strong> - ${galleryData[index].location}`;
    }
    
    function closeLightbox() {
        lightbox.style.display = 'none';
    }
    
    function showPrevImage() {
        currentImageIndex = (currentImageIndex - 1 + galleryData.length) % galleryData.length;
        lightboxImg.src = galleryData[currentImageIndex].image;
        captionText.innerHTML = `<strong>${galleryData[currentImageIndex].title}</strong> - ${galleryData[currentImageIndex].location}`;
    }
    
    function showNextImage() {
        currentImageIndex = (currentImageIndex + 1) % galleryData.length;
        lightboxImg.src = galleryData[currentImageIndex].image;
        captionText.innerHTML = `<strong>${galleryData[currentImageIndex].title}</strong> - ${galleryData[currentImageIndex].location}`;
    }
    
    // 灯箱事件
    closeBtn.addEventListener('click', closeLightbox);
    prevBtn.addEventListener('click', showPrevImage);
    nextBtn.addEventListener('click', showNextImage);
    
    lightbox.addEventListener('click', (e) => {
        if (e.target === lightbox) {
            closeLightbox();
        }
    });
    
    // 键盘导航
    document.addEventListener('keydown', (e) => {
        if (lightbox.style.display === 'block') {
            if (e.key === 'Escape') {
                closeLightbox();
            } else if (e.key === 'ArrowLeft') {
                showPrevImage();
            } else if (e.key === 'ArrowRight') {
                showNextImage();
            }
        }
    });
    
    // 初始化加载所有数据
    loadGames();
    loadStories();
    loadNovels();
    loadGallery();
    
    // 设置首页为活动状态
    document.querySelector('#home').classList.add('active');
    document.querySelector('.nav-links a[href="#home"]').classList.add('active');
});
