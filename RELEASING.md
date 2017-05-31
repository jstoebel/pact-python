# Releasing

1. Increment the version according to semantic versioning rules in `pact/__init__.py`

2. To upgrade the the versions of `pact-mock_service` and `pact-provider-verifier`, change the
   appropriate `GEM_VESRION` variable in `scripts/build.sh` to the new version.

3. Update the `CHANGELOG.md` using:

    $ git log --pretty=format:'  * %h - %s (%an, %ad)' vX.Y.Z..HEAD

4. Add files to git

    $ git add CHANGELOG.md pact/__init__.py

5. Commit

    $ git commit -m "Releasing version X.Y.Z"

6. Tag

    $ git tag -a vX.Y.Z -m "Releasing version X.Y.Z" && git push origin --tags

7. Wait until travis has run and the new tag is available at https://github.com/pact-foundation/pact-python/releases/tag/vX.Y.Z

8. Set the title to `pact-python-X.Y.Z`

9. Save