# WhatConverts Call Tracking Quick Setup Checklist

## Pre-Setup (10 minutes)
- [ ] Gather current phone number from Unbounce pages: ________________
- [ ] Have destination phone ready: ________________
- [ ] Know expected daily call volume: ______ calls/day
- [ ] Calculate tracking numbers needed:
  - < 10 calls/day = 5-10 numbers
  - 10-50 calls/day = 15-25 numbers
  - 50+ calls/day = 30+ numbers

## WhatConverts Setup (15 minutes)
- [ ] Create account at whatconverts.com
- [ ] Add website profile with Unbounce domain
- [ ] Copy tracking code from Tracking → Tracking Code

## Dynamic Number Pool (20 minutes)
- [ ] Go to: Tracking → Calls → Phone Numbers → Add Dynamic Pool
- [ ] Choose "Advanced Setup"
- [ ] Enter phone number to replace
- [ ] Select "All Traffic"
- [ ] Choose number quantity based on volume
- [ ] Select area code and number type
- [ ] Enter destination phone
- [ ] Enable call recording
- [ ] Save configuration

## Unbounce Installation (10 minutes)

### Method 1: Script Manager (Preferred)
- [ ] Unbounce → Settings → Script Manager
- [ ] Add Script → Custom Script
- [ ] Name: "WhatConverts Tracking"
- [ ] Placement: Head, Include: All
- [ ] Paste tracking code
- [ ] Select domain(s)
- [ ] Save and Publish

### Method 2: Individual Pages
- [ ] For each landing page:
  - [ ] Edit page → Javascripts
  - [ ] Add script in Head
  - [ ] Paste tracking code
  - [ ] Save and Publish

## Testing (15 minutes)
- [ ] Test URL 1 - Basic swap:
  ```
  yourdomain.com/?gclid=test&wc_clear=true
  ```
  Phone shows tracking number? ✓

- [ ] Test URL 2 - Full Google Ads:
  ```
  yourdomain.com/?gclid=test&utm_source=google&utm_medium=cpc&utm_campaign=test&utm_keyword=test&wc_clear=true
  ```
  
- [ ] Make test call
- [ ] Check WhatConverts Lead Manager:
  - [ ] Call appears
  - [ ] Shows "Google CPC"
  - [ ] Shows keyword "test"
  - [ ] Recording available

## Final Verification
- [ ] All Unbounce pages/variants have tracking
- [ ] Calls forward to correct number
- [ ] Marketing data captures properly
- [ ] Team knows about whisper message

## Go Live!
- [ ] Remove any test data
- [ ] Brief team on new tracking
- [ ] Monitor first day closely
- [ ] Celebrate - you're tracking calls! 🎉

---

**Troubleshooting Hotline**: support@whatconverts.com
**Total Setup Time**: ~60 minutes