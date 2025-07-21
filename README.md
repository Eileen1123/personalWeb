<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>【我的名字/昵称】的个人主页</title>
    <style>
        /* 页面整体样式 */
        body {
            font-family: 'Helvetica Neue', Arial, 'Hiragino Sans GB', 'Microsoft YaHei', sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f0f2f5;
            color: #333;
            line-height: 1.8;
        }
        /* 内容主容器 */
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px 40px;
            background-color: #ffffff;
            border-radius: 12px;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
        }
        /* 顶部标题和介绍 */
        .header {
            text-align: center;
            border-bottom: 2px solid #eee;
            padding-bottom: 20px;
            margin-bottom: 30px;
        }
        .header h1 {
            font-size: 2.5em;
            color: #2c3e50;
            margin: 10px 0;
        }
        .header p {
            font-size: 1.1em;
            color: #7f8c8d;
        }
        /* 照片区域 */
        .photo-gallery {
            text-align: center;
            margin: 30px 0;
        }
        .photo-gallery img {
            max-width: 80%;
            height: auto;
            border-radius: 8px;
            border: 5px solid #fff;
            box-shadow: 0 4px 15px rgba(0,0,0,0.15);
            transition: transform 0.3s ease;
        }
        .photo-gallery img:hover {
            transform: scale(1.05) rotate(2deg);
        }
        /* 内容区块样式 */
        .section {
            margin-bottom: 30px;
            padding: 20px;
            background-color: #fafafa;
            border-left: 5px solid #3498db;
            border-radius: 8px;
        }
        .section h2 {
            margin-top: 0;
            color: #3498db;
            font-size: 1.5em;
        }
        .section p, .section blockquote {
            font-size: 1.1em;
        }
        /* 可点击揭晓答案的样式 */
        .reveal {
            background-color: #e9ecef;
            padding: 15px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .reveal:hover {
            background-color: #dde2e6;
        }
        .reveal .answer {
            display: none; /* 默认隐藏答案 */
            margin-top: 10px;
            color: #e74c3c;
            font-weight: bold;
        }
        /* 2026寄语的特殊样式 */
        .future-message {
            border-left-color: #f1c40f;
        }
        .future-message h2 {
            color: #f1c40f;
        }
        blockquote {
            border-left: 4px solid #ccc;
            padding-left: 15px;
            margin: 0;
            color: #555;
            font-style: italic;
        }
        /* 网页页脚 */
        footer {
            text-align: center;
            margin-top: 40px;
            color: #999;
            font-size: 0.9em;
        }
    </style>
</head>
<body>

    <div class="container">

        <div class="header">
            <h1>✨ 【我的名字/昵称】 ✨</h1>
            <p>🎓【一句话介绍学习经历，例如：一个正在计算机科学领域努力搬砖的奋斗者】</p>
        </div>

        <div class="photo-gallery">
            <h2>📸 我的靓照/沙雕照 📸</h2>
            <img src="placeholder.jpg" alt="我的照片">
            </div>

        <div class="section">
            <h2>🍜 我的美食最爱 🍜</h2>
            <p>人是铁，饭是钢，我最爱的是 <strong>【没有火锅的冬天是不完整的！🍲】</strong>！</p>
        </div>

        <div class="section">
            <h2>🪁 学习之余，我最大的爱好是... 🪁</h2>
            <p>放下书本，我就会立刻投身于 <strong>【在代码之外，我沉迷于用相机捕捉生活中的光影瞬间！📷】</strong> 的世界！</p>
        </div>

        <div class="section">
            <h2>🔮 关于我的一些“小标签” 🔮</h2>
            <p><strong>星座：</strong> 【好奇心爆棚的双子座♊️】</p>
            <p><strong>MBTI：</strong> 【ENFP，快乐修狗就是我！🐶】</p>
        </div>

        <div class="section">
            <h2>🤫 我的隐藏技能 🤫</h2>
            <div class="reveal" onclick="toggleReveal(this)">
                <p>很多人不知道，我其实超会... (点击揭晓)</p>
                <div class="answer">
                    <p>【徒手开椰子🥥 / 模仿海绵宝宝笑声 / 一分钟内记住一副打乱的扑克牌】！是的，你没看错！</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>😅 一件让我记忆犹新的糗事 😅</h2>
             <div class="reveal" onclick="toggleReveal(this)">
                <p>那是一个风和日丽的下午，我竟然... (点击查看我的黑历史)</p>
                <div class="answer">
                    <p>【在图书馆里戴着耳机听歌，以为没人听见，结果跟着唱破了音... 全场安静，我只想钻进地缝里。】</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🤏 我的一个小毛病/小缺点 🤏</h2>
            <p>人无完人嘛，我承认我在 <strong>【拖延症晚期患者，deadline是第一生产力】</strong> 方面还有待提高~</p>
        </div>

        <div class="section future-message">
            <h2>💌 对 2026 年的自己说句话 💌</h2>
            <blockquote>
                <p>"Hi，一年后的我，希望你 <strong>【已经掌握了新的编程语言，并且依旧热爱生活，保持好奇！】</strong>"</p>
            </blockquote>
        </div>

        <footer>
            <p>页面生成于 2025年7月。由 Gemini 智能助理协助创建。</p>
        </footer>
    </div>

    <script>
        function toggleReveal(element) {
            const answer = element.querySelector('.answer');
            if (answer.style.display === 'block') {
                answer.style.display = 'none';
            } else {
                answer.style.display = 'block';
            }
        }
    </script>

</body>
</html>
