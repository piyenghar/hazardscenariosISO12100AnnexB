## 📢 Update — July 2025

This dataset is introduced and described in the following publication:

**P. Iyenghar**, *On the Development and Application of a Structured Dataset for Data-Driven Risk Assessment in Industrial Functional Safety*,  
2025 IEEE 21st International Conference on Factory Communication Systems (WFCS), Rostock, Germany, 2025, pp. 1–8.  
[DOI: 10.1109/WFCS63373.2025.11077569](https://doi.org/10.1109/WFCS63373.2025.11077569) · [IEEE Xplore Link](https://ieeexplore.ieee.org/document/11077569)

---

### 📄 Citation

If you use this dataset, please cite:

```bibtex
@INPROCEEDINGS{11077569,
  author={Iyenghar, Padma},
  booktitle={2025 IEEE 21st International Conference on Factory Communication Systems (WFCS)},
  title={On the Development and Application of a Structured Dataset for Data-Driven Risk Assessment in Industrial Functional Safety},
  year={2025},
  pages={1-8},
  keywords={Accuracy;ISO Standards;Benchmark testing;Hazards;Risk management;Reliability;Scenario generation;Machinery;Artificial intelligence;Software development management;machinery safety;performance level;safety function;hazards;dataset;LLM;RAG},
  doi={10.1109/WFCS63373.2025.11077569}
}
```

## 📦 Description of the dataset — `hazardscenarios_iso12100AnnexB`

A **comprehensive, curated** dataset of hazard scenarios systematically generated based on **Annex B of ISO 12100** and assigned **Performance Level required (PLr)** according to **ISO 13849**.

---

### 📂 Files in the Dataset

| File name | Description |
|-----------|-------------|
| `combination_of_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to combinations of different hazards. |
| `electrical_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to electrical hazards. |
| `environmental_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to environmental hazards. |
| `ergonomic_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to ergonomic hazards. |
| `material_substance_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to hazards from materials and substances. |
| `mechanical_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to mechanical hazards. |
| `noise_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to noise hazards. |
| `radiation_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to radiation hazards. |
| `thermal_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to thermal hazards. |
| `vibration_hazards_hazard_scenarios.json` | Hazard scenarios specifically related to vibration hazards. |
| `plausible_combinations_hazards_origin_consequences.json` | Plausible combinations of hazards, their origins, and potential consequences. |
| `safety_parameters_updated.json` | Updated safety parameters used in hazard scenario generation. |

---

### 📝 Hazard Scenario Template

Each hazard scenario follows this structure:

| Field | Description |
|-------|-------------|
| **Hazard ID** | Unique identifier for each hazard scenario. Often includes abbreviations for the hazard type (e.g., `ME` for Mechanical, `EL` for Electrical) followed by a sequential number. |
| **Hazard Type** | General category of the hazard, as defined in ISO 12100 Annex B (e.g., Mechanical Hazards, Electrical Hazards, Thermal Hazards). |
| **Origin** | Specific source or cause of the hazard (e.g., *Rotating Elements*, *Sharp Edges*, *Falling Objects*). |
| **Potential Consequence** | Potential negative outcome or injury (e.g., *Entanglement*, *Electrocution*, *Burns*, *Hearing Loss*). |
| **User Type** | Role of the person interacting with the machinery when the hazard occurs (e.g., *Operator*, *Maintenance Personnel*, *Setup/Programmer*). |
| **Task** | Specific activity being performed (e.g., *Normal Operation*, *Cleaning*, *Maintenance*, *Setup/Programming*). |
| **Environment** | Operational context (e.g., *Industrial*, *Outdoor*). |
| **Severity** | Level of potential injury, corresponding to ISO 13849-1 categories S1 (*slight*) or S2 (*serious/fatal*). |
| **Frequency** | Exposure frequency, corresponding to ISO 13849-1 categories F1 (*seldom-to-less-often*) or F2 (*frequent-to-continuous*). |
| **Possibility** | Likelihood of occurrence, corresponding to ISO 13849-1 categories P1 (*possible*) or P2 (*likely*). |
| **PLr** | Required Performance Level for safety functions, derived from severity, frequency, and possibility. |
| **Description** | Full narrative description of the hazard scenario. |

---

### 📜 Description Field Generation Template

The `Description` field of each hazard scenario is dynamically generated using the following format:

```text
In {env} settings, {user_type} performing {task} tasks may encounter {origin}, 
which can lead to {consequence}. These tasks are classified as {freq_desc}, 
with a possibility described as {poss_desc}. The severity of potential injuries 
is described as {severity_desc}.
