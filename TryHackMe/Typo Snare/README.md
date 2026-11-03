# Ransomware Attack — Threat Hunting Investigation

**Platform:** TryHackMe  
**Environment:** TryGovMe  
**Investigation Type:** Threat Hunting / Incident Reconstruction  
**Affected Organisation:** SwiftSpend Financial  
**Incident Date:** 26 September 2023  
**Status:** Investigation in Progress

---

## 1. Investigation Overview

### Background

On 26 September 2023, SwiftSpend Financial experienced a ransomware incident affecting two developer workstations. At approximately 4:00 PM, the Security Operations Center (SOC) received an alert indicating that both systems had been encrypted and ransom notes had appeared.

Shortly before the incident, the central SIEM became unavailable, limiting the team's visibility. Fortunately, logs from both affected endpoints had been preserved for further investigation.

Initial information suggested that the compromise may have originated from Perry's workstation after he downloaded a third-party utility to extract an encrypted `.7z` archive.

This investigation aims to reconstruct the attacker's activities using available endpoint logs, command-line artifacts, process relationships, and indicators of compromise.

### Investigation Objectives

- Validate the initial threat hunting hypothesis using available evidence.
- Investigate known indicators of compromise (IOCs) and identify additional suspicious activity.
- Reconstruct the attack chain from initial access through ransomware deployment.
- Correlate attacker behaviour with the MITRE ATT&CK framework.
- Identify compromised accounts, affected systems, and the overall impact.
- Document findings and recommend appropriate incident response actions.

## 2. Initial Threat Intelligence

The SOC team provided the following indicators to support the investigation.

### Network Indicators

| Type | Indicator |
|---|---|
| Domain | `7zipp.org` |
| IP Address | `206.189.34.218` |

### Host Indicators

| Type | Indicator |
|---|---|
| File extensions | `.777zzz`, `.msi`, `.ps1` |
| File names | `7zipp.exe`, `7zipp.dll`, `mimikatz.exe` |

### File Hashes

```text
4b9213d22989474b467aa53080d9e295
29efd64dd3c7fe1e2b022b7ad73a1ba5
61c0810a23580cf492a6ba4f7654566108331e7a4134c968c2d6a05261b2d8a1
fd713992f39338986e8573aff1232675323fde827328159b29a31cc3cd515874
```

**Note:** These are investigation leads supplied in the scenario. Their presence, maliciousness, and relationship to the incident must be validated against the available evidence.

## 3. Threat Hunting Hypothesis

The initial hypothesis is that Perry's workstation was compromised after downloading and executing a malicious utility disguised as legitimate archive extraction software.

The attacker may have used this initial foothold to execute additional tools, compromise credentials, move to another workstation, interfere with security monitoring, and ultimately deploy ransomware.

**Hypothesis Status:** Pending validation.

---

## 4. Investigation and Evidence

*To be completed as the investigation progresses.*

## 5. Attack Chain Reconstruction

*Pending investigation findings.*

## 6. Scope and Impact

*Pending identification of affected systems, accounts, and assets.*

## 7. MITRE ATT&CK Mapping

*To be populated with techniques supported by investigation evidence.*

## 8. Incident Response Recommendations

*To be completed after reconstructing the attack.*

## 9. Conclusion and Lessons Learned

*To be completed after the investigation.*
