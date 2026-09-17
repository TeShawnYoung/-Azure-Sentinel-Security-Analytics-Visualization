# Azure Sentinel Security Analytics & Visualization

## Project Overview

This project demonstrates the development of **Microsoft Sentinel security analytics, KQL queries, and interactive security workbooks** designed to transform raw security telemetry into actionable visualizations for security monitoring, threat hunting, and investigation.

The project focuses on building practical security monitoring scenarios across endpoint, identity, network, threat intelligence, and Azure resource telemetry.

Each scenario includes the underlying **KQL query**, **Microsoft Sentinel Workbook**, **visual dashboard**, and detailed documentation explaining the analysis and security findings. 

---

## Core Visualizations & Security Scenarios

### 1. ☁️ Azure Resource Creation & Modifications

**Focus:** Monitoring Azure resource creation and modification activity.

**Key Capabilities:**

* Azure resource activity monitoring
* Administrative action analysis
* Resource creation tracking
* Modification tracking
* Investigation of potentially unauthorized cloud activity

**Resources:**

* 📄 [Detailed Lab Documentation](Documentation/Azure-Resource-Creation-Modifications.md)
* 📊 [Workbook JSON](Workbooks/Azure-Resource-Creation-Modifications.json)
* 🔎 [KQL Query](Queries/Azure-Resource-Creation-Modifications.kql)
* 🖼️ [Dashboard Screenshot](Screenshots/Azure-Resource-Creation-Modifications.png)

---

### 2. 📤 Data Exfiltration

**Focus:** Identification and visualization of potentially unusual data transfer activity.

**Key Capabilities:**

* Data transfer analysis
* Source and destination investigation
* High-volume activity identification
* Geographic and network context
* Potential exfiltration pattern analysis

**Resources:**

* 📄 [Detailed Lab Documentation](Documentation/Data-Exfiltration.md)
* 📊 [Workbook JSON](Workbooks/Data-Exfiltration.json)
* 🔎 [KQL Query](Queries/Data-Exfiltration.kql)
* 🖼️ [Dashboard Screenshot](Screenshots/Data-Exfiltration.png)

---

### 3. 🚨 Azure Sentinel (SIEM) Identity & Endpoint Authentication Monitoring

**Focus:** A multi-scenario Sentinel workbook project correlating identity and endpoint authentication telemetry to surface credential attacks, account compromise, and brute-force activity in near real time.

**Log Sources:** `SigninLogs`, `DeviceLogonEvents`

**Scenarios Covered:**

* **Entra ID Authentication Failures** — failed sign-in analysis, source IP investigation, geographic patterns, and account-targeting analysis to identify potential credential attacks.
* **Entra ID Authentication Success** — successful sign-in monitoring, geographic source analysis, and user/application context to flag unusual or potentially compromised account activity.
* **VM Authentication Failures** — failed authentication attempts against Azure virtual machines, source IP investigation, and geographic visualization to identify potential brute-force activity.

**Key Capabilities:**

* Cross-scenario identity and endpoint authentication monitoring
* Source IP and geographic authentication pattern analysis
* Account and device targeting analysis
* Correlation between failed and successful authentication activity
* Identification of credential attacks, brute-force attempts, and potentially compromised accounts

**Resources:**

* 📦 [Project Repository](https://github.com/TeShawnYoung/Azure-Sentinel-SIEM-Identity-Endpoint-Authentication-Monitoring)
* 📄 [Entra ID Authentication Failures](https://github.com/TeShawnYoung/Azure-Sentinel-SIEM-Identity-Endpoint-Authentication-Monitoring/tree/main/Entra-ID-Authentication-Failures)
* 📄 [Entra ID Authentication Success](https://github.com/TeShawnYoung/Azure-Sentinel-SIEM-Identity-Endpoint-Authentication-Monitoring/tree/main/Entra-ID-Authentication-Success)
* 📄 [VM Authentication Failures](https://github.com/TeShawnYoung/Azure-Sentinel-SIEM-Identity-Endpoint-Authentication-Monitoring/tree/main/VM-Authentication-Failures)

---

### 4. 🌍 Inbound Authentication Origins

**Focus:** Geographic analysis of external authentication activity.

**Log Source:** `DeviceLogonEvents`

**Key Capabilities:**

* Geographic visualization of external source IP addresses
* Successful vs. failed authentication analysis
* Authentication source volume analysis
* Targeted device and account identification
* Identification of unusual geographic authentication patterns

**Resources:**

* 📄 [Detailed Lab Documentation](Documentation/Inbound-Authentication-Origins.md)
* 📊 [Workbook JSON](Workbooks/Inbound-Authentication-Origins.json)
* 🔎 [KQL Query](Queries/Inbound-Authentication-Origins.kql)
* 🖼️ [Dashboard Screenshot](Screenshots/Inbound-Authentication-Origins.png)

---

### 5. 🛡️ Inbound Threat Intelligence

**Focus:** Geographic and source-level visualization of inbound activity associated with threat intelligence data.

**Key Capabilities:**

* Threat intelligence correlation
* Source IP analysis
* Geographic threat visualization
* Identification of potentially malicious sources
* Investigation prioritization

**Resources:**

* 📄 [Detailed Lab Documentation](Documentation/Inbound-Threat-Intel.md)
* 📊 [Workbook JSON](Workbooks/Inbound-Threat-Intel.json)
* 🔎 [KQL Query](Queries/Inbound-Threat-Intel.kql)
* 🖼️ [Dashboard Screenshot](Screenshots/Inbound-Threat-Intel.png)

---

### 6. 🌐 Outbound Connections

**Focus:** Analysis and visualization of outbound network connections.

**Log Source:** `DeviceNetworkEvents`

**Key Capabilities:**

* External destination analysis
* Source device identification
* Connection volume analysis
* Geographic/network visualization
* Investigation of unusual outbound activity

**Resources:**

* 📄 [Detailed Lab Documentation](Documentation/Outbound-Connections.md)
* 📊 [Workbook JSON](Workbooks/Outbound-Connections.json)
* 🔎 [KQL Query](Queries/Outbound-Connections.kql)
* 🖼️ [Dashboard Screenshot](Screenshots/Outbound-Connections.png)

---

## Technical Architecture & Workflow

1. **Ingestion**
   Security telemetry is collected through Microsoft Sentinel and connected data sources such as endpoint, identity, network, threat intelligence, and Azure activity logs.

2. **Data Extraction & Analysis**
   **Kusto Query Language (KQL)** is used to filter, transform, enrich, aggregate, and analyze security telemetry.

3. **Security Enrichment**
   Where applicable, telemetry is enriched with geographic, identity, network, or threat intelligence context to provide additional investigative value.

4. **Visualization**
   KQL results are transformed into interactive **Microsoft Sentinel Workbooks** using maps, tables, charts, and other visualization components.

5. **Investigation**
   Visualizations are designed to help analysts identify anomalies, prioritize suspicious activity, and develop additional investigative queries.

---

## Skills Demonstrated

* **Microsoft Sentinel:** Security workbook development and visualization
* **KQL:** Query development, filtering, aggregation, transformation, and analysis
* **Security Monitoring:** Monitoring endpoint, identity, network, and cloud telemetry
* **Threat Hunting:** Identifying anomalous and potentially malicious activity
* **Security Investigation:** Source, account, device, geographic, and activity analysis
* **Security Data Enrichment:** Adding geographic and threat intelligence context
* **Data Visualization:** Converting security telemetry into analyst-focused dashboards
* **SIEM Operations:** Using Microsoft Sentinel to support security monitoring and investigation
