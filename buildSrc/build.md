# build

* Build everything with m
* m can handle parallel tasks with a -jN


## m pseudotargets


```

    droid - m droid is the normal build. This target is here because the default target requires a name.
    all - m all builds everything that m droid does, plus everything that doesn't have the droid tag. The build server runs this to make sure that everything that is in the tree and has an Android.mk file builds.
    clean - m clean deletes all of the output and intermediate files for this configuration. This is the same as rm -rf out/.

```
