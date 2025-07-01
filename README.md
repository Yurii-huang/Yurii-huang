# 👋 Welcome to Yurii's GitHub!

<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yurii's GitHub Stats</title>
</head>
<body>
    <div id="stats-container">
        <!-- 占位元素，后续通过 JS 动态填充内容 -->
    </div>

    <script>
        function updateStats() {
            const isDarkMode = window.matchMedia('(prefers-color-scheme: dark)').matches;
            const statsContainer = document.getElementById('stats-container');
            let statsHTML;

            if (isDarkMode) {
                // 深色模式卡片
                statsHTML = `
                    <div>
                        <img height="150px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Yurii-huang&show_icons=true&theme=tokyonight&layout=compact" />
                        <img height="150px" src="https://github-readme-stats.vercel.app/api?username=Yurii-huang&show_icons=true&theme=tokyonight" />
                    </div>
                `;
            } else {
                // 浅色模式卡片
                statsHTML = `
                    <div>
                        <img height="150px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Yurii-huang&show_icons=true&theme=default&layout=compact" />
                        <img height="150px" src="https://github-readme-stats.vercel.app/api?username=Yurii-huang&show_icons=true&theme=default" />
                    </div>
                `;
            }

            statsContainer.innerHTML = statsHTML;
        }

        // 初始加载时更新统计卡片
        updateStats();

        // 监听系统主题变化
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', updateStats);
    </script>
</body>
</html>
