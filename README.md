# packman
A documentation and tracking project with the goal of making package management systems more secure.

## Table Of Package Management Systems

| Language | Name | Tier | Controls | Packman Lead | Packman Page | 
|----------|------|------|----------|--------------|--------------|
| Javascript | NPM | 1   |  |  | [NPM Page](./npm.md) |
| Ruby       | RubyGems | 1 | | | |
| Python     | PyPy     | 1 | |  | |
| Java       | Maven Central | 2 | | | 
| .Net       | NuGet      | ? | | |
| Dockerhub  | Docker     | 1 | | |

## Tiers and Controls

* Tier 1:  The lowest level of maturity.  Consider this untrusted.
* Tier 2:  Basic controls in place.
* Tier 3:  Very secure.

| Criteria # | Control | Tier 1 | Tier 2 | Tier 3 |
|------------|---------|--------|--------|--------|
| 1 | MFA to push artifacts | &#9744; | &#9745; | &#9745; |
| 2 | Strong authentication | &#9744; | &#9745; | &#9745; |
| 3 | Security contacts | &#9744; | &#9745; | &#9745; |
| 4 | Code signing | &#9744; | &#9744; | &#9745; |
| 5 | Code analysis (static) | &#9744; | &#9744; | &#9745; |

## Detail About Controls

### MFA To Push Artifacts

Since being able to push new code to a package manager is a powerful function, it is important to know that it cannot be easily done by guessing a maintainer's password.  Implementing MFA 

... 

## References to Related Projects

[Dependency Track](https://www.owasp.org/index.php/OWASP_Dependency_Track_Project)
[Dependency Check]()
