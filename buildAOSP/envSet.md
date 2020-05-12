# set the env


```
Initialize the environment with the envsetup.sh script:

source build/envsetup.sh

or

. build/envsetup.sh

```

## enables:


```

    lunch - lunch product_name-build_variant selects product_name as the product to build, and build_variant as the variant to build, and stores those selections in the environment to be read by subsequent invocations of m and other similar commands.

    m - Runs builds from the top of the tree. This is useful because you can run make from within subdirectories. If you have the TOP environment variable set, it uses that. If you don't, it looks up the tree from the current directory, trying to find the top of the tree. You can either build the whole source code tree by running m without arguments or build specific targets by specifying their names.

    mma - Builds all of the modules in the current directory, and their dependencies.

    mmma - Builds all of the modules in the supplied directories, and their
    dependencies.

    croot - cd to the top of the tree.

```
