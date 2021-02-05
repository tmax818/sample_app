# README

# Ruby on Rails Tutorial sample application

This is the sample application for
[*Ruby on Rails Tutorial:
Learn Web Development with Rails*](https://www.railstutorial.org/)
(6th Edition)
by [Michael Hartl](https://www.michaelhartl.com/).

## License

All source code in the [Ruby on Rails Tutorial](https://www.railstutorial.org/)
is available jointly under the MIT License and the Beerware License. See
[LICENSE.md](LICENSE.md) for details.

## Getting started

To get started with the app, clone the repo and then install the needed gems:

```
$ bundle install --without production
```

Next, migrate the database:

```
$ rails db:migrate
```

Finally, run the test suite to verify that everything is working correctly:

```
$ rails test
```

If the test suite passes, you'll be ready to run the app in a local server:

```
$ rails server
```

For more information, see the
[*Ruby on Rails Tutorial* book](https://www.railstutorial.org/book).

# My Notes:

- This is my version of the rails tutorial. I have included the readme because I have a huge man-crush on Michael Hartl!

## Start of branch (static-pages)

```bash
$ rails g[enerate] controller StaticPages home help
```

- modify [home.html.erb](app/views/static_pages/home.html.erb)
- modify [help.html.erb](app/views/static_pages/help.html.erb)
- write [tests](test/controllers/static_pages_controller_test.rb)

- add [route](config/routes.rb)
- add [controller](app/controllers/static_pages_controller.rb)

```bash
$ touch app/views/static_pages/about.html.erb
```

- now it's green

- add [view](app/views/static_pages/about.html.erb)

- disable the layout [file](app/views/layouts/application.html.erb)
  - I found this more confusing than just adding it to the layout file.

```bash
$ mv app/views/layouts/application.html.erb layout_file   # temporary change
```

- change the [root](config/routes.rb)