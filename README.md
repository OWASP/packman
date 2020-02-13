# packman

A documentation and tracking project with the goal of making package management systems more secure.  See [issues](./ISSUES.md) for a very rough list of a few of the related issues we have seen.

## Table Of Package Management Systems

| Language | Name | Tier | Controls | Packman Lead | Packman Page | 
|----------|------|------|----------|--------------|--------------|
| JavaScript | npm | 1   |  |  | [npm](./npm.md) |
| Ruby       | RubyGems | 1 | | | [rubygems](./rubygems.md)|
| Python     | PyPi     | 1 | |  | |
| Java       | Maven Central | 2 | | | [maven central](./mavencentral.md)|
| Java       | Android Central | ? | | | |
| .Net       | NuGet      | 2 | | |[nuget](./nuget.md)|
| Dockerhub  | Docker     | 1 | | |
| Golang     | go get     | 1 | | | [golang](./golang.md)|
| PHP        | Composer   | ? | | |
| Cocoa      | Cocoa Pods | ? | | |
| Swift      | Swift Package Manager | 1 | | | [swiftpm](./swiftpm.md)|
| Rust       | Cargo      | 2? | | | [rustcargo](./rustcargo.md)|

## Tiers and Controls

* Tier 1:  The lowest level of maturity.  Consider this untrusted.
* Tier 2:  Basic controls in place.
* Tier 3:  Very secure.

| Control | Tier 1 | Tier 2 | Tier 3 |
|---------|--------|--------|--------|
| Strong Authentication | &#9744; | &#9745; | &#9745; |
| MFA To Push Artifacts | &#9744; | &#9745; | &#9745; |
| Security Contacts | &#9744; | &#9745; | &#9745; |
| Packages Can Notify of Security Issues | &#9744; | &#9745; | &#9745; |
| Code package tied to source code | &#9744; | &#9745; | &#9745;|
| Prevents Credential from Being Published | &#9744; | &#9745; | &#9745; |
| Update notifications | &#9744; | &#9745; | &#9745;|
| Code signing | &#9744; | &#9744; | &#9745; |
| Integrity Verification | &#9744; | &#9744; | &#9745; |
| Code analysis (static) | &#9744; | &#9744; | &#9745; |
| Code Dependency Analysis | &#9744; | &#9744; | &#9745; |
| Package Manager Does Not Run Code | &#9744; | &#9744; | &#9745; |
| Package Manager Does Not Collect Info | &#9744; | &#9744; | &#9745; |
| Project Roles Guide | &#9744; | &#9744; | &#9745; |
| Project Roles Review | &#9744; | &#9744; | &#9745; |
| Account Level Library Tagging | &#9744; | &#9744; | &#9744; |

## Detail About Controls

The following sections describe each of the controls referenced in the above table in more detail.

### Strong Authentication

Strong authentication means that the system requires: 
- Complex passwords (> 10 chars with symbols,numbers,etc. or > 16 chars)
- Is resistant to brute forcing through lockouts
- Has password change notifications
- Supports only short sessions

### MFA To Push Artifacts

Since being able to push new code to a package manager is a powerful function, it is important to know that it cannot be easily done by guessing a maintainer's password.  Implementing MFA 

### Security Contacts and Process

To satisfy this requirement, the package manager must have a way to receive security information from the community and a process for handling such feedback.  A published email such as security@, together with a mechanism to ensure that the feedback is captured and responded to would satisfy this requirement.

### Packages Can Notify of Security Issues

Packages may themselves identify issues or be notified of issues.  The platform should support a way for a package maintainer to report a release with a security issue and: 
- Potentially remove it from the package source
- Flag for update

### Code Packages Tied to Source Code

Packages must somehow be tied to an explicit version of code (a tag?) in a well known public repository (bitbucket.org, github.com).

### Update Notifications

When packages are updated, all maintainers for that package should be notified.

### Consumer Check Status of a Package

When security issues are identified in a package, there should be a way for a consumer to check for those.  This could be a command that allows the consumer to check for known issues.

### Code Signing

It should be possible for developers to sign their code.  When they do, the package manager should verify the signatures and provide a way for those to be distributed to consumers of the package.

### Integrity verification

Package manager provides a method for verifying the integrity of the downloaded package.

None - no integrity verification is done
Partial - integrity verification is done using a weak method*
Yes - Verification is done using a sufficiently secure method
* we need want to define this.

### Code Analysis Static

The platform can provide static code analysis to proactively identify potential issues in important libraries.

### Code Dependency Analysis

The platform can track vulnerabilities in libraries the package depends on (upstream packages) and notify maintainers when that is the case.

### Package Manager Does Not Run Code

The package manager should not run code on package install.

### Package Manager Should Not Collect Information

The package manager should not collect information about the project using the dependency.  

### Project Roles Guide

The package management system should have a guide for roles on a project which should include a succession plan and terms for active engagement.

### Project Roles Review

The package management system maintainers should have a process for reviewing the roles on projects to ensure the maintainers are active.

### Account Level Library Tagging

Consumers of libraries should be able to tag their interest or approval in a specific library so that they can ensure that builds only use libraries they have tagged in certain ways.  Eg. marked as code reviewed.

### Prevents credential from being published

The package manager provides some control to prevent the authentication credentials / token / session from being leaked as part of the package contents.

None - no control is present and the user is to protect themselves
Partial - insert comment
Yes - credentials / tokens are either blocked from publication or are revoked through an automated way triggered by publication of a package. Users should be notified in some way that action has taken place.

## References to Related Projects

- [Dependency Track](https://www.owasp.org/index.php/OWASP_Dependency_Track_Project)
- [Dependency Check](https://www.owasp.org/index.php/OWASP_Dependency_Check)
- [PURL Spec](https://github.com/package-url/purl-spec)
