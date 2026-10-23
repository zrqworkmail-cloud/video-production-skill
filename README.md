# Video Production Skill

面向 Codex 的通用视频制作 Skill。适用于剧情短片、社交视频、纪录片、解说、产品视频、动态图形，以及使用生成式模型的视频项目。

它从当前项目阶段继续工作，组织剧本、镜头、素材、生成、剪辑与审片。具体工具由项目决定：可以使用已有素材、ComfyUI/本地模型、代码时间线或现有剪辑软件。Skill 本身不附带模型、渲染器、付费接口或影片素材。

## 安装

把这个仓库链接交给 Codex，并说明：

> 请安装 https://github.com/zrqworkmail-cloud/video-production-skill 中的 skills/video-production 技能。

也可将 `skills/video-production` 整个目录复制到 Codex 的用户级 Skills 目录 `$CODEX_HOME/skills/`。请保留 `references/`，并在新的会话中确认技能已被发现。

用户级安装可供不同项目调用；项目自身的指令和技术约束仍然适用。自动选择是否触发由宿主决定，也可以明确调用 `$video-production`。本仓库不会修改全局配置或自动安装其他技能。

## 使用示例

- `$video-production 根据这些资料制作一支 60 秒的竖屏科普视频，先完成剧本和分镜。`
- `$video-production 接着当前项目制作，保留已确认的人物和风格。`
- `$video-production 检查这些镜头的人物动作和接镜，修改生成提示词；GPU 正忙时只准备任务。`
- `$video-production 给已有宣传片修改末尾五秒，并验证导出文件。`

## 执行方式

1. 读取项目现状、用户要求和已确认决策，判断当前制作阶段。
2. 按需要准备简报、剧本、分镜、连续性记录和素材。
3. 使用项目适合的工具制作可审查的镜头或短场景，再逐步放回时间线。
4. 针对问题层修复，保留来源、版本和已认可素材。
5. 审查画面、声音与上下文，再单独检查文件的编码、尺寸、时长和可播放性。

简单修改直接处理相关部分。新风格、新模型或昂贵批量任务先做代表性试样；费用、上传、安装和共享算力按已有用户授权执行。图片内文字和独立文字层都可以使用，以视觉意图、准确性和后续编辑需求选择。

## 文件

- [SKILL.md](skills/video-production/SKILL.md)：入口与通用制作决策。
- [generative-shots.md](skills/video-production/references/generative-shots.md)：生成式镜头、提示词、模型参数和本地任务的按需指导。
- [REVIEW.md](REVIEW.md)：本次审查、验证方法与已知限制。
- [SOURCES.md](SOURCES.md)：方法来源和适用边界。

## 验证状态

已通过 Codex skill-creator 的结构校验和人工静态审查。尚未对所有题材、宿主、模型和渲染器做独立端到端验证。技能格式有效不等于成片质量保证；真实生成、动态画面、声音和硬件状态需在具体项目中检查。

## License

原创文本使用 [MIT License](LICENSE)。本仓库引用外部方法链接，未打包其代码、镜头库、音频、模型或模板；外部资源各自的许可继续适用。
