# Rocket web backend application

## About
This is a project based on a fork of ![Rust web boilerplate](https://github.com/svenstaro/rust-web-boilerplate). 

## Development setup

Install a few external dependencies and make sure `~/.cargo/bin` is in your `$PATH`:

    cargo install diesel_cli
    cargo install watchexec

Set up your environment by sourcing `local_env.sh`.

    source local_env.sh

For every new shell you need to source this file and you're good to go.

Make sure you have a working local postgres setup. Your current user should be
admin in your development postgres installation and it should use the "peer" or
"trust" auth methods (see `pg_hba.conf`).

Now you can launch the `watch.sh` script which helps you quickly iterate. It
will remove and recreate the DB and run the migrations and then the tests on
all code changes.

    ./watch.sh
