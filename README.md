I'd like to come up with a set of criteria to objectively analyze toolchains.

Note that this criteria can be re-evaluated for any variation of a particular brand of toolchain.  For example, gcc may be compiled statically or with runtime dependencies, and each varition will have a very different analysis.

* Portability
    - size
    - system dependencies
    - install footprint (how many places in the system are touched when installed)
    - can multiple versions be installed?
* Versatility
    - how many platforms can the same binaries run on?
    - cross-compilation? how many platforms can you compile for?
* Maintainability
    - what is required to submit changes/fixes to the toolchain?
    - how long does it take to submit a change?
    - what does it take to file a bug report?
    - how long does it take for a bug report to be fixed?


### Prebuilt Binaries

In the following I use the term "prebuilt binaries" to refer to the set of files required to run the toolchain, including any runtime dependencies.  For example, if the toolchain uses the libc runtime library, then that would be included in the term "prebuilt binaries".

* Where can the prebuilt binaries be downloaded from?
* How big are the prebuilt binaries?
* How many disjoint directories do the prebuilt binaries occupy?  What's the minimum number of directories the toolchain can be isolated to?
* How Does the toolchain have any runtime dependencies?  If so, how big are they? How would someone find/determine where those runtime dependencies will be found?
* How many sets of binaries does it take to run on the full set of standard platforms?
    - Windows 7, 8, 10?
    - Linux? Is it distro specific?
    - BSD?
    - MAC?

* Along with the toolchain, how many extra dependencies does it take to build the toolchain?
* How many variations of prebuilt binaries are there?

* Could you copy the toolchain from one machine to another? Will it work?  How many different types of platforms will your binaries work on?

* Does the toolchain cross-compile?
