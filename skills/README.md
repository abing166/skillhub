# Skills 目录

这里用于存放具体的场景技能。

## 目录命名

使用英文小写 + 短横线：

```text
<domain>-<scenario>-<ability>
```

示例：

```text
xhs-cover-copy
xhs-comment-seeding
github-skill-docs
obsidian-knowledge-structure
```

## 单个技能目录结构

```text
skills/<skill-id>/
├── skill.md
├── install.md
├── prompts/
│   └── main.md
├── examples/
│   ├── input.md
│   └── output.md
└── assets/
```

## 新增技能步骤

```bash
mkdir -p skills/<skill-id>/prompts skills/<skill-id>/examples skills/<skill-id>/assets
cp templates/skill-template.md skills/<skill-id>/skill.md
```

然后补充：

- `skill.md`：技能说明
- `install.md`：安装方法
- `prompts/main.md`：核心指令
- `examples/input.md`：输入示例
- `examples/output.md`：输出示例

## 提交前检查

- 是否有明确适用场景
- 是否有输入字段
- 是否有执行流程
- 是否有输出格式
- 是否有安装方法
- 是否已脱敏
