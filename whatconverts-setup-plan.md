# WhatConverts Setup Plan for Google Ads + Unbounce

## Overview
This guide will help you set up WhatConverts to track:
- Form submissions from Unbounce landing pages
- Phone calls (both from displayed numbers and form submissions)
- Google Ads conversion data with proper attribution

## Phase 1: Prerequisites & Account Setup

### 1.1 WhatConverts Account
- [ ] Sign up for WhatConverts account at whatconverts.com
- [ ] Choose appropriate plan (must support number of tracking numbers needed)
- [ ] Complete account verification
- [ ] Note your Account ID (found in Account Settings)

### 1.2 Access Requirements
- [ ] Admin access to Google Ads account
- [ ] Admin access to Unbounce account
- [ ] Access to domain DNS (if using custom tracking domain)

### 1.3 Gather Information
- [ ] List all Unbounce landing page URLs
- [ ] Count number of forms on each page
- [ ] List all phone numbers currently displayed
- [ ] Google Ads Customer ID
- [ ] List of conversion actions to track

## Phase 2: WhatConverts Base Configuration

### 2.1 Profile Setup
1. Log into WhatConverts
2. Navigate to Settings > Profile
3. Set up your company information
4. Configure timezone to match Google Ads

### 2.2 Tracking Code Installation
1. Go to Settings > Tracking Code
2. Copy the WhatConverts JavaScript tracking code
3. Important settings to configure:
   - Enable "Track all forms automatically"
   - Enable "Track phone calls"
   - Set cookie duration (recommend 90 days)

## Phase 3: Unbounce Integration

### 3.1 Install WhatConverts Tracking Code
1. Log into Unbounce
2. For each landing page:
   - Click on the page
   - Go to "Javascripts" section
   - Click "Add New Javascript"
   - Name it "WhatConverts Tracking"
   - Paste the WhatConverts tracking code
   - Set placement to "Head"
   - Set to load on "All page variants"
   - Save and republish page

### 3.2 Form Tracking Configuration
1. The WhatConverts code will automatically detect Unbounce forms
2. For custom tracking:
   - Add class "wc-track" to forms you want to track
   - Or use form ID targeting in WhatConverts dashboard

### 3.3 Hidden Field Setup (for better attribution)
1. In Unbounce form builder, add hidden fields:
   - gclid (for Google Ads click ID)
   - utm_source
   - utm_medium
   - utm_campaign
   - utm_term
   - utm_content
2. These will be automatically populated and sent to WhatConverts

## Phase 4: Call Tracking Setup

### 4.1 Tracking Number Pool
1. In WhatConverts, go to "Tracking Numbers"
2. Purchase tracking numbers:
   - Purchase enough numbers for concurrent visitors
   - Rule of thumb: 1 number per 50-100 monthly visitors
3. Set up number pool settings:
   - Area code preferences
   - Toll-free vs local numbers

### 4.2 Dynamic Number Replacement
1. In WhatConverts, go to "Call Tracking"
2. Configure swap targets:
   - Add each phone number from your Unbounce pages
   - Use CSS selector or phone number matching
3. Set swap conditions:
   - Swap for all visitors, or
   - Swap only for paid traffic (recommended)

### 4.3 Call Forwarding
1. Set destination number for call forwarding
2. Configure call recording (if needed)
3. Set up whisper message (optional)
4. Configure business hours

## Phase 5: Google Ads Integration

### 5.1 Connect Google Ads Account
1. In WhatConverts, go to Integrations > Google Ads
2. Click "Connect Google Ads Account"
3. Authenticate with Google account
4. Select the correct Google Ads account
5. Grant necessary permissions

### 5.2 Conversion Action Setup
1. Choose conversion import method:
   - Automatic: WhatConverts creates conversions in Google Ads
   - Manual: You create conversions, WhatConverts sends data
2. For each conversion type:
   - Form Submission
   - Phone Call (from ads)
   - Phone Call (from website)
3. Set conversion values if applicable

### 5.3 GCLID Tracking
1. Ensure Google Ads auto-tagging is enabled
2. WhatConverts will automatically capture GCLID
3. This enables accurate conversion attribution

## Phase 6: Testing & Verification

### 6.1 Form Tracking Test
1. Visit your Unbounce page with test parameters:
   `?utm_source=test&utm_medium=test&gclid=test123`
2. Submit a test form
3. Check WhatConverts dashboard for the lead
4. Verify all data is captured correctly

### 6.2 Call Tracking Test
1. Visit page from Google Ads (or with gclid parameter)
2. Verify phone number swaps correctly
3. Make test call
4. Check WhatConverts dashboard for call record
5. Verify recording and data capture

### 6.3 Google Ads Data Flow
1. Wait 3-4 hours after test conversions
2. Check Google Ads for imported conversions
3. Verify conversion values and attribution

## Phase 7: Optimization & Monitoring

### 7.1 Set Up Reporting
1. Configure email reports in WhatConverts
2. Set up Google Ads conversion columns
3. Create custom reports for client

### 7.2 Quality Assurance
1. Set up lead scoring rules
2. Configure spam filters
3. Set up alerts for tracking issues

### 7.3 Ongoing Maintenance
- Weekly: Check tracking is working
- Monthly: Review number pool utilization
- Quarterly: Audit conversion data accuracy

## Common Issues & Solutions

### Forms Not Tracking
- Check if WhatConverts script is loading
- Verify form has proper ID/class
- Check for JavaScript conflicts

### Numbers Not Swapping
- Verify tracking pool has available numbers
- Check swap conditions match traffic source
- Ensure phone numbers match exactly

### Google Ads Conversions Missing
- Verify GCLID is being captured
- Check conversion import settings
- Ensure proper attribution window

## Next Steps
1. Complete prerequisites checklist
2. Schedule implementation (2-3 hours)
3. Plan testing phase (1 hour)
4. Set up monitoring routine

---

**Note**: This plan will be customized based on your specific requirements once you provide more details about your setup.