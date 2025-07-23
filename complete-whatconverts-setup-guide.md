# Complete WhatConverts Setup Guide for Google Ads + Unbounce

## Your Configuration Summary
- ✅ Existing WhatConverts account
- 📄 1 Unbounce landing page with 3 variants
- 📞 Static phone number displayed at top of page
- 🎯 Multiple Google Ads campaigns feeding to this page
- 📊 Single conversion action for all campaigns
- 🔧 Using Unbounce's native scripts (we'll add WhatConverts)
- 📈 Need to track both form submissions and phone calls

---

## Phase 1: WhatConverts Base Setup (15 minutes)

### 1.1 Get Your Tracking Code
1. Log into WhatConverts
2. Click **Tracking** in top menu → **Tracking Code**
3. Copy the **Standard HTML Code** (it looks like this):

```javascript
<script type="text/javascript">
var _wc = _wc || {};
_wc.account_id = 'YOUR_ACCOUNT_ID_HERE';
(function() {
  var wc = document.createElement('script');
  wc.type = 'text/javascript';
  wc.async = true;
  wc.src = ('https:' == document.location.protocol ? 'https://' : 'http://') + 
          'cdn.whatconverts.com/widget.min.js';
  var s = document.getElementsByTagName('script')[0];
  s.parentNode.insertBefore(wc, s);
})();
</script>
```

### 1.2 Configure WhatConverts Settings
In WhatConverts dashboard:
1. Go to **Settings** → **Tracking**
2. Enable these options:
   - ✅ Track all forms automatically
   - ✅ Track phone calls
   - ✅ Capture URL parameters
   - ✅ First party cookies (set to 90 days)

---

## Phase 2: Unbounce Integration (30 minutes)

### 2.1 Add Tracking Code to Your Landing Page

Since you have 3 variants, you'll use the **Landing Page Method** and ensure it applies to ALL variants:

1. Log into Unbounce
2. Select your landing page
3. Click **Edit**
4. Click **Javascripts** at the bottom of the page editor
5. Click **Add New Javascript**
6. Configure:
   - **Name**: "WhatConverts Tracking"
   - **Placement**: Head
   - **Included on**: All page variants ⚠️ CRITICAL!
7. Paste your WhatConverts tracking code
8. Click **Save Code**
9. **Save** and **Publish** your page

### 2.2 Add Hidden Fields for Google Ads Tracking

1. In the Unbounce editor, click on your form
2. Add these hidden fields:
   - Field name: `gclid` → Maps to URL parameter: `gclid`
   - Field name: `utm_source` → Maps to URL parameter: `utm_source`
   - Field name: `utm_medium` → Maps to URL parameter: `utm_medium`
   - Field name: `utm_campaign` → Maps to URL parameter: `utm_campaign`
   - Field name: `utm_content` → Maps to URL parameter: `utm_content`
   - Field name: `utm_term` → Maps to URL parameter: `utm_term`

3. Save and republish the page

---

## Phase 3: Form Tracking Configuration (20 minutes)

### 3.1 Set Up Form Tracking in WhatConverts

Since you have 3 variants, you need to add each variant's form separately:

#### For EACH variant:

1. **Get Form Details**:
   - Go to your Unbounce page (the live version)
   - Right-click on the form
   - Select "Inspect" or "Inspect Element"
   - Find `<form action="..."` (will start with `/fsg?pageId=`)
   - Copy the entire action value (e.g., `/fsg?pageId=12345678-90ab-cdef...`)

2. **Get Submit Button ID**:
   - Right-click the submit button
   - Click "Inspect"
   - Find the button ID (like `lp-pom-button-123`)
   - Copy this ID

3. **Add to WhatConverts**:
   - Log into WhatConverts
   - Go to **Tracking** → **Forms** → **Web Forms**
   - Click **Add Web Form** → **Manual Setup**
   - Configure:
     - **Form Name**: "Unbounce Form - Variant A" (name each variant)
     - **Attribute Type**: Action
     - **Attribute Value**: Paste the form action from step 1
     - **Alternate Submit Button**: Yes
     - **Button Attribute Type**: ID
     - **Button Attribute Value**: Paste the button ID from step 2
   - Click **Finish**

⚠️ **IMPORTANT**: Repeat for all 3 variants! Each will have a different form action value.

---

## Phase 4: Call Tracking Setup (30 minutes)

### 4.1 Purchase Tracking Numbers

1. In WhatConverts, go to **Tracking Numbers**
2. Click **Add Tracking Numbers**
3. Purchase numbers based on your expected traffic:
   - **< 1,000 visits/month**: 10-15 numbers
   - **1,000-5,000 visits/month**: 20-30 numbers
   - **> 5,000 visits/month**: 40-50 numbers

### 4.2 Set Up Dynamic Number Insertion (DNI)

1. Go to **Call Tracking** → **Swap Targets**
2. Click **Add New Swap Target**
3. Enter your phone number EXACTLY as it appears on your page
   - Include spaces, dashes, parentheses exactly as shown
   - Example: If page shows "(555) 123-4567", enter it exactly like that
4. Configure swap settings:
   - **Swap When**: "Visitor came from Google Ads" (or "Has GCLID parameter")
   - **Number Pool**: Select your purchased numbers
   - **Session Duration**: 30 minutes

### 4.3 Configure Call Forwarding

1. Still in Call Tracking settings:
   - **Forward To**: Your actual business number
   - **Record Calls**: Yes (check local laws)
   - **Whisper Message**: "Google Ads lead" (optional)
   - **Business Hours**: Set if needed

---

## Phase 5: Google Ads Integration (20 minutes)

### 5.1 Connect Google Ads Account

Based on the documentation, you'll need to:

1. In WhatConverts, go to **Integrations** → **Google Ads**
2. Click **Connect to Google Ads**
3. Authenticate with your Google account
4. Select the correct Google Ads account
5. Grant necessary permissions

### 5.2 Set Up Single Conversion Action

Since you want ONE conversion for all campaigns:

**In Google Ads:**
1. Go to Tools & Settings → Conversions
2. Click the + button to create new conversion
3. Select **Import** → **Other data sources or CRMs** → **Track conversions from clicks**
4. Configure:
   - **Conversion name**: "WhatConverts - All Leads"
   - **Category**: Lead
   - **Value**: Don't use a value (or set different values)
   - **Count**: Every
   - **Click-through conversion window**: 30 days
   - **Attribution model**: Data-driven (or Last click)
5. Save the conversion

**In WhatConverts:**
1. Go back to Google Ads integration settings
2. Select your import method
3. Map to the conversion you just created

### 5.3 Enable Auto-tagging in Google Ads

1. In Google Ads, go to Settings → Account settings
2. Ensure **Auto-tagging** is ON
3. This allows GCLID tracking

---

## Phase 6: Testing Protocol (30 minutes)

### 6.1 Test Form Tracking (Each Variant)

For each of your 3 variants:

1. Create test URL:
   ```
   https://your-page.unbounce.com/variant-a/?gclid=TEST_VARIANT_A&utm_source=google&utm_medium=cpc&utm_campaign=test
   ```

2. Submit test form with identifiable info:
   - Name: "Test Variant A"
   - Email: test-a@test.com
   - Phone: Use a real number you can verify

3. Check WhatConverts dashboard immediately:
   - Lead should appear within 60 seconds
   - Verify GCLID = "TEST_VARIANT_A"
   - Check all form fields captured

### 6.2 Test Call Tracking

1. Visit page with test GCLID: `?gclid=TEST_CALL_123`
2. Verify phone number changed to a tracking number
3. Call the tracking number
4. In WhatConverts, verify:
   - Call appears in dashboard
   - Recording works (if enabled)
   - GCLID captured correctly

### 6.3 Verify Google Ads Data Flow

1. After testing, wait 3-4 hours
2. Check Google Ads → Conversions
3. Your test conversions should NOT appear (they have fake GCLIDs)
4. Real conversions will show up once live

---

## Phase 7: Go-Live Checklist

Before launching:

- [ ] WhatConverts tracking code is on all 3 variants
- [ ] All 3 form variants are added to WhatConverts
- [ ] Hidden fields capture GCLID and UTMs
- [ ] Phone number swaps when visiting with ?gclid parameter
- [ ] Test form submissions appear in dashboard
- [ ] Test calls appear in dashboard
- [ ] Google Ads account is connected
- [ ] Conversion action is created and mapped
- [ ] Email notifications are set up for new leads

---

## Ongoing Monitoring

### First Week - Daily Checks
- Verify leads appearing in WhatConverts
- Check Google Ads is receiving conversions (3-4 hour delay)
- Monitor phone number pool usage (<80% is good)

### Weekly
- Review conversion data accuracy
- Check for any JavaScript errors
- Verify all variants still tracking

### Monthly
- Audit a sample of conversions
- Review call recordings
- Adjust number pool size if needed

---

## Quick Troubleshooting

### Forms Not Tracking?
1. Check browser console (F12) for JavaScript errors
2. Verify form action hasn't changed after Unbounce updates
3. Try manually adding class `wc-track` to form

### Phone Numbers Not Swapping?
1. Clear cookies and try with fresh ?gclid parameter
2. Check exact phone number format matches
3. Verify number pool isn't exhausted

### No Conversions in Google Ads?
1. Normal delay is 3-4 hours
2. Check conversion window (30 days)
3. Verify GCLID is being captured in WhatConverts

---

## Support Contacts

**WhatConverts Support**
- Email: support@whatconverts.com
- Help: https://www.whatconverts.com/contact

**Questions to ask if stuck:**
1. "My Unbounce form has 3 variants - do I need to add each one separately?"
2. "What's the recommended number pool size for [X] visits per month?"
3. "How do I verify GCLID is passing correctly?"

---

## Time Estimate
- Setup: 2.5 hours
- Testing: 30 minutes
- **Total: 3 hours**

Ready to start? Begin with Phase 1 and work through systematically!