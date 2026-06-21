# 安装与接入说明

本文档说明如何把 SkillHub 中的技能安装到本地环境、Hermes 或 Obsidian。

## 1. 克隆仓库

```bash
git clone https://github.com/abing166/skillhub.git
cd skillhub
```

更新到最新版：

```bash
git pull
```

## 2. 安装单个技能到 Hermes

假设要安装的技能 ID 是：

```text
<skill-id>
```

默认安装命令：

```bash
mkdir -p ~/.hermes/skills
cp -r skills/<skill-id> ~/.hermes/skills/
```

安装后目录示例：

```text
~/.hermes/skills/<skill-id>/skill.md
```

如果 Hermes 的技能目录不是 `~/.hermes/skills`，请改成你的真实路径。

## 3. 安装到 Obsidian

进入你的 Obsidian Vault：

```bash
cd /你的/Obsidian/Vault/路径
```

克隆 SkillHub：

```bash
git clone https://github.com/abing166/skillhub.git SkillHub
```

然后在 Obsidian 中使用：

```text
SkillHub/skills
```

## 4. 手动复制安装

也可以直接复制某个技能目录：

```text
skills/<skill-id>/
```

复制到你的 AI 工具、知识库或项目文档目录即可。

## 5. 技能更新

如果是 Git 克隆安装：

```bash
cd skillhub
git pull
```

如果是手动复制安装，需要重新复制对应技能目录。

## 6. 敏感信息规则

禁止提交以下内容：

- 账号密码
- API Key
- Token
- Cookie
- 客户隐私
- 患者信息
- 内部未脱敏经营数据

需要配置密钥时，统一使用本地 `.env` 或 GitHub Secrets。
