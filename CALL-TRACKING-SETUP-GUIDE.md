# WhatConverts Call Tracking Setup Guide for Google Ads → Unbounce

## Overview
This guide will help you set up call tracking for your Google Ads campaigns driving traffic to Unbounce landing pages. You'll be able to track which keywords, ads, and campaigns generate phone calls.

## What You'll Achieve
- Track calls back to specific Google Ads keywords
- See full customer journey (landing page → call)
- Record calls and qualify leads
- Send call conversions back to Google Ads for optimization

## Prerequisites Checklist

### Account Access Needed:
- [ ] WhatConverts account (sign up at whatconverts.com)
- [ ] Unbounce account with admin access
- [ ] Google Ads account (for testing)
- [ ] Access to your business phone system

### Information to Gather:
- [ ] Current phone number(s) displayed on Unbounce pages
- [ ] Destination phone number (where calls should forward)
- [ ] List of all Unbounce landing pages/domains
- [ ] Expected daily call volume
- [ ] Budget for tracking numbers ($2-5 per number/month)

## Phase 1: WhatConverts Initial Setup

### Step 1: Create WhatConverts Account
1. Go to whatconverts.com and sign up
2. Complete basic account setup
3. Add your company information

### Step 2: Add Your Website Profile
1. Click "Profiles" → "Add Profile"
2. Enter your Unbounce domain(s)
3. Select your timezone
4. Save profile

### Step 3: Get Your Tracking Code
1. Go to "Tracking" → "Tracking Code"
2. Copy the Standard HTML code
3. Keep this handy for Unbounce integration

## Phase 2: Configure Dynamic Number Pool

### Step 1: Access Phone Number Setup
1. In WhatConverts, go to "Tracking" → "Calls" → "Phone Numbers"
2. Click "+ Add Dynamic Pool"
3. Select "Advanced Setup"

### Step 2: Configure for Google Ads Tracking
1. **Number to Replace**: Enter your current phone number from Unbounce
2. **Traffic Source**: Select "All Traffic" (captures all marketing data)
3. Click "Next Step"

### Step 3: Select Tracking Numbers
1. **Pool Size Calculation**:
   - Low volume (< 10 calls/day): 5-10 numbers
   - Medium volume (10-50 calls/day): 15-25 numbers
   - High volume (50+ calls/day): 30+ numbers
2. Choose country and area code
3. Select Local or Toll-Free
4. Click "Find Numbers" and review options
5. Click "Next Step"

### Step 4: Set Call Forwarding
1. Enter your destination phone number
2. Configure call features:
   - [ ] Call Recording (recommended)
   - [ ] Call Transcription
   - [ ] Whisper Message (tells you it's a tracked call)
   - [ ] Greeting Message (optional)
3. Set business hours if needed
4. Click "Next Step" then "Finish"

## Phase 3: Install on Unbounce

### Option A: Script Manager (Recommended - Covers All Pages)
1. Log into Unbounce
2. Go to "Settings" → "Script Manager"
3. Click "Add a Script"
4. Select "Custom Script"
5. Name it "WhatConverts Tracking"
6. Click "Add Script Details"
7. Configure:
   - Placement: Head
   - Included On: All
8. Paste your WhatConverts tracking code
9. Select your domain(s)
10. Click "Save and Publish Script"

### Option B: Individual Page Method
1. Open each landing page in Unbounce
2. Click "Edit"
3. Click "Javascripts" (bottom of editor)
4. Add new script:
   - Name: "WhatConverts Tracking"
   - Placement: Head
5. Paste tracking code
6. Save and publish
7. Repeat for ALL pages and variants

## Phase 4: Testing Your Setup

### Test 1: Basic Number Swap
1. Open incognito/private browser
2. Visit: `https://yourdomain.com/?gclid=test&wc_clear=true`
3. Verify phone number changed to tracking number
4. Note which tracking number appears

### Test 2: Google Ads Simulation
1. Visit: `https://yourdomain.com/?gclid=test&utm_source=google&utm_medium=cpc&utm_campaign=test-campaign&utm_keyword=test-keyword&wc_clear=true`
2. Call the tracking number displayed
3. In WhatConverts Lead Manager, verify:
   - Call appears with "Google CPC" source
   - Keyword shows as "test-keyword"
   - Campaign shows as "test-campaign"

### Test 3: Call Flow
1. Make a test call
2. Verify:
   - Call forwards correctly
   - Recording works (if enabled)
   - Whisper message plays (if enabled)

## Phase 5: Verify Everything Works

### In WhatConverts Dashboard:
- [ ] Tracking numbers show as "Active"
- [ ] Test calls appear in Lead Manager
- [ ] Marketing data (source, keyword, campaign) captured correctly
- [ ] Call recordings accessible

### On Unbounce Pages:
- [ ] Numbers swap when visiting with tracking parameters
- [ ] Original number still shows for direct traffic
- [ ] All page variants have tracking code

## Common Issues & Solutions

### Numbers Not Swapping
- Clear browser cache and cookies
- Verify tracking code is in page header
- Check if JavaScript is enabled
- Ensure tracking code is on all variants

### No Marketing Data
- Verify UTM parameters in URLs
- Check Google Ads auto-tagging (gclid)
- Test with manual UTM parameters

### Calls Not Forwarding
- Verify destination number format
- Check business hours settings
- Ensure tracking numbers are active

## Next Steps

1. **Monitor Performance**:
   - Check Lead Manager daily
   - Review call quality and duration
   - Identify top-performing keywords

2. **Set Up Integrations**:
   - Connect Google Ads for conversion import
   - Set up lead notifications
   - Configure CRM integration

3. **Optimize**:
   - Adjust number pool size based on volume
   - Set up lead scoring
   - Create custom reports

## Quick Reference Test URLs

Replace `yourdomain.com` with your actual domain:

```
# Basic test
https://yourdomain.com/?gclid=test&wc_clear=true

# Full Google Ads test
https://yourdomain.com/?gclid=test&utm_source=google&utm_medium=cpc&utm_campaign=test-campaign&utm_keyword=test-keyword&wc_clear=true

# Organic test
https://yourdomain.com/?utm_source=google&utm_medium=organic&wc_clear=true
```

## Support Resources

- WhatConverts Support: support@whatconverts.com
- Help Documentation: whatconverts.com/help
- This guide: Update as you learn!

---

**Remember**: Always test with real devices and real calls to ensure everything works before launching campaigns!