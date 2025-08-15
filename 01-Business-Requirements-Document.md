# NA-X Cryptocurrency Exchange Business Requirements Document

**Version:** 1.0  
**Date:** August 13, 2025  
**Document Owner:** NA-X Development Team  

## Executive Summary

NA-X seeks to expand its current personalized OTC cryptocurrency brokerage operations by launching a full-featured cryptocurrency exchange platform serving Australian and US markets. This expansion leverages strategic partnerships with Shift Markets (Australia) and Coinme (US) to provide white-label exchange infrastructure while maintaining NA-X's brand identity and customer relationships.

## 1. Business Context and Objectives

*This document provides business requirements that are detailed in the [Functional Requirements Document](./02-Functional-Requirements-Document.md) and scoped in the [Scope Document](./00-Scope-Document.md). For MVP delivery, refer to the [MVP Functional Requirements Document](./03-MVP-Functional-Requirements-Document.md).*

### 1.1 Current State
- **Business Model:** Personalized OTC cryptocurrency brokerage
- **Australian Operations:** Corporate Authorised Representative (CAR) under Trend Capital Group's AFSL
- **Customer Management:** Transitioning from Airtable to HubSpot CRM
- **Target Market:** High-value cryptocurrency transactions with personalized service

### 1.2 Strategic Objectives
- **Market Expansion:** Launch regulated exchange services in Australia and US
- **Scalability:** Move from manual OTC processes to automated exchange platform
- **Compliance:** Maintain regulatory compliance while expanding service offerings
- **Customer Experience:** Provide unified customer experience across markets

### 1.3 Success Criteria
- Successful launch of Australian exchange within 6 months
- Achievement of regulatory compliance in both jurisdictions
- Seamless customer migration from OTC to exchange services
- Integration of all planned third-party services and liquidity providers
- Positive customer feedback and adoption rates

## 2. Market Analysis and Strategy

### 2.1 Australian Market (Primary Focus)
- **Regulatory Framework:** Operate under Trend Capital Group's AFSL as CAR
- **Compliance Requirements:** AUSTRAC, ASIC regulations via Trend oversight
- **Competitive Advantage:** Personalized service with institutional-grade platform

### 2.2 US Market (Secondary Phase)
- **Compliance Strategy:** Leverage existing licenses and compliance infrastructure
- **Market Entry:** Focus on core buy/sell/custody functionality

## 3. Business Requirements by Functional Area

### 3.1 Customer Onboarding and Management
**BR-001:** Unified customer registration process across both markets  
**BR-002:** KYC/AML verification meeting respective jurisdictional requirements  
**BR-003:** HubSpot CRM integration for centralized customer management  
**BR-004:** Migration path for existing OTC customers to exchange platform  
**BR-005:** Customer support integration with existing service standards  

### 3.2 Trading and Exchange Services
**BR-006:** Spot trading for approved cryptocurrency pairs  
**BR-007:** Real-time market data and order book functionality  
**BR-008:** Multiple order types (market, limit, stop-loss)  
**BR-009:** Crypto swap functionality for direct asset exchange  
**BR-010:** Professional trading interface suitable for high-value clients  

### 3.3 Fiat Operations (Australian Market)
**BR-011:** Real-time AUD transfer capabilities  
**BR-012:** Multiple fiat payment provider support  
**BR-013:** Bank account verification and withdrawal functionality  
**BR-014:** Transaction status tracking and reconciliation  
**BR-015:** Compliance with Australian banking and payment regulations  

### 3.4 Cryptocurrency Operations
**BR-016:** Multi-currency wallet support with institutional custody  
**BR-017:** Secure deposit address generation for supported cryptocurrencies  
**BR-018:** Withdrawal functionality with appropriate security controls  
**BR-019:** Transaction confirmation and status tracking  
**BR-020:** Operational security controls for digital assets  

### 3.5 Liquidity and Market Making
**BR-021:** Integration with approved liquidity providers  
**BR-022:** Aggregated liquidity feeds from multiple sources  
**BR-023:** Dynamic pricing and spread management  
**BR-024:** Market making capabilities for improved user experience  

### 3.6 Risk Management
**BR-025:** Risk management controls for exposure limits  
**BR-027:** Transaction monitoring and suspicious activity reporting

## 4. Compliance Requirements

### 4.1 Australian Regulatory Framework
**BR-026:** Operate within Trend's AFSL authorisations; seek variations if needed  
**BR-028:** Support Trend's AUSTRAC reporting (SMR, TTR, IFTI)  
**BR-029:** Implement Trend-approved AML/CTF onboarding and monitoring procedures  
**BR-030:** Maintain records for 7 years minimum  
**BR-031:** Provide oversight tools and reporting to Trend  

### 4.2 Data Protection and Privacy
**BR-032:** Australian data residency requirements for customer information  
**BR-033:** Privacy Act compliance for personal information handling  
**BR-034:** GDPR compliance for European customers  
**BR-035:** Secure data handling and encryption standards  

### 4.3 Financial Services Compliance
**BR-036:** ASIC compliance for financial services provision  
**BR-037:** Consumer credit protection requirements  
**BR-038:** Financial services guide and disclosure requirements  
**BR-039:** Dispute resolution and complaints handling  

### 4.4 Platform Requirements
**BR-040:** Seamless integration capabilities with third-party services  
**BR-041:** Real-time data synchronization across business operations  
**BR-042:** Scalable platform supporting business growth projections  
**BR-043:** Enterprise-grade security and compliance standards  
**BR-044:** Business continuity and disaster recovery capabilities

## 5. Stakeholder Requirements

### 5.1 End Users (Customers)
**BR-045:** Users require intuitive and responsive trading interfaces  
**BR-046:** Users require fast and reliable trade execution  
**BR-047:** Users require transparent fee structures and real-time portfolio information  

### 5.2 NA-X Operations Team  
**BR-048:** Business requires comprehensive back-office management capabilities  
**BR-049:** Business requires integrated customer support workflow with HubSpot CRM  

### 5.3 Trend Capital Group (Licensee)
**BR-050:** Licensee requires complete oversight and supervision capabilities  
**BR-051:** Licensee requires automated regulatory reporting systems  

### 5.4 Regulatory Bodies
**BR-052:** Regulators require complete transaction transparency and audit capabilities

## 6. Constraints and Assumptions

### 6.1 Regulatory Constraints
- All Australian operations must remain within Trend Capital Group's AFSL scope
- US operations limited to Coinme's licensed capabilities
- Data residency requirements for Australian customer information
- Compliance with all applicable financial services regulations

### 6.2 Business Constraints
- Budget allocation for development, integration, and compliance costs
- Timeline constraints for market entry and competitive positioning
- Resource availability for development, testing, and operations
- Risk tolerance for new market entry and technology adoption

### 6.3 Key Business Assumptions
- Trend Capital Group's AFSL covers all planned service offerings
- Existing OTC customers will migrate to exchange platform
- Market conditions will support exchange launch timing
- Regulatory environment will remain stable during implementation period

## 7. Success Metrics and KPIs

### 7.1 Launch Metrics
- Time to market for Australian exchange launch
- Successful completion of all regulatory approvals
- Customer migration rate from OTC to exchange platform
- System uptime and performance metrics during launch

### 7.2 Operational Metrics
- Daily active users and trading volume
- Customer acquisition and retention rates
- Transaction processing efficiency
- Customer support response times and satisfaction scores

### 7.3 Financial Metrics
- Revenue growth from expanded service offerings
- Cost efficiency improvements from automation
- Customer lifetime value improvements
- Return on investment for platform investment

### 7.4 Compliance Metrics
- Regulatory reporting accuracy and timeliness
- AML/CTF compliance audit results
- Security incident frequency and severity
- Customer data protection compliance rates

## 8. Approval and Sign-off

This Business Requirements Document requires approval from:
- NA-X Executive Leadership
- Trend Capital Group (for Australian operations)
- Technology and Compliance Teams
- Legal and Regulatory Advisors

**Document Status:** Draft for Review  
**Next Review Date:** August 27, 2025  
**Approval Required By:** September 3, 2025  