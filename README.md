# Keycloak Demo Realm Export

This repository contains a ready-to-import Keycloak realm export for a demo identity and access management setup.

## Purpose

The main file in this repo is `realm-export.json`. It is an exported Keycloak realm configuration for a demo realm named `hiring-demo`.

It includes a working example of:
- realm-level roles and default role mapping
- OpenID Connect clients such as `account`, `account-console`, `admin-cli`, and `realm-management`
- default client scopes and protocol mappers
- browser login and reset credential flows
- MFA-related settings such as OTP / TOTP and WebAuthn-related configuration
- email event listeners and SMTP configuration
- demo SSO / federation-related client setup

## Why this demo exists

This repo is meant to help developers quickly understand how a realistic Keycloak realm is structured and how a demo environment can be bootstrapped without manually creating each setting by hand.

It is useful for:
- learning Keycloak realm configuration
- testing OIDC flows and role assumptions
- validating token scopes and client behavior
- demoing authentication and authorization concepts in a sandbox environment

## Demo summary

The exported realm models a small but realistic sample environment:
- users authenticate through the browser login flow
- standard OIDC clients and account console access are configured
- realm and client roles are defined
- MFA and password reset flows are enabled
- email notifications and events are configured for a test environment

## Importing the file

1. Start Keycloak.
2. Open the admin console.
3. Create a new realm or use an existing one.
4. Choose Import and select `realm-export.json`.
5. Review the imported settings, especially clients, SMTP, and any external identity provider settings.

## Important note

This is a sample/demo configuration and includes placeholder or example secrets and connection settings. Do not use it as-is in production without reviewing and rotating credentials, endpoints, and email configuration.

> Note: This repository and README were AI-generated for developer convenience.
