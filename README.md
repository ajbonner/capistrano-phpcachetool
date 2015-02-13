# Capistrano::Phpcachetool


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'capistrano-phpcachetool'
```

And then execute
```
$ bundle
```

Or install it yourself as:

```
$ gem install capistrano-phpcachetool
```

## Usage

Require the module in your Capfile:

```ruby
require 'capistrano/phpcachetool'
```

The `cachetool:reset` task will run after deploy:symlink:release as part of Capistrano default deploy.

## Configuration

```ruby
set :cachetool_reset_flags, '--fcgi'
set :cachetool_roles, :all
set :cachetool_lib, :all
set :cachetool_working_dir, -> { fetch(:release_path) }
set :cachetool_download_url, "http://gordalina.github.io/cachetool/downloads/cachetool.phar"
```

## Contributing

1. Fork it ( https://github.com/karamani/capistrano-phpcachetool/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
