---
name: notion-upload
description: 上传指定文件到 Notion 指定页面。使用方式：/notion-upload <文件路径> [页面标题]。当用户想要将文件上传到 Notion 时使用。
user-invocable: true
tools: Bash
---

# Notion Upload

将本地文件上传到 Notion 指定页面。

## 使用方式

```
/notion-upload <文件路径> [页面标题]
```

- **文件路径**（必需）：要上传的文件的完整路径
- **页面标题**（可选）：Notion 页面标题，默认为文件名

## 执行步骤

1. 验证文件是否存在且可读
2. 执行 Python 脚本上传到 Notion：

```bash
python3 "/Users/nelson/code/claude-script/notion_write.py" --file "<文件路径>" --title "<页面标题>"
```

## 示例

- `/notion-upload /Users/nelson/code/project/readme.md`
- `/notion-upload ./notes.txt 我的笔记标题`
- `/notion-upload /Users/nelson/doc.pdf 文档标题`
