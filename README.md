This is a [XMLTV](http://wiki.xmltv.org/index.php/Main_Page) grabber for [Sveriges Radio](https://sverigesradio.se).
It is implemented as a very simple shell script that downloads the daily schedules available at
https://sverigesradio.se/xmltv and merges them into a single file.

Note that there is no configuration. All radio stations are grabbed unconditionally.\
The standard `--days` and `--offset` command-line options are supported.

## Requirements

- Linux system (GNU userland)
- `curl`
- XMLTV tools (package `xmltv` or `xmltv-util` depending on distro)

## Installation

1. Download https://raw.githubusercontent.com/lbschenkel/tv_grab_se_sr/master/tv_grab_se_sr
2. Put into `/usr/local/bin` or another directory in `$PATH`
3. Make sure it's executable: `chmod a+x`

Now the grabber should be discoverable by the `tv_find_grabbers` tool:
```
$ tv_find_grabbers
/usr/local/bin/tv_grab_se_sr|Sveriges Radio (sverigesradio.se)
```

The grabber should now be visible in applications such as Tvheadend.
