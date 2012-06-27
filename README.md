Flail is an exception catcher for Rack applications.

##### Supports

* Rails 2.3.x
* Rails 3.x


#### Install

```
$ [sudo] gem install flail
```

For Rails 2.3.x, install the gem as a plugin


#### Usage


Add an initializer to configure (or call configure during application startup):

```ruby
Flail.configure do
  # configure a custom handler for the error payload
  # don't call if you want to use the default http post handler
  handler do |payload|
  end

  # endpoint for default handler
  endpoint "https://flail.net/swing"

  # environment of application, defaults to Rails.env
  # included in payload
  env "production"

  # hostname to use of server, defaults to Socket.gethostname
  # included in payload
  host Socket.gethostname

  # arbitrary api key which can identify
  # your project or be anything else
  api "custom_key"
end
```


#### Author


Original author: John "asceth" Long
