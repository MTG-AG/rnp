Prerequisites
=============

Compile
=======

(Prefix /usr/local by default)
```
./build.sh
make install
```

Clean build artifacts
=====================
```
./remove_artifacts.sh
```

Otherwise use `git clean`.

Running commands
================

```
netpgp
netpgpkeys
netpgpverify
```

Building RPM
============

Start container:
```
docker run -v ~/src/netpgp:/usr/local/netpgp -it centos:7 bash
```

Set up build environment.
```
/usr/local/netpgp/packaging/redhat/extra/prepare_build.sh
```

Run the rpmbuild script.
```
cd /usr/local/netpgp
./remove_artifacts.sh

cd /usr/local
netpgp/packaging/redhat/extra/build_rpm.sh
```

