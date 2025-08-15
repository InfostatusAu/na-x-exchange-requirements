# NA-X Cryptocurrency Exchange MVP Functional Requirements Document

**Version:** 1.0  
**Date:** August 14, 2025  
**Document Owner:** NA-X Technical Team  

## 1. Introduction and Scope

### 1.1 Purpose
This document defines the MVP (Minimum Viable Product) functional requirements for the NA-X cryptocurrency exchange platform, focusing exclusively on Priority 0 (P0) features required for initial Australian market launch. This document references the [Business Requirements Document](./01-Business-Requirements-Document.md) for business justification and the [Scope Document](./00-Scope-Document.md) for overall project context.

### 1.2 MVP Scope
The MVP covers core functionality required for:
- Australian market launch
- Basic exchange operations (registration, KYC, trading, wallet management)
- Essential compliance and security features
- Minimum back-office capabilities for operations

### 1.3 Out of MVP Scope
- US market features
- Advanced trading features and analytics
- Enhanced user experience features
- Advanced back-office and reporting tools

### 1.4 Traceability
Each functional requirement includes:
- **[BR-XXX]** reference to corresponding business requirement
- **Priority** level (only P0 included in MVP)
- **Acceptance Criteria** for validation

## 2. User Authentication and Authorization

### 2.1 User Registration
**FR-AUTH-001** [P0] [BR-001] System shall provide secure user registration with email verification  
*Acceptance Criteria:*
- Email validation with confirmation link
- Password strength requirements (min 12 chars, uppercase, lowercase, numbers, symbols)
- CAPTCHA integration to prevent automated registration
- Duplicate email detection and appropriate error messaging

**FR-AUTH-002** [P0] [BR-002] System shall collect required KYC information during registration  
*Acceptance Criteria:*
- Personal information collection (name, DOB, address, phone)
- Document upload interface for ID verification
- Integration with Sumsub via Shift Markets API
- Progress tracking for KYC completion status

**FR-AUTH-003** [P0] [BR-029,BR-040] System shall enforce Two-Factor Authentication (2FA)  
*Acceptance Criteria:*
- TOTP support via authenticator apps
- SMS backup option where available
- Recovery codes generation and secure storage
- Mandatory 2FA for sensitive operations (withdrawals, settings changes)

### 2.2 User Authentication
**FR-AUTH-004** [P0] [BR-001] System shall provide secure login functionality  
*Acceptance Criteria:*
- Email/password authentication
- Rate limiting for failed login attempts (5 attempts per 15 minutes)
- Account lockout protection with time-based unlock
- Session management with secure token generation

### 2.3 Session Management
**FR-AUTH-007** [P0] [BR-034] System shall implement secure session management  
*Acceptance Criteria:*
- JWT tokens with appropriate expiration (15 minutes access, 7 days refresh)
- Automatic token refresh for active sessions
- Secure token storage (httpOnly cookies for web)
- Session invalidation on logout and suspicious activity

## 3. User Profile and Account Management

### 3.1 Profile Management
**FR-PROFILE-001** [P0] [BR-003,BR-004] Users shall manage their profile information  
*Acceptance Criteria:*
- View and edit personal information (non-KYC critical fields)
- Update contact preferences and notification settings
- Change password with current password verification
- Manage 2FA devices (add, remove, backup codes)

**FR-PROFILE-002** [P0] [BR-002] Users shall view their KYC verification status  
*Acceptance Criteria:*
- Clear display of verification status (pending, approved, rejected, expired)
- Detailed information about required documents and next steps
- Re-submission capability for rejected documents
- Status update notifications

### 3.2 Security Settings
**FR-PROFILE-004** [P0] [BR-034] Users shall manage security settings  
*Acceptance Criteria:*
- Enable/disable 2FA methods
- View active sessions and location information
- Terminate specific sessions remotely
- Set up login notifications via email/SMS

## 4. Dashboard and Portfolio Management

### 4.1 Account Dashboard
**FR-DASH-001** [P0] [BR-010] System shall display comprehensive account overview  
*Acceptance Criteria:*
- Total portfolio value in AUD
- Individual asset balances with current market values
- 24-hour change indicators with percentage and absolute values
- Quick access to core functions (deposit, withdraw, trade)

**FR-DASH-002** [P0] [BR-004,BR-010] System shall display recent account activity  
*Acceptance Criteria:*
- Recent transactions (last 10) with type, amount, and status
- Open orders summary with quick cancel functionality
- Pending deposits/withdrawals with expected completion times
- Trade history with profit/loss calculations

### 4.2 Asset Management
**FR-DASH-004** [P0] [BR-016,BR-019] Users shall view detailed asset information  
*Acceptance Criteria:*
- Current balance and market value for each cryptocurrency
- Available vs. locked balances (orders, withdrawals)
- Historical balance changes with transaction details
- Asset-specific actions (deposit, withdraw, trade)

## 5. Fiat Operations (Australian Market)

### 5.1 AUD Deposits
**FR-FIAT-001** [P0] [BR-011] Users shall deposit AUD via NPP/PayID  
*Acceptance Criteria:*
- Display unique PayID for instant transfers
- Real-time deposit confirmation and balance updates
- Support for major Australian banks
- Transaction reference tracking for reconciliation

**FR-FIAT-002** [P0] [BR-012] Users shall deposit AUD via payment providers  
*Acceptance Criteria:*
- Integration with Stripe for card payments
- BCB Group integration for bank transfers
- Banxa integration for additional payment methods
- Clear fee disclosure before transaction initiation

### 5.2 AUD Withdrawals
**FR-FIAT-004** [P0] [BR-013] Users shall withdraw AUD to verified bank accounts  
*Acceptance Criteria:*
- Bank account verification via micro-deposits or instant verification
- Withdrawal amount validation against available balance
- 2FA requirement for withdrawal confirmation
- Withdrawal limits and velocity checks

**FR-FIAT-005** [P0] [BR-015,BR-025] System shall process withdrawal requests securely  
*Acceptance Criteria:*
- Anti-fraud checks and risk scoring
- Manual review triggers for large amounts
- Withdrawal confirmation emails with cancellation window
- Integration with payment providers for execution

## 6. Cryptocurrency Operations

### 6.1 Crypto Deposits
**FR-CRYPTO-001** [P0] [BR-017] System shall generate unique deposit addresses  
*Acceptance Criteria:*
- Unique address generation for each supported cryptocurrency
- QR code display for mobile wallet scanning
- Address validation and format checking
- Integration with Fireblocks via Shift Markets

**FR-CRYPTO-002** [P0] [BR-019] System shall track crypto deposit confirmations  
*Acceptance Criteria:*
- Real-time blockchain monitoring for incoming transactions
- Confirmation count display with required confirmations
- Balance updates after sufficient confirmations
- Transaction hash display for blockchain verification

### 6.2 Crypto Withdrawals
**FR-CRYPTO-004** [P0] [BR-018] Users shall withdraw cryptocurrencies to external addresses  
*Acceptance Criteria:*
- Address validation for target cryptocurrency type
- Amount validation against available balance and minimum limits
- 2FA requirement for withdrawal confirmation
- Withdrawal fee calculation and display

**FR-CRYPTO-005** [P0] [BR-018,BR-025] System shall implement withdrawal security controls  
*Acceptance Criteria:*
- Address whitelist functionality for enhanced security
- Daily and monthly withdrawal limits with KYC tier adjustments
- Velocity checks and suspicious activity detection
- Email confirmation with time-delayed execution option

### 6.3 Wallet Management
**FR-CRYPTO-007** [P0] [BR-016] System shall display wallet balances accurately  
*Acceptance Criteria:*
- Real-time balance updates from Fireblocks integration
- Separation of available vs. locked balances
- Historical balance tracking with transaction attribution
- Multi-currency portfolio view with total values

## 7. Trading Functionality

### 7.1 Market Data
**FR-TRADE-001** [P0] [BR-007] System shall display real-time market data  
*Acceptance Criteria:*
- Live price feeds via WebSocket connections
- Order book depth with bid/ask spreads
- Recent trade history with timestamps and volumes
- 24-hour statistics (high, low, volume, change)

**FR-TRADE-002** [P0] [BR-010] System shall provide interactive price charts  
*Acceptance Criteria:*
- Candlestick and line chart options
- Multiple timeframes (1m, 5m, 15m, 1h, 4h, 1d)
- Basic technical indicators (SMA, EMA, RSI, MACD)
- Chart drawing tools for analysis

### 7.2 Order Management
**FR-TRADE-004** [P0] [BR-006,BR-008] Users shall place market orders  
*Acceptance Criteria:*
- Instant execution at current market price
- Slippage protection with maximum deviation limits
- Balance validation before order submission
- Order confirmation with executed price display

**FR-TRADE-005** [P0] [BR-006,BR-008] Users shall place limit orders  
*Acceptance Criteria:*
- Price specification with precision matching exchange requirements
- Time-in-force options (GTC, IOC, FOK)
- Order book position indication
- Partial fill handling and notifications

**FR-TRADE-006** [P0] [BR-008,BR-025] Users shall place stop-loss orders  
*Acceptance Criteria:*
- Stop price configuration with trigger conditions
- Automatic conversion to market order when triggered
- Stop-loss order monitoring and status updates
- Risk management calculations and warnings

**FR-TRADE-007** [P0] [BR-006,BR-010] Users shall manage open orders  
*Acceptance Criteria:*
- View all open orders with current status
- Cancel individual or all orders functionality
- Modify order quantities and prices where supported
- Order expiration handling and notifications

### 7.3 Trade Execution and History
**FR-TRADE-008** [P0] [BR-006,BR-033] System shall execute trades efficiently  
*Acceptance Criteria:*
- Sub-second order matching and execution
- Real-time order status updates
- Trade confirmation notifications
- Balance updates immediately after execution

**FR-TRADE-009** [P0] [BR-047] Users shall access comprehensive trade history  
*Acceptance Criteria:*
- Complete trade log with dates, prices, and fees
- Filtering and search capabilities by date, asset, type
- Profit/loss calculations for closed positions
- Export functionality for tax reporting

## 8. Compliance and Risk Management

### 8.1 AML/CTF Compliance
**FR-COMP-001** [P0] [BR-029,BR-027] System shall implement transaction monitoring  
*Acceptance Criteria:*
- Automated screening against sanctions lists
- Velocity checks and unusual activity detection
- Risk scoring for transactions and users
- Suspicious activity reporting workflow

**FR-COMP-002** [P0] [BR-030] System shall maintain audit trails  
*Acceptance Criteria:*
- Complete transaction logging with immutable records
- User activity tracking including IP addresses and devices
- Document retention for 7 years minimum
- Secure log storage with integrity verification

**FR-COMP-003** [P0] [BR-028,BR-031] System shall support regulatory reporting  
*Acceptance Criteria:*
- Automated data collection for AUSTRAC reporting
- Transaction threshold monitoring and reporting
- Customer due diligence record maintenance
- Export capabilities for regulatory examinations

### 8.2 Risk Management
**FR-COMP-004** [P0] [BR-025] System shall implement user limits  
*Acceptance Criteria:*
- KYC tier-based transaction limits
- Daily, weekly, and monthly velocity limits
- Geographic restrictions and compliance checks
- Override mechanisms for manual approval

## 9. Integration Requirements

### 9.1 Shift Markets Integration
**FR-INT-001** [P0] [BR-031] System shall integrate with Shift Markets V4 GraphQL API  
*Acceptance Criteria:*
- Authentication and session management
- Real-time data synchronization
- Error handling and retry mechanisms
- Rate limiting compliance

**FR-INT-002** [P0] [BR-032] System shall integrate with Shift Markets WebSocket feeds  
*Acceptance Criteria:*
- Real-time market data subscription
- Order status updates
- Balance change notifications
- Connection resilience and reconnection logic

### 9.2 HubSpot CRM Integration
**FR-INT-004** [P0] [BR-003] System shall synchronize customer data with HubSpot  
*Acceptance Criteria:*
- Bidirectional data synchronization
- Customer lifecycle stage tracking
- Support ticket integration
- Marketing automation triggers

### 9.3 Fireblocks Integration
**FR-INT-005** [P0] [BR-016,BR-020] System shall integrate with Fireblocks for custody  
*Acceptance Criteria:*
- Secure API communication
- Transaction policy enforcement
- Multi-signature workflow support
- Real-time balance synchronization

## 10. Performance and Scalability

### 10.1 Performance Requirements
**FR-PERF-001** [P0] [BR-033] System shall meet response time requirements  
*Acceptance Criteria:*
- API responses under 100ms for read operations
- Trade execution under 500ms end-to-end
- Page load times under 2 seconds
- 99.9% uptime SLA

**FR-PERF-002** [P0] [BR-033] System shall handle concurrent user load  
*Acceptance Criteria:*
- Support 1,000 concurrent active users (MVP)
- Auto-scaling based on traffic patterns
- Graceful degradation under heavy load
- Load balancing across multiple instances

### 10.2 Data Management
**FR-PERF-003** [P0] [BR-032,BR-035] System shall ensure data consistency  
*Acceptance Criteria:*
- ACID compliance for financial transactions
- Real-time data synchronization across services
- Conflict resolution for concurrent updates
- Backup and recovery procedures

## 11. Security Requirements

### 11.1 Application Security
**FR-SEC-001** [P0] [BR-034] System shall implement comprehensive security controls  
*Acceptance Criteria:*
- HTTPS enforcement for all communications
- Content Security Policy (CSP) headers
- SQL injection and XSS protection
- Regular security vulnerability assessments

**FR-SEC-002** [P0] [BR-040,BR-032,BR-033,BR-034,BR-035] System shall protect sensitive data  
*Acceptance Criteria:*
- Encryption at rest for all sensitive data
- Encryption in transit for all communications
- Secure key management via AWS KMS
- PII minimization and anonymization where possible
- Australian data residency compliance
- GDPR and Privacy Act compliance controls

### 11.2 Access Control
**FR-SEC-003** [P0] [BR-034] System shall implement role-based access control  
*Acceptance Criteria:*
- User role definitions with permission matrices
- Administrative access controls with approval workflows
- API access controls with rate limiting
- Audit logging for all access attempts

## 12. Monitoring and Alerting

### 12.1 System Monitoring
**FR-MON-001** [P0] [BR-035] System shall provide comprehensive monitoring  
*Acceptance Criteria:*
- Real-time system health dashboards
- Performance metrics collection and analysis
- Error rate monitoring with threshold alerts
- Infrastructure monitoring via CloudWatch

**FR-MON-002** [P0] [BR-035] System shall implement alerting mechanisms  
*Acceptance Criteria:*
- Critical system alerts with immediate notification
- Business metric alerts for anomaly detection
- Escalation procedures for unresolved alerts
- Alert fatigue prevention with intelligent grouping

## 13. Testing and Quality Assurance

### 13.1 Testing Requirements
**FR-TEST-001** [P0] [BR-033,BR-035] System shall undergo comprehensive testing  
*Acceptance Criteria:*
- Unit test coverage minimum 80%
- Integration testing for all external services
- End-to-end testing for critical user flows
- Performance testing under expected load

**FR-TEST-002** [P0] [BR-034] System shall pass security testing  
*Acceptance Criteria:*
- Penetration testing by third-party security firm
- Vulnerability scanning and remediation
- Code security review by security specialists
- Compliance with OWASP Top 10 guidelines

### 13.2 User Acceptance Testing
**FR-TEST-003** [P0] [BR-004,BR-005] System shall complete user acceptance testing  
*Acceptance Criteria:*
- Beta testing with selected customers
- Usability testing for core user flows
- Accessibility testing for compliance
- Cross-browser and device compatibility testing

## 14. Non-Functional Requirements

### 14.1 Performance Requirements
- **Response Time:** All API calls must respond within 100ms for read operations, 500ms for write operations
- **Throughput:** System must support minimum 1,000 requests per second
- **Concurrent Users:** Support minimum 1,000 concurrent active users
- **Uptime:** Maintain 99.9% availability (8.77 hours downtime per year maximum)

### 14.2 Scalability Requirements
- **Horizontal Scaling:** System must auto-scale based on load with minimum 30-second response time
- **Database Performance:** Database queries must complete within 50ms for 95% of requests
- **Load Distribution:** Support geographic load distribution across Australian data centers

### 14.3 Security Requirements
- **Data Encryption:** All data encrypted at rest using AES-256, in transit using TLS 1.3
- **Authentication:** Multi-factor authentication mandatory for all sensitive operations
- **Session Security:** Session tokens expire within 15 minutes, refresh tokens within 7 days
- **Audit Logging:** All security events logged with tamper-proof integrity verification

### 14.4 Reliability Requirements
- **Data Backup:** Real-time data replication with 15-minute Recovery Point Objective (RPO)
- **Disaster Recovery:** 4-hour Recovery Time Objective (RTO) for critical systems
- **Error Handling:** Graceful degradation with user-friendly error messages
- **Transaction Integrity:** ACID compliance for all financial transactions

### 14.5 Compatibility Requirements
- **Browser Support:** Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Mobile Responsiveness:** Full functionality on devices with minimum 360px width
- **API Versioning:** Backward compatibility maintained for minimum 12 months
- **Third-party Integration:** Compatibility with Shift Markets API v4.0+

### 14.6 Compliance Requirements
- **Data Residency:** All Australian customer data must remain within Australia
- **Privacy:** Full GDPR and Australian Privacy Act compliance
- **Financial Regulations:** Compliance with AUSTRAC, ASIC, and Trend Capital Group requirements
- **Audit Trail:** Complete audit trail for all transactions with 7-year retention

## 15. Acceptance Criteria

### 15.1 MVP Success Criteria
- All P0 functional requirements implemented and tested
- Security penetration testing completed with no critical vulnerabilities
- Performance requirements met under load testing
- Integration testing completed with all external services
- User acceptance testing completed with 90% satisfaction rate

### 15.2 Go-Live Criteria
- Regulatory approval from relevant Australian authorities
- Trend Capital Group oversight capabilities fully operational
- Customer migration path from OTC platform validated
- Production monitoring and alerting systems fully operational
- Support processes and documentation completed

---

**Document Approval:**
- Product Owner: _________________
- Technical Lead: _________________
- Compliance Officer: _________________
- Security Officer: _________________

**Next Review Date:** August 28, 2025