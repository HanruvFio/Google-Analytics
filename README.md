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

## Reports
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
