# Changelog

## Unreleased

💥 Breaking changes:

- Pull Request Title goes here

  Description goes here (optional)

  To migrate you need to change: X

  ([PR #N](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/N))

🆕 New features:

- Pull Request Title goes here

  Description goes here (optional)

  ([PR #N](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/N))

- New component: Digital Marketplace Header component

  *Requirement before using this component:*
  - To use this the application must be using `govuk-frontend` template
  - To use this the application must be using `govuk-frontend` phase banner as phase tag
    is no longer part of the header and sits underneath and outside the header

  *Installing component:*
  1. Check config.py has this line for jinja to find the components
      ```
                  os.path.join(repo_root, 'node_modules', 'digitalmarketplace-govuk-frontend')
      ```

  2. Import the component in `_base_page.html`
     `{% from "digitalmarketplace/components/header/macro.njk" import dmheader %}`

  3. Use the component `{{ dmHeader({}) }}`

  ([PR #25](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/25))

- New component: Digital Marketplace Footer component

  *Requirement before using this component:*
  - To use this the application must be using `govuk-frontend` template
  - digitalmarketplace-util v48.8.0+ must be installed

  *Installing component:*
  1. Check config.py has this line for jinja to find the components
      ```
                  os.path.join(repo_root, 'node_modules', 'digitalmarketplace-govuk-frontend')
      ```

  2. Import the component in `_base_page.html`
     `{% from "digitalmarketplace/components/footer/macro.njk" import dmFooter %}`

  3. Use the component `{{ dmFooter({}) }}`

  ([PR #21](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/21))

🔧 Fixes:

- Pull Request Title goes here

  Description goes here (optional)

  ([PR #N](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/N))

## 0.2.1

🔧 Fixes:

- Fix layout issues with error pages

  Error pages content was not centrally aligned.

  Check frontend app `config.py` includes `os.path.join(repo_root, 'node_modules', 'digitalmarketplace-govuk-frontend', 'digitalmarketplace', 'templates'),` to lookup the error templates

  Make sure `base_page.html` is using `mainContent` and `pageTitle` blocks

  ([PR #23](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/23))

## 0.2.0

🆕 New features:

- Add error templates

  Error templates which use GOV.UK Frontend classes for styling.

  ([PR #14](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/14))

- Add site verification and custom dimension tracking

  This originally originally built into `digitalmarketplace-frontend-toolkit` and will
  be needed in the future when we do away with `digitalmarketplace-frontend-toolkit`.

  ([PR #15](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/15))

## 0.1.0

🆕 New features:

- Import and use govuk-frontend v2.13.0

  ([PR #1](https://github.com/alphagov/digitalmarketplace-govuk-frontend/pull/1))