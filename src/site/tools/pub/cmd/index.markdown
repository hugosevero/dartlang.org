---
layout: default
title: "Pub Commands"
---

{% include toc.html %}

# {{ page.title }}

Aside from managing packages, [pub](/tools/pub/) also has support for
building web apps.

If your web app's directory structure follows pub's [package layout
conventions](/tools/pub/package-layout.html), you can use the pub
development server (<code class="literal">pub serve</code>) to continuously
build and serve the app's assets. Once you're ready to deploy the web app,
use <code class="literal">pub build</code> to generate the final files.

Quick links to the `pub` commands:

* [`pub build`](pub-build.html)
* [`pub cache`](pub-cache.html)
* [`pub deps`](pub-deps.html)
* [`pub get`](pub-get.html)
* [`pub publish`](pub-lish.html)
* [`pub serve`](pub-serve.html)
* [`pub upgrade`](pub-upgrade.html)
* [`pub uploader`](pub-uploader.html)

<aside class="alert alert-info" markdown="1">
*Problems?*
See [Troubleshooting Pub](../troubleshoot.html).
</aside>

Pub's commands fall into the following categories:

## App creation and maintenance

`pub` provides two commands that support
the creation and maintenance of a Dart application.

* The [`pub get`](pub-get.html) command retrieves the packages that are
  listed as the dependencies for the application.

* The [`pub deps`](pub-deps.html) command lists all of the dependencies
  used by the package.

* The [`pub upgrade`](pub-upgrade.html) command retrieves the latest
  versions of all the packages that are listed as dependencies
  used by the application.

## Development

During the development cycle of an application, the
[`pub serve`](pub-serve.html)
command is used to start up a development server.
This server can be accessed via the browser on localhost and
allows you to view your web-based app.

## Deployment

When you are ready to deploy your app, the
[`pub build`](pub-build.html) command
creates the *build* directory, compiles the Dart code, and places 
the assets into the build directory.

## Publication

If you want to share your Dart packages with the world, you can
use the [`pub publish`](pub-lish.html) command to upload your package to 
[pub.dartlang.org](http://pub.dartlang.org). The
[`pub uploader`](pub-uploader.html) command enables specific users
to modify and upload new versions of your package.

---

## Global options {#global-options}

Several command-line options work with all of the pub commands.
These include:

`--help` or `-h`
: Print usage information.

`--version`
: Print version of pub.

`--trace`
: Print debugging information when an error occurs.

`--verbosity=<level>`
: The specified level determines the amount of information that is displayed:

* `all`
: Show all output, including internal tracing messages.

* `io`
: Show I/O operations.

* `normal`
: Show errors, warnings, and user messages.

* `solver`
: Show steps during version resolution.

`-verbose` or `-v`
: Equivalent to `--verbosity=all`.
