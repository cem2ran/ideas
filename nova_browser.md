*What if browsers could understand your browsing context, solve the complexity of managing open tabs and suggest websites relevant to your current browsing session.*

The problem I’d like to solve is twofold and revolves around browsing and categorisation of web content:

## Web browsing in the age of social media and apps
In the last few years I’ve seen an increase in the amount of browser windows and tabs that I as well as others have open. Tabs have a tendency to creep into browser windows that contain content that is completely different, due to the nature of opening links. When you receive an email with a link or when you visit social media and open a link it usually just opens in the most recently used window.
When tabs are allowed to mix and match with unrelated tabs they face the possibility of being lost and therefore outlive their true lifespan. The effect of not being disciplined and not closing down a tab as soon as it is truly consumed leads to a negative feedback loop where the addition of every new tab decreases the visibility of the existing tabs and overall increases the chances of any tab being lost and not closed down.

I propose the grouping of related tabs together into distinct sessions as a possible way of solving this problem. There would only be one session open at a time and all other sessions would be hidden. This leads to better discoverability, focus and readability as there are simply fewer tabs and windows present. This in turn has the added benefit of ensuring that unused tabs aren't being kept open and consuming resources. 

The end product could be a browser extension installable on most browsers, which takes care of hiding and persisting unrelated sessions and bring into focus the relevant one when necessary.

Unsupervised techniques such as (hierarchically) clustering and expectation maximization could be utilized on the text contents of the websites, urls and titles to perform the groupings of browser tabs into windows. The clusters would be reevaluated whenever a new tab is created.

## From browsing session to bookmarks
Another problem is that of (re)discovering content, which cannot be fully consumed at the given moment. I usually use a bookmarking service to save the link for later, but more than ever the link is simply lost as the session/topic that it relates to isn't propagated along when bookmarked. The only way of achieving this is by manually tagging the bookmarked content, i.e. manual categorization. Failing to provide a tag, which herein includes selecting the most meaningful tag to describe the content leads to bookmarks being presented in a long unstructured list sorted by most recent addition.

One possible solution would be to hierarchically cluster web pages into relevant topics/tags and possibly also provide an interface that makes use of the hierarchy. One could additionally propose relevant tags. Supervised methods have not yet been considered, but a dataset for the purposes of training and testing could be constructed by mining the [Reddit dataset](https://bigquery.cloud.google.com/table/fh-bigquery:reddit_posts.full_corpus_201512) available on Google BigQuery. It contains relations between headings and links that are categorized into topics known as "subreddits".

## New tab; New search. Why not show relevant websites?
An extension to the project would be to provide recommendations based on the users current session. Opening a new tab could provide a list of recommendations relevant to the session.

### Glossary
**Session -** A session refers to the grouping of semantically related web pages.
