# Developer Learning Master Skill

面向 Java 开发人员的通用技术教材生成 Skill。可用于 Codex 等支持 Agent Skills 规范的编程助手。

## 安装到当前项目

将压缩包内的 `.agents/skills/developer-learning-master/` 目录复制到你的项目根目录，最终结构为：

```text
your-project/
└── .agents/
    └── skills/
        └── developer-learning-master/
            ├── SKILL.md
            ├── references/
            └── assets/
```

## 安装为个人级 Skill

如果你的 Codex 环境支持用户级 Skills，可将 `developer-learning-master` 文件夹复制到 Codex 用户 Skills 目录。不同客户端/版本的发现路径可能不同；若未识别，优先使用项目级 `.agents/skills/` 路径，并重启或重新加载 Codex。

## 调用示例

```text
使用 $developer-learning-master，为我生成一套 Redis 7.x 系统化学习教材。
请自动应用 Skill 中的全部通用教材标准，结合 Redis 技术特点规划内容。
先输出版本假设、资料来源、完整学习路线和章节目录；确认后再分章节生成 Markdown 文件。
```

```text
使用 $developer-learning-master，生成 Redis 7.x 学习文档，
重点解释底层数据结构、持久化、复制、哨兵、Cluster、
缓存一致性、缓存雪崩/穿透/击穿，以及 Spring Boot 整合。
```

```text
使用 $developer-learning-master，生成 Spring Framework 6.x 源码学习文档，
重点讲 IoC 容器启动、Bean 生命周期、AOP 代理和事务实现。
源码分析必须标注对应版本的类、方法和调用链。
```

## 通用生成要求

以上示例中的高标准要求已经固化在 `SKILL.md`，对所有技术主题默认生效，而非仅适用于 MySQL。包括：

- 从基础到高级工程实践及架构设计；
- 深入讲解底层原理和关键机制；
- 对适合的主题进行带版本依据的源码分析；
- 使用 Mermaid 绘制架构图、时序图和执行流程图；
- 提供匹配技术栈的可运行案例（Java、SQL、配置、命令等）；
- 覆盖生产实践、性能优化、安全和故障排查；
- 提供分层面试题及详细答案；
- 按章节拆分 Markdown 文件；
- 优先引用官方文档、官方源码和标准规范；
- 先生成完整目录和学习路线，再分批生成正文。

## 推荐工作方式

1. 先要求 AI 输出目录、版本假设和资料来源。
2. 审核目录后，按 2–4 章一批生成，避免长上下文导致内容缩水。
3. 每批完成后运行质量检查，并让 AI 修订。
4. 最后生成综合实战、面试题、索引和变更记录。

## 重要说明

- Skill 是工作规范和流程，不会自动保证联网、源码访问或代码执行能力。
- 最新版本和官方资料需要当前 AI 环境具备相应检索能力。
- 未实际运行的示例必须标注为待验证。
- 不建议将生产密码、真实业务数据或内部敏感配置放入学习文档。
