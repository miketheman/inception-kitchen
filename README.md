# inception-kitchen

Docker-in-Docker for Test-Kitchen

## What??

Thanks to the efforts of chef, test-kitchen, kitchen-docker, we can now run tests
inside isolated, repeatable environments.

## Why!?

Running kitchen tests can be time consuming, as well as not easily automated
from GitHub pull requests.
This aims to provide a mechanism where one might trigger a series of builds based
on a commit/pull request to test the new code or behaviors.

## How?

Build this image locally like so:

    docker build --tag=inception-kitchen --rm=true .

Run it locally:

    docker run --privileged -t -i inception-kitchen

Once inside, you can test behavior with a `.kitchen.yml` file.
See [.kitchen.yml-example](.kitchen.yml-example) for an example.
