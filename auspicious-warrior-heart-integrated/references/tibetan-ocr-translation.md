# 藏文OCR与翻译参考手册

## 目录
- [OCR识别规范](#ocr识别规范)
- [翻译处理流程](#翻译处理流程)
- [术语校核标准](#术语校核标准)
- [权威词典资源](#权威词典资源)
- [字体与编码支持](#字体与编码支持)
- [转写工具](#转写工具)
- [专业翻译团队参考](#专业翻译团队参考)

---

## OCR识别规范

### 支持字体类型
1. **乌金体（印刷体）**：识别准确率高，为主要支持类型
2. **乌梅体（手写体）**：识别准确率中等，需人工校核
3. **竹笔体**：古籍常见，识别难度较大
4. **德格版字体**：大藏经标准字体

### 识别输出规范
- 输出 Unicode 标准藏文字符
- 保留原始段落结构与换行
- 低置信度字符标记 `[?]`
- 识别置信度低于70%的段落标注「待人工校核」

### 常见识别错误修正
- 相似字母混淆：ཀ/ཏ、ག/ད、པ/བ 等
- 上下加字识别偏差
- 标点符号与特殊符号误识

---

## 翻译处理流程

### 双向翻译支持
- **藏译汉**：优先保证佛学术语准确性
- **汉译藏**：采用书面语标准表达

### 标准输出格式
```
【原始藏文】
བདེ་གཤེགས་ཆོས་ཀྱི་སྐུ་

【威利转写】
bde gshegs chos kyi sku

【汉文译文】
法身佛（佛陀的法身）
```

### 翻译原则
1. **术语一致性**：同一术语在全文中保持译法统一
2. **宗派区分**：格鲁、萨迦、宁玛、噶举等宗派术语采用各自传统译法
3. **语境适配**：根据显宗/密宗、经/论/律不同语境调整译法
4. **出处标注**：重要术语标注大藏经出处

---

## 术语校核标准

### 核心佛学术语标准译法

| 藏文 | 威利转写 | 标准汉译 | 异译 |
|------|----------|----------|------|
| བྱང་ཆུབ་སེམས་དཔའ་ | byang chub sems dpa' | 菩萨 | 菩提萨埵 |
| སངས་རྒྱས་ | sangs rgyas | 佛 | 佛陀、薄伽梵 |
| ཆོས་ | chos | 法 | 达摩 |
| དཀོན་མཆོག་གསུམ་ | dkon mchog gsum | 三宝 | 三皈依 |
| བྱང་ཆུབ་ཀྱི་སེམས་ | byang chub kyi sems | 菩提心 | 觉心 |
| སྐུ་གསུམ་ | sku gsum | 三身 | 法报化三身 |
| དབང་བསྐུར་ | dbang bskur | 灌顶 | 阿阇梨灌顶 |
| བསྒོམ་པ་ | bsgom pa | 禅修 | 观修、修习 |

### 宗派术语差异
- **格鲁派**：偏重因明与戒律术语
- **宁玛派**：大圆满相关专有术语
- **萨迦派**：道果法相关术语
- **噶举派**：大手印、那洛六法相关术语

---

## 权威词典资源

### 在线词典
1. **蒙兰在线藏语词典**（最全面）
   - 网址：https://www.monlamdic.com/
   - 特点：藏藏、藏汉、藏英多模式，词汇量最大

2. **Steinert 在线藏语词典**
   - 网址：shturl.cc/8Tj0oO6CvQj3nKRwMEQoLsG38UlsyDALh1y
   - 特点：聚合多部词典资源

3. **THL 藏英翻译工具**
   - 网址：shturl.cc/GNZI8jbpNUGEcMvTtJP2eXXnrYuSvrww1RLJfV5Y2VoXN9qaEw7w9ApKuoDcKpxpJa
   - 特点：藏英双向，学术标准

4. **THL 藏语历史词典**
   - 网址：shturl.cc/eZPNXBxC4WzEWuESza
   - 特点：历史词汇与古藏文

5. **佛法词典（Rigpa Wiki）**
   - 网址：http://rywiki.tsadra.org/index.php/Main_Page
   - 特点：藏英佛学术语详解

6. **佛教研究术语表**
   - 网址：http://buddhistinformatics.ddbc.edu.tw/glossaries/glossaries.php
   - 特点：多语种对照，梵藏汉英

### 离线词典方案
- **GoldenDict 整合方案**：http://digitaltibetan.org/index.php/GoldenDict_-_online_and_offline_Tibetan_dictionaries_combined
- 支持多部词典同时检索

---

## 字体与编码支持

### 标准 Unicode 字体
1. **珠穆朗玛藏文 Unicode 字体**
   - 网址：http://www.yalasoo.com/English/docs/yalasoo_en_qomolangma_fonts.html
   - 特点：开源免费，支持完整藏文字符集

2. **尼塔尔塔国际藏文桑布扎字体**
   - 网址：http://www.nitartha.net/sambhota4.html
   - 特点：学术出版标准字体

3. **数字藏文资源库字体集合**
   - 网址：http://digitaltibetan.org/index.php/Digital_Tibetan

4. **THL 字体资源**
   - 网址：shturl.cc/JWSmbBJ4

### 编码标准
- 统一使用 Unicode 标准（UTF-8）
- 避免使用非标准私用区字符
- 传统编码（如 Sambhota）需转换为 Unicode

---

## 转写工具

### 威利转写（Wylie Transliteration）
- **THL 威利转写 ↔ Unicode 转换器**
  - 网址：shturl.cc/i3ru43qwrmt1lyJHO3BkkU0FgqNDbXoRa2y7Jel7kkEKQxbFn785
  - 功能：藏文 Unicode 与威利转写双向转换

### 音标转换
- **THL 藏文 ↔ 音标转换工具**
  - 网址：shturl.cc/UntrSvUJ8WFnWhoYYqj3QPyczs1PK5F8PB0nIDpVajklpwDjdKRn
  - 功能：藏文转国际音标

---

## 专业翻译团队参考

### 国际翻译组织
1. **帕德玛卡拉翻译小组**（Padmakara Translation Group）
   - 网址：http://www.songtsen.org/F/padmakara/apropos_comite.php
   - 特点：宁玛派传统，译著丰富

2. **Dharmachakra 翻译委员会**
   - 网址：http://www.dharmachakra.net/
   - 特点：噶举派传统

3. **那烂陀翻译委员会**（Nalanda Translation Committee）
   - 网址：http://nalandatranslation.org/
   - 特点：噶举派，创古仁波切指导

4. **贝罗察纳翻译团**（Berotsana Translation Group）
   - 网址：http://www.berotsana.org/

5. **瑞巴翻译公司**（Rigpa Translations）
   - 网址：https://www.rigpatranslations.org/

### 学术翻译资源
- **伯金档案与译文库**（Berzin Archives）
  - 网址：http://www.berzinarchives.com/
  - 特点：亚历山大·伯金博士，藏传佛教百科式翻译
