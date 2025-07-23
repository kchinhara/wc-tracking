# 🔍 Verify Your WhatConverts Call Tracking Setup

## Current Configuration Check

### ✅ What You Have:
- **Pool**: 4 tracking numbers (+448083040633-636) for "All Traffic"
- **Google Call Extension**: +448083040637
- **Forward To**: +448450752752
- **Swap Number**: 7769518628 ⚠️ (This might be the issue!)

## 🚨 Potential Issue: Swap Number Format

Your swap number `7769518628` doesn't match UK format. This should be the **exact** phone number displayed on your Unbounce pages.

### Action Required:
1. **Check your Unbounce pages** - What phone number is actually displayed?
   - Should be something like: +44 845 075 2752 or 0845 075 2752
   - Could be formatted with spaces, dashes, or parentheses

2. **Update the swap number** in WhatConverts:
   - Go to Tracking → Calls → Phone Numbers
   - Edit your "All Traffic" pool
   - Change swap number to match EXACTLY what's on Unbounce
   - Remove ALL formatting (no spaces, dashes, parentheses)
   - Example: If Unbounce shows "0845 075 2752", enter "08450752752"

## 🧪 Test Your Setup NOW

### Test 1: Basic Number Swap
```
https://your-unbounce-domain.com/?wc_clear=true
```
**Expected**: Should show one of your tracking numbers (+448083040633-636)

### Test 2: Google Ads Test
```
https://your-unbounce-domain.com/?gclid=test&utm_source=google&utm_medium=cpc&utm_campaign=test-campaign&utm_keyword=test-keyword&wc_clear=true
```
**Expected**: Tracking number appears

### Test 3: Make a Test Call
1. Call the tracking number that appears
2. Check WhatConverts Lead Manager
3. Verify:
   - Call appears immediately
   - Shows "Google CPC" as source
   - Shows "test-keyword" as keyword
   - Call forwards to +448450752752

## 📋 Quick Diagnostic Checklist

### In Browser (View Page Source):
- [ ] WhatConverts script present? (search for "whatconverts")
- [ ] Phone number on page matches swap number in WhatConverts?

### In WhatConverts:
- [ ] Swap number has NO formatting (just digits)?
- [ ] Pool shows as "Active"?
- [ ] Last checkout shows recent time?

### Call Test Results:
- [ ] Number swaps when visiting with test URL?
- [ ] Call forwards correctly?
- [ ] Lead appears in dashboard with correct attribution?

## 🔧 If Numbers Don't Swap:

1. **Wrong Swap Number** (Most Common)
   - The swap number MUST match exactly what's on your page
   - Check for hidden characters or spaces

2. **JavaScript Issues**
   - Open browser console (F12)
   - Look for red errors
   - Check if WhatConverts script loads

3. **Cookie/Cache Issues**
   - Always test in incognito/private mode
   - Use `?wc_clear=true` parameter

## 📞 Your Specific Numbers to Test:

When the swap works, you should see one of these:
- +448083040633
- +448083040634
- +448083040635
- +448083040636

## Need More Help?

1. **Check browser console** for JavaScript errors
2. **View page source** to confirm script installation
3. **Email support@whatconverts.com** with:
   - Your profile ID
   - Test URL
   - Screenshot of the issue

---

**Most likely fix**: Update your swap number to match exactly what's on your Unbounce pages!