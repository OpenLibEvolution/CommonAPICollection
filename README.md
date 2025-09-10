# Common API Collection

## Project Overview
Common API Collection is an open-source project dedicated to collecting, organizing, and standardizing core API information for common components/libraries across various language ecosystems. This project provides structured API metadata including class/method/field signatures, parameter types, return values, etc., to support code generation and component upgrade scenarios.

**Important Notice**: All data is automatically generated and cannot be modified directly. However, we strongly encourage developers to report issues and suggest improvements!

## Project Vision
- 🌐 Create a multilingual API metadata hub
- 📚 Provide machine-readable API data structures
- 🛠️ Support developer tools and automation workflows
- 🤝 Advance dataset development through community collaboration

## Supported Ecosystems
| Ecosystem | Status       | Maintainer     |
|-----------|--------------|----------------|
| Java (Maven) | ✅ Active | @openlibevolution |
| Python (PyPI) | ⏳ Planned |  |
| JavaScript (npm) | ⏳ Planned |  |

## Directory Structure
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

## Data Format Example (log4j API)
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

## How to Contribute

### 🐛 Report Data Issues
If you find:
- Incorrect API signatures
- Missing common members
- Missing essential methods
- Inaccurate labels

**Submission Steps**:
1. Visit [Issues page](https://github.com/OpenLibEvolution/CommonAPICollection/issues)
2. Use **"Data Accuracy Report"** template
3. Provide concrete evidence (official documentation links or real project code snippets)

### 💡 Suggest New Components/Ecosystems
Want us to support new components or ecosystems?
1. Use **"Component Request"** template
2. Include:
   - Component name and official repository
   - Typical usage scenarios
   - Importance analysis in ecosystem

### 🔍 Propose Data Format Improvements
Have professional suggestions for API data format?
- Create **"Methodology Enhancement"** topic in Discussions
- Describe your suggested improvement algorithms or data sources

### 🚀 Share Use Cases
We particularly welcome:
- Research papers based on this dataset
- Development tool integrations (e.g. IDE plugins)
- Code quality analysis tool applications

Share your achievements in **"Showcases"** category of Discussions!

## License
This project is licensed under [CC BY-NC-SA 4.0](LICENSE).

## Support & Contact

- 🐞 **Issue Reporting**: [Issues](https://github.com/OpenLibEvolution/CommonAPICollection/issues)
- 💬 **Technical Discussion**: [Discussions](https://github.com/OpenLibEvolution/CommonAPICollection/discussions)
- 📧 **Urgent Contact**: openlibevolution@gmail.com

---

**Your Insights Make Automated Data Better!**  
While data is machine-generated, human expertise is key to improving quality. We look forward to your professional feedback!