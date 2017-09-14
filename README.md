# Subify

Replace the a string with another string. A scenario I use this for is pasting sensitive code on stackoverflow or reddit. Sure search and replace in file works but I use this in conjuntion with my [leftify](https://github.com/vmcilwain/subify) gem so that it is also indented.

## Disclaimer

`Use at your own risk!` I am not responsible any damage to your file or fystem. If you are not sure this will work for you, install it on a vagrant vm and give it a try there. You can use the Vagrantfile that is in this repo to take care of configuring a useable vm.

## Usage

Replaces `Hello` with `Bye`

```
printf "Hello World" | subify Hello Bye
```

produces:

```
Bye World
```

Using with Leftify gem

```
printf "Hello
World" | leftify | subify Hello Bye
```

produces:

```
    Bye
    World
```

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'subify'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install subify

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Releasing

To release a new version:

* update the version number in `version.rb`
* tag the the code `git tag v1.0.0`
* push the tag `git push --tags`
* then run `bundle exec rake build`
* `gem push pkg/subify-version`

Which will push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on [GitHub](https://github.com/vmcilwain/subify).

This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
