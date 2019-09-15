# Social Demo

A series of projects that transform an HTML page into a federated social media platform.

## Overview

The first demo is a concept built using contemporary web styling components. Subsequent demos build the backing systems, replacing elements with dynamic implementations.

## Status

See the Git commit history for details. The projects were developed over several weeks of morning coffee sessions. The README is a work in progress, as I reverse engineer the experiments.

## Projects

### Social.html

`social.html`

A basic [HTML]() [page](), [coded]() using [Bootstrap 4]().

Renders several types of post into cards, and has basic contact and post forms.

### Muh Timeline

Six Demos that explore elements of a backing system for `social.html`.

#### 1

`src/muh_timeline/social_demo.cljs`

The social.html page [ported]() to [EDN]() for use with [Hiccup]() via [an automated tool]().

#### 2

`src/muh_timeline/social_demo_2.cljs`

The [static]() EDN structure broken into [view template]() [functions](), [composed]() and [rendered]() via [string]().

#### 3

`src/muh_timeline/social_demo_3.cljs`

The Hiccup [representation]() ported to [Reagent](), allowing for automatic re-rendering.

#### 4

`src/muh_timeline/social_demo_4.cljs`

Explores [server-side rendering](datascript) for the same view templates.

#### 5

`src/muh_timeline/social_demo_5.clj`

Imports existing [Cryogen]() blog project into a [datalog]()-like [database](), and back the views with [actual content]().

#### 6

`src/muh_timeline/social_demo_.cljs`

Experiments with [filesystem]() and database [observers](), to trigger the [rendering pipeline]().


## Social Model App

Experiments with rendering a site based on a datalog database.

TODO document

## Social Trends

Builds visual timelines for a datalog-like database in ClojureScript.

TODO document


## Magic Link Auth

Connects to an [SMTP]() server and sends a link with a login [token]() that is good for 5 seconds.

## Setup

To get an interactive development environment run:

    lein figwheel

and open your browser at [localhost:3449](http://localhost:3449/).
This will auto compile and send all changes to the browser without the
need to reload. After the compilation process is complete, you will
get a Browser Connected REPL. An easy way to try it is:

    (js/alert "Am I connected?")

and you should see an alert in the browser window.

To clean all compiled files:

    lein clean

To create a production build run:

    lein do clean, cljsbuild once min

And open your browser in `resources/public/index.html`. You will not
get live reloading, nor a REPL. 

## License

Copyright © 2014 FIXME

Distributed under the Eclipse Public License either version 1.0 or (at your option) any later version.
