# Amazon Cognito (amazon-cognito)

Amazon Cognito is a fully managed AWS user identity and authentication service that adds sign-up, sign-in, and access control to web and mobile applications, scaling to millions of users. It provides User Pools for authentication (user directories, MFA, customizable auth flows) and Identity Pools for authorization (federated identities that dispense temporary AWS credentials), with support for OAuth 2.0, OpenID Connect, and SAML 2.0. The Cognito APIs are AWS regional service endpoints accessed over HTTPS using AWS Signature Version 4 (SigV4), typically via the AWS SDKs.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/amazon-cognito/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/amazon-cognito/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Authentication
- AWS
- Identity
- OAuth
- OIDC
- SAML
- User Management
- Federated Identity

## Timestamps

- **Created:** 2026-05-11
- **Modified:** 2026-05-19

## APIs

### Amazon Cognito User Pools API

The Amazon Cognito User Pools API provides user directory management, sign-up, sign-in, and token-based authentication for web and mobile applications. It supports multi-factor authentication, account recovery, and customizable authentication flows with operations covering user pools, users, groups, app clients, and resource servers. Authentication uses AWS Signature Version 4 (SigV4).

- **Human URL:** [https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/Welcome.html](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/Welcome.html)
- **Base URL:** `https://cognito-idp.us-east-1.amazonaws.com`

#### Tags

- Authentication
- Identity
- User Management
- MFA
- OAuth 2.0
- OIDC

#### Properties

- [Documentation](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html)
- [API Reference](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/Welcome.html)
- [OpenAPI](openapi/amazon-cognito-user-pools-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/amazon-cognito-user-pools.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/amazon-cognito-user-pools.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/user-pools-user-pool-type-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/user-pools-user-pool-type-structure.json)
- [JSON-LD](json-ld/amazon-cognito-user-pools-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Getting Started](https://docs.aws.amazon.com/cognito/latest/developerguide/getting-started-with-cognito-user-pools.html)

### Amazon Cognito Identity Pools API

The Amazon Cognito Identity Pools (Federated Identities) API enables developers to create unique identities for users and federate them with identity providers. It provides temporary, limited-privilege AWS credentials to access AWS services with operations covering identity pool management, credential dispensing, and provider configuration. Authentication uses AWS Signature Version 4 (SigV4).

- **Human URL:** [https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html](https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html)
- **Base URL:** `https://cognito-identity.us-east-1.amazonaws.com`

#### Tags

- Authentication
- Federated Identity
- Authorization
- SAML

#### Properties

- [Documentation](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-identity.html)
- [API Reference](https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html)
- [OpenAPI](openapi/amazon-cognito-identity-pools-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/amazon-cognito-identity-pools.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/amazon-cognito-identity-pools.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/identity-pools-identity-pool-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/identity-pools-identity-pool-structure.json)
- [JSON-LD](json-ld/amazon-cognito-identity-pools-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Getting Started](https://docs.aws.amazon.com/cognito/latest/developerguide/getting-started-with-identity-pools.html)

## Common Properties

- [Website](https://aws.amazon.com/cognito/)
- [Documentation](https://docs.aws.amazon.com/cognito/)
- [Pricing](https://aws.amazon.com/cognito/pricing/)
- [Sign Up](https://portal.aws.amazon.com/billing/signup)
- [Portal](https://aws.amazon.com/)
- [Console](https://console.aws.amazon.com/cognito/)
- [Login](https://signin.aws.amazon.com/)
- [Support](https://aws.amazon.com/premiumsupport/)
- [Status Page](https://status.aws.amazon.com/)
- [Blog](https://aws.amazon.com/blogs/security/)
- [F A Q](https://aws.amazon.com/cognito/faqs/)
- [Terms of Service](https://aws.amazon.com/service-terms/)
- [Privacy Policy](https://aws.amazon.com/privacy/)
- [GitHub Organization](https://github.com/aws)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/amazon-cognito)
- [Spectral Rules](rules/amazon-cognito-spectral-rules.yml)
- [Vocabulary](vocabulary/amazon-cognito-vocabulary.yaml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
