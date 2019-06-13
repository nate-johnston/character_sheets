# Character Sheets

This is where I keep character sheets that I use in my D&D games.  

# How the automated tooling works

I run the [Gogs git server](https://gogs.io) on my hosting machine.  I have a
postcommit webhook set up on that server pointing to a service I have running on
localhost.  That service is the
[gitlab-webhooks-receiver](https://github.com/shawn-sterling/gitlab-webhook-receiver)
which I have configured to run ERB on any templates it finds.  It also will
refresh my website, which is built using [Hugo](https://gohugo.io/).  That way
whenever I `git push` the ERB for a character sheet, it is automatically
templated and published.
