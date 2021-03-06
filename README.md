# pyrocore

A collection of tools for the BitTorrent protocol and especially the rTorrent client.

![rtcontrol + curses demo](https://raw.githubusercontent.com/pyroscope/pyroscope/master/pyrocore/docs/videos/rtcontrol-curses.gif)

The `PyroScope` command line utilities are *not* the same as 
[rTorrent-PS](https://github.com/pyroscope/rtorrent-ps),
and they work perfectly fine without it;
the same is true the other way 'round.
It's just that both unsurprisingly have synergies if used together,
and some features *do* only work when both are present.


## Introduction

``pyrocore`` is part of the
[PyroScope](https://github.com/pyroscope/pyroscope/blob/wiki/PyroScope.md)
family of projects, and offers a collection of tools for the
[BitTorrent protocol](https://github.com/pyroscope/pyroscope/blob/wiki/BitTorrent.md)
and especially the rTorrent client. This includes:

 * [CommandLineTools](https://github.com/pyroscope/pyroscope/blob/wiki/CommandLineTools.md) for automation of common tasks, like metafile creation, and [filtering and mass-changing your loaded torrents](https://github.com/pyroscope/pyroscope/blob/wiki/RtControlExamples.md).
 * rTorrent extensions like a [QueueManager](https://github.com/pyroscope/pyroscope/blob/wiki/QueueManager.md) and statistics (_work in progress_).
 * All this is based on the `pyrocore` Python package, that you can use to [write your own scripts](https://github.com/pyroscope/pyroscope/blob/wiki/WriteYourOwnScripts.md) for any special needs that aren't covered by the standard tools.

See the
[ScreenShotGallery](https://github.com/pyroscope/pyroscope/blob/wiki/ScreenShotGallery.md)
if you want to get a first impression without installing the software.

To get in contact and share your experiences with other users of PyroScope,
join the [pyroscope-users](http://groups.google.com/group/pyroscope-users) mailing list
or the inofficial ``##rtorrent`` channel on ``irc.freenode.net``.


## Installation

To install the software, use the following commands:

```sh
# To be executed in a shell with your normal user account!
mkdir -p ~/bin ~/lib
git clone "https://github.com/pyroscope/pyrocore.git" ~/lib/pyroscope

# Pass "/usr/bin/python2" or whatever to the script,
# if "/usr/bin/python" is not a suitable version
~/lib/pyroscope/update-to-head.sh

# Check success
rtcontrol --version
```

You can choose a different install directory, just change the paths accordingly.

:loudspeaker: | If you want to switch over from an old installation based on subversion source (from [Google code](https://code.google.com/p/pyroscope/)), then _move that old directory away_, before installation! Like this:
---- | :----
:computer: | ``( cd ~/lib && mv pyroscope pyroscope-$(date +'%Y-%m-%d').bak )``


## Customization

It's very easy to
[WriteYourOwnScripts](https://github.com/pyroscope/pyroscope/blob/wiki/WriteYourOwnScripts.md)
to automate anything that the standard commands can't do.


## External Links

 * [User Mailing List](http://groups.google.com/group/pyroscope-users)
 * [rTorrent Homepage](http://libtorrent.rakshasa.no/)
 * [rTorrent Community Wiki](http://community.rutorrent.org/PyroScope)
 * [Open HUB](https://www.openhub.net/p/pyroscope/)
 * [free(code)](http://freecode.com/projects/pyrocore)
 * [Bintray](https://bintray.com/pkg/show/general/pyroscope/rtorrent-ps/rtorrent-ps)
 * [pyrobase](https://github.com/pyroscope/pyrobase/wiki)


## News

Date     | Description
:-------------------: | :----
*14–Mar–2015* | Moved from [Google Code](https://code.google.com/p/pyroscope/ ) to [GitHub](https://github.com/pyroscope/pyroscope). Documentation will be in a limbo state and spread over both sites for some time, I'll try to reasonably cross-link.
*05–Jun–2011* | [pyrocore 0.4.2](http://freshmeat.net/projects/pyrocore/releases/332769) released.
*17–Apr–2011* | [pyrocore 0.4.1](http://freshmeat.net/projects/pyrocore/releases/331021) released.
*05–Mar–2011* | [pyrocore 0.3.10](http://freshmeat.net/projects/pyrocore/releases/329060) released.
*05–Sep–2010* | [pyrocore 0.3.7](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.3.7) released, offering automatic classification for completion paths, a working `rtmv` in symlinked mode, grouping of filter conditions, rTorrent fast-resume support, and better cron logging.
*29–Aug–2010* | [pyrocore 0.3.6](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.3.6) released, featuring more torrent life-cycle fields, selecting into rTorrent views, file listings and filtering based on file type, and finer control over formatting pathname fields.
*28–Aug–2010* | Published the [API documentation](http://packages.python.org/pyrocore/apidocs/index.html) in Javadoc style including class diagrams and cross-referenced source code.
*20–Aug–2010* | [pyrocore 0.3.5](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.3.5) released, adding custom attributes and item tagging, and column headers to result listings.
*16–Aug–2010* | [pyrocore 0.3.4](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.3.4) released, with a finished `chtor` and new `rtxmlrpc` tool, additional fields containing load and completion time, and action options to delete or throttle items, or put them under manual control.
*20–Mar–2010* | [pyrocore 0.3.3](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.3.3) released, including many new `chtor` options, and some `rtcontrol` improvements.
*14–Mar–2010* | [pyrocore 0.3.2](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.3.2) released, allowing you to mass-start/stop items in a selection result.
*13–Mar–2010* | [pyrocore 0.3.1](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.3.1) released, adding filtering, sorting and output formatting to `rtcontrol`.
*08–Mar–2010* | [pyrocore 0.2.1](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.2.1) released, with new tools `chtor` and `pyroadmin`, and a finished configuration system.
*19–Feb–2010* | First release of `pyrocore` ([v0.1.1](http://pypi.python.org/pypi?:action=display&name=pyrocore&version=0.1.1)), containing the `lstor` and `mktor` utilities.
