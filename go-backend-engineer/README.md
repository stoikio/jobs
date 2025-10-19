# Go Back-end Engineer — Technical test

## Introduction

We want to build an **URL Shortener** service (only the API). The API can be used to turn a long URL into a tiny URL.

A long URL might look like:

> https://medium.com/equify-tech/the-three-fundamental-stages-of-an-engineering-career-54dac732fc74

And the service would turn it into a tiny URL that could look like this:

> https://\<my-domain\>/\<slug\>

When the user types this URL in its browser it is automatically redirected to the original URL via an HTTP redirect.

**_\<my-domain\>_** would be the domain of the API, for example tiny.io. For the purpose of this test, you can use localhost.

**_\<slug\>_** would be a random short string with letters and numbers. (eg. aY2Pv8, Lt1fov, 9vqp4g…)

## Requirements

### Must have

- Build the API in Go
- Use a SQL storage
- Dockerize the API
- Think of edge cases and make sure your solution is robust. We will **challenge** you on this point, you don’t have to implement the perfect solution, but you should be able to **pitch** your vision in under 5 minutes.

### Liberties

- The **random strings** generation does not have to be cryptographically secured

### Nice to have

If you have time you may go beyond the assignment. But this is not a feature contest !

- Tests
- Shortening the same URL twice returns the same generated string
- Expiration dates on URLs
- Clicks counter

## What we will look for

Writing the code should be very straight forward, we are more interested in how you communicate, what is your vision, and how you solve issues.

- Can you explain your decision process?
- What would you do to go to production?
- How would you implement more complex features?