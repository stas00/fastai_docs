# Portable Link Checker

This is https://github.com/w3c/link-checker with some custom tweaks.



## Usage

Run the self-contained perl executable:

```
./checklink-linux [...]
```



## Build

The rest of the information is for those who can't use the above executable as is.


## Using the perl script directly

You of course don't need the executable, just install its prerequisites with:

```
cpanm W3C::LinkChecker
```

or via CPAN shell:

```
perl -MCPAN -e shell
install install W3C::LinkChecker
```

and now you can invoke `./checklink` directly.


## Building the executable

If for any reason you need to update the executable (or make one for another platform), install the script's dependencies (previous step), the build tools and then make the executable.

## Build tools prerequisites

Install Perl PAR Packager:

```
sudo apt install libpar-packer-perl
```

or via cpanm:

```
cpanm pp
```

or via CPAN shell:

```
perl -MCPAN -e shell
install pp
```

## Build the portable version of the tool

This will build a portable executable version for your platform (it's portable in a sense that it doesn't need any of its many dependencies). e.g. for linux:

```
cd checklink
pp -o checklink-linux checklink
```
