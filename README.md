## Proof repository for bad core patching

This repository is to act as an example for erroneous Drupal 8 core patching with `cweagans/composer-patches` and `composer`, and nothing more.

### Branch: [example-with-error](https://github.com/amcgowanca/composer-patches-drupal-patching-proof/tree/example-with-error)

This branch contains a completely fresh Acquia BLT project setup after running the standard `composer create-project` command:

```
composer create-project --no-interaction acquia/blt-project my-project
```

You will note that there is absolutely no modifications to the standard composer.json outside of any common changes.

A complete codebase has been pushed to the branch [example-with-error-built](https://github.com/amcgowanca/composer-patches-drupal-patching-proof/tree/example-with-error-built) through the use of `git add --all --force`.

Observe that under the [docroot/core](https://github.com/amcgowanca/composer-patches-drupal-patching-proof/tree/example-with-error-built/docroot/core) directory that a subdirectory named `b` ([link](https://github.com/amcgowanca/composer-patches-drupal-patching-proof/tree/example-with-error-built/docroot/core/b)) exists, as well as an additional `core` ([link](https://github.com/amcgowanca/composer-patches-drupal-patching-proof/tree/example-with-error-built/docroot/core/core)) directory.

### Branch: [example-without-error]()

This branch contains a few minor modifications to the project's root `composer.json` file in which it makes use of the revised `cweagans/composer-patches` project and additional Composer plugin named [composer-patches-drupal-patching](https://github.com/amcgowanca/composer-patches-drupal-patching).

A completely built codebase, similar to that of the _example-with-error-built_ is available named [example-without-error-built](https://github.com/amcgowanca/composer-patches-drupal-patching-proof/tree/example-without-error-built). This was similarly created through the use of `git add --all --force` upon executing a `composer install` with the modified `composer.json`.

Observe that under the [docroot/core](https://github.com/amcgowanca/composer-patches-drupal-patching-proof/tree/example-without-error-built/docroot/core) directory no longer contains the additional or new subdirectories `b` or `core` _and_ that patches have *in fact* been applied to Drupal core where they previously were not.
