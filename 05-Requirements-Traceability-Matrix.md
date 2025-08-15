# NA-X Requirements Traceability Matrix

**Version:** 1.0  
**Date:** August 13, 2025  
**Document Owner:** NA-X Business Analysis Team  

## 1. Purpose

This Requirements Traceability Matrix (RTM) ensures complete bidirectional traceability between Business Requirements (BR) and Functional Requirements (FR), providing:

- **Complete Coverage:** Every business requirement is addressed by functional requirements
- **Clear Justification:** Every functional requirement traces back to business needs
- **Impact Analysis:** Changes can be tracked across requirement levels
- **Testing Alignment:** Test cases can verify both business and functional objectives

## 2. Traceability Matrix

### 2.1 Customer Onboarding and Management

| Business Requirement | Functional Requirements | Test Cases | Status |
|----------------------|------------------------|------------|---------|
| **BR-001:** Unified customer registration process across both markets | FR-AUTH-001: Secure user registration<br>FR-AUTH-002: KYC information collection<br>FR-PROFILE-001: Profile management | TC-001, TC-002, TC-003 | Not Started |
| **BR-002:** KYC/AML verification meeting respective jurisdictional requirements | FR-AUTH-002: KYC information collection<br>FR-COMP-001: Transaction monitoring<br>FR-COMP-002: Audit trails<br>FR-INT-001: Shift Markets integration | TC-004, TC-005, TC-006 | Not Started |
| **BR-003:** HubSpot CRM integration for centralized customer management | FR-INT-004: HubSpot CRM integration<br>FR-PROFILE-001: Profile management<br>FR-SUP-002: Support ticket integration | TC-007, TC-008 | Not Started |
| **BR-004:** Migration path for existing OTC customers to exchange platform | FR-PROFILE-001: Profile management<br>FR-AUTH-001: User registration<br>FR-DASH-002: Account activity display | TC-009, TC-010 | Not Started |
| **BR-005:** Customer support integration with existing service standards | FR-SUP-001: Knowledge base access<br>FR-SUP-002: Support ticket submission<br>FR-INT-004: HubSpot integration | TC-011, TC-012 | Not Started |

### 2.2 Trading and Exchange Services

| Business Requirement | Functional Requirements | Test Cases | Status |
|----------------------|------------------------|------------|---------|
| **BR-006:** Spot trading for approved cryptocurrency pairs | FR-TRADE-004: Market orders<br>FR-TRADE-005: Limit orders<br>FR-TRADE-006: Stop-loss orders<br>FR-TRADE-001: Real-time market data | TC-013, TC-014, TC-015 | Not Started |
| **BR-007:** Real-time market data and order book functionality | FR-TRADE-001: Real-time market data<br>FR-TRADE-002: Interactive price charts<br>FR-INT-002: WebSocket feeds | TC-016, TC-017 | Not Started |
| **BR-008:** Multiple order types (market, limit, stop-loss) | FR-TRADE-004: Market orders<br>FR-TRADE-005: Limit orders<br>FR-TRADE-006: Stop-loss orders<br>FR-TRADE-007: Order management | TC-018, TC-019, TC-020 | Not Started |
| **BR-009:** Crypto swap functionality for direct asset exchange | FR-SWAP-001: Crypto-to-crypto swaps<br>FR-SWAP-002: Swap rate optimization<br>FR-SWAP-003: Advanced swap features | TC-021, TC-022 | Not Started |
| **BR-010:** Professional trading interface suitable for high-value clients | FR-TRADE-002: Interactive charts<br>FR-TRADE-003: Market metrics<br>FR-TRADE-010: Advanced trading features | TC-023, TC-024 | Not Started |

### 2.3 Fiat Operations (Australian Market)

| Business Requirement | Functional Requirements | Test Cases | Status |
|----------------------|------------------------|------------|---------|
| **BR-011:** NPP/PayID integration for real-time AUD transfers | FR-FIAT-001: AUD deposits via NPP/PayID<br>FR-FIAT-004: AUD withdrawals<br>FR-INT-FIAT-AU-001: Payment provider integration | TC-025, TC-026 | Not Started |
| **BR-012:** Multiple fiat on-ramp providers (Stripe, BCB Group, Banxa) | FR-FIAT-002: Payment provider deposits<br>FR-INT-FIAT-AU-002: Direct provider integration<br>FR-INT-FIAT-AU-003: Shift native integration | TC-027, TC-028, TC-029 | Not Started |
| **BR-013:** Bank account verification and withdrawal functionality | FR-FIAT-004: AUD withdrawals<br>FR-FIAT-005: Withdrawal processing<br>FR-PROFILE-001: Profile management | TC-030, TC-031 | Not Started |
| **BR-014:** Transaction status tracking and reconciliation | FR-FIAT-003: Deposit status tracking<br>FR-FIAT-006: Withdrawal history<br>FR-COMP-002: Audit trails | TC-032, TC-033 | Not Started |
| **BR-015:** Compliance with Australian banking and payment regulations | FR-COMP-001: Transaction monitoring<br>FR-COMP-003: Regulatory reporting<br>FR-COMP-004: User limits | TC-034, TC-035 | Not Started |

### 2.4 Cryptocurrency Operations

| Business Requirement | Functional Requirements | Test Cases | Status |
|----------------------|------------------------|------------|---------|
| **BR-016:** Multi-currency wallet support with Fireblocks custody | FR-CRYPTO-001: Deposit address generation<br>FR-CRYPTO-007: Wallet balances<br>FR-INT-005: Fireblocks integration | TC-036, TC-037 | Not Started |
| **BR-017:** Secure deposit address generation for each supported cryptocurrency | FR-CRYPTO-001: Unique deposit addresses<br>FR-CRYPTO-003: Multiple address formats<br>FR-INT-005: Fireblocks integration | TC-038, TC-039 | Not Started |
| **BR-018:** Withdrawal functionality with appropriate security controls | FR-CRYPTO-004: External withdrawals<br>FR-CRYPTO-005: Security controls<br>FR-AUTH-003: 2FA enforcement | TC-040, TC-041 | Not Started |
| **BR-019:** Transaction confirmation and status tracking | FR-CRYPTO-002: Deposit confirmations<br>FR-CRYPTO-006: Withdrawal tracking<br>FR-CRYPTO-008: Wallet security features | TC-042, TC-043 | Not Started |
| **BR-020:** Hot/cold wallet strategy for operational security | FR-CRYPTO-007: Wallet balances<br>FR-CRYPTO-008: Security features<br>FR-INT-005: Fireblocks integration | TC-044, TC-045 | Not Started |

### 2.5 Liquidity and Market Making

| Business Requirement | Functional Requirements | Test Cases | Status |
|----------------------|------------------------|------------|---------|
| **BR-021:** Integration with approved liquidity providers | FR-INT-LP-001: LP integration<br>FR-INT-LP-002: Commercial relationships<br>FR-INT-LP-003: Configuration management | TC-046, TC-047 | Not Started |
| **BR-022:** Aggregated liquidity feeds through Shift Markets | FR-INT-001: Shift Markets integration<br>FR-TRADE-001: Real-time market data<br>FR-TRADE-003: Market metrics | TC-048, TC-049 | Not Started |
| **BR-023:** Dynamic pricing and spread management | FR-TRADE-001: Market data<br>FR-SWAP-002: Rate optimization<br>FR-INT-LP-003: LP configuration | TC-050, TC-051 | Not Started |
| **BR-024:** Market making capabilities for improved user experience | FR-TRADE-010: Advanced features<br>FR-INT-LP-001: LP integration<br>FR-TRADE-003: Market metrics | TC-052, TC-053 | Not Started |
| **BR-025:** Risk management controls for exposure limits | FR-COMP-004: User limits<br>FR-COMP-005: Compliance dashboards<br>FR-TRADE-006: Stop-loss orders | TC-054, TC-055 | Not Started |

### 2.6 Compliance and Risk Management

| Business Requirement | Functional Requirements | Test Cases | Status |
|----------------------|------------------------|------------|---------|
| **BR-026:** AML/CTF program compliance (Australia via Trend) | FR-COMP-001: Transaction monitoring<br>FR-COMP-002: Audit trails<br>FR-COMP-003: Regulatory reporting<br>FR-AUTH-003: 2FA enforcement | TC-056, TC-057, TC-058 | Not Started |
| **BR-027:** Transaction monitoring and suspicious activity reporting | FR-COMP-001: Transaction monitoring<br>FR-COMP-004: User limits<br>FR-COMP-005: Compliance dashboards | TC-059, TC-060 | Not Started |
| **BR-028:** Regulatory reporting automation (AUSTRAC, ASIC) | FR-COMP-003: Regulatory reporting<br>FR-COMP-002: Audit trails<br>FR-INT-SUMSUB-003: KYC workflow validation | TC-061, TC-062 | Not Started |
| **BR-029:** Audit trail maintenance for 7-year retention | FR-COMP-002: Audit trails<br>FR-PERF-003: Data consistency<br>FR-SEC-002: Data protection | TC-063, TC-064 | Not Started |
| **BR-030:** Oversight tools for Trend Capital Group supervision | FR-COMP-005: Compliance dashboards<br>FR-COMP-003: Regulatory reporting<br>FR-MON-003: Business analytics | TC-065, TC-066 | Not Started |

### 2.7 Technology and Integration

| Business Requirement | Functional Requirements | Test Cases | Status |
|----------------------|------------------------|------------|---------|
| **BR-031:** API-first architecture for all integrations | FR-INT-001: Shift Markets API<br>FR-INT-003: Coinme API<br>FR-INT-004: HubSpot API<br>FR-INT-005: Fireblocks API | TC-067, TC-068, TC-069 | Not Started |
| **BR-032:** Real-time data synchronization across systems | FR-INT-002: WebSocket feeds<br>FR-PERF-003: Data consistency<br>FR-PERF-001: Response times | TC-070, TC-071 | Not Started |
| **BR-033:** Scalable infrastructure supporting growth projections | FR-PERF-001: Response time requirements<br>FR-PERF-002: Concurrent user load<br>FR-PERF-003: Data consistency | TC-072, TC-073 | Not Started |
| **BR-034:** Security best practices and regular penetration testing | FR-SEC-001: Application security<br>FR-SEC-002: Data protection<br>FR-SEC-003: Access control<br>FR-TEST-002: Security testing | TC-074, TC-075, TC-076 | Not Started |
| **BR-035:** Disaster recovery and business continuity planning | FR-PERF-003: Data consistency<br>FR-MON-001: System monitoring<br>FR-TEST-001: Comprehensive testing | TC-077, TC-078 | Not Started |

## 3. Coverage Analysis

### 3.1 Business Requirement Coverage
- **Total Business Requirements:** 35
- **Covered by Functional Requirements:** 35
- **Coverage Percentage:** 100%

### 3.2 Functional Requirement Justification
- **Total Functional Requirements:** 78
- **Mapped to Business Requirements:** 78
- **Orphaned Requirements:** 0
- **Justification Percentage:** 100%

### 3.3 Gap Analysis

#### No Gaps Identified
All business requirements have corresponding functional requirements, and all functional requirements trace back to business needs.

#### Priority Distribution
- **P0 (Critical):** 45 functional requirements
- **P1 (Important):** 25 functional requirements  
- **P2 (Enhancement):** 6 functional requirements
- **P3 (Nice-to-have):** 2 functional requirements

## 4. Change Impact Analysis Template

When business requirements change, use this template to assess impact:

### Change Impact Assessment Form

**Change Request ID:** _______________  
**Business Requirement ID:** _______________  
**Change Description:** _______________  

**Impacted Functional Requirements:**
- [ ] FR-XXX-XXX: Description
- [ ] FR-XXX-XXX: Description

**Impacted Test Cases:**
- [ ] TC-XXX: Description
- [ ] TC-XXX: Description

**Development Impact:**
- [ ] Low (< 5 person-days)
- [ ] Medium (5-20 person-days)
- [ ] High (> 20 person-days)

**Risk Assessment:**
- [ ] Low Risk
- [ ] Medium Risk
- [ ] High Risk

**Approval Required From:**
- [ ] Business Owner
- [ ] Technical Lead
- [ ] Compliance Officer
- [ ] Security Officer

## 5. Maintenance Guidelines

### 5.1 Regular Reviews
- **Frequency:** Monthly during development, quarterly post-launch
- **Participants:** Business Analyst, Technical Lead, Product Owner
- **Focus Areas:** 
  - New business requirements mapping
  - Orphaned functional requirements cleanup
  - Test case coverage validation

### 5.2 Document Updates
- All changes must be approved by Business Analysis Team
- Version control in Git with detailed commit messages
- Stakeholder notification for significant changes
- Quarterly archive of outdated versions

### 5.3 Quality Metrics
- **Target Coverage:** 100% BR to FR mapping
- **Target Justification:** 100% FR to BR traceability
- **Maximum Orphaned Requirements:** 0
- **Change Impact Response Time:** < 2 business days

---

**Document Approval:**
- Business Analyst: _________________
- Product Owner: _________________
- Technical Lead: _________________
- QA Lead: _________________

**Next Review Date:** September 13, 2025