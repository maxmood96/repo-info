## `varnish:latest`

```console
$ docker pull varnish@sha256:b82ab28f118683d78f51def75548dfe69f43ff8e99b38941f947530d1b908563
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:4039140b76232eec80a20cc88ac433bbb4727d03696b0a835ee78b001fe9cdbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134242696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a98a8567bf1308d835b8d3ed2f1160c60b8c8f020f14404a006c509f94380d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e40b94aefb1b6d8ae5d6c53ce49a74edfe3c31c5a9c77ae1d6f9740c2dd339`  
		Last Modified: Tue, 14 Jan 2025 02:20:04 GMT  
		Size: 106.0 MB (106028247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778a4381aafd09f111a97ef6e1b8f52c3ac35d691f1e3b1d41dcbffff26530fb`  
		Last Modified: Tue, 14 Jan 2025 02:19:59 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd612d0fbd41fb76959af36b18c84c20b0c3b4c181aa6ddcee4a40af948b418`  
		Last Modified: Tue, 14 Jan 2025 02:19:59 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:00a58d0b02b8fff240e73279c1e41dc7f36c7ebfff04845bc8bd34bca5f57d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c3483b951e10dd84212149d450361d9b4a8e5ea6811feba8ad757cbb724172`

```dockerfile
```

-	Layers:
	-	`sha256:c8f205b98193da43ad58d7c9b0c5521a71d2e88e834fb1291c6097fe2882fb99`  
		Last Modified: Tue, 14 Jan 2025 02:19:59 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a9852d834bf8d60efa0d69bbb18bb417aa71282c36483181dcf8321fad20bda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104591775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7564f3bb7e0a54c2b0d65dbc3bf5018c7da60b71afe88daea643e02fa88e1578`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319ae97b2e04b000f81a8da8231bc26e22089dd585b9a39f084b5fb619bda967`  
		Last Modified: Wed, 25 Dec 2024 03:38:12 GMT  
		Size: 80.7 MB (80656222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f75f80d39226a75bc8de59ed5280115d0f23b163a86c4813514ad799ca8ab`  
		Last Modified: Wed, 25 Dec 2024 03:38:09 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be1e2e997886b8cd15d9aad2ecef090a72ebd937bfa5159c4d0003c22ccf3dd`  
		Last Modified: Wed, 25 Dec 2024 03:38:10 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:6b37db258657e646c4f8566d0652be06c1484902e72d04ae7c709287672f32f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9cb6392b1c8f40e6d18ee3bb5415edcdf6a7fcf182b19b5db321b4999f2f22`

```dockerfile
```

-	Layers:
	-	`sha256:ebf8d8e9cf9fee557dd5001ba8cf13dfeafc3dba97daf3c53aad00c2949d6f9a`  
		Last Modified: Wed, 25 Dec 2024 03:38:09 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:11a759fcc6bce4d2613815177fc5b858e6f12c2c5c67ac95ef518d101572aa52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128539442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095c37d7892029d44e3778c5e1ca464b91759715ca0d5edf1d3f9401e4b87237`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4589ae8959d23ead7f6e706e881e24555de316bd0fe65f2e8652257084ef6f`  
		Last Modified: Wed, 25 Dec 2024 01:44:04 GMT  
		Size: 100.5 MB (100478690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f50b3b3ae2eead325939f741c850ce3c95f807b8b3a542a02592bc365fccdb`  
		Last Modified: Wed, 25 Dec 2024 01:44:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8b89fcf47499fee976e191029b871d50bca465c6ae96f1c553e554929fbb75`  
		Last Modified: Wed, 25 Dec 2024 01:44:01 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:22a32b9449eb950df602c88ec2a0368e399f501a2dfc760cbd83ba34d555f6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed390fda33685444617b95b6164bfea6c3f044da2bfad16cd2712e8aa71778c`

```dockerfile
```

-	Layers:
	-	`sha256:6f834baa23179396d1ed8bb4330862b0e3002509fc668e4df3cf425d469b3056`  
		Last Modified: Wed, 25 Dec 2024 01:44:01 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:7e9fddd1d278d74973967d101a0455000513bdeafce00948b4ea9344b9402795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131328263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1aa983d2e6be3df290433486eda5fd56ad576fdfa0752182eb9c0cab04b6a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb4468a2acada0f145ed2fd4521ed8248e291fc4b01fc2ccac3aec1a345e98`  
		Last Modified: Tue, 14 Jan 2025 02:34:55 GMT  
		Size: 102.1 MB (102138633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ababe885647448dbfeeb322ed9d09121a10ab7cb2759ee9573afca198c8f9b1`  
		Last Modified: Tue, 14 Jan 2025 02:34:51 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d187f573e92221dd412e334803b58457aa24406505e6d6f07240791348331877`  
		Last Modified: Tue, 14 Jan 2025 02:34:51 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:a3b660558f6f38b5615b8cf42da7297c5fa443bb7dcdfb60cb3596d1dfad11c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afe5d18424cfbe50dd391621e83dd941a280a5cad9455a2b094326a3558a4bc`

```dockerfile
```

-	Layers:
	-	`sha256:944ff41e3cf2f4d6599c6f057d70816be9f42f6b9c4e39acf2b0a54dcd4e209f`  
		Last Modified: Tue, 14 Jan 2025 02:34:51 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:023956b82e9a1d9c9bb184334f4b7b9199c66381c24f428c897f5d4a7400474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137011865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748f3334be11673591b49c72941ef4d1cfa9237427d24bee54a5258588b71aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bddbff44e0d90b074d9252780960e743d65647400597bdbdb723bd5f9bfe803`  
		Last Modified: Tue, 14 Jan 2025 05:17:46 GMT  
		Size: 105.0 MB (104964983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95ccf741d55e2393a51c73fd89317f3547d5adb7207dbde5537afc3658ae86`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ddfad3345715772448bcf8f5c45dfe64cbea01e0ea80d3ba7c3b7017ade57`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:ccfa4ec81beea4b85eb4896509d2d04ff65ad6a685b0bc603e2f715d7b928a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa66aabb06da34b938cc62ea7b7a45196de3d0760ad94174a4a248bee7daa84d`

```dockerfile
```

-	Layers:
	-	`sha256:cecd8427a1bfba726b6d75bff2d19dadfce919cd4b4f62886d38f8a4cf02efba`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:e2658e2b46db161c995e14a46b8c86e2b05dc52e2cd75659a137f647a0003ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112112393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0144263695361fa97ddcffd6c3c9e365b173d3762af5d764c3c42cd60689cdc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f774a4d8b78e92bed8a0db33c73b450dcc47592fda460bc69effd0c061b09`  
		Last Modified: Tue, 14 Jan 2025 04:53:05 GMT  
		Size: 85.3 MB (85251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d03d5f51f4613e32fd2d3b277656f0203dd8009b2f6e316eddcebc5673a33`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3f67992ed74220778b755e60f7b81a6c917eb1adcd846f3f8afacd330ac60`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:0ed1c02bb35bcc48d4ba11375bd017df3aadeba9577ccd32dc79760544ab8cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f9efc6ce720fdc68b64ba55e6b126ded9de51d7b46334bd48b8042023cfd05`

```dockerfile
```

-	Layers:
	-	`sha256:3bca138d1c90f55120aa3f3e4314121ca90f7142456f54a8cc8c7d86640772fd`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json
