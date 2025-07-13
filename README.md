```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>探寻互联网新世界 - 互联网影响新体验</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #3a86ff;
            --secondary: #8338ec;
            --accent: #ff006e;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #06d6a0;
            --warning: #ffd166;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
        }
        
        body::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 300px;
            background: linear-gradient(120deg, var(--primary), var(--secondary));
            z-index: -1;
            clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
}
        
        header {
            text-align: center;
            padding: 40px 20px 30px;
            color: white;
            position: relative;
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }
        
        .subtitle {
            font-size: 1.4rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto 30px;
            font-weight: 300;
        }
        
        .learning-objectives {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 20px;
            max-width: 900px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 15px;
        }
        
        .objective-card {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 12px;
            padding: 15px;
            color: var(--dark);
            display: flex;
            align-items: center;
            transition: transform 0.3s ease;
        }
        
        .objective-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }
        
        .objective-card i {
            font-size: 2rem;
            margin-right: 15px;
            color: var(--primary);
        }
        
        .tabs-container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            overflow: hidden;
            margin-top: 30px;
        }
        
        .tabs {
            display: flex;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            padding: 0 20px;
        }
        
        .tab {
            padding: 18px 30px;
            cursor: pointer;
            color: white;
            font-weight: 500;
            position: relative;
            transition: all 0.3s;
        }
        
        .tab.active {
            background: rgba(255, 255, 255, 0.2);
        }
        
        .tab::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: var(--warning);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }
        
        .tab.active::after {
            transform: scaleX(1);
        }
        
        .tab-content {
            padding: 30px;
            display: none;
        }
        
        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        section {
            margin-bottom: 40px;
        }
        
        .section-title {
            font-size: 1.8rem;
            color: var(--secondary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid var(--warning);
display: inline-block;
        }
        
        .cards-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 25px;
        }
        
        .card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .card-header {
            background: linear-gradient(120deg, var(--primary), var(--secondary));
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 1.4rem;
            font-weight: 600;
        }
        
        .card-content {
            padding: 20px;
        }
        
        .card-content ul {
            padding-left: 20px;
            margin: 15px 0;
        }
        
        .card-content li {
            margin-bottom: 10px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 25px;
            background: var(--primary);
            color: white;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            margin-top: 15px;
            border: none;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(58, 134, 255, 0.3);
        }
        
        .btn:hover {
            background: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(131, 56, 236, 0.4);
        }
        
        .question-container {
            background: linear-gradient(135deg, #f6d365 0%, #fda085 100%);
            border-radius: 15px;
            padding: 25px;
            margin: 30px 0;
            color: var(--dark);
        }
        
        .question-title {
            font-size: 1.6rem;
            margin-bottom: 15px;
            color: #d9480f;
        }
        
        .options {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin: 20px 0;
        }
        
        .option {
            flex: 1;
            min-width: 200px;
            background: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            text-align: center;
            font-weight: 500;
        }
        
        .option:hover {
            background: white;
            transform: scale(1.03);
        }
        
        .option.selected {
            background: var(--success);
            color: white;
            transform: scale(1.05);
        }
        
        textarea {
            width: 100%;
            min-height: 150px;
            padding: 15px;
            border-radius: 10px;
            border: 2px solid #ddd;
            margin: 20px 0;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        textarea:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(58, 134, 255, 0.2);
        }
        
        .resources {
display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .resource-card {
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
            transition: all 0.3s;
        }
        
        .resource-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }
        
        .resource-card h3 {
            margin-bottom: 15px;
            color: var(--secondary);
        }
        
        .assignment {
            background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
            border-radius: 15px;
            padding: 25px;
            margin-top: 40px;
        }
        
        .footer {
            text-align: center;
            padding: 40px 20px;
            color: white;
            margin-top: 50px;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @media (max-width: 768px) {
            .tabs {
                flex-wrap: wrap;
            }
            
            .tab {
                flex: 1 0 120px;
                text-align: center;
                padding: 15px 10px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .subtitle {
                font-size: 1.1rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>探寻互联网新世界</h1>
            <p class="subtitle">第3课 互联网影响新体验 - 探索互联网对各行业及文化传承的影响</p >
            
            <div class="learning-objectives">
                <div class="objective-card">
                    <i class="fas fa-user"></i>
                    <div>了解互联网对个人生活的影响</div>
                </div>
                <div class="objective-card">
                    <i class="fas fa-industry"></i>
                    <div>了解互联网对社会各行业的影响</div>
                </div>
                <div class="objective-card">
                    <i class="fas fa-landmark"></i>
                    <div>了解互联网对文化传承的影响</div>
                </div>
                <div class="objective-card">
                    <i class="fas fa-balance-scale"></i>
                    <div>感受互联网带来的便利和挑战</div>
                </div>
            </div>
        </header>
        
        <div class="tabs-container">
            <div class="tabs">
                <div class="tab active" data-tab="personal">互联网与个人生活</div>
                <div class="tab" data-tab="industry">互联网+各行各业</div>
                <div class="tab" data-tab="culture">互联网与文化传承</div>
                <div class="tab" data-tab="summary">课堂总结与作业</div>
            </div>
            
            <div class="tab-content active"
id="personal-content">
                <section>
                    <h2 class="section-title">互联网在个人生活中的应用</h2>
                    <p>互联网已经深度融入我们的日常生活，在沟通交流、学习娱乐等方面带来了革命性变化。</p >
                    
                    <div class="question-container">
                        <h3 class="question-title">问题情景:</h3>
                        <p>请从以下应用中选择一个方面，详细介绍其对你生活、学习的影响：</p >
                        
                        <div class="options">
                            <div class="option" data-option="learning">网络学习</div>
                            <div class="option" data-option="communication">网络交流</div>
                            <div class="option" data-option="entertainment">网络娱乐</div>
                        </div>
                        
                        <textarea placeholder="请在此输入你的回答..."></textarea>
                        <button class="btn" id="submit-answer">提交回答</button>
                    </div>
                    
                    <div class="cards-container">
                        <div class="card">
                            <div class="card-header">网络学习</div>
                            <div class="card-content">
                                <p>互联网彻底改变了传统学习方式：</p >
                                <ul>
                                    <li>丰富的在线课程和教育资源</li>
                                    <li>不受时间和空间限制的学习机会</li>
                                    <li>个性化学习路径和进度安排</li>
                                    <li>全球优质教育资源的普及</li>
                                </ul>
                                了解更多
                            </div>
                        </div>
                        
                        <div class="card">
                            <div class="card-header">网络交流</div>
                            <div class="card-content">
                                <p>社交方式的数字化变革：</p >
                                <ul>
                                    <li>即时通讯跨越地理限制</li>
                                    <li>社交媒体的文化与思想交流</li>
                                    <li>在线协作工具的广泛应用</li>
                                    <li>全球化的社交网络建立</li>
                                </ul>
                                了解更多
                            </div>
                        </div>
                        
                        <div class="card">
                            <div class="card-header">网络娱乐</div>
                            <div class="card-content">
                                <p>娱乐产业的数字化转型：</p >
                                <ul>
                                    <li>流媒体平台的兴起</li>
                                    <li>网络游戏和电子竞技</li>
                                    <li>自媒体和内容创作</li>
                                    <li>虚拟现实娱乐体验</li>
                                </ul>
                                了解更多
</div>
                        </div>
                    </div>
                </section>
            </div>
            
            <div class="tab-content" id="industry-content">
                <section>
                    <h2 class="section-title">各行各业的"互联网+"</h2>
                    <p>随着互联网的普及，农业、工业、教育、科研、医疗、交通等领域都出现了"互联网+"的趋势。我国在"互联网+"的创新应用上已处于世界领先地位。</p >
                    
                    <div class="cards-container">
                        <div class="card">
                            <div class="card-header">互联网+农业</div>
                            <div class="card-content">
                                <p>"互联网+"是推进农业现代化的必要手段：</p >
                                <ul>
                                    <li>智能灌溉系统</li>
                                    <li>精准种植技术</li>
                                    <li>农产品质量追溯系统</li>
                                    <li>农产品电子商务平台</li>
                                </ul>
                                <button class="btn resource-btn" data-resource="agriculture">查看农业案例</button>
                            </div>
                        </div>
                        
                        <div class="card">
                            <div class="card-header">互联网+工业</div>
                            <div class="card-content">
                                <p>我国在"5G+工业互联网"体系化发展走在全球前列：</p >
                                <ul>
                                    <li>智能制造技术应用</li>
                                    <li>工业生产过程优化</li>
                                    <li>供应链数字化管理</li>
                                    <li>预测性设备维护</li>
                                </ul>
                                <button class="btn resource-btn" data-resource="industry">查看工业案例</button>
                            </div>
                        </div>
                        
                        <div class="card">
                            <div class="card-header">互联网+科研</div>
                            <div class="card-content">
                                <p>信息技术改变着科学研究的方方面面：</p >
                                <ul>
                                    <li>大型科研设备联网协作</li>
                                    <li>科研数据云存储与分析</li>
                                    <li>全球科研合作平台</li>
                                    <li>开放科学数据共享</li>
                                </ul>
<button class="btn resource-btn" data-resource="research">查看科研案例</button>
                            </div>
                        </div>
                        
                        <div class="card">
                            <div class="card-header">互联网+教育</div>
                            <div class="card-content">
                                <p>构建网络化、数字化、个性化教育体系：</p >
                                <ul>
                                    <li>翻转课堂教学模式</li>
                                    <li>微课和慕课(MOOC)平台</li>
                                    <li>人工智能辅助教学</li>
                                    <li>虚拟现实学习环境</li>
                                </ul>
                                <button class="btn resource-btn" data-resource="education">查看教育案例</button>
                            </div>
                        </div>
                    </div>
                </section>
            </div>
            
            <div class="tab-content" id="culture-content">
                <section>
                    <h2 class="section-title">互联网与文化传承</h2>
                    <p>互联网与文化的融合催生了新生态、新平台，推动了传统文化的创造性转化与创新性发展。</p >
                    
                    <div class="resources">
                        <div class="resource-card">
                            <h3>数字文物库</h3>
                            <p>访问故宫博物院网站的数字文物库，感受互联网如何让文物"活"起
