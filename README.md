# Project Code Explanation

## Classes and Structure

1. **`ScenarioNetwork`**: This class builds the Directed Acyclic Graph (DAG) representing the project stages, with each node as a project stage and each directed edge as a possible transition between stages.

2. **`FuzzyLinguisticDescriptor`**: This class establishes linguistic variables with basic membership functions (Low, Medium, High). These functions represent fuzzy categories, enabling qualitative assessments of project indicators and external factors.

3. **`TSKFuzzyNetwork`**: This class defines a simplified Takagi-Sugeno-Kang (TSK) fuzzy neural network. It uses fuzzy logic to combine inputs and derive outputs based on fuzzy production rules, which guide the project’s stage transition decisions.

4. **`CybersecurityProjectSimulation`**: This class manages the project’s lifecycle through its stages, utilizing the fuzzy rules and the TSK network to adaptively transition between stages, in response to external factors and project outcomes.

## Fuzzy Rules and Evaluation

- **Fuzzy Logic Rules**: Fuzzy rules are set to evaluate the current state based on `TrendReq` (required level of cybersecurity) and `TrendCap` (current capacity to meet cybersecurity needs). These fuzzy rules determine the likelihood of transitioning to each possible next stage.
  
- **Weighted Decision Making**: The TSK fuzzy network calculates weighted outcomes from multiple fuzzy rules to choose the next stage. Higher weights reflect a stronger alignment with the current project conditions, allowing the network to adaptively choose paths based on rule confidence.

## Running the Simulation

- **Simulation Flow**: The simulation starts at the initial stage (the source node in the DAG). It evaluates the current state and conditions using fuzzy logic, then selects the next stage based on the weighted fuzzy rules. The process repeats until the simulation reaches the final stage (sink node) or no further transitions are available.

- **Program Extension**: This program is designed to be expanded with real fuzzy parameters and more complex rule structures. Additional machine learning elements could further refine rule adaptations based on dynamic project and external factor data, providing a more robust simulation for real-world cybersecurity projects.



# External Factors Dataset for Cybersecurity Management Project

| Feature                    | Description                                                                                           | Range              | Source                                                                                      |
|----------------------------|-------------------------------------------------------------------------------------------------------|---------------------|---------------------------------------------------------------------------------------------|
| `EconomicPressure`         | Level of financial or budgetary pressure on the project                                               | >0                 | Economic and financial analysis reports                                                     |
| `RegulatoryChanges`        | Frequency of regulatory and compliance requirement changes                                            | 0-10               | Compliance monitoring systems, regulatory update reports                                    |
| `TechnologyAvailability`   | Accessibility of new cybersecurity technologies                                                       | >0                 | Market analyses, tech trend reports                                                         |
| `ThreatActivity`           | Cyber threat activity levels                                                                          | >0                 | Cybersecurity threat intelligence feeds, monitoring systems                                 |
| `MarketInnovation`         | Rate of innovation in the cybersecurity industry                                                      | 0-100              | Industry research reports, whitepapers on cybersecurity market trends                       |
| `PoliticalStability`       | Political stability impacting project environments                                                   | 0-5                | Political risk analysis, reports from international organizations                           |
| `GlobalThreatLevel`        | Overall global cyber threat level                                                                     | >0                 | International threat intelligence sources, global cybersecurity risk assessments            |
| `DataBreachIncidents`      | Number of reported data breach incidents                                                              | Integer            | Internal incident reports, industry data breach databases                                   |
| `CybersecurityBudgets`     | Budgets allocated specifically for cybersecurity measures                                             | Approx. 30-70M     | Internal financial records, cybersecurity budget planning reports                           |
| `ITWorkforceAvailability`  | Availability of skilled IT and cybersecurity professionals                                            | 0-10               | Workforce analytics, labor market research reports                                          |
| `TechnologyMaturity`       | Maturity level of technology used in cybersecurity                                                   | 0-100              | Maturity assessment reports, technical audits                                               |
| `SecurityComplianceRate`   | Percentage of compliance with security standards and policies                                         | 0-100%             | Compliance audit results, internal policy adherence reports                                 |
| `UserAwarenessLevel`       | Percentage of user awareness and training in cybersecurity protocols                                  | 0-100%             | Employee survey results, training program completion metrics                                |
| `RansomwareIncidents`      | Number of ransomware incidents impacting the organization                                             | Integer            | Security event monitoring tools, incident response reports                                  |
| `GlobalCyberPolicyChange`  | Changes in international cybersecurity policies impacting local regulations                           | >0                 | Policy review reports, industry publications on regulatory trends                           |
| `SupplyChainRisk`          | Risk levels associated with supply chain vulnerabilities                                              | >0                 | Supply chain risk assessment reports, external vendor evaluations                           |
| `CloudDependency`          | Extent of reliance on cloud-based technologies                                                        | 0-100%             | IT infrastructure reports, cloud usage analytics                                            |
| `ThirdPartyRisk`           | Risk levels posed by third-party vendors and service providers                                        | Approx. 30-70      | Vendor risk assessments, third-party risk management reports                                |
| `IoTThreatLevel`           | Threat level in the organization’s Internet of Things (IoT) ecosystem                                 | >0                 | IoT security monitoring systems, IoT threat intelligence feeds                              |
| `DigitalTransformationIndex` | Overall progress and investment in digital transformation initiatives                               | 0-100              | Digital strategy reports, benchmarking assessments of digital transformation readiness      |

Each feature in this table represents a potential external factor that can influence the management of a cybersecurity project. The "Source" field lists potential data sources that can be used for gathering relevant information.
