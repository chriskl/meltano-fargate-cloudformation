# meltano-fargate-cloudformation

A Sceptre-based CloudFormation template for running Meltano on ephemeral Fargate tasks. Designed to work with [meltano-fargate-docker](https://github.com/HealthEngineAU/meltano-fargate-docker)

## Setup

Create a Python virtual environment:

    $ python -m venv .venv
    $ source .venv/bin/activate
    $ pip install -r requirements.txt

Customise the configuration:

    $ cp config/meltano.yaml.in config/meltano.yaml

Edit `config/meltano.yaml` and set the GitHub URL.

Create the stack

    $ sceptre create meltano.yaml
