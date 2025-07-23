# Troubleshooting Call Tracking Setup - WhatConverts

If you're having trouble setting up call tracking, first check the following troubleshooting steps. If you're still having issues, [contact WhatConverts support](https://www.whatconverts.com/contact) for individual assistance.

## 1. Ensure Tracking Code Is Installed

It is important that you make sure the tracking code has been added to every page of your website. To find if the tracking code is on your page follow these steps:

### Step 1: Check Page Source
1. Open your website in a browser of your choice
2. Right click your mouse and select "View page source"
3. Press `CTRL+F` on your keyboard to open the search feature
4. Enter your unique profile ID (which can be found by navigating to the "Tracking" menu in WhatConverts and selecting "Tracking Code")

### Step 2: Verify Tracking Code
This should take you to the tracking code within the page source and should look something like this (asterisks represent your unique profile ID):

```html
<script type="text/javascript" src="//s.ksrndkehqnwntyxlhgto.com/*****.js?ver=6.4.3" id="whatconverts-tracking-script-js"></script>
```

### Step 3: Check Google Tag Manager (if applicable)
**Note:** If you have installed your [WhatConverts Tracking Code in Google Tag Manager](https://www.whatconverts.com/help/docs/integrations/google-tag-manager/), you will need to check to make sure the GTM snippet is on your site and inside the GTM container for your tracking code using the steps above as well.

### Step 4: Install if Missing
If you do not find the tracking code on your website, you will need to add it. Full instructions on installing your WhatConverts Tracking Code can be found here: [Adding WhatConverts Script to Your Site](https://www.whatconverts.com/help/docs/getting-started/step-by-step-setup-guide/adding-whatconverts-script-to-your-site/).

---

## 2. Clear Cookies

You can [simulate a Google Ads click](https://www.whatconverts.com/help/docs/integrations/google-ads/testing-your-tracking-number-simulate-a-google-ads-click/) and clear your cookies by appending the following to the end of your URL:

```
?wc_clear=true&gclid=test
```

### Example:
```
http://www.YOURWEBSITE.com/?wc_clear=true&gclid=test
```

### What This Does:
- Adding `?wc_clear=true` to the end of your URL clears the current attribution from WhatConverts tracking cookie
- `gclid=test` simulates a Google Ads click

For full instructions on clearing the cookies in your browser see: [How to Clear your Cookies to Test Your Number Swapping](https://www.whatconverts.com/help/docs/faq/how-to-clear-your-cookies-to-test-your-number-swapping/)

---

## 3. Add and Verify Swap Number

### What is a Swap Number?
The swap number is the phone number that's hard-coded (or static) on a website. It is typically the main business number.

The swap number will be dynamically switched out with the tracking number when a visitor arrives on your website. Which users see each tracking number is determined by how your phone numbers are set up in your WhatConverts profile.

### How to Review/Edit Your Swap Number

1. Log into the WhatConverts profile you would like to review
2. Click "Tracking" in the top menu
3. Click "Phone Calls" and select "Phone Numbers"

#### For Dynamic Number Pool:
If you are using a Dynamic Number Pool to track your calls, you can find your swap number by [Editing the Dynamic Number Pool](https://www.whatconverts.com/help/docs/faq/how-do-i-review-my-dynamic-number-pool-settings/).

#### For Single Static Number:
If you are using a single static number marketing source, click the Edit Number button (pencil icon) in the row with your phone number. Edit the Swap Number in the Static Number module.

### Important Note:
**Make sure your swap number does not include any punctuation (such as hyphens or parenthesis).**

Once your changes have been made, click "Finish".

---

## 4. Test Tracking Numbers

### Testing Process:
1. In an incognito window, visit your website via the traffic source you've set up your tracking numbers to swap for
2. Call the tracking number you see on the page
3. Go back to your WhatConverts profile
4. Click "Leads" in the top menu
5. In the Lead Manager, review your test call

### Testing Different Traffic Sources:

#### To simulate a Google Ads click:
Add the following to the end of your URL:
```
?gclid=test&wc_clear=true
```

#### To simulate a Google Organic visit:
Add the following to the end of your URL:
```
?utm_source=google&utm_medium=organic&wc_clear=true
```

#### To clear your prior WhatConverts attribution and track your click as a Direct visit:
Add the following to the end of your URL:
```
?wc_clear=true
```

### Expected Results:
The following example is from a simulated Google Ads click - you should see similar attribution data in your Lead Manager for your test call.

---

## Support

If you have any questions, please [contact WhatConverts Support](https://www.whatconverts.com/contact) or email [support@whatconverts.com](mailto:support@whatconverts.com)

## Get a FREE Presentation of WhatConverts

One of our marketing experts will give you a full presentation of how WhatConverts can help you grow your business.

[Schedule a Demo](https://www.whatconverts.com/request-a-demo/lets-talk)