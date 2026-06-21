# SkillHub

SkillHub 是用于沉淀自研「场景技能」的仓库。后续我们一起研发出的可复用技能，都按统一结构放到这里，方便给本地 Hermes、Obsidian、Codex 或其他 AI 工作流复用。

> 当前仓库是公开仓库。不要提交账号、密码、Token、客户隐私、患者信息、内部经营数据等敏感内容。

## 仓库定位

这个仓库主要沉淀四类内容：

1. 场景技能：针对具体业务场景的标准操作能力
2. Prompt 模板：可复用的指令、角色设定、输出格式
3. 安装说明：如何把技能接入本地 Hermes / Obsidian / 其他 AI 工具
4. 示例样本：脱敏后的输入、输出、案例

## 推荐目录结构

```text
skillhub/
├── README.md
├── docs/
│   └── INSTALL.md
├── skills/
│   ├── README.md
│   └── <skill-id>/
│       ├── skill.md
│       ├── install.md
│       ├── prompts/
│       │   └── main.md
│       ├── examples/
│       │   ├── input.md
│       │   └── output.md
│       └── assets/
└── templates/
    └── skill-template.md
```

## 技能命名规范

建议使用英文小写 + 短横线：

```text
领域-场景-能力
```

示例：

```text
xhs-cover-copy
xhs-comment-seeding
github-skill-docs
medical-content-review
obsidian-knowledge-structure
```

## 单个技能标准结构

每个技能建议至少包含：

```text
skills/<skill-id>/
├── skill.md        # 技能主说明
├── install.md      # 安装/接入方法
├── prompts/        # Prompt 或系统指令
├── examples/       # 脱敏示例
└── assets/         # 可选素材
```

## 安装方法

### 方法一：克隆整个技能库

```bash
git clone https://github.com/abing166/skillhub.git
cd skillhub
```

后续更新：

```bash
git pull
```

### 方法二：安装到本地 Hermes 技能目录

如果 Hermes 使用本地 skills 目录，可以把某个技能目录复制进去：

```bash
mkdir -p ~/.hermes/skills
cp -r skills/<skill-id> ~/.hermes/skills/
```

如果你的 Hermes 技能路径不是 `~/.hermes/skills`，把上面的路径替换成你本地真实路径即可。

### 方法三：接入 Obsidian 知识库

可以把本仓库克隆到 Obsidian Vault 内：

```bash
cd /你的/Obsidian/Vault/路径
git clone https://github.com/abing166/skillhub.git SkillHub
```

然后在 Obsidian 中直接检索和维护 `SkillHub/skills`。

## 新增技能流程

1. 从 `templates/skill-template.md` 复制一份
2. 在 `skills/` 下创建技能目录
3. 完成 `skill.md`、`install.md`、`prompts/`、`examples/`
4. 确认没有敏感信息
5. 提交到 GitHub

示例：

```bash
mkdir -p skills/xhs-cover-copy/prompts skills/xhs-cover-copy/examples skills/xhs-cover-copy/assets
cp templates/skill-template.md skills/xhs-cover-copy/skill.md
```

## 后续约定

后续我们研发新的场景技能时，统一提交到这个仓库：

```text
https://github.com/abing166/skillhub.git
```

每个技能都必须说明：

- 适用场景
- 输入要求
- 执行流程
- 输出格式
- 安装方法
- 使用示例
- 注意事项
