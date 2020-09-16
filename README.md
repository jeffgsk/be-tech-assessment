# Back End Technical Assessment

## Overview

We'd like to create a nodejs http service that can count all the URLs in a website's Sitemap(s).

## Requirements

- create an http endpoint that accepts a URL of the site we are interested. it should create a count that the user of the service can retrieve from another endpoint later

- when the count is created:
    - since this is just an exercise, keep the count in memory and don't worry about scaling. But it's something we'll discuss in a follow-up interview.

    - find sitemaps listed in the robots.txt of the URL
      - if there is not a robots.txt present then return an error

    - return a count all the URLs in the given sitemaps

    - take sitemap index's into account, these are sitemaps that list other sitemaps
      - even though it's against the spec, sites often have sitemap indexes that list more sitemap indexes (nested to an arbitrary depth) and therefore we should handle these somehow. You can either ignore them, handle them, or error the count.

- create an http endpoint that can retrieve a running / done count and status

## Constraints

- We don't have strong preferences on which http library / framework for node you use, use whatever you know best

- Overall, just use any libraries that help you get the job done quicker.

- We use Typescript for everything here, so if you are familiar with Typescript use it. If you think it would slow you down too much then no need to use it.


## Output

Your output for this should be whatever code you have written, and the minimum viable documentation that you think the reviewer would need to run the project and use the API. How to get the server running and a couple example http calls is enough.

Don't feel the need to spend an excessive amount of time on this. If it's taking more than a couple hours then just turn in what you have. We'll talk through what you have in a follow up session and how we might modify it for use in a production system.

Given that your final output might not be a fully working system, our preference would be for you to complete the task from the outside in so to speak. A working api server > api endpoints that return stub data > api endpoints that return partially working data > etc.
