# Post-Quantum-TLS-Traffic-Captures-for-O-RAN

## Overview
This repository contains packet capture (PCAP) artifacts collected from controlled experiments on a real **OpenAirInterface (OAI) O-RAN testbed** at **UCD NetsLab**. The dataset captures TLS 1.3 secure channel establishment between the O-RAN Centralized Unit (O-CU) and Distributed Unit (O-DU) over the CU–DU transport (fronthaul) network.

Experiments were conducted using a **post-quantum-enabled build of BoringSSL**, enabling negotiation of classical, hybrid, and post-quantum cryptographic algorithms.

All configurations target **NIST Security Level-1**, ensuring fair and deployment-relevant comparison across cryptographic approaches.

---

## Scope
The captures demonstrate **transport-layer secure communication** between CU and DU nodes.

> **Note:** Native O-RAN protocols (e.g., SCTP-based F1-C and GTP-U) are not modified.  
> This dataset evaluates a deployable overlay approach for introducing quantum-safe security into existing RAN architectures.

---

## Cryptographic Coverage

### Classical
- X25519  
- prime256v1  

### Post-Quantum (Level-1)
- **KEM:** ML-KEM, HQC  
- **Signatures:** Falcon, ML-DSA, SPHINCS+  

### Hybrid
Representative classical + PQC combinations are included to support migration-path analysis toward quantum-safe telecom infrastructure.

Restricting experiments to **NIST Level-1** avoids unequal-strength comparisons and reflects practical deployment expectations.

---

## Experimental Environment
- **Platform:** OpenAirInterface O-RAN testbed (UCD NetsLab)  
- **Nodes:** O-CU ↔ O-DU  
- **Transport:** Dedicated CU–DU network  
- **TLS Stack:** PQC-enabled BoringSSL  
- **Protocol:** TLS 1.3  
- **Capture Tool:** tcpdump  


---

## Intended Audience
This repository is intended for researchers in:

- Post-Quantum Cryptography  
- O-RAN / 5G / 6G Security  
- Secure fronthaul design  
- Transport-layer cryptography  

---

## Citation
If you use this dataset, please cite the associated paper (forthcoming).

---

## Repository Structure
