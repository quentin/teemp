teemp
=====

Redirects GNU tee outputs to a shared memory directory.

Provides symlinks to GNU tee, backed by files stored in /dev/shm/teemp.$USER/ .
Actual data file name is generated using the SHA1 signature of the absolute path of the symlink file. 

    $ ls | teemp ~/out
    [...]
    $ ls -l ~/out
    lrwxrwxrwx 1 sabahq ecr 62 2013-02-19 13:24 /home/sabahq/out -> /dev/shm/teemp.sabahq/01f8195e651eb78946f47b0220e580e1499aea8b
