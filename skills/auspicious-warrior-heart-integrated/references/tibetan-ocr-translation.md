# 藏文OCR与翻译参考手册

## 目录
- [OCR识别工具](#ocr识别工具)
- [翻译处理流程](#翻译处理流程)
- [术语校核标准](#术语校核标准)
- [权威词典资源](#权威词典资源)
- [字体与编码支持](#字体与编码支持)
- [转写工具](#转写工具)
- [专业翻译团队参考](#专业翻译团队参考)

---

## OCR识别工具

### 在线OCR工具

1. **Dharmamitra 藏文OCR**
   - 网址：https://dharmamitra.org/zh/ocr
   - 特点：
     - 专门针对藏文优化
     - 支持乌金体、乌梅体
     - 识别准确率高
     - 中文界面

2. **百度 PaddleOCR**
   - 网址：https://aistudio.baidu.com/paddleocr
   - 特点：
     - 开源OCR引擎
     - 支持多语言
     - 可本地部署
     - 藏文识别需训练模型

### 识别规范

#### 支持的字体类型
1. **乌金体（印刷体）**
   - 现代印刷书籍常用
   - 识别准确率最高
   - 包括德格版、拉萨体等

2. **乌梅体（手写体）**
   - 传统手写文献
   - 识别难度较高
   - 需人工校核

3. **藏文篆刻体**
   - 印章、铭文
   - 识别难度最高

#### 识别输出标准
- 输出 Unicode 编码藏文文本
- 保留原始段落结构
- 低置信度字符标记 `[?]`
- 标注识别置信度

---

## 翻译处理流程

### 批量文档翻译标准流程

#### 前置处理阶段
1. **文档抽样检查**
   - 抽取文档前10页
   - 识别文档类型（佛经、论典、历史文献等）
   - 评估翻译难度

2. **版权信息清洗**
   - 移除现代版权声明
   - 移除出版社广告页
   - 保留原始文献内容

#### 分批翻译阶段
1. **文档切割**
   - 大文档按章节或页数切割
   - 每批次控制在合理 Token 范围内
   - 保留上下文衔接标记

2. **进度反馈**
   - 每翻译完一个批次显示进度
   - 格式：`已完成 X/Y 批次（Z%）`
   - 中途不停止，直至翻译完整

3. **质量控制**
   - 关键术语一致性检查
   - 专有名词统一译法
   - 段落结构完整性验证

#### 专业模式（佛经翻译）
- **系统提示词**：你为专业的藏传佛教翻译专家，将文档完整翻译成中文，如果有藏文拼写错误，请适当进行修正。
- 采用佛学专业译法
- 保留经文体例（偈颂、散文等）
- 重要术语附梵文/藏文原文

#### 备用方案
- **触发条件**：Token 不足或翻译服务不可用
- **备用工具**：Dharmamitra 在线翻译
  - 网址：https://dharmamitra.org/zh/translate
- **处理方式**：剩余文档用在线工具翻译
- **最终交付**：合并所有批次，统一格式后交付

---

## 术语校核标准

### 核心佛学术语标准译法

| 藏文 | 威利转写 | 标准汉译 | 备注 |
|------|----------|----------|------|
| སངས་རྒྱས་ | sangs rgyas | 佛，佛陀 | 觉者 |
| ཆོས་ | chos | 法 | 教法、事物 |
| དགེ་འདུན་ | dge 'dun | 僧团 | 僧伽 |
| བྱང་ཆུབ་སེམས་དཔའ་ | byang chub sems dpa' | 菩萨 | 菩提萨埵 |
| ཤེས་རབ་ | shes rab | 般若 | 智慧 |
| སྙིང་རྗེ་ | snying rje | 慈悲 | 大悲 |
| ཚུལ་ཁྲིམས་ | tshul khrims | 戒律 | 尸罗 |
| ཏིང་ངེ་འཛིན་ | ting nge 'dzin | 三昧 | 禅定 |

### 宗派术语差异
- **格鲁派**：侧重因明、中观应成派术语
- **萨迦派**：侧重道果法相关术语
- **宁玛派**：侧重大圆满、伏藏相关术语
- **噶举派**：侧重大手印、那洛六法相关术语

### 校核流程
1. 关键术语匹配标准词典
2. 交叉验证多部词典译法
3. 标注异译与出处
4. 保留原文脚注

---

## 权威词典资源

### 在线词典

1. **Steinert 在线藏语词典**
   - 网址：shturl.cc/8Tj0oO6CvQj3nKRwMEQoLsG38UlsyDALh1y
   - 特点：聚合多部词典资源，检索方便

2. **蒙兰在线藏语词典（Monlam Dictionary）**
   - 网址：https://www.monlamdic.com/
   - 特点：
     - 最全面的藏语词典
     - 藏藏、藏汉、藏英多模式
     - 词汇量最大
     - 有手机 App

3. **GoldenDict 在线+离线藏语词典整合方案**
   - 网址：http://digitaltibetan.org/index.php/GoldenDict_-_online_and_offline_Tibetan_dictionaries_combined
   - 特点：
     - 支持多部词典同时检索
     - 在线离线两用
     - 可自定义词典库

4. **THL 藏英翻译工具**
   - 网址：shturl.cc/GNZI8jbpNUGEcMvTtJP2eXXnrYuSvrww1RLJfV5Y2VoXN9qaEw7w9ApKuoDcKpxpJa
   - 特点：藏英双向，学术标准

5. **THL 藏语历史词典**
   - 网址：shturl.cc/eZPNXBxC4WzEWuESza
   - 特点：历史词汇与古藏文研究

6. **佛法词典（Rigpa Wiki / Dharma Dictionary）**
   - 网址：http://rywiki.tsadra.org/index.php/Main_Page
   - 特点：
     - 藏英佛学术语详解
     - 按主题分类
     - 含修行相关词汇

7. **佛教研究术语表（Buddhist Glossaries）**
   - 网址：http://buddhistinformatics.ddbc.edu.tw/glossaries/glossaries.php
   - 特点：
     - 多语种对照（梵、藏、汉、英）
     - 法鼓文理学院开发
     - 学术研究用

---

## 字体与编码支持

### 藏文字体

1. **数字藏文资源库（Digital Tibetan）**
   - 网址：http://digitaltibetan.org/index.php/Digital_Tibetan
   - 内容：藏文字体、编码、输入方法综合资源
   - 特点：资源全面，适合初学者

2. **西藏与喜马拉雅地区图书馆（THL）字体资源**
   - 网址：shturl.cc/JWSmbBJ4
   - 内容：THL 项目藏文字体集合
   - 特点：学术标准，支持多种字体

3. **珠穆朗玛藏文 Unicode 字体**
   - 网址：http://www.yalasoo.com/English/docs/yalasoo_en_qomolangma_fonts.html
   - 内容：开源免费 Unicode 藏文字体
   - 特点：支持完整藏文字符集，跨平台

4. **尼塔尔塔国际藏文桑布扎字体**
   - 网址：http://www.nitartha.net/sambhota4.html
   - 内容：Sambhota 字体系统
   - 特点：藏传佛教界广泛使用，传统排版

### 编码标准
- Unicode 标准（UTF-8）：推荐使用
- 传统编码（Sambhota、Tibetan Machine Uni等）：需转换

---

## 转写工具

### 威利转写工具

1. **THL 威利转写 ↔ Unicode 转换器**
   - 网址：shturl.cc/i3ru43qwrmt1lyJHO3BkkU0FgqNDbXoRa2y7Jel7kkEKQxbFn785
   - 功能：藏文 Unicode 与威利转写双向转换
   - 特点：学术标准，准确率高

### 音标转换工具

1. **THL 藏文 ↔ 音标转换工具**
   - 网址：shturl.cc/UntrSvUJ8WFnWhoYYqj3QPyczs1PK5F8PB0nIDpVajklpwDjdKRn
   - 功能：藏文转国际音标（IPA）
   - 特点：支持卫藏、康巴、安多等方言

---

## 专业翻译团队参考

### 国际翻译组织

1. **帕德玛卡拉翻译小组（Padmakara Translation Group）**
   - 网址：http://www.songtsen.org/F/padmakara/apropos_comite.php
   - 特点：
     - 宁玛派传统
     - 译著丰富，质量高
     - 法译本为主，也有英译本

2. **Dharmachakra 翻译委员会**
   - 网址：http://www.dharmachakra.net/
   - 特点：
     - 噶举派传统
     - 英文翻译

3. **那烂陀翻译委员会（Nalanda Translation Committee）**
   - 网址：http://nalandatranslation.org/
   - 特点：
     - 噶举派
     - 创古仁波切指导
     - 英文翻译

4. **贝罗察纳翻译团（Berotsana Translation Group）**
   - 网址：http://www.berotsana.org/
   - 特点：藏文翻译团体

5. **瑞巴翻译公司（Rigpa Translations）**
   - 网址：https://www.rigpatranslations.org/
   - 特点：专业藏文翻译服务

### 学术翻译资源

1. **伯金档案与译文库（Berzin Archives）**
   - 网址：http://www.berzinarchives.com/
   - 特点：
     - 亚历山大·伯金博士
     - 藏传佛教百科式翻译
     - 内容极其丰富
     - 多语种（英、德、俄、西等）

### 在线翻译工具

1. **Dharmamitra 在线翻译**
   - 网址：https://dharmamitra.org/zh/translate
   - 特点：
     - 藏汉在线翻译
     - 佛学术语优化
     - 备用翻译方案
