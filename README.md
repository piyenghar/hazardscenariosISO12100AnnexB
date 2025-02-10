# hazardscenarios_iso12100AnnexB
Comprehensive curated dataset of hazard scenarios systematically generated based on annex B of ISO12100 and PLr assigned based on ISO 13849. The dataset comprises of the following files: 

**combination_of_hazards_hazard_scenarios.json:** Contains hazard scenarios specifically related to combinations of different hazards.

**electrical_hazards_hazard_scenarios.json: ** Contains hazard scenarios specifically related to electrical hazards.

**environmental_hazards_hazard_scenarios.json:** Contains hazard scenarios specifically related to environmental hazards.

**ergonomic_hazards_hazard_scenarios.json:** Contains hazard scenarios specifically related to ergonomic hazards.

**material_substance_hazards_hazard_scenarios.json:** Contains hazard scenarios specifically related to hazards from materials and substances.

**mechanical_hazards_hazard_scenarios.json: **Contains hazard scenarios specifically related to mechanical hazards.

**noise_hazards_hazard_scenarios.json:** Contains hazard scenarios specifically related to noise hazards.

**radiation_hazards_hazard_scenarios.json:** Contains hazard scenarios specifically related to radiation hazards.

**thermal_hazards_hazard_scenarios.json:** Contains hazard scenarios specifically related to thermal hazards.

**vibration_hazards_hazard_scenarios.json:** Contains hazard scenarios specifically related to vibration hazards.

**plausible_combinations_hazards_origin_consequences.json:** Defines the plausible combinations of hazards, their origins, and potential consequences.
**safety_parameters_updated.json:** Contains updated safety parameters used in the hazard scenario generation.



The hazard scenarios file comprise of the following template for each entry. **Explanation of the elements in the template:**

"**Hazard ID**": A unique identifier assigned to each hazard scenario. This ID can be used for referencing and tracking individual scenarios.  It often incorporates abbreviations for the hazard type (e.g., ME for Mechanical, EL for Electrical) followed by a sequential number.

"**Hazard Type**": The general category of the hazard, as defined in ISO 12100, Annex B.  Examples include "Mechanical Hazards," "Electrical Hazards," "Thermal Hazards," etc.

"**Origin**": The specific source or cause of the hazard. For example, within "Mechanical Hazards," an origin could be "Rotating Elements," "Sharp Edges," or "Falling Objects."

"**Potential Consequence**": The potential negative outcome or injury that could result from the hazard. Examples include "Entanglement," "Electrocution," "Burns," "Hearing Loss," etc.

"**User Type**": The role of the person interacting with the machinery when the hazard occurs.  Common user types include "Operator," "Maintenance Personnel," "Setup/Programmer," etc.  This helps to consider different risk profiles based on user roles.

"**Task**": The specific action or activity the user is performing when exposed to the hazard.  Examples are "Normal Operation," "Cleaning," "Maintenance," "Setup/Programming."  The task influences the likelihood and nature of potential hazards.

"**Environment**": The context or setting where the machinery is operating.  This could be "Industrial," "Outdoor," or other relevant environments.  The environment can influence the severity or likelihood of certain hazards.

"**Severity**": The level of potential injury resulting from the hazard.  This is often categorized using terms like "slight," "serious," or "fatal," corresponding to S1 and S2 in ISO 13849-1.

"**Frequency**": How often a person is likely to be exposed to the hazard.  Categories like "seldom-to-less-often," "frequent-to-continuous" (F1 and F2 in ISO 13849-1) are typically used.

"**Possibility**": The likelihood of the potential consequence occurring, given the hazard and origin.  Terms like "possible," "likely," or "rare" are used, corresponding to P1 and P2 in ISO 13849-1.

"**PLr**": The required Performance Level, a measure of the reliability and effectiveness of safety functions needed to mitigate the risk.  This is determined based on the severity, frequency, and possibility of harm, as defined in ISO 13849-1.

"**Description**": A detailed narrative describing the hazard scenario, combining all the information from the other fields. This provides a clear and concise summary of the scenario for risk assessment purposes.


The "**Description**" field of each hazard scenario is dynamically generated based on the following template, incorporating the specific values for environment, user type, task, origin, consequence, frequency, and possibility:

"Description": In {env} settings, {user_type} performing {task} tasks may encounter {origin}, which can lead to {consequence}. These tasks are classified as {freq_desc}, with a possibility described as {poss_desc}. The severity of potential injuries is described as {severity_desc}."

