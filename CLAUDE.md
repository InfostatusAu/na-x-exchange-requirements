# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a project documentation repository for NA-X cryptocurrency exchange expansion planning. The repository contains strategic documents, technical specifications, and architectural designs for launching cryptocurrency exchange services in Australia (via Shift Markets platform) and potentially the US (via Coinme platform).

## Project Architecture Context

### Core Business Model
- **Current State**: NA-X operates as a personalized OTC cryptocurrency brokerage
- **Australian Operations**: Corporate Authorised Representative (CAR) under Trend Capital Group's AFSL
- **Planned Expansion**: Full Australian exchange via Shift Markets white-label platform + potential US market entry via Coinme CaaS

### Technology Stack (Proposed)
- **Frontend**: Amplify hosting with React/modern JS framework
- **API Gateway**: AWS API Gateway with WAF protection  
- **Backend**: ECS Fargate containers (modular monolith approach for MVP)
- **Database**: DynamoDB for operational state, S3 for audit trails (Aurora PostgreSQL considered for future)
- **Load Balancer**: Private ALB with VPC Link from API Gateway
- **Message Queues**: SQS for async processing, EventBridge for orchestration
- **Caching**: ElastiCache/MemoryDB for market data (optional for MVP)
- **Monitoring**: CloudWatch + X-Ray for observability

### Integration Points
- **Shift Markets**: V4 GraphQL API for Australian exchange backend
- **Fireblocks**: Cryptocurrency custody solution
- **HubSpot**: CRM integration (transitioning from Airtable)
- **Payment Providers**: Stripe, BCB Group, Banxa for AUD on/off-ramps (NPP/PayID priority)
- **Liquidity Providers**: Coinbase, Kraken, Binance, KuCoin, B2C2, etc.
- **KYC/AML**: Sumsub via Shift Markets integration

## Development Approach

### MVP Strategy
- Start with modular monolith in single ECS Fargate service
- Clear internal module boundaries for future microservice extraction
- API Gateway + Private ALB for production-ready security from day one
- DynamoDB + S3 for minimal operational overhead

### Service Decomposition Triggers
Break into microservices only when:
- Different scaling curves (e.g., webhook bursts need 2-3x capacity)
- Latency isolation required (external service flakiness affecting core flows)
- Availability blast radius concerns
- Independent team ownership needed

### First Services to Extract (when needed)
1. **Webhooks Gateway** - Payment/Shift event processing with signature verification
2. **HubSpot Sync Worker** - CRM synchronization with backoff/DLQ handling

## Compliance Requirements

### Australian Regulatory Framework
- Must operate within Trend Capital Group's AFSL authorizations
- Support AUSTRAC reporting (SMR, TTR, IFTI) via Trend
- Implement AML/CTF procedures under Trend's program
- Maintain 7-year record retention
- Provide oversight tools for Trend supervision

### Security Standards
- OWASP SSDLC practices
- All communications over HTTPS
- Content Security Policy (CSP) headers
- Regular penetration testing
- Secrets Manager + KMS for credential management
- Least-privilege IAM with role-based access

## Key Architectural Decisions

### API Gateway + Private ALB
- **Rationale**: Combines robust API management with private service isolation
- **Benefits**: Native auth/throttling, request transformation, WebSocket support, future microservice routing
- **Alternative Considered**: Public ALB (simpler but loses edge controls)

### DynamoDB over Aurora (MVP)
- **Rationale**: Integration state and audit trails fit key-value patterns better than relational
- **Benefits**: Serverless scaling, minimal ops, conditional writes for idempotency
- **Migration Path**: DynamoDB Streams → Aurora for future relational needs

### Modular Monolith First
- **Rationale**: Fastest MVP delivery while preserving clean service boundaries
- **Benefits**: Reduced deployment complexity, uniform scaling profile for orchestration workloads
- **Evolution**: Extract services based on actual scaling/reliability signals

## Development Standards

### API Integration
- All external APIs must include circuit breakers and timeout budgets
- Implement idempotency for external calls
- Emit domain events to SQS/EventBridge for future service consumption
- Use structured logging (JSON) to CloudWatch

### Testing Requirements
- Unit tests for components and functions
- Integration tests for API interactions  
- End-to-end tests for critical user flows (registration, deposit, trade, withdrawal)
- Security testing including penetration testing before launch

### Deployment Standards
- Blue/green deployments via CodeDeploy
- Health checks at ALB + synthetic canaries
- Multi-AZ task deployment
- Infrastructure as Code (Terraform recommended)

## Common Commands

Note: This repository currently contains only documentation. No build, test, or deployment commands are available yet. Development commands will be added once the codebase implementation begins.

## Documentation Structure

- **AWS Architecture chatgpt converstation.txt**: Detailed technical architecture discussion and recommendations
- **NA-X Australian Web Application Strategy Guide**: Comprehensive integration strategy with Shift Markets
- **NA-X Exchange Scoping Report**: Full project scope covering both Australian and US market expansion
- **Scope Document**: Focused Australian exchange requirements and deliverables

## Next Steps for Implementation

1. **API Validation**: Verify Shift Markets V4 GraphQL capabilities against functional requirements
2. **AFSL Assessment**: Confirm Trend Capital Group's license covers all planned services/tokens
3. **Infrastructure Setup**: Provision VPC, API Gateway, ECS, and observability stack
4. **MVP Development**: Build modular monolith with clear service boundaries
5. **Compliance Integration**: Implement KYC/AML workflows meeting Trend's standards