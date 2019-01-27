---
layout: post
title: "Jekyll 101"
categories: [jekyll, tutorial, docs]
image: https://jlospinoso.github.io/images/jekyll.svg
tags: [jekyll, tutorial]
---
#### Content taken from official docs

Jekyll is a simple, extendable, static site generator. You give it text written
in your favorite markup language and it churns through layouts to create a
static website. Throughout that process you can tweak how you want the site URLs
to look, what data gets displayed in the layout, and more.

## Instructions

1. Install a full [Ruby development environment](/docs/installation/)
2. Install Jekyll and [bundler](/docs/ruby-101/#bundler) [gems](/docs/ruby-101/#gems)
```
gem install jekyll bundler
```
3. Create a new Jekyll site at `./myblog`
```
jekyll new myblog
```
4. Change into your new directory
```
cd myblog
```
5. Build the site and make it available on a local server
```
bundle exec jekyll serve
```
6. Now browse to [http://localhost:4000](http://localhost:4000){:target="_blank"}

If you encounter any unexpected errors during the above, please refer to the
[troubleshooting](/docs/troubleshooting/#configuration-problems) page or the
already-mentioned [requirements](/docs/installation/#requirements) page, as
you might be missing development headers or other prerequisites.

<hr>

Jekyll is written in Ruby. If you're new to Ruby, this page is to help you get
up to speed with some of the terminology.

## Gems

A gem is code you can include in Ruby projects. It allows you to package up functionality and share it across other projects or with other people. Gems can perform functionality such as:

* Converting a Ruby object to JSON
* Pagination
* Interacting with APIs such as Github
* Jekyll itself is a gem as well as many Jekyll plugins including
[jekyll-feed](https://github.com/jekyll/jekyll-feed),
[jekyll-seo-tag](https://github.com/jekyll/jekyll-seo-tag) and
[jekyll-archives](https://github.com/jekyll/jekyll-archives).


## Gemfile

A `Gemfile` is a list of gems required for your site. For a simple Jekyll site it might look something like this:

```ruby
source 'https://rubygems.org'

gem 'jekyll'

group :jekyll_plugins do
  gem 'jekyll-feed'
  gem 'jekyll-seo-tag'
end
```

## Bundler

Bundler installs the gems in your `Gemfile`. It's not a requirement for you to use a `Gemfile` and `bundler` however it's highly recommended as it ensures you're running the same version of Jekyll and Jekyll plugins across different environments.

`gem install bundler` installs [Bundler](https://rubygems.org/gems/bundler). You only need to install it once &mdash; not every time you create a new Jekyll project. Here are some additional details:

If you're using a `Gemfile` you would first run `bundle install` to install the gems, then `bundle exec jekyll serve` to build your site. This guarantees you're using the gem versions set in the `Gemfile`. If you're not using a `Gemfile` you can just run `jekyll serve`.

For more information about how to use Bundler in your Jekyll project, this [tutorial](/tutorials/using-jekyll-with-bundler/) should provide answers to the most common questions and explain how to get up and running quickly.


Jekyll is a [Ruby Gem](/docs/ruby-101/#gems) that can be installed on most systems.

## Requirements

* [Ruby](https://www.ruby-lang.org/en/downloads/) version 2.2.5 or above, including all development headers (ruby version can be checked by running `ruby -v`)
* [RubyGems](https://rubygems.org/pages/download) (which you can check by running `gem -v`)
* [GCC](https://gcc.gnu.org/install/) and [Make](https://www.gnu.org/software/make/) (in case your system doesn't have them installed, which you can check by running `gcc -v`,`g++ -v`  and `make -v` in your system's command line interface)

<hr>

[Full Link here](https://jekyllrb.com/docs/)
