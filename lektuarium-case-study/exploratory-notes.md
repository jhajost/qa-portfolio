# Lektuarium – Exploratory Testing Notes

## Test Environments
- Android: Chrome, Firefox
- Desktop (Windows 11): Chrome, Firefox

## Key Findings

### 1. State Management
- Book status changes from "read" to "to read" after lending and receiving back

### 2. Browser Compatibility
- Multiple features fail in Firefox but work in Chrome:
  - barcode scanning (mobile)
  - changing library visibility
  - adding friends
  - displaying book list on profile

### 3. Navigation / UX Issues (Mobile)
- No navigation from Bibliodesk to:
  - main Lektuarium page
  - user profile
  - friend invitations

### 4. ISBN / Metadata Issues
- Some correct ISBNs not found in external sources
- Some ISBNs return incorrect book metadata
- Some ISBNs recognised but require manual book entry
