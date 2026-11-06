# Anime Scene Background Skill

一个用于将照片或场景描述转化为克制的动漫风格游戏环境背景的 Codex Skill。它将场景结构与美术风格分别处理，并支持控制画面细节保留程度。

## 美术方向

- 平视的中远景，安静、客观地呈现场景
- 以环境为主体，保留清晰可读的建筑和空间关系
- 可在稀疏、平衡、丰富三档间调整细节密度
- 默认不添加人物、戏剧化机位、强叙事构图或角色互动空间

## 仓库内容

- `SKILL.md`：完整的 Skill 指令
- `references/prompt-examples.md`：常见场景风格化任务的提示词范例
- `evals/evals.json`：用于检查 Skill 行为的示例请求和预期结果

## 安装

将整个仓库文件夹复制到 Codex 的 Skills 目录，并命名为 `anime-scene-background`：

- 如果设置了 `CODEX_HOME`，放到 `$CODEX_HOME/skills/anime-scene-background`
- 否则放到 `~/.codex/skills/anime-scene-background`

之后可以在请求中使用 `$anime-scene-background` 调用它。
