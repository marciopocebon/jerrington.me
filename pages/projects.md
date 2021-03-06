---------------
title: Projects
---------------

[Computing Workshop][]
-----

Computing Workshop is a 9-session mini-course on computing, taking a holistic
approach that covers both hardware and software.

Students will:

* learn about the major hardware components of a computer and how they work;
* build physical digital logic circuits using transistors;
* practise elements of static web development using HTML and CSS;
* use [Haskell][] to implement algorithms and build a static site generator
  with [Hakyll][].

[servant-pushbullet-client][]
-----

This library describes the Pushbullet API as a type and provides functions
created with [Servant][servant-client] to call the API. It also provides some
miscellaneous functions for dealing with particulars of the Pushbullet API,
such as pagination of results.

This library depends on [another one][pushbullet-types] I wrote which simply
describes the types of objects returned by the Pushbullet API.

Ultimately, the reason I wrote these libraries was to write [tpb][], an
application to interact with the Pushbullet API on the command-line.
On top of this application, I wrote a number of scripts for sending and
receiving SMS on the command-line.

[servant-github-webhook][]
-----

This is my first published Haskell library. It implements
[Servant][servant-server] combinators to
represent routes that are meant to service GitHub webhooks. These combinators
provide routing based on webhook type and automatic verification of GitHub
digital signatures.

Vent over Tea
-----

In the spring of 2015,
[Dan Crisan][] and I built the first iteration of the
[Vent over Tea][] web site together.

Publications
-----

### The Great Migration and African-American genomic diversity

In 2014 as a research assistant in the lab of
[Simon Gravel][],
I contributed to [tracts][],
which is a tool for modelling local ancestry patterns along the genome.
Simply put, given a model of migration and the ancestry proportions of
individuals in a present population, tracts evaluates the likelihood of the
migration described by that model having occurred.

Tracts had an issue when presented with large populations that would arise due
to an averaging of the present population's ancestry proportions. I resolved
this by implementing a new demographic model in tracts that performs a model
evaluation on multiple subpopulations and combines the results of those
evaluations. By splitting the population in this way, tracts can avoid
discarding the information given by the variance in the present population's
ancestry proportions.

This new evaluation method was used to produce some of the results in the paper
[_The Great Migration and African-American genomic diversity_][great migration],
 of which I am a coauthor.

[servant-server]: https://hackage.haskell.org/package/servant-server
[servant-client]: https://hackage.haskell.org/package/servant-client
[servant-pushbullet-client]: https://github.com/tsani/servant-pushbullet-client
[pushbullet-types]: https://github.com/tsani/pushbullet-types
[servant-github-webhook]: https://github.com/tsani/servant-github-webhook
[Dan Crisan]: http://dancrisan.com/
[Vent over Tea]: http://ventovertea.com/
[Simon Gravel]: http://simongravel.lab.mcgill.ca/Home.html
[tracts]: http://github.com/sgravel/tracts
[great migration]: http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1006059
[tpb]: https://github.com/tsani/tpb
[Computing Workshop]: https://computing-workshop.com/
[Haskell]: https://haskell.org/
[Hakyll]: https://jaspervdj.be/hakyll/
