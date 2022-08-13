# FreshService API Client
Ruby toolkit for the Fresh Service API V2.

## Table of Contents
1. [Installation](#installation)
2. [Making requests](#making-requests)
   1. [Initialization](#initialization)
   2. [Ticket](#ticket)
   3. [Group](#group)
   4. [Service Request](#service-request)
3. [Development](#development)
5. [License](#license)


## Installation
Add this line to your application's Gemfile:

```ruby
gem 'fresh_service'
```

And then execute:

    $ bundle install

Or install it yourself as:

    $ gem install fresh_service

## Making requests
### Initialization
```ruby
# client initialization
client = FreshService::Client.new
```
### Ticket
```ruby
# Create a ticket
# @see https://api.freshservice.com/#create_ticket
client.create_ticket(options = {})

# Update a ticket
# @see https://api.freshservice.com/#update_ticket_priority
client.update_ticket(ticket_id, options = {})

# View a ticket
# @see https://api.freshservice.com/#view_a_ticket
client.view_ticket(ticket_id, options = {})
```

### Group
```ruby
# Create a group
# @see https://api.freshservice.com/#create_a_group
client.create_group(options = {})

# View a group
# @see https://api.freshservice.com/#view_a_group
client.view_group(group_id, options = {})
```

### Service Request
```ruby
# Create a Service Request
# @see https://api.freshservice.com/#create_service_request
client.create_service_request(display_id, options = {})

# Update a Service Request
# @see https://api.freshservice.com/#update_req_items_of_sr
client.update_service_request(ticket_id, item_id, options = {})
```

## Development
If you want to run on Fresh Service locally

    bin/bootstrap

This will install gem dependencies and get you up and running. If you want
to run a Ruby console, you can crank one up with:

    bin/console

Using the scripts in `./bin` instead of `bundle exec rspec`, `bundle
console`, etc.  ensures your dependencies are up-to-date.

## License

MIT
