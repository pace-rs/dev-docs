# Frequently asked technical questions

## How does pace store my data?

Pace stores your data in a TOML file for now. This is a simple and
human-readable format that is easy to parse and write - and to backup. Read more
about how pace utilizes the
[storage](https://pace.cli.rs/docs/data_management/activity_log_storage.html).

## How can I import my data from other time tracking tools?

Pace currently does not support data import, but it is planned for the near
future. The data is stored in a human-readable format, so you can always convert
it manually. Or write a script to do it for you. The
[storage format](https://pace.cli.rs/docs/data_management/activity_log_storage.html#storage-format)
is documented.

## Can users integrate pace with other tools?

Pace currently does not support integrations, but it is planned for the near
future. The data is stored in a human-readable format, so you can always write a
script to do it for you. This is a bit cumbersome, also when it comes to syncing
data. The idea is to have a plugin system, where you can write your own plugins
to integrate with other tools.

## How can I export my data to other time tracking tools?

Pace currently does not support data export, but it is planned for the near
future. The data is stored in a human-readable format, so you can always convert
it manually if you need to. Or write a script to do it for you.

## Will users be able to use pace on mobile devices?

Pace is a command-line tool and is not designed to be used on mobile devices.
However, you can use it on a server and access it via a web interface. This is
planned for the near future. Also different frontends are planned for the
future, for Desktop and Mobile.
