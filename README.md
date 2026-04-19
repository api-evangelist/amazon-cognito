# Amazon Cognito (amazon-cognito)
Amazon Cognito is a fully managed user identity and authentication service that enables developers to add sign-up, sign-in, and access control to web and mobile applications. It supports OAuth 2.0, SAML 2.0, and OpenID Connect standards, providing secure user directories that scale to millions of users. Cognito offers user pools for authentication and identity pools for authorization, allowing integration with social identity providers and enterprise identity systems.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/amazon-cognito/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Authentication, AWS, Identity, OAuth, User Management

## Timestamps

- **Created:** 2016-04-18
- **Modified:** 2026-04-19

## APIs

### Cognito User Pools API
Amazon Cognito User Pools API provides user directory management, sign-up, sign-in, and token-based authentication for web and mobile applications. It supports multi-factor authentication, account recovery, and customizable authentication flows with 103 operations.

**Human URL:** [https://aws.amazon.com/cognito/](https://aws.amazon.com/cognito/)

#### Tags:

 - Authentication, AWS, Identity, User Management

#### Properties

- [Documentation](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html)
- [OpenAPI](openapi/amazon-cognito-user-pools-openapi.yml)
- [APIReference](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/Welcome.html)
- [Pricing](https://aws.amazon.com/cognito/pricing/)
- [GettingStarted](https://docs.aws.amazon.com/cognito/latest/developerguide/getting-started-with-cognito-user-pools.html)
- [FAQ](https://aws.amazon.com/cognito/faqs/)
- [JSONSchema](json-schema/user-pools-user-pool-type-schema.json)
- [JSONStructure](json-structure/user-pools-user-pool-type-structure.json)
- [JSON-LD](json-ld/amazon-cognito-user-pools-context.jsonld)

### Cognito Identity Pools API
Amazon Cognito Identity Pools (Federated Identities) API enables developers to create unique identities for users and federate them with identity providers. It provides temporary, limited-privilege AWS credentials to access AWS services with 23 operations.

**Human URL:** [https://aws.amazon.com/cognito/](https://aws.amazon.com/cognito/)

#### Tags:

 - Authentication, AWS, Federated Identity, Authorization

#### Properties

- [Documentation](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-identity.html)
- [OpenAPI](openapi/amazon-cognito-identity-pools-openapi.yml)
- [APIReference](https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html)
- [Pricing](https://aws.amazon.com/cognito/pricing/)
- [GettingStarted](https://docs.aws.amazon.com/cognito/latest/developerguide/getting-started-with-identity-pools.html)
- [FAQ](https://aws.amazon.com/cognito/faqs/)
- [JSONSchema](json-schema/identity-pools-identity-pool-schema.json)
- [JSONStructure](json-structure/identity-pools-identity-pool-structure.json)
- [JSON-LD](json-ld/amazon-cognito-identity-pools-context.jsonld)

## Common Properties

- [Portal](https://aws.amazon.com/)
- [Website](https://aws.amazon.com/cognito/)
- [Documentation](https://docs.aws.amazon.com/cognito/)
- [TermsOfService](https://aws.amazon.com/service-terms/)
- [PrivacyPolicy](https://aws.amazon.com/privacy/)
- [Support](https://aws.amazon.com/premiumsupport/)
- [Blog](https://aws.amazon.com/blogs/security/)
- [GitHubOrganization](https://github.com/aws)
- [Console](https://console.aws.amazon.com/cognito/)
- [SignUp](https://portal.aws.amazon.com/billing/signup)
- [Login](https://signin.aws.amazon.com/)
- [StatusPage](https://status.aws.amazon.com/)
- [YouTube](https://www.youtube.com/user/AmazonWebServices)
- [StackOverflow](https://stackoverflow.com/questions/tagged/amazon-cognito)
- [Contact](https://aws.amazon.com/contact-us/)

## Features

| Name | Description |
|------|-------------|
| User Pools | Fully managed user directories with sign-up, sign-in, and account management supporting millions of users. |
| Identity Pools (Federated Identities) | Grant temporary AWS credentials to authenticated users from social identity providers, SAML, or user pools. |
| Multi-Factor Authentication | Add SMS-based, TOTP, or email-based MFA to user pools for enhanced security. |
| OAuth 2.0 and OpenID Connect | Standards-compliant OAuth 2.0 authorization server with OIDC support for easy integration. |
| Social Identity Providers | Federate with Google, Facebook, Amazon, Apple, and any OIDC or SAML 2.0 compatible provider. |
| Advanced Security Features | Risk-based adaptive authentication, compromised credential detection, and IP-based restriction. |
| Customizable Authentication Flows | Lambda triggers for custom authentication challenges, migration, pre/post sign-up, and token customization. |
| User Groups | Organize users into groups with associated IAM roles for role-based access control. |

## Use Cases

| Name | Description |
|------|-------------|
| Web and Mobile App Authentication | Add user sign-up and sign-in to web and mobile applications without managing authentication infrastructure. |
| API Authorization | Protect APIs using Cognito-issued JWT tokens validated by API Gateway or application code. |
| Enterprise SSO | Federate with corporate SAML 2.0 identity providers for single sign-on in enterprise applications. |
| Social Login | Enable users to sign in with their Google, Facebook, or Apple credentials. |
| Serverless App Security | Secure serverless applications with temporary AWS credentials dispensed through identity pools. |
| Multi-Tenant SaaS | Create isolated user pools per tenant for multi-tenant SaaS applications. |

## Integrations

| Name | Description |
|------|-------------|
| AWS API Gateway | Authorize API requests using Cognito User Pool authorizers. |
| AWS Lambda | Customize authentication with Lambda triggers for sign-up, sign-in, and token generation. |
| AWS IAM | Map Cognito groups and roles to IAM permissions for granular access control. |
| AWS AppSync | Secure GraphQL APIs with Cognito User Pool authorization. |
| Amazon ALB | Offload authentication to Cognito from Application Load Balancers. |
| Google, Facebook, Apple | Social identity provider federation for consumer applications. |
| SAML 2.0 Providers | Enterprise identity provider federation via SAML for corporate SSO. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Cognito User Pools OpenAPI](openapi/amazon-cognito-user-pools-openapi.yml)
- [Cognito Identity Pools OpenAPI](openapi/amazon-cognito-identity-pools-openapi.yml)

### JSON Schema

531 schema files extracted from the OpenAPI specifications covering all request/response models for both User Pools and Identity Pools APIs.

### JSON Structure

531 JSON Structure files converted from JSON Schema using the json-structure.org specification.

### JSON-LD

- [Amazon Cognito User Pools Context](json-ld/amazon-cognito-user-pools-context.jsonld) — 269 types, 308 properties
- [Amazon Cognito Identity Pools Context](json-ld/amazon-cognito-identity-pools-context.jsonld) — 52 types, 55 properties

### Examples

531 example JSON files generated from JSON Schema definitions.

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Cognito User Pools API](capabilities/shared/cognito-user-pools.yaml) — 12 operations for user pool and user management
- [Cognito Identity Pools API](capabilities/shared/cognito-identity-pools.yaml) — 5 operations for federated identity management

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Amazon Cognito User Authentication](capabilities/user-authentication.yaml) | User Pools + Identity Pools | 12 | Application Developer, Platform Administrator |

## Vocabulary

- [Amazon Cognito Vocabulary](vocabulary/amazon-cognito-vocabulary.yaml) — Unified taxonomy mapping 7 resources, 8 actions, 1 workflow, and 2 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [Amazon Cognito Spectral Rules](rules/amazon-cognito-spectral-rules.yml) — 26 rules across 13 categories enforcing Amazon Cognito API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
