# 国内电商图生成器

面向淘宝、天猫、京东和拼多多的 Codex Skill。根据商品照片、真实卖点、品牌定位和平台角色，规划并生成主图、白底图、轮播图、SKU 图和详情页模块。

它不是把 Amazon 文案翻译成中文，也不是套用一套固定模板。Skill 会结合国内消费者的决策习惯、类目视觉语言、品牌主题和当前商品证据重新组织画面。

## 核心能力

- 区分搜索主图、白底图、轮播卖点图、SKU 图、详情页和活动图。
- 支持淘宝、天猫、京东、拼多多的平台适配。
- 从商品照片中提取可见结构，避免生成不存在的配件、功能和参数。
- 根据品牌主题指定颜色、字体、人物、场景、信息密度和视觉冲击档位。
- 支持多个创意方向，而不是只更换背景或标题。
- 根据类目专用规则处理消费者顾虑、摄影方式和成交信息。
- 对价格、承重、排名、专利、认证和促销等高风险信息进行证据检查。

## 当前类目

目前已经沉淀健身力量器材规则，覆盖：

- 成人室内单杠、引体向上器和力量塔
- 儿童室内单杠
- 固定双杠和分体双杠
- 哑铃凳
- 引体、双杠支撑和核心训练等动作展示

健身类目支持高密度力量电商、产品结构、训练动作、家庭场景、尺寸、安装、SKU 和细节证明等展示形式。

## 安装

克隆到 Codex Skills 目录：

```bash
git clone https://github.com/smilexiaobao1992/ecommerce-image-generator.git \
  ~/.codex/skills/china-ecommerce-image-generator
```

重新启动或刷新 Codex 的 Skill 列表后即可使用。

## 使用方法

在任务中调用：

```text
使用 $china-ecommerce-image-generator，基于这组产品照片为淘宝生成 4 个主图方向。
产品是室内引体向上双杠，品牌主色为绿色，定位高端，重点解决稳定性和占地顾虑。
```

也可以只重做某一个图片角色：

```text
使用 $china-ecommerce-image-generator 重做 MAIN-01。
保留商品结构和品牌绿色，采用高密度力量电商风格，不使用固定底栏。
信息密度使用 D2，视觉冲击使用 I3-HIGH-IMPACT。
```

### 指定视觉冲击强度

视觉冲击和信息密度可以分别指定：

| 参数 | 效果 |
|---|---|
| `I1-RESTRAINED` | 克制旗舰：安静网格、少穿插、适合白底/SKU/文件证明 |
| `I2-ASSERTIVE` | 平衡转化：标题醒目、对比明确，默认档 |
| `I3-HIGH-IMPACT` | 高冲击电商：大字、强对比、品牌色切面、产品与文字穿插、高空间利用率 |

例如：

```text
使用 $china-ecommerce-image-generator 生成淘宝健身器材轮播图。
主题使用 BRAND-LIME，信息密度使用 D2，视觉冲击使用 I3-HIGH-IMPACT。
标题允许两行大字和绿/藏青切面，但商品与动作必须保持第一视觉主体。
```

`I3` 不代表堆满徽章或促销元素。它强化的是字号、对比、色块面积、
穿插关系和画面占用率，商品真实性、文案证据和动作正确性仍是硬门槛。

跨平台适配示例：

```text
使用 $china-ecommerce-image-generator，把当前天猫轮播图分别改成京东和拼多多版本。
商品事实保持一致，但重新设计信息层级、文字密度和构图。
```

## 推荐输入

输入越完整，生成结果越可靠。建议提供：

- 清晰的产品正面、侧面、结构和使用照片
- 准确的 SKU、颜色、数量和包装内容
- 已确认的尺寸、材质、承重、专利或认证资料
- 目标平台和图片角色
- 品牌 Logo、主题色、字体或官网链接
- 目标消费者及其核心顾虑
- 希望展示的训练动作、使用场景或竞品截图
- 明确禁止出现的内容

无法验证的数据不会自动编造。涉及最终上架时，平台规格和规则仍应以当前商家后台为准。

## 图片角色

| 角色 | 用途 |
|---|---|
| `MAIN-01` | 搜索曝光第一张主图 |
| `WHITE-01` | 合规白底商品图 |
| `CAR-02...07` | 核心卖点、结构、尺寸、场景、细节和使用说明 |
| `SKU-01` | 单个真实 SKU 或属性图 |
| `DET-01...08` | 详情页模块 |
| `CAM-01` | 活动、广告或品牌传播图，不等同于普通主图 |

## 目录结构

```text
china-ecommerce-image-generator/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── china-ecommerce-image-strategy.md
    ├── platform-rules-and-compliance.md
    └── categories/
        └── fitness-strength-visual-system.md
```

- `SKILL.md`：工作流、图片角色和类目路由。
- `china-ecommerce-image-strategy.md`：国内电商通用策略。
- `platform-rules-and-compliance.md`：平台规则与合规检查。
- `categories/`：按需加载的类目专用视觉与成交规则。

## 扩展新类目

新增类目时，在 `references/categories/` 创建独立 Markdown 文件，例如：

```text
references/categories/home-appliances.md
references/categories/furniture.md
references/categories/beauty-skincare.md
```

类目文件建议包含：

1. 消费者购买动机和核心顾虑。
2. 搜索主图与轮播图的类目视觉语言。
3. 商品、人物、场景和文字的推荐比例。
4. 适用的摄影、字体、颜色和信息密度。
5. 主图、轮播图和详情页的推荐顺序。
6. 必须验证的数据及禁止表达。
7. 不同产品子类的展示路线。

然后在 `SKILL.md` 的“Load the right references”部分增加对应的触发词和加载路径。通用规则留在核心文件中，类目差异只放在对应参考文件，避免不同类目的设计语言相互污染。

## 设计与合规原则

- 高端不等于空白，国内电商图需要充分利用有效画面。
- 商品必须是第一视觉主体，人物和场景服务于理解与成交。
- 创意方向需要改变消费者心理钩子、摄影、构图和证明方式。
- 竞品用于研究类目点击逻辑，不直接复制其颜色、文案或版式。
- 不生成未经证实的承重、销量、排名、认证、专利和促销信息。
- AI 生成图必须检查商品结构、文字准确性、动作合理性和平台合规性后再上架。

## 验证

修改 Skill 后运行：

```bash
python3 "${CODEX_HOME:-$HOME/.codex}/skills/.system/skill-creator/scripts/quick_validate.py" .
```
