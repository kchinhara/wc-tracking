# Customized WhatConverts Setup Plan for Your Configuration

## Your Specific Setup
- ✅ Existing WhatConverts account
- 📄 1 Unbounce page with 3 variants
- 📞 Phone number at top of page (static display)
- 🎯 Multiple Google Ads campaigns
- 📊 Single conversion action for all campaigns
- 🔧 Using Unbounce's native tracking
- 📈 Tracking both form fills and phone calls

## Quick Start Checklist

### Phase 1: Initial Setup (30 minutes)

#### 1.1 In WhatConverts Dashboard
1. Log into your WhatConverts account
2. Navigate to **Settings > Tracking Code**
3. Copy your unique tracking code
4. Note your Account ID for later reference

#### 1.2 Configure Tracking Settings
In WhatConverts settings, ensure these are enabled:
- ✅ "Track all forms automatically" 
- ✅ "Track phone calls"
- ✅ "Capture URL parameters" (for GCLID)
- ✅ "First party cookies" (90-day duration recommended)

### Phase 2: Unbounce Implementation (45 minutes)

#### 2.1 Install Tracking Code on All Variants
Since you have 3 variants, you need to add the code to the BASE page:

1. Log into Unbounce
2. Navigate to your landing page
3. Click **Javascripts** (bottom of the builder)
4. Click **Add New Javascript**
5. Configure as follows:
   - **Name**: "WhatConverts Tracking"
   - **Placement**: Head
   - **Include on**: All page variants ⚠️ (This is crucial!)
   - **Code**: Paste your WhatConverts tracking code

```javascript
<!-- WhatConverts Tracking Code -->
<script type="text/javascript">
var _wc = _wc || {};
_wc.account_id = 'YOUR_ACCOUNT_ID';
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

6. **Save** and **Republish** the page

#### 2.2 Add Hidden Fields to Your Form
This captures Google Ads data automatically:

1. In Unbounce page builder, click on your form
2. Add these hidden fields:
   - **Field Name**: `gclid` → **Parameter**: `gclid`
   - **Field Name**: `utm_source` → **Parameter**: `utm_source`
   - **Field Name**: `utm_medium` → **Parameter**: `utm_medium`
   - **Field Name**: `utm_campaign` → **Parameter**: `utm_campaign`

These will auto-populate when visitors come from Google Ads.

### Phase 3: Phone Call Tracking Setup (30 minutes)

#### 3.1 Purchase Tracking Numbers
Since your phone number is at the top of the page:

1. In WhatConverts, go to **Tracking Numbers**
2. Click **Add Tracking Numbers**
3. Purchase numbers based on traffic:
   - **Low traffic** (<1000 visits/month): 5-10 numbers
   - **Medium traffic** (1000-5000): 15-25 numbers
   - **High traffic** (>5000): 30-50 numbers
4. Choose local or toll-free based on your business

#### 3.2 Configure Dynamic Number Insertion (DNI)
1. Go to **Call Tracking > Swap Targets**
2. Click **Add New Swap Target**
3. Enter your current phone number exactly as it appears on the page
4. Configure swap settings:
   - **Swap When**: Visitor has GCLID parameter (for Google Ads only)
   - **Number Pool**: Select your purchased numbers
   - **Session Duration**: 30 minutes (default)

#### 3.3 Set Call Forwarding
1. In **Call Tracking Settings**:
   - **Forward To**: Your business phone number
   - **Record Calls**: Yes (if legal in your area)
   - **Whisper Message**: "Lead from Google Ads" (optional)

### Phase 4: Google Ads Integration (20 minutes)

#### 4.1 Connect Your Google Ads Account
1. In WhatConverts, go to **Integrations > Google Ads**
2. Click **Connect Account**
3. Authenticate and select your Google Ads account
4. Grant required permissions

#### 4.2 Create Single Conversion Action
Since you want one conversion action for all campaigns:

1. In Google Ads, create ONE offline conversion:
   - **Name**: "WhatConverts - All Conversions"
   - **Category**: "Lead"
   - **Value**: Use different values (optional) or "Don't use value"
   - **Count**: "Every"
   - **Attribution**: 30-day click, 1-day view

2. In WhatConverts **Google Ads Settings**:
   - **Import Method**: "Import into existing conversion"
   - **Select Conversion**: Choose your created conversion
   - **Import**: Both calls and forms

### Phase 5: Testing Protocol (20 minutes)

#### 5.1 Test Each Variant
For EACH of your 3 variants:

1. Create test URL:
   ```
   https://your-page.unbounce.com/variant-a/?gclid=TEST123&utm_source=google&utm_medium=cpc&utm_campaign=test
   ```

2. Verify:
   - Phone number swaps to tracking number
   - Form hidden fields populate
   - Submit test form with identifiable data

3. Check WhatConverts dashboard:
   - Lead appears within 1 minute
   - GCLID is captured
   - UTM parameters are recorded

#### 5.2 Test Call Tracking
1. Call the swapped number
2. Verify in WhatConverts:
   - Call appears in dashboard
   - Recording works (if enabled)
   - Correct attribution to test GCLID

### Phase 6: Launch Checklist

Before going live:
- [ ] All 3 variants have tracking code
- [ ] Form captures GCLID on all variants
- [ ] Phone numbers swap correctly
- [ ] Test conversions appear in WhatConverts
- [ ] Google Ads integration is active
- [ ] Set up email notifications for new leads

### Ongoing Monitoring

#### Daily (First Week)
- Check WhatConverts dashboard for leads
- Verify phone number pool utilization
- Confirm Google Ads is receiving conversions

#### Weekly
- Review conversion data in Google Ads
- Check for any tracking errors
- Monitor number pool usage (aim for <80% utilization)

#### Monthly
- Audit conversion accuracy
- Review call recordings for quality
- Adjust number pool size if needed

## Troubleshooting Quick Fixes

### Forms Not Tracking
1. Check browser console for JavaScript errors
2. Verify WhatConverts script loads on all variants
3. Try adding `wc-track` class to form manually

### Phone Numbers Not Swapping
1. Clear browser cache and cookies
2. Verify GCLID parameter is present in URL
3. Check number pool isn't exhausted

### Conversions Not Showing in Google Ads
1. Wait 3-4 hours (normal delay)
2. Verify conversion action is active
3. Check attribution window settings

## Time Estimate
- Initial setup: 2-2.5 hours
- Testing: 30 minutes
- Total: ~3 hours

## Questions to Ask WhatConverts Support
If you need clarification:
1. "How do I ensure tracking works across all Unbounce variants?"
2. "What's the best number pool size for [your traffic volume]?"
3. "How can I test without affecting real conversion data?"

---

**Next Step**: Start with Phase 1 and work through systematically. Let me know when you hit any snags!