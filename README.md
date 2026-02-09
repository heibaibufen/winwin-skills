# winwin-skills 使用指南

Claude Code 技能仓库使用说明

## 安装

### 方法 1：使用 uv tool（推荐）

1. **安装 uv**（如果未安装）

```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# 或使用 pip
pip install uv

# Windows
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

2. **安装 winwin-cli**

```bash
# 使用 uv tool 安装（推荐）
uv tool install winwin-cli

# 或使用 uv pip
uv pip install winwin-cli

# 或使用 pip
pip install winwin-cli
```

2. **列出可用技能**
```bash
winwin-cli skills list
```

3. **安装技能**
```bash
# 安装到 Claude Code
winwin-cli skills install winwin-cli --platform claude-code
winwin-cli skills install vega-lite-charts --platform claude-code
```

### 方法 2：手动安装

```bash
# 克隆仓库
git clone https://github.com/heibaibufen/winwin-skills.git
cd winwin-skills

# 复制技能到 Claude Code 目录
cp -r skills/* ~/.claude/skills/
```

## 使用

### winwin-cli 技能

在 Claude Code 中直接使用，无需手动调用命令。

**示例**：
- "把这个 PDF 转换为 Markdown"
- "搜索我的文档中关于 API 的内容"
- "安装 git-workflow 技能"

### vega-lite-charts 技能

在 Claude Code 中描述你需要的图表：

**示例**：
- "创建一个饼图展示销售数据"
- "生成一个中国地图展示各省份分布"
- "画一个四象限分析图"

## 技能目录结构

```
skills/
├── winwin-cli/          # 命令行工具集
│   ├── SKILL.md
│   ├── convert/         # 文档转换
│   ├── kb-search/       # 知识库检索
│   └── skills/          # 技能管理
└── vega-lite-charts/    # 图表可视化
    ├── SKILL.md
    └── [各种图表类型]/
```

## 常见问题

**技能未生效？**
- 确认技能已复制到 `~/.claude/skills/` 目录
- 重启 Claude Code

**winwin-cli 命令未找到？**
```bash
# 检查安装
which winwin-cli
winwin-cli --version
```

**更多问题？**
- 查看各技能目录下的 SKILL.md 文档
- 提交 issue 到 [https://github.com/heibaibufen/winwin-skills](https://github.com/heibaibufen/winwin-skills)
