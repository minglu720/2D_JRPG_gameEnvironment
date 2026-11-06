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
- `references/assets/style-references/`：随 Skill 保存的视觉参考图
- `evals/evals.json`：用于检查 Skill 行为的示例请求和预期结果

## 在 Codex 中安装

在 Codex 中调用 `$skill-installer`，并让它从这个仓库地址安装 Skill：`https://github.com/minglu720/2D_JRPG_gameEnvironment`。

安装后，可以用 `$anime-scene-background` 显式调用；也可以直接提出符合它用途的图片风格处理任务。如果 Skill 没出现在选择器里，重启 Codex。
