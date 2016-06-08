# ASP.NET 5 Buildpack

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for building [ASP.NET 5](http://docs.asp.net/en/latest/conceptual-overview/aspnet.html) apps using [`project.json` files](https://github.com/aspnet/Home/wiki/Project.json-file) and the [dnvm package manager](https://github.com/aspnet/Home/wiki/Version-Manager).

### Runtimes:
- [Mono](http://www.mono-project.com/) is bundled for runtime execution currently.
- When [.NET Core](https://github.com/dotnet/core/blob/master/roadmap.md) is ready (Q1 2016), there will be changes.

### Usage

Example usage:

    $ heroku create --buildpack http://github.com/nguymin4/dotnet-buildpack.git
    $ git push heroku master

The buildpack will detect your app as ASP.NET 5 if it has `project.json`. If the source code you want to build contains multiple `project.json` files, you can use a [`.deployment`](https://github.com/projectkudu/kudu/wiki/Customizing-deployments) or set a `$PROJECT` config var to control which one is built.
