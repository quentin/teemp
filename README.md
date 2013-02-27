teemp
=====

Transparently redirects GNU tee outputs to a shared memory directory or basically any directory.

Provides symlinks to GNU tee, backed by files stored in a ramdisk.
Actual data file name is generated using the SHA1 signature of the absolute path of the symlink file. 

    $ ls | teemp ~/out
    [...]
    $ ls -l ~/out
    lrwxrwxrwx 1 sabahq ecr 62 2013-02-19 13:24 /home/sabahq/out -> /dev/shm/teemp.sabahq/01f8195e651eb78946f47b0220e580e1499aea8b

Configuration is read from `/etc/.teemp`, `$HOME/.teemp` and `$PWD/.teemp`. 
Read the code to find out the possible key/value entries.
