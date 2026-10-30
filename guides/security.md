# Security Guidelines (Reusable)

This is a reusable security guide. Adapt to project needs.

## Secrets Management
- Never commit secrets, API keys, tokens, or credentials
- Use environment variables or secure secret storage
- Add sensitive files to .gitignore
- Rotate secrets if exposed

## Code Security
- Validate and sanitize all inputs
- Use parameterized queries to prevent SQL injection
- Avoid command injection
- Handle errors without leaking sensitive info
- Use secure random number generation

## Dependencies
- Keep dependencies up to date
- Review dependencies before adding
- Watch for known vulnerabilities
- Use lock files

## Network Security
- Use HTTPS by default
- Validate certificates
- Implement proper authentication/authorization
- Don't send sensitive data in URLs

## Logging
- Never log secrets or PII
- Use appropriate log levels
- Be careful with debug logs in production

## Permissions
- Follow principle of least privilege
- Request minimal permissions
- Justify permission usage

## Incident Response
- Document how to report vulnerabilities
- Have a process for security issues
- Don't disclose publicly until patched
