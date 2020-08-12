---
date: 2020-08-03T11:03:49-07:00
title: GitHub GraphQL Sponsorships
tags: github, graphql
---

# GitHub GraphQL Sponsorships

How to use GitHub's GraphQL API to get a list of projects you sponsor.

```
query {
  user(login: "senorprogrammer") {
    name
    sponsorshipsAsSponsor(last: 100) {
      totalCount
      edges {
        node {
          id
          sponsorable {
            sponsorsListing {
              slug
            }
          }
          tier {
            name
            monthlyPriceInCents
          }
        }
      }
    }
  }
}
```

Output:

```
{
  "data": {
    "user": {
      "name": "Chris Cummer",
      "sponsorshipsAsSponsor": {
        "totalCount": 2,
        "edges": [
          {
            "node": {
              "id": "MDExOlNwb25zb3JzaGlwNjMyNA==",
              "sponsorable": {
                "sponsorsListing": {
                  "slug": "sponsors-gdamore"
                }
              },
              "tier": {
                "name": "$2 a month",
                "monthlyPriceInCents": 200
              }
            }
          },
          {
            "node": {
              "id": "MDExOlNwb25zb3JzaGlwNTg5NA==",
              "sponsorable": {
                "sponsorsListing": {
                  "slug": "sponsors-caarlos0"
                }
              },
              "tier": {
                "name": "$5 a month",
                "monthlyPriceInCents": 500
              }
            }
          }
        ]
      }
    }
  }
}
```
