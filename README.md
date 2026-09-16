# Azure Sentinel Security Analytics & Visualization

## Project Overview

This project demonstrates the development of **Microsoft Sentinel security analytics, KQL queries, and interactive security workbooks** designed to transform raw security telemetry into actionable visualizations for security monitoring, threat hunting, and investigation.

The project focuses on building practical security monitoring scenarios across endpoint, identity, network, threat intelligence, and Azure resource telemetry.

Each scenario includes the underlying **KQL query**, **Microsoft Sentinel Workbook**, **visual dashboard**, and detailed documentation explaining the analysis and security findings.

---

## Core Visualizations & Security Scenarios

### 1. 🌍 Inbound Authentication Origins

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

### 2. 🌐 Outbound Connections

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

### 3. 📤 Data Exfiltration

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

### 4. 🛡️ Inbound Threat Intelligence

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

### 5. 🔐 Entra ID Authentication Failures

**Focus:** Analysis of failed Microsoft Entra ID authentication activity.

**Log Source:** `SigninLogs`

**Key Capabilities:**

* Authentication failure analysis
* Source IP investigation
* Geographic authentication patterns
* Account targeting analysis
* Identification of potential credential attacks

**Resources:**

* 📄 [Detailed Lab Documentation](Documentation/Entra-ID-Authentication-Failures.md)
* 📊 [Workbook JSON](Workbooks/Entra-ID-Authentication-Failures.json)
* 🔎 [KQL Query](Queries/Entra-ID-Authentication-Failures.kql)
* 🖼️ [Dashboard Screenshot](Screenshots/Entra-ID-Authentication-Failures.png)

---

### 6. ✅ Entra ID Authentication Success

**Focus:** Analysis of successful Microsoft Entra ID authentication activity.

**Log Source:** `SigninLogs`

**Key Capabilities:**

* Successful authentication monitoring
* Geographic source analysis
* User and application context
* Unusual authentication identification
* Investigation of potentially compromised accounts

**Resources:**

* 📄 [Detailed Lab Documentation](Documentation/Entra-ID-Authentication-Success.md)
* 📊 [Workbook JSON](Workbooks/Entra-ID-Authentication-Success.json)
* 🔎 [KQL Query](Queries/Entra-ID-Authentication-Success.kql)
* 🖼️ [Dashboard Screenshot](Screenshots/Entra-ID-Authentication-Success.png)

---

### 7. ☁️ Azure Resource Creation & Modifications

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

### 8. 🖥️ VM Authentication Failures

**Focus:** Analysis of authentication failures targeting Azure virtual machines.

**Key Capabilities:**

* VM authentication monitoring
* Failed login analysis
* Source IP investigation
* Geographic activity visualization
* Identification of potential brute-force activity

**Resources:**

* 📄 [Detailed Lab Documentation](Documentation/VM-Authentication-Failures.md)
* 📊 [Workbook JSON](Workbooks/VM-Authentication-Failures.json)
* 🔎 [KQL Query](Queries/VM-Authentication-Failures.kql)
* 🖼️ [Dashboard Screenshot](Screenshots/VM-Authentication-Failures.png)

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

## Repository Structure

```text
Azure Sentinel Security Analytics & Visualization
│
├── README.md
│
└── LABS
    │
    ├── Inbound-Authentication-Origins
    │   ├── README.md
    │   ├── Inbound-Authentication-Origins.json
    │   ├── Inbound-Authentication-Origins.kql
    │   └── Inbound-Authentication-Origins.png
    │
    ├── Outbound-Connections
    │   ├── README.md
    │   ├── Outbound-Connections.json
    │   ├── Outbound-Connections.kql
    │   └── Outbound-Connections.png
    │
    ├── Data-Exfiltration
    │   ├── README.md
    │   ├── Data-Exfiltration.json
    │   ├── Data-Exfiltration.kql
    │   └── Data-Exfiltration.png
    │
    ├── Inbound-Threat-Intelligence
    │   ├── README.md
    │   ├── Inbound-Threat-Intelligence.json
    │   ├── Inbound-Threat-Intelligence.kql
    │   └── Inbound-Threat-Intelligence.png
    │
    ├── Entra-ID-Authentication-Failures
    │   ├── README.md
    │   ├── Entra-ID-Authentication-Failures.json
    │   ├── Entra-ID-Authentication-Failures.kql
    │   └── Entra-ID-Authentication-Failures.png
    │
    ├── Entra-ID-Authentication-Success
    │   ├── README.md
    │   ├── Entra-ID-Authentication-Success.json
    │   ├── Entra-ID-Authentication-Success.kql
    │   └── Entra-ID-Authentication-Success.png
    │
    ├── Azure-Resource-Creation-Modifications
    │   ├── README.md
    │   ├── Azure-Resource-Creation-Modifications.json
    │   ├── Azure-Resource-Creation-Modifications.kql
    │   └── Azure-Resource-Creation-Modifications.png
    │
    └── VM-Authentication-Failures
        ├── README.md
        ├── VM-Authentication-Failures.json
        ├── VM-Authentication-Failures.kql
        └── VM-Authentication-Failures.png
```

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
