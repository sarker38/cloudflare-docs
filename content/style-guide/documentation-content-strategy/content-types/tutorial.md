---
pcx_content_type: concept
title: Tutorial
---

# Tutorial

{{<glossary-definition term_id="tutorial">}}

{{<render file="_howto-vs-tutorial.md">}}

## Template

We have a [pre-built template](https://github.com/cloudflare/cloudflare-docs/blob/production/archetypes/tutorial.md) that helps you follow our general structure and content guidelines.

You can copy the file directly or - if you have [Hugo](https://github.com/cloudflare/cloudflare-docs?tab=readme-ov-file#setup) installed on your local machine - you can run the following command:

```sh
$ hugo new content --kind tutorial {new_file_location}
```

In practice, that might look like:

```sh
$ hugo new content --kind tutorial content/workers/tutorials/new-tutorial.md
```

## Guidelines

**A tutorial is:**
+ User-focused
+ Aligned to a user's goal or job-to-be-done
+ Descriptive and guiding

**A tutorial can:**

+ Describe how to integrate with a third party
+ Be delivered in the Cloudflare dashboard
+ Describe how to set up multiple products to complete a single job-to-be-done

**A tutorial is not:**

+ Product configuration information, how-to (or any of the other content types)
+ How to complete a task in the UI or API
+ A dumping ground for screenshots
+ Content with no end goal or job-to-be-done

### Tone

Guiding, straightforward, educational, authoritative

### content_type

`tutorial`

### Structure

#### Required components

[**Title**](/style-guide/documentation-content-strategy/component-attributes/titles/): Short verb phrase in second-person imperative.

**Context**: An introductory paragraph on the user's goal or job-to-be-done and how they will accomplish that in the tutorial. Consider including the intended audience for the tutorial. Refer to [Context](/style-guide/documentation-content-strategy/component-attributes/context/) for more information.

**Consider the user story framing**: "As a `___`, I want to `___` so I can `___`."

[**Steps**](/style-guide/documentation-content-strategy/component-attributes/steps-tasks-procedures/): Numbered steps that complete a task.

#### Optional components

[**Notes/warnings**](/style-guide/documentation-content-strategy/component-attributes/notes-tips-warnings/)

[**Examples**](/style-guide/documentation-content-strategy/component-attributes/examples/)

**Screenshots**

[**Links**](/style-guide/documentation-content-strategy/component-attributes/links/)

**Boundaries**

## Examples

[Workers Tutorials](/workers/tutorials)
