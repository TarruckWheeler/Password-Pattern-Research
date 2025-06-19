# Contributing to Password Pattern Research

First off, thank you for considering contributing to this security research! 🎉

## 🤝 Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct:

- **Be respectful** of differing viewpoints and experiences
- **Accept constructive criticism** gracefully
- **Focus on what's best** for the community and security
- **Show empathy** towards other community members
- **Never use this research** for malicious purposes

## 🚀 How Can I Contribute?

### 1. Reporting Bugs
Before creating bug reports, please check existing issues. When creating a bug report, include:

```markdown
**Bug Description:**
A clear and concise description

**To Reproduce:**
1. Go to '...'
2. Click on '....'
3. See error

**Expected Behavior:**
What you expected to happen

**Environment:**
- OS: [e.g., Ubuntu 20.04]
- Python version: [e.g., 3.9.0]
- Rust version: [e.g., 1.70.0]
```

### 2. Suggesting Enhancements
Enhancement suggestions are tracked as GitHub issues. Create an issue and provide:
- **Use case** - Why is this needed?
- **Proposed solution** - How should it work?
- **Alternatives** - What other solutions did you consider?

### 3. Code Contributions

#### First Time Setup
```bash
# Fork and clone the repo
git clone https://github.com/YOUR-USERNAME/password-pattern-research.git
cd password-pattern-research

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
pip install -r requirements-dev.txt

# Install pre-commit hooks
pre-commit install
```

#### Development Process
1. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes following our style guide

3. Write/update tests:
   ```bash
   pytest tests/
   cargo test
   ```

4. Run security checks:
   ```bash
   # Python security scan
   bandit -r src/

   # Dependency audit
   pip-audit
   cargo audit
   ```

5. Commit with a descriptive message:
   ```bash
   git commit -m "feat: add pattern detection for keyboard walks"
   ```

6. Push and create a Pull Request

## 📝 Style Guidelines

### Python Style
```python
# We follow PEP 8 with these additions:
# - Use type hints for all functions
# - Maximum line length: 88 (Black formatter)
# - Use descriptive variable names

from typing import List, Dict, Optional

def analyze_password_pattern(
    passwords: List[str], 
    threshold: float = 0.84
) -> Dict[str, float]:
    """
    Analyze password patterns in a list of passwords.
    
    Args:
        passwords: List of passwords to analyze
        threshold: Confidence threshold for pattern detection
        
    Returns:
        Dictionary mapping patterns to their occurrence rates
    """
    # Implementation here
    pass
```

### Rust Style
```rust
// Follow official Rust style guide
// Use clippy for linting
// Document all public functions

/// Analyzes password entropy using Shannon entropy calculation
/// 
/// # Arguments
/// * `password` - The password to analyze
/// 
/// # Returns
/// The entropy value in bits
pub fn calculate_entropy(password: &str) -> f64 {
    // Implementation
}
```

### JavaScript Style
```javascript
// Use ES6+ features
// Prettier for formatting
// JSDoc for documentation

/**
 * Constant-time string comparison to prevent timing attacks
 * @param {string} a - First string
 * @param {string} b - Second string
 * @returns {boolean} Whether strings are equal
 */
const constantTimeCompare = (a, b) => {
    // Implementation
};
```

## 🧪 Testing Requirements

All contributions must include tests:

```python
# Example test
def test_pattern_detection():
    passwords = ["Password123", "Password124", "Password125"]
    patterns = detect_patterns(passwords)
    assert patterns["increment"] == 0.95  # 95% confidence
```

Coverage requirements:
- New features: 90% coverage minimum
- Bug fixes: Must include regression test
- Security features: 100% coverage required

## 📊 Commit Message Convention

We use conventional commits:

```
feat: add keyboard walk pattern detection
fix: resolve timing leak in comparison function
docs: update API documentation
test: add tests for Markov chain implementation
security: patch CVE-2024-XXXX vulnerability
perf: optimize pattern matching algorithm
refactor: restructure timing attack module
```

## 🔒 Security Considerations

When contributing:

1. **Never commit real passwords or breached data**
2. **Use only synthetic test data**
3. **Run security scans before submitting**
4. **Consider timing attack implications**
5. **Document any security assumptions**

## 📦 Dependencies

Adding new dependencies requires justification:
- Is it actively maintained?
- Does it have security vulnerabilities?
- Is the license compatible (MIT/Apache/BSD)?
- Can we implement it ourselves reasonably?

## 🚢 Release Process

1. Update version numbers
2. Update CHANGELOG.md
3. Run full test suite
4. Security audit
5. Tag release
6. Deploy documentation

## 💡 Research Contributions

We also welcome:
- New attack techniques (responsibly disclosed)
- Defense mechanism proposals
- Academic paper references
- Real-world case studies (anonymized)

## ❓ Questions?

- Check our [FAQ](docs/FAQ.md)
- Join our [Discord](https://discord.gg/yourserver)
- Email: contribute@yourdomain.com

## 🏆 Recognition

Contributors will be:
- Added to [AUTHORS.md](AUTHORS.md)
- Acknowledged in release notes
- Eligible for bug bounties (security findings)

---

Thank you for helping make cryptocurrency more secure! 🔐
