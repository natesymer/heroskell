HEROSKELL
==

A Haskell buildpack for deploying WAI apps (without NGINX or similar). Your Haskell program should include its own webserver.

Heroskell first makes sure that GHC, cabal-install, Cabal, GMP, Happy, and Alex
are installed. Then, it builds your project & packages it for Heroku. Slug sizes are around ~10MB for a semi-large Haskell app. The final slug contains your executable so that `Procfile`s should look like:

    web: myexecutable

USAGE
===

Either use this buildpack as-is, or if you need a specific version of GHC/cabal/GMP, fork this repository and modify the config vars at the top of `bin/compile`.
