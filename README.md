# Miya Assistant - Web 版

一个基于浏览器的 AI 聊天应用，兼容妹居物语的日记格式。

## 功能

- ✅ 导入妹居物语日记 JSON
- ✅ 根据好感度自动切换人设卡片
- ✅ 每次对话后自动写日记
- ✅ 自动提取重要事件为一句话记忆
- ✅ 记忆之间可互相关联
- ✅ 每次对话前回忆日记和记忆
- ✅ 对话中实时联想历史记忆
- ✅ 流式输出（打字机效果）
- ✅ PWA 支持（可安装到手机桌面）
- ✅ 数据本地存储（localStorage + 导出备份）

## 部署方式

### 方式一：GitHub Pages（推荐）

1. Fork 或创建新仓库
2. 把 `index.html` 和 `manifest.json` 上传到仓库根目录
3. 进入仓库 Settings → Pages → Source 选择 main 分支
4. 访问 `https://你的用户名.github.io/仓库名/`

### 方式二：本地使用

直接双击 `index.html` 打开即可（需要联网访问 API）。

### 方式三：其他静态托管

Vercel、Netlify、Cloudflare Pages 等都支持，直接部署即可。

## 使用说明

1. 打开应用后，点击左上角 ☰ 进入设置
2. 填入 API 地址和 Key（支持 DeepSeek、OpenAI、Claude 等兼容 API）
3. 点击「📁 导入日记 JSON」导入你的妹居物语存档
4. 开始对话！

## API 配置

| 服务商 | API 地址 | 模型 |
|--------|---------|------|
| DeepSeek | `https://api.deepseek.com/v1` | deepseek-chat |
| OpenAI | `https://api.openai.com/v1` | gpt-4o |
| 本地 Ollama | `http://localhost:11434/v1` | llama3 |

## 注意事项

- 所有数据存储在浏览器 localStorage 中，清除浏览器数据会丢失
- 请定期使用「📥 导出数据」功能备份
- API Key 只存在本地，不会上传到任何服务器
- 首次导入日记后，系统会自动从日记中提取重要记忆碎片
