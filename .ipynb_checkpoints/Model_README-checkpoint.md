
# Forest Industry Climate Impact Assessment Model

---

Welcome to the Forest Industry Climate Impact Assessment Model repository. This model provides a comprehensive landscape-level assessment of the forest industry's climate impact, focusing on the supply side. It simulates various forest management practices using the forest estate model and examines how changes in forest supply affect the overall climate performance of the forest industry.

---

## 🌲 Scenario Illustration

Consider a simplified forest industry scenario:

- If a particular area is not harvested, the forest continues to grow. Trees shed leaves and other organic matter, which decays, but there's no supply for the downstream industry.
  
- If the area is harvested, logs are removed, eliminating litterfall until the next generation of trees grows. The remaining branches and roots decay in the ecosystem. The harvested logs go to lumber mills, emitting greenhouse gases during the manufacturing process. The lumber becomes products that decay over time. If sawdust and shavings turn into bioenergy, they can replace coal, reducing emissions.

The decision to harvest or not has distinct overall emissions outcomes.

Our model replicates these processes within the forest industry, giving users choices about harvesting methods and the resulting system-level climate impacts.

---

## 📊 Model Selections 

| Model                            | Emission Phase                                           |
|----------------------------------|----------------------------------------------------------|
| Forest estate model (ws3)        | Carbon sequestration                                     |
| Ecosystem carbon model (libCBM)  | Ecosystem carbon pool dynamics                           |
|                                  | Dead organic matter decay emission                       |
| First-order decay model          | Harvested wood products life decay                       |
|                                  | Harvested wood products landfill decay                   |
| Life cycle assessment model      | Forest operational emission                              |
|                                  | Harvested wood products manufacturing emission           |
|                                  | Harvested wood products transportation emission          |
|                                  | Harvested wood products substitution emission            |
| DLCIA model                      | Convert emission to climate impact                       |

---

## 📜 Table of Contents
- [Background](#background)
- [Model Overview](#model-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Data Sources](#data-sources)
- [Model Outputs](#model-outputs)
- [Contributing](#contributing)
- [Contact & Support](#contact--support)
- [Acknowledgments](#acknowledgments)

---

## 📚 Background
While many studies have extensively explored forest carbon dynamics, none have holistically considered all the emission phases within the forest industry. Many disciplines draw conclusions within their specific sections, but optimizing each section individually doesn't provide an overarching perspective. This system-level assessment integrates all sections to offer a comprehensive view of forest industry carbon management.

---

## 📈 Model Overview
- **Objective**: Assess the climate impact of the forest industry under various harvest scenarios.
- **Components**: Forest estate model, forest ecosystem carbon model, wood products decay model, life cycle assessment model, and climate impact conversion model.
- **Assumptions**: All the supply from the forest could be accepted by the downstream industry.

---

## 🛠 Installation
All installation procedures are coded within the script.

---

## 💼 Usage
The model is divided into various sections, with detailed instructions provided in each. Refer to the README file in each document for guidance.
- Inventory analysis and curve generation
- Forest estate model simulation and associated forest ecosystem carbon simulation
- Overall emission calculation and climate impact conversion
- Result analysis

---

## 📊 Data Sources
- **Inventory Data**: Forest inventory data is from the Vegetation Resource Inventory and can be sourced from the [government website](https://www2.gov.bc.ca/gov/content/industry/forestry/managing-our-forest-resources/forest-inventory/data-management-and-access/vri-data-standards).
- **Life Cycle Inventory Data**: Ecoinvent v3.9 and Canadian fuel LCI.

---

## 📉 Model Outputs
The model produces results section by section. The primary outcome is the climate impact, measured in terms of carbon dioxide emissions over a specific timeframe (typically 500 years) and GHG emissions for each period.
- **Visualizations**: Climate impact comparison reports for different harvest scenarios.
- **Data**: Emission tables.

---

## 🤝 Contributing
Feel free to contribute to the model if you have suggestions or improvements.

---

## 📞 Contact & Support
- **Lead Author**: [Jimmy Ke](https://www.linkedin.com/in/jimmy-ke/) - jimmy49594823@gmail.com
- **Maintenance**: Gregory Paradis - gregory.paradis@ubc.ca

---

## 🏆 Acknowledgments
Jimmy Ke spearheaded the development and conceptualization of this model. He managed model connections, performance tuning, the HWP decay model, LCA modeling, data collection, emission calculations, climate impact conversions, and data analysis scripts.

Gregory Paradis originally created the inventory analysis and curve generation script that has been adapted for this model. Additionally, Greg provided an example of connecting the forest estate model with the carbon budget model, which Jimmy fine-tuned for project use.

---

Hope you find the model insightful! 🌳📊🌎
