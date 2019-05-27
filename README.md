## What?
Axeman is a utility for downloading, parsing, and storing <a
href="https://www.certificate-transparency.org/what-is-ct">Certificate
Transparency Lists</a> using python3's concurrency and multi-processing. Its aim
is to download and parse certificates relatively quickly and efficiently,
storing them as Base64 encoded DER on the local filesystem.

This fork applies several fixes to deal with both output directory bugs in
addition to output format, deviating away from the CSV format provided.

## Installing it
Installation should be super straight forward, but you need a newer version of
python (3.5+) to run it.

```
pip3 install git+http://github.com/tphts/Axeman
```

## Usage

```
$ axeman -h
usage: axeman [-h] [-f LOG_FILE] [-s START_OFFSET] [-l] [-u CTL_URL]
              [-o OUTPUT_DIR] [-v] [-c CONCURRENCY_COUNT]

Pull down certificate transparency list information

optional arguments:
  -h, --help            show this help message and exit
  -f LOG_FILE           location for the axeman log file
  -s START_OFFSET       Skip N number of lists before starting
  -l                    List all available certificate lists
  -u CTL_URL            Retrieve this CTL only
  -o OUTPUT_DIR         The output directory to store certificates in
  -v                    Print out verbose/debug info
  -c CONCURRENCY_COUNT  The number of concurrent downloads to run at a time
```

# License
The original Axeman in addition to the changes applied within this fork are
licensed under the MIT license.
