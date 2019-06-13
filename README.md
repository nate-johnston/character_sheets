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

# So that means I don't have to write any HTML, any AT ALL!!

No, not so fast.  There is a lot that is customized about character sheets.
This makes things much more automated but there are a lot of little quirks that
still need to be reflected.  But the goal is that when the character goes up a
level, you just adjust the level line and push and suddenly all the attack
bonuses, spell DCs, skill bonuses etc. all are automatically recalculated.
