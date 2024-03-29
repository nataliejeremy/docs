---
title: Continuous Integration solutions on Pantheon
parent_guide:
  - going-live
filename: source/_docs/continuous-integration-solutions-on-pantheon.md
---

Continuous Integration is a method of running automated unit and integration tests to apply quality control. Pantheon doesn't provide or host tools for continuous integration, but many tools and techniques are compatible with Pantheon. If you have a particular use case or technique that you'd like to highlight, let us know with a support ticket!

## Terminus Command-line Interface

[Terminus](/documentation/advanced-topics/terminus-the-pantheon-command-line-interface/) is a Drush-based command-line interface (CLI) into the Pantheon core API. Most operations available through the Pantheon dashboard can be performed with Terminus, including:

- Site creation
- [Multidev environment](/documentation/advanced-topics/branching-git-workflows-for-teams-with-multidev/) creation and removal
- Content cloning
- Code pushes

Terminus can be used for scripting many operations. For example, a post-commit hook could trigger Jenkins to create a multidev environment with the latest code on master and the content from live, then run automated browser tests using [Selenium](http://www.seleniumhq.org/).

## SimpleTest on Pantheon

[SimpleTest](https://drupal.org/project/simpletest) is a testing framework based on the [SimpleTest PHP library](http://simpletest.sourceforge.net/) that is included with Drupal core. If you are creating a custom web application, then you should consider including SimpleTests of your module functionality.

After enabling the SimpleTest module, you can use Drush to remotely execute SimpleTest on your Pantheon site. For example, if you wanted to execute the UserSaveTestCase test and generate XML output into a writeable directory, use the following command:

    SITE_NAME=yoursitename
    ENV=dev
    drush @pantheon.$SITE_NAME.$ENV test-run -l http://$ENV-$SITE_NAME.gotpantheon.com/ UserSaveTestCase --xml='sites/default/files'

The end results would be written to http://dev-yoursitename.gotpantheon.com/sites/default/files/UserSaveTestCase.xml

## Known Limitations

At this time, Pantheon does not provide or support:

- [Webhooks](http://en.wikipedia.org/wiki/Webhook); this is a known feature request, no ETA yet.
- [Git hooks](http://git-scm.com/book/en/Customizing-Git-Git-Hooks); this is a known feature request, no ETA yet.
- [Jenkins](http://jenkins-ci.org/) or other Continuous Integration software (there are no plans; consider a hosted CI solution instead such as [Travis CI](https://travis-ci.com/), [CircleCi](https://circleci.com/) or [Drone](https://drone.io/))
- Shell access; this is a known feature request, no ETA yet.
- [PHPUnit](https://github.com/sebastianbergmann/phpunit/) Unit Testing PHP Framework (you can still write tests and include them in your code, but you won't be able to run the tests on Pantheon)
