# WhatConverts Call & Form Tracking Project

## Project Overview
This project contains documentation and setup guides for implementing WhatConverts call and form tracking for Google Ads campaigns driving traffic to Unbounce landing pages.

## Current Setup Status
- ✅ WhatConverts account configured
- ✅ Dynamic number pool active (4 tracking numbers)
- ✅ Unbounce integration completed
- ✅ Google Ads conversion import configured
- ✅ Form tracking configured (Step 2 only for qualified leads)

## Key Configuration Details

### Phone Numbers
- **Business Line**: +448450752752
- **Display Format**: 08450 752 752
- **Tracking Pool**: 4 numbers (+448083040633-636)
- **Google Call Extension**: +448083040637

### Google Ads Integration
- **Conversion Actions Created**:
  - VGA WC Leads (all lead types: calls, forms, chats)
  - VGA WC Call Extension (Google call assets only)
- **Attribution**: Last Click, 90-day lookback
- **Value**: No conversion value set

### Form Tracking Configuration
- **Two-step Unbounce forms**: Only Step 2 (contact details) is tracked
- **Prevents false conversions**: Step 1 only submissions don't count as leads
- **Qualified leads only**: Must have phone or email to be tracked

### Testing URLs
Replace `your-domain.com` with actual Unbounce domain:

```bash
# Basic number swap test
https://your-domain.com/?wc_clear=true

# Full Google Ads test (calls and forms)
https://your-domain.com/?gclid=test&utm_source=google&utm_medium=cpc&utm_campaign=test-campaign&utm_keyword=test-keyword&wc_clear=true
```

## Important Notes
1. **Never rename** the Google Ads conversion actions or integration will break
2. Campaign/keyword data is captured but may not display in Lead Manager columns
3. View detailed lead data by clicking "View Lead" for each call
4. All lead types report to Google Ads as single conversion action
5. **Form tracking**: Delete Step 1 forms from WhatConverts to track only qualified leads

## Support Resources
- WhatConverts Support: support@whatconverts.com
- Help Documentation: whatconverts.com/help

## Project Files
- `CALL-TRACKING-SETUP-GUIDE.md` - Comprehensive setup instructions
- `CALL-TRACKING-QUICK-CHECKLIST.md` - Quick reference checklist
- `VERIFY-YOUR-SETUP.md` - Troubleshooting guide
- Research files with WhatConverts documentation URLs

## Claude's Memories
- 1