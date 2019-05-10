# heroku-buildpack-builds

Heroku Buildpack for various build processes.

## What Projects Should I Add to This Buildpack?

If you answer yes to this question: do the build artifacts need to live inside
the Heroku image?

For example, the artifacts for the `air_lms/static/report-center` project are
pushed to S3 via the Django `collectstatic` task (which happens after the
deployment process).

## What Do I Need to Do?

1. Modify the `bin/compile` script to handle your build process.
1. Possibly modify `bin/deploy_constants.py` (in the Veelo GitLab repo) to
   accommodate your artifacts.
