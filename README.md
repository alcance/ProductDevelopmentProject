# Product Development Hiring Project

This outlines a recent problem we ran into and came up with a development solution for. We'd like to see how you would handle it. What is most important is gaining some insight into your development process and seeing how you work.

## Background

[BriteCore](http://www.britecore.com/) is a web-based platform insurance companies use to manage their business. Insurance is a form of risk management. Risks are anything that someone could incur a loss on. BriteCore has historically worked primarily with property-based risks (homes, farms, churches, etc.).

## Problem

Since BriteCore was created to work mostly with property-based insurance, the data model is pretty rigid. The data model assumes that all risks are properties and have addresses. This makes it difficult for BriteCore to work with different forms of insurance like Automobile Policies, Cyber Liability Coverage (protection against hacking), or Prize Insurance (if someone gets a $1 million hole-in-one prize at a golf tournament, the golf course doesn't pay it, they have an insurance policy to cover them).

## Primary Goal

We would like to see you come up with a solution that allows insurers to define their own custom data model for their risks. There should be no database tables called `automobiles`, `houses`, or `prizes`. Instead, insurers should be able to create their own risk types and attach as many different fields as they would like.

Fields are bits of data like first name, age, zip code, model, serial number, or prize dollar amount. Basically any data the carrier would want to collect about the risk. Fields can also be of different types, like text, date, number, currency, and so forth.

### Data

For the data layer, model the risk types and how the generic fields and field types would relate to these risk types. Field types should be either `text`, `number`, `date` or `enum` (where there are multiple potential options but only one choice can be made).

Deliverables will be either...

1. A Python file containing the ORM classes for these tables. **Bonus points** if you use the Django ORM, but SQLAlchemy or Peewee would work fine, too.
2. An entity relationship diagram, which depicts the tables and their relationship to one another.
3. Both 1 and 2, because you're awesome.

### Backend

For the backend, create a single API endpoint that returns a risk type, including all of its fields and their field types. We're looking for a clean, well-structured API response with a sane URL and that accepts the correct HTTP method(s).

Deliverables will be...

1. A small, well-tested REST API written in Python.

### Frontend

The frontend is all about collecting information as it relates to these generic models. Create a single page that hits your risk type API endpoint and displays all of the fields to the user in a form. Be sure to display at least one field of each type on the page. Don't worry about submitting the form.

Fields should use appropriate widgets based on their type. `text` fields should display as text boxes, `date` fields should use date pickers, and so on.

Deliverables will be...

1. A single HTML file or a small JavaScript app. **Bonus points** if you use ES6 and a modern JavaScript framework. **Mega bonus points** if you use Vue.js specifically.

## Questions

For questions, please contact grant@britecore.com.

## Finished?

When you're done with the above project, please submit your GitHub repo to grant@britecore.com. Also submit...

1. A video of you running the code and loading the page in a browser (plus some screenshots).
2. **Bonus points** if you host the application and send us the URL so we can play with it.
3. **Mega bonus points** if you host the backend on [AWS Lambda](https://aws.amazon.com/lambda/) using [Zappa](https://github.com/Miserlou/Zappa).