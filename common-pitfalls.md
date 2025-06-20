# Common Pitfalls in TKMarketplace Development

This document outlines common issues and mistakes to avoid when working on the TKMarketplace codebase.

## Code Clarity and Documentation

### Unnecessary Comments

Avoid comments that don't add value. Comment "why", not "what" when code is clear.

```javascript
// DON'T: Comments that restate the obvious
const urlObj = new URL(url); // Parse the URL to get its domain

// DON'T: Explain standard language features
function decode(str) { return JSON.parse(decodeURIComponent(str).replace(/\+/g, ' ')); } // decodeURIComponent doesn't convert '+' to space

// DON'T: Repeat framework requirements
return h.redirect(redirectUrl).takeover(); // must return an error, a takeover response, or a continue signal.
```

**Tips:**
- Let clean code speak for itself
- Use descriptive names instead of comments
- Comment only complex logic and business rules
- Explain "why" not "what"
- Comments require maintenance; outdated comments mislead