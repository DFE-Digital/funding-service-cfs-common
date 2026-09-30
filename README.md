# funding-service-cfs-common

Shared libraries, models, utilities, and cross-cutting components used across the Calculate Funding Service (CFS) platform.

## Overview

Calculate Funding Common provides reusable functionality that is consumed by multiple Calculate Funding services and applications. The repository promotes consistency, reduces duplication, and provides a central location for common domain models and infrastructure components.

Key areas include:

- Shared domain models
- Common interfaces and contracts
- Utility libraries
- Configuration helpers
- Logging components
- Exception handling
- API client abstractions
- Authentication and security helpers
- Serialization and validation utilities

## Purpose

This repository serves as a foundational dependency for CFS services including:

- Frontend applications
- API services
- Background processors
- Publishing services
- Data migration tools
- Calculation services

By maintaining common functionality in a single repository, services can share standards and behaviours while reducing maintenance overhead.

## Technology Stack

- .NET
- C#
- .NET Class Libraries
- NuGet Package Management
- GitHub Actions
- SonarQube

## Repository Structure

```text
CalculateFunding-Common/
│
├── CalculateFunding.Common/
├── CalculateFunding.Common.ApiClient/
├── CalculateFunding.Common.Models/
├── CalculateFunding.Common.Interfaces/
├── CalculateFunding.Common.Utility/
├── CalculateFunding.Common.Tests/
└── docs/
```

## Getting Started

### Prerequisites

- .NET SDK (see global.json)
- Visual Studio 2022 / VS Code / Rider

### Clone Repository

```bash
git clone https://github.com/DFE-Digital/funding-service-cfs-common.git
cd funding-service-cfs-common
```

### Restore Dependencies

```bash
dotnet restore
```

### Build

```bash
dotnet build
```

### Run Tests

```bash
dotnet test
```

## Consuming the Library

Projects should reference the relevant common packages via project references or published NuGet packages.

Example:

```xml
<ProjectReference Include="..\CalculateFunding.Common\CalculateFunding.Common.csproj" />
```

## Development Guidelines

When adding shared functionality:

- Ensure it is applicable across multiple services
- Avoid introducing service-specific business logic
- Maintain backward compatibility where possible
- Include unit tests
- Update documentation

## Testing

Run all tests:

```bash
dotnet test
```

Generate test results:

```bash
dotnet test --logger trx
```

## CI/CD

GitHub Actions pipelines perform:

1. Build
2. Unit Tests
3. Code Quality Analysis
4. Security Scanning
5. Package Publication


## Contributing

Before submitting a Pull Request:

- Ensure all tests pass
- Follow coding standards
- Include documentation updates
- Assess impact on dependent services

## Ownership

Department for Education (DfE)

Funding & Grants Service
``
