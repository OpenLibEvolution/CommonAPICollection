# Common API Collection

## 项目概述
Common API Collection 是一个开源项目，旨在收集、整理和标准化各种语言生态中常见组件/库的核心API信息。本项目提供结构化的API元数据，包括类、方法、成员的参数个数、类型、返回值等信息，以支持代码生成、组件升级等应用场景。

**重要说明**：所有数据均由自动化流程生成，不接受直接修改，但我们强烈鼓励开发者报告问题、提出改进建议！

## 项目愿景
- 🌐 创建多语言生态的API元数据中心
- 📚 提供机器可读的API数据结构
- 🛠️ 支持开发者工具和自动化工作流
- 🤝 通过社区协作推进数据集的发展

## 支持的语言生态
| 生态系统 | 状态       | 维护者       |
|----------|------------|--------------|
| Java (Maven) | ✅ 活跃 | @openlibevolution |
| Python (PyPI) | ⏳ 计划中 |  |
| JavaScript (npm) | ⏳ 计划中 |  |

## 目录结构
```
common-api-collection/
├── maven/
│   ├── org/
│   │   ├── slf4j/
│   │   │   ├── slf4j-api.json
│   │   │   └── slf4j-simple.json
│   ├── junit/
│   │   └── junit.json
│   └── ... 
├── schemas/
│   └── api-schema-v1.json
├── LICENSE
└── README.md
```

## 数据格式示例 (log4j API)
```json
{
  "metadata": {
    "groupId": "org.slf4j",
    "artifactId": "slf4j-api",
    "ecosystem": "maven"
  },
  "versions": [
    {
      "version": "2.0.17",
      "apis": [
        {
          "class": "org.apache.logging.log4j.Logger",
          "fields": [
            {
              "name": "DEBUG",
              "type": "org.slf4j.event.Level"
            },
            {
              "name": "ERROR",
              "type": "org.slf4j.event.Level"
            }
          ],
          "methods": [
            {
              "name": "valueOf",
              "return_type": "org.slf4j.event.Level",
              "parameters": [
                {
                  "type": "java.lang.String",
                  "name": null
                }
              ]
            },
            {
              "name": "values",
              "return_type": "org.slf4j.event.Level[]",
              "parameters": []
            }
          ]
        }
      ]
    }
  ]
}
```

## 如何贡献

### 🐛 报告数据问题
如果您发现以下类型问题：
- API签名不正确
- 常用成员缺失
- 常用方法缺失
- 标签不准确

**提交问题步骤**：
1. 前往 [Issues页面](https://github.com/OpenLibEvolution/CommonAPICollection/issues)
2. 使用 **"Data Accuracy Report"** 模板
3. 提供具体证据（如官方文档链接或真实项目代码片段）

### 💡 建议新组件或生态
希望我们增加对新组件或生态的支持？
1. 使用 **"Component Request"** 模板
2. 包含以下信息：
   - 组件名称和官方仓库
   - 典型使用场景说明
   - 该组件在生态中的重要性分析

### 🔍 提议数据格式改进
对API数据的格式有专业建议？
- 在Discussions区创建 **"Methodology Enhancement"** 主题
- 描述您建议的改进算法或数据源

### 🚀 分享使用案例
我们特别欢迎：
- 基于本数据集的研究论文
- 开发工具集成案例（如IDE插件）
- 代码质量分析工具的应用

在Discussions区 **"Showcases"** 类别分享您的成果！

## 许可协议
本项目采用 [CC BY-NC-SA 4.0 许可](LICENSE)。

## 支持与联系

- 🐞 **问题报告**：[Issues](https://github.com/OpenLibEvolution/CommonAPICollection/issues)
- 💬 **技术讨论**：[Discussions](https://github.com/OpenLibEvolution/CommonAPICollection/discussions)
- 📧 **紧急联系**：openlibevolution@gmail.com

---

**您的洞察力让自动化数据更精准！**  
虽然数据是机器生成的，但人类的专业判断是提升质量的关键。期待您的专业反馈！