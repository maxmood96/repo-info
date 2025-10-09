<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.16`](#varnish6016)
-	[`varnish:7.7`](#varnish77)
-	[`varnish:7.7-alpine`](#varnish77-alpine)
-	[`varnish:7.7.3`](#varnish773)
-	[`varnish:7.7.3-alpine`](#varnish773-alpine)
-	[`varnish:8`](#varnish8)
-	[`varnish:8-alpine`](#varnish8-alpine)
-	[`varnish:8.0`](#varnish80)
-	[`varnish:8.0-alpine`](#varnish80-alpine)
-	[`varnish:8.0.0`](#varnish800)
-	[`varnish:8.0.0-alpine`](#varnish800-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:478db776da03729215b20dd81277050cdd0464615cf4b45f7a86f4e535bca453
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

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:edbcf0cd549f53684fc336b974b1c3fe89cb9a2af5a5a2f136777a226581e3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69a36386db13b384d7adf8030bd4311732d4338a012187246d7fe640abcef87`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021bd6671d3c11349807a74fa9eed35c5ab7ae0b1861bdbad9e0c1f3bb0836c5`  
		Last Modified: Tue, 30 Sep 2025 21:32:34 GMT  
		Size: 75.3 MB (75320304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283d977df10b07fad39caa773e480b85b2316bb0210df4529286f9e3f64071df`  
		Last Modified: Tue, 30 Sep 2025 20:32:52 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:fdaad8c93b08a3788a9b33f4ad7ea9f826c4629f41078677b7d301d48a4a63d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db71b02b550e84775078b00b1c320ba9a498e132b71f30dea306cc2e8262af21`

```dockerfile
```

-	Layers:
	-	`sha256:fa7091d13984269be7930011aabfc70e936efb08c9c46386147647138e188614`  
		Last Modified: Tue, 30 Sep 2025 21:32:14 GMT  
		Size: 12.7 KB (12692 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a30882f2f37a7f0c60fbc676321e0459df53287e851da20a26afb21e5bd4fe0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75968311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606aaec99eb1f0b5e0f508c8d4be2e4ee5e7d497756758d76fa46bc159c51614`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b53a6933c8cb5576fd491d862f80ae9c4b4b40f9e404254e245cfd5f745416e`  
		Last Modified: Tue, 30 Sep 2025 01:06:27 GMT  
		Size: 52.0 MB (52033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926848c99eb438a02a41f571b7177bee432513f7919ef280589d71bd84cdcd8`  
		Last Modified: Tue, 30 Sep 2025 01:06:24 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:71169cedf935771cd7e0c53ade969c8c4d720d487a19da86f088656405d4fc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2444ba45a8498982ac7273cd3295dd1a4df75adc41da91a5d008b7c11ce2f89`

```dockerfile
```

-	Layers:
	-	`sha256:57d8d64e3d2e1be41e57ac45ca90c81533539687a60caa9892abe362e1918835`  
		Last Modified: Wed, 01 Oct 2025 21:19:21 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a2aac0559b353cb60b49686e387cc2369c4fe84952783f965980c226fdc77207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98404617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda087f571e171269283c9c4e691e2a8d665240031fbd46506953c181f299498`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a9b5f2ef0a48e29a325995aaa014a02ee8e27a2d6b6c7f1eae706c5e6e5a4`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 70.3 MB (70301719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62acb4a8b52242bb4d121dca852e3cdee447dd87cddb494c3ec202454bdee7a`  
		Last Modified: Tue, 30 Sep 2025 00:15:08 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:94e57ecd1d41808eb3bc924d4c61c2571da38d126a5a21a235927117d40e3f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5269aab6856b2cce907b5896eedda8a0baf058f610e832b67fdf302adc2f2b17`

```dockerfile
```

-	Layers:
	-	`sha256:fb18672428481ccd161b086f4a89f40e1684dbc5a7129fa72cca8c9981cdc789`  
		Last Modified: Tue, 30 Sep 2025 12:19:44 GMT  
		Size: 12.8 KB (12784 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:770c31fec1c0d1e8bb18b3f73130aa7d7b9cedbd371f68718c46015db8093d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101009937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7369af1ac997223f89a186307d3cf0ad66d6c7483d96e030e3d2bf70e54178d5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac062943d6dbf85d9967efb33f240d7174233498ecefeae11fc3e752e4b701a6`  
		Last Modified: Tue, 30 Sep 2025 15:11:14 GMT  
		Size: 71.8 MB (71799554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acb1e036848264770a871e40dbc8f57b501eaa6a3973e6d6002bd0469ae1eac`  
		Last Modified: Tue, 30 Sep 2025 01:11:00 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:0540529c49b2c9cf0341f115c4e4de158e14ccd3eeb46eecf643fcd720a151c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612d547d40a94907dee9f043de061252f518a847f289ed29eea07e8b3e42a9f5`

```dockerfile
```

-	Layers:
	-	`sha256:284ab7a9bc5e80ab20f48608dfda7f7e25be01c46c4bd04faa1880a3d4647191`  
		Last Modified: Tue, 30 Sep 2025 15:21:15 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:33614a26f6cf8caaa6f149d237e8dd550625d372a6e2b55440dec6460c6c45de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105448843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ede35632676bf8b6077af4627923c4ac550c5ad7f3aaddf472ff1b8afff799`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37332b11d69c63d3807d704d5c4810b1837ad185ea9efd87f1cf803b9db772a`  
		Last Modified: Tue, 30 Sep 2025 02:23:32 GMT  
		Size: 73.4 MB (73379392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6c6b5317a767b461b18bc3a77bda753e29cde5c9470fcf71a103464c668137`  
		Last Modified: Tue, 30 Sep 2025 02:23:17 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:393d1b4f9ce8a87d7da85c90cb4e5de595ea7ebdb070e6289542af8d34986bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3f98654479446cb0b375bc94b3731300338118952d9a3f27113fa8c1b70aa0`

```dockerfile
```

-	Layers:
	-	`sha256:d644c1c9995c7a7a09c28e819ff1ae53125e36d54a241916937b065617c785c2`  
		Last Modified: Wed, 01 Oct 2025 21:19:28 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:dd816940571162d6ee1e989f9c9952bae13cf153bcea3e5e5fa9654f6d81d3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81335071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e39171b878b614da5e82f45d179d7fde3eb76ff4017254c2e737115caa4513f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e5a4571b8763222bc9df6252308856a003d945316511f14da7b7c397cbbcfa`  
		Last Modified: Wed, 01 Oct 2025 00:30:47 GMT  
		Size: 54.4 MB (54449997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d87403c37cdba5b295b8dd02cb3c9a68249c1ca86a8658955712801fc9edd1`  
		Last Modified: Tue, 30 Sep 2025 03:57:19 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:67fbf88ebd64cd482b3ba39fb4aa2617c9d8e90112d0a7220dc93a23b0ca31d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382986cfda5f76f4c8b9ff355bf4142f88e49fc7f32b7e0462c284caae2ca060`

```dockerfile
```

-	Layers:
	-	`sha256:7c98189558027159262d622199a4fa7eed6df5488f9ea32417c53665e9081ff5`  
		Last Modified: Wed, 01 Oct 2025 00:30:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.16`

```console
$ docker pull varnish@sha256:478db776da03729215b20dd81277050cdd0464615cf4b45f7a86f4e535bca453
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

### `varnish:6.0.16` - linux; amd64

```console
$ docker pull varnish@sha256:edbcf0cd549f53684fc336b974b1c3fe89cb9a2af5a5a2f136777a226581e3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69a36386db13b384d7adf8030bd4311732d4338a012187246d7fe640abcef87`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021bd6671d3c11349807a74fa9eed35c5ab7ae0b1861bdbad9e0c1f3bb0836c5`  
		Last Modified: Tue, 30 Sep 2025 21:32:34 GMT  
		Size: 75.3 MB (75320304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283d977df10b07fad39caa773e480b85b2316bb0210df4529286f9e3f64071df`  
		Last Modified: Tue, 30 Sep 2025 20:32:52 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:fdaad8c93b08a3788a9b33f4ad7ea9f826c4629f41078677b7d301d48a4a63d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db71b02b550e84775078b00b1c320ba9a498e132b71f30dea306cc2e8262af21`

```dockerfile
```

-	Layers:
	-	`sha256:fa7091d13984269be7930011aabfc70e936efb08c9c46386147647138e188614`  
		Last Modified: Tue, 30 Sep 2025 21:32:14 GMT  
		Size: 12.7 KB (12692 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a30882f2f37a7f0c60fbc676321e0459df53287e851da20a26afb21e5bd4fe0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75968311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606aaec99eb1f0b5e0f508c8d4be2e4ee5e7d497756758d76fa46bc159c51614`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b53a6933c8cb5576fd491d862f80ae9c4b4b40f9e404254e245cfd5f745416e`  
		Last Modified: Tue, 30 Sep 2025 01:06:27 GMT  
		Size: 52.0 MB (52033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926848c99eb438a02a41f571b7177bee432513f7919ef280589d71bd84cdcd8`  
		Last Modified: Tue, 30 Sep 2025 01:06:24 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:71169cedf935771cd7e0c53ade969c8c4d720d487a19da86f088656405d4fc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2444ba45a8498982ac7273cd3295dd1a4df75adc41da91a5d008b7c11ce2f89`

```dockerfile
```

-	Layers:
	-	`sha256:57d8d64e3d2e1be41e57ac45ca90c81533539687a60caa9892abe362e1918835`  
		Last Modified: Wed, 01 Oct 2025 21:19:21 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a2aac0559b353cb60b49686e387cc2369c4fe84952783f965980c226fdc77207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98404617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda087f571e171269283c9c4e691e2a8d665240031fbd46506953c181f299498`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a9b5f2ef0a48e29a325995aaa014a02ee8e27a2d6b6c7f1eae706c5e6e5a4`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 70.3 MB (70301719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62acb4a8b52242bb4d121dca852e3cdee447dd87cddb494c3ec202454bdee7a`  
		Last Modified: Tue, 30 Sep 2025 00:15:08 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:94e57ecd1d41808eb3bc924d4c61c2571da38d126a5a21a235927117d40e3f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5269aab6856b2cce907b5896eedda8a0baf058f610e832b67fdf302adc2f2b17`

```dockerfile
```

-	Layers:
	-	`sha256:fb18672428481ccd161b086f4a89f40e1684dbc5a7129fa72cca8c9981cdc789`  
		Last Modified: Tue, 30 Sep 2025 12:19:44 GMT  
		Size: 12.8 KB (12784 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; 386

```console
$ docker pull varnish@sha256:770c31fec1c0d1e8bb18b3f73130aa7d7b9cedbd371f68718c46015db8093d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101009937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7369af1ac997223f89a186307d3cf0ad66d6c7483d96e030e3d2bf70e54178d5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac062943d6dbf85d9967efb33f240d7174233498ecefeae11fc3e752e4b701a6`  
		Last Modified: Tue, 30 Sep 2025 15:11:14 GMT  
		Size: 71.8 MB (71799554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acb1e036848264770a871e40dbc8f57b501eaa6a3973e6d6002bd0469ae1eac`  
		Last Modified: Tue, 30 Sep 2025 01:11:00 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:0540529c49b2c9cf0341f115c4e4de158e14ccd3eeb46eecf643fcd720a151c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612d547d40a94907dee9f043de061252f518a847f289ed29eea07e8b3e42a9f5`

```dockerfile
```

-	Layers:
	-	`sha256:284ab7a9bc5e80ab20f48608dfda7f7e25be01c46c4bd04faa1880a3d4647191`  
		Last Modified: Tue, 30 Sep 2025 15:21:15 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; ppc64le

```console
$ docker pull varnish@sha256:33614a26f6cf8caaa6f149d237e8dd550625d372a6e2b55440dec6460c6c45de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105448843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ede35632676bf8b6077af4627923c4ac550c5ad7f3aaddf472ff1b8afff799`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37332b11d69c63d3807d704d5c4810b1837ad185ea9efd87f1cf803b9db772a`  
		Last Modified: Tue, 30 Sep 2025 02:23:32 GMT  
		Size: 73.4 MB (73379392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6c6b5317a767b461b18bc3a77bda753e29cde5c9470fcf71a103464c668137`  
		Last Modified: Tue, 30 Sep 2025 02:23:17 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:393d1b4f9ce8a87d7da85c90cb4e5de595ea7ebdb070e6289542af8d34986bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3f98654479446cb0b375bc94b3731300338118952d9a3f27113fa8c1b70aa0`

```dockerfile
```

-	Layers:
	-	`sha256:d644c1c9995c7a7a09c28e819ff1ae53125e36d54a241916937b065617c785c2`  
		Last Modified: Wed, 01 Oct 2025 21:19:28 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; s390x

```console
$ docker pull varnish@sha256:dd816940571162d6ee1e989f9c9952bae13cf153bcea3e5e5fa9654f6d81d3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81335071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e39171b878b614da5e82f45d179d7fde3eb76ff4017254c2e737115caa4513f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e5a4571b8763222bc9df6252308856a003d945316511f14da7b7c397cbbcfa`  
		Last Modified: Wed, 01 Oct 2025 00:30:47 GMT  
		Size: 54.4 MB (54449997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d87403c37cdba5b295b8dd02cb3c9a68249c1ca86a8658955712801fc9edd1`  
		Last Modified: Tue, 30 Sep 2025 03:57:19 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:67fbf88ebd64cd482b3ba39fb4aa2617c9d8e90112d0a7220dc93a23b0ca31d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382986cfda5f76f4c8b9ff355bf4142f88e49fc7f32b7e0462c284caae2ca060`

```dockerfile
```

-	Layers:
	-	`sha256:7c98189558027159262d622199a4fa7eed6df5488f9ea32417c53665e9081ff5`  
		Last Modified: Wed, 01 Oct 2025 00:30:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:9310a9cbdb61b632afb83fff44fa7c71b90f987a0587d23fc159e3b22334d577
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

### `varnish:7.7` - linux; amd64

```console
$ docker pull varnish@sha256:feb27787cd34f85263e0c591a947c90a01ca9082d4db5e8d56ce8fd39ececd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116344965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0192faac62b9eec84df7907e4eb139a9ea473cc3e7c57c78c15aa40651aeff5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b82bb006d56a9a208eca4bffb9e1e098368320b3fab7f67cdc2dd79dad4c86`  
		Last Modified: Tue, 30 Sep 2025 21:33:06 GMT  
		Size: 86.6 MB (86565152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7cb22c2f76de71127b4e09b5455fc95836614c6c0c5a941181219883745b5e`  
		Last Modified: Tue, 30 Sep 2025 01:05:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036dd63ac5b112d011fa5fda2c3d53d5384ef1b2e12fc332f168fa0e9b92bf9d`  
		Last Modified: Tue, 30 Sep 2025 01:05:11 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:d2c49efdb9688d0933b973d5d4f3c3121cdc3bffddbb2400a1bff80fa5744200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aeaece4ccec8dbdfa7a985432df4a634c5bab3e367c8f0b727ea27947260e6`

```dockerfile
```

-	Layers:
	-	`sha256:09149e48eec29e1632ede18e8bcc7660017d23659e476a5c05e21b76af9fa71a`  
		Last Modified: Tue, 30 Sep 2025 21:32:47 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9a0a576248e3d011b4947e5a74e61c5c7ff29f38ff030eb06baa9550348ff161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87152968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d5b118f151e98200705c07123a2452e185dc36beb379bf01a3959e6d7120a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3ef5967cc3af519476a7d1003a8c50ff757dc2ad6fc3efb554c5930835bdef`  
		Last Modified: Tue, 30 Sep 2025 01:07:11 GMT  
		Size: 60.9 MB (60938163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df71cd8f1ded8d32285abf30be2878d4c27c61bbf4dd27fddfa6756af4dfca15`  
		Last Modified: Tue, 30 Sep 2025 01:07:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf0fae6e41dd18ce4bd19f5903c4ccf7a8c60af8a43028ba0473bbed6f182a`  
		Last Modified: Tue, 30 Sep 2025 01:07:06 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:32ae2e7ec68987e97ca435fa46c0032a9b3632ac990b17dbc97c57dab02f7c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f763821ad5c8f0de3985f062c5a06915836b0d147d1cd3784c8cc1409dd3c90d`

```dockerfile
```

-	Layers:
	-	`sha256:3b3061b7c84355510b63919b85ac719ff16b89a1896f7110d335a8596e589096`  
		Last Modified: Wed, 01 Oct 2025 21:19:33 GMT  
		Size: 19.1 KB (19132 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0d7c1c994530d1ed1ca5853a890e344630822f13d8d9178cac04b849b59c52cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110523275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823d030972d97c92df6bc33ef78be438ad647d179137fe35f4bfb6f61d8db9ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378788f9ca239860d89fb5c3bbea1545f80a9267aa9459ec3f9da569d769ed18`  
		Last Modified: Tue, 30 Sep 2025 00:15:42 GMT  
		Size: 80.4 MB (80380388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb797e799e3bd572e943838004c1524a12dbcae17a3f5745748f6cf4c918f2cc`  
		Last Modified: Tue, 30 Sep 2025 00:15:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff005f26e2985d74a3fbf6d89f2eefd91990d5d3e5d0079f3436f7f0f5d03907`  
		Last Modified: Tue, 30 Sep 2025 00:15:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:4ea1f26847fd13abcc92c49e207e1348e5aa24daedc35ab91326e39467ecae6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20574620b612025dc02f51df435429c5bfbdad7b3f8c33785deb4cd003aa1386`

```dockerfile
```

-	Layers:
	-	`sha256:0515453d2e39868223779e91e4f179ca2d1489b84e6801d027381d9bb9d225f6`  
		Last Modified: Wed, 01 Oct 2025 12:30:32 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; 386

```console
$ docker pull varnish@sha256:c75c4ed9c763f676a84df2cab594c7feb7b572205a3220e15c0f60841b642d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114480792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377b468274da6095a7f77a47984053439376992a1405ea905800600b71dc1046`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541acb4695489a091f8e5ef52e0305e4d07442c2c732b3e283b9a52b864b69b6`  
		Last Modified: Tue, 30 Sep 2025 00:22:30 GMT  
		Size: 83.2 MB (83184211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57eb89afe2e724f226654e1c0e3f03494b2ab8b00c84bdd180501eda7f1be8`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac1c1e383ee3b87879b512392777229af0dc886705fc472d405f32456bc99b`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:dcc28285e54b4016cb30e6a2c4bcb82c727bad02e68be857268a32265839ee18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186bd63fb6a66f62f0e8d25bd70e7acbf722ceae870f9ffb7120227f11054219`

```dockerfile
```

-	Layers:
	-	`sha256:6d79edad424240488ffad7394464124b187930d9cc060ac6ddfb85373ff8160b`  
		Last Modified: Tue, 30 Sep 2025 15:21:28 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; ppc64le

```console
$ docker pull varnish@sha256:4bc9bc90b7dd65041a2467a434ea78d6fcd9714632f6410987120e6a5dac8cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111789981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2bbe954c5d32e5d2594fb251362aae7d44cc957184d96bcf8d6a32882d283`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5539ac0687305028c3b091d0bd005dd435a7120b1adeed651519755a284087`  
		Last Modified: Tue, 30 Sep 2025 09:19:11 GMT  
		Size: 78.2 MB (78189477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef2b4323b35b04baffb47f2a0dce4b48b005b82cc0de3c4a190b5ea26873a`  
		Last Modified: Tue, 30 Sep 2025 09:19:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06820665efb4162770e24bafe372923c2bb07df762507b5f2c01ea82b1be250`  
		Last Modified: Tue, 30 Sep 2025 09:19:02 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:f100f29fb73ef707a31f32fca0ef4b48feb996f678d4a06c67e1e5e2c8956c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6b9e54d90a46a1a4b11ccc7f8cb58ddedead0044d1d8cc8e0a34d33b8d622`

```dockerfile
```

-	Layers:
	-	`sha256:40cc376b259c0c4a078d0b58a028f300ca0082ed7b67382a1fafb6c01ef2ce01`  
		Last Modified: Wed, 01 Oct 2025 21:19:40 GMT  
		Size: 19.1 KB (19098 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; s390x

```console
$ docker pull varnish@sha256:657d3edd68a65c906ae591fd1a3d089da6612dd697b8898288aec8d8a6ac1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93297601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179329da1a7815cc9e37d5f66b534a417ff28e4afc4565dba050a4426b2a7c52`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89997ec12fbc73cab93ec270f9f6217ad1c36201f98c7ac10ca1d56cd48f75fa`  
		Last Modified: Tue, 30 Sep 2025 09:31:10 GMT  
		Size: 63.5 MB (63458324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08725b35f85e66d1853a06666f987c279cc65cdcf9def2dd3277ed44bfa864f3`  
		Last Modified: Tue, 30 Sep 2025 09:31:04 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9914c3e06a10fc608b5ae547675a47c6f03f8bf05b700ae6baf38bfe616c28`  
		Last Modified: Tue, 30 Sep 2025 09:31:05 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:e976e1e6a0a0584d964d85bd4d1b658e25697067e72323e5adec8ed2b2597842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e460bd852b26343edd236905e792573503082e32f52ad8e5fa971b267dd9cca0`

```dockerfile
```

-	Layers:
	-	`sha256:03e3283fe7e981c8719816b768c237efc142716e967326bad41ac96f6dc65c03`  
		Last Modified: Wed, 01 Oct 2025 00:30:19 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7-alpine`

```console
$ docker pull varnish@sha256:c11cf7d63e01386a3f02cbba27821c6270f8b692d3a0ee84806cf812b9487eec
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

### `varnish:7.7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:c9659dab18a500d9fe04fa785eefc64d24edc2e862bb59084ceee34b38dce496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80509232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2cf69fd1f3fcd8a03b3feccc63efeaeeefad5ccb90260bbe35fa15fe2de63`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482641fcef0c8088913cb713ac90451442ec8de569addab8851373246f0fe29f`  
		Last Modified: Wed, 08 Oct 2025 23:31:54 GMT  
		Size: 76.7 MB (76704725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65912544d120184afcbb1ffd23d1693126dfef25bc88d90974cbefbe1b254df4`  
		Last Modified: Wed, 08 Oct 2025 23:31:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe1e835e84c50d6f9db4c2d94590deeb81cf7ab3d855f3234bd46d9ce4c6f5`  
		Last Modified: Wed, 08 Oct 2025 23:31:40 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:c81fb0c5623e84838532ea464dee82356f2a5f34b72391aec38f6630314a095b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4101277619c6c9054473d726c7e91f76c357ea28000c56bdb380a44193d2f90c`

```dockerfile
```

-	Layers:
	-	`sha256:b39bd93d289b05c0717b67efb0653c0581280531c9664232626794a908bb05ad`  
		Last Modified: Thu, 09 Oct 2025 00:19:32 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:32895706e539e8206106474af679442182babdc28ba6e9628c11c3c4ad643ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62518955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0d48349671c7c80be42e08ecbb37dfb0935824605f204d9c8b2d933dfd2b5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96a0a13dbec284bd8cd345c59d8375d7a837d2b1fd77940ab14c123ae7bbfc9`  
		Last Modified: Wed, 08 Oct 2025 22:12:11 GMT  
		Size: 59.3 MB (59295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b2423e65b9488dad1ba24b9b874fb325d6d88ffb995ab80a23b00564a038c8`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a96bc498d9e4d162d79b72167c6dde22de2a0dd5695ded9638cafa3fb58b4b2`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:da78635d73aad180804fc8b230700f4389f337ae1245edbfab53a9e0fa9a412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ad716355c051c3737347007ed90b77d468dece570401ffd7941df02ba575c`

```dockerfile
```

-	Layers:
	-	`sha256:85e849d6e3caf0956144b3822a7b2669e0ad733c6d76c66deb932570858ec90e`  
		Last Modified: Thu, 09 Oct 2025 00:19:35 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:35e2e2be25388c5bda5c91171fd22571cfd80a62fa0a6d1033f918d5ff2cc3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77506872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce0ebfdc5663581b7f629f831661a430d6e82b4525ae7b9b87be517a942527`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6cbd79b4f613e51c0f166692056c8144bbcb4f243f84b4590619bc21a0b072`  
		Last Modified: Thu, 09 Oct 2025 02:39:52 GMT  
		Size: 73.4 MB (73366746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79326203fca5ed4aedf0d71d2ff79336ab5bb671356f694f877f1f6adaa22f14`  
		Last Modified: Wed, 08 Oct 2025 21:47:10 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecce3bc45b8924bb7789a68a8cc79abfbe8faf7f37b2ea9069d9fcb54607e0b`  
		Last Modified: Wed, 08 Oct 2025 21:47:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:97a740ba648cb7e51ecee68ae342ec2b52c9f01e060d1feafb1220f0572ca4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e524b7cb420a4730e4930229517182e0c0a815832c7ffb86a0b7b1231542c67`

```dockerfile
```

-	Layers:
	-	`sha256:4bb0166a0b7691b680dcebd874fb383803abe3fd354b3f732beaf911f8daa68e`  
		Last Modified: Thu, 09 Oct 2025 00:19:39 GMT  
		Size: 18.9 KB (18947 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b4de4c6555d41ce3142fc76516f70de1eae08d4fc1ab832130a134de00879f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82737865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27534bc22899d318c0c1a4dfc1406179ea7c3984e4ccf34390696457c8f6765f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643b7ceed7bcee1c3d59fc18d494ef6a37bd8678404893b1229c369bdc84210a`  
		Last Modified: Wed, 08 Oct 2025 21:41:42 GMT  
		Size: 79.1 MB (79116881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bae575509feeebb714ff2363fa2a8fa1f4c8cc866719191cbd213f1afc6579`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a54a65e140f7edb0a6dddbf380306157d5be82151c8301edadbdcfcd4f162d2`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:16528c0ea97f5c2ee589ce603534b6b802907590277ee04c11cc7793b594f5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2233b2b41bc17a81460516bb93fe762712d93ab9476f8f4bf82bfdb193223c6f`

```dockerfile
```

-	Layers:
	-	`sha256:9fa86eeaebb4e88469136afe59bbc44222e410bfd91aa08affc869b2e131770a`  
		Last Modified: Thu, 09 Oct 2025 00:19:42 GMT  
		Size: 18.8 KB (18827 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:bfb05dc6aa06e1dd936e7ff7c07a4e93ab7a7854e3b02b7c6d8f0fc833ed1d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76639272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da184a45ec589f94e137caa1332b801e609de03627735362300c14b9907525f4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeffbb7c94dcb75dca07f8c37dd42060aaf2af42c122e19a9c159b75ec63870`  
		Last Modified: Thu, 09 Oct 2025 03:39:11 GMT  
		Size: 72.9 MB (72904969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07abff344c3433c1799307c959211f701cdab20eb5f16683c3b8dce4d0cab7b7`  
		Last Modified: Thu, 09 Oct 2025 03:39:03 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0b47abd662b4e4cfaf443ccbf5693bac345b973f4e09d054a3d7b418bd5af`  
		Last Modified: Thu, 09 Oct 2025 03:39:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:47bee8ec48ed360f57235cd70d7ffe22d7d32acc8ba9e9a3ad9d2e1bcce645e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82584094cbda0713e76670be3615a054abb4a64d0b78dce89bc79b3acd35eb86`

```dockerfile
```

-	Layers:
	-	`sha256:2691e5e8553df139393bd8fbd4351de7f140f73f2de776fda9dc2bfea15847d1`  
		Last Modified: Thu, 09 Oct 2025 06:19:31 GMT  
		Size: 18.9 KB (18893 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ec1794f8e9d2ce3a43d4e7a40c048f202ba0b916f0e81d6ef078fe305043aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71290928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f100d551ae21d2db13ebc83234b956478ae94f03d1b82b5062535a1e8ee31d2c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0d17d7d5880eb2320ab71fd37521411789c0b0b141fd671a1cafeb64b11757`  
		Last Modified: Thu, 09 Oct 2025 03:10:10 GMT  
		Size: 67.6 MB (67639628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a597f898d06d096f4ad6afb8109ca6cc4d6a4f3f18ed479fae9d7d3c6906070`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d8ee3c9020de00cfbad575a804b20dc1eb0a46d7026d2f06a99e38909362aa`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:8a460acaba06608ea00cf72a7391f0f91f9ddcfc70163d3c521d852d609819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615cd31422df6224627eb7815825bc3df8c0a4b43c60e38246a3174fbfd9ef4c`

```dockerfile
```

-	Layers:
	-	`sha256:aa184cf214624641b9944315fba469e91f1a21cd156bc8f7176224c266a74a87`  
		Last Modified: Thu, 09 Oct 2025 03:19:30 GMT  
		Size: 18.9 KB (18853 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.3`

```console
$ docker pull varnish@sha256:9310a9cbdb61b632afb83fff44fa7c71b90f987a0587d23fc159e3b22334d577
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

### `varnish:7.7.3` - linux; amd64

```console
$ docker pull varnish@sha256:feb27787cd34f85263e0c591a947c90a01ca9082d4db5e8d56ce8fd39ececd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116344965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0192faac62b9eec84df7907e4eb139a9ea473cc3e7c57c78c15aa40651aeff5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b82bb006d56a9a208eca4bffb9e1e098368320b3fab7f67cdc2dd79dad4c86`  
		Last Modified: Tue, 30 Sep 2025 21:33:06 GMT  
		Size: 86.6 MB (86565152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7cb22c2f76de71127b4e09b5455fc95836614c6c0c5a941181219883745b5e`  
		Last Modified: Tue, 30 Sep 2025 01:05:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036dd63ac5b112d011fa5fda2c3d53d5384ef1b2e12fc332f168fa0e9b92bf9d`  
		Last Modified: Tue, 30 Sep 2025 01:05:11 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:d2c49efdb9688d0933b973d5d4f3c3121cdc3bffddbb2400a1bff80fa5744200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aeaece4ccec8dbdfa7a985432df4a634c5bab3e367c8f0b727ea27947260e6`

```dockerfile
```

-	Layers:
	-	`sha256:09149e48eec29e1632ede18e8bcc7660017d23659e476a5c05e21b76af9fa71a`  
		Last Modified: Tue, 30 Sep 2025 21:32:47 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9a0a576248e3d011b4947e5a74e61c5c7ff29f38ff030eb06baa9550348ff161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87152968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d5b118f151e98200705c07123a2452e185dc36beb379bf01a3959e6d7120a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3ef5967cc3af519476a7d1003a8c50ff757dc2ad6fc3efb554c5930835bdef`  
		Last Modified: Tue, 30 Sep 2025 01:07:11 GMT  
		Size: 60.9 MB (60938163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df71cd8f1ded8d32285abf30be2878d4c27c61bbf4dd27fddfa6756af4dfca15`  
		Last Modified: Tue, 30 Sep 2025 01:07:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf0fae6e41dd18ce4bd19f5903c4ccf7a8c60af8a43028ba0473bbed6f182a`  
		Last Modified: Tue, 30 Sep 2025 01:07:06 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:32ae2e7ec68987e97ca435fa46c0032a9b3632ac990b17dbc97c57dab02f7c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f763821ad5c8f0de3985f062c5a06915836b0d147d1cd3784c8cc1409dd3c90d`

```dockerfile
```

-	Layers:
	-	`sha256:3b3061b7c84355510b63919b85ac719ff16b89a1896f7110d335a8596e589096`  
		Last Modified: Wed, 01 Oct 2025 21:19:33 GMT  
		Size: 19.1 KB (19132 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0d7c1c994530d1ed1ca5853a890e344630822f13d8d9178cac04b849b59c52cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110523275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823d030972d97c92df6bc33ef78be438ad647d179137fe35f4bfb6f61d8db9ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378788f9ca239860d89fb5c3bbea1545f80a9267aa9459ec3f9da569d769ed18`  
		Last Modified: Tue, 30 Sep 2025 00:15:42 GMT  
		Size: 80.4 MB (80380388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb797e799e3bd572e943838004c1524a12dbcae17a3f5745748f6cf4c918f2cc`  
		Last Modified: Tue, 30 Sep 2025 00:15:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff005f26e2985d74a3fbf6d89f2eefd91990d5d3e5d0079f3436f7f0f5d03907`  
		Last Modified: Tue, 30 Sep 2025 00:15:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:4ea1f26847fd13abcc92c49e207e1348e5aa24daedc35ab91326e39467ecae6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20574620b612025dc02f51df435429c5bfbdad7b3f8c33785deb4cd003aa1386`

```dockerfile
```

-	Layers:
	-	`sha256:0515453d2e39868223779e91e4f179ca2d1489b84e6801d027381d9bb9d225f6`  
		Last Modified: Wed, 01 Oct 2025 12:30:32 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; 386

```console
$ docker pull varnish@sha256:c75c4ed9c763f676a84df2cab594c7feb7b572205a3220e15c0f60841b642d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114480792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377b468274da6095a7f77a47984053439376992a1405ea905800600b71dc1046`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541acb4695489a091f8e5ef52e0305e4d07442c2c732b3e283b9a52b864b69b6`  
		Last Modified: Tue, 30 Sep 2025 00:22:30 GMT  
		Size: 83.2 MB (83184211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57eb89afe2e724f226654e1c0e3f03494b2ab8b00c84bdd180501eda7f1be8`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac1c1e383ee3b87879b512392777229af0dc886705fc472d405f32456bc99b`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:dcc28285e54b4016cb30e6a2c4bcb82c727bad02e68be857268a32265839ee18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186bd63fb6a66f62f0e8d25bd70e7acbf722ceae870f9ffb7120227f11054219`

```dockerfile
```

-	Layers:
	-	`sha256:6d79edad424240488ffad7394464124b187930d9cc060ac6ddfb85373ff8160b`  
		Last Modified: Tue, 30 Sep 2025 15:21:28 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:4bc9bc90b7dd65041a2467a434ea78d6fcd9714632f6410987120e6a5dac8cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111789981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2bbe954c5d32e5d2594fb251362aae7d44cc957184d96bcf8d6a32882d283`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5539ac0687305028c3b091d0bd005dd435a7120b1adeed651519755a284087`  
		Last Modified: Tue, 30 Sep 2025 09:19:11 GMT  
		Size: 78.2 MB (78189477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef2b4323b35b04baffb47f2a0dce4b48b005b82cc0de3c4a190b5ea26873a`  
		Last Modified: Tue, 30 Sep 2025 09:19:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06820665efb4162770e24bafe372923c2bb07df762507b5f2c01ea82b1be250`  
		Last Modified: Tue, 30 Sep 2025 09:19:02 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:f100f29fb73ef707a31f32fca0ef4b48feb996f678d4a06c67e1e5e2c8956c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6b9e54d90a46a1a4b11ccc7f8cb58ddedead0044d1d8cc8e0a34d33b8d622`

```dockerfile
```

-	Layers:
	-	`sha256:40cc376b259c0c4a078d0b58a028f300ca0082ed7b67382a1fafb6c01ef2ce01`  
		Last Modified: Wed, 01 Oct 2025 21:19:40 GMT  
		Size: 19.1 KB (19098 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; s390x

```console
$ docker pull varnish@sha256:657d3edd68a65c906ae591fd1a3d089da6612dd697b8898288aec8d8a6ac1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93297601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179329da1a7815cc9e37d5f66b534a417ff28e4afc4565dba050a4426b2a7c52`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89997ec12fbc73cab93ec270f9f6217ad1c36201f98c7ac10ca1d56cd48f75fa`  
		Last Modified: Tue, 30 Sep 2025 09:31:10 GMT  
		Size: 63.5 MB (63458324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08725b35f85e66d1853a06666f987c279cc65cdcf9def2dd3277ed44bfa864f3`  
		Last Modified: Tue, 30 Sep 2025 09:31:04 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9914c3e06a10fc608b5ae547675a47c6f03f8bf05b700ae6baf38bfe616c28`  
		Last Modified: Tue, 30 Sep 2025 09:31:05 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:e976e1e6a0a0584d964d85bd4d1b658e25697067e72323e5adec8ed2b2597842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e460bd852b26343edd236905e792573503082e32f52ad8e5fa971b267dd9cca0`

```dockerfile
```

-	Layers:
	-	`sha256:03e3283fe7e981c8719816b768c237efc142716e967326bad41ac96f6dc65c03`  
		Last Modified: Wed, 01 Oct 2025 00:30:19 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.3-alpine`

```console
$ docker pull varnish@sha256:c11cf7d63e01386a3f02cbba27821c6270f8b692d3a0ee84806cf812b9487eec
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

### `varnish:7.7.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:c9659dab18a500d9fe04fa785eefc64d24edc2e862bb59084ceee34b38dce496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80509232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2cf69fd1f3fcd8a03b3feccc63efeaeeefad5ccb90260bbe35fa15fe2de63`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482641fcef0c8088913cb713ac90451442ec8de569addab8851373246f0fe29f`  
		Last Modified: Wed, 08 Oct 2025 23:31:54 GMT  
		Size: 76.7 MB (76704725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65912544d120184afcbb1ffd23d1693126dfef25bc88d90974cbefbe1b254df4`  
		Last Modified: Wed, 08 Oct 2025 23:31:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe1e835e84c50d6f9db4c2d94590deeb81cf7ab3d855f3234bd46d9ce4c6f5`  
		Last Modified: Wed, 08 Oct 2025 23:31:40 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:c81fb0c5623e84838532ea464dee82356f2a5f34b72391aec38f6630314a095b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4101277619c6c9054473d726c7e91f76c357ea28000c56bdb380a44193d2f90c`

```dockerfile
```

-	Layers:
	-	`sha256:b39bd93d289b05c0717b67efb0653c0581280531c9664232626794a908bb05ad`  
		Last Modified: Thu, 09 Oct 2025 00:19:32 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:32895706e539e8206106474af679442182babdc28ba6e9628c11c3c4ad643ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62518955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0d48349671c7c80be42e08ecbb37dfb0935824605f204d9c8b2d933dfd2b5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96a0a13dbec284bd8cd345c59d8375d7a837d2b1fd77940ab14c123ae7bbfc9`  
		Last Modified: Wed, 08 Oct 2025 22:12:11 GMT  
		Size: 59.3 MB (59295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b2423e65b9488dad1ba24b9b874fb325d6d88ffb995ab80a23b00564a038c8`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a96bc498d9e4d162d79b72167c6dde22de2a0dd5695ded9638cafa3fb58b4b2`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:da78635d73aad180804fc8b230700f4389f337ae1245edbfab53a9e0fa9a412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ad716355c051c3737347007ed90b77d468dece570401ffd7941df02ba575c`

```dockerfile
```

-	Layers:
	-	`sha256:85e849d6e3caf0956144b3822a7b2669e0ad733c6d76c66deb932570858ec90e`  
		Last Modified: Thu, 09 Oct 2025 00:19:35 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:35e2e2be25388c5bda5c91171fd22571cfd80a62fa0a6d1033f918d5ff2cc3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77506872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce0ebfdc5663581b7f629f831661a430d6e82b4525ae7b9b87be517a942527`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6cbd79b4f613e51c0f166692056c8144bbcb4f243f84b4590619bc21a0b072`  
		Last Modified: Thu, 09 Oct 2025 02:39:52 GMT  
		Size: 73.4 MB (73366746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79326203fca5ed4aedf0d71d2ff79336ab5bb671356f694f877f1f6adaa22f14`  
		Last Modified: Wed, 08 Oct 2025 21:47:10 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecce3bc45b8924bb7789a68a8cc79abfbe8faf7f37b2ea9069d9fcb54607e0b`  
		Last Modified: Wed, 08 Oct 2025 21:47:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:97a740ba648cb7e51ecee68ae342ec2b52c9f01e060d1feafb1220f0572ca4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e524b7cb420a4730e4930229517182e0c0a815832c7ffb86a0b7b1231542c67`

```dockerfile
```

-	Layers:
	-	`sha256:4bb0166a0b7691b680dcebd874fb383803abe3fd354b3f732beaf911f8daa68e`  
		Last Modified: Thu, 09 Oct 2025 00:19:39 GMT  
		Size: 18.9 KB (18947 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b4de4c6555d41ce3142fc76516f70de1eae08d4fc1ab832130a134de00879f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82737865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27534bc22899d318c0c1a4dfc1406179ea7c3984e4ccf34390696457c8f6765f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643b7ceed7bcee1c3d59fc18d494ef6a37bd8678404893b1229c369bdc84210a`  
		Last Modified: Wed, 08 Oct 2025 21:41:42 GMT  
		Size: 79.1 MB (79116881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bae575509feeebb714ff2363fa2a8fa1f4c8cc866719191cbd213f1afc6579`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a54a65e140f7edb0a6dddbf380306157d5be82151c8301edadbdcfcd4f162d2`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:16528c0ea97f5c2ee589ce603534b6b802907590277ee04c11cc7793b594f5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2233b2b41bc17a81460516bb93fe762712d93ab9476f8f4bf82bfdb193223c6f`

```dockerfile
```

-	Layers:
	-	`sha256:9fa86eeaebb4e88469136afe59bbc44222e410bfd91aa08affc869b2e131770a`  
		Last Modified: Thu, 09 Oct 2025 00:19:42 GMT  
		Size: 18.8 KB (18827 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:bfb05dc6aa06e1dd936e7ff7c07a4e93ab7a7854e3b02b7c6d8f0fc833ed1d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76639272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da184a45ec589f94e137caa1332b801e609de03627735362300c14b9907525f4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeffbb7c94dcb75dca07f8c37dd42060aaf2af42c122e19a9c159b75ec63870`  
		Last Modified: Thu, 09 Oct 2025 03:39:11 GMT  
		Size: 72.9 MB (72904969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07abff344c3433c1799307c959211f701cdab20eb5f16683c3b8dce4d0cab7b7`  
		Last Modified: Thu, 09 Oct 2025 03:39:03 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0b47abd662b4e4cfaf443ccbf5693bac345b973f4e09d054a3d7b418bd5af`  
		Last Modified: Thu, 09 Oct 2025 03:39:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:47bee8ec48ed360f57235cd70d7ffe22d7d32acc8ba9e9a3ad9d2e1bcce645e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82584094cbda0713e76670be3615a054abb4a64d0b78dce89bc79b3acd35eb86`

```dockerfile
```

-	Layers:
	-	`sha256:2691e5e8553df139393bd8fbd4351de7f140f73f2de776fda9dc2bfea15847d1`  
		Last Modified: Thu, 09 Oct 2025 06:19:31 GMT  
		Size: 18.9 KB (18893 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ec1794f8e9d2ce3a43d4e7a40c048f202ba0b916f0e81d6ef078fe305043aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71290928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f100d551ae21d2db13ebc83234b956478ae94f03d1b82b5062535a1e8ee31d2c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0d17d7d5880eb2320ab71fd37521411789c0b0b141fd671a1cafeb64b11757`  
		Last Modified: Thu, 09 Oct 2025 03:10:10 GMT  
		Size: 67.6 MB (67639628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a597f898d06d096f4ad6afb8109ca6cc4d6a4f3f18ed479fae9d7d3c6906070`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d8ee3c9020de00cfbad575a804b20dc1eb0a46d7026d2f06a99e38909362aa`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:8a460acaba06608ea00cf72a7391f0f91f9ddcfc70163d3c521d852d609819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615cd31422df6224627eb7815825bc3df8c0a4b43c60e38246a3174fbfd9ef4c`

```dockerfile
```

-	Layers:
	-	`sha256:aa184cf214624641b9944315fba469e91f1a21cd156bc8f7176224c266a74a87`  
		Last Modified: Thu, 09 Oct 2025 03:19:30 GMT  
		Size: 18.9 KB (18853 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:6ae8d462e3e2915e3be0c156b8864f842fb9bc8cf5f35b891c4bd1315979b33f
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

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:c97e31abb26c2a4bc80a60d0ca080f1e3a18e31ace60dbbaf4037ba29f9f3d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116466266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004bda53957dbb10230c7308b9596abf362bd6a0699bffa29463a7799274c2da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe861ac020fae87c9b3ce06a9bb9d050070b059d6c2a12c4ab7c81af27f4b2`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 86.7 MB (86686458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a2eafd8f6a49966509e8c6c54adeada7389ecb2bf14d232209ec99d6b78d7`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095bb281dc5a0973162db00f0de12ba6ac3f347e5c674d0a31052e2959ff96bf`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:3968cd90f6dd9784b74ecd501fe63144337ecb3e3abdee2961ac95dc51fbf32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82998fc1361929d6bd83b06965600e1bbdb0ff26200bdbab4a7850b941cca`

```dockerfile
```

-	Layers:
	-	`sha256:5ee38ca58b7551f252813868294b3e7bcf0cfa381fbe5256c7db0837747640f1`  
		Last Modified: Tue, 30 Sep 2025 21:32:26 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c02038c5c962e46372c533d346254ca69a84c5e120da6a2fa5e8237f0aada3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87285907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68bac847b83dd500b14b6ba1be50843667c2205abc51096b39ba8cac7b336e6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e3ca0a47d505f944b52e38a1f01835240092643e2e23c574fbe357b4571f9`  
		Last Modified: Wed, 01 Oct 2025 21:20:23 GMT  
		Size: 61.1 MB (61071100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753350ea5a9b9b29e0efbc34b8965e5e629452cc884f7a7c62994779c3dc9912`  
		Last Modified: Tue, 30 Sep 2025 01:14:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e794bb60e2416f58cdff4f685e48c8d78936d12687e23453cdf28616b9bee752`  
		Last Modified: Tue, 30 Sep 2025 01:14:06 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:8a23ef099d594ffe99a8c69f79dc29b627d3cf20f4efdb13ec9f3fbfaf85c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd0a643a2045cdab182ed9d568543f4b5a84c8ba3f9b26146cf25c109e9c46`

```dockerfile
```

-	Layers:
	-	`sha256:99081134ed748cbccefa2e85a9027e77fb0c830aac5bc880dcf3c083912b9712`  
		Last Modified: Wed, 01 Oct 2025 21:19:45 GMT  
		Size: 19.7 KB (19682 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f4563fdf791d840eeeb1d9e1b67ff1d4d7c39b306a9eb5f06f2db226487a6e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110654081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e18f227550da1dc8768ec1061690dba89ad2c5768ec1a7efa589ffe56ad86b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aef1242cf499e781216fcddef2b78081f3d1f7aa47f426845f1b847e70af0d`  
		Last Modified: Tue, 30 Sep 2025 00:16:15 GMT  
		Size: 80.5 MB (80511196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a90e6bfca1f466cd1cec43cc7918d767a06fe1a7d24faccb8e72f9d79918e1`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461be9984bef381c386ea94b6c79cb5d58e5bf043817110d4b8eec93609e7d5a`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:520c90561c90f64742da03b7e160172dc28fb70ec6a7f98901a3962f20625da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969160c2a8d28f1dd9028122950ab56d4defcd60ab02ee350cfdd4613e4c6def`

```dockerfile
```

-	Layers:
	-	`sha256:2ee77033648443ffdc6b128b310bf3599308b30966bea13d646b34e0ff109b88`  
		Last Modified: Tue, 30 Sep 2025 12:19:35 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; 386

```console
$ docker pull varnish@sha256:2e6f1b4e8275dfb5ae193d6ebf7006be19dbd90418f6b286dfa9fcaba124cfef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114623546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba378edc8b41e0ac78fb7d7160b94056584bc998278840064b20e6e3c552aaf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629ed7a24ff9c6fc99e21417dd14d80467889003580e3ff53a891dceef00a6b`  
		Last Modified: Tue, 30 Sep 2025 00:22:36 GMT  
		Size: 83.3 MB (83326965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57eb89afe2e724f226654e1c0e3f03494b2ab8b00c84bdd180501eda7f1be8`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8a07125c1ba76ef4a10c9f4f8c272959405da5d4074be84ef010e7e3daeb84`  
		Last Modified: Tue, 30 Sep 2025 00:22:30 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:f3b9af8c499722fb4b46b87fbc09783c94e48eb053c146127a7b6469eef48d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda44628af7e53672609a7747b9c2020b0e1891ce6b74b263fce3cf1b2510f1b`

```dockerfile
```

-	Layers:
	-	`sha256:2fab048c8c298c095cf5d957c545a0de2380783658ec62c83df4739a442db74a`  
		Last Modified: Tue, 30 Sep 2025 15:21:37 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; ppc64le

```console
$ docker pull varnish@sha256:698d9a167d7e39ef3d3a792b576e4ee35d9164c84229d0840b37aab3cf4bf9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111923681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf9f5f25dff8d15e6313cdadb31322976baf5d6fe1878df3fddedcf18b77ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888630ee3abf7ef0fe160c12c4dbc18f474c8875783ba40ff2dc298a71d1202f`  
		Last Modified: Tue, 30 Sep 2025 09:13:27 GMT  
		Size: 78.3 MB (78323180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c567d85e9f86b9e73e829c44c48c342d314211629e64015d048c9b11733e1e`  
		Last Modified: Tue, 30 Sep 2025 09:13:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392a07010bd9e6c85df4adf663f60a94bcbb243646c196f96d87f80982a9f8cf`  
		Last Modified: Tue, 30 Sep 2025 09:13:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:f28c3843800558653416a7186290b7c2333a587f98755d6fea3e339e30596d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0fc75c4ecb3c83e38b6f81c41766439fe29be027e152b88bb04e2cb6da56620`

```dockerfile
```

-	Layers:
	-	`sha256:f93bd5db122e41ce05d3286fc0377077dcb324eaf9b57cb8b0b1a7fcfb0f7480`  
		Last Modified: Wed, 01 Oct 2025 21:19:52 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; s390x

```console
$ docker pull varnish@sha256:3bf251b37cff6a447015e1d1b090a4b24097017afcacfb2ae012d2b8a7e04427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93425005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a0a3a8b7e7e3df39e4df4a424bbf6eb691292f2b50fd21c2619c6d689cac6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b638f836f809ae3e31620a66cae836c3c3b68b284ba451e9ee536e40eaa651`  
		Last Modified: Tue, 30 Sep 2025 09:27:43 GMT  
		Size: 63.6 MB (63585726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded88d027593837b0ba58bba11d70df695a2c82a4366804ca9e520040399a17`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b78ba670c2a2180caea9453f4ea4ce1ad713d15cd2c4fad462bba0ca8545b4`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:ad60e6c63b8b23d8246f671b010fdc5a7d07b26c0da71f43981280b1f12a7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2260eaed8f6fffb7e3b42628ecd6ebc9fa6b54be77f7afa2a4560a66f2c56`

```dockerfile
```

-	Layers:
	-	`sha256:74f98e3dae4b83f9101c4cad341b804127057bde8bbd27281be38b73ec5e2138`  
		Last Modified: Wed, 01 Oct 2025 00:30:10 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8-alpine`

```console
$ docker pull varnish@sha256:a2e68e6187c4bf3bfdf6d7d9f4dd6716cd41efaf62cb61d5f019ec150fe0ab2b
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

### `varnish:8-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ba8eb77be0459bf456469de17bfcda246c1170cea2949f6e36268a4fc2572c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80649740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5767790423f2deee85c93bba37a0c085dfdf901ba2625c8de97e7d01f40397`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d19719f963d4a327551f30c9936cd5e5d60c25e910f7f5a9ec84a9c2d682e6`  
		Last Modified: Thu, 09 Oct 2025 00:20:16 GMT  
		Size: 76.8 MB (76845235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083cb84d1525d5b94d9cfb9600551c78ae232af47f4bbafe99a11aba44b58ba`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f40f6190ff3cdb1a4890ffc069683aac52131b3a870ac3d2af0c2e3e7a9ffa`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6ac6f629cadc67b582643f7c4905078c6912d36aa7571441d5de8644c0c2767c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102d50b64eac75ab5f17fa71d569a08a4f62f2bb0f1c0c6365cfe1ac48e2122`

```dockerfile
```

-	Layers:
	-	`sha256:beabe22d3dfff560717c37f0887b9b883923342c0d22d5ec68cf9652a1209463`  
		Last Modified: Thu, 09 Oct 2025 00:19:52 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e624ea76108774c09f9e48032091401821dfdb94cf59624daf83ffc8490a0b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62654398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae51093fc76d05ea36eaf5469c85d6275a6a811822a0773eb25293512bcac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336ba603488fddde3a5260a9fddc822e750dfbfc59da41b6536b9a99cd34515`  
		Last Modified: Wed, 08 Oct 2025 22:12:09 GMT  
		Size: 59.4 MB (59430786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3d374d0d4a1a8ff7a1c6fcb91410aeafcf2f8880ca05eebe06bf7604a01111`  
		Last Modified: Wed, 08 Oct 2025 22:12:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99e557263f6da4d98b610f5d3d45b0c8e156c6b96bc49f3c1f314ae656a2a4c`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9078640134ba8b45cdb3b09c56f97c02c4d54bcc6c26ffc1aac9d4e19bc08baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc606692f8108ef5d823be4b268b7fbb6f77777b044ef151882fa21e492c9a1`

```dockerfile
```

-	Layers:
	-	`sha256:085e876cc8d3d19c17b2f7986a3e6f2bbf0bb1337153e3d459ea5eb2bdf943f9`  
		Last Modified: Thu, 09 Oct 2025 00:19:55 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2d60c0f5043faf5c659a586a9aeb8e3f2f6b77b1de74457ba2302154906e3b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77646588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d859ae3182d210801ea3d56332c129a0fdd14660537ee96e871dd650be10009`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89df23746d0dc373775c6c3909ef191fc5b685a8414cdcac2b1104e4354d8213`  
		Last Modified: Wed, 08 Oct 2025 21:47:22 GMT  
		Size: 73.5 MB (73506464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a4838380d12fe8a616bb2554ca0fad2162efeeb8f3cd2c80662d848c36bab1`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa02b94be62585c016a55f8ba157f043c2fd3ceb77edd0bb0f29d2c7988860`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:56acacec5d07daf794ba7631eef4916b5e2818995d2f4b688aefae71b2f63066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f568cf93c272ad9235cbea7d929f9a6185ea1414d13f6f33eda459c3b3d34b0`

```dockerfile
```

-	Layers:
	-	`sha256:509cafe80bab2cdc5955af89fe1b042ac21e60d489bd03d33624efe954b91379`  
		Last Modified: Thu, 09 Oct 2025 00:19:58 GMT  
		Size: 19.4 KB (19438 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; 386

```console
$ docker pull varnish@sha256:65206c02858aecf59c8ec6bfaaafa059f4e4901bd876a9dec0c215d51e1f2a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82874569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3164ef01d5ae90f502da0b6f9da074b36fa56ff2b0d6ff297f9359e3d74e0a8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cb961e3fec70bb2f3b518c46ada6f4ca49360acd574cf45ec32b32eaafb01b`  
		Last Modified: Wed, 08 Oct 2025 21:41:33 GMT  
		Size: 79.3 MB (79253583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78236060e4a99dac0a6931eb84850f7caab72617e2c0bc7a4c41a1e58c9047c`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a08316b257931ed28a9aa1962f4220f5f2c0ef72b1b9bd744ba704082491e`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0408eb02adca0c5fd76a410aedf2c9d409145229ae11ef5f93a2e31b0b8645af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739495427886fd79e3484e3bd305e575b5da6e9c8dd9b728e7d09c34b5d657da`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c9a00e2d724a783a713638779b64c37b740ccd716e28e35c5ba70f5b0015`  
		Last Modified: Thu, 09 Oct 2025 00:20:02 GMT  
		Size: 19.3 KB (19285 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:677cc3ec09c593cfdf723379d9120bd1b9b407eeb508b4ad2bcaba9346b28aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e035d28b41a18d5fefb7a12f9e2523688e7cbb4973c6f58d4189c2a396395d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08db313ba0b74ae969f29bc00b7803b78db0de38106aab9fa13e6fc4c20ff06`  
		Last Modified: Thu, 09 Oct 2025 03:37:12 GMT  
		Size: 73.0 MB (73040138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a125238abb15614acca8c40fbbdf92434d2d8f057fae857298235de015531b2`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4376b12c3b402608cb7391bb3c6042ccd7e850142306e2a0b8ba13507296e4d1`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a1fdea113bc5acf33aa0908c87ad481e8fb471c0c16043320014b0d30d1a8d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3520cddf7d20e95153c75f682aaa3b623d23c9116963cf67c3f5303339bdefd`

```dockerfile
```

-	Layers:
	-	`sha256:f2ce0afefc61f5a41d9a3426b61425c87e3bee67d737063113e3bd24821f54e3`  
		Last Modified: Thu, 09 Oct 2025 06:19:43 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:e040b0db456d799b0ff9dcea9b17bda702c27d05cadbd345d5add1e9f8f7a55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71428457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60881cbce6790d05e3be256b05124ed36d4f58d94bceb295841ea392f7ebab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2bd97591c904b46405111198f80adcb211a3d82071b457cd6ead8e0d6b631c`  
		Last Modified: Thu, 09 Oct 2025 02:30:48 GMT  
		Size: 67.8 MB (67777154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211e62f62da811326f4c91458d5841b9582b8d0470bc1998e17467eff9c03ad3`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d475471c3c97d3a9c9ea4a34f85ba393635831e8a0afec1466cd431135ac8c57`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1c14e3e6e67b7aa214245bb2b5d4da8a77fd5d6d3e4e06172a74921f6b806164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9629cc539632351d549586b170aa75b664d5d7658312a091153217619f6184a4`

```dockerfile
```

-	Layers:
	-	`sha256:02e61c597cad44d949cacce426a408a5ed4f30945003406052031e88e5a71423`  
		Last Modified: Thu, 09 Oct 2025 03:19:40 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0`

```console
$ docker pull varnish@sha256:6ae8d462e3e2915e3be0c156b8864f842fb9bc8cf5f35b891c4bd1315979b33f
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

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:c97e31abb26c2a4bc80a60d0ca080f1e3a18e31ace60dbbaf4037ba29f9f3d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116466266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004bda53957dbb10230c7308b9596abf362bd6a0699bffa29463a7799274c2da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe861ac020fae87c9b3ce06a9bb9d050070b059d6c2a12c4ab7c81af27f4b2`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 86.7 MB (86686458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a2eafd8f6a49966509e8c6c54adeada7389ecb2bf14d232209ec99d6b78d7`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095bb281dc5a0973162db00f0de12ba6ac3f347e5c674d0a31052e2959ff96bf`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:3968cd90f6dd9784b74ecd501fe63144337ecb3e3abdee2961ac95dc51fbf32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82998fc1361929d6bd83b06965600e1bbdb0ff26200bdbab4a7850b941cca`

```dockerfile
```

-	Layers:
	-	`sha256:5ee38ca58b7551f252813868294b3e7bcf0cfa381fbe5256c7db0837747640f1`  
		Last Modified: Tue, 30 Sep 2025 21:32:26 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c02038c5c962e46372c533d346254ca69a84c5e120da6a2fa5e8237f0aada3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87285907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68bac847b83dd500b14b6ba1be50843667c2205abc51096b39ba8cac7b336e6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e3ca0a47d505f944b52e38a1f01835240092643e2e23c574fbe357b4571f9`  
		Last Modified: Wed, 01 Oct 2025 21:20:23 GMT  
		Size: 61.1 MB (61071100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753350ea5a9b9b29e0efbc34b8965e5e629452cc884f7a7c62994779c3dc9912`  
		Last Modified: Tue, 30 Sep 2025 01:14:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e794bb60e2416f58cdff4f685e48c8d78936d12687e23453cdf28616b9bee752`  
		Last Modified: Tue, 30 Sep 2025 01:14:06 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:8a23ef099d594ffe99a8c69f79dc29b627d3cf20f4efdb13ec9f3fbfaf85c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd0a643a2045cdab182ed9d568543f4b5a84c8ba3f9b26146cf25c109e9c46`

```dockerfile
```

-	Layers:
	-	`sha256:99081134ed748cbccefa2e85a9027e77fb0c830aac5bc880dcf3c083912b9712`  
		Last Modified: Wed, 01 Oct 2025 21:19:45 GMT  
		Size: 19.7 KB (19682 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f4563fdf791d840eeeb1d9e1b67ff1d4d7c39b306a9eb5f06f2db226487a6e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110654081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e18f227550da1dc8768ec1061690dba89ad2c5768ec1a7efa589ffe56ad86b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aef1242cf499e781216fcddef2b78081f3d1f7aa47f426845f1b847e70af0d`  
		Last Modified: Tue, 30 Sep 2025 00:16:15 GMT  
		Size: 80.5 MB (80511196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a90e6bfca1f466cd1cec43cc7918d767a06fe1a7d24faccb8e72f9d79918e1`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461be9984bef381c386ea94b6c79cb5d58e5bf043817110d4b8eec93609e7d5a`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:520c90561c90f64742da03b7e160172dc28fb70ec6a7f98901a3962f20625da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969160c2a8d28f1dd9028122950ab56d4defcd60ab02ee350cfdd4613e4c6def`

```dockerfile
```

-	Layers:
	-	`sha256:2ee77033648443ffdc6b128b310bf3599308b30966bea13d646b34e0ff109b88`  
		Last Modified: Tue, 30 Sep 2025 12:19:35 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; 386

```console
$ docker pull varnish@sha256:2e6f1b4e8275dfb5ae193d6ebf7006be19dbd90418f6b286dfa9fcaba124cfef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114623546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba378edc8b41e0ac78fb7d7160b94056584bc998278840064b20e6e3c552aaf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629ed7a24ff9c6fc99e21417dd14d80467889003580e3ff53a891dceef00a6b`  
		Last Modified: Tue, 30 Sep 2025 00:22:36 GMT  
		Size: 83.3 MB (83326965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57eb89afe2e724f226654e1c0e3f03494b2ab8b00c84bdd180501eda7f1be8`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8a07125c1ba76ef4a10c9f4f8c272959405da5d4074be84ef010e7e3daeb84`  
		Last Modified: Tue, 30 Sep 2025 00:22:30 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:f3b9af8c499722fb4b46b87fbc09783c94e48eb053c146127a7b6469eef48d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda44628af7e53672609a7747b9c2020b0e1891ce6b74b263fce3cf1b2510f1b`

```dockerfile
```

-	Layers:
	-	`sha256:2fab048c8c298c095cf5d957c545a0de2380783658ec62c83df4739a442db74a`  
		Last Modified: Tue, 30 Sep 2025 15:21:37 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:698d9a167d7e39ef3d3a792b576e4ee35d9164c84229d0840b37aab3cf4bf9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111923681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf9f5f25dff8d15e6313cdadb31322976baf5d6fe1878df3fddedcf18b77ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888630ee3abf7ef0fe160c12c4dbc18f474c8875783ba40ff2dc298a71d1202f`  
		Last Modified: Tue, 30 Sep 2025 09:13:27 GMT  
		Size: 78.3 MB (78323180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c567d85e9f86b9e73e829c44c48c342d314211629e64015d048c9b11733e1e`  
		Last Modified: Tue, 30 Sep 2025 09:13:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392a07010bd9e6c85df4adf663f60a94bcbb243646c196f96d87f80982a9f8cf`  
		Last Modified: Tue, 30 Sep 2025 09:13:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:f28c3843800558653416a7186290b7c2333a587f98755d6fea3e339e30596d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0fc75c4ecb3c83e38b6f81c41766439fe29be027e152b88bb04e2cb6da56620`

```dockerfile
```

-	Layers:
	-	`sha256:f93bd5db122e41ce05d3286fc0377077dcb324eaf9b57cb8b0b1a7fcfb0f7480`  
		Last Modified: Wed, 01 Oct 2025 21:19:52 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; s390x

```console
$ docker pull varnish@sha256:3bf251b37cff6a447015e1d1b090a4b24097017afcacfb2ae012d2b8a7e04427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93425005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a0a3a8b7e7e3df39e4df4a424bbf6eb691292f2b50fd21c2619c6d689cac6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b638f836f809ae3e31620a66cae836c3c3b68b284ba451e9ee536e40eaa651`  
		Last Modified: Tue, 30 Sep 2025 09:27:43 GMT  
		Size: 63.6 MB (63585726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded88d027593837b0ba58bba11d70df695a2c82a4366804ca9e520040399a17`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b78ba670c2a2180caea9453f4ea4ce1ad713d15cd2c4fad462bba0ca8545b4`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:ad60e6c63b8b23d8246f671b010fdc5a7d07b26c0da71f43981280b1f12a7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2260eaed8f6fffb7e3b42628ecd6ebc9fa6b54be77f7afa2a4560a66f2c56`

```dockerfile
```

-	Layers:
	-	`sha256:74f98e3dae4b83f9101c4cad341b804127057bde8bbd27281be38b73ec5e2138`  
		Last Modified: Wed, 01 Oct 2025 00:30:10 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0-alpine`

```console
$ docker pull varnish@sha256:a2e68e6187c4bf3bfdf6d7d9f4dd6716cd41efaf62cb61d5f019ec150fe0ab2b
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

### `varnish:8.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ba8eb77be0459bf456469de17bfcda246c1170cea2949f6e36268a4fc2572c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80649740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5767790423f2deee85c93bba37a0c085dfdf901ba2625c8de97e7d01f40397`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d19719f963d4a327551f30c9936cd5e5d60c25e910f7f5a9ec84a9c2d682e6`  
		Last Modified: Thu, 09 Oct 2025 00:20:16 GMT  
		Size: 76.8 MB (76845235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083cb84d1525d5b94d9cfb9600551c78ae232af47f4bbafe99a11aba44b58ba`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f40f6190ff3cdb1a4890ffc069683aac52131b3a870ac3d2af0c2e3e7a9ffa`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6ac6f629cadc67b582643f7c4905078c6912d36aa7571441d5de8644c0c2767c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102d50b64eac75ab5f17fa71d569a08a4f62f2bb0f1c0c6365cfe1ac48e2122`

```dockerfile
```

-	Layers:
	-	`sha256:beabe22d3dfff560717c37f0887b9b883923342c0d22d5ec68cf9652a1209463`  
		Last Modified: Thu, 09 Oct 2025 00:19:52 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e624ea76108774c09f9e48032091401821dfdb94cf59624daf83ffc8490a0b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62654398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae51093fc76d05ea36eaf5469c85d6275a6a811822a0773eb25293512bcac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336ba603488fddde3a5260a9fddc822e750dfbfc59da41b6536b9a99cd34515`  
		Last Modified: Wed, 08 Oct 2025 22:12:09 GMT  
		Size: 59.4 MB (59430786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3d374d0d4a1a8ff7a1c6fcb91410aeafcf2f8880ca05eebe06bf7604a01111`  
		Last Modified: Wed, 08 Oct 2025 22:12:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99e557263f6da4d98b610f5d3d45b0c8e156c6b96bc49f3c1f314ae656a2a4c`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9078640134ba8b45cdb3b09c56f97c02c4d54bcc6c26ffc1aac9d4e19bc08baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc606692f8108ef5d823be4b268b7fbb6f77777b044ef151882fa21e492c9a1`

```dockerfile
```

-	Layers:
	-	`sha256:085e876cc8d3d19c17b2f7986a3e6f2bbf0bb1337153e3d459ea5eb2bdf943f9`  
		Last Modified: Thu, 09 Oct 2025 00:19:55 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2d60c0f5043faf5c659a586a9aeb8e3f2f6b77b1de74457ba2302154906e3b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77646588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d859ae3182d210801ea3d56332c129a0fdd14660537ee96e871dd650be10009`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89df23746d0dc373775c6c3909ef191fc5b685a8414cdcac2b1104e4354d8213`  
		Last Modified: Wed, 08 Oct 2025 21:47:22 GMT  
		Size: 73.5 MB (73506464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a4838380d12fe8a616bb2554ca0fad2162efeeb8f3cd2c80662d848c36bab1`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa02b94be62585c016a55f8ba157f043c2fd3ceb77edd0bb0f29d2c7988860`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:56acacec5d07daf794ba7631eef4916b5e2818995d2f4b688aefae71b2f63066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f568cf93c272ad9235cbea7d929f9a6185ea1414d13f6f33eda459c3b3d34b0`

```dockerfile
```

-	Layers:
	-	`sha256:509cafe80bab2cdc5955af89fe1b042ac21e60d489bd03d33624efe954b91379`  
		Last Modified: Thu, 09 Oct 2025 00:19:58 GMT  
		Size: 19.4 KB (19438 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:65206c02858aecf59c8ec6bfaaafa059f4e4901bd876a9dec0c215d51e1f2a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82874569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3164ef01d5ae90f502da0b6f9da074b36fa56ff2b0d6ff297f9359e3d74e0a8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cb961e3fec70bb2f3b518c46ada6f4ca49360acd574cf45ec32b32eaafb01b`  
		Last Modified: Wed, 08 Oct 2025 21:41:33 GMT  
		Size: 79.3 MB (79253583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78236060e4a99dac0a6931eb84850f7caab72617e2c0bc7a4c41a1e58c9047c`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a08316b257931ed28a9aa1962f4220f5f2c0ef72b1b9bd744ba704082491e`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0408eb02adca0c5fd76a410aedf2c9d409145229ae11ef5f93a2e31b0b8645af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739495427886fd79e3484e3bd305e575b5da6e9c8dd9b728e7d09c34b5d657da`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c9a00e2d724a783a713638779b64c37b740ccd716e28e35c5ba70f5b0015`  
		Last Modified: Thu, 09 Oct 2025 00:20:02 GMT  
		Size: 19.3 KB (19285 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:677cc3ec09c593cfdf723379d9120bd1b9b407eeb508b4ad2bcaba9346b28aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e035d28b41a18d5fefb7a12f9e2523688e7cbb4973c6f58d4189c2a396395d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08db313ba0b74ae969f29bc00b7803b78db0de38106aab9fa13e6fc4c20ff06`  
		Last Modified: Thu, 09 Oct 2025 03:37:12 GMT  
		Size: 73.0 MB (73040138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a125238abb15614acca8c40fbbdf92434d2d8f057fae857298235de015531b2`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4376b12c3b402608cb7391bb3c6042ccd7e850142306e2a0b8ba13507296e4d1`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a1fdea113bc5acf33aa0908c87ad481e8fb471c0c16043320014b0d30d1a8d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3520cddf7d20e95153c75f682aaa3b623d23c9116963cf67c3f5303339bdefd`

```dockerfile
```

-	Layers:
	-	`sha256:f2ce0afefc61f5a41d9a3426b61425c87e3bee67d737063113e3bd24821f54e3`  
		Last Modified: Thu, 09 Oct 2025 06:19:43 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:e040b0db456d799b0ff9dcea9b17bda702c27d05cadbd345d5add1e9f8f7a55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71428457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60881cbce6790d05e3be256b05124ed36d4f58d94bceb295841ea392f7ebab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2bd97591c904b46405111198f80adcb211a3d82071b457cd6ead8e0d6b631c`  
		Last Modified: Thu, 09 Oct 2025 02:30:48 GMT  
		Size: 67.8 MB (67777154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211e62f62da811326f4c91458d5841b9582b8d0470bc1998e17467eff9c03ad3`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d475471c3c97d3a9c9ea4a34f85ba393635831e8a0afec1466cd431135ac8c57`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1c14e3e6e67b7aa214245bb2b5d4da8a77fd5d6d3e4e06172a74921f6b806164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9629cc539632351d549586b170aa75b664d5d7658312a091153217619f6184a4`

```dockerfile
```

-	Layers:
	-	`sha256:02e61c597cad44d949cacce426a408a5ed4f30945003406052031e88e5a71423`  
		Last Modified: Thu, 09 Oct 2025 03:19:40 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.0`

```console
$ docker pull varnish@sha256:6ae8d462e3e2915e3be0c156b8864f842fb9bc8cf5f35b891c4bd1315979b33f
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

### `varnish:8.0.0` - linux; amd64

```console
$ docker pull varnish@sha256:c97e31abb26c2a4bc80a60d0ca080f1e3a18e31ace60dbbaf4037ba29f9f3d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116466266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004bda53957dbb10230c7308b9596abf362bd6a0699bffa29463a7799274c2da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe861ac020fae87c9b3ce06a9bb9d050070b059d6c2a12c4ab7c81af27f4b2`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 86.7 MB (86686458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a2eafd8f6a49966509e8c6c54adeada7389ecb2bf14d232209ec99d6b78d7`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095bb281dc5a0973162db00f0de12ba6ac3f347e5c674d0a31052e2959ff96bf`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:3968cd90f6dd9784b74ecd501fe63144337ecb3e3abdee2961ac95dc51fbf32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82998fc1361929d6bd83b06965600e1bbdb0ff26200bdbab4a7850b941cca`

```dockerfile
```

-	Layers:
	-	`sha256:5ee38ca58b7551f252813868294b3e7bcf0cfa381fbe5256c7db0837747640f1`  
		Last Modified: Tue, 30 Sep 2025 21:32:26 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c02038c5c962e46372c533d346254ca69a84c5e120da6a2fa5e8237f0aada3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87285907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68bac847b83dd500b14b6ba1be50843667c2205abc51096b39ba8cac7b336e6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e3ca0a47d505f944b52e38a1f01835240092643e2e23c574fbe357b4571f9`  
		Last Modified: Wed, 01 Oct 2025 21:20:23 GMT  
		Size: 61.1 MB (61071100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753350ea5a9b9b29e0efbc34b8965e5e629452cc884f7a7c62994779c3dc9912`  
		Last Modified: Tue, 30 Sep 2025 01:14:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e794bb60e2416f58cdff4f685e48c8d78936d12687e23453cdf28616b9bee752`  
		Last Modified: Tue, 30 Sep 2025 01:14:06 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:8a23ef099d594ffe99a8c69f79dc29b627d3cf20f4efdb13ec9f3fbfaf85c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd0a643a2045cdab182ed9d568543f4b5a84c8ba3f9b26146cf25c109e9c46`

```dockerfile
```

-	Layers:
	-	`sha256:99081134ed748cbccefa2e85a9027e77fb0c830aac5bc880dcf3c083912b9712`  
		Last Modified: Wed, 01 Oct 2025 21:19:45 GMT  
		Size: 19.7 KB (19682 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f4563fdf791d840eeeb1d9e1b67ff1d4d7c39b306a9eb5f06f2db226487a6e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110654081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e18f227550da1dc8768ec1061690dba89ad2c5768ec1a7efa589ffe56ad86b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aef1242cf499e781216fcddef2b78081f3d1f7aa47f426845f1b847e70af0d`  
		Last Modified: Tue, 30 Sep 2025 00:16:15 GMT  
		Size: 80.5 MB (80511196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a90e6bfca1f466cd1cec43cc7918d767a06fe1a7d24faccb8e72f9d79918e1`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461be9984bef381c386ea94b6c79cb5d58e5bf043817110d4b8eec93609e7d5a`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:520c90561c90f64742da03b7e160172dc28fb70ec6a7f98901a3962f20625da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969160c2a8d28f1dd9028122950ab56d4defcd60ab02ee350cfdd4613e4c6def`

```dockerfile
```

-	Layers:
	-	`sha256:2ee77033648443ffdc6b128b310bf3599308b30966bea13d646b34e0ff109b88`  
		Last Modified: Tue, 30 Sep 2025 12:19:35 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0` - linux; 386

```console
$ docker pull varnish@sha256:2e6f1b4e8275dfb5ae193d6ebf7006be19dbd90418f6b286dfa9fcaba124cfef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114623546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba378edc8b41e0ac78fb7d7160b94056584bc998278840064b20e6e3c552aaf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629ed7a24ff9c6fc99e21417dd14d80467889003580e3ff53a891dceef00a6b`  
		Last Modified: Tue, 30 Sep 2025 00:22:36 GMT  
		Size: 83.3 MB (83326965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57eb89afe2e724f226654e1c0e3f03494b2ab8b00c84bdd180501eda7f1be8`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8a07125c1ba76ef4a10c9f4f8c272959405da5d4074be84ef010e7e3daeb84`  
		Last Modified: Tue, 30 Sep 2025 00:22:30 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:f3b9af8c499722fb4b46b87fbc09783c94e48eb053c146127a7b6469eef48d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda44628af7e53672609a7747b9c2020b0e1891ce6b74b263fce3cf1b2510f1b`

```dockerfile
```

-	Layers:
	-	`sha256:2fab048c8c298c095cf5d957c545a0de2380783658ec62c83df4739a442db74a`  
		Last Modified: Tue, 30 Sep 2025 15:21:37 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:698d9a167d7e39ef3d3a792b576e4ee35d9164c84229d0840b37aab3cf4bf9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111923681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf9f5f25dff8d15e6313cdadb31322976baf5d6fe1878df3fddedcf18b77ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888630ee3abf7ef0fe160c12c4dbc18f474c8875783ba40ff2dc298a71d1202f`  
		Last Modified: Tue, 30 Sep 2025 09:13:27 GMT  
		Size: 78.3 MB (78323180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c567d85e9f86b9e73e829c44c48c342d314211629e64015d048c9b11733e1e`  
		Last Modified: Tue, 30 Sep 2025 09:13:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392a07010bd9e6c85df4adf663f60a94bcbb243646c196f96d87f80982a9f8cf`  
		Last Modified: Tue, 30 Sep 2025 09:13:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:f28c3843800558653416a7186290b7c2333a587f98755d6fea3e339e30596d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0fc75c4ecb3c83e38b6f81c41766439fe29be027e152b88bb04e2cb6da56620`

```dockerfile
```

-	Layers:
	-	`sha256:f93bd5db122e41ce05d3286fc0377077dcb324eaf9b57cb8b0b1a7fcfb0f7480`  
		Last Modified: Wed, 01 Oct 2025 21:19:52 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0` - linux; s390x

```console
$ docker pull varnish@sha256:3bf251b37cff6a447015e1d1b090a4b24097017afcacfb2ae012d2b8a7e04427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93425005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a0a3a8b7e7e3df39e4df4a424bbf6eb691292f2b50fd21c2619c6d689cac6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b638f836f809ae3e31620a66cae836c3c3b68b284ba451e9ee536e40eaa651`  
		Last Modified: Tue, 30 Sep 2025 09:27:43 GMT  
		Size: 63.6 MB (63585726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded88d027593837b0ba58bba11d70df695a2c82a4366804ca9e520040399a17`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b78ba670c2a2180caea9453f4ea4ce1ad713d15cd2c4fad462bba0ca8545b4`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:ad60e6c63b8b23d8246f671b010fdc5a7d07b26c0da71f43981280b1f12a7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2260eaed8f6fffb7e3b42628ecd6ebc9fa6b54be77f7afa2a4560a66f2c56`

```dockerfile
```

-	Layers:
	-	`sha256:74f98e3dae4b83f9101c4cad341b804127057bde8bbd27281be38b73ec5e2138`  
		Last Modified: Wed, 01 Oct 2025 00:30:10 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.0-alpine`

```console
$ docker pull varnish@sha256:a2e68e6187c4bf3bfdf6d7d9f4dd6716cd41efaf62cb61d5f019ec150fe0ab2b
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

### `varnish:8.0.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ba8eb77be0459bf456469de17bfcda246c1170cea2949f6e36268a4fc2572c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80649740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5767790423f2deee85c93bba37a0c085dfdf901ba2625c8de97e7d01f40397`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d19719f963d4a327551f30c9936cd5e5d60c25e910f7f5a9ec84a9c2d682e6`  
		Last Modified: Thu, 09 Oct 2025 00:20:16 GMT  
		Size: 76.8 MB (76845235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083cb84d1525d5b94d9cfb9600551c78ae232af47f4bbafe99a11aba44b58ba`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f40f6190ff3cdb1a4890ffc069683aac52131b3a870ac3d2af0c2e3e7a9ffa`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6ac6f629cadc67b582643f7c4905078c6912d36aa7571441d5de8644c0c2767c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102d50b64eac75ab5f17fa71d569a08a4f62f2bb0f1c0c6365cfe1ac48e2122`

```dockerfile
```

-	Layers:
	-	`sha256:beabe22d3dfff560717c37f0887b9b883923342c0d22d5ec68cf9652a1209463`  
		Last Modified: Thu, 09 Oct 2025 00:19:52 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e624ea76108774c09f9e48032091401821dfdb94cf59624daf83ffc8490a0b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62654398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae51093fc76d05ea36eaf5469c85d6275a6a811822a0773eb25293512bcac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336ba603488fddde3a5260a9fddc822e750dfbfc59da41b6536b9a99cd34515`  
		Last Modified: Wed, 08 Oct 2025 22:12:09 GMT  
		Size: 59.4 MB (59430786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3d374d0d4a1a8ff7a1c6fcb91410aeafcf2f8880ca05eebe06bf7604a01111`  
		Last Modified: Wed, 08 Oct 2025 22:12:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99e557263f6da4d98b610f5d3d45b0c8e156c6b96bc49f3c1f314ae656a2a4c`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9078640134ba8b45cdb3b09c56f97c02c4d54bcc6c26ffc1aac9d4e19bc08baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc606692f8108ef5d823be4b268b7fbb6f77777b044ef151882fa21e492c9a1`

```dockerfile
```

-	Layers:
	-	`sha256:085e876cc8d3d19c17b2f7986a3e6f2bbf0bb1337153e3d459ea5eb2bdf943f9`  
		Last Modified: Thu, 09 Oct 2025 00:19:55 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2d60c0f5043faf5c659a586a9aeb8e3f2f6b77b1de74457ba2302154906e3b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77646588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d859ae3182d210801ea3d56332c129a0fdd14660537ee96e871dd650be10009`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89df23746d0dc373775c6c3909ef191fc5b685a8414cdcac2b1104e4354d8213`  
		Last Modified: Wed, 08 Oct 2025 21:47:22 GMT  
		Size: 73.5 MB (73506464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a4838380d12fe8a616bb2554ca0fad2162efeeb8f3cd2c80662d848c36bab1`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa02b94be62585c016a55f8ba157f043c2fd3ceb77edd0bb0f29d2c7988860`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:56acacec5d07daf794ba7631eef4916b5e2818995d2f4b688aefae71b2f63066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f568cf93c272ad9235cbea7d929f9a6185ea1414d13f6f33eda459c3b3d34b0`

```dockerfile
```

-	Layers:
	-	`sha256:509cafe80bab2cdc5955af89fe1b042ac21e60d489bd03d33624efe954b91379`  
		Last Modified: Thu, 09 Oct 2025 00:19:58 GMT  
		Size: 19.4 KB (19438 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:65206c02858aecf59c8ec6bfaaafa059f4e4901bd876a9dec0c215d51e1f2a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82874569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3164ef01d5ae90f502da0b6f9da074b36fa56ff2b0d6ff297f9359e3d74e0a8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cb961e3fec70bb2f3b518c46ada6f4ca49360acd574cf45ec32b32eaafb01b`  
		Last Modified: Wed, 08 Oct 2025 21:41:33 GMT  
		Size: 79.3 MB (79253583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78236060e4a99dac0a6931eb84850f7caab72617e2c0bc7a4c41a1e58c9047c`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a08316b257931ed28a9aa1962f4220f5f2c0ef72b1b9bd744ba704082491e`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0408eb02adca0c5fd76a410aedf2c9d409145229ae11ef5f93a2e31b0b8645af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739495427886fd79e3484e3bd305e575b5da6e9c8dd9b728e7d09c34b5d657da`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c9a00e2d724a783a713638779b64c37b740ccd716e28e35c5ba70f5b0015`  
		Last Modified: Thu, 09 Oct 2025 00:20:02 GMT  
		Size: 19.3 KB (19285 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:677cc3ec09c593cfdf723379d9120bd1b9b407eeb508b4ad2bcaba9346b28aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e035d28b41a18d5fefb7a12f9e2523688e7cbb4973c6f58d4189c2a396395d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08db313ba0b74ae969f29bc00b7803b78db0de38106aab9fa13e6fc4c20ff06`  
		Last Modified: Thu, 09 Oct 2025 03:37:12 GMT  
		Size: 73.0 MB (73040138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a125238abb15614acca8c40fbbdf92434d2d8f057fae857298235de015531b2`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4376b12c3b402608cb7391bb3c6042ccd7e850142306e2a0b8ba13507296e4d1`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a1fdea113bc5acf33aa0908c87ad481e8fb471c0c16043320014b0d30d1a8d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3520cddf7d20e95153c75f682aaa3b623d23c9116963cf67c3f5303339bdefd`

```dockerfile
```

-	Layers:
	-	`sha256:f2ce0afefc61f5a41d9a3426b61425c87e3bee67d737063113e3bd24821f54e3`  
		Last Modified: Thu, 09 Oct 2025 06:19:43 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:e040b0db456d799b0ff9dcea9b17bda702c27d05cadbd345d5add1e9f8f7a55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71428457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60881cbce6790d05e3be256b05124ed36d4f58d94bceb295841ea392f7ebab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2bd97591c904b46405111198f80adcb211a3d82071b457cd6ead8e0d6b631c`  
		Last Modified: Thu, 09 Oct 2025 02:30:48 GMT  
		Size: 67.8 MB (67777154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211e62f62da811326f4c91458d5841b9582b8d0470bc1998e17467eff9c03ad3`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d475471c3c97d3a9c9ea4a34f85ba393635831e8a0afec1466cd431135ac8c57`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1c14e3e6e67b7aa214245bb2b5d4da8a77fd5d6d3e4e06172a74921f6b806164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9629cc539632351d549586b170aa75b664d5d7658312a091153217619f6184a4`

```dockerfile
```

-	Layers:
	-	`sha256:02e61c597cad44d949cacce426a408a5ed4f30945003406052031e88e5a71423`  
		Last Modified: Thu, 09 Oct 2025 03:19:40 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:a2e68e6187c4bf3bfdf6d7d9f4dd6716cd41efaf62cb61d5f019ec150fe0ab2b
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

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ba8eb77be0459bf456469de17bfcda246c1170cea2949f6e36268a4fc2572c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80649740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5767790423f2deee85c93bba37a0c085dfdf901ba2625c8de97e7d01f40397`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d19719f963d4a327551f30c9936cd5e5d60c25e910f7f5a9ec84a9c2d682e6`  
		Last Modified: Thu, 09 Oct 2025 00:20:16 GMT  
		Size: 76.8 MB (76845235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083cb84d1525d5b94d9cfb9600551c78ae232af47f4bbafe99a11aba44b58ba`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f40f6190ff3cdb1a4890ffc069683aac52131b3a870ac3d2af0c2e3e7a9ffa`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6ac6f629cadc67b582643f7c4905078c6912d36aa7571441d5de8644c0c2767c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102d50b64eac75ab5f17fa71d569a08a4f62f2bb0f1c0c6365cfe1ac48e2122`

```dockerfile
```

-	Layers:
	-	`sha256:beabe22d3dfff560717c37f0887b9b883923342c0d22d5ec68cf9652a1209463`  
		Last Modified: Thu, 09 Oct 2025 00:19:52 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e624ea76108774c09f9e48032091401821dfdb94cf59624daf83ffc8490a0b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62654398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae51093fc76d05ea36eaf5469c85d6275a6a811822a0773eb25293512bcac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336ba603488fddde3a5260a9fddc822e750dfbfc59da41b6536b9a99cd34515`  
		Last Modified: Wed, 08 Oct 2025 22:12:09 GMT  
		Size: 59.4 MB (59430786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3d374d0d4a1a8ff7a1c6fcb91410aeafcf2f8880ca05eebe06bf7604a01111`  
		Last Modified: Wed, 08 Oct 2025 22:12:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99e557263f6da4d98b610f5d3d45b0c8e156c6b96bc49f3c1f314ae656a2a4c`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9078640134ba8b45cdb3b09c56f97c02c4d54bcc6c26ffc1aac9d4e19bc08baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc606692f8108ef5d823be4b268b7fbb6f77777b044ef151882fa21e492c9a1`

```dockerfile
```

-	Layers:
	-	`sha256:085e876cc8d3d19c17b2f7986a3e6f2bbf0bb1337153e3d459ea5eb2bdf943f9`  
		Last Modified: Thu, 09 Oct 2025 00:19:55 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2d60c0f5043faf5c659a586a9aeb8e3f2f6b77b1de74457ba2302154906e3b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77646588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d859ae3182d210801ea3d56332c129a0fdd14660537ee96e871dd650be10009`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89df23746d0dc373775c6c3909ef191fc5b685a8414cdcac2b1104e4354d8213`  
		Last Modified: Wed, 08 Oct 2025 21:47:22 GMT  
		Size: 73.5 MB (73506464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a4838380d12fe8a616bb2554ca0fad2162efeeb8f3cd2c80662d848c36bab1`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa02b94be62585c016a55f8ba157f043c2fd3ceb77edd0bb0f29d2c7988860`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:56acacec5d07daf794ba7631eef4916b5e2818995d2f4b688aefae71b2f63066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f568cf93c272ad9235cbea7d929f9a6185ea1414d13f6f33eda459c3b3d34b0`

```dockerfile
```

-	Layers:
	-	`sha256:509cafe80bab2cdc5955af89fe1b042ac21e60d489bd03d33624efe954b91379`  
		Last Modified: Thu, 09 Oct 2025 00:19:58 GMT  
		Size: 19.4 KB (19438 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:65206c02858aecf59c8ec6bfaaafa059f4e4901bd876a9dec0c215d51e1f2a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82874569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3164ef01d5ae90f502da0b6f9da074b36fa56ff2b0d6ff297f9359e3d74e0a8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cb961e3fec70bb2f3b518c46ada6f4ca49360acd574cf45ec32b32eaafb01b`  
		Last Modified: Wed, 08 Oct 2025 21:41:33 GMT  
		Size: 79.3 MB (79253583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78236060e4a99dac0a6931eb84850f7caab72617e2c0bc7a4c41a1e58c9047c`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a08316b257931ed28a9aa1962f4220f5f2c0ef72b1b9bd744ba704082491e`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0408eb02adca0c5fd76a410aedf2c9d409145229ae11ef5f93a2e31b0b8645af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739495427886fd79e3484e3bd305e575b5da6e9c8dd9b728e7d09c34b5d657da`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c9a00e2d724a783a713638779b64c37b740ccd716e28e35c5ba70f5b0015`  
		Last Modified: Thu, 09 Oct 2025 00:20:02 GMT  
		Size: 19.3 KB (19285 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:677cc3ec09c593cfdf723379d9120bd1b9b407eeb508b4ad2bcaba9346b28aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e035d28b41a18d5fefb7a12f9e2523688e7cbb4973c6f58d4189c2a396395d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08db313ba0b74ae969f29bc00b7803b78db0de38106aab9fa13e6fc4c20ff06`  
		Last Modified: Thu, 09 Oct 2025 03:37:12 GMT  
		Size: 73.0 MB (73040138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a125238abb15614acca8c40fbbdf92434d2d8f057fae857298235de015531b2`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4376b12c3b402608cb7391bb3c6042ccd7e850142306e2a0b8ba13507296e4d1`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a1fdea113bc5acf33aa0908c87ad481e8fb471c0c16043320014b0d30d1a8d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3520cddf7d20e95153c75f682aaa3b623d23c9116963cf67c3f5303339bdefd`

```dockerfile
```

-	Layers:
	-	`sha256:f2ce0afefc61f5a41d9a3426b61425c87e3bee67d737063113e3bd24821f54e3`  
		Last Modified: Thu, 09 Oct 2025 06:19:43 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:e040b0db456d799b0ff9dcea9b17bda702c27d05cadbd345d5add1e9f8f7a55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71428457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60881cbce6790d05e3be256b05124ed36d4f58d94bceb295841ea392f7ebab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2bd97591c904b46405111198f80adcb211a3d82071b457cd6ead8e0d6b631c`  
		Last Modified: Thu, 09 Oct 2025 02:30:48 GMT  
		Size: 67.8 MB (67777154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211e62f62da811326f4c91458d5841b9582b8d0470bc1998e17467eff9c03ad3`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d475471c3c97d3a9c9ea4a34f85ba393635831e8a0afec1466cd431135ac8c57`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1c14e3e6e67b7aa214245bb2b5d4da8a77fd5d6d3e4e06172a74921f6b806164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9629cc539632351d549586b170aa75b664d5d7658312a091153217619f6184a4`

```dockerfile
```

-	Layers:
	-	`sha256:02e61c597cad44d949cacce426a408a5ed4f30945003406052031e88e5a71423`  
		Last Modified: Thu, 09 Oct 2025 03:19:40 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:6ae8d462e3e2915e3be0c156b8864f842fb9bc8cf5f35b891c4bd1315979b33f
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

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:c97e31abb26c2a4bc80a60d0ca080f1e3a18e31ace60dbbaf4037ba29f9f3d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116466266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004bda53957dbb10230c7308b9596abf362bd6a0699bffa29463a7799274c2da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe861ac020fae87c9b3ce06a9bb9d050070b059d6c2a12c4ab7c81af27f4b2`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 86.7 MB (86686458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a2eafd8f6a49966509e8c6c54adeada7389ecb2bf14d232209ec99d6b78d7`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095bb281dc5a0973162db00f0de12ba6ac3f347e5c674d0a31052e2959ff96bf`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:3968cd90f6dd9784b74ecd501fe63144337ecb3e3abdee2961ac95dc51fbf32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82998fc1361929d6bd83b06965600e1bbdb0ff26200bdbab4a7850b941cca`

```dockerfile
```

-	Layers:
	-	`sha256:5ee38ca58b7551f252813868294b3e7bcf0cfa381fbe5256c7db0837747640f1`  
		Last Modified: Tue, 30 Sep 2025 21:32:26 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c02038c5c962e46372c533d346254ca69a84c5e120da6a2fa5e8237f0aada3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87285907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68bac847b83dd500b14b6ba1be50843667c2205abc51096b39ba8cac7b336e6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e3ca0a47d505f944b52e38a1f01835240092643e2e23c574fbe357b4571f9`  
		Last Modified: Wed, 01 Oct 2025 21:20:23 GMT  
		Size: 61.1 MB (61071100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753350ea5a9b9b29e0efbc34b8965e5e629452cc884f7a7c62994779c3dc9912`  
		Last Modified: Tue, 30 Sep 2025 01:14:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e794bb60e2416f58cdff4f685e48c8d78936d12687e23453cdf28616b9bee752`  
		Last Modified: Tue, 30 Sep 2025 01:14:06 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:8a23ef099d594ffe99a8c69f79dc29b627d3cf20f4efdb13ec9f3fbfaf85c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd0a643a2045cdab182ed9d568543f4b5a84c8ba3f9b26146cf25c109e9c46`

```dockerfile
```

-	Layers:
	-	`sha256:99081134ed748cbccefa2e85a9027e77fb0c830aac5bc880dcf3c083912b9712`  
		Last Modified: Wed, 01 Oct 2025 21:19:45 GMT  
		Size: 19.7 KB (19682 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f4563fdf791d840eeeb1d9e1b67ff1d4d7c39b306a9eb5f06f2db226487a6e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110654081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e18f227550da1dc8768ec1061690dba89ad2c5768ec1a7efa589ffe56ad86b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aef1242cf499e781216fcddef2b78081f3d1f7aa47f426845f1b847e70af0d`  
		Last Modified: Tue, 30 Sep 2025 00:16:15 GMT  
		Size: 80.5 MB (80511196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a90e6bfca1f466cd1cec43cc7918d767a06fe1a7d24faccb8e72f9d79918e1`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461be9984bef381c386ea94b6c79cb5d58e5bf043817110d4b8eec93609e7d5a`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:520c90561c90f64742da03b7e160172dc28fb70ec6a7f98901a3962f20625da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969160c2a8d28f1dd9028122950ab56d4defcd60ab02ee350cfdd4613e4c6def`

```dockerfile
```

-	Layers:
	-	`sha256:2ee77033648443ffdc6b128b310bf3599308b30966bea13d646b34e0ff109b88`  
		Last Modified: Tue, 30 Sep 2025 12:19:35 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:2e6f1b4e8275dfb5ae193d6ebf7006be19dbd90418f6b286dfa9fcaba124cfef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114623546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba378edc8b41e0ac78fb7d7160b94056584bc998278840064b20e6e3c552aaf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629ed7a24ff9c6fc99e21417dd14d80467889003580e3ff53a891dceef00a6b`  
		Last Modified: Tue, 30 Sep 2025 00:22:36 GMT  
		Size: 83.3 MB (83326965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57eb89afe2e724f226654e1c0e3f03494b2ab8b00c84bdd180501eda7f1be8`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8a07125c1ba76ef4a10c9f4f8c272959405da5d4074be84ef010e7e3daeb84`  
		Last Modified: Tue, 30 Sep 2025 00:22:30 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:f3b9af8c499722fb4b46b87fbc09783c94e48eb053c146127a7b6469eef48d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda44628af7e53672609a7747b9c2020b0e1891ce6b74b263fce3cf1b2510f1b`

```dockerfile
```

-	Layers:
	-	`sha256:2fab048c8c298c095cf5d957c545a0de2380783658ec62c83df4739a442db74a`  
		Last Modified: Tue, 30 Sep 2025 15:21:37 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:698d9a167d7e39ef3d3a792b576e4ee35d9164c84229d0840b37aab3cf4bf9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111923681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf9f5f25dff8d15e6313cdadb31322976baf5d6fe1878df3fddedcf18b77ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888630ee3abf7ef0fe160c12c4dbc18f474c8875783ba40ff2dc298a71d1202f`  
		Last Modified: Tue, 30 Sep 2025 09:13:27 GMT  
		Size: 78.3 MB (78323180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c567d85e9f86b9e73e829c44c48c342d314211629e64015d048c9b11733e1e`  
		Last Modified: Tue, 30 Sep 2025 09:13:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392a07010bd9e6c85df4adf663f60a94bcbb243646c196f96d87f80982a9f8cf`  
		Last Modified: Tue, 30 Sep 2025 09:13:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:f28c3843800558653416a7186290b7c2333a587f98755d6fea3e339e30596d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0fc75c4ecb3c83e38b6f81c41766439fe29be027e152b88bb04e2cb6da56620`

```dockerfile
```

-	Layers:
	-	`sha256:f93bd5db122e41ce05d3286fc0377077dcb324eaf9b57cb8b0b1a7fcfb0f7480`  
		Last Modified: Wed, 01 Oct 2025 21:19:52 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:3bf251b37cff6a447015e1d1b090a4b24097017afcacfb2ae012d2b8a7e04427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93425005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a0a3a8b7e7e3df39e4df4a424bbf6eb691292f2b50fd21c2619c6d689cac6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b638f836f809ae3e31620a66cae836c3c3b68b284ba451e9ee536e40eaa651`  
		Last Modified: Tue, 30 Sep 2025 09:27:43 GMT  
		Size: 63.6 MB (63585726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded88d027593837b0ba58bba11d70df695a2c82a4366804ca9e520040399a17`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b78ba670c2a2180caea9453f4ea4ce1ad713d15cd2c4fad462bba0ca8545b4`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:ad60e6c63b8b23d8246f671b010fdc5a7d07b26c0da71f43981280b1f12a7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2260eaed8f6fffb7e3b42628ecd6ebc9fa6b54be77f7afa2a4560a66f2c56`

```dockerfile
```

-	Layers:
	-	`sha256:74f98e3dae4b83f9101c4cad341b804127057bde8bbd27281be38b73ec5e2138`  
		Last Modified: Wed, 01 Oct 2025 00:30:10 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:a2e68e6187c4bf3bfdf6d7d9f4dd6716cd41efaf62cb61d5f019ec150fe0ab2b
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

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ba8eb77be0459bf456469de17bfcda246c1170cea2949f6e36268a4fc2572c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80649740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5767790423f2deee85c93bba37a0c085dfdf901ba2625c8de97e7d01f40397`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d19719f963d4a327551f30c9936cd5e5d60c25e910f7f5a9ec84a9c2d682e6`  
		Last Modified: Thu, 09 Oct 2025 00:20:16 GMT  
		Size: 76.8 MB (76845235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083cb84d1525d5b94d9cfb9600551c78ae232af47f4bbafe99a11aba44b58ba`  
		Last Modified: Wed, 08 Oct 2025 23:38:29 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f40f6190ff3cdb1a4890ffc069683aac52131b3a870ac3d2af0c2e3e7a9ffa`  
		Last Modified: Wed, 08 Oct 2025 23:38:28 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6ac6f629cadc67b582643f7c4905078c6912d36aa7571441d5de8644c0c2767c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102d50b64eac75ab5f17fa71d569a08a4f62f2bb0f1c0c6365cfe1ac48e2122`

```dockerfile
```

-	Layers:
	-	`sha256:beabe22d3dfff560717c37f0887b9b883923342c0d22d5ec68cf9652a1209463`  
		Last Modified: Thu, 09 Oct 2025 00:19:52 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e624ea76108774c09f9e48032091401821dfdb94cf59624daf83ffc8490a0b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62654398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae51093fc76d05ea36eaf5469c85d6275a6a811822a0773eb25293512bcac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336ba603488fddde3a5260a9fddc822e750dfbfc59da41b6536b9a99cd34515`  
		Last Modified: Wed, 08 Oct 2025 22:12:09 GMT  
		Size: 59.4 MB (59430786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3d374d0d4a1a8ff7a1c6fcb91410aeafcf2f8880ca05eebe06bf7604a01111`  
		Last Modified: Wed, 08 Oct 2025 22:12:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99e557263f6da4d98b610f5d3d45b0c8e156c6b96bc49f3c1f314ae656a2a4c`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9078640134ba8b45cdb3b09c56f97c02c4d54bcc6c26ffc1aac9d4e19bc08baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc606692f8108ef5d823be4b268b7fbb6f77777b044ef151882fa21e492c9a1`

```dockerfile
```

-	Layers:
	-	`sha256:085e876cc8d3d19c17b2f7986a3e6f2bbf0bb1337153e3d459ea5eb2bdf943f9`  
		Last Modified: Thu, 09 Oct 2025 00:19:55 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2d60c0f5043faf5c659a586a9aeb8e3f2f6b77b1de74457ba2302154906e3b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77646588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d859ae3182d210801ea3d56332c129a0fdd14660537ee96e871dd650be10009`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89df23746d0dc373775c6c3909ef191fc5b685a8414cdcac2b1104e4354d8213`  
		Last Modified: Wed, 08 Oct 2025 21:47:22 GMT  
		Size: 73.5 MB (73506464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a4838380d12fe8a616bb2554ca0fad2162efeeb8f3cd2c80662d848c36bab1`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa02b94be62585c016a55f8ba157f043c2fd3ceb77edd0bb0f29d2c7988860`  
		Last Modified: Wed, 08 Oct 2025 21:47:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:56acacec5d07daf794ba7631eef4916b5e2818995d2f4b688aefae71b2f63066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f568cf93c272ad9235cbea7d929f9a6185ea1414d13f6f33eda459c3b3d34b0`

```dockerfile
```

-	Layers:
	-	`sha256:509cafe80bab2cdc5955af89fe1b042ac21e60d489bd03d33624efe954b91379`  
		Last Modified: Thu, 09 Oct 2025 00:19:58 GMT  
		Size: 19.4 KB (19438 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:65206c02858aecf59c8ec6bfaaafa059f4e4901bd876a9dec0c215d51e1f2a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82874569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3164ef01d5ae90f502da0b6f9da074b36fa56ff2b0d6ff297f9359e3d74e0a8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cb961e3fec70bb2f3b518c46ada6f4ca49360acd574cf45ec32b32eaafb01b`  
		Last Modified: Wed, 08 Oct 2025 21:41:33 GMT  
		Size: 79.3 MB (79253583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78236060e4a99dac0a6931eb84850f7caab72617e2c0bc7a4c41a1e58c9047c`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a08316b257931ed28a9aa1962f4220f5f2c0ef72b1b9bd744ba704082491e`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0408eb02adca0c5fd76a410aedf2c9d409145229ae11ef5f93a2e31b0b8645af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739495427886fd79e3484e3bd305e575b5da6e9c8dd9b728e7d09c34b5d657da`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2c9a00e2d724a783a713638779b64c37b740ccd716e28e35c5ba70f5b0015`  
		Last Modified: Thu, 09 Oct 2025 00:20:02 GMT  
		Size: 19.3 KB (19285 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:677cc3ec09c593cfdf723379d9120bd1b9b407eeb508b4ad2bcaba9346b28aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76774439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e035d28b41a18d5fefb7a12f9e2523688e7cbb4973c6f58d4189c2a396395d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08db313ba0b74ae969f29bc00b7803b78db0de38106aab9fa13e6fc4c20ff06`  
		Last Modified: Thu, 09 Oct 2025 03:37:12 GMT  
		Size: 73.0 MB (73040138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a125238abb15614acca8c40fbbdf92434d2d8f057fae857298235de015531b2`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4376b12c3b402608cb7391bb3c6042ccd7e850142306e2a0b8ba13507296e4d1`  
		Last Modified: Thu, 09 Oct 2025 03:37:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a1fdea113bc5acf33aa0908c87ad481e8fb471c0c16043320014b0d30d1a8d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3520cddf7d20e95153c75f682aaa3b623d23c9116963cf67c3f5303339bdefd`

```dockerfile
```

-	Layers:
	-	`sha256:f2ce0afefc61f5a41d9a3426b61425c87e3bee67d737063113e3bd24821f54e3`  
		Last Modified: Thu, 09 Oct 2025 06:19:43 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:e040b0db456d799b0ff9dcea9b17bda702c27d05cadbd345d5add1e9f8f7a55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71428457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60881cbce6790d05e3be256b05124ed36d4f58d94bceb295841ea392f7ebab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2bd97591c904b46405111198f80adcb211a3d82071b457cd6ead8e0d6b631c`  
		Last Modified: Thu, 09 Oct 2025 02:30:48 GMT  
		Size: 67.8 MB (67777154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211e62f62da811326f4c91458d5841b9582b8d0470bc1998e17467eff9c03ad3`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d475471c3c97d3a9c9ea4a34f85ba393635831e8a0afec1466cd431135ac8c57`  
		Last Modified: Thu, 09 Oct 2025 02:30:35 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1c14e3e6e67b7aa214245bb2b5d4da8a77fd5d6d3e4e06172a74921f6b806164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9629cc539632351d549586b170aa75b664d5d7658312a091153217619f6184a4`

```dockerfile
```

-	Layers:
	-	`sha256:02e61c597cad44d949cacce426a408a5ed4f30945003406052031e88e5a71423`  
		Last Modified: Thu, 09 Oct 2025 03:19:40 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:6ae8d462e3e2915e3be0c156b8864f842fb9bc8cf5f35b891c4bd1315979b33f
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
$ docker pull varnish@sha256:c97e31abb26c2a4bc80a60d0ca080f1e3a18e31ace60dbbaf4037ba29f9f3d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116466266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004bda53957dbb10230c7308b9596abf362bd6a0699bffa29463a7799274c2da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe861ac020fae87c9b3ce06a9bb9d050070b059d6c2a12c4ab7c81af27f4b2`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 86.7 MB (86686458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a2eafd8f6a49966509e8c6c54adeada7389ecb2bf14d232209ec99d6b78d7`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095bb281dc5a0973162db00f0de12ba6ac3f347e5c674d0a31052e2959ff96bf`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:3968cd90f6dd9784b74ecd501fe63144337ecb3e3abdee2961ac95dc51fbf32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82998fc1361929d6bd83b06965600e1bbdb0ff26200bdbab4a7850b941cca`

```dockerfile
```

-	Layers:
	-	`sha256:5ee38ca58b7551f252813868294b3e7bcf0cfa381fbe5256c7db0837747640f1`  
		Last Modified: Tue, 30 Sep 2025 21:32:26 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c02038c5c962e46372c533d346254ca69a84c5e120da6a2fa5e8237f0aada3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87285907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68bac847b83dd500b14b6ba1be50843667c2205abc51096b39ba8cac7b336e6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e3ca0a47d505f944b52e38a1f01835240092643e2e23c574fbe357b4571f9`  
		Last Modified: Wed, 01 Oct 2025 21:20:23 GMT  
		Size: 61.1 MB (61071100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753350ea5a9b9b29e0efbc34b8965e5e629452cc884f7a7c62994779c3dc9912`  
		Last Modified: Tue, 30 Sep 2025 01:14:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e794bb60e2416f58cdff4f685e48c8d78936d12687e23453cdf28616b9bee752`  
		Last Modified: Tue, 30 Sep 2025 01:14:06 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:8a23ef099d594ffe99a8c69f79dc29b627d3cf20f4efdb13ec9f3fbfaf85c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd0a643a2045cdab182ed9d568543f4b5a84c8ba3f9b26146cf25c109e9c46`

```dockerfile
```

-	Layers:
	-	`sha256:99081134ed748cbccefa2e85a9027e77fb0c830aac5bc880dcf3c083912b9712`  
		Last Modified: Wed, 01 Oct 2025 21:19:45 GMT  
		Size: 19.7 KB (19682 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f4563fdf791d840eeeb1d9e1b67ff1d4d7c39b306a9eb5f06f2db226487a6e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110654081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e18f227550da1dc8768ec1061690dba89ad2c5768ec1a7efa589ffe56ad86b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aef1242cf499e781216fcddef2b78081f3d1f7aa47f426845f1b847e70af0d`  
		Last Modified: Tue, 30 Sep 2025 00:16:15 GMT  
		Size: 80.5 MB (80511196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a90e6bfca1f466cd1cec43cc7918d767a06fe1a7d24faccb8e72f9d79918e1`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461be9984bef381c386ea94b6c79cb5d58e5bf043817110d4b8eec93609e7d5a`  
		Last Modified: Tue, 30 Sep 2025 00:16:07 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:520c90561c90f64742da03b7e160172dc28fb70ec6a7f98901a3962f20625da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969160c2a8d28f1dd9028122950ab56d4defcd60ab02ee350cfdd4613e4c6def`

```dockerfile
```

-	Layers:
	-	`sha256:2ee77033648443ffdc6b128b310bf3599308b30966bea13d646b34e0ff109b88`  
		Last Modified: Tue, 30 Sep 2025 12:19:35 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:2e6f1b4e8275dfb5ae193d6ebf7006be19dbd90418f6b286dfa9fcaba124cfef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114623546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba378edc8b41e0ac78fb7d7160b94056584bc998278840064b20e6e3c552aaf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629ed7a24ff9c6fc99e21417dd14d80467889003580e3ff53a891dceef00a6b`  
		Last Modified: Tue, 30 Sep 2025 00:22:36 GMT  
		Size: 83.3 MB (83326965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57eb89afe2e724f226654e1c0e3f03494b2ab8b00c84bdd180501eda7f1be8`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8a07125c1ba76ef4a10c9f4f8c272959405da5d4074be84ef010e7e3daeb84`  
		Last Modified: Tue, 30 Sep 2025 00:22:30 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:f3b9af8c499722fb4b46b87fbc09783c94e48eb053c146127a7b6469eef48d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda44628af7e53672609a7747b9c2020b0e1891ce6b74b263fce3cf1b2510f1b`

```dockerfile
```

-	Layers:
	-	`sha256:2fab048c8c298c095cf5d957c545a0de2380783658ec62c83df4739a442db74a`  
		Last Modified: Tue, 30 Sep 2025 15:21:37 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:698d9a167d7e39ef3d3a792b576e4ee35d9164c84229d0840b37aab3cf4bf9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111923681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf9f5f25dff8d15e6313cdadb31322976baf5d6fe1878df3fddedcf18b77ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888630ee3abf7ef0fe160c12c4dbc18f474c8875783ba40ff2dc298a71d1202f`  
		Last Modified: Tue, 30 Sep 2025 09:13:27 GMT  
		Size: 78.3 MB (78323180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c567d85e9f86b9e73e829c44c48c342d314211629e64015d048c9b11733e1e`  
		Last Modified: Tue, 30 Sep 2025 09:13:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392a07010bd9e6c85df4adf663f60a94bcbb243646c196f96d87f80982a9f8cf`  
		Last Modified: Tue, 30 Sep 2025 09:13:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:f28c3843800558653416a7186290b7c2333a587f98755d6fea3e339e30596d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0fc75c4ecb3c83e38b6f81c41766439fe29be027e152b88bb04e2cb6da56620`

```dockerfile
```

-	Layers:
	-	`sha256:f93bd5db122e41ce05d3286fc0377077dcb324eaf9b57cb8b0b1a7fcfb0f7480`  
		Last Modified: Wed, 01 Oct 2025 21:19:52 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:3bf251b37cff6a447015e1d1b090a4b24097017afcacfb2ae012d2b8a7e04427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93425005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a0a3a8b7e7e3df39e4df4a424bbf6eb691292f2b50fd21c2619c6d689cac6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b638f836f809ae3e31620a66cae836c3c3b68b284ba451e9ee536e40eaa651`  
		Last Modified: Tue, 30 Sep 2025 09:27:43 GMT  
		Size: 63.6 MB (63585726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded88d027593837b0ba58bba11d70df695a2c82a4366804ca9e520040399a17`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b78ba670c2a2180caea9453f4ea4ce1ad713d15cd2c4fad462bba0ca8545b4`  
		Last Modified: Tue, 30 Sep 2025 09:27:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:ad60e6c63b8b23d8246f671b010fdc5a7d07b26c0da71f43981280b1f12a7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2260eaed8f6fffb7e3b42628ecd6ebc9fa6b54be77f7afa2a4560a66f2c56`

```dockerfile
```

-	Layers:
	-	`sha256:74f98e3dae4b83f9101c4cad341b804127057bde8bbd27281be38b73ec5e2138`  
		Last Modified: Wed, 01 Oct 2025 00:30:10 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:9310a9cbdb61b632afb83fff44fa7c71b90f987a0587d23fc159e3b22334d577
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

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:feb27787cd34f85263e0c591a947c90a01ca9082d4db5e8d56ce8fd39ececd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116344965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0192faac62b9eec84df7907e4eb139a9ea473cc3e7c57c78c15aa40651aeff5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b82bb006d56a9a208eca4bffb9e1e098368320b3fab7f67cdc2dd79dad4c86`  
		Last Modified: Tue, 30 Sep 2025 21:33:06 GMT  
		Size: 86.6 MB (86565152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7cb22c2f76de71127b4e09b5455fc95836614c6c0c5a941181219883745b5e`  
		Last Modified: Tue, 30 Sep 2025 01:05:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036dd63ac5b112d011fa5fda2c3d53d5384ef1b2e12fc332f168fa0e9b92bf9d`  
		Last Modified: Tue, 30 Sep 2025 01:05:11 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:d2c49efdb9688d0933b973d5d4f3c3121cdc3bffddbb2400a1bff80fa5744200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aeaece4ccec8dbdfa7a985432df4a634c5bab3e367c8f0b727ea27947260e6`

```dockerfile
```

-	Layers:
	-	`sha256:09149e48eec29e1632ede18e8bcc7660017d23659e476a5c05e21b76af9fa71a`  
		Last Modified: Tue, 30 Sep 2025 21:32:47 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9a0a576248e3d011b4947e5a74e61c5c7ff29f38ff030eb06baa9550348ff161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87152968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d5b118f151e98200705c07123a2452e185dc36beb379bf01a3959e6d7120a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3ef5967cc3af519476a7d1003a8c50ff757dc2ad6fc3efb554c5930835bdef`  
		Last Modified: Tue, 30 Sep 2025 01:07:11 GMT  
		Size: 60.9 MB (60938163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df71cd8f1ded8d32285abf30be2878d4c27c61bbf4dd27fddfa6756af4dfca15`  
		Last Modified: Tue, 30 Sep 2025 01:07:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf0fae6e41dd18ce4bd19f5903c4ccf7a8c60af8a43028ba0473bbed6f182a`  
		Last Modified: Tue, 30 Sep 2025 01:07:06 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:32ae2e7ec68987e97ca435fa46c0032a9b3632ac990b17dbc97c57dab02f7c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f763821ad5c8f0de3985f062c5a06915836b0d147d1cd3784c8cc1409dd3c90d`

```dockerfile
```

-	Layers:
	-	`sha256:3b3061b7c84355510b63919b85ac719ff16b89a1896f7110d335a8596e589096`  
		Last Modified: Wed, 01 Oct 2025 21:19:33 GMT  
		Size: 19.1 KB (19132 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0d7c1c994530d1ed1ca5853a890e344630822f13d8d9178cac04b849b59c52cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110523275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823d030972d97c92df6bc33ef78be438ad647d179137fe35f4bfb6f61d8db9ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378788f9ca239860d89fb5c3bbea1545f80a9267aa9459ec3f9da569d769ed18`  
		Last Modified: Tue, 30 Sep 2025 00:15:42 GMT  
		Size: 80.4 MB (80380388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb797e799e3bd572e943838004c1524a12dbcae17a3f5745748f6cf4c918f2cc`  
		Last Modified: Tue, 30 Sep 2025 00:15:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff005f26e2985d74a3fbf6d89f2eefd91990d5d3e5d0079f3436f7f0f5d03907`  
		Last Modified: Tue, 30 Sep 2025 00:15:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:4ea1f26847fd13abcc92c49e207e1348e5aa24daedc35ab91326e39467ecae6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20574620b612025dc02f51df435429c5bfbdad7b3f8c33785deb4cd003aa1386`

```dockerfile
```

-	Layers:
	-	`sha256:0515453d2e39868223779e91e4f179ca2d1489b84e6801d027381d9bb9d225f6`  
		Last Modified: Wed, 01 Oct 2025 12:30:32 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:c75c4ed9c763f676a84df2cab594c7feb7b572205a3220e15c0f60841b642d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114480792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377b468274da6095a7f77a47984053439376992a1405ea905800600b71dc1046`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541acb4695489a091f8e5ef52e0305e4d07442c2c732b3e283b9a52b864b69b6`  
		Last Modified: Tue, 30 Sep 2025 00:22:30 GMT  
		Size: 83.2 MB (83184211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57eb89afe2e724f226654e1c0e3f03494b2ab8b00c84bdd180501eda7f1be8`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac1c1e383ee3b87879b512392777229af0dc886705fc472d405f32456bc99b`  
		Last Modified: Tue, 30 Sep 2025 00:22:23 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:dcc28285e54b4016cb30e6a2c4bcb82c727bad02e68be857268a32265839ee18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186bd63fb6a66f62f0e8d25bd70e7acbf722ceae870f9ffb7120227f11054219`

```dockerfile
```

-	Layers:
	-	`sha256:6d79edad424240488ffad7394464124b187930d9cc060ac6ddfb85373ff8160b`  
		Last Modified: Tue, 30 Sep 2025 15:21:28 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:4bc9bc90b7dd65041a2467a434ea78d6fcd9714632f6410987120e6a5dac8cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111789981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2bbe954c5d32e5d2594fb251362aae7d44cc957184d96bcf8d6a32882d283`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5539ac0687305028c3b091d0bd005dd435a7120b1adeed651519755a284087`  
		Last Modified: Tue, 30 Sep 2025 09:19:11 GMT  
		Size: 78.2 MB (78189477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef2b4323b35b04baffb47f2a0dce4b48b005b82cc0de3c4a190b5ea26873a`  
		Last Modified: Tue, 30 Sep 2025 09:19:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06820665efb4162770e24bafe372923c2bb07df762507b5f2c01ea82b1be250`  
		Last Modified: Tue, 30 Sep 2025 09:19:02 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:f100f29fb73ef707a31f32fca0ef4b48feb996f678d4a06c67e1e5e2c8956c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6b9e54d90a46a1a4b11ccc7f8cb58ddedead0044d1d8cc8e0a34d33b8d622`

```dockerfile
```

-	Layers:
	-	`sha256:40cc376b259c0c4a078d0b58a028f300ca0082ed7b67382a1fafb6c01ef2ce01`  
		Last Modified: Wed, 01 Oct 2025 21:19:40 GMT  
		Size: 19.1 KB (19098 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:657d3edd68a65c906ae591fd1a3d089da6612dd697b8898288aec8d8a6ac1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93297601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179329da1a7815cc9e37d5f66b534a417ff28e4afc4565dba050a4426b2a7c52`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89997ec12fbc73cab93ec270f9f6217ad1c36201f98c7ac10ca1d56cd48f75fa`  
		Last Modified: Tue, 30 Sep 2025 09:31:10 GMT  
		Size: 63.5 MB (63458324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08725b35f85e66d1853a06666f987c279cc65cdcf9def2dd3277ed44bfa864f3`  
		Last Modified: Tue, 30 Sep 2025 09:31:04 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9914c3e06a10fc608b5ae547675a47c6f03f8bf05b700ae6baf38bfe616c28`  
		Last Modified: Tue, 30 Sep 2025 09:31:05 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e976e1e6a0a0584d964d85bd4d1b658e25697067e72323e5adec8ed2b2597842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e460bd852b26343edd236905e792573503082e32f52ad8e5fa971b267dd9cca0`

```dockerfile
```

-	Layers:
	-	`sha256:03e3283fe7e981c8719816b768c237efc142716e967326bad41ac96f6dc65c03`  
		Last Modified: Wed, 01 Oct 2025 00:30:19 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:c11cf7d63e01386a3f02cbba27821c6270f8b692d3a0ee84806cf812b9487eec
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

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:c9659dab18a500d9fe04fa785eefc64d24edc2e862bb59084ceee34b38dce496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80509232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2cf69fd1f3fcd8a03b3feccc63efeaeeefad5ccb90260bbe35fa15fe2de63`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482641fcef0c8088913cb713ac90451442ec8de569addab8851373246f0fe29f`  
		Last Modified: Wed, 08 Oct 2025 23:31:54 GMT  
		Size: 76.7 MB (76704725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65912544d120184afcbb1ffd23d1693126dfef25bc88d90974cbefbe1b254df4`  
		Last Modified: Wed, 08 Oct 2025 23:31:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe1e835e84c50d6f9db4c2d94590deeb81cf7ab3d855f3234bd46d9ce4c6f5`  
		Last Modified: Wed, 08 Oct 2025 23:31:40 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:c81fb0c5623e84838532ea464dee82356f2a5f34b72391aec38f6630314a095b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4101277619c6c9054473d726c7e91f76c357ea28000c56bdb380a44193d2f90c`

```dockerfile
```

-	Layers:
	-	`sha256:b39bd93d289b05c0717b67efb0653c0581280531c9664232626794a908bb05ad`  
		Last Modified: Thu, 09 Oct 2025 00:19:32 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:32895706e539e8206106474af679442182babdc28ba6e9628c11c3c4ad643ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62518955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0d48349671c7c80be42e08ecbb37dfb0935824605f204d9c8b2d933dfd2b5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96a0a13dbec284bd8cd345c59d8375d7a837d2b1fd77940ab14c123ae7bbfc9`  
		Last Modified: Wed, 08 Oct 2025 22:12:11 GMT  
		Size: 59.3 MB (59295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b2423e65b9488dad1ba24b9b874fb325d6d88ffb995ab80a23b00564a038c8`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a96bc498d9e4d162d79b72167c6dde22de2a0dd5695ded9638cafa3fb58b4b2`  
		Last Modified: Wed, 08 Oct 2025 22:12:04 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:da78635d73aad180804fc8b230700f4389f337ae1245edbfab53a9e0fa9a412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ad716355c051c3737347007ed90b77d468dece570401ffd7941df02ba575c`

```dockerfile
```

-	Layers:
	-	`sha256:85e849d6e3caf0956144b3822a7b2669e0ad733c6d76c66deb932570858ec90e`  
		Last Modified: Thu, 09 Oct 2025 00:19:35 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:35e2e2be25388c5bda5c91171fd22571cfd80a62fa0a6d1033f918d5ff2cc3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77506872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce0ebfdc5663581b7f629f831661a430d6e82b4525ae7b9b87be517a942527`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6cbd79b4f613e51c0f166692056c8144bbcb4f243f84b4590619bc21a0b072`  
		Last Modified: Thu, 09 Oct 2025 02:39:52 GMT  
		Size: 73.4 MB (73366746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79326203fca5ed4aedf0d71d2ff79336ab5bb671356f694f877f1f6adaa22f14`  
		Last Modified: Wed, 08 Oct 2025 21:47:10 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecce3bc45b8924bb7789a68a8cc79abfbe8faf7f37b2ea9069d9fcb54607e0b`  
		Last Modified: Wed, 08 Oct 2025 21:47:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:97a740ba648cb7e51ecee68ae342ec2b52c9f01e060d1feafb1220f0572ca4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e524b7cb420a4730e4930229517182e0c0a815832c7ffb86a0b7b1231542c67`

```dockerfile
```

-	Layers:
	-	`sha256:4bb0166a0b7691b680dcebd874fb383803abe3fd354b3f732beaf911f8daa68e`  
		Last Modified: Thu, 09 Oct 2025 00:19:39 GMT  
		Size: 18.9 KB (18947 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b4de4c6555d41ce3142fc76516f70de1eae08d4fc1ab832130a134de00879f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82737865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27534bc22899d318c0c1a4dfc1406179ea7c3984e4ccf34390696457c8f6765f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643b7ceed7bcee1c3d59fc18d494ef6a37bd8678404893b1229c369bdc84210a`  
		Last Modified: Wed, 08 Oct 2025 21:41:42 GMT  
		Size: 79.1 MB (79116881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bae575509feeebb714ff2363fa2a8fa1f4c8cc866719191cbd213f1afc6579`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a54a65e140f7edb0a6dddbf380306157d5be82151c8301edadbdcfcd4f162d2`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:16528c0ea97f5c2ee589ce603534b6b802907590277ee04c11cc7793b594f5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2233b2b41bc17a81460516bb93fe762712d93ab9476f8f4bf82bfdb193223c6f`

```dockerfile
```

-	Layers:
	-	`sha256:9fa86eeaebb4e88469136afe59bbc44222e410bfd91aa08affc869b2e131770a`  
		Last Modified: Thu, 09 Oct 2025 00:19:42 GMT  
		Size: 18.8 KB (18827 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:bfb05dc6aa06e1dd936e7ff7c07a4e93ab7a7854e3b02b7c6d8f0fc833ed1d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76639272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da184a45ec589f94e137caa1332b801e609de03627735362300c14b9907525f4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeffbb7c94dcb75dca07f8c37dd42060aaf2af42c122e19a9c159b75ec63870`  
		Last Modified: Thu, 09 Oct 2025 03:39:11 GMT  
		Size: 72.9 MB (72904969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07abff344c3433c1799307c959211f701cdab20eb5f16683c3b8dce4d0cab7b7`  
		Last Modified: Thu, 09 Oct 2025 03:39:03 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0b47abd662b4e4cfaf443ccbf5693bac345b973f4e09d054a3d7b418bd5af`  
		Last Modified: Thu, 09 Oct 2025 03:39:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:47bee8ec48ed360f57235cd70d7ffe22d7d32acc8ba9e9a3ad9d2e1bcce645e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82584094cbda0713e76670be3615a054abb4a64d0b78dce89bc79b3acd35eb86`

```dockerfile
```

-	Layers:
	-	`sha256:2691e5e8553df139393bd8fbd4351de7f140f73f2de776fda9dc2bfea15847d1`  
		Last Modified: Thu, 09 Oct 2025 06:19:31 GMT  
		Size: 18.9 KB (18893 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ec1794f8e9d2ce3a43d4e7a40c048f202ba0b916f0e81d6ef078fe305043aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71290928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f100d551ae21d2db13ebc83234b956478ae94f03d1b82b5062535a1e8ee31d2c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0d17d7d5880eb2320ab71fd37521411789c0b0b141fd671a1cafeb64b11757`  
		Last Modified: Thu, 09 Oct 2025 03:10:10 GMT  
		Size: 67.6 MB (67639628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a597f898d06d096f4ad6afb8109ca6cc4d6a4f3f18ed479fae9d7d3c6906070`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d8ee3c9020de00cfbad575a804b20dc1eb0a46d7026d2f06a99e38909362aa`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:8a460acaba06608ea00cf72a7391f0f91f9ddcfc70163d3c521d852d609819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615cd31422df6224627eb7815825bc3df8c0a4b43c60e38246a3174fbfd9ef4c`

```dockerfile
```

-	Layers:
	-	`sha256:aa184cf214624641b9944315fba469e91f1a21cd156bc8f7176224c266a74a87`  
		Last Modified: Thu, 09 Oct 2025 03:19:30 GMT  
		Size: 18.9 KB (18853 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:478db776da03729215b20dd81277050cdd0464615cf4b45f7a86f4e535bca453
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

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:edbcf0cd549f53684fc336b974b1c3fe89cb9a2af5a5a2f136777a226581e3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69a36386db13b384d7adf8030bd4311732d4338a012187246d7fe640abcef87`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021bd6671d3c11349807a74fa9eed35c5ab7ae0b1861bdbad9e0c1f3bb0836c5`  
		Last Modified: Tue, 30 Sep 2025 21:32:34 GMT  
		Size: 75.3 MB (75320304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283d977df10b07fad39caa773e480b85b2316bb0210df4529286f9e3f64071df`  
		Last Modified: Tue, 30 Sep 2025 20:32:52 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:fdaad8c93b08a3788a9b33f4ad7ea9f826c4629f41078677b7d301d48a4a63d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db71b02b550e84775078b00b1c320ba9a498e132b71f30dea306cc2e8262af21`

```dockerfile
```

-	Layers:
	-	`sha256:fa7091d13984269be7930011aabfc70e936efb08c9c46386147647138e188614`  
		Last Modified: Tue, 30 Sep 2025 21:32:14 GMT  
		Size: 12.7 KB (12692 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a30882f2f37a7f0c60fbc676321e0459df53287e851da20a26afb21e5bd4fe0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75968311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606aaec99eb1f0b5e0f508c8d4be2e4ee5e7d497756758d76fa46bc159c51614`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b53a6933c8cb5576fd491d862f80ae9c4b4b40f9e404254e245cfd5f745416e`  
		Last Modified: Tue, 30 Sep 2025 01:06:27 GMT  
		Size: 52.0 MB (52033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926848c99eb438a02a41f571b7177bee432513f7919ef280589d71bd84cdcd8`  
		Last Modified: Tue, 30 Sep 2025 01:06:24 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:71169cedf935771cd7e0c53ade969c8c4d720d487a19da86f088656405d4fc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2444ba45a8498982ac7273cd3295dd1a4df75adc41da91a5d008b7c11ce2f89`

```dockerfile
```

-	Layers:
	-	`sha256:57d8d64e3d2e1be41e57ac45ca90c81533539687a60caa9892abe362e1918835`  
		Last Modified: Wed, 01 Oct 2025 21:19:21 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a2aac0559b353cb60b49686e387cc2369c4fe84952783f965980c226fdc77207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98404617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda087f571e171269283c9c4e691e2a8d665240031fbd46506953c181f299498`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a9b5f2ef0a48e29a325995aaa014a02ee8e27a2d6b6c7f1eae706c5e6e5a4`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 70.3 MB (70301719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62acb4a8b52242bb4d121dca852e3cdee447dd87cddb494c3ec202454bdee7a`  
		Last Modified: Tue, 30 Sep 2025 00:15:08 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:94e57ecd1d41808eb3bc924d4c61c2571da38d126a5a21a235927117d40e3f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5269aab6856b2cce907b5896eedda8a0baf058f610e832b67fdf302adc2f2b17`

```dockerfile
```

-	Layers:
	-	`sha256:fb18672428481ccd161b086f4a89f40e1684dbc5a7129fa72cca8c9981cdc789`  
		Last Modified: Tue, 30 Sep 2025 12:19:44 GMT  
		Size: 12.8 KB (12784 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:770c31fec1c0d1e8bb18b3f73130aa7d7b9cedbd371f68718c46015db8093d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101009937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7369af1ac997223f89a186307d3cf0ad66d6c7483d96e030e3d2bf70e54178d5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac062943d6dbf85d9967efb33f240d7174233498ecefeae11fc3e752e4b701a6`  
		Last Modified: Tue, 30 Sep 2025 15:11:14 GMT  
		Size: 71.8 MB (71799554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acb1e036848264770a871e40dbc8f57b501eaa6a3973e6d6002bd0469ae1eac`  
		Last Modified: Tue, 30 Sep 2025 01:11:00 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:0540529c49b2c9cf0341f115c4e4de158e14ccd3eeb46eecf643fcd720a151c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612d547d40a94907dee9f043de061252f518a847f289ed29eea07e8b3e42a9f5`

```dockerfile
```

-	Layers:
	-	`sha256:284ab7a9bc5e80ab20f48608dfda7f7e25be01c46c4bd04faa1880a3d4647191`  
		Last Modified: Tue, 30 Sep 2025 15:21:15 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:33614a26f6cf8caaa6f149d237e8dd550625d372a6e2b55440dec6460c6c45de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105448843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ede35632676bf8b6077af4627923c4ac550c5ad7f3aaddf472ff1b8afff799`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37332b11d69c63d3807d704d5c4810b1837ad185ea9efd87f1cf803b9db772a`  
		Last Modified: Tue, 30 Sep 2025 02:23:32 GMT  
		Size: 73.4 MB (73379392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6c6b5317a767b461b18bc3a77bda753e29cde5c9470fcf71a103464c668137`  
		Last Modified: Tue, 30 Sep 2025 02:23:17 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:393d1b4f9ce8a87d7da85c90cb4e5de595ea7ebdb070e6289542af8d34986bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3f98654479446cb0b375bc94b3731300338118952d9a3f27113fa8c1b70aa0`

```dockerfile
```

-	Layers:
	-	`sha256:d644c1c9995c7a7a09c28e819ff1ae53125e36d54a241916937b065617c785c2`  
		Last Modified: Wed, 01 Oct 2025 21:19:28 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:dd816940571162d6ee1e989f9c9952bae13cf153bcea3e5e5fa9654f6d81d3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81335071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e39171b878b614da5e82f45d179d7fde3eb76ff4017254c2e737115caa4513f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e5a4571b8763222bc9df6252308856a003d945316511f14da7b7c397cbbcfa`  
		Last Modified: Wed, 01 Oct 2025 00:30:47 GMT  
		Size: 54.4 MB (54449997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d87403c37cdba5b295b8dd02cb3c9a68249c1ca86a8658955712801fc9edd1`  
		Last Modified: Tue, 30 Sep 2025 03:57:19 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:67fbf88ebd64cd482b3ba39fb4aa2617c9d8e90112d0a7220dc93a23b0ca31d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382986cfda5f76f4c8b9ff355bf4142f88e49fc7f32b7e0462c284caae2ca060`

```dockerfile
```

-	Layers:
	-	`sha256:7c98189558027159262d622199a4fa7eed6df5488f9ea32417c53665e9081ff5`  
		Last Modified: Wed, 01 Oct 2025 00:30:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json
