# Security Policy

## Supported Versions

We actively support the following versions of Moorph GUI Clean:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | ✅ Fully supported |
| Previous| ⚠️ Security fixes only |
| Older   | ❌ Not supported   |

## Security Considerations

### Client-Side Security
Since Moorph GUI Clean is a **browser-based application** with no backend services, security considerations are focused on:

* **API Key Protection**: OpenAI API keys are stored locally in browser storage
* **Input Validation**: All user inputs are sanitized and validated
* **XSS Prevention**: Content Security Policy (CSP) headers and proper input handling
* **Dependency Security**: Regular updates to npm packages and security audits

### What We Do NOT Store
This "clean" version intentionally avoids:
* User authentication or personal data
* Server-side data persistence
* Cloud service integration
* Third-party tracking or analytics

## Reporting Security Vulnerabilities

### How to Report
If you discover a security vulnerability, please report it responsibly:

1. **DO NOT** create a public GitHub issue
2. **DO NOT** discuss the vulnerability publicly until it's resolved
3. **DO** contact us privately using one of these methods:

**Preferred Method**: Create a private security advisory
* Go to the [Security tab](https://github.com/VibeCAD/gui-clean/security) in our GitHub repository
* Click "Report a vulnerability"
* Provide detailed information about the issue

**Alternative Method**: Email (if available)
* Send details to the project maintainers
* Include "SECURITY" in the subject line
* Use PGP encryption if possible

### What to Include
When reporting a security vulnerability, please include:

* **Description**: Clear description of the vulnerability
* **Steps to Reproduce**: Detailed steps to reproduce the issue
* **Impact**: Potential security impact and affected components
* **Suggested Fix**: If you have ideas for fixing the issue
* **Environment**: Browser, OS, and version information
* **Evidence**: Screenshots, code snippets, or proof of concept (if safe)

### Response Timeline
We aim to respond to security reports within:
* **24 hours**: Initial acknowledgment
* **72 hours**: Preliminary assessment
* **1 week**: Detailed analysis and fix timeline
* **2 weeks**: Security patch release (for critical issues)

## Security Best Practices

### For Users
* **API Key Security**: Never share your OpenAI API key publicly
* **Browser Updates**: Keep your browser updated to the latest version
* **Extension Safety**: Be cautious with browser extensions that might access page content
* **Network Security**: Use HTTPS and avoid unsecured public WiFi for sensitive work

### For Contributors
* **Dependency Updates**: Regularly update npm packages
* **Code Review**: All security-related changes require thorough review
* **Input Validation**: Validate all user inputs, especially for 3D scene manipulation
* **CSP Compliance**: Ensure new features comply with Content Security Policy

### For Maintainers
* **Security Audits**: Regular security audits of dependencies
* **Vulnerability Scanning**: Automated scanning for known vulnerabilities
* **Release Security**: Security review before each release
* **Incident Response**: Prepared response plan for security incidents

## Common Security Scenarios

### API Key Exposure
**Risk**: OpenAI API keys stored in browser localStorage
**Mitigation**: 
* Clear warning about key privacy
* Option to clear stored keys
* No transmission to external servers

### Cross-Site Scripting (XSS)
**Risk**: Malicious scripts in user-generated content
**Mitigation**:
* Input sanitization for all user inputs
* Proper content escaping in UI
* Content Security Policy headers

### Dependency Vulnerabilities
**Risk**: Known vulnerabilities in npm packages
**Mitigation**:
* Regular `npm audit` checks
* Automated dependency updates
* Security-focused dependency selection

### 3D Content Injection
**Risk**: Malicious 3D models or scene manipulation
**Mitigation**:
* Validation of 3D object parameters
* Limits on scene complexity
* Sanitization of AI-generated commands

## Security Updates

### Notification
Security updates will be announced through:
* GitHub Security Advisories
* Release notes with security tags
* Community notifications for critical issues

### Update Process
1. **Identification**: Vulnerability discovered or reported
2. **Assessment**: Severity and impact analysis
3. **Fix Development**: Secure patch development
4. **Testing**: Thorough security testing
5. **Release**: Coordinated security release
6. **Disclosure**: Public disclosure after fix deployment

## Scope

This security policy covers:
* **Core Application**: React frontend and 3D rendering
* **AI Integration**: OpenAI API communication
* **Dependencies**: npm packages and build tools
* **Browser Security**: Client-side security measures

This policy does NOT cover:
* Third-party websites or services
* User's local system security
* Network security beyond HTTPS
* Physical security of user devices

## Security Hall of Fame

We appreciate security researchers who help keep our project secure. Responsible disclosure contributors will be recognized (with their permission) in our security hall of fame.

## Legal

### Responsible Disclosure
We support responsible disclosure and will not pursue legal action against security researchers who:
* Report vulnerabilities through proper channels
* Do not access or modify user data
* Do not disrupt service availability
* Follow coordinated disclosure timelines

### Safe Harbor
We consider security research conducted under this policy to be:
* Authorized under the Computer Fraud and Abuse Act
* Exempt from DMCA restrictions
* Protected activity under security research provisions

## Questions?

For questions about this security policy:
* Review our [contributing guidelines](CONTRIBUTING.md)
* Check existing issues and discussions
* Contact project maintainers through appropriate channels

---

**Security is everyone's responsibility.** Thank you for helping keep Moorph GUI Clean safe and secure! 🔒 