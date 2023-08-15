# Typst Bot

A Discord bot that renders Typst code.

Built with poise so it has all the goodies like edit tracking, typing status, and automatic help generation.

## Hosting

The bot uses two binaries:

- `bot`: connects to Discord and processes messages
- `worker`: receives requests, interacts with Typst, responds

`bot` will automatically spawn `worker`, so you only need to run `bot`.

To set up the working environment, create a directory with the following items:

- `fonts`: Copied from the repo. Make sure you have Git LFS set up so the fonts are downloaded properly.
- `worker`: The worker binary, copied/hardlinked from the target directory after building.
- `bot`: The bot binary, copied/hardlinked from the target directory after building. (This doesn't need to be in this directory, but having everything in one place simplifies things.)

To run, CD into this directory, set `DISCORD_TOKEN` to your bot token, and run the `bot` binary (not the `worker` binary that's also in the directory).

To allow use of packages, set `CACHE_DIRECTORY` to a directory to download and read packages from.

## License

AGPL. Use `?source` to get a link to the source from deployments of the bot.
