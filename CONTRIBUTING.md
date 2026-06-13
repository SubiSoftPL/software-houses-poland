# Contributing to Software Houses Poland

Thanks for helping keep this the best curated list of software houses in Poland! Contributions of new companies, corrections, and better descriptions are very welcome.

## Ground rules

- **Keep it factual.** Only add real companies with a working website. No invented entries, no fabricated claims, no fake reviews.
- **No pay-for-placement.** This is an editorial list. Inclusion and order are not for sale.
- **One company, one place per city.** Avoid duplicates.
- **Neutral, useful descriptions.** One or two sentences: what they build, who they serve, and a differentiator. Avoid marketing fluff ("world-class", "best-in-class").

## How to add or edit a company

### National Top 50 list
Edit [`README.md`](README.md). Use this format inside the *Top Software Houses in Poland* list:

```markdown
1. **[Company Name](https://company-website.com)** — Short, factual description. · City
```

### A city page
Each city is a file in [`cities/`](cities/). Edit the `companies:` list in its front matter — no HTML needed. The visible list **and** the structured data (Schema.org `ItemList`) are generated from this automatically:

```yaml
companies:
  - name: "Company Name"
    url: "https://company-website.com"   # omit this line if you can't verify the URL
    description: "Short, factual description of what they build and who they serve."
    location: "City"                       # optional, useful on regional pages like Silesia
```

### Add a brand-new city
1. Copy an existing file in `cities/` (e.g. `software-house-krakow.md`).
2. Update the front matter: `permalink`, `title`, `h1`, `city`, `description`, `intro`, `companies`, `faqs`.
3. Add one matching entry to [`_data/cities.yml`](_data/cities.yml) so it appears in the navigation, sitemap and `llms.txt`.

## Before you open a pull request

- **Verify every link** opens the company's real, current website.
- Update the `updated:` date on any city page you change, and the **Last updated** line in `README.md`.
- If you can, preview locally: `bundle install` then `bundle exec jekyll serve`.

Open a [pull request](../../pulls) or an [issue](../../issues). Thank you!
