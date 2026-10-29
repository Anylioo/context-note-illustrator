# 生成提示词模板（只用于 status=READY 的独立主题或合并主题）

使用前，按 `SKILL.md` 的“解析请求”规则确定参数：用户明确设置优先，未指定的参数采用该表默认值。将 Visual Brief 中的实际值填入以下占位符后再调用图像工具；比例和方向保持一致。

生成一张 **{ASPECT_RATIO}、{LANGUAGE}、{ORIENTATION}、粉彩手绘风的学术笔记插画**。主题：`{TOPIC}`。装饰要求：`{DECORATION_RULES}`。

## 强制知识边界

严格上下文模式。图中只能表达以下**已锁定内容**，不得自己新增事实、模型参数、公式、引文、图表数值、实验趋势；如有教学示例，要标注“示意 / 非实测”。

```text
标题：{TITLE}
主旨：{CORE_MESSAGE}
模块与短文案：{SECTIONS}
公式及变量解释：{VERIFIED_FORMULAS_AND_VARIABLES}
必须画出的关系图：{DIAGRAMS_AND_ARROWS}
必要标签与页码：{PROVENANCE}
底部总结：{TAKEAWAY}
```

## 固定视觉目标

将以下 3 张文件作为图片风格参考（在工具允许时实际输入）：

- `assets/style-ref-routing-experts.webp`
- `assets/style-ref-attention-evolution.webp`
- `assets/style-ref-expert-parallelism.webp`

保持深蓝手写大标题、暖黄色标题条、浅蓝细圆角边框、粉蓝绿橙紫卡片、清楚的编号小节、合理分布的示意图和底部结论条。根据 `{DECORATION_RULES}` 安排装饰；排版适配 `{ASPECT_RATIO}` 和 `{ORIENTATION}`，文字使用 `{LANGUAGE}`。**不复用三张参考图的知识内容。**

以技术准确性和所选语言的文字可读性优先。字号不能小到无法阅读。如果内容太多，省略可选文字，而非篡改公式或压缩至模糊。不要绘制未经来源支持的柱状图、曲线、参数量、年份或性能结论。
