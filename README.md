
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>✨ 朱玲仪的个人主页</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&display=swap');
        
        body {
            font-family: 'Noto Sans SC', sans-serif;
            background: linear-gradient(135deg, #fce7f3 0%, #fecdd3 100%);
        }
        
        .card {
            background: white;
            border-radius: 0.75rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            transition: all 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        
        .btn {
            padding: 0.5rem 1rem;
            border: 1px solid #d1d5db;
            border-radius: 0.375rem;
            background: white;
            cursor: pointer;
            transition: all 0.2s;
        }
        
        .btn:hover {
            background: #f3f4f6;
        }
        
        .hidden-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
        }
        
        .hidden-content.show {
            max-height: 500px;
        }
        
        .fade-in {
            animation: fadeIn 0.3s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body class="min-h-screen py-12 px-4">
    <div class="max-w-4xl mx-auto">
        <!-- 个人信息头部 -->
        <div class="text-center mb-12">
            <h1 class="text-4xl md:text-5xl font-bold text-pink-700 mb-4" style="font-family: KaiTi, serif;">
                ✨ 朱玲仪（Eileen） ✨
            </h1>
            <p class="text-xl text-gray-600 max-w-2xl mx-auto">
                🎓 毕业于波士顿大学数据分析专业，现在在项目上完成作为Operation Analyst的相关工作
            </p>
        </div>

        <!-- 照片展示 -->
        <div class="card mb-12">
            <div class="p-6">
                <h2 class="text-xl font-bold mb-4 flex items-center">
                    📸 我的靓照
                </h2>
                <img src="WechatIMG221.jpg" 
                     alt="我的照片" 
                     class="rounded-lg mx-auto object-cover w-full h-96">
            </div>
        </div>

        <!-- 美食最爱 -->
        <div class="card mb-12">
            <div class="p-6">
                <h2 class="text-xl font-bold mb-4 flex items-center">
                    🍖 我的美食最爱
                </h2>
                <div class="flex flex-col items-center">
                    <img src="BBQ.jpg" 
                         alt="最爱的烤肉" 
                         class="rounded-lg mx-auto object-cover w-full h-64 mb-4">
                    <p class="text-lg text-center">
                        没有烤肉的夏天是不完整的！<span class="font-bold text-red-500">滋滋作响的烤肉才是灵魂伴侣！🥩</span>
                    </p>
                </div>
            </div>
        </div>

        <!-- 兴趣爱好 -->
        <div class="card mb-12">
            <div class="p-6">
                <h2 class="text-xl font-bold mb-4 flex items-center">
                    🎮 学习之余，我最大的爱好是...
                </h2>
                <div class="flex flex-col md:flex-row items-center gap-8">
                    <img src="Gaming.jpg" 
                         alt="我的爱好" 
                         class="rounded-lg mx-auto object-cover w-full md:w-1/2 h-64">
                    <div class="text-lg md:text-xl">
                        <p class="mb-2">放下书本，我就会立刻投身于</p>
                        <p class="font-bold text-purple-600 mb-2">唱歌和打游戏</p>
                        <p>最常玩的游戏是 <span class="font-bold text-orange-500">守望先锋</span>！</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- 个人信息卡片 -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
            <!-- 小标签 -->
            <div class="card">
                <div class="p-6">
                    <h2 class="text-xl font-bold mb-4 flex items-center">
                        🔮 关于我的一些"小标签"
                    </h2>
                    <div class="space-y-4">
                        <div>
                            <p class="font-medium">星座：</p>
                            <p class="text-lg">♉️ 省钱与奢华的矛盾体：在不感兴趣的地方极度抠门，在热爱的事物上一掷千金。</p>
                        </div>
                        <div>
                            <p class="font-medium">MBTI：</p>
                            <p class="text-lg">🔧 ISTP，动手达人就是我！喜欢把想法变成现实</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 隐藏技能 -->
            <div class="card">
                <div class="p-6">
                    <h2 class="text-xl font-bold mb-4 flex items-center">
                        🤫 我的隐藏技能
                    </h2>
                    <p class="text-lg text-gray-600"></p>
                </div>
            </div>
        </div>

        <!-- 糗事和小缺点 -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
            <!-- 糗事卡片 -->
            <div class="card">
                <div class="p-6">
                    <h2 class="text-xl font-bold mb-4 flex items-center">
                        😅 让我记忆犹新的糗事
                    </h2>
                    <button onclick="toggleContent('embarrassing')" class="btn mb-4">
                        <span id="embarrassing-btn">点击查看糗事</span>
                    </button>
                    <div id="embarrassing-content" class="hidden-content">
                        <p class="text-lg fade-in">
                            在第一年留学的时候跟朋友购物，在结账时收银员问我：How's your day today， 我听成了How's your date，并说我不是同性恋，没有在dating😂
                        </p>
                    </div>
                </div>
            </div>

            <!-- 小缺点卡片 -->
            <div class="card">
                <div class="p-6">
                    <h2 class="text-xl font-bold mb-4 flex items-center">
                        🙈 我的小缺点
                    </h2>
                    <button onclick="toggleContent('quirks')" class="btn mb-4">
                        <span id="quirks-btn">点击查看缺点</span>
                    </button>
                    <div id="quirks-content" class="hidden-content">
                        <p class="text-lg fade-in">
                            人无完人嘛，我承认我是 <span class="font-bold text-purple-500">重度懒癌患者</span>！
                            能躺着绝不坐着，能坐着绝不站着，床就是我的第二个家～
                            每次周末计划要早起学习，结果都在床上和被子缠绵到中午😴
                        </p>
                    </div>
                </div>
            </div>
        </div>

        <!-- 未来寄语 -->
        <div class="card" style="background: linear-gradient(135deg, #fce7f3 0%, #fecdd3 100%); border: none;">
            <div class="p-6">
                <h2 class="text-xl font-bold mb-4 flex items-center">
                    💌 对 2026 年的自己说句话
                </h2>
                <div class="flex flex-col items-center text-center">
                    <p class="text-2xl font-bold text-pink-700">
                        "Hi，一年后的我，希望你能够在项目上成为一个成熟的能为团队兜底的OA，并且游戏技术更上一层楼！🎮"
                    </p>
                </div>
            </div>
        </div>
    </div>

    <script>
        function toggleContent(id) {
            const content = document.getElementById(id + '-content');
            const btn = document.getElementById(id + '-btn');
            
            if (content.classList.contains('show')) {
                content.classList.remove('show');
                btn.textContent = '点击' + (id === 'embarrassing' ? '查看糗事' : '查看缺点');
            } else {
                content.classList.add('show');
                btn.textContent = '收起';
            }
        }
    </script>
</body>
</html>
