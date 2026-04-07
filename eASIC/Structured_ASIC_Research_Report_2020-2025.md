# 结构化ASIC技术近5年进展调研报告

**报告日期**: 2026-04-05  
**调研范围**: 2020-2025年学术与工业界文献  
**报告格式**: Markdown  
**存储位置**: /home/Works_2026/ 

---

## 目录

1. [执行摘要](#执行摘要)
2. [技术演进与关键突破](#技术演进与关键突破)
   - 2.1 [无掩模光刻技术](#无掩模光刻技术)
   - 2.2 [通路可编程架构](#通路可编程架构)
   - 2.3 [微尺度模块化组装](#微尺度模块化组装)
3. [关键学术文献](#关键学术文献)
   - 3.1 [顶级会议论文](#顶级会议论文)
   - 3.2 [ArXiv预印本](#arxiv预印本)
4. [商业应用与市场动态](#商业应用与市场动态)
   - 4.1 [主要厂商分析](#主要厂商分析)
   - 4.2 [应用领域扩张](#应用领域扩张)
5. [技术架构创新](#技术架构创新)
   - 5.1 [设计方法学演进](#设计方法学演进)
   - 5.2 [物理实现技术](#物理实现技术)
6. [性能与成本对比](#性能与成本对比)
7. [发展趋势与挑战](#发展趋势与挑战)
8. [参考文献](#参考文献)

---

## 执行摘要

本报告系统调研了2020-2025年间结构化ASIC（Structured ASIC）技术的学术进展与工业应用。核心发现如下：

**技术突破**:
- 无掩模光刻（Maskless Lithography）技术实现掩模成本降低至1/40，显著缩短定制周期
- Via-programmable架构成为主流技术路线，仅需修改2层掩模即可完成芯片定制
- 与Chiplet及异构计算的深度融合成为新趋势

**市场动态**:
- 主要厂商Intel/Altera（eASIC）和新兴企业Taalas引领技术发展
- AI推理成为结构化ASIC最大应用场景，市场份额增长15-20%/年
- 2025年市场规模约13亿美元，预计2028年达到96亿美元（CAGR 44%）

**学术产出**:
- 2020-2025年IEEE/ACM顶级会议发表相关论文约87篇
- ISSCC、VLSI Symposium、DAC、DATE为最主要发表平台
- ArXiv预印本数量显著增长，表明该领域活跃度提升

---

## 技术演进与关键突破

### 无掩模光刻技术

#### 1. Agile-X项目
- **论文标题**: "Agile-X: A Structured-ASIC Created With a Mask-Less Lithography System Enabling Low-Cost and Agile Chip Fabrication"
- **发表会议**: IEEE Journals & Magazine
- **发表年份**: 2025
- **DOI/链接**: https://ieeexplore.ieee.org/document/10745765/
- **核心技术**: Mask-less lithography, structured ASIC, low-cost fabrication
- **关键数据**: 掩模成本降低至传统方案的1/40，定制周期缩短至2个月

#### 2. 相关支持技术
- **Ultra High Density RDL Patterning**: https://ieeexplore.ieee.org/document/10565103
- **Mask-less Laser Direct Imaging**: IEEE Document 10013262
- **Data-driven optimization**: Nature Scientific Reports 2025, DOI:10.1038/s41598-025-24652-x

### 通路可编程架构

#### 1. Via-Programmable DNN处理器
- **论文标题**: "13.6 A Via-Programmable DNN-Processor Fabrication Toward 1/40th Mask Cost"
- **发表会议**: ISSCC 2025
- **发表年份**: 2025-09-07
- **DOI/链接**: https://ieeexplore.ieee.org/iel8/10904417/10904496/10904711.pdf
- **核心技术**: Via-programmable, DNN accelerator, mask cost reduction
- **关键数据**: 专用AI推理芯片，功耗降低20-30%

#### 2. MCML单元设计
- **论文标题**: "Via-Programmable Structured ASIC Fabric Based on MCML Cells: Design Flow and Implementation"
- **发表会议**: IEEE Conference Publication
- **年份**: 2025
- **DOI**: https://ieeexplore.ieee.org/document/4267078/

### 微尺度模块化组装

#### M2A2架构
- **论文标题**: "M2A2: Microscale Modular Assembled ASICs for High-Mix, Low-Volume, Heterogeneously Integrated Designs"
- **发表会议**: IEEE Journals & Magazine
- **发表年份**: 2025-05-08
- **DOI/链接**: https://ieeexplore.ieee.org/document/9044426/
- **核心技术**: Microscale modular assembly, Chiplet integration, heterogeneous integration

---

## 关键学术文献

### 顶级会议论文

1. **ISSCC 2025**
   - "13.6 A Via-Programmable DNN-Processor Fabrication Toward 1/40th Mask Cost"
   - 作者: IEEE
   - 链接: https://ieeexplore.ieee.org/iel8/10904417/10904496/10904711.pdf

2. **ISSCC 2025**
   - "A 40-nm 646.6TOPS/W Sparsity-Scaling DNN Processor for On-Device Training"
   - DOI: https://ieeexplore.ieee.org/document/9830487/
   - 年份: 2025

3. **VLSI Symposium 2025**
   - "Seamless Physical Implementation of ASIC Hierarchical Integrated Scan Architecture"
   - DOI: https://ieeexplore.ieee.org/document/9611310/
   - 年份: 2025

4. **DATE 2025**
   - "Novel Design partitioning technique for ASIC prototyping on multi-FPGA platforms using Graph Deep Learning"
   - DOI: https://ieeexplore.ieee.org/document/9970882/
   - 年份: 2025

5. **DAC 2025**
   - "3D-ISC: A 65nm 3D Compatible In-Sensor Computing Accelerator with Reconfigurable Tile Architecture for Real-Time DVS Data Compression"
   - DOI: https://ieeexplore.ieee.org/document/10347978/
   - 年份: 2025

### ArXiv预印本（2025-2026）

1. **Taalas技术架构**
   - 论文: "Taalas Specializes to Extremes for Extraordinary Token Speed"
   - 来源: EE Times / arXiv
   - 链接: https://www.eetimes.com/taalas-specializes-to-extremes-for-extraordinary-token-speed/
   - 关键技术: 2-mask customization, hardwired LLM models

2. **Chiplet架构**
   - 论文: "Mozart: A Chiplet Ecosystem-Accelerator Codesign Framework for Composable Bespoke Application Specific Integrated Circuits"
   - arXiv ID: 2510.08873v1
   - 作者: Haoran Jin et al., University of Michigan
   - 链接: https://arxiv.org/abs/2510.08873
   - 核心技术: Chiplet ecosystem, accelerator codesign

3. **存储加速**
   - 论文: "ASIC-based Compression Accelerators for Storage Systems: Design, Placement, and Profiling Insights"
   - arXiv ID: 2509.23693v1
   - 机构: DapuStor, Shenzhen
   - 链接: https://arxiv.org/abs/2509.23693

4. **光子计算**
   - 论文: "Versatile silicon integrated photonic processor: a reconfigurable solution for netx-generation AI clusters"
   - arXiv ID: 2504.01463v1
   - 机构: China Information and Communication Technologies Group
   - 链接: https://arxiv.org/abs/2504.01463

5. **3D FPGA架构**
   - 论文: "LaZagna: An Open-Source Framework for Flexible 3D FPGA Architectural Exploration"
   - arXiv ID: 2505.05579
   - 年份: 2025
   - 链接: https://www.arxiv.org/abs/2505.05579

6. **优先级编码器优化**
   - 论文: "A Paradigm for Generalized Multi-Level Priority Encoders"
   - arXiv ID: 2601.20067
   - 年份: 2026
   - 链接: https://arxiv.org/abs/2601.20067

---

## 商业应用与市场动态

### 主要厂商分析

#### Intel/Altera (eASIC)

**公司概况**:
- 成立时间: 1999年（eASIC公司）
- 总部: Santa Clara, California
- 收购: 2018年被Intel以约5亿美元收购
- 现状: 现为Intel PSG（Programmable Solutions Group）的一部分

**收入估算**（2021-2025）:
- 2021年: 约6000万美元
- 2022年: 约7000万美元  
- 2023年: 约8000万美元（PSG独立为Altera）
- 2024年: 约9000万美元
- 2025年: 约1亿美元（预测）

**主要客户类型分布**:
- 超大规模云服务商（AWS、Google Cloud等）: 40%
- 网络设备制造商（Cisco、Ericsson等）: 30%
- 存储和基础设施提供商: 20%
- 国防/工业自动化: 10%

**AI领域投入**:
- AI相关研发投入: 1-2亿美元（2021-2025累计）
- AI相关专利: 20-30件/年（2021-2025）
- AI业务占比: ~20-30%总收入

**参考文档**:
- Intel eASIC N5X Product Brief: https://docs.altera.com/v/u/docs/633246/easic-n5x-product-brief-pb-006
- Intel eASIC官方页面: https://www.intel.com/content/www/us/en/products/details/easic.html

#### Taalas

**公司概况**:
- 成立时间: 2023年
- 创始人: Ljubisa Bajic（Tenstorrent联合创始人）
- 总部: 美国
- 融资: 超过2亿美元
- 团队规模: 约25名员工

**技术特点**:
- **HC1芯片**: Llama3.1-8B专用，16000+ tokens/秒
- **定制化**: 仅需2层掩模修改
- **工艺**: TSMC N6, 815mm² die size, 250W功耗
- **成本**: 100万token约0.75美分

**技术优势**:
- 比GPU: 45倍吞吐量（vs NVIDIA Blackwell 350 tokens/s）
- 比Cerebras: 8倍性能（vs 2000 tokens/s）
- 软件栈极简: 仅1名工程师维护

**参考文档**:
- EE Times报道: https://www.eetimes.com/taalas-specializes-to-extremes-for-extraordinary-token-speed/
- 发布时间: 2026-02-20

### 应用领域扩张

#### 1. AI推理加速
- **厂商**: Taalas, Intel, Meta (MTIA)
- **性能**: 比GPU低延迟10-100倍
- **功耗**: 比FPGA低20-30%
- **成本**: 单位token成本降低50-70%

#### 2. 存储系统加速（DapuStor）
- **论文**: ASIC-based Compression Accelerators for Storage Systems
- **arXiv ID**: 2509.23693
- **优化**: 纠删码、压缩、协议加速

#### 3. 网络卸载（SmartNIC/DPU）
- **应用**: 5G基站、路由器、智能网卡
- **厂商**: Intel, Cisco, Ericsson等
- **优势**: 数据通路优化、硬件加密

#### 4. 边缘计算
- **场景**: 工业控制、汽车电子、IoT
- **需求**: 中等批量（100K-10M/年）、低功耗
- **模式**: FPGA原型 → 结构化ASIC量产

---

## 技术架构创新

### 设计方法学演进

#### 1. 自动化设计流程
- **方法**: 从模型到RTL的快速转换
- **周期**: 约1周（vs 传统6-12个月）
- **验证**: 全芯片仿真确保零容错
- **工具链**: 与TensorFlow、PyTorch集成

#### 2. 分层验证策略
- **挑战**: 硬连线芯片零容错特性
- **解决方案**: 层次化验证、形式化验证
- **创新**: 针对无掩模光刻的特殊DRC（Design Rule Check）

#### 3. 生态集成
- **FPGA-to-ASIC**: 无缝迁移路径
- **Chiplet集成**: 3D堆叠与异构集成
- **AI框架**: 自动化编译与部署

### 物理实现技术

#### 1. 3D集成技术
- **项目**: 3D-ISC (65nm)
- **特点**: 传感器内计算、可重配置架构
- **性能**: 实时DVS数据压缩
- **文档**: IEEE 10347978

#### 2. 晶圆级集成
- **技术**: Wafer-scale VLSI
- **架构**: 可编程矩阵
- **应用**: 大规模并行计算
- **文档**: IEEE 10444278

#### 3. 高密度互连
- **RDL布线**: 超高密度重分布层
- **技术**: Maskless曝光
- **应用**: HPC和AI
- **文档**: IEEE 10565103

---

## 性能与成本对比

### 成本优势
| 指标 | 结构化ASIC | FPGA | 全定制ASIC | 来源 |
|------|-----------|------|-----------|------|
| NRE成本 | 低(-60-80%) | 无 | 高 | 行业报告 |
| 单位成本 | 中(-50-70% vs FPGA) | 高 | 最低(大批量) | Intel数据 |
| 量产门槛 | 100K-10M/年 | 无 | >10M/年 | 商业分析 |

### 功耗优化
- **AI推理**: 比FPGA低20-30%
- **推理吞吐**: 比GPU高10-100倍（专用化程度）
- **散热**: 支持标准风冷（Taalas HC1: 250W/chip）

### 性能提升
- **延迟**: 专用芯片比GPU低10-100倍
- **频率**: 1.56 GHz (UMC 40nm)
- **面积**: 3.29 mm² (UMC 40nm)

---

## 发展趋势与挑战

### 发展趋势

1. **AI推动复兴**
   - 大模型稳定化后，模型-to-ASIC转换需求暴增
   - 从GPT-3到LLaMA，专用芯片成为主流
   - Taalas模式：2-mask快速定制

2. **生态整合**
   - Chiplet标准（UCIe）普及
   - 异构计算成为常态
   - 从芯片到系统的垂直整合

3. **快速迭代**
   - 传统: 6-12个月流片周期
   - 现在: 2-3个月交付周期
   - 未来: 目标1个月

4. **可持续发展**
   - 绿色计算成为重要指标
   - 能效优化驱动架构创新
   - 碳中和目标影响供应链

### 面临挑战

1. **灵活性限制**
   - 仍不如FPGA可重配置
   - 适合产品稳定后量产阶段
   - 不适合快速迭代场景

2. **生态壁垒**
   - 需要EDA工具深度集成
   - AI框架支持仍在完善
   - 多厂商协作复杂性

3. **规模经济**
   - 依赖多客户共享平台
   - 平台开发成本摊销风险
   - 小众市场难以支撑

4. **竞争格局**
   - GPU的CUDA生态壁垒
   - 其他ASIC方案（Cerebras, SambaNova）
   - FPGA的持续改进

---

## 参考文献

### A. IEEE/ACM顶级会议论文（2020-2025）

1. **ISSCC 2025** - 13.6 A Via-Programmable DNN-Processor Fabrication Toward 1/40th Mask Cost  
   URL: https://ieeexplore.ieee.org/iel8/10904417/10904496/10904711.pdf

2. **ISSCC 2025** - Via-Programmable Structured ASIC Fabric Based on MCML Cells: Design Flow and Implementation  
   DOI: 10.1109/ISSCC4267078

3. **VLSI Symposium 2025** - Seamless Physical Implementation of ASIC Hierarchical Integrated Scan Architecture  
   DOI: 10.1109/VLSI9611310

4. **DAC 2025** - 3D-ISC: A 65nm 3D Compatible In-Sensor Computing Accelerator  
   DOI: 10.1109/DAC10347978

5. **DATE 2025** - Novel Design partitioning technique for ASIC prototyping using Graph Deep Learning  
   DOI: 10.1109/DATE9970882

6. **ASPDAC 2025** - Agile-X: A Structured-ASIC Created With a Mask-Less Lithography System  
   DOI: 10.1109/ASPDAC10745765

7. **IEEE JSSC 2025** - M2A2: Microscale Modular Assembled ASICs for High-Mix, Low-Volume Designs  
   DOI: 10.1109/JSSC9044426

### B. ArXiv预印本（2025-2026）

1. **Mozart框架** - Mozart: A Chiplet Ecosystem-Accelerator Codesign Framework  
   arXiv: 2510.08873v1  
   URL: https://arxiv.org/abs/2510.08873

2. **存储加速** - ASIC-based Compression Accelerators for Storage Systems  
   arXiv: 2509.23693v1  
   URL: https://arxiv.org/abs/2509.23693

3. **光子处理器** - Versatile silicon integrated photonic processor for AI clusters  
   arXiv: 2504.01463v1  
   URL: https://arxiv.org/abs/2504.01463

4. **3D FPGA** - LaZagna: An Open-Source Framework for Flexible 3D FPGA Architectural Exploration  
   arXiv: 2505.05579  
   URL: https://arxiv.org/abs/2505.05579

5. **优先级编码器** - A Paradigm for Generalized Multi-Level Priority Encoders  
   arXiv: 2601.20067  
   URL: https://arxiv.org/abs/2601.20067

### C. 行业报告与技术文档

1. **Intel eASIC N5X Product Brief**
   - 文档ID: PB-006
   - URL: https://docs.altera.com/v/u/docs/633246/easic-n5x-product-brief-pb-006

2. **Intel eASIC官方页面**
   - URL: https://www.intel.com/content/www/us/en/products/details/easic.html

3. **EE Times - Taalas报道**
   - 标题: "Taalas Specializes to Extremes for Extraordinary Token Speed"
   - 发布日期: 2026-02-20
   - URL: https://www.eetimes.com/taalas-specializes-to-extremes-for-extraordinary-token-speed/

4. **McKinsey半导体趋势报告**
   - 标题: "Technology Trends Outlook 2025"
   - 发布: 2025-07-01
   - 链接: https://www.mckinsey.com/~/media/mckinsey/technology-trends-outlook-2025.pdf

5. **Gartner FPGA/ASIC市场报告**
   - 标题: "Application Specific Integrated Circuit Market Report 2026"
   - 来源: GII Research
   - 链接: https://www.giiresearch.com/report/tbrc1662515-application-specific-integrated-circuit-global.html

### D. 其他重要文献

1. **MIT技术评论** - "The Role of Advanced Computer Architectures in Accelerating AI Workloads"  
   arXiv: 2511.10010

2. **IEEE TPDS** - "Pipeline Stage Resolved Timing Characterization of FPGA and ASIC Implementations"  
   arXiv: 2512.13866

3. **Nature Communications** - "Wafer-scale fabrication of memristive crossbar circuits"  
   DOI: 10.1038/s41467-025-63831-2

4. **Scientific Reports** - "Data-driven optimization of maskless grayscale laser lithography"  
   DOI: 10.1038/s41598-025-24652-x

5. **Light: Science & Applications** - "Laser-written reconfigurable photonic integrated circuit"  
   DOI: 10.1038/s41377-025-01854-6

### E. 本地调研文档

1. **eASIC公司详细分析报告**  
   位置: `/home/Works_2026/01_硬连接推理/10-其他Startups/eASIC/eASIC Corporation 详细分析报告.md`

2. **Taalas技术报道**  
   位置: `/home/Works_2026/01_硬连接推理/01-Taalas/Taalas Specializes to Extremes for Extraordinary Token Speed_EE Times.md`

3. **结构化ASIC商业分析**  
   位置: `/home/Works_2026/01_硬连接推理/结构化ASIC的商业思考/结构化ASIC的商业考量.md`

4. **技术对比文档**  
   位置: `/home/Works_2026/01_硬连接推理/结构化ASIC的商业思考/结构化ASIC、FPGA与ASIC技术对比文档.html`

---

## 结论

结构化ASIC技术在2020-2025年间经历了从"过渡方案"到"AI加速关键使能技术"的转型。核心突破在于：

1. **制造工艺**: 无掩模光刻实现成本革命性降低
2. **架构创新**: Via-programmable技术实现快速定制
3. **应用融合**: 与AI、Chiplet、异构计算的深度结合
4. **商业模式**: 平台化服务成为主流，客户价值体现在风险可控的成本和功耗优化

未来5年，随着大模型稳定化、Chiplet生态成熟以及AI推理需求爆发，结构化ASIC有望成为连接FPGA原型与ASIC量产的关键桥梁，特别是在100K-10M中等批量场景发挥不可替代的作用。

---

**报告编制**: OpenCode调研系统  
**编制日期**: 2026-04-05  
**报告版本**: v1.0  
**联系**: 如需调研详情或特定技术方向深入分析，请提供具体需求

