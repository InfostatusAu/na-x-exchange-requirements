# Scope Document: NA-X Crypto Exchange – Australia (Shift Markets)

**Version:** 1.0  
**Date:** August 14, 2025  
**Document Owner:** NA-X Development Team  

## 1. Introduction

### 1.1 Purpose
Define the functional, technical, and compliance requirements for NA-X's Australian cryptocurrency exchange using the Shift Markets platform.

### 1.2 Document Relationships
This scope document provides the foundation for:
- **[Business Requirements Document](./01-Business-Requirements-Document.md)** - Business justification and stakeholder needs
- **[Functional Requirements Document](./02-Functional-Requirements-Document.md)** - Detailed technical and functional specifications
- **[MVP Functional Requirements Document](./03-MVP-Functional-Requirements-Document.md)** - Priority 0 requirements for initial launch

### 1.3 Objectives
- Launch a compliant, secure, and scalable exchange under NA-X's CAR arrangement with Trend Capital Group (AFSL holder)
- Integrate with Shift Markets backend for trading, wallet, and liquidity functions
- Support Australian fiat on/off-ramps and crypto custody via Trend-managed accounts
- Deliver a custom NA-X-branded web application optimised for Australian compliance and UX

## 2. Project Scope

### 2.1 In Scope

#### 2.1.1 Web and Mobile Crypto Exchange App
- Shift Markets V4 GraphQL API integration for trading, wallet operations, and market data
- Custom NA-X front-end using modern JS framework (React)
- Responsive web design with mobile-first approach
- Progressive Web App (PWA) capabilities for mobile experience

#### 2.1.2 Customer Onboarding and Management
- Onboarding with KYC/AML via Shift/Sumsub under Trend's AML/CTF program
- User registration, verification, and profile management
- HubSpot CRM integration for customer lifecycle management
- Migration tools for existing OTC customers

#### 2.1.3 Trading Operations
- Spot trading for approved cryptocurrency pairs
- Real-time market data and order book functionality
- Multiple order types: market, limit, stop-loss
- Trading interface with professional-grade charting and analysis tools

#### 2.1.4 Wallet and Custody Services
- Fireblocks custody for deposits/withdrawals, hot/cold wallet management
- Multi-currency wallet support for approved cryptocurrencies
- Secure deposit address generation and withdrawal processing
- Transaction confirmation and status tracking

#### 2.1.5 Fiat Operations (AUD)
- Fiat integration with NPP/PayID-enabled providers (Stripe, BCB Group, Banxa)
- Bank account verification and management
- AUD deposit and withdrawal functionality
- Real-time payment processing and reconciliation

#### 2.1.6 Liquidity and Market Making
- Liquidity connectivity to Trend-managed LPs (Coinbase, Kraken, Binance, etc.)
- Aggregated liquidity feeds through Shift Markets
- Dynamic pricing and spread management
- Market making capabilities for improved user experience

#### 2.1.7 Compliance and Reporting
- Compliance reporting, monitoring, and oversight tools for Trend
- AML/CTF transaction monitoring and suspicious activity reporting
- Audit trail maintenance with 7-year retention
- Automated regulatory reporting (AUSTRAC, ASIC)

#### 2.1.8 Treasury and Reconciliation
- Treasury reconciliation across Shift, Fireblocks, and bank/payment data
- Real-time balance tracking and reporting
- Financial reporting and analytics
- Multi-party reconciliation workflows

### 2.2 Out of Scope

#### 2.2.1 US Operations
- US operations (Coinme integration) - deferred to Phase 2
- US regulatory compliance and licensing
- USD-specific payment integrations

#### 2.2.2 Advanced Trading Features
- Advanced derivatives trading (futures, options)
- Margin trading and lending services
- Staking and DeFi integration services
- Algorithmic trading and institutional APIs (Phase 2)

#### 2.2.3 Alternative Custody Solutions
- Custody solutions outside Fireblocks integration
- Self-custody wallet integrations
- Hardware wallet direct integrations

#### 2.2.4 Advanced Features
- Mobile native applications (iOS/Android)
- Advanced portfolio management tools
- Social trading features
- Gamification and rewards programs

## 3. Key Deliverables

### 3.1 Primary Deliverables
- **MVP Exchange Platform** with onboarding, fiat operations, spot trading, wallet management, and reporting
- **Back-office Configuration** for NA-X operations and Trend oversight capabilities
- **Compliance Framework** with operational and compliance procedure documentation
- **Infrastructure Deployment** with security and scalability best practices
- **Training and Handover** to NA-X and Trend operations teams

### 3.2 Documentation Deliverables
- Technical architecture documentation
- API integration specifications
- Security and compliance procedures
- User manuals and training materials
- Operational runbooks and incident response procedures

### 3.3 Testing and Quality Assurance
- Comprehensive testing suite (unit, integration, end-to-end)
- Security penetration testing and vulnerability assessments
- User acceptance testing with beta customer group
- Performance and load testing under expected traffic

## 4. Functional Requirements Summary

*Detailed functional requirements are specified in the [Functional Requirements Document](./02-Functional-Requirements-Document.md). MVP requirements are detailed in the [MVP Functional Requirements Document](./03-MVP-Functional-Requirements-Document.md).*

The platform will provide comprehensive cryptocurrency exchange functionality including user onboarding, trading operations, wallet management, fiat operations, and compliance capabilities as detailed in the respective requirements documents.

## 5. Technology Approach

### 5.1 Integration Strategy
- **Exchange Platform:** Shift Markets white-label platform integration
- **Custody Services:** Institutional-grade custody solution
- **Payment Processing:** Multiple Australian payment providers
- **CRM Integration:** HubSpot for customer relationship management

### 5.2 Platform Characteristics
- **Architecture:** Modern web-based platform with mobile responsiveness
- **Real-time Capabilities:** Live market data and transaction updates
- **Security:** Enterprise-grade security and compliance standards
- **Scalability:** Cloud-based infrastructure supporting business growth

## 6. Risk Assessment & Mitigation

### 6.1 High-Risk Items

| Risk | Impact | Probability | Mitigation Strategy |
|------|--------|-------------|-------------------|
| **Regulatory Compliance Gaps** | High | Medium | Early and continuous regulatory engagement, compliance-first development approach |
| **Platform Integration Failures** | High | Medium | Early endpoint validation, continuous vendor engagement, fallback planning |
| **Security Vulnerabilities** | High | Low | Code reviews, penetration testing, security audits, SSDLC adherence |
| **Trend Oversight Requirements Unmet** | High | Low | Continuous engagement, formalised operational agreement, regular reviews |

### 6.2 Medium-Risk Items

| Risk | Impact | Probability | Mitigation Strategy |
|------|--------|-------------|-------------------|
| **Market Entry Delays** | Medium | Medium | Phased delivery approach, MVP focus, parallel workstreams |
| **Customer Migration Challenges** | Medium | Medium | Phased rollout with limited initial customer base, migration incentives |
| **Payment Integration Delays** | Medium | Low | Prioritise proven payment providers with platform compatibility |
| **Data Inconsistencies** | Medium | Low | Automated reconciliation, robust error handling, real-time monitoring |

### 6.3 Risk Monitoring
- Monthly risk assessment reviews with stakeholders
- Escalation procedures for high-impact risks
- Contingency planning for critical path dependencies
- Regular risk register updates throughout project lifecycle

## 7. Assumptions

### 7.1 Technology Assumptions
- Platform providers will provide complete documentation and support throughout development
- Custody solutions will meet regulatory security requirements  
- Third-party integrations will be technically feasible and stable
- Platform capacity will support expected user load and growth
- API rate limits and availability will support business requirements

### 7.2 Business Assumptions
- Trend will manage AUSTRAC/ASIC filings and regulatory relationships
- Fiat and liquidity provider accounts are Trend-held; NA-X operates under delegated authority
- Existing OTC customers will migrate to exchange platform
- Market conditions will support exchange launch timing
- Budget allocation will be sufficient for development and integration costs

### 7.3 Regulatory Assumptions
- Regulatory environment will remain stable during development period
- Trend's AFSL covers all planned service offerings and tokens
- Australian data residency requirements will not change significantly
- Current compliance frameworks will remain applicable
- Third-party providers maintain necessary licenses and approvals

## 8. Constraints

### 8.1 Regulatory Constraints
- All exchange operations must comply with Trend Capital Group's AFSL scope and oversight requirements
- Integration must be limited to payment providers and liquidity partners approved and contracted via Trend
- Data storage must comply with Australian data residency requirements
- Customer onboarding must follow Trend's approved AML/CTF procedures

### 8.2 Platform Constraints
- Development must align with chosen platform capabilities and release schedule
- Security and operational processes must pass Trend's internal audit before launch
- Performance requirements must support expected user load and trading volumes
- Platform architecture must support future market expansion

### 8.3 Business Constraints
- Budget allocation for development, integration, and compliance costs
- Timeline constraints for competitive market entry
- Resource availability for development, testing, and operations
- Dependency on third-party service provider availability and support

## 9. Acceptance Criteria

### 9.1 Functional Acceptance
- All in-scope functionality is developed, tested, and deployed in a secure and stable environment
- Trading operations meet agreed performance and reliability thresholds
- Fiat and crypto transaction flows are fully functional, reconciled, and auditable
- User interface provides intuitive and responsive experience across all supported devices

### 9.2 Compliance Acceptance
- The KYC/AML process meets Trend's compliance standards and passes UAT with Trend stakeholders
- All regulatory reporting capabilities are functional and tested
- Security assessments completed with no critical vulnerabilities
- Data protection and privacy controls meet Australian regulatory requirements

### 9.3 Operational Acceptance
- Back-office tools provide Trend with the required oversight, reporting, and audit capabilities
- Monitoring and alerting systems are fully operational with appropriate response procedures
- Customer support tools and processes are integrated and functional
- Financial reconciliation processes are automated and auditable

### 9.4 Quality Acceptance
- All deliverables are approved by NA-X and Trend as meeting the agreed scope and quality standards
- Performance testing demonstrates system can handle expected load
- User acceptance testing completed with satisfactory customer feedback
- Documentation and training materials are complete and approved

## 10. Project Success Criteria

### 10.1 Delivery Success Criteria
- Successful launch within agreed timeline (6 months from project start)
- Zero critical security vulnerabilities at launch
- All functional acceptance criteria met and validated
- Complete documentation and training materials delivered

### 10.2 Technical Success Criteria  
- System uptime >99.9% during first month of operation
- API response times within specified thresholds
- Zero data loss or corruption incidents
- 100% reconciliation accuracy across all financial systems

*Business success metrics including customer adoption, financial performance, and operational KPIs are detailed in the [Business Requirements Document](./01-Business-Requirements-Document.md).*

---

**Document Approval:**
- Project Sponsor: _________________
- Technical Lead: _________________
- Compliance Officer: _________________
- Trend Capital Group Representative: _________________

**Next Review Date:** August 28, 2025
**Approval Required By:** September 5, 2025