# Changelog – PM CENTRAL V7.2

## Updated
- Replaced the PM Compliance SharePoint URL with the new link supplied by the user.
- Updated dashboard platform label from Netlify to Cloudflare Workers.
- Added a clearer MPE2 Team identity chip on the dashboard.
- Updated About page to V7.2 Cloudflare MPE2 Edition and Cloudflare Workers + GitHub.
- Updated application title, package version, build metadata, and deployment documentation.
- Preserved the existing team workspaces, Apps Script URLs, SharePoint fallback behavior, navigation, and local features.

## Review notes / limitations
- PE and NPE remain placeholders until their approved form URLs are supplied.
- Equipment, schedule, work order, and uploads are still browser-local; they are not centrally synchronized.
- Microsoft Graph API, OneDrive automatic upload, authentication, and role-based access are not implemented in this release.
- SharePoint iframe display may depend on Microsoft 365 policy and the viewer's permission; direct-open fallback remains available.
