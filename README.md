# Google-Analytics

## Add Chrome Plugins
https://chromewebstore.google.com/detail/analytics-debugger/ilnpmccnfdjdjjikgkefkcegefikecdc?hl=en&pli=1
   * In the debugging console you can now see what tags are firing on a site
https://chromewebstore.google.com/detail/omnibug/bknpehncffejahipecakbfkomebjmokl?hl=en
   * Will tell events that fire for the tags

## Adding A website

### Log into fio analytics account

### Add a Property

### Insert the tag on the site

1. Create a data stream
   a. In Analytics > Admin > Data Streams > Complete website details, make usre enhanced measurement is enabled

2. Add the tag to the website
   a. Wordpress > Plugin
   b. Webflow > Site settings > Integration

NB: Go to the admin panel > Events > Make sure the form submit is a key event for tracking its metrics

## UTMs (A way to understand where users come from)
  * Bold part is the UTM String, they are alwyas lowercase with no spaces in between
<img width="613" height="40" alt="image" src="https://github.com/user-attachments/assets/e0b45363-5003-4ded-a28b-9dae60a10acf" />

  * Analytics can provide information on where a page has been accessed from
<img width="905" height="248" alt="image" src="https://github.com/user-attachments/assets/6498d4eb-84ff-4de6-a608-30e74f7e06c0" />

### UTM Types:
  * You have a facebook post, and you have a facebook ad (these 2 are different types of content from a single source facebook)
    * UTM Source: This identifies the platform or "referrer" where the traffic originated. Since both examples are on Facebook, the source remains the same.
      * **Value:** facebook
      * **Purpose:** To show that the traffic came from Facebook rather than Google, LinkedIn, or an email list.
    * UTM Medium: This is the most important field for your specific example. It identifies the type of traffic or the high-level channel. This is where you distinguish between "free" and "paid."
      * **For the Facebook Post:** social (or organic)
      * **For the Facebook Ad:** cpc (Cost Per Click) or paid
      * **Purpose:** To help you see if your paid marketing is performing better than your free social media efforts.
    * UTM Campaign: This identifies the specific effort or promotion. This is usually a name you invent to group your links together.
      * **For the Facebook Post:** spring_sale_announcement
      * **For the Facebook Ad:** spring_sale_retargeting
      * **Purpose:** To track the success of a specific marketing initiative across different channels.
    * UTM Term: This is primarily used to identify who you are targeting or what they searched for.
      * **For the Facebook Post:** You typically leave this blank, or use it to note a specific interest group (e.g., organic_followers).
      * **For the Facebook Ad:** You use this for your specific audience target (e.g., past_purchasers or fitness_interests).
      * **Purpose:** Traditionally used for paid search keywords, but on social media, it’s used for audience identification.
    * UTM Content: This is used to identify the specific version of a link or ad to see which one performs better (A/B testing).
      * **For the Facebook Post:** If you post a link in the text and the same link in a comment, you could use text_link vs. comment_link.
      * **For the Facebook Ad:** You use this to distinguish between different visuals, such as blue_banner vs. lifestyle_video.
      * **Purpose:** To differentiate between multiple links or creative variations that lead to the same URL.
     
#### Example 1: wwww.beautifulplates.com/shop/**utm_source=facebook&utm_medium=organic&utm_campaign=spring_sale**
  * Source: Facebook
  * Medium: Organic (Normal traffic from a social post)
  * Campaign: Spring Sale

#### Example 2: wwww.beautifulplates.com/shop/**utm_source=instagram&utm_medium=cpc&utm_campaign=adset_4**
  * Source: Instagram
  * Medium: CPC (cost per click, paid add campagn)
  * Campaign: adset_4

#### Example 3: wwww.beautifulplates.com/shop/**utm_source=mailchimp&utm_medium=email&utm_campaign=weekly_newsletter**
  * Source: Mailchimp
  * Medium: email
  * Campaign: weekly_newsletter

### Setup
1. Use this template - **Make a copy to respective client folder**: https://docs.google.com/spreadsheets/d/12GcdYo6s8ZCAe27S81OFpQU3JQLgANz0/edit?usp=drive_link&ouid=102891394710966900821&rtpof=true&sd=true
UTM Campagn Builder Tool: https://ga-dev-tools.google/campaign-url-builder/

## Report Dimentions and Metrics
### Dimentions (Y axis)

1. Page Title: The specific name of the page as defined by the <title> HTML tag.

2. Page Path + Query String: The part of the URL after the domain (e.g., /products?id=123).

3. Hostname: The main domain where your tracking code is running (e.g., www.yoursite.com).

4. Landing Page + Query String: The very first page a user arrived at when they started their session.

5. Session Source: Where your traffic came from specifically (e.g., google, newsletter, or facebook).

6. Session Medium: The broad category of the source (e.g., organic, cpc for ads, or email).

7. Session Campaign: The specific marketing effort or promotion name tied to the visit.

8. Session Manual Ad Content: The specific link or ad version clicked (often used in A/B testing).

9. Event Name: The specific action a user took (e.g., page_view, file_download, or click).

10. Device Category: The type of hardware the visitor used (e.g., desktop, mobile, or tablet).

### Metrics (X axis)

1. Users: The total number of unique people who visited your site.

2. Sessions: The total number of visits (one user can have multiple sessions).

3. Views: The total number of times a screen or page was loaded.

4. Bounce Rate: The percentage of sessions that were not engaged (usually sessions lasting < 10 seconds).

5. Engagement Rate: The opposite of bounce rate; the percentage of sessions that were meaningful/active.

6. Average Engagement Time: The average amount of time the site was actually in the foreground of the user's screen.

7. Views Per Session: The average number of pages a person looked at during a single visit.

8. Event Count: The total number of times any "Event" was triggered.

9 Key Events: The total number of times an action you've marked as "important" (formerly "Conversions") occurred.

## Most commonly used reports

1. **Acquisitions > User Acquisition:** This report focuses on Discovery. It tells you how people found your website for the very first time in their lives.
  * First User Primary Channel Group: The broad category of that first visit.
    * Direct: They typed your URL into the browser or used a bookmark.
    * Referral: They clicked a link on another website (a "backlink") to get to you.
  * First User Medium
2. **Acquisitions > Traffic Acquisition:** This report focuses on Sessions. It tells you where a user came from for their current visit, even if they've visited before.
  * First User Primary Channel Group
    * Direct: When People Endter the address in the address bar
    * Referral: Someone else liked to the website (Backlink)
  * First User Medium: First User Medium: The specific "type" of that first contact, such as organic, cpc (paid ads), or email.
3. **Engagements > Events:** You can see which event got fired how many times
4. **Engagements> Pages and Screens** : Gives info per page of a site and metrics
5. **Landing Page:** Which pages are mostly used when people enter the site
    * If you want to know where people are coming from to that page you can select plus icon next to landing page and search for session source.
6. **User > Tech > Tech Details:** Help see what devices users use most when interacting with the site.

#Building A dashboard for clients

## **GA4 Custom Report: Client Acquisition & Campaign Performance**

This guide outlines how to build a high-clarity report in Google Analytics 4 to track marketing campaigns, website traffic, and form submissions without the clutter of standard reports.

### 1. Create the Custom Detail Report
1. Log in to **Google Analytics 4**.
2. Navigate to **Reports** > **Library** (located at the bottom of the left-hand menu).
3. Click **Create new report** and select **Create detail report**.
4. Choose **Traffic acquisition** as the starting template to utilize its session-based logic.

### 2. Customize Dimensions (Rows)
*To keep the report focused on where users come from and where they arrive.*
1. In the **Report customization** panel on the right, click **Dimensions**.
2. **Remove** all existing dimensions except:
    * `Session source / medium` (This shows your UTM Source and Medium).
    * `Session campaign` (This shows your specific UTM Campaign name).
3. Click **Add dimension** and search for:
    * `Landing page` (To see exactly which page they landed on).
4. Set `Session source / medium` as the **Primary dimension** (indicated by the checkmark).
5. Click **Apply**.

### 3. Customize Metrics (Columns)
*To remove "noise" and focus on success indicators.*
1. Click **Metrics** in the right-hand panel.
2. **Remove** all existing metrics except:
    * `Sessions` (Total visits).
    * `Engaged sessions` (High-quality visits).
3. Click **Add metric** and search for:
    * `Key events` (This replaces 'Conversions' and shows form submits).
4. Click **Apply**.

### 4. Finalize Visuals & Save
1. (Optional) If you want a table-only view for the client, click the **eye icon** next to the Charts (Bar chart and Line chart) to hide them.
2. Click **Save**.
3. **Report Name:** `Monthly Client Performance Report`.
4. Click **Save** again.

### 5. Add to Side Menu (Publishing)
*Your report will not appear in the left menu until it is added to a collection.*
1. Go back to the **Library**.
2. Find the **Life cycle** or **Business objectives** collection and click **Edit collection**.
3. Search for your new `Monthly Client Performance Report` in the right-hand list.
4. **Drag and drop** it into the "Acquisition" or "Engagement" folder on the left.
5. Click **Save** > **Save changes to current collection**.

### 6. How to Use the Report
* **Comparing Sources:** The report automatically lists all sources (e.g., `google / organic`, `linkedin.com / referral`, and your custom `linkedin-post / organic`).
* **Drill Down:** Click the **blue "+" icon** next to `Session source / medium` in the table to add `Landing page` as a second column.
* **Filter by Date:** Use the date picker in the top right to compare Day, Week, Month, or Year.

  
## **Client Report Collection**
1. Acquisitions > Overview
  - Active And New Users Card
  - New Users by firts user primary channel group
  - Sessions by sessions primary channel group
2. Engagement Overview
  - Views by Page title and screen class
3. Monthly Client Performance Report
 
