Title: Bedrock Linux: News Archive
Nav: home.nav

News Archive
============

## {id="switch-osx"} Bedrock Switching to OSX (April Fools 2013)
<small>2013-04-01</small>

The April fools joke for 2013:

The primary complaint about the Bedrock OS project throughout its history is
that it is insufficiently user friend.  To quote Jonathan Corbert of Linux
Weekly News:

> [Bedrock Linux] may be especially well suited for those users who have gotten
> frustrated with the way distributions like Gentoo do everything for them.

Clearly, this needs to be remedied.  The Bedrock Linux developers feel very
strong that if you're going to do something, you should do it right, and no
Linux-based operation system has ever gotten the reputation for
user-friendliness that OSX has.  Switching to OSX is a necessity if the Bedrock
OS is ever going to become truly user friendly.

From a technical standpoint it seems quite doable.  The crux of how Bedrock
works under the hood - chroot() - is available on OSX as well.  Apple OSX is
UNIX.  Moreover, work to make things like CUPS or webkit work on Bedrock will
cleanly carry over.

Really, there isn't any downside.  This Linux thing was never going to catch on
anyways.  The upsides, though, are tremendous.  Consider:

- Rosetta - the PowerPC-x86 binary translator for OSX - is not supported on OSX
  as of 10.7 "Lion".  What about those poor people who bought software like
  Diablo 2 for OSX in the PowerPC days?  With Bedrock OSX, they can just use an
  older OSX release that supports Rosetta and play Diablo 2 on their shiny
  newer OSX!

- The latest version of OSX, as of the time of writing, has some applications
  crash when a user enters "FILE:///" into a number of text objects, such as a
  Finder window's search box.  Prior releases of OSX did not have this.  You
  could simply use an older Finder release until this is fixed!

- With Linux, the lack of standardization makes developing Bedrock OS a pain.
  If some obscure distro does things in a way the Bedrock developers are not
  familiar, it might not work out of the box as a client.  OSX, however, has a
  known number of releases.  We just have to support those.  Much easier.
  Bedrock development will likely speed up greatly once the switch has occurred.

However, converting the base project will take about one year.  Expect Bedrock
OSX to be available on April 1st, 2014.

## {id="bosco-update"} Bedrock Linux 1.0alpha3 Bosco update
<small>2013-01-16</small>

Bosco has been updated, fixing various issues.  If you are currently using a
Bosco installation from before 2012-01-16, it is recommended you update.
Download and untar the [userland](1.0alpha3/bedrock-userland-1.0alpha3.tar.gz)
to a temporary directory (such as `/tmp/bosco-update`), and replace the
following files from the core system with those from the userland tarball:

- /etc/init.d/rcS
- /etc/init.d/rcK
- /etc/init.d/rc.local
	- careful not to overwrite any settings you may have placed in here
- /bedrock/bin/brc
	- you'll have to compile the updated brc.c
		- `gcc -Wall brc.c -o /bedrock/brc/brc -static -lcap`
		- `{class="rcmd"} setcap cap_sys_chroot=ep /bedrock/bin/brc`
- /bedrock/sbin/bru

## {id="bosco-release"} Bedrock Linux 1.0alpha3 Bosco released
<small>2012-12-25</small>

The third Bedrock Linux release, 1.0alpha3 Bosco has been released.
See the high-level changelog [here](1.0alpha3/changelog.html)

## {id="linux.com-new-distros"} Bedrock Linux mentioned on linux.com
<small>2012-12-12</small>

Bedrock Linux was mentioned in an [article on
linux.com](https://www.linux.com/news/hardware/desktops/679646-6-linux-distros-born-in-2012/)
about new Linux distributions created in 2012.


## {id="website\_overhaul"} Website Overhaul, includes atom/rss
<small>2012-11-18</small>

Website overhauled.  Huge thanks to [simonlc](http://simon.lc/) for assisting
me with a new website design.  Note that the website now supports atom, and so
if you would like to follow Bedrock Linux development and news feel free to
point your RSS feed reader to "http://bedrocklinux.org/atom.xml".

## {id="bosco\_performance"} Bosco performance boosted; backported to Momo
<small>2012-11-16</small>

Bosco plans discussed [here](http://bedrocklinux.org/1.0alpha3/plans.html) have
been implemented and show a huge real-world performance boost.  This
functionality was backported to Momo for those who are interested in trying it
out before Bosco is ready.  See
[here](http://bedrocklinux.org/1.0alpha2/backports.html) for benchmarks and
instructions on how to install the backport update.

## {id="olf-2012"} Bedrock Linux at Ohio Linux Fest 2012
<small>2012-09-29</small>

Bedrock Linux's founder/lead dev is presenting Bedrock Linux today at [the Ohio
LinuxFest 2012](http://www.ohiolinux.org/talks#BEDROCK).  The slides for the
presentation are available [here](http://bedrocklinux.org/media/bedrocklinux-olf.pdf).

## {id="lwn"} Bedrock Linux is on LWN
<small>2012-09-13</small>

An article on Bedrock Linux is available
[here](http://lwn.net/Articles/515709/); however, it is currently only
available to LWN subscribers.  It will be made freely available to everyone on
September 20th, 2012

## {id="bosco\_plans"} Bosco Plans
<small>2012-09-03</small>

Plans for the upcoming release, 1.0alpha3 Bosco, are now available
[here](http://bedrocklinux.org/1.0alpha3/plans.html).  In summary, the next
release should be simpler and faster.

## {id="new\_domain"} Hosting and domain change
<small>2012-08-18</small>

Bedrock Linux is now at its own domain: bedrocklinux.org

## {id="linux\_action\_show"} Bedrock Linux mentioned on Linux Action Show
<small>2012-08-14</small>

Bedrock Linux is on [the Linux Action Show](
http://www.youtube.com/watch?v=9ca_Tm9cv1g&t=11m15s).  Relevant section goes
from 11:15-16:41.  "One of the most fascinating Linux distributions we've heard
of in years."

## {id="momo\_release"} Bedrock Linux 1.0alpha2 Momo releasd
<small>2012-08-13</small>

The second Bedrock Linux release, 1.0alpha2 "Momo" has been released.
This release primarily addresses issues brought up from the prior release as
well as contributions from others.

## {id="slashdot"} Short video demonstration of Bedrock Linux
<small>2012-08-09</small>

A short video demonstration of Bedrock Linux can be found
[here](http://www.youtube.com/watch?v=MuYMBCcgs98)
## {id="slashdot"} Bedrock Linux on Wired's website
<small>2012-08-05</small>

Bedrock Linux was very briefly mentioned on Wired magazine's website [here](http://www.wired.com/wiredenterprise/elsewhere/bedrock-linux-combines-benefits-of-other-linux-distros-20120805/)

## {id="slashdot"} Bedrock Linux on Slashdot
<small>2012-08-05</small>

Bedrock Linux is on
[Slashdot](http://linux.slashdot.org/story/12/08/05/1211244/bedrock-linux-combines-benefits-of-other-linux-distros).

## {id="momo\_release"} First public Bedrock Linux release out
<small>2012-08-03</small>

The first release of Bedrock Linux, 1.0alpha1 "Appa," is now out.
