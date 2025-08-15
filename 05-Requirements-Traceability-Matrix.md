# NA-X Requirements Traceability Matrix

**Version:** 3.0  
**Date:** August 15, 2025  
**Document Owner:** NA-X Business Analysis Team  

## 1. Purpose

This Requirements Traceability Matrix (RTM) ensures complete bidirectional traceability between Business Requirements (BR) and Functional Requirements (FR), providing:

- **Complete Coverage:** Every business requirement is addressed by functional requirements
- **Clear Justification:** Every functional requirement traces back to business needs
- **Impact Analysis:** Changes can be tracked across requirement levels
- **Testing Alignment:** Test cases can verify both business and functional objectives

*This matrix reflects the consolidated BRD structure with no overlapping requirements.*

## 2. Enhanced Traceability Matrix

*This matrix provides complete lifecycle traceability linking Business Requirements to Functional Requirements, Constraints, Assumptions, Success Metrics, and Risk Items.*

### 2.1 Customer Onboarding and Management

| BR ID | Business Requirement | Functional Requirements | Constraints | Assumptions | Success Metrics | Risk Items | Priority | Status |
|-------|----------------------|------------------------|-------------|-------------|-----------------|------------|----------|---------|
| **BR-001** | Unified customer registration process across both markets | FR-AUTH-001, FR-AUTH-002, FR-PROFILE-001 | CST-001, CST-002 | ASM-001, ASM-002 | MET-002, MET-005 | RSK-001, RSK-002 | P0 | Not Started |
| **BR-002** | KYC/AML verification meeting respective jurisdictional requirements | FR-AUTH-002, FR-PROFILE-002, FR-COMP-001 | CST-001, CST-004 | ASM-001, ASM-004 | MET-002, MET-013, MET-014 | RSK-001, RSK-002, RSK-003 | P0 | Not Started |
| **BR-003** | HubSpot CRM integration for centralized customer management | FR-INT-004, FR-PROFILE-001 | CST-009, CST-010 | ASM-005, ASM-007 | MET-006, MET-008 | RSK-005, RSK-019 | P0 | Not Started |
| **BR-004** | Migration path for existing OTC customers to exchange platform | FR-PROFILE-001, FR-DASH-002 | CST-006, CST-007 | ASM-002 | MET-003, MET-006 | RSK-008 | P0 | Not Started |
| **BR-005** | Customer support integration with existing service standards | FR-PROFILE-006 | CST-007, CST-010 | ASM-005 | MET-008 | RSK-019 | P1 | Not Started |

### 2.2 Trading and Exchange Services

| BR ID | Business Requirement | Functional Requirements | Constraints | Assumptions | Success Metrics | Risk Items | Priority | Status |
|-------|----------------------|------------------------|-------------|-------------|-----------------|------------|----------|---------|
| **BR-006** | Spot trading for approved cryptocurrency pairs | FR-TRADE-004, FR-TRADE-005, FR-TRADE-007, FR-TRADE-008 | CST-001, CST-009 | ASM-001, ASM-005 | MET-005, MET-007 | RSK-001, RSK-004 | P0 | Not Started |
| **BR-007** | Real-time market data and order book functionality | FR-TRADE-001, FR-INT-002 | CST-009, CST-011 | ASM-005, ASM-008 | MET-007 | RSK-004, RSK-007 | P0 | Not Started |
| **BR-008** | Multiple order types (market, limit, stop-loss) | FR-TRADE-004, FR-TRADE-005, FR-TRADE-006 | CST-009 | ASM-005 | MET-007 | RSK-004 | P0 | Not Started |
| **BR-009** | Crypto swap functionality for direct asset exchange | FR-SWAP-001, FR-SWAP-002 | CST-009, CST-010 | ASM-005, ASM-007 | MET-005 | RSK-004, RSK-018 | P1 | Not Started |
| **BR-010** | Professional trading interface suitable for high-value clients | FR-TRADE-002, FR-TRADE-003, FR-DASH-001 | CST-011 | ASM-002, ASM-008 | MET-005, MET-006, MET-007 | RSK-006, RSK-008 | P0 | Not Started |

### 2.3 Fiat Operations (Australian Market)

| BR ID | Business Requirement | Functional Requirements | Constraints | Assumptions | Success Metrics | Risk Items | Priority | Status |
|-------|----------------------|------------------------|-------------|-------------|-----------------|------------|----------|---------|
| **BR-011** | Real-time AUD transfer capabilities | FR-FIAT-001 | CST-001, CST-010 | ASM-001, ASM-005 | MET-007, MET-009 | RSK-001, RSK-016 | P0 | Not Started |
| **BR-012** | Multiple fiat payment provider support | FR-FIAT-002 | CST-010 | ASM-005, ASM-007 | MET-009 | RSK-016 | P0 | Not Started |
| **BR-013** | Bank account verification and withdrawal functionality | FR-FIAT-004, FR-FIAT-005 | CST-001, CST-004 | ASM-001, ASM-006 | MET-007, MET-013 | RSK-001, RSK-016 | P0 | Not Started |
| **BR-014** | Transaction status tracking and reconciliation | FR-FIAT-003, FR-FIAT-006 | CST-011 | ASM-008 | MET-007 | RSK-006 | P1 | Not Started |
| **BR-015** | Compliance with Australian banking and payment regulations | FR-COMP-001, FR-COMP-003 | CST-001, CST-004 | ASM-001, ASM-004 | MET-013, MET-014 | RSK-001, RSK-002, RSK-003 | P0 | Not Started |

### 2.4 Cryptocurrency Operations

| Business Requirement | Functional Requirements | Priority | Status |
|----------------------|------------------------|----------|---------|
| **BR-016:** Multi-currency wallet with institutional custody | FR-CRYPTO-007: Wallet balances<br>FR-INT-005: Fireblocks integration | P0 | Not Started |
| **BR-017:** Secure deposit address generation for supported cryptocurrencies | FR-CRYPTO-001: Unique deposit addresses<br>FR-CRYPTO-003: Multiple address formats | P0 | Not Started |
| **BR-018:** Withdrawal functionality with appropriate security controls | FR-CRYPTO-004: Cryptocurrency withdrawals<br>FR-CRYPTO-005: Withdrawal security controls | P0 | Not Started |
| **BR-019:** Transaction confirmation and status tracking | FR-CRYPTO-002: Deposit confirmations<br>FR-CRYPTO-006: Withdrawal tracking | P0 | Not Started |
| **BR-020:** Operational security controls for digital assets | FR-CRYPTO-008: Wallet security features<br>FR-SEC-001: Security controls | P1 | Not Started |

### 2.5 Liquidity and Market Making

| Business Requirement | Functional Requirements | Priority | Status |
|----------------------|------------------------|----------|---------|
| **BR-021:** Integration with approved liquidity providers | FR-INT-001: Platform API integration<br>FR-TRADE-001: Real-time market data | P0 | Not Started |
| **BR-022:** Aggregated liquidity feeds from multiple sources | FR-INT-002: WebSocket feeds<br>FR-TRADE-001: Real-time market data | P0 | Not Started |
| **BR-023:** Dynamic pricing and spread management | FR-TRADE-003: Market metrics<br>FR-SWAP-002: Swap rate optimization | P1 | Not Started |
| **BR-024:** Market making capabilities for improved user experience | FR-TRADE-010: Advanced trading features | P1 | Not Started |

### 2.6 Risk Management

| Business Requirement | Functional Requirements | Priority | Status |
|----------------------|------------------------|----------|---------|
| **BR-025:** Risk management controls for exposure limits | FR-COMP-004: User limits<br>FR-CRYPTO-005: Withdrawal security controls | P0 | Not Started |
| **BR-027:** Transaction monitoring and suspicious activity reporting | FR-COMP-001: Transaction monitoring<br>FR-PROFILE-005: Security activity log | P0 | Not Started |

### 2.7 Compliance Requirements

#### 2.7.1 Australian Regulatory Framework

| Business Requirement | Functional Requirements | Priority | Status |
|----------------------|------------------------|----------|---------|
| **BR-026:** Operate within Trend's AFSL authorisations | FR-COMP-003: Regulatory reporting<br>FR-COMP-005: Compliance dashboards | P0 | Not Started |
| **BR-028:** Support Trend's AUSTRAC reporting (SMR, TTR, IFTI) | FR-COMP-003: Regulatory reporting<br>FR-COMP-002: Audit trails | P0 | Not Started |
| **BR-029:** Implement Trend-approved AML/CTF onboarding and monitoring procedures | FR-AUTH-003: Two-Factor Authentication<br>FR-COMP-001: Transaction monitoring | P0 | Not Started |
| **BR-030:** Maintain records for 7 years minimum | FR-COMP-002: Audit trails<br>FR-TRADE-009: Trade history<br>FR-PROFILE-005: Security activity log | P0 | Not Started |
| **BR-031:** Provide oversight tools and reporting to Trend | FR-COMP-003: Regulatory reporting<br>FR-COMP-005: Compliance dashboards<br>FR-MON-003: Business analytics | P0 | Not Started |

#### 2.7.2 Data Protection and Privacy

| Business Requirement | Functional Requirements | Priority | Status |
|----------------------|------------------------|----------|---------|
| **BR-032:** Australian data residency requirements for customer information | FR-SEC-002: Sensitive data protection | P0 | Not Started |
| **BR-033:** Privacy Act compliance for personal information handling | FR-SEC-002: Sensitive data protection<br>FR-SEC-003: Role-based access control | P0 | Not Started |
| **BR-034:** GDPR compliance for European customers | FR-SEC-002: Sensitive data protection<br>FR-PROFILE-001: Profile management | P0 | Not Started |
| **BR-035:** Secure data handling and encryption standards | FR-SEC-002: Sensitive data protection<br>FR-SEC-001: Security controls | P0 | Not Started |

#### 2.7.3 Financial Services Compliance

| Business Requirement | Functional Requirements | Priority | Status |
|----------------------|------------------------|----------|---------|
| **BR-036:** ASIC compliance for financial services provision | FR-COMP-003: Regulatory reporting | P0 | Not Started |
| **BR-037:** Consumer credit protection requirements | FR-COMP-003: Regulatory reporting<br>FR-COMP-004: User limits | P0 | Not Started |
| **BR-038:** Financial services guide and disclosure requirements | FR-PROFILE-006: Customer support and dispute resolution | P1 | Not Started |
| **BR-039:** Dispute resolution and complaints handling | FR-PROFILE-006: Customer support and dispute resolution | P1 | Not Started |

#### 2.7.4 Security and Business Continuity Requirements

| BR ID | Business Requirement | Functional Requirements | Constraints | Assumptions | Success Metrics | Risk Items | Priority | Status |
|-------|----------------------|------------------------|-------------|-------------|-----------------|------------|----------|---------|
| **BR-040** | Enterprise-grade security and compliance standards | FR-SEC-001, FR-SEC-002, FR-SEC-003, FR-AUTH-003 | CST-004, CST-011 | ASM-006 | MET-014, MET-015, MET-016 | RSK-013, RSK-014, RSK-015 | P0 | Not Started |
| **BR-041** | Business continuity and disaster recovery capabilities | FR-MON-001, FR-MON-002, FR-PERF-003, FR-TEST-001 | CST-011 | ASM-006, ASM-008 | MET-004, MET-015 | RSK-020 | P0 | Not Started |

### 2.8 Platform and Technical Requirements

| BR ID | Business Requirement | Functional Requirements | Constraints | Assumptions | Success Metrics | Risk Items | Priority | Status |
|-------|----------------------|------------------------|-------------|-------------|-----------------|------------|----------|---------|
| **BR-042** | Seamless integration capabilities with third-party services | FR-INT-001, FR-INT-003, FR-INT-004, FR-INT-005 | CST-009, CST-010 | ASM-005, ASM-007 | MET-012 | RSK-004, RSK-005, RSK-019 | P0 | Not Started |
| **BR-043** | Real-time data synchronization across business operations | FR-INT-002, FR-PERF-003 | CST-009, CST-011 | ASM-005, ASM-008 | MET-007 | RSK-004, RSK-006, RSK-007 | P0 | Not Started |
| **BR-044** | Scalable platform supporting business growth projections | FR-PERF-001, FR-PERF-002 | CST-011 | ASM-008 | MET-005, MET-007 | RSK-006 | P0 | Not Started |

### 2.9 Stakeholder Requirements

| Business Requirement | Functional Requirements | Priority | Status |
|----------------------|------------------------|----------|---------|
| **BR-045:** Users require intuitive and responsive trading interfaces | FR-DASH-001: Account overview<br>FR-TRADE-002: Interactive charts<br>FR-PROFILE-001: Profile management | P0 | Not Started |
| **BR-046:** Users require fast and reliable trade execution | FR-TRADE-008: Trade execution<br>FR-PERF-001: Response time requirements | P0 | Not Started |
| **BR-047:** Users require transparent fee structures and real-time portfolio information | FR-DASH-001: Account overview<br>FR-DASH-002: Account activity<br>FR-TRADE-009: Trade history | P0 | Not Started |
| **BR-048:** Business requires comprehensive back-office management capabilities | FR-COMP-005: Compliance dashboards<br>FR-MON-003: Business analytics | P1 | Not Started |
| **BR-049:** Business requires integrated customer support workflow with HubSpot CRM | FR-INT-004: HubSpot integration<br>FR-PROFILE-006: Customer support | P0 | Not Started |
| **BR-050:** Licensee requires complete oversight and supervision capabilities | FR-COMP-005: Compliance dashboards<br>FR-MON-001: System monitoring<br>FR-MON-003: Business analytics | P0 | Not Started |
| **BR-051:** Licensee requires automated regulatory reporting systems | FR-COMP-003: Regulatory reporting<br>FR-COMP-002: Audit trails | P0 | Not Started |
| **BR-052:** Regulators require complete transaction transparency and audit capabilities | FR-COMP-002: Audit trails<br>FR-COMP-003: Regulatory reporting<br>FR-TRADE-009: Trade history | P0 | Not Started |

## 3. Coverage Analysis

### 3.1 Business Requirements Coverage
- **Total BRs:** 52 (BR-001 to BR-052)
- **Covered by FRs:** 52 (100%)
- **Uncovered BRs:** 0

### 3.2 Priority Distribution
- **P0 (Critical for MVP):** 39 BRs (75%)
- **P1 (Important for full functionality):** 13 BRs (25%)

### 3.3 Functional Areas Coverage
- **Authentication & Authorization:** 7 BRs covered
- **Trading & Exchange:** 5 BRs covered
- **Fiat Operations:** 5 BRs covered
- **Cryptocurrency Operations:** 5 BRs covered
- **Compliance & Risk Management:** 20 BRs covered
- **Platform & Technical Requirements:** 3 BRs covered
- **Security & Business Continuity:** 2 BRs covered
- **Stakeholder Requirements:** 8 BRs covered

## 4. Gap Analysis

### 4.1 Missing Functional Requirements
*All business requirements are currently covered by functional requirements. No gaps identified.*

### 4.2 Orphaned Functional Requirements
*Analysis shows all functional requirements trace back to business requirements. No orphaned FRs identified.*

## 5. Testing Implications

### 5.1 Test Coverage Requirements
- **P0 Requirements:** Must have automated test coverage with 95%+ pass rate
- **P1 Requirements:** Must have test coverage with 90%+ pass rate
- **Compliance Requirements:** Must have 100% audit trail coverage

### 5.2 Test Prioritization
1. **Authentication & Security (BR-029, BR-043):** Critical path testing
2. **Trading Operations (BR-006 to BR-010):** Core functionality testing
3. **Compliance Reporting (BR-028, BR-031):** Regulatory compliance testing
4. **Data Protection (BR-032 to BR-035):** Privacy and security testing

## 6. Change Impact Analysis

### 6.1 High-Impact Changes
Changes to the following BRs would require extensive FR updates:
- **BR-042:** Platform integration capabilities
- **BR-040:** Security and compliance standards
- **BR-029:** AML/CTF procedures

### 6.2 Low-Impact Changes
Changes to the following BRs have isolated impact:
- **BR-038, BR-039:** Customer support features
- **BR-023, BR-024:** Market making capabilities

---

**Document Approval:**
- Business Analyst: _________________
- Technical Lead: _________________
- QA Manager: _________________
- Project Manager: _________________

**Next Review Date:** August 29, 2025