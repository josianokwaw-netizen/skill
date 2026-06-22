# CLAUDE.md — Skill 仓库行为规范

本仓库存放 Claude Code skill 文件，供 Claude Code on the Web 使用。

## 仓库结构

```
skills/
  <skill-name>/
    SKILL.md        # skill 定义文件
```

## 命名规范

- skill 目录名使用 **kebab-case**（小写字母 + 连字符），例如 `my-skill`、`code-review`
- 每个 skill 有且只有一个入口文件 `SKILL.md`

## 关联仓库

本 skill 仓库关联目标仓库：[josianokwaw-netizen/111](https://github.com/josianokwaw-netizen/111)

Claude Code 在目标仓库中执行 skill 时，会从本仓库加载对应的 `skills/<name>/SKILL.md`。

## 开发规范

- 新增 skill 前，先在 `skills/` 下创建以 kebab-case 命名的目录
- `SKILL.md` 须包含 skill 的触发条件、执行步骤和预期输出
- 提交信息使用英文，格式：`<type>(<scope>): <summary>`
- 不得在 skill 文件中硬编码敏感信息（密钥、token 等）
