# Events

## About

This [Ruby on Rails](http://rubyonrails.org/) app powers the [AgileVentures main developer site](http://agileventures.org/), showing lists of active [projects](https://www.agileventures.org/projects), [members](https://www.agileventures.org/users), [upcoming events](https://www.agileventures.org/events), [past event recordings](https://www.agileventures.org/scrums), as well as information for how to [get involved](https://www.agileventures.org/membership-plans).

## Installation

See the [Project Setup](docs/project_setup.md) documentation

## Contributing

See our [Contribution guidelines](CONTRIBUTING.md)


## Approaches

* Agile Development
  * In the past we had regular sprints, offered daily standups, and got regular feedback from end users.  We have discussions on Slack and occasional meetings now.
* Behaviour Driven Development (BDD)
  * We use Cucumber and RSpec testing tools that describe the behaviors of the system and its units
  * We try to work outside in, starting with acceptance tests, dropping to integration tests, then unit tests, and then writing application code
  * We do spike application code occasionally to work out what's going on, but then either throw away the spike or make sure all our tests break before wrapping the application code in tests (by strategically or globally breaking things)
  * Where possible we go for declarative over imperative scenarios in our acceptance tests, trying to boil down the high-level features to be easily comprehensible in terms of user intention
* Domain Driven Design (DDD)
  * Sometimes we switch to inside out, trying to adjust the underlying entity schema to better represent the domain model
* Self-documenting code
  * We prefer executable documentation (tests) and relatively short methods where the method and variable names effectively document the code

## Reading material

* [Imperative vs Declarative Cucumber](http://fasteragile.com/blog/2015/01/19/declarative-user-stories-translate-to-good-cucumber-features/)

## Admin rake tasks

```bash
rake fetch_github_last_updates
rake fetch_github_languages
rake fetch_github_content_for_static_pages
rake fetch_github_readme_files
rake fetch_github_commits
rake karma_calculator
rake geocode:all
rake user:create_anonymous
rake vcr_billy_caches:reset
```

Updating the live static pages (like 'About' and 'Getting Started') requires the administrator to run `rake fetch_github:content_for_static_pages.`
