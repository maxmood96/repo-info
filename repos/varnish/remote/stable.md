## `varnish:stable`

```console
$ docker pull varnish@sha256:6d3c884e37c3b16c725662aa5681099b77df91a52a75c0883d14094960a03b5e
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
$ docker pull varnish@sha256:387797e5486b73cb88648a546e0ef4c32f0b3c49a1f364a756847bbfdda4cc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103548929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7c9c8115cab8369fe9464b715ae9e0ec4d0f930100517b7b862b632e4c693a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:46:12 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 29 Dec 2025 23:46:12 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 29 Dec 2025 23:46:12 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 29 Dec 2025 23:46:12 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Dec 2025 23:46:12 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 29 Dec 2025 23:46:12 GMT
WORKDIR /etc/varnish
# Mon, 29 Dec 2025 23:46:12 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:46:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Dec 2025 23:46:12 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 29 Dec 2025 23:46:12 GMT
CMD []
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123bf779f072036858f5bc0a00843ccf87807893d214ea9d9314115d2e3c281`  
		Last Modified: Mon, 29 Dec 2025 23:46:38 GMT  
		Size: 75.3 MB (75319751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ad7c5909db626385b355eb9effed57bf7a3c968c5d5b7f886017c2a9407f0d`  
		Last Modified: Mon, 29 Dec 2025 23:46:30 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:33896b463411b362e8edbb660a6934138aa0973c3538925e71e7f07685c44c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3db43a1390fbd371723eee295bd4f137035edd8789d5774429f4878d47be22`

```dockerfile
```

-	Layers:
	-	`sha256:a6b0e6f8b999d3ed6428eb6920f591f7c921a4f5a252129de0c59033051a7e26`  
		Last Modified: Tue, 30 Dec 2025 04:20:10 GMT  
		Size: 12.7 KB (12657 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7fbe2694a77fd18b4472fe95c3d1d9ebde900a116f5eb4f6dc2bfa97994ba941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75969344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8901e7febfb6ff2bfe22dab792f3b3547c148210430eb97bb31479691fdead`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:34:18 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 30 Dec 2025 00:34:18 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 30 Dec 2025 00:34:18 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 30 Dec 2025 00:34:18 GMT
ENV VARNISH_SIZE=100M
# Tue, 30 Dec 2025 00:34:18 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 30 Dec 2025 00:34:18 GMT
WORKDIR /etc/varnish
# Tue, 30 Dec 2025 00:34:18 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:34:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 30 Dec 2025 00:34:18 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 30 Dec 2025 00:34:18 GMT
CMD []
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0be732571f048d855f4d0f42b257bc3ff63c1fc684703ee0f4be362ef76043e`  
		Last Modified: Tue, 30 Dec 2025 00:34:39 GMT  
		Size: 52.0 MB (52034537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00454f9c904f13da819369f3ef8ed1ce83a936cc3cc121cd2a6c2b418e2d36f3`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:add0b585b6af09f32cc411701e0e0fbcfe31c9dca60d958b1bd602f1a56b592c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986a988c6ee0aff3dce928fb6605ec5765212459d0109ea4232acb69876f2ea5`

```dockerfile
```

-	Layers:
	-	`sha256:3b96ef6b87597fa60fac8ab5ef30f36b559b3ebd33e592be9f3609e3be970711`  
		Last Modified: Tue, 30 Dec 2025 04:20:13 GMT  
		Size: 12.7 KB (12728 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7fb96a049da0f1b3fdb0c2fc90c8477e4a4fa60bfa6eae0b5e5815c7b36f2e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98404442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b65919b9f86c32ef81a4cfbd86471f327c758843660a45916fd515237a6a82`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:46:18 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 29 Dec 2025 23:46:18 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 29 Dec 2025 23:46:18 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 29 Dec 2025 23:46:18 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Dec 2025 23:46:18 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 29 Dec 2025 23:46:18 GMT
WORKDIR /etc/varnish
# Mon, 29 Dec 2025 23:46:18 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:46:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Dec 2025 23:46:18 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 29 Dec 2025 23:46:18 GMT
CMD []
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1edb7a018da957882b2c09b0d4c93d44c7c0cd17f172f5601934412e70af5f`  
		Last Modified: Mon, 29 Dec 2025 23:46:42 GMT  
		Size: 70.3 MB (70301480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21635f1467fe56f21d5246f2e70ead054badaf74ccb7b3cde3e6918d019b8b43`  
		Last Modified: Mon, 29 Dec 2025 23:46:36 GMT  
		Size: 720.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:1ec45fb244f8293884beffd53b9020ed4402ffb5bf217708464d5b6e33c08960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f833a46b7bc68924a7c8023073698ffef50c0179bdff8c60c59457323e561b4`

```dockerfile
```

-	Layers:
	-	`sha256:2e3718771d2567a9a576d1cc24c358658f0767aaf8f38d1769b695a4558c1084`  
		Last Modified: Tue, 30 Dec 2025 04:20:16 GMT  
		Size: 12.7 KB (12748 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:dfb3526fa31563dce5b773e40f0bc27d481c892feb10ab47dffc411ada72cc21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101009987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4842512b2342cb0880f1a6c50a4125bb3d9dd5a86a6fa2730607a3861fe6a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:48:53 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 29 Dec 2025 23:48:53 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 29 Dec 2025 23:48:53 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 29 Dec 2025 23:48:53 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Dec 2025 23:48:53 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 29 Dec 2025 23:48:54 GMT
WORKDIR /etc/varnish
# Mon, 29 Dec 2025 23:48:54 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:48:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Dec 2025 23:48:54 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 29 Dec 2025 23:48:54 GMT
CMD []
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bbd3cc1b990dcc7ffa781503171fa3bcbd20ec179f5f726228b574e2cb25b3`  
		Last Modified: Mon, 29 Dec 2025 23:49:16 GMT  
		Size: 71.8 MB (71799462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1dc3c526e384ce0ffacdb39c12e22bcd80a25a3128651d5419988787cdec4`  
		Last Modified: Mon, 29 Dec 2025 23:49:10 GMT  
		Size: 720.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:1b4a87ba979fb96296c580dfb4a20f621be4e8fec602cbde40e0069d137c10f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb703446c73c8b70f4c3d671d65e6f04e7e4ec7e6058590281398484d78735eb`

```dockerfile
```

-	Layers:
	-	`sha256:751abce7fdbda7d8654542c49f0d4d0c7fc32e432f6281b3a6619676801d6cbe`  
		Last Modified: Tue, 30 Dec 2025 04:21:12 GMT  
		Size: 12.6 KB (12630 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:5d2de19e743322524eec47d432761c4342ef4b367aacd592e74055fec88f320f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105449249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2847f177ec664448454b2eefc4e25bec8403218990c315de182df0511b99ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 03:18:46 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 30 Dec 2025 03:18:46 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 30 Dec 2025 03:18:46 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 30 Dec 2025 03:18:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 30 Dec 2025 03:18:46 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 30 Dec 2025 03:18:47 GMT
WORKDIR /etc/varnish
# Tue, 30 Dec 2025 03:18:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 03:18:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 30 Dec 2025 03:18:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 30 Dec 2025 03:18:48 GMT
CMD []
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183351a60adf03d8603550e3d1f9912edb132148ea112472b4042d2c2b3ffdf4`  
		Last Modified: Tue, 30 Dec 2025 03:19:22 GMT  
		Size: 73.4 MB (73379651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cbf98e8faba0947e618de85a0d2b6039649aabd78ac195a7b41eb85685b2bd`  
		Last Modified: Tue, 30 Dec 2025 03:19:17 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:fae8d74d073220489c7275548f41abfcef31e8936ea98276ce3b5f12eef565fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda3ac0ab099e280d0b86a6e5d4a169ea1978223e8aa3774cc7a621e87648d0e`

```dockerfile
```

-	Layers:
	-	`sha256:b3c7a9ff0461af33250f39b33e524c58fb26498f2fb17c292ec2816197de16e8`  
		Last Modified: Tue, 30 Dec 2025 04:21:15 GMT  
		Size: 12.7 KB (12695 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:6fc4b5f3d3501f134f2f683207dc80530b0fb88d53623e93dd10248feda02040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81335090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e943109fb5600dc0b189e69e8dee21ccaf194d6d43466140b4df96effb078a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:42:35 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 30 Dec 2025 00:42:35 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 30 Dec 2025 00:42:35 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 30 Dec 2025 00:42:35 GMT
ENV VARNISH_SIZE=100M
# Tue, 30 Dec 2025 00:42:35 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 30 Dec 2025 00:42:35 GMT
WORKDIR /etc/varnish
# Tue, 30 Dec 2025 00:42:35 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:42:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 30 Dec 2025 00:42:35 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 30 Dec 2025 00:42:35 GMT
CMD []
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175ebc2cbc672383ff5428f41c1a3bad808dfa991a252b330cf16bb1d92f4d38`  
		Last Modified: Tue, 30 Dec 2025 00:43:03 GMT  
		Size: 54.4 MB (54449938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6b39b54e3b0e1803879f1577a03549876d16249bcb0e61c443dfad23fe963`  
		Last Modified: Tue, 30 Dec 2025 00:42:55 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:ccbc42000cc0b96d9115b00bc56a6a7e151e93188add903c854d79e573bd1372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e759bda94aacd64b3f9276fa177de55fb6ae476d6fe9b6cd79683076bcb6570`

```dockerfile
```

-	Layers:
	-	`sha256:32e540e7e7aaf642caa3e7ad090b55e40eafad91c0dee840f3f1d5edd1551f40`  
		Last Modified: Tue, 30 Dec 2025 01:20:11 GMT  
		Size: 12.7 KB (12656 bytes)  
		MIME: application/vnd.in-toto+json
