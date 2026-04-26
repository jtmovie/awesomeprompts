# Prompt 投稿模板

新建 Issue 时，复制下面模板，把内容替换成你的 prompt 信息。提交后给 Issue 添加 `prompt-submission` 标签。

```text
Title: 这里写 prompt 标题
Model: gpt-image
Category: use-case
Subcategory: infographic-edu-visual
Language: zh
Author: 作者名或账号
Author URL: https://example.com/author
Images: https://github.com/user-attachments/assets/图片ID
Description: 一句话描述这个 prompt 的用途
---
这里写真正的 prompt 正文。

可以是中文、英文、日文，也可以是 JSON。

来源：https://example.com/source
```

## 字段说明

- `Title`: 必填，prompt 标题。
- `Model`: 可选，默认 `gpt-image`。目前支持 `gpt-image`、`seedance`、`flux`。
- `Category`: 可选，默认 `use-case`。目前支持 `use-case`、`style`、`subject`。
- `Subcategory`: 可选，默认 `profile-avatar`。建议按用途填写，例如 `infographic-edu-visual`、`product-marketing`、`social-media-post`。
- `Language`: 可选，默认 `en`。目前支持 `en`、`zh`、`ja`、`de`、`ko`、`fr`、`es`、`multi`。
- `Author`: 可选，原作者或投稿人。
- `Author URL`: 可选，作者主页或来源链接。
- `Images`: 可选，示例图链接。多张图用英文逗号分隔。
- `Description`: 可选，一句话简介。
- `---`: 必须保留。上面是元数据，下面是真正的 prompt 正文。

## 图片链接怎么填

如果图片上传到了 GitHub Issue，编辑框里会生成类似：

```html
<img width="941" height="1672" alt="Image" src="https://github.com/user-attachments/assets/ec9dd419-30a7-4765-8fe2-ed26fae7cd3b" />
```

只复制 `src="..."` 里面的链接：

```text
Images: https://github.com/user-attachments/assets/ec9dd419-30a7-4765-8fe2-ed26fae7cd3b
```

多张图片：

```text
Images: https://github.com/user-attachments/assets/aaa, https://github.com/user-attachments/assets/bbb
```

## 示例 1：信息图 prompt

```text
Title: 信息图可视化设计
Model: gpt-image
Category: use-case
Subcategory: infographic-edu-visual
Language: zh
Author: insight_express
Author URL: https://www.xiaohongshu.com/
Images: https://github.com/user-attachments/assets/ec9dd419-30a7-4765-8fe2-ed26fae7cd3b
Description: 城市生命系统图谱信息图 prompt
---
Vertical 9:16 isometric cutaway infographic "城市生命系统图谱 / Urban Metabolism Atlas". Smart city from sky to bedrock: skyscrapers, streets, subway, utility tunnels, water/sewage/gas/heating pipes, fiber, data center, flood tanks, aquifers, geothermal wells, bedrock. Color-coded flows for power/water/data/traffic/waste. 12 numbered panels bilingual CN/EN: 能源/水循环/交通/数据/垃圾/建筑/公共服务/物流/气候韧性/生态/地质/治理看板. 24h timeline at bottom. Style: engineering white paper + scientific atlas, light paper bg, crisp lines, 8K. No cyberpunk, no gibberish text, must show both above AND below ground.

来源：小红书号 insight_express
```

## 示例 2：JSON prompt

```text
Title: 界面交互设计图
Model: gpt-image
Category: use-case
Subcategory: product-marketing
Language: ja
Author: wory37303852
Author URL: https://x.com/wory37303852
Images: https://github.com/user-attachments/assets/c2c77955-ce6b-44be-b10c-2983e8c4a709
Description: VR headset exploded view product diagram poster.
---
{
  "type": "exploded view product diagram poster",
  "subject": "VR headset",
  "style": "clean high-tech 3D render, studio lighting, glowing accents",
  "background": "{argument name=\"background color\" default=\"soft purple and blue gradient\"}",
  "header": {
    "logo": "∞ {argument name=\"product name\" default=\"Meta Quest 3\"}",
    "subtitle": "{argument name=\"main catchphrase\" default=\"まったく新しい現実を、まったく新しい構造から。\"}"
  }
}

来源：https://x.com/wory37303852
```
