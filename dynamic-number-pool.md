# Setting Up Dynamic Number Pool for All Traffic - WhatConverts

## Overview

WhatConverts uses a pool of telephone numbers, called a dynamic number pool, that are dynamically assigned and recycled to different users. You can set up a dynamic number pool to capture:

- All traffic
- Only organic traffic
- Traffic from a specific source and medium

Each of these methods will capture data from each visit that includes the source and medium for the marketing channel it came from, where on the site each visitor landed, and what page ultimately converted each visitor into a lead.

This article will show you how to set up a dynamic number pool to capture all traffic, organic traffic, and source-specific traffic. For most users and situations, we recommend setting up an all traffic number pool.

## Setup Instructions

### Initial Setup Steps

1. In your WhatConverts profile, select "Tracking" from the top menu
2. Select "Calls", then "Phone Numbers"
3. Click "+ Add Dynamic Pool"
4. Select "Advanced Setup"
5. Enter the phone number that you would like to swap on your website (This is the phone number that is currently static on your site)

## To Track All Traffic

### Step 1: Configure Traffic Source
- Under "What's the traffic source to be assigned to this number pool?", select "All Traffic"
- Click "Next Step"

### Step 2: Choose Numbers
- Follow the guide to determine how many numbers you'll need for your website
- Choose the country, phone number type (local or toll free) and area code
- Click "Find Numbers"
- Review the numbers and click "Next Step"

### Step 3: Set Destination
- Enter the destination number (the number of the phone you will actually be answering) to which your tracking calls should be forwarded
- Click "Next Step"
- The next few prompts will guide you through setting up these tracking numbers to ensure you have all the features that you want for your call tracking needs
- Once you are satisfied with the settings you've chosen, click "Finish"

### Step 4: Test Implementation
1. Open a new browser session and input your site's URL, adding the following to the end:
   ```
   ?gclid=test&utm_keyword=testkeyword&wc_clear=true
   ```
   
   The test URL should look like this:
   ```
   http://www.YOURWEBSITE.com/?gclid=test&utm_keyword=testkeyword&wc_clear=true
   ```

2. The telephone number you see on the site should now be one of your tracking numbers instead of your normal static phone number
3. Call the phone number, then navigate to the Lead Manager within your WhatConverts account
4. In your WhatConverts Lead Manager, check the newest phone call lead
5. You should see a new phone call lead from Google CPC with the keyword "testkeyword"

## To Track Organic Traffic

### Step 1: Configure Traffic Source
- Under "What's the traffic source to be assigned to this number pool?", select "Search"
- Under "Visitors from," select "All"
- Under "for," select "Organic"
- Click "Next Step"

### Step 2: Choose Numbers
- Follow the guide to determine how many numbers you'll need for your website
- Choose the country, phone number type (local or toll free) and area code
- Click "Find Numbers"
- Review the numbers and click "Next Step"

### Step 3: Set Destination
- Enter the destination number (the number of the phone you will actually be answering) to which your tracking calls should be forwarded
- Click "Next Step"
- The next few prompts will guide you through setting up these tracking numbers to ensure you have all the features that you want for your call tracking needs
- Once you are satisfied with the settings you've chosen, click "Finish"

### Step 4: Test Implementation
1. Open a new browser session and input your site's URL, adding the following to the end:
   ```
   ?utm_source=google&utm_medium=organic&wc_clear=true
   ```
   
   The test URL should look like this:
   ```
   http://www.YOURWEBSITE.com/?utm_source=google&utm_medium=organic&wc_clear=true
   ```

2. The telephone number you see on the site should now be one of your tracking numbers instead of your normal static phone number
3. Call the phone number, then navigate to the Lead Manager within your WhatConverts account
4. In your WhatConverts Lead Manager, check the newest phone call lead
5. You should see a new phone call lead from Google organic

## To Track Traffic from a Specific Source and Medium

### Step 1: Configure Traffic Source
- Under "What's the traffic source to be assigned to this number pool?", select "Source and Medium"
- Enter the source and medium exactly as they appear in your URL (campaign, content, and keyword settings are optional)
- **Note:** UTM parameters are case sensitive
- Click "Next Step"

### Step 2: Choose Numbers
- Follow the guide to determine how many numbers you'll need for your website
- Choose the country, phone number type (local or toll free) and area code
- Click "Find Numbers"
- Review the numbers and click "Next Step"

### Step 3: Set Destination
- Enter the destination number (the number of the phone you will actually be answering) to which your tracking calls should be forwarded
- Click "Next Step"
- The next few prompts will guide you through setting up these tracking numbers to ensure you have all the features that you want for your call tracking needs
- Once you are satisfied with the settings you've chosen, click "Finish"

### Step 4: Test Implementation
1. Open a new browser session and input your site's address, adding your UTM source and medium to the end of the URL to simulate a click from your chosen source
2. Use the following URL format, replacing YOURWEBSITE, SOURCE, and MEDIUM with your own site, source, and medium:
   ```
   http://www.YOURWEBSITE.com/?utm_source=SOURCE&utm_medium=MEDIUM&wc_clear=true
   ```

3. The telephone number you see on the site should now be one of your tracking numbers instead of your normal static phone number
4. Call the phone number, then navigate to the Lead Manager within your WhatConverts account
5. In your WhatConverts Lead Manager, check the newest phone call lead
6. You should see a new phone call lead from your chosen source and medium

## Support

If you have any questions, please [contact WhatConverts Support](https://www.whatconverts.com/contact/) or email [support@whatconverts.com](mailto:support@whatconverts.com).

## Get a FREE Presentation of WhatConverts

One of our marketing experts will give you a full presentation of how WhatConverts can help you grow your business.

[Schedule a Demo](https://www.whatconverts.com/request-a-demo/lets-talk)