# Form Tracking Setup for Two-Step Unbounce Forms

## Challenge
Two-step Unbounce forms can create false conversions if Step 1 (service details) is tracked without Step 2 (contact details).

## Solution
Only track Step 2 form submissions to ensure all leads have contactable information.

## Implementation Steps

### 1. Identify Form Names in WhatConverts
- Go to Tracking → Web Forms
- Look for forms like:
  - "Mobile Media - Step 1 Service Details" ❌
  - "Mobile Media - Step 2 Contact Details" ✅

### 2. Remove Step 1 Tracking
- Delete or disable Step 1 form from WhatConverts
- Keep only Step 2 form active

### 3. Test Configuration

#### Partial Form Test (Step 1 only):
```
https://your-domain.com/?gclid=test&utm_source=google&utm_medium=cpc&utm_campaign=partial-test&utm_keyword=step1-only&wc_clear=true
```
**Expected**: No lead created in WhatConverts

#### Complete Form Test (Both steps):
```
https://your-domain.com/?gclid=test&utm_source=google&utm_medium=cpc&utm_campaign=complete-test&utm_keyword=both-steps&wc_clear=true
```
**Expected**: Lead created with contact details and attribution data

## Benefits
- ✅ Only qualified leads sent to Google Ads
- ✅ Accurate conversion tracking
- ✅ No inflated conversion numbers
- ✅ All leads have contact information

## Alternative Approaches
If you can't delete Step 1:
1. Set up lead scoring rules requiring email/phone
2. Configure Google Ads to only import scored leads
3. Use Unbounce form settings to fire conversion on Step 2 only

## Remember
Always test after changes to ensure tracking works correctly!