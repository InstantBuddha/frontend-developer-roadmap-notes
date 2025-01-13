# 02 HTML

- [02 HTML](#02-html)
  - [Semantic html](#semantic-html)
  - [SEO](#seo)
    - [How pages are ranked?](#how-pages-are-ranked)
    - [Keywords](#keywords)
    - [Search intent](#search-intent)
    - [How to find keywords](#how-to-find-keywords)
      - [Generate keyword ideas](#generate-keyword-ideas)
      - [Understanding ranking difficulty](#understanding-ranking-difficulty)
    - [On-page SEO](#on-page-seo)
      - [How to optimize a page for a search keyword?](#how-to-optimize-a-page-for-a-search-keyword)
    - [Link building (backlinks)](#link-building-backlinks)
      - [Link building techniques](#link-building-techniques)
      - [How to do blogger outreach for backlinks](#how-to-do-blogger-outreach-for-backlinks)
    - [Technical SEO](#technical-seo)
      - [robots.txt](#robotstxt)
        - [Further info:](#further-info)
        - [robots.txt vs. sensitive pages](#robotstxt-vs-sensitive-pages)
      - [Sitemaps](#sitemaps)
      - [Redirects](#redirects)
      - [Canonical tag](#canonical-tag)


## Semantic html

Semantic HTML refers to the use of HTML markup to reinforce the meaning of web content, rather than merely defining its appearance. It involves using HTML elements that clearly describe their purpose and content. Semantic HTML improves accessibility, SEO, and code readability. Key elements include `<header>, <nav>, <main>, <article>, <section>, <aside>, and <footer>. It also encompasses using appropriate heading levels (<h1> to <h6>), lists (<ul>, <ol>,<li>), and data tables (<table>, <th>, <td>).` Semantic HTML helps screen readers interpret page content, enables better browser rendering, and provides clearer structure for developers. By using semantically correct elements, developers create more meaningful, accessible, and maintainable web documents that are easier for both humans and machines to understand and process.

[A good summary](https://cs.fyi/guide/writing-semantic-html) where I learned about semantic HTML tags, and how they can be used to make your web pages more accessible and easier to understand. You also learned about some of the most commonly used semantic tags, including `<header>, <nav>, <main>, <article>, <aside>, <section>, <footer>, <details>, <summary>, <figure>, <figcaption>, <mark>, <time>, and <progress>. `

![Layout image](https://www.w3schools.com/html/img_sem_elements.gif)

## SEO

[Notes for this video](https://www.youtube.com/watch?v=xsVTqzratPs)

Seo is important because it gives constant inflow of users unlike marketing camopaigns.

### How pages are ranked?

1. Backlinks: how many sites link to your site (especially prominent ones).
2. Search intent: you should try to rank high on relevant keywords
3. Content depth: is your content useful? It is NOT the same as being long.

### Keywords

1. First you should choose relevant keywords for your content. (Things that people might Google)
2. Search demand/volume: how maThe number of times a specific keyword or search query is entered into a search engine within a given timeframe, typically a month.
3. Traffic potential: The estimated amount of organic traffic a website could receive if it ranks for a particular keyword or group of keywords.
   - It is best to decide which words are relevant to your business.
4. Search intent: if you have a recipe site don't want to be high on the "buy oven" search results because there the intent is different.
5. Understanding ranking difficulty: how easy to get to the top of the ranking? Is it worth the value to make the effort?

### Search intent

Why do people do their search?

1. Google the keyword and see the top results: this gives you an idea what people get or want when they search this.
  - The 3 Cs of search intent:
    1. Content type: Blog posts, videos, product pages, category pages, landing pages
    2. Content format: How to guides, tutorials, List posts, Opinion editorials, tools, calculators
    3. Content angle: Here are some examples of content angles for common topics:
      - Topic 1: What is Stoicism?
        - Beginner's Angle: "Stoicism Explained: A Beginner’s Guide to Ancient Wisdom"
        - Practical Angle: "5 Stoic Practices to Stay Calm in a Chaotic World"
        - Academic Angle: "The Influence of Stoicism on Modern Philosophy"
        - Local/Cultural Angle: "How Stoicism Can Be Applied to Modern Hungarian Society"
      - Topic 2: Introduction to Philosophy
        - Inspirational Angle: "How Philosophy Can Change the Way You See the World"
        - Practical Angle: "Why Studying Philosophy Is the Best Decision for Your Career"
        - Accessible Angle: "Philosophy for Everyone: How to Start Thinking Like a Philosopher"

### How to find keywords

1. step 1: generate keyword ideas
   - Search keyword tools: for search volume, difficulty scores and SEO metrics, discover potential topics to go after (for example they have aHrefs keyword explorer)
2. step 2: check if they are worth going after

#### Generate keyword ideas

1. broad keywords: add seeds to keywords explorer like: golf balls, golf clubs, golf hats.
2. go to phrase match and check the more specific ideas of keywords
3. choose keywords based on the following:
   - search demand: check with the search volume filter (for example with higher than 300 mothly searches)
   - traffic potential: more important than demand because this results in clicks and traffic. For the keywords we need to see the top ranking pages and see how much traffic they get. (it can be done with the SERP button next to the keyword)
   - business potential: the value a keyword has to my business. Is the keyword relevant to us?
   - match search intent: if the keyword's top ranking pages are ecommerce pages it might not be a good idea to invest work in this keyword if we are a blog.
   - how hard to rank top at Google
4. Keyword modifiers: for example if the base keyword is "golf hats", we can modify it by adding "best", "top", "review" or the current year.
5. How to find new keywords that you have not checked? 
  - check what keywords drive the most traffic to your competitors (not necessary business competitors, but search competitors: websites that rank for keywords that you don't, but would want to)
    - To do this, click on your keyword list, 
    - then check the "traffic share by domain report"
    - then check the competitor's top ranking page list
    - by reading this list, you can get good ideas

#### Understanding ranking difficulty

Before targetting the keyword, you need to understand how hard it would be to beat the competition

Three things to consider here:
1. search intent: go through the 3Cs of search intent. Furhermore,
   - if the top pages include the primary keyword or a variation of it in the title and or the url, they target the keyword 
2. Metrics of the top ranking pages
   - check the number of websites that are linking to the page (referring domains) and the quality of these:
     - can I get more quality referring domains? 
3. topical authority of top ranking sites (domain rating)
   - you should target keywords where your website's dr is similar to the top ranking pages
   - check for keywords in the domain name: it is important
   - check for basic information about what topics the site is about

| Question - the more is true the more chance you have                                 | Yes | No  |
| ------------------------------------------------------------------------------------ | --- | --- |
| Do some of the top-ranking pages fail to closely match search intent?                | ✅   |     |
| Can I get more QUALITY backlinks than the top-ranking pages?                         | ✅   |     |
| Is my website in a similar DR range OR higher than the top-ranking websites?         | ✅   |     |
| Is my website equally or MORE topically authoritative than the top-ranking websites? | ✅   |     |

### On-page SEO

Optimizing pages for search intent --> better ranking. This includes optimizing HTML tags like titles and meta descriptions.

It is NOT about (these are just to mess up user experience):
  - Not about stuffing exact match keywords (it was common earlier but it does not work now)
  - Not about using the keywords many times
  - Not about meeting minimum word count

**What is On-page SEO?**
Optimizing web pages to rank higher in search engines.
The goal of your pages should be to **satisfy the searcher's intent**.
Address these: Content type, Content format, Content angle because you want people to se what they expect to see
For this, improve: Titles, Subheadings, Internal linking, Readability, the content.

#### How to optimize a page for a search keyword?

Actually not only the most important keywords bring traffic but others too. 
To potimize for many keywords:
  1. optimize the page to rank (satisfy searcher intent)
    - optimize content: learn from your competitors: you might even copy the page layout and the way information is organized (to stay mediocre as I see it)
    - content gap analysis: use an SEO tool to find keywords that the top pages are ranking for and you aren't
       - Content Gap Analysis is the process of identifying gaps in the content on your website compared to what your target audience is searching for and what your competitors are offering. By addressing these gaps, you can create content that better meets user intent, improve your site's search rankings, and attract more organic traffic. 
       - It might even be interesting to see what keywords the users look for to learn about the language they use or what they are interested in.
    - Technical On-Page SEO Optimizations: Although the content is the most important, there are other useful things to do:
      - Include the keyword in your title WHEN it makes sense. (or alternatives for the main keyword, maybe with an angle)
      - Use short and descriptive url slug (preferably including the keywords)
        **Subfolders can be used to describe subtopics**, such as url/health/pregnancy/slug-for-keywords
      - Meta description: in the HTML you can summarize the page (they might not be used as a ranking signal, but might influence click through rates)
      - Add internal links to and from your pages: super powerful, because they can pass link authority to other relevant pages and they help search engines to understand page content.
      - Optimize images: even images might bring traffic
        1. Name the image file appropriately
        2. Use descriptive alt text (but avoid stuffing too many keywords)
        3. Compress images --> faster load times (shortpixel can be used)
      - Optimize readability (the Hemingway app can be used)
        - Short sentences
        - Descriptive subheadings
        - Large enough font
        - Avoid using big words
        - Use everyday language
      - Others:
        - Open graph meta tags 
          - for example: 
            ```html
            <head>
              <meta property="og:title" content="Discover Philosophy at Filozofia.hu" />
              <meta property="og:description" content="Join our philosophy courses and delve into timeless wisdom. Learn more about ethics, metaphysics, and more." />
              <meta property="og:image" content="https://www.filozofia.hu/images/philosophy-class.jpg" />
              <meta property="og:url" content="https://www.filozofia.hu/courses" />
              <meta property="og:type" content="website" />
              <meta property="og:site_name" content="Filozofia.hu" />
            </head>
            ```
        - Schema markup
          - Schema Markup (or structured data) is a form of microdata added to a webpage's HTML code to provide search engines with more detailed information about the content on that page. It uses a standardized vocabulary defined by Schema.org.
          - It seems to be useful to add extra information and searchability.
          - An example of using React with React Helmet for a page that lists books as products:
            ```javascript
            import React from "react";
            import { Helmet } from "react-helmet";

            const BooksPage = () => {
              const books = [
                {
                  name: "Philosophy 101",
                  description: "An introduction to the fundamentals of philosophy.",
                  price: "19.99",
                  currency: "USD",
                  isbn: "1234567890123",
                  author: "John Doe",
                },
                {
                  name: "Ethics and Morality",
                  description: "Exploring ethical theories and their applications.",
                  price: "25.50",
                  currency: "USD",
                  isbn: "9784567890123",
                  author: "Jane Smith",
                },
              ];

              const structuredData = {
                "@context": "https://schema.org",
                "@type": "ItemList",
                "itemListElement": books.map((book, index) => ({
                  "@type": "ListItem",
                  "position": index + 1,
                  "item": {
                    "@type": "Product",
                    "name": book.name,
                    "description": book.description,
                    "offers": {
                      "@type": "Offer",
                      "price": book.price,
                      "priceCurrency": book.currency,
                    },
                    "isbn": book.isbn,
                    "author": {
                      "@type": "Person",
                      "name": book.author,
                    },
                  },
                })),
              };

              return (
                <div>
                  <Helmet>
                    <script type="application/ld+json">
                      {JSON.stringify(structuredData)}
                    </script>
                  </Helmet>
                  <h1>Books</h1>
                  <ul>
                    {books.map((book, index) => (
                      <li key={index}>
                        <h2>{book.name}</h2>
                        <p>{book.description}</p>
                        <p>Price: {book.price} {book.currency}</p>
                        <p>Author: {book.author}</p>
                      </li>
                    ))}
                  </ul>
                </div>
              );
            };

            export default BooksPage;            
            ``` 
  2. backlinks

### Link building (backlinks)

Getting other websites to link to your page

In most cases it is only about emailing to complete strangers and asking them to link to you.

It is like networking in reality. Mostly building relationships with relevant site owners to enhance both of your pages.

It is especially useful for **comptetitive phrases** the keywords that drive the most traffic and revenue to your business.

The 3 main building strategies for getting backlinks:
- create them: on other sites like social media (not too effective)
- buy them: not the best, and expensive (effective unless you get caught)
- earn them: 
  - email website owners to link to you.
  - Become a source for an online publication
  - Earn backlinks organically (they do it by themselves)

Good backlinks: (unfortunately if spam sites link to you it is bad)
What makes backlinks good?
  - Relevance: sites relevant in the topic  (actually there are backlink checking tools)
  - Authoritative: if it has high page ranking (domain rating, url rating in the tools)
  - the link itself: 
    - the anchor text is useful for Google to understand what the page is good for, BUT adding a lot of keyword-rich anchor texts is called a link scheme and it is BAD
    - the rel attribute: (they handle them as hints)
      - No rel attribute: followed link: relevance can be passed
      - Nofollow: they would not associate themselves with the linked page
      - UGC user generated content
      - Sponsored
    - the link placement: if it is in a prominent place, it is more likely to be followed 
  
#### Link building techniques

1. find people based on metrics, who might be important.
2. refine your list, validate the people are important.
3. contact them.

Other solutions:
1. HARO: journalists need sources, you register, write stuff and if they like it, they will link to you.
2. Guest blogging: you create content for others and they link back to you. Good for both of you.
3. Skyscraper technique: 
   1. find content that has a lot of links
   2. create your own version, but improve it
   3. reach out for the most popular post and ask them to link to yours

#### How to do blogger outreach for backlinks

Can target kind of masses of people or individuals (shotgun method), but this might need a lot of preparatory time (sniper method).

### Technical SEO

To optimize the website to help search engines find you, understand, index your pages.

#### robots.txt 

At yourdomain.com/robots.txt
There can be several of these, so you might add an other at store.yourdomain.com/robots.txt

**There are directives:**

##### Further info:
The `robots.txt` file is a simple text file placed in the root directory of your website that tells web crawlers (e.g., search engine bots) which parts of your site they can or cannot access. It's a vital tool in SEO for controlling crawler behavior and optimizing your site’s crawl budget.

**Purpose of `robots.txt` in SEO**
1. **Crawl Control**: Restrict access to non-essential or sensitive pages (e.g., admin panels, staging areas) to save crawl budget.
2. **Prevent Duplicate Content**: Block crawlers from accessing duplicate content that could harm your site's ranking.
3. **Improve User Experience**: Ensure only valuable pages are indexed and shown to users in search results.
4. **Maintain Security**: Prevent crawlers from accessing secure or private directories.

---

**Basic Syntax of `robots.txt`**
A `robots.txt` file uses directives to communicate with crawlers. Here's the structure:

**User-Agent**
Specifies the bot to which the directive applies. Common user-agents include:
- `Googlebot` (Google’s crawler)
- `Bingbot` (Bing’s crawler)
- `*` (all bots)

**Disallow**
Blocks access to specific pages or directories.

**Allow**
Allows access to a specific page within a blocked directory (Googlebot-specific).

**Sitemap**
Specifies the location of your XML sitemap(s).

---

**Examples of Directives**

1. Block All Crawlers from the Entire Site
```plaintext
User-agent: *
Disallow: /
```

2. Allow All Crawlers Full Access
```plaintext
User-agent: *
Disallow:
```

3. Block Specific Directories or Pages
```plaintext
User-agent: *
Disallow: /admin/
Disallow: /private-data/
Disallow: /temp-page.html
```

4. Allow Specific Files in a Disallowed Directory (Googlebot Example)
```plaintext
User-agent: Googlebot
Disallow: /downloads/
Allow: /downloads/whitepaper.pdf
```

5. Block a Specific Bot
```plaintext
User-agent: BadBot
Disallow: /
```

6. Specify the Sitemap Location
```plaintext
User-agent: *
Disallow:
Sitemap: https://www.example.com/sitemap.xml
```

---

**Best Practices for `robots.txt`**
1. **Don’t Block Important Pages**: Avoid disallowing URLs you want indexed (e.g., main content pages).
2. **Use Wildcards and Dollar Signs**:
   - `*`: Matches any sequence of characters.
   - `$`: Denotes the end of a URL.
   Example:
   ```plaintext
   Disallow: /*.pdf$
   ```
3. **Test Your File**: Use Google’s [robots.txt Tester](https://www.google.com/webmasters/tools/robots-testing-tool) to ensure proper configuration.
4. **Avoid Sensitive Data Exposure**: Don’t rely solely on `robots.txt` to hide sensitive content, as the file is publicly accessible.

---

**Common Mistakes**
- **Blocking Important Resources**: Blocking CSS, JavaScript, or API endpoints can harm page rendering and SEO.
- **Incorrect Syntax**: Ensure proper directives and placement.
- **Forgetting the Sitemap**: Always include a link to your sitemap for better crawl efficiency.

##### robots.txt vs. sensitive pages

You're absolutely correct to consider the implications of adding sensitive URLs like `/login` to `robots.txt`. While `robots.txt` is useful for guiding search engine crawlers, it is publicly accessible and can inadvertently expose sensitive or private URLs to malicious actors.

**Best Practices for Handling Sensitive URLs (e.g., `/login`)**
1. **Avoid Listing Sensitive URLs in `robots.txt`**  
   Adding `/login` to `robots.txt` might prevent search engines from crawling and indexing it, but it also advertises the existence of the URL to anyone who checks the `robots.txt` file. If the page isn't meant for public use, it’s better not to mention it in `robots.txt`.

2. **Use Server-Side Authentication and Security**  
   Protect your sensitive URLs with robust security measures:
   - **Strong Authentication**: Enforce secure admin login mechanisms (e.g., multi-factor authentication, strong passwords).
   - **IP Whitelisting**: Restrict access to specific IP addresses if the URL is used internally.
   - **Rate Limiting**: Prevent brute-force attacks by limiting login attempts.
   - **CAPTCHA**: Add CAPTCHA to the login page to prevent automated attacks.

3. **Use Meta Tags or HTTP Headers**  
   Instead of using `robots.txt`, use the following directives in the login page's HTML or headers:
   - **Meta Tag**:  
     ```html
     <meta name="robots" content="noindex, nofollow">
     ```
   - **HTTP Header**:  
     ```plaintext
     X-Robots-Tag: noindex, nofollow
     ```
   These directives ensure the page isn’t indexed or followed by crawlers, but without exposing the URL in `robots.txt`.

**Key Takeaway**
The best practice is **not to list sensitive or private URLs in `robots.txt`**. Instead, rely on proper server-side security, meta directives, and HTTP headers to protect those pages and prevent them from being indexed. 

#### Sitemaps

A sitemap.xml is an XML file that provides search engines with a roadmap of your website's structure, helping them discover and index your content efficiently.

Common Mistakes to Avoid

- Including Non-200 URLs: Exclude pages with errors (e.g., 404, 500) or redirects.
- Overloading the Sitemap: Avoid listing unimportant pages (e.g., filter parameters, session IDs).
- Neglecting Mobile URLs: Ensure mobile-friendly or responsive pages are properly listed.

#### Redirects

Redirects are HTTP responses that guide users and search engines from one URL to another. They are crucial for managing URL changes, preserving SEO value, and enhancing user experience.

---

**Types of Redirects in SEO**

1. **301 Redirect (Permanent)**  
   - Signals a URL has been permanently moved to a new location.  
   - Passes nearly all SEO value (link equity) to the new URL.  
   - Best for long-term changes like domain migrations or consolidating duplicate content.

2. **302 Redirect (Temporary)**  
   - Indicates a temporary move.  
   - Search engines may not pass full SEO value to the new URL.  
   - Use for short-term changes, such as A/B testing or maintenance.

3. **307 Redirect (Temporary)**  
   - HTTP/1.1 version of a temporary redirect. Similar to 302 in function but more precise for HTTP/1.1 requests.  
   - Maintains request method (e.g., POST stays POST).

4. **Meta Refresh Redirect**  
   - Implemented via HTML `<meta>` tags, e.g., `<meta http-equiv="refresh" content="5;url=https://example.com">`.  
   - Not ideal for SEO, as they are slower and may confuse search engines.

---

**Importance of Redirects for SEO**

1. **Preserve SEO Value**: Redirects help retain link equity when URLs change.
2. **Improve User Experience**: Prevent users from encountering 404 errors.  
3. **Manage URL Changes**: Facilitate domain migrations, restructuring, or canonicalization.
4. **Fix Broken Links**: Redirect old or deleted URLs to active, relevant pages.

---

**Best Practices for SEO-Friendly Redirects**

1. **Use 301 Redirects for Permanent Changes**  
   Ensure link equity is passed to the new URL.

2. **Redirect to Relevant Pages**  
   Redirect users to the most contextually relevant page, not just the homepage, to preserve user intent.

3. **Avoid Redirect Chains and Loops**  
   - **Redirect Chains**: Multiple redirects in sequence (A → B → C) slow down crawling.  
   - **Redirect Loops**: URLs redirect back to themselves or cause an endless loop.

4. **Monitor Redirects**  
   Regularly audit redirects with tools like Google Search Console or Screaming Frog to identify issues.

5. **Update Internal Links**  
   Replace old URLs with updated ones in internal links to reduce reliance on redirects.

6. **Use Canonical Tags Alongside Redirects**  
   If duplicate content exists, use canonical tags to indicate the preferred URL.

---

**Common Redirect Use Cases in SEO**

- **Domain Migrations**:  
  Redirect `http://example.com` → `https://www.example.com`.

- **URL Structure Changes**:  
  Redirect `/old-page` → `/new-page`.

- **Consolidating Content**:  
  Merge duplicate pages and redirect them to the canonical page.

- **Handling Deleted Pages**:  
  Redirect deleted pages to relevant alternatives or a custom 404 page.

---

By properly implementing and managing redirects, you can preserve your site’s SEO value, maintain a positive user experience, and ensure that search engines efficiently crawl and index your content.

#### Canonical tag

A canonical tag (<link rel="canonical" href="URL">) is an HTML element used to tell search engines the preferred version of a webpage when multiple pages have similar or duplicate content. It helps consolidate SEO value and prevents issues caused by duplicate content.

**Real-Life Example of When Canonical Tags Are Needed**

**Scenario: An E-commerce Website with Filtered or Sorted Pages**

Imagine you own an online store selling shoes, and your website allows users to filter or sort products by various criteria, such as color, size, price, or popularity. Each filter or sort option generates a unique URL, like:

1. `https://example.com/shoes` (Default category page)
2. `https://example.com/shoes?color=red` (Filtered by red color)
3. `https://example.com/shoes?sort=price-asc` (Sorted by price, ascending)
4. `https://example.com/shoes?color=red&sort=price-asc` (Filtered and sorted)

**The Problem:**
All these URLs display the same or similar products, creating duplicate content. Search engines might:
- Split SEO rankings between these URLs.
- Waste crawl budget on multiple variations.
- Confuse which version to rank in search results.

**The Solution:**
Add a canonical tag to all variations, pointing to the main category page (`https://example.com/shoes`):

```html
<link rel="canonical" href="https://example.com/shoes">
```

**Why It’s Needed:**
- Ensures search engines consolidate ranking signals (backlinks, relevance) to the main page.
- Prevents duplicate content issues and focuses search engine efforts on indexing the main page.
- Improves user experience by ensuring a consistent landing page in search results.

**Result:**
Search engines understand that `https://example.com/shoes` is the authoritative version, even if users interact with filtered or sorted URLs. This boosts the main page's SEO value while keeping other variations crawlable for users.