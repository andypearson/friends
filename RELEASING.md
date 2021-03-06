# Releasing

These are steps for the maintainer to take to release a new version of this gem.

1. On the `master` branch, update the `VERSION` constant in
`lib/friends/version.rb`.
2. Commit the change (`git add -A && git commit -m 'Bump to vX.X'`).
3. Add a tag (`git tag -am "vX.X" vX.X`).
4. `git push && git push --tags`
5. `CHANGELOG_GITHUB_TOKEN=... github_changelog_generator`
6. `git add -A && git commit -m 'Update CHANGELOG for vX.X'`
7. `git push`
8. `gem build friends.gemspec && gem push *.gem && rm *.gem`
9. Celebrate!
