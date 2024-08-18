# JS Full-stack Engineer — Technical test

## Introduction

We want to build an **URL Shortener** service (only the API). The API can be used to turn a long URL into a tiny URL.

A long URL might look like:

> https://medium.com/equify-tech/the-three-fundamental-stages-of-an-engineering-career-54dac732fc74

And the service would turn it into a tiny URL that could look like this:

> https://\<my-domain\>/\<slug\>

**_\<my-domain\>_** would be the domain of the API, in our case [localhost:3000](http://localhost:3000) is fine.

**_\<slug\>_** would be a random short string with letters and numbers. (eg. aY2Pv8, Lt1fov, 9vqp4g…)

When the user types this URL (eg. http://localhost:3000/aY2Pv8) in its browser it is automatically redirected to the original URL via an HTTP redirect.

## Requirements

### Must have

- Build the API in Node using Typescript
- Use a SQL storage (via Docker or a solution like SQLite)
- The README should explain how to run your project **locally** in dev mode
  - Ideally: `npm install` followed by `npm start`
  - You can assume the reader has Node and Docker install (If you need Docker at all…)
- Think of edge cases and make sure your solution is robust. We will **challenge** you on this point, you don’t have to implement the perfect solution, but you should be able to **pitch** your vision in under 5 minutes.

### Liberties

- Use whichever **lib** or **framework** you like (Express, Koa, NestJs, Prisma, Knex, Kysely…)
- If you can write the backend in 40 lines of code that is fine, don’t feel obligated to integrate complexe design patterns or libraries.
- You can generate **random strings** using a library like [nanoid](https://www.npmjs.com/package/nanoid), you do not have to implement it yourself, it does not have to be cryptographically secured
- You don’t have to worry about building, packaging, and hosting your project in production. Just make sure it is runnable on localhost.
- Don’t bother with https and domain names. http://localhost:3000 is perfect

### Nice to have

If you have time you may go beyond the assignment. But this is not a feature contest !

- Tests (very basic, does not have to be 100% coverage)
- Shortening the same URL twice returns the same generated string
- Expiration dates on URLs
- Clicks counter

## What we will look for

Writing the code should be very straight forward, we are more interested in how you communicate, what is your vision, and how you solve issues.

- Can you explain your decision process?
- What would you do to go to production?
- How would you implement more complex features?
