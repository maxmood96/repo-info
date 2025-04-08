## `varnish:stable`

```console
$ docker pull varnish@sha256:09e38dd951078930e1066b7ec8724e9a005d523be57b16ee2ae9d0f95b3dcc39
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
$ docker pull varnish@sha256:87142cba7b80ce2b2666b2bc4ee115c5612d72851b377ecbfd28089e9011b5e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3250c8c9f9c9583930f6b9ace939e69b4f589f08c93f33317915e197111677f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55018f8f57e61991c1e17bf41539f5c79578b9f28126540ca2b703c53ec1bf9`  
		Last Modified: Tue, 08 Apr 2025 01:25:40 GMT  
		Size: 99.5 MB (99516877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a379e2dd06d6626a0c7c1cdb9e38ab9d46f7dbc64425efce0aac86cbeb2e4a4d`  
		Last Modified: Tue, 08 Apr 2025 01:25:36 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:284849056ad961dc7c3bc4540f5eda16e78ad7f7d183b48a3c9c17e7bc50b0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7d8383467e2ab13d666a9ad28584674426cc6ef2279c96972f8e68b4d92660`

```dockerfile
```

-	Layers:
	-	`sha256:397f7750d063c766fe58b9098a9608549d757f64da8260c1da3b76b65066abc0`  
		Last Modified: Tue, 08 Apr 2025 01:25:36 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:bfe1f94479d9a163088bd9f09223bc011f7b8572d2ed5d3e00ef9889984b07d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98289762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eba2773714bc0fc4928aa8f43dedad2346cdc98b1493072d166deddd77ed7d6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee1caaf8bc5b8a613c859586009ad668377ede37c5632143c49ef3b8850c446`  
		Last Modified: Tue, 08 Apr 2025 07:37:20 GMT  
		Size: 74.4 MB (74351140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba80c750b9124c98d7fcb9c6ca360aff4227a99c5b14f041b93af1b821598f9`  
		Last Modified: Tue, 08 Apr 2025 07:37:18 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:b36139337acefaf8940122cca74b9debbd433d955b5a5d36633f6f75c1ee5f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3b228642be6b959b5cd48bca1b49b91172b223ead51ad1f838e2eca85d64ad`

```dockerfile
```

-	Layers:
	-	`sha256:697301eefa40cd8dd30660110d2384da31b3b7181e4d41465374f0e61bdb4392`  
		Last Modified: Tue, 08 Apr 2025 07:37:18 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:77d94016814b2bd86dcda9cab7b71aa796ee8c87434c48690f8eb533073ed735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122360728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01d4c07160ba382814e59f639660c9bdab5746c84ee2c0b4a4711118e47170b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529904ef57b119339d38e865b986f984cf01aea0519131e32f7771dd472c766e`  
		Last Modified: Tue, 08 Apr 2025 06:02:39 GMT  
		Size: 94.3 MB (94293652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34de9fe961c9c514a6b00f704a2d650937171ff7c67e343dde194a45a858b237`  
		Last Modified: Tue, 08 Apr 2025 06:02:36 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:3abcedc36d53c211fe74906cf2ebbf508474f2394c1550001569c355988ca27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e316aa8f0343f7cc4b6fc913758904844f6da3a31af83cc83351b98a4f5213`

```dockerfile
```

-	Layers:
	-	`sha256:0c0b7b1d6988bbbf911e07f4d8444fe9735840806ec315091ee59896032f16fb`  
		Last Modified: Tue, 08 Apr 2025 06:02:36 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:ffbd0fa7fe88f18e04a16094e335b4b89cf5fc0c116fe395d0060f0a3402409f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124906093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889dbfe640368242c1b51747d80637a99ccc0b5ec90f0339d127c92b2a2f9f3a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252937c76cfbce98ded9efe5902c68acf2bb501fa9bdcd6f8b2048fcfb046a6e`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 95.7 MB (95694606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed0b9427b0c53681700c18b067c3d2d146be9a4575aca6169d3a5cff3c06fcd`  
		Last Modified: Tue, 08 Apr 2025 01:25:25 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:5f21d7e437edce0ee634902386fb97219069f332b1209baffb492eed3d74479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212193e7b570dc672b666a49289c5f8259d9d239570ad8eface5f164d447ee1e`

```dockerfile
```

-	Layers:
	-	`sha256:93406ce33cedf3647183428349657cd8ea301c44bc3f0bf85e15f812b35004c0`  
		Last Modified: Tue, 08 Apr 2025 01:25:25 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:3e67febebc8d79186892fa48baf34951cb725ab6d9515e513858252d80e1691f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130410959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa81c0078495e0e4869211c2040570bf02e942e01c175075d91f43c7217b006`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3cdc3625c03e3f33adc490d4c94cd8bc287d40b286643f0b9b9d869bdd5feb`  
		Last Modified: Tue, 08 Apr 2025 04:29:04 GMT  
		Size: 98.3 MB (98341973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2752f5cbc281b7fb3545a51650b21910716831e1f6a71cfa5cb8f01dfb360a82`  
		Last Modified: Tue, 08 Apr 2025 04:29:01 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:15ee27e6d17405a3274f13891f902175cb5642f0427f99ed15e3714a08277010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef6aa6b2505096e21b5f231c88566d2e3a016207009cd417b4b7c6891944fcc`

```dockerfile
```

-	Layers:
	-	`sha256:0fa14cb58be5f783b5d4304ef3a433d966eb9954503f2daec5c7ec52351e2424`  
		Last Modified: Tue, 08 Apr 2025 04:29:01 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:729ee1ddf0330d1ccbbe6d0883a2fa9bd461527fa9cc15b458e61ac19c7e5095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105624811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17556060b8c34d46e1d017864b6ccf0545b72d0649d95ca7c700325a33dad50`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7152a8a2bea8575397ef2d22e25d90720138159d9b7cb67c28a7d24cb5bc4be4`  
		Last Modified: Tue, 08 Apr 2025 03:43:28 GMT  
		Size: 78.7 MB (78739449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7023049dc1e444a83030dab0ee522be24d348108f270ef03037cf635dbd07abc`  
		Last Modified: Tue, 08 Apr 2025 03:43:26 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:3be20ca2b93c1e09eeb132d990bbfe09ff2f34277398ab3fafc3ce10d99dd4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a27307f0947a12ea81ca894d8934aa89383dab30481bfc62dea20a07ef54adf`

```dockerfile
```

-	Layers:
	-	`sha256:fc6457c86a2923028225e8cd0a7a8a5e66858804a8a071a2dc985affb924bacd`  
		Last Modified: Tue, 08 Apr 2025 03:43:26 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json
