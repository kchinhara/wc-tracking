https://www.whatconverts.com/help/docs/lead-tracking/form-tracking/form-tracking-with-unbounce/

# Unbounce Form Tracking

## Prerequisites

Before integrating your Unbounce forms to begin tracking in WhatConverts, make sure to add your WhatConverts tracking code to each landing page and light box. For detailed instructions: [Call Tracking for Unbounce](https://www.whatconverts.com/help/docs/integrations/unbounce-integration/call-tracking-for-unbounce/)

## Setup Instructions

### Step 1: Extract Form Action Element
Go to the page your form is located on. Right click your form and find `<form action ="` (this will begin with "/fsg?pageID=)"). Copy the action element into a notepad document.

### Step 2: Find Submit Button ID
Right-click the submit button and click "Inspect".

### Step 3: Copy Button ID
Copy the ID of the button. It will be similar to "lp-pom-button-##". Paste that into your notepad.

### Step 4: Access WhatConverts Dashboard
Log into the WhatConverts profile you want to track your Unbounce form(s) in. Select "Tracking" from the top menu. Select "Forms" and click "Web Forms".

### Step 5: Add Web Form
1. Click the "Add Web Form" button, and select "Manual Setup"
2. Name your form
3. Select Attribute Type "Action" and paste Attribute Value from Step 1
4. Click "Yes" under "Is there an alternate Submit Button?"
5. Select the Attribute Type of "ID" then paste the value copied in Step 2
6. Click the "Finish" button

**Important:** Repeat these steps for each variant of your form.

### Step 6: Test Form Tracking
1. Test your form tracking by filling in the form on your Unbounce page to submit a test lead
2. Go back to your WhatConverts Profile
3. Click "Leads" in the top menu
4. Under the Lead Manager review your test form submission

## Support

If you have any questions, please [contact WhatConverts Support](https://www.whatconverts.com/contact) or email [support@whatconverts.com](mailto:support@whatconverts.com)

## Get a FREE presentation of WhatConverts

One of our marketing experts will give you a full presentation of how WhatConverts can help you grow your business.

[Schedule a Demo](https://www.whatconverts.com/request-a-demo/lets-talk)