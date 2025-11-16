# KCS Pro - Support Documentation

## Quick Start

### Installation
1. Install KCS Pro from Atlassian Marketplace
2. Navigate to **Apps** → **KCS Pro Dashboard** in Confluence
3. Enter a space key and click **Scan Space**

### First Scan
1. Go to the KCS Pro dashboard
2. Enter your Confluence space key (e.g., "DEMO")
3. Click "Scan Space" (basic analysis, no AI needed)
4. View your health score and action queue

---

## Features

### Health Score
Your knowledge base health score (0-100) based on:
- **Stale content** (pages not updated recently)
- **Duplicates** (similar/identical content)
- **Readability** (Flesch reading ease score)
- **Completeness** (content length and structure)

### Historical Tracking
Track improvements over time with 3-point comparison:
- **Baseline**: Set manually when you're at a good state
- **Last Scan**: Previous scan results
- **Current**: Most recent scan

**To set baseline:** Run a scan, then click "Set Current as Baseline"

### Action Queue
Prioritized list of pages needing attention:
- **High priority**: Agent flags, duplicates
- **Medium priority**: Stale content
- **Low priority**: Readability/completeness issues

### Agent Flagging
Team members can flag pages for review:
1. Navigate to any Confluence page
2. Click the **flag icon** in the page byline
3. Add a comment explaining the issue
4. Flag appears in the action queue

**To resolve:** Click "Resolve" button in dashboard

### AI Analysis
Get specific improvement suggestions powered by AI:

**Setup:**
1. Go to **Settings** tab
2. Choose AI provider (Anthropic, OpenAI, Azure, or Custom)
3. Enter your API key
4. Save settings

**Per-page analysis:**
- Click **🤖 AI** button next to any page in action queue
- Get tone analysis, clarity score, and specific suggestions

**Supported AI Providers:**
- **Anthropic Claude** (recommended) - `claude-sonnet-4-20250514`
- **OpenAI** - GPT-4 or GPT-3.5
- **Azure OpenAI** - Requires deployment name + endpoint
- **Custom** - Any OpenAI-compatible API

---

## Configuration

### Settings
- **Stale threshold**: Days before a page is considered stale (default: 90)
- **AI provider**: Choose your AI provider and configure API key

### Pricing Tiers
- **Free (up to 10 users)**: Basic analysis, 30-day history
- **Standard (11-100 users)**: $1.00/user/month - AI analysis, 90-day history
- **Standard (101-500 users)**: $0.75/user/month - All Standard features
- **Standard (501+ users)**: $0.50/user/month - All Standard features

---

## Troubleshooting

### "No pages found in this space"
- Verify space key is correct (case-sensitive)
- Ensure you have read permissions for the space
- Check that space has pages (not empty)

### AI Analysis Not Working
- Verify API key is correct in Settings
- Check API key has credits/quota available
- Ensure correct model name for your provider
- Review Forge logs for detailed errors

### Scans Taking Too Long
- Large spaces (500+ pages) can take 2-5 minutes
- AI analysis adds time (~1-2 seconds per page)
- Consider scanning specific spaces rather than entire instances

### Health Score Seems Wrong
- Adjust stale threshold in Settings
- Review which metrics are pulling score down
- Check action queue for specific issues

---

## Best Practices

### Regular Scanning
- Scan weekly or monthly to track trends
- Set baseline when knowledge base is in good shape
- Use historical tracking to show progress to leadership

### Team Workflow
1. Run initial scan to establish baseline
2. Review action queue in team meeting
3. Assign pages from queue to team members
4. Use agent flags for issues discovered while working
5. Re-scan monthly to track improvements

### AI Usage
- Start with basic analysis (free)
- Add AI for high-priority pages in action queue
- Use AI suggestions to train team on quality standards

---

## Support

### Contact
- Email: [your-support-email@domain.com]
- Response time: 24-48 hours

### Feature Requests
Submit via [GitHub Issues / Feedback Form]

### Bug Reports
Include:
- Space key and approximate page count
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if applicable

---

## FAQ

**Q: Does KCS Pro modify my pages?**
A: No, it only reads and analyzes. The only modification is adding optional badges.

**Q: Where is my data stored?**
A: All data stays in Atlassian Forge storage within your Confluence instance.

**Q: Can I export scan results?**
A: Currently manual copy from dashboard. CSV export coming in future release.

**Q: Does it work with Confluence Server/Data Center?**
A: No, currently Cloud only. Server/DC support planned.

**Q: How much does AI analysis cost?**
A: You pay your AI provider directly (typically $0.01-0.03 per page analyzed).

**Q: Is there a demo/sandbox?**
A: 30-day free trial includes all features. Test on a small space first.
