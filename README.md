# Spree Wombat

Connect your SpreeCommerce Storefront to Wombat, providing push API and webhook handlers

## Installation

Add spree_wombat to your Gemfile:

```ruby
gem 'spree_wombat', github: 'spree/spree_wombat', branch: '2-2-stable'
```

Bundle your dependencies:

```shell
bundle
```

Add your Wombat credentials to `config/initializers/spree.rb`:

```ruby
Spree::Wombat::Config[:connection_token] = "sdfsfddfdss"
Spree::Wombat::Config[:connection_id] = "sdfsfddfdss"
```

By default we push to `https://push.wombat.co` but you can override that setting
like this:

```ruby
Spree::Hub::Config[:push_url] = "push_url"
```

## Testing

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

Copyright (c) 2014 Spree Commerce, Inc. and other contributors, released under the New BSD License
