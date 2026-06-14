# Amazon Cognito GraphQL Schema

## Overview

This GraphQL schema provides a conceptual representation of the Amazon Cognito API surface, covering both User Pools and Identity Pools. It is designed as a reference schema that maps Cognito's REST/SDK operations into typed GraphQL queries, mutations, and subscriptions.

Amazon Cognito is a fully managed AWS identity service that supports:

- **User Pools** — managed user directories with sign-up, sign-in, MFA, customizable auth flows, OAuth 2.0, OIDC, and SAML federation
- **Identity Pools** — federated identity broker that dispenses temporary AWS credentials
- **Amplify** — AWS Amplify wraps Cognito with a higher-level GraphQL-friendly API and AppSync integration

## Schema Source

- Derived from: [Amazon Cognito Developer Guide](https://docs.aws.amazon.com/cognito/latest/developerguide/)
- User Pools API Reference: [https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/Welcome.html](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/Welcome.html)
- Identity Pools API Reference: [https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html](https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html)

## Schema File

[amazon-cognito-schema.graphql](amazon-cognito-schema.graphql)

## Type Summary

The schema defines 65+ named types organized across the following domains:

### User Pool Types
| Type | Description |
|------|-------------|
| `UserPool` | Top-level user pool resource |
| `UserPoolConfig` | Schema, alias, and username configuration |
| `UserPoolDomain` | Hosted UI domain configuration |
| `UserPoolEmail` | Email sending configuration (SES) |
| `UserPoolSMS` | SMS sending configuration (SNS) |
| `UserPoolMFA` | MFA settings (SMS, TOTP) |
| `UserPoolPasswordPolicy` | Password complexity rules |
| `SoftwareTokenMFAConfig` | TOTP MFA settings |
| `SmsMFAConfig` | SMS MFA settings |
| `SmsConfiguration` | SNS caller ARN for SMS |

### User Pool Client Types
| Type | Description |
|------|-------------|
| `UserPoolClient` | App client resource |
| `UserPoolClientConfig` | OAuth flows, auth flows, callback URLs |
| `UserPoolClientTokenValidity` | Token expiry settings |
| `TokenValidityUnits` | Units for token validity durations |
| `OAuthFlow` | OAuth 2.0 flow configuration |
| `AnalyticsMetadata` | Pinpoint analytics integration |

### Authentication & Token Types
| Type | Description |
|------|-------------|
| `SignInResult` | Result of a sign-in attempt |
| `AuthResult` | Authentication result including tokens and challenge |
| `Tokens` | Access, ID, and refresh token bundle |
| `AccessToken` | JWT access token |
| `IdToken` | JWT identity token |
| `RefreshToken` | Opaque refresh token |
| `ChallengeResponse` | Generic challenge response |
| `NewPasswordChallenge` | NEW_PASSWORD_REQUIRED challenge |
| `MFAChallenge` | SMS or TOTP MFA challenge |
| `CustomChallenge` | Lambda-backed custom challenge |
| `TOTPSetup` | Associate software token flow |
| `TOTPCode` | Verify TOTP code result |
| `TokenRevocation` | Token revocation record |
| `SignInNextStep` | Next step in multi-step sign-in |
| `CodeDeliveryDetails` | Channel and destination for verification codes |
| `NewDeviceMetadata` | Device key/group for device tracking |
| `SignUpResult` | Result of user sign-up |

### User Types
| Type | Description |
|------|-------------|
| `CognitoUser` | Regular user (self-service context) |
| `AdminUser` | User with admin-API context |
| `UserAttribute` | Name/value attribute pair |
| `UserStatus` | User account status (enum) |
| `UserDevices` | Remembered devices for a user |
| `AdminGroup` | Group with admin context |

### Group Types
| Type | Description |
|------|-------------|
| `Group` | Cognito user group |
| `GroupMembership` | User-to-group association |

### Schema & Constraints
| Type | Description |
|------|-------------|
| `SchemaAttribute` | User pool custom/built-in attribute definition |
| `NumberAttributeConstraints` | Min/max for number attributes |
| `StringAttributeConstraints` | Min/max length for string attributes |
| `VerificationMessageTemplate` | Email/SMS verification message templates |
| `MessageTemplate` | Invite message template |
| `DeviceConfiguration` | Device tracking settings |
| `AdminCreateUserConfig` | Admin-only user creation settings |
| `UsernameConfiguration` | Case sensitivity for usernames |

### Lambda Trigger Types
| Type | Description |
|------|-------------|
| `LambdaTriggers` | All Lambda trigger ARNs for a user pool |
| `PreSignUpTrigger` | Pre sign-up Lambda trigger |
| `PostConfirmation` | Post confirmation Lambda trigger |
| `PreAuth` | Pre authentication Lambda trigger |
| `PostAuth` | Post authentication Lambda trigger |
| `TokenGeneration` | Pre token generation Lambda trigger |
| `UserMigration` | User migration Lambda trigger |
| `CustomMessage` | Custom message Lambda trigger |
| `VerifyAuthChallenge` | Verify auth challenge response trigger |
| `CreateAuthChallenge` | Create auth challenge trigger |
| `DefineAuthChallenge` | Define auth challenge trigger |

### Identity Pool Types
| Type | Description |
|------|-------------|
| `IdentityPool` | Federated identity pool |
| `FederatedIdentity` | Individual federated identity record |
| `SocialIdentity` | Social provider identity link |
| `CognitoIdentityProviderRef` | Cognito user pool as identity provider |

### Identity Provider Types
| Type | Description |
|------|-------------|
| `IdentityProvider` | Generic external identity provider |
| `SAMLProvider` | SAML 2.0 identity provider |
| `OIDCProvider` | OIDC identity provider |

### Resource Server & Scopes
| Type | Description |
|------|-------------|
| `ResourceServer` | OAuth 2.0 resource server |
| `Scope` | Custom scope on a resource server |

### Risk Configuration Types
| Type | Description |
|------|-------------|
| `RiskConfiguration` | Adaptive authentication configuration |
| `AccountTakeoverRiskConfig` | Account takeover detection settings |
| `AccountTakeoverActions` | Actions per risk level |
| `AccountTakeoverActionType` | Individual risk level action |
| `CompromisedCredentialRiskConfig` | Compromised credentials detection |
| `CompromisedCredentialActions` | Actions for compromised credentials |
| `NotifyEmail` | Risk notification email configuration |
| `NotifyEmailTemplate` | Email template for risk notifications |
| `RiskExceptionConfig` | IP allow/block lists for risk engine |

### Analytics Types
| Type | Description |
|------|-------------|
| `UserPoolAnalytics` | Aggregate usage metrics for a user pool |
| `DailyActiveUsers` | DAU with date and change percent |
| `SignInTypes` | Breakdown of sign-in method usage |

### Utility Types
| Type | Description |
|------|-------------|
| `APIKey` | AppSync / Amplify API key |
| `CustomDomainConfig` | ACM certificate for custom domain |

### Connection (Pagination) Types
`UserPoolConnection`, `UserPoolClientConnection`, `UserConnection`, `GroupConnection`, `IdentityProviderConnection`, `ResourceServerConnection`, `IdentityPoolConnection`, `FederatedIdentityConnection`

### Input Types
`UserAttributeInput`, `MFASettingsInput`, `ScopeInput`, `CustomDomainConfigInput`, `UserPoolClientConfigInput`, `TokenValidityUnitsInput`, `UserPoolPasswordPolicyInput`, `CompromisedCredentialConfigInput`, `AccountTakeoverConfigInput`, `NotifyEmailInput`

### Enumerations
`UserStatusType`, `MFAOptionType`, `OAuthFlowType`, `TokenValidityUnitsType`, `ExplicitAuthFlowsType`, `ChallengeNameType`, `VerifiedAttributeType`, `AliasAttributeType`, `UsernameAttributeType`, `IdentityProviderTypeType`, `RiskDecisionType`, `RiskLevelType`, `EventType`, `AccountTakeoverEventActionType`

### Scalars
`AWSDateTime`, `AWSJSON`, `AWSEmail`, `AWSPhone`

## Operations

### Queries
- User Pool management: `getUserPool`, `listUserPools`, `getUserPoolConfig`, `getUserPoolDomain`, `getUserPoolAnalytics`
- User Pool Client management: `getUserPoolClient`, `listUserPoolClients`
- User management: `getUser`, `listUsers`, `listUsersInGroup`, `adminGetUser`
- Group management: `getGroup`, `listGroups`, `listGroupsForUser`
- Identity Provider management: `getIdentityProvider`, `listIdentityProviders`, `getSAMLProvider`, `getOIDCProvider`
- Resource Server management: `getResourceServer`, `listResourceServers`
- Risk configuration: `getRiskConfiguration`
- Identity Pool management: `getIdentityPool`, `listIdentityPools`, `describeIdentity`, `listIdentities`

### Mutations
- User Pool lifecycle: `createUserPool`, `updateUserPool`, `deleteUserPool`, domain management
- App client lifecycle: `createUserPoolClient`, `updateUserPoolClient`, `deleteUserPoolClient`
- Admin user operations: `adminCreateUser`, `adminUpdateUserAttributes`, `adminDeleteUser`, `adminEnableUser`, `adminDisableUser`, `adminResetUserPassword`, `adminSetUserPassword`, `adminSetUserMFAPreference`, `adminConfirmSignUp`
- Group management: `createGroup`, `updateGroup`, `deleteGroup`, `adminAddUserToGroup`, `adminRemoveUserFromGroup`
- Authentication flows: `signUp`, `confirmSignUp`, `resendConfirmationCode`, `signIn`, `respondToAuthChallenge`, `signOut`, `revokeToken`, `forgotPassword`, `confirmForgotPassword`, `changePassword`
- MFA setup: `associateSoftwareToken`, `verifySoftwareToken`, `setUserMFAPreference`
- Identity provider management: `createIdentityProvider`, `updateIdentityProvider`, `deleteIdentityProvider`
- Resource server management: `createResourceServer`, `updateResourceServer`, `deleteResourceServer`
- Risk configuration: `setRiskConfiguration`
- Identity Pool lifecycle: `createIdentityPool`, `updateIdentityPool`, `deleteIdentityPool`

### Subscriptions
- `onUserCreated`, `onUserDeleted`, `onUserStatusChanged` — user lifecycle events
- `onSignIn`, `onSignUp` — authentication events
- `onRiskEvent` — adaptive authentication events

## Relationship to Amplify and AppSync

AWS Amplify uses Amazon Cognito as its default authentication provider. When using AWS AppSync (AWS's managed GraphQL service), Cognito User Pools are a first-class authorization mode. The `@auth` directive in Amplify GraphQL transforms maps directly to Cognito User Pool groups and identity claims, enabling fine-grained row-level security on AppSync resolvers.

The scalars `AWSDateTime`, `AWSJSON`, `AWSEmail`, and `AWSPhone` match the built-in scalars provided by AWS AppSync.
