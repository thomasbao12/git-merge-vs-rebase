git rebase, merge, and cherry-pick all end up using hunks!

I thought if we had the following:

file@sha1@main:

a
b
c
d

file@sha2@main:
a
b'
c
d

file@sha1'@side-branch:
a
b
c'
d

git rebase would detect a hunk conflict and merge would result, but I was wrong!
git uses hunks!

a
b'
c'
d
