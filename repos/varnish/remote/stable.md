## `varnish:stable`

```console
$ docker pull varnish@sha256:2369139db49a955bcae5aacede0e5d103da14cf6c1411403bb6abe74ffc44ae5
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
$ docker pull varnish@sha256:0750bef310a46e5cdd9f5526e3df4479c613b48507c7aa1b97c653c3e795a20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127722433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba9a8008e6a81732d63adcbf61a4a95e92f3f16ed2a6d742249d317515bbe9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 25 Dec 2024 01:40:21 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 25 Dec 2024 01:40:21 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 25 Dec 2024 01:40:21 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 25 Dec 2024 01:40:21 GMT
ENV VARNISH_SIZE=100M
# Wed, 25 Dec 2024 01:40:21 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
WORKDIR /etc/varnish
# Wed, 25 Dec 2024 01:40:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 25 Dec 2024 01:40:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 25 Dec 2024 01:40:21 GMT
CMD []
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49585684dd2a27a68cf1ab01d4e3c7cdfab92a526c20a9fa5ca0ef1adea6a066`  
		Last Modified: Thu, 20 Mar 2025 21:09:18 GMT  
		Size: 99.5 MB (99516814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f433ad6794a0596a719222678004817ceb59d5158261fbf02678f5850329b1b`  
		Last Modified: Thu, 20 Mar 2025 21:09:16 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:2ce8cbf32acad6e6a10a6aef853be8e6812e830171f86d32dddd0c613d6e132f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e60f5c4a709e5c6259330cfb6bb8e399114e12cac5ce349fe7910abc7550d`

```dockerfile
```

-	Layers:
	-	`sha256:004fa04edb88de7f5b5b99811416ce02278c94169bcbf232761e90f74ed0351c`  
		Last Modified: Thu, 20 Mar 2025 21:09:16 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:cd530d59f3c8a2f446f100f2369ab44d0e4240d643e2523a2de78858400a3f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98266329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b662085f9f4e7e1f59444b7d07dcda97f6d0d68983b2fd78f7d3f3ddc48b7f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 25 Dec 2024 01:40:21 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 25 Dec 2024 01:40:21 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 25 Dec 2024 01:40:21 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 25 Dec 2024 01:40:21 GMT
ENV VARNISH_SIZE=100M
# Wed, 25 Dec 2024 01:40:21 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
WORKDIR /etc/varnish
# Wed, 25 Dec 2024 01:40:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 25 Dec 2024 01:40:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 25 Dec 2024 01:40:21 GMT
CMD []
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab3a7fc3dff82f10a3432ce14ef93a69bc7aa5e79e4b1a7dfa4030237b83675`  
		Last Modified: Thu, 20 Mar 2025 20:58:03 GMT  
		Size: 74.4 MB (74350487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02362b1d89b66db448f76ab7b47e727846379452be28b7709ab8b682bcf3ad2`  
		Last Modified: Thu, 20 Mar 2025 20:57:58 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:acf231e4f35b89deed7b90f2714fdad1830564dfe9307a5c3a1835130fb566ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ddb20bd58dcd5483b4bbcdaeeabe2af9473e37d293b6e2f81f923f3afc1375`

```dockerfile
```

-	Layers:
	-	`sha256:047a21c6a7bf9ebccaba7106d6c4f4c070e5c6477eb6a3311e7ae6855c27e132`  
		Last Modified: Thu, 20 Mar 2025 20:57:57 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cfc4a9fcd45769a8b0d6ba4d449d493a5547a4c3c0019cbbc138d55884cc1d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122338440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c487c2e01704082b9b34252f16e74effc13194c1e48381a1de386272c3e22b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 25 Dec 2024 01:40:21 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 25 Dec 2024 01:40:21 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 25 Dec 2024 01:40:21 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 25 Dec 2024 01:40:21 GMT
ENV VARNISH_SIZE=100M
# Wed, 25 Dec 2024 01:40:21 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
WORKDIR /etc/varnish
# Wed, 25 Dec 2024 01:40:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 25 Dec 2024 01:40:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 25 Dec 2024 01:40:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9418311501fc549327b6a7e917f9929b22fe419c56f6e69cce068b5324c73240`  
		Last Modified: Thu, 20 Mar 2025 20:56:53 GMT  
		Size: 94.3 MB (94293648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77258c76e45b639a620795861b6a690bdec61398a4cf9f17a78bf8756fe4094`  
		Last Modified: Thu, 20 Mar 2025 20:56:50 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:552c7fc0f0fc9985c1934a35557f695cc7d92430f8ba9e149233b1176bb44af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5204d72c4de70924bf251929855d6da3635af55f0ecaaab07da14b9e5e402f6`

```dockerfile
```

-	Layers:
	-	`sha256:d6a63a688d4b98726a83477224af0042ddc55035c996598f45f2fc239179c13e`  
		Last Modified: Thu, 20 Mar 2025 20:56:50 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:5cd6bd20631a0d7b06a3a3d2a30f833fd80c596628291a4264358d8718863842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124884363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61099fa9a76b99afd9b39b0b929690ac014cbd618fe4ad522aefaf5173b8da19`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 25 Dec 2024 01:40:21 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 25 Dec 2024 01:40:21 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 25 Dec 2024 01:40:21 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 25 Dec 2024 01:40:21 GMT
ENV VARNISH_SIZE=100M
# Wed, 25 Dec 2024 01:40:21 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
WORKDIR /etc/varnish
# Wed, 25 Dec 2024 01:40:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 25 Dec 2024 01:40:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 25 Dec 2024 01:40:21 GMT
CMD []
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a727a04eddaa6f849bdfe564c62a827cc3905e8293abf6c3a508a93795c6068c`  
		Last Modified: Thu, 20 Mar 2025 20:49:44 GMT  
		Size: 95.7 MB (95694081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e38b574148d8bd3256eda1853d184360bc68074294adaccd63042dcbd780ca`  
		Last Modified: Thu, 20 Mar 2025 20:49:40 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:12ed0af52ec967187af44b20909d508db1f37dbfcf823cf9c2bb1bbe0b468729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7765e0f66046bc47f7a00ace744db4f7280ac9172c7aa73be387b129513340e7`

```dockerfile
```

-	Layers:
	-	`sha256:b6e9702f393a802fff0187fd31ad54263ab364ac51c4402817dc6cbeb3e42e98`  
		Last Modified: Thu, 20 Mar 2025 20:49:40 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:57e4551b829c28bc4bc4b8807a454771ffbd97ab312ed0a8ec3e135b7e132837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130390278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08387d9d3ba09c2d9884dc359f86fd76d615dbe5c72dd8cfef5cf365b4793993`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 25 Dec 2024 01:40:21 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 25 Dec 2024 01:40:21 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 25 Dec 2024 01:40:21 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 25 Dec 2024 01:40:21 GMT
ENV VARNISH_SIZE=100M
# Wed, 25 Dec 2024 01:40:21 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
WORKDIR /etc/varnish
# Wed, 25 Dec 2024 01:40:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 25 Dec 2024 01:40:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 25 Dec 2024 01:40:21 GMT
CMD []
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e841eb5f8fb85dd6fea1194c5b547259ca635916cbbb787b8b2d34f7153205`  
		Last Modified: Thu, 20 Mar 2025 21:03:29 GMT  
		Size: 98.3 MB (98341709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52e749bcee501fc8ebe9788946e9de70f0b92074c08233f518fe918c33923b9`  
		Last Modified: Thu, 20 Mar 2025 21:03:26 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:1cdc64df1df3723a6e20406f98c92bb89b93808b9ec6be055b981383d8679e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d32fa135c288c9e292f4e47beef620144f5b309aa2a5894f68c3752b908079`

```dockerfile
```

-	Layers:
	-	`sha256:3f75daa2dfd4400d5361c6c3dd9f60f90fec126db00115df214dd2d1f8ed5d6f`  
		Last Modified: Thu, 20 Mar 2025 21:03:26 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:d7214994f5febcf15a38600748a1b6fdc434dcbe9d0cab6eab45c27a3055399e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105600938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398324f75fdf43d53290c0c794da1cfd0a9f92cd52eac232c1676184fb40d6a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 25 Dec 2024 01:40:21 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 25 Dec 2024 01:40:21 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 25 Dec 2024 01:40:21 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 25 Dec 2024 01:40:21 GMT
ENV VARNISH_SIZE=100M
# Wed, 25 Dec 2024 01:40:21 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
WORKDIR /etc/varnish
# Wed, 25 Dec 2024 01:40:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 25 Dec 2024 01:40:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 25 Dec 2024 01:40:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 25 Dec 2024 01:40:21 GMT
CMD []
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b46c2c09e054097bf95d9499de5addc8be0b95d37b8d8ce6bb8292ffeb1a707`  
		Last Modified: Thu, 20 Mar 2025 20:58:16 GMT  
		Size: 78.7 MB (78739125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2933b5d8d9b2346748232632abd44261328200e164492fcae87c42f31ac43dc6`  
		Last Modified: Thu, 20 Mar 2025 20:58:15 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:6498f9f1af68249c14548d6a1c0b9526238a868fe4ca2e391d098dadc785b429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df54e502fe2046d1c8c6d469c26823b0326f49fd6f6f91b1e22eca24acc0a9f`

```dockerfile
```

-	Layers:
	-	`sha256:a84b8cb2a408beedece7aad50b9612f97e8d9122194aaef0fd7ead5699aa346d`  
		Last Modified: Thu, 20 Mar 2025 20:58:15 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json
