# Human-Interactive Robotics Lab, IISc

**Live site:** https://hiro.cps.iisc.ac.in

## Local development

The site is built with [Jekyll](https://jekyllrb.com/). To run it locally:

```bash
bundle install
bundle exec jekyll serve
```

The site is then available at http://localhost:4000.

## Structure

- `_pages/` — pages (Home, Research, People, Publications, Contact)
- `_data/publications.yml` — publication list shown on the Publications page
- `_includes/`, `_layouts/` — templates
- `assets/` — styles, images, and fonts
- `people/drraviprakash/` — Prof. Ravi Prakash's homepage
- `_config.yml` — site configuration

## Editing

- **Publications:** add an entry to `_data/publications.yml`.
- **People:** edit `_pages/people.md`; member photos go in `assets/img/people/`.

## Deployment

Commits pushed to the `master` branch are built and deployed to GitHub Pages
automatically. The custom domain is configured in `CNAME`.

## License

Released under the [MIT License](LICENSE). Built on the
[al-folio](https://github.com/alshedivat/al-folio) Jekyll theme.
