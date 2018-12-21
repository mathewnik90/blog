---
layout: default
tags: technology
comments: true
---


In this blog, I will provide a brief about how I set up this blog, in other words, how to set up a basic Jekyll blog site. <!--more-->Some of you must have already figured out that I have set up this blog using GitHub pages. If you haven&#39;t, don&#39;t worry, I will guide you through step by step instructions to set up a similar blog.

(**Note** : I will be using external references for steps that are already available online. The idea here is to collate the information that I found useful in setting up this blog. Hopefully, I think this will be useful to someone else as well.)

These steps should take 1-2 hours to complete depending on your experience with web technologies and clarity about the final output. You do not need to complete all the steps in one go, you can leave at one of the steps and resume the set up later.

**Step 1** : Acquire your domain

1. Go to one of the popular domain registration sites and buy a domain. Some of the popular ones are:
  - [https://GoDaddy.com](https://GoDaddy.com)
  - [https://Bigrock.com](https://Bigrock.com)
2. Finalize from one of the available names
3. Pay the amount and register the domain

**Step 2** : Set up a GitHub pages website

1. Sign in to your [GitHub account](https://github.com/login) (or create if you don&#39;t already have it)
2. Next follow [these instructions](https://guides.github.com/features/pages/) to set up your first [https://repositoryname.github.io](https://repositoryname.github.io)  page. The subdomain name is same as your repository name. This will eventually change once you use your custom domain. 
3. Even though it is not mentioned in the guide, I would strongly recommend to `_Enforce HTTPS`_ on the webpage. Benefits of using HTTPS are readily available with a basic google search ([Example](https://www.bluecorona.com/blog/reasons-to-have-https-website)).

 ![]({{site.baseurl}}/assets/images/blog-support/setting_up_blog_custom_domain.jpg)

**Step 3** : Update the content on the webpage

1. Now that you have the basic website ready, let&#39;s try changing some content.
2. Update the content in the index.md file
3. Markdown is simple to understand. Use [this page](https://guides.github.com/features/mastering-markdown/) to get basic understanding of markdown and create some content.
4. Good job! Now you have a website and some basic content ready, albeit without the domain name that you have bought. We will get there soon.

**Notes**:
  1. I have observed that, at times, after contents are pushed to GitHub, it may take a while to appear on your [https://repositoryname.github.io](https://repositoryname.github.io) webpage.
  2. You just need to create the markdown file. GitHub will automatically trigger Jekyll to generate the HTML content.
  3. The name of the generated HTML file is the same as the name of the markdown file. The file with the name as index.md will be converted to index.html. In other words, as you must have figured out already index.md is your landing page.

**Step 4** : Set up custom domain

1. Create a CNAME file in GitHub. [Steps to create a CNAME file](https://hackernoon.com/use-custom-domain-with-github-pages-2-straightforward-steps-cf561eee244f)
2. Add A records to your website ([What are A records](https://support.dnsimple.com/articles/a-record/))
  - Go to the DNS provider web page
  - There should be a page for DNS management
  - Add the IP addresses present [here](https://help.github.com/articles/setting-up-an-apex-domain/#configuring-a-records-with-your-dns-provider) as records
  - [This blog](https://hackernoon.com/how-to-set-up-godaddy-domain-with-github-pages-a9300366c7b) provides detailed steps for GoDaddy. The steps for your DNS provider should be similar
3. Wait for a _couple of hours_ for the DNS records to reflect. Et Voila! There you have your website hosted on GitHub pages.

The above steps should help you set up a basic blog. However, if you want to go beyond the basic set up, you will need to modify the CSS styles or scripts on the layout page or the individual pages.

**Step 5** : Setting up Jekyll on local

1. Setting up Jekyll on your local machine will provide you with a better user experience for editing the pages.
2. Steps to set up the Jekyll environment are mentioned on their [official website](https://jekyllrb.com/docs/installation/windows/).

**Step 6** : Run the set up on local

1. Download the zip file for the theme from GitHub and unzip it. For example: Cayman theme is available [here](https://pages-themes.github.io/cayman/).
2. Clone your repository or download your repository from GitHub.
3. Replace the index.md file with your file.
4. Open Command Prompt:
    1. Navigate to the folder where the zip file is present.
    2. Run the command using bundle exec jekyll serve.

You can now make changes locally on your machine and push the changes to GitHub. I use [Visual Studio Code](https://code.visualstudio.com/download), but you can use any other editor to make the changes. Once the changes are pushed to GitHub, the changes you have made should automatically reflect on your website. You can check out my repository at [https://github.com/mathewnik90/blog/](https://github.com/mathewnik90/blog/).

Hope these steps helped you to set up your own blog. Happy blogging!

**Additional References** :

1. [Beginners tutorial](https://www.youtube.com/watch?v=bwThn0rxv7M&amp;index=1&amp;list=PLm_Qt4aKpfKijgP0rDH7FSJOlS9IBGbT1)
2. [How to set up the navigation bar](http://joshualande.com/jekyll-github-pages-poole)
3. [Creating an archive page using Jekyll](http://chris.house/blog/building-a-simple-archive-page-with-jekyll/)
4. [Creating related post section  using Jekyll](https://blog.webjeda.com/jekyll-related-posts/)
5. [Styling Jekyll Markdown](https://digitaldrummerj.me/styling-jekyll-markdown/)
6. [Getting started with Jekyll](https://developer.telerik.com/featured/getting-started-with-jekyll/)