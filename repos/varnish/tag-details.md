<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.13`](#varnish6013)
-	[`varnish:7`](#varnish7)
-	[`varnish:7-alpine`](#varnish7-alpine)
-	[`varnish:7.6`](#varnish76)
-	[`varnish:7.6-alpine`](#varnish76-alpine)
-	[`varnish:7.6.1`](#varnish761)
-	[`varnish:7.6.1-alpine`](#varnish761-alpine)
-	[`varnish:7.7`](#varnish77)
-	[`varnish:7.7-alpine`](#varnish77-alpine)
-	[`varnish:7.7.0`](#varnish770)
-	[`varnish:7.7.0-alpine`](#varnish770-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:f1627a662a4bbb9fc4759202d15162c4a09394230001332dc7b07c5819564314
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
$ docker pull varnish@sha256:ab303565b5539b30566a7b1ad3ebbd005919e85cd486e2e91cb9e942b0906183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545aeccb6abdaf1c10e6010b2922282ac2ad02aa023e16a78a387a9992acd8e7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67648ea82312889df780c03818e66dbda6438f92c80dd7fc872a0edb2ad4e2b`  
		Last Modified: Mon, 28 Apr 2025 21:56:44 GMT  
		Size: 99.5 MB (99515839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dfb8e6b2be6e67c850dc82909d9bfd382718debc0f57a2bff5cb54db58ec9c`  
		Last Modified: Mon, 28 Apr 2025 21:56:40 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:9789645accfe58d663426ad28d1e7d3c81a361d751e869ec31c0d95409ca0b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a904c1a9fd65616e3c7d77ea138356595ba10f715ad084c4a7dce111410cf`

```dockerfile
```

-	Layers:
	-	`sha256:06d28f6084e4496b4f9afaa24aa6e86b3693e1b692552008bbed6912246ac1a0`  
		Last Modified: Mon, 28 Apr 2025 21:56:40 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e05a7d308f600d12c7ca20d67e5829b18b9dc288ec5145730a4242a01ac08f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98288920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5e25f6e59a37a4c69ad5ec874404bd339d6c974c930372b2bd6c61da597e03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afd1e156989368f6e666d38cbcbbddee98d6d589cfab5f656736802bd30d620`  
		Last Modified: Tue, 29 Apr 2025 03:36:23 GMT  
		Size: 74.4 MB (74350094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cc51571a88822dfed8e9892fc6d4a241ceb58cdbdbf185ca8c55f85a7ae48a`  
		Last Modified: Tue, 29 Apr 2025 03:36:21 GMT  
		Size: 720.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:4749c6b8b2d1452c7b84c704abe9f8a3da7f117f1c74607ee09a5b8693e044f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8028707394edfe4d3367ee99486252c3c8ba08c629a6ce3d5be37f859fc735`

```dockerfile
```

-	Layers:
	-	`sha256:30e1cdce869e12ed2dec7c2bab241172b95b06e79c31636ede419b0c9ce35c45`  
		Last Modified: Tue, 29 Apr 2025 03:36:21 GMT  
		Size: 12.7 KB (12732 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ea5690ea35f34ee6c52a90abacbe55ef701bb020e032cfe3a4a017ed4c24941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122359056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b15a3433566c27a95d2fb5d227db18611a58089e00f29cc2a20bf3607ec2e67`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f07bf5498cc53e332bcd52e9c936f3f8c2dacca688722ffc4975b72a0c8a39f`  
		Last Modified: Tue, 29 Apr 2025 01:46:18 GMT  
		Size: 94.3 MB (94291679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfade164f990e3d97229ec2e3b14ded6cd5a50463bb71dae262c06d022ee006`  
		Last Modified: Tue, 29 Apr 2025 01:46:15 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:fec29a8db8167835c3d33c13a53adb187be8ea1137e6437ae8cb7a02670e3d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0add89bfc80390c60bae6a10e97291fa9c4670e89dba05fca30a38e0b906263e`

```dockerfile
```

-	Layers:
	-	`sha256:709bb17f371f9cd6d69c1228e0c6c31cc07e4cf35023cac9a99f4c380ae40334`  
		Last Modified: Tue, 29 Apr 2025 01:46:15 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:baed0f4c518b3031447533c5124da57eef5fb94d48ff34121fbb13353a31a468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124905026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10a158cab887e28dc0310795e865268ef6fab3afa24c4736e534c5511c9bcc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c721a5f1a0287cb31914178d641a48fa6274d52b08210daa2d85721fb41fd546`  
		Last Modified: Mon, 28 Apr 2025 21:54:50 GMT  
		Size: 95.7 MB (95693406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9cb400d85d47cc31734b9480164e0fba4cd9204cdc79694d370b894edb293c`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:c14c4e1400c264fb990b93d9125c09324cb6644dfb9c36cef4e8db41f8227627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c14ae74490207909574666aff7d17fa462f1c628ecd4a652aa619ce851273b0`

```dockerfile
```

-	Layers:
	-	`sha256:6377d9af43befec53fe4750bbebf4a1b9af0a7dbc30b6c9fe8b5649be6a94ab3`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:2ab2742df42e389b2d99b9b98f5d0f204cd5b2815db1d6ca1650f4b455f0612e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130405865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62af1c76c0e8c751881da24bbc76d605b15bfd206b20210b19c7f53737347323`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f1df676d0d3abc4949bfa1dea6269425b20479a4c559d02450410f90cd7f49`  
		Last Modified: Tue, 29 Apr 2025 00:37:38 GMT  
		Size: 98.3 MB (98336669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ed85d7bbb179a43d80cde46090f4332590ab823c91852bd65014a4918c9a67`  
		Last Modified: Tue, 29 Apr 2025 00:37:35 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:fdf5528c67d68405073265decbd118edaf02082ced8c7eefdbc36d7fee9f306d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63c1819b6d2fd1c6160178365c3036888a57785713559bc742dd2fe94c9d8b6`

```dockerfile
```

-	Layers:
	-	`sha256:d34991ca2d68b135ab293a3bf02619ec2939d20786a7f44f725cd251b448561c`  
		Last Modified: Tue, 29 Apr 2025 00:37:35 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:7828527c1d0af8f5746ee8a3a008886eb1c022ac7740f333e730654c7dec6335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241cc916ed898550243ebba83f6e9b75ccafa64071888671514deccace37cc3d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be33dfb4c49615e8253f2ebdbbedfbabd730fd663917126ea31c212a55796a0d`  
		Last Modified: Tue, 29 Apr 2025 00:00:47 GMT  
		Size: 78.7 MB (78743483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7559210d805dd5af9d8a51a6b402e5cca6457dbd86b11500e5e0bfb120ff7204`  
		Last Modified: Tue, 29 Apr 2025 00:00:46 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:56e40c2e20a892c4d5bb11fab3f28806328e2c40dc20a84193b7020992309cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395ef4d628ed77d9861592b9ebbf10acc9001c96b583f74f6da217bf41dc519a`

```dockerfile
```

-	Layers:
	-	`sha256:396878abb84adc7edba33dd84d36dd0cd0abcd7a097e67e6fa7f5353933fe50e`  
		Last Modified: Tue, 29 Apr 2025 00:00:46 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.13`

```console
$ docker pull varnish@sha256:f1627a662a4bbb9fc4759202d15162c4a09394230001332dc7b07c5819564314
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

### `varnish:6.0.13` - linux; amd64

```console
$ docker pull varnish@sha256:ab303565b5539b30566a7b1ad3ebbd005919e85cd486e2e91cb9e942b0906183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545aeccb6abdaf1c10e6010b2922282ac2ad02aa023e16a78a387a9992acd8e7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67648ea82312889df780c03818e66dbda6438f92c80dd7fc872a0edb2ad4e2b`  
		Last Modified: Mon, 28 Apr 2025 21:56:44 GMT  
		Size: 99.5 MB (99515839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dfb8e6b2be6e67c850dc82909d9bfd382718debc0f57a2bff5cb54db58ec9c`  
		Last Modified: Mon, 28 Apr 2025 21:56:40 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:9789645accfe58d663426ad28d1e7d3c81a361d751e869ec31c0d95409ca0b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a904c1a9fd65616e3c7d77ea138356595ba10f715ad084c4a7dce111410cf`

```dockerfile
```

-	Layers:
	-	`sha256:06d28f6084e4496b4f9afaa24aa6e86b3693e1b692552008bbed6912246ac1a0`  
		Last Modified: Mon, 28 Apr 2025 21:56:40 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e05a7d308f600d12c7ca20d67e5829b18b9dc288ec5145730a4242a01ac08f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98288920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5e25f6e59a37a4c69ad5ec874404bd339d6c974c930372b2bd6c61da597e03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afd1e156989368f6e666d38cbcbbddee98d6d589cfab5f656736802bd30d620`  
		Last Modified: Tue, 29 Apr 2025 03:36:23 GMT  
		Size: 74.4 MB (74350094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cc51571a88822dfed8e9892fc6d4a241ceb58cdbdbf185ca8c55f85a7ae48a`  
		Last Modified: Tue, 29 Apr 2025 03:36:21 GMT  
		Size: 720.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:4749c6b8b2d1452c7b84c704abe9f8a3da7f117f1c74607ee09a5b8693e044f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8028707394edfe4d3367ee99486252c3c8ba08c629a6ce3d5be37f859fc735`

```dockerfile
```

-	Layers:
	-	`sha256:30e1cdce869e12ed2dec7c2bab241172b95b06e79c31636ede419b0c9ce35c45`  
		Last Modified: Tue, 29 Apr 2025 03:36:21 GMT  
		Size: 12.7 KB (12732 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ea5690ea35f34ee6c52a90abacbe55ef701bb020e032cfe3a4a017ed4c24941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122359056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b15a3433566c27a95d2fb5d227db18611a58089e00f29cc2a20bf3607ec2e67`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f07bf5498cc53e332bcd52e9c936f3f8c2dacca688722ffc4975b72a0c8a39f`  
		Last Modified: Tue, 29 Apr 2025 01:46:18 GMT  
		Size: 94.3 MB (94291679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfade164f990e3d97229ec2e3b14ded6cd5a50463bb71dae262c06d022ee006`  
		Last Modified: Tue, 29 Apr 2025 01:46:15 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:fec29a8db8167835c3d33c13a53adb187be8ea1137e6437ae8cb7a02670e3d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0add89bfc80390c60bae6a10e97291fa9c4670e89dba05fca30a38e0b906263e`

```dockerfile
```

-	Layers:
	-	`sha256:709bb17f371f9cd6d69c1228e0c6c31cc07e4cf35023cac9a99f4c380ae40334`  
		Last Modified: Tue, 29 Apr 2025 01:46:15 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; 386

```console
$ docker pull varnish@sha256:baed0f4c518b3031447533c5124da57eef5fb94d48ff34121fbb13353a31a468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124905026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10a158cab887e28dc0310795e865268ef6fab3afa24c4736e534c5511c9bcc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c721a5f1a0287cb31914178d641a48fa6274d52b08210daa2d85721fb41fd546`  
		Last Modified: Mon, 28 Apr 2025 21:54:50 GMT  
		Size: 95.7 MB (95693406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9cb400d85d47cc31734b9480164e0fba4cd9204cdc79694d370b894edb293c`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:c14c4e1400c264fb990b93d9125c09324cb6644dfb9c36cef4e8db41f8227627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c14ae74490207909574666aff7d17fa462f1c628ecd4a652aa619ce851273b0`

```dockerfile
```

-	Layers:
	-	`sha256:6377d9af43befec53fe4750bbebf4a1b9af0a7dbc30b6c9fe8b5649be6a94ab3`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; ppc64le

```console
$ docker pull varnish@sha256:2ab2742df42e389b2d99b9b98f5d0f204cd5b2815db1d6ca1650f4b455f0612e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130405865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62af1c76c0e8c751881da24bbc76d605b15bfd206b20210b19c7f53737347323`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f1df676d0d3abc4949bfa1dea6269425b20479a4c559d02450410f90cd7f49`  
		Last Modified: Tue, 29 Apr 2025 00:37:38 GMT  
		Size: 98.3 MB (98336669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ed85d7bbb179a43d80cde46090f4332590ab823c91852bd65014a4918c9a67`  
		Last Modified: Tue, 29 Apr 2025 00:37:35 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:fdf5528c67d68405073265decbd118edaf02082ced8c7eefdbc36d7fee9f306d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63c1819b6d2fd1c6160178365c3036888a57785713559bc742dd2fe94c9d8b6`

```dockerfile
```

-	Layers:
	-	`sha256:d34991ca2d68b135ab293a3bf02619ec2939d20786a7f44f725cd251b448561c`  
		Last Modified: Tue, 29 Apr 2025 00:37:35 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; s390x

```console
$ docker pull varnish@sha256:7828527c1d0af8f5746ee8a3a008886eb1c022ac7740f333e730654c7dec6335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241cc916ed898550243ebba83f6e9b75ccafa64071888671514deccace37cc3d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be33dfb4c49615e8253f2ebdbbedfbabd730fd663917126ea31c212a55796a0d`  
		Last Modified: Tue, 29 Apr 2025 00:00:47 GMT  
		Size: 78.7 MB (78743483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7559210d805dd5af9d8a51a6b402e5cca6457dbd86b11500e5e0bfb120ff7204`  
		Last Modified: Tue, 29 Apr 2025 00:00:46 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:56e40c2e20a892c4d5bb11fab3f28806328e2c40dc20a84193b7020992309cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395ef4d628ed77d9861592b9ebbf10acc9001c96b583f74f6da217bf41dc519a`

```dockerfile
```

-	Layers:
	-	`sha256:396878abb84adc7edba33dd84d36dd0cd0abcd7a097e67e6fa7f5353933fe50e`  
		Last Modified: Tue, 29 Apr 2025 00:00:46 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7`

```console
$ docker pull varnish@sha256:3677549b54558d31781d7bc5cf7eedb7dc529c8c2bdd658b5051bee38bddf716
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

### `varnish:7` - linux; amd64

```console
$ docker pull varnish@sha256:5e582fe889ca8310d2438bbd359daab57ca51b822852380c213c6b757ce95d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134415217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d742f05731972fee8d565fd85b4063c391bd1a581ce6f5fac464be67f98619`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7b4e8561448447b5f17cdf10d16890983d981514d3e05b75afd403b4996105`  
		Last Modified: Mon, 28 Apr 2025 21:57:18 GMT  
		Size: 106.2 MB (106185535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb22ecd6cb33ac30f613868cf419ec33d9f59a3c8730f4ce33ffaf8c3bf64ee`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823c65497a18778874aa28bee2837df9e19da913bf21ba619d9a0e9cf2fc53b5`  
		Last Modified: Mon, 28 Apr 2025 21:57:17 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:b4d10289b86494a80849156633f8e20e092f09cc5390c4d270f0f94c0e574366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b937ebe837f9e47fd72b397157665e81c31d53a1341960b83dbf77c8b73ba8`

```dockerfile
```

-	Layers:
	-	`sha256:af5ca19bbc966bd6ae113c6fb062c2fc3ae349ae26d039823d1d2145154f260c`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c402e70ff618c750e4410ce74a6db1d84900b9e3c3b17f0ec158d091e93acc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104769290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9641fa2fee25c455ea22d4b8e218fcddab8fa85fefcd0e1a0f6a5a9deccde2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9364319ee06ae4bf793ccb5fc25bfd513c692eb71fafb6ac87776949ee3bc100`  
		Last Modified: Tue, 29 Apr 2025 03:30:45 GMT  
		Size: 80.8 MB (80829172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa721a1687c539d9c9a35850d4e20fddb509dbd6956a6cc445c000c70803012`  
		Last Modified: Tue, 29 Apr 2025 03:30:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4041ff56553fd96405a370eec490461068688511cb919ac9b7fac30ffba130d2`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:acdf0d138dd54916c74c1c1ea388a7030e5b4d097f444af960939582d45911fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ac5243e35371d10811891153007e8d691ea5583b0e6f7d76de7adfe58ffeea`

```dockerfile
```

-	Layers:
	-	`sha256:8674f207a0c369f9b69dd03060109a0130b0e8e16aa45c114de5512badf6bf19`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e14d12b67892d1a28aa7f4b76eb3c271aba73ad7815838bb0e64a98727c8fec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128717070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9d429f1d4a98fe900ea9c5dbaf87edab863c532203908094cfc71aa41a8b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f15d75e39de09fd0b81df4c7a488430e737e8b13bcc87349e672b54f6dfe0`  
		Last Modified: Tue, 29 Apr 2025 01:41:44 GMT  
		Size: 100.6 MB (100648406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2beda40612114f7b4e72b251f4e11ef46cfe9b526c8b8c8f91ab637b94e5e4e`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907bb59a11ef4a09e17a8bfd536e895f54a6aa41dfc6ab16e303bf5d85fb05d`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:7c4fbd9538c71f1e43a5917239e7a6a06e5ca22ec225138afd4be8cf287f3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfa568f8a6779d61b60d9de5199c559340fe5d6b4848e7e9760269c82229212`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c6f1e11c15ae9323f4854c423f6734d033a88917973b673de74478be0c8fc`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:12e085143d06fd1f852cc6e44ca2fcfc92a2c1c3ff25edb7b26bcb022e89f567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131508706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44bd4d23a67aa97268702362f0f8e033489d29f2b889668c4e6cfd6cac30b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b0acd2647e8753d66ff4f8e9283a0e95cbd8d1b4a074e3587232c2c84fe5`  
		Last Modified: Mon, 28 Apr 2025 21:55:26 GMT  
		Size: 102.3 MB (102295800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2693aef1f511398eb6ddf46822cf63cfbff6525e42d286ef7709c4eff63d9f45`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901bd6790d92b32002940e613c07c22254557b4a9986d92deda977a97eee74b`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:b5a68cfe963088ffd67f5e2047080feb3e01c5d362ed65d6a2af9a381cdb043a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f1f91bec453456dd78729905045a12be8b3e823090abd36546cc3bbdad60a4`

```dockerfile
```

-	Layers:
	-	`sha256:c6c6cd5add8cac6fe641c8ebd9e866072721b41e52effcfad7b52262602f33a1`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:57413efcd46c2d2a269e5b6d7d281e75df5295d8822fdbd43a1403856eae3eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137197788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab9a7c1f01651ce6374b1794bfdedaeedd17365045cc956c7ed4c15ba1a127`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a9ff1699f2e910d7dc5b9eb4faec71a66c0dec32a6f666c86161ca4116c29`  
		Last Modified: Tue, 29 Apr 2025 00:27:59 GMT  
		Size: 105.1 MB (105127296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68d270a371be1ef6a95992cbe1367f2c489a0d60ac1d6cc43799b41a75b43f1`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22dc480c2d31d38f0f5126e1899429c2a2f57e076a48a30ae50fd54f5368`  
		Last Modified: Tue, 29 Apr 2025 00:27:56 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:798748a8668f2d191df9a0ddead23e04595d4d6b3d7e86384e3e1235fa9e9992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0d05f566163ef49c04c513870aa065a234685892985d1d2ab675fb29c1462a`

```dockerfile
```

-	Layers:
	-	`sha256:716b65325abd64c3e8d0d7d53a0ec58a4bb4a8a239e59e9108887a92624f9b3f`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:00922e2886c9708ebd0398bec71a14a080323bd372e07086d071353267955acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112320868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474b3921d4cbde7bc1762576743522e68cd31f960e959a37f610d2ea2dd1abc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3117e4cac62b98179e474b41ecff263277909443424fde57be72cc3c4b458a49`  
		Last Modified: Mon, 28 Apr 2025 23:56:17 GMT  
		Size: 85.4 MB (85433954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad77db3e5534bad6736406965e8a8a9a47defa03a530c5185e0b8efedb7536c`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87d84786ca3a0a3b8613a9ab75e1f8a8f33d1a43c98523f30a3a0e1743783d`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:d19a0fd1b9dd1c1507c14b5a37daef2f02777fab5602c97d6b27147d5e38dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b385edcff1a6bfa467177b3c3b6d5b98f2fabf1cbbbdd697615b8da2e322de9f`

```dockerfile
```

-	Layers:
	-	`sha256:f3c18d363652d564de4601374b57093fbcdd554ed35713f5db6392f8dcb5bb47`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:d62e5a73fe9928aae297c1cab31d3d602c6e71863dca69ff3daa03f6d9948dba
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

### `varnish:7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:d7e148ec7d3a887e2ffc8aec14aaebc6eb169fc48995eabb29882fc6988c2fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73660932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bc8783b318613ff3297d2e84859d2839c1d064ef286021173e84302d003a94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6197199357be88819ed2d1d3f2a78e9f03de447def19ba8e7a1e4facfe53d0`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 70.2 MB (70238008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46db07dd06f45e7fa84d447b12fe6796e23178b4f018e6efa358e52d0f95f1e`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56637b510d4d3e86e2ecb77499b26ff8e2088f282c26dd242728eedc872a221a`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6aab6a99ed6c459097f0a53d453e3d9c667948f0e348eab3c02d3e2063a8e4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8277fb0c5e18c543a480c9980b8cdb815e7a103b1be70ac5dca920b665f2b`

```dockerfile
```

-	Layers:
	-	`sha256:2220ab8b577a4aef4d317e22d7fb49d2a57830d65f928b21891f9b913ef473c3`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 19.5 KB (19504 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5cdff5f8cdc86735cf3884098b25bb98d252d73dbee2fcbb8da0f192bcffba02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57868334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1a7af8983e9d8dedae368516ea89161e2c08ae5fcbe241d8c103c388bc5cec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83fdeaed4a0f5fd1c7da49f735cc0ffc5f2ebe699edb3411c56d4a89dfc789ec`  
		Last Modified: Fri, 14 Feb 2025 12:02:28 GMT  
		Size: 2.9 MB (2928999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b2fcb1e173a7c9c0f213b66e7007b5c1e6640f963db140b7641cb9c82d49d`  
		Last Modified: Thu, 20 Mar 2025 20:51:33 GMT  
		Size: 54.9 MB (54937275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927054ad65fa76f4687ff13459e96e9e2c431c80f35cbd75c8e2a6935801b26`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feee134b9efa4613b0c6af347a8ac2620e23353606389764b1846db5cdcae00e`  
		Last Modified: Thu, 20 Mar 2025 20:51:32 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4ead67a26abaf8fe0d1fb19622d8d14c546e14707461473039106e5208ae281c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7cae3e6c1ee2779eb84c3a428d8285db3addb6a09e7da5c31ac5129738f7f3`

```dockerfile
```

-	Layers:
	-	`sha256:4ddf3e6cd0fb731c535d6dc8b6d3a64b7c0c4dc2d511a6d54ccb1f363f2e9b0b`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 19.6 KB (19588 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ae93dd32a098b75e43257f1233d2da431329b067789195f24e455bbc7bcc9f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70380462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c55ab7ec3face2422bcc229b98c44b77778cf19c2d111eb139bc6c99de8e57c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e341e2e806c5beace803379ac980e67270f064187e8cc3eb2d3d497c640359b3`  
		Last Modified: Thu, 20 Mar 2025 20:50:57 GMT  
		Size: 67.0 MB (67016981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922bc3294fe218e430ef6821ad70f471a5d5623dca0110c170e38c0dc2b5e21e`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa3b8614225790b3a53a681d04efcf6afefbdbdffee3ef2df54fb955e651ddc`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9754f7a97aefd96a8a5083c616d6b696ae8a0a1bcacee125a7281a3ee6ea7d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2bcb3a16f36e11111d6c2196771af075f5cfa77ff4050c4d6d7251a49ec4fe`

```dockerfile
```

-	Layers:
	-	`sha256:a2f3555c80c3b024f6cb3eae0ecc06626ca24716b014f41e1f575a46e99c5b73`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 19.6 KB (19620 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:ed8a3d011fd526ed92bc7fc37bd43253026a1dcc9007f3704aa0d74092a1cfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75675277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce80b46b1d57f82c93ebb8fedc397df0c5e9d73c0f9f4bca30b953f173374ce`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceea9d04caf7123c428cc71b6e189a701c0df9dfb5c4636cdb932a182c5dc92b`  
		Last Modified: Thu, 20 Mar 2025 20:49:18 GMT  
		Size: 72.4 MB (72417773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbf628b09c56f1ed9a9bc0c6c80e30384c1e212514ac6d4320fad560f76154`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68e4e53b91e7a2a0bacd7195519477e580278fbd62ff1e165dc3d26182a5e40`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:095da0d2ed38cc0f3cdd97f259030778e2db708196bbd692ee530528d96fcba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054084cd1ffb8a0cb53a2ebbef0d5b644fb8d8f6af5bbcd46c0dcb8e3bd6a73b`

```dockerfile
```

-	Layers:
	-	`sha256:006e78a4fc563908ab782848ef484c1cd38954fe1d7db867bbd567741a5616d9`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:ed47ea7fca08b1d59646052271e39082656a30391b9d1065e5731d876e174e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71173698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfb1a9773960e2166100bdf78b0094372fe8f1f088fa1ae554461f53db2b632`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fd377eadab07129ae42057b3a16a87aca2e34cc454137b6ad3eebd6472d671`  
		Last Modified: Thu, 20 Mar 2025 20:53:21 GMT  
		Size: 67.8 MB (67805504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81a16e6a322ac046043d3947a2b952f562ed9e6b9a8dcb8d08aeef3ebf1473`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6081bae5b7b1caccd6289bf5cdad31d109060d1b56a9b6e68e48daee158f59`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3603283b01c0481efe5f71fbfdfc61da6c79565d645af850ec154e0b2af60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e9863851dd0104e6518306251bd45cd43ab025a102f8fef257b4017a68d7be`

```dockerfile
```

-	Layers:
	-	`sha256:56107729091864baa86fc11d1a3bd790a74d944f1f8c591da367f65ba5db438a`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:142b451bbc107898e7a43626694442f8d689e862bc76e6658c16a0e3e480c97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65564524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9c3fc8d83faf437103d088d06f0ab28c78071fbc721bfaa507344fb60f4e38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26ca67b2cc4f3c0d15180a19540e9b0a8077bec01f8213e27886b9cbb53750a`  
		Last Modified: Thu, 20 Mar 2025 20:52:03 GMT  
		Size: 62.3 MB (62307641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a98df498d36504153285d47ac06e34aa48bce7cd6649d7d8233f1ae913b56`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172ffc710311115ba888f35e74818e247cfc16ab6e82c0ea1256a68f0adec21`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6d2ff36f410fb69c0d1ab67ef1d8ef8c534c4e9d021da06dbb777f05f1d38670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef5c0271027e9dc11cf1442054efecab44ebdac61c2f31e161f0727b747116e`

```dockerfile
```

-	Layers:
	-	`sha256:6f29dbad55a89c5bf361b46d778edd1d920636239f023fd05dd37b9a502f3816`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6`

```console
$ docker pull varnish@sha256:392b7a345bbece3fff16412696879a2e2cd818a38094caaabc880a2999d17b25
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

### `varnish:7.6` - linux; amd64

```console
$ docker pull varnish@sha256:2ff25c0539a93bfaab23560820679eaeead08a20b83d308b5963ca0f134c6440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134223431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7ae0c300b5434fac6efdb73a5f8e42076ff494fda57378adad16f328282b25`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd216553706e69a2f474de76f228faab86ce1125e5940e0609e1bcb1d05581d8`  
		Last Modified: Mon, 28 Apr 2025 21:57:26 GMT  
		Size: 106.0 MB (105993748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37a969703010e8a4205f70a0c873161a902d34c1cc7db02b619698754c21e1`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a02b7a4b892df9ebb3f70c42dd6af257abce9438b514accf626e6b4ba4a585`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:7ca43761a990badfd7465a643026e91bd0bb0c524733cbdfea5d002942c7fe68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d1398c922fc29fd9c65a8134e66bbf3a95d27023888cf7d4840739a12b304b`

```dockerfile
```

-	Layers:
	-	`sha256:f743c3c420c533c168e954a51a9b13cb0069ea8a3301b3dfc5c8e1e7abc3cc01`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d10729abf1128e476456659b6430558d63948d73a98989f34a1634e6fe99323b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104605767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2cf92822d35a0b7991aa3e98197a3b57f162654b3bd256224ab9f27da4eb71`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26699162f33b93aaee327495a053e9e73ed91c7f9ef49957cdc41278ac3c0c4d`  
		Last Modified: Tue, 29 Apr 2025 03:33:56 GMT  
		Size: 80.7 MB (80665649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f598f5990a40210d6afe2d8b5ae214ff215d711ace58c837ab456ba1fdcbfdcb`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5564fa94668584067783e080ce6387d24fd607e70905167f6e52e3471ba1792c`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:824678cb3925eacab1c68f38bb8ce743c22782aa17d3f8856f33b801d7a187c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1817272c11a485f4fd3ffb9bc23195d8ad7fb9a19253d1ce02800622d9a6d1d4`

```dockerfile
```

-	Layers:
	-	`sha256:c0508effd86891effe9ba5956cbe4ac5f3bbc1d00518cf15a66313e4ea5d1b73`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3d87d6e9107f05b3fdf4faa907da022c409e14e12a41938ed789f5c22d08360c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128546406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec921b50493106c35f93a6b65fce5826e9cf12aa1967010c2e64bf6b6caa56af`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9007928d56da5956c3adb5c9b09cd6052e96eea3d6b32188b18f1abdfafa146`  
		Last Modified: Tue, 29 Apr 2025 01:44:22 GMT  
		Size: 100.5 MB (100477739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec066d9f82de1a6eeab143dcd97003245d1c11b278233dff87c405b260a7d9`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec3524e4e7f30b267be1cfc7a6670001491801c87ba8f2e7c1b0fabe6ac016a`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:622a6360a17e934022c7d4fe24ebf4db904777f9cd490f35c7063b90c47f0117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc7c639574b829cf3f99b393c5c893bbd2196d4faf4e3d8dcd16b1cd384f861`

```dockerfile
```

-	Layers:
	-	`sha256:436db9522c40712324082095c6781b04835223afddf2c628e654f72d30cd7be9`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:b316e37e5e0956ddee4d3aedc2dd2dd5364d7fca3587f7b5ab91129f10f7c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131346360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a327fca69bdd4a49b802a99ccb4ce9e7079e679b10498bf79696c9072e97e5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe369bcdf81670933ddffbfb1c2526dd850b10c9bfa6625a6a9ba80b99e6a553`  
		Last Modified: Mon, 28 Apr 2025 21:55:36 GMT  
		Size: 102.1 MB (102133453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07707c37a55d9f43914fbb068753ce52f76bfff997783b74c7de6f820aecf764`  
		Last Modified: Mon, 28 Apr 2025 21:55:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a075088a22133c4633cbe4644976b94ee415685dd6e84eabfa015b5bfc20566`  
		Last Modified: Mon, 28 Apr 2025 21:55:33 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:42dedbcf904216f149eb9f3b3a24cdfdc184259ce9ea3ed64bd1fcbbfede42ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8018d56b0c1e07eab3226f34b2f5195d543d2f954237f87412041940ce4d0b`

```dockerfile
```

-	Layers:
	-	`sha256:01be35c1c45bf9e604c6549165dd929cb56d66baa5bf06d3885791e09b7f5ef5`  
		Last Modified: Mon, 28 Apr 2025 21:55:32 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:c541fd0765cf5296adc92ae9857b103e883ab287effd245f2e2ecf639c29bf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137028796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323add35bc6ea4f4a5a8b204ff25e99ac5ef6bf1e32cdf9e529402da0f3ec3ae`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3193435e4946ec028eeea6d9cd36c97de2d8aadad82e23c06d4d57a7b796eec1`  
		Last Modified: Tue, 29 Apr 2025 00:33:19 GMT  
		Size: 105.0 MB (104958305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87731d847ede151767ec041ca951a73ce8fc086290b136ca26ba4aeccee77c86`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38ed7e15cf5cceec258fb261134dfbd40ea6224996f9008056c03e560e0aa1d`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:ddf964f71b0c0952f1a6bc496153e9a3c48f62055a9e8dea374500f9ad45f5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf6c2ed8342dd48583fd61e8228f2f785985c3dc376f729a9a53d364f22396c`

```dockerfile
```

-	Layers:
	-	`sha256:59ac67029d18279dac18dd817629f21a4aebd2534e7767e7bbee3a31d72ae093`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 18.9 KB (18884 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:72b074e2f19bc90c53b61eb1c7b69a251b13007f13c842859a439dd59897953b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112144101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b34dabe3364079afbafc0635d712c83c133e66658674f46f2d389f30930d6a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c0afa22588812a685d63f169267aaa819a5d4694e83b7ea954d3e1e0c4da38`  
		Last Modified: Mon, 28 Apr 2025 23:58:57 GMT  
		Size: 85.3 MB (85257186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094ff07e8df96906a4ab6e53b3dc03e09b65b05a7f6d90391ada09d1b2709215`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a7d67eca8d2ce4bc90cb000e30962e8413c6c17486bbfe92ec2942ce141ff1`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:76f330b0e7338efa15c393bfcd33f5e9b99aa7389ade0daea954617684f9c6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e6d6994a8e7c391a4537c6c49733b01d84d2d85ce856e4ff4523dee5470354`

```dockerfile
```

-	Layers:
	-	`sha256:d6425b061c170152fa4451d358ec00bc5665f23f503ac58305c082d6da433442`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:889cbd23197112e75773111a63ca342b15ff07c78101b3452df284c1914fcbe8
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

### `varnish:7.6-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:cea8646dcc243e71ed9e3d45055c8d4edbb244f62308d85985c76041d3e9a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73503835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7ca24fc498e3f92c1488fd4ff724d5fbdd51ba1572ff7a03c7850c5807b467`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f18e5ee15b30322b340b50363205554d0072c742abc97109ee109af901d70`  
		Last Modified: Thu, 20 Mar 2025 20:49:03 GMT  
		Size: 70.1 MB (70080908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984719446ab1208d5434dc302aaddb6a50728448133507f6571aecfb9bf2385`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093556cead941ed143ba4d8eae061178a833fcd6a012ccf6fb0587dc2b6df5a7`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:620589ef60655bd95a7224c102279a7e251fd7c93fb34ec70eb376b7849a0a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f7eac1ff2486705ed7ab3703f1975d838c850cd2354a34ebd991788379f4da`

```dockerfile
```

-	Layers:
	-	`sha256:7cf4aaaab0b9957870eeb0d720d0e0e4cfcc99f495e815950d36c3a45705b61f`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 18.8 KB (18804 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3a68f396e3a33a39d15e7ee577b4d3762d673eb6aee39d798af309d58bc9ba46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57701783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bdd592b48398e853a7e5def2226eea0b3e705e6e6268982d2d29c80359fdf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83fdeaed4a0f5fd1c7da49f735cc0ffc5f2ebe699edb3411c56d4a89dfc789ec`  
		Last Modified: Fri, 14 Feb 2025 12:02:28 GMT  
		Size: 2.9 MB (2928999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27416bff113d8f24380377ffb42ac39dfdd67b1137b2373b871d39fcd3c426fa`  
		Last Modified: Thu, 20 Mar 2025 20:55:52 GMT  
		Size: 54.8 MB (54770727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db75fcc41dd2a451d7daedc14c136e54985557e45451152b2ca6e63341a8f2b7`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fad2892c6952544d2917b6650809e2994fe1794a5781cf4a291cf48726624c4`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:23989a80ae452da348f6f36847ec90aeb87fa622e1185a542d0968172b962cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735ed7f1d4b3e6c76ab7c0799882d144ab04e77869eea01ceb8efe7560f10e16`

```dockerfile
```

-	Layers:
	-	`sha256:c52cf7abb4f6619880b530088a6f3f9254c8c698b9ef295210e206c791d918a0`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3e99b357cfebf29315f5c6c1757e97474ea415d3ecdf9351abc0b6b7bbf0a9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70224522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec791631402f7ae975774f4b6c2fe49a56a44577665ec8f469d911655947971`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314dbe51a23e5aa36e6f06cb8131fb67ce3336f95cce019738e2b56b21edf0b0`  
		Last Modified: Thu, 20 Mar 2025 20:54:54 GMT  
		Size: 66.9 MB (66861043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b9a16fdb9c48c3123dedd60c7e6ba7e0e0962e57068c081b20e444deb8dfcc`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7ffa8106b9714bcdcf65732cd12da3e815e160582e810d0848d4f99ca61ff4`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e9c5c8719e2984189db33d8d8e30ca9672fdc56c95f4b531da4be7212cf6a7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4b22bbdefa389173bb668631bdabf08de9af4bb0dda35baeefc83fc1d46926`

```dockerfile
```

-	Layers:
	-	`sha256:9f9604e2370f4626f35df6ac79eeffd6d362b00f0248799bd606ddd4c2705a3e`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:5c791d454d530cd33c23edb3a5138931390382951bb4f8860e8ae77dff0d4c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75520843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757b34fc17bec41eb78d0aa86510a54a70249f736c538898be6c926ff65c07b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105edcac606f410c0a0480d6aa3ba8c697e6849c4e9bacbdbf8edf276e85faa2`  
		Last Modified: Thu, 20 Mar 2025 20:49:13 GMT  
		Size: 72.3 MB (72263339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2146b0b689108a78ccc703c22bed6653e16a9083948bcce183a965e16e0042`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3639f317bd35f20772ffa4d992ca7f78a98979fadab9c48b99cbc1efe98a2165`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d2e530159f245e975e1997f8009298d7c9fe6a05eadca7d7619ae79af1f3d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4710a17a7af83aaf44a8b1ae0756a96a92990e79509ef4cef6ca3b613d0a2b4`

```dockerfile
```

-	Layers:
	-	`sha256:ebdb2b6983834e3a0de138515539bd40e0abe377996086267afca1e52f798936`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:cecd5ab036369bc9f93e96b751d336fb5c2e900cd9881569d77d833d2e81f300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71019634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635256b7fcb8cfdda9959ab995354551d8f4f43c7f52ffa3a3ef7cb34899e0de`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dbb81854e57495f319359a216625484e49eda40cc71bbedd331c77a691db03`  
		Last Modified: Thu, 20 Mar 2025 20:59:24 GMT  
		Size: 67.7 MB (67651439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db38eb2c902867cb53b936c6379d20d3a30f98fb468c109e5da24d7059ef0b8e`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687ef06ba3519de4b614d0a1d2680236223054ec3e9cfa088d0d0adccdb7049`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f71c8954ca22f4d38cbdc1c4e6036f80ca96efea432b5e0d90014a7a57dbb567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f4feeaf4c5a7ae7fcc344eff51f6490162ddd1435b36e6e87a06fe15488e59`

```dockerfile
```

-	Layers:
	-	`sha256:526b999ab1be5a288adff6be69eb0a6318ba6df88c93367acc253ca560f9dfd7`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:24660accdbdc53f4bb3603c08280b6f6384fb66a0445b39daa0dcb9e58a8cc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65405882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3a59e903c9d2a5a1f9e716fe06b237797002be14d5bbb3d0d080717021f17d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6ed6a11500b4dd92fd1b04a0eefcc30aeee6a545bd70b481dca6a8aa8c28f4`  
		Last Modified: Thu, 20 Mar 2025 20:56:26 GMT  
		Size: 62.1 MB (62149009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af226806eb4379bc9469a0210d5c4a8104803fe0fd7f52e2988b5ccc362dece8`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed42a627c6611b8e149439a43ed94fbdf3aecb62043b5896d7195734c49bd4a`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:85fca3d73c264caa655ec59dfdabbff7897081a02d21c3e588e2f3729fc40aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b547091505d268e8cd358ad6d34098c51ec84f2f08c8ce9e9519ea2ebc5d2aa`

```dockerfile
```

-	Layers:
	-	`sha256:7d07064a5d33392132cfab6a4f816bee701f6e3523f300c70f0b1cc832cb0b57`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.1`

```console
$ docker pull varnish@sha256:392b7a345bbece3fff16412696879a2e2cd818a38094caaabc880a2999d17b25
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

### `varnish:7.6.1` - linux; amd64

```console
$ docker pull varnish@sha256:2ff25c0539a93bfaab23560820679eaeead08a20b83d308b5963ca0f134c6440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134223431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7ae0c300b5434fac6efdb73a5f8e42076ff494fda57378adad16f328282b25`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd216553706e69a2f474de76f228faab86ce1125e5940e0609e1bcb1d05581d8`  
		Last Modified: Mon, 28 Apr 2025 21:57:26 GMT  
		Size: 106.0 MB (105993748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37a969703010e8a4205f70a0c873161a902d34c1cc7db02b619698754c21e1`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a02b7a4b892df9ebb3f70c42dd6af257abce9438b514accf626e6b4ba4a585`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:7ca43761a990badfd7465a643026e91bd0bb0c524733cbdfea5d002942c7fe68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d1398c922fc29fd9c65a8134e66bbf3a95d27023888cf7d4840739a12b304b`

```dockerfile
```

-	Layers:
	-	`sha256:f743c3c420c533c168e954a51a9b13cb0069ea8a3301b3dfc5c8e1e7abc3cc01`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d10729abf1128e476456659b6430558d63948d73a98989f34a1634e6fe99323b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104605767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2cf92822d35a0b7991aa3e98197a3b57f162654b3bd256224ab9f27da4eb71`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26699162f33b93aaee327495a053e9e73ed91c7f9ef49957cdc41278ac3c0c4d`  
		Last Modified: Tue, 29 Apr 2025 03:33:56 GMT  
		Size: 80.7 MB (80665649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f598f5990a40210d6afe2d8b5ae214ff215d711ace58c837ab456ba1fdcbfdcb`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5564fa94668584067783e080ce6387d24fd607e70905167f6e52e3471ba1792c`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:824678cb3925eacab1c68f38bb8ce743c22782aa17d3f8856f33b801d7a187c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1817272c11a485f4fd3ffb9bc23195d8ad7fb9a19253d1ce02800622d9a6d1d4`

```dockerfile
```

-	Layers:
	-	`sha256:c0508effd86891effe9ba5956cbe4ac5f3bbc1d00518cf15a66313e4ea5d1b73`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3d87d6e9107f05b3fdf4faa907da022c409e14e12a41938ed789f5c22d08360c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128546406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec921b50493106c35f93a6b65fce5826e9cf12aa1967010c2e64bf6b6caa56af`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9007928d56da5956c3adb5c9b09cd6052e96eea3d6b32188b18f1abdfafa146`  
		Last Modified: Tue, 29 Apr 2025 01:44:22 GMT  
		Size: 100.5 MB (100477739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec066d9f82de1a6eeab143dcd97003245d1c11b278233dff87c405b260a7d9`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec3524e4e7f30b267be1cfc7a6670001491801c87ba8f2e7c1b0fabe6ac016a`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:622a6360a17e934022c7d4fe24ebf4db904777f9cd490f35c7063b90c47f0117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc7c639574b829cf3f99b393c5c893bbd2196d4faf4e3d8dcd16b1cd384f861`

```dockerfile
```

-	Layers:
	-	`sha256:436db9522c40712324082095c6781b04835223afddf2c628e654f72d30cd7be9`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; 386

```console
$ docker pull varnish@sha256:b316e37e5e0956ddee4d3aedc2dd2dd5364d7fca3587f7b5ab91129f10f7c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131346360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a327fca69bdd4a49b802a99ccb4ce9e7079e679b10498bf79696c9072e97e5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe369bcdf81670933ddffbfb1c2526dd850b10c9bfa6625a6a9ba80b99e6a553`  
		Last Modified: Mon, 28 Apr 2025 21:55:36 GMT  
		Size: 102.1 MB (102133453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07707c37a55d9f43914fbb068753ce52f76bfff997783b74c7de6f820aecf764`  
		Last Modified: Mon, 28 Apr 2025 21:55:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a075088a22133c4633cbe4644976b94ee415685dd6e84eabfa015b5bfc20566`  
		Last Modified: Mon, 28 Apr 2025 21:55:33 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:42dedbcf904216f149eb9f3b3a24cdfdc184259ce9ea3ed64bd1fcbbfede42ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8018d56b0c1e07eab3226f34b2f5195d543d2f954237f87412041940ce4d0b`

```dockerfile
```

-	Layers:
	-	`sha256:01be35c1c45bf9e604c6549165dd929cb56d66baa5bf06d3885791e09b7f5ef5`  
		Last Modified: Mon, 28 Apr 2025 21:55:32 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:c541fd0765cf5296adc92ae9857b103e883ab287effd245f2e2ecf639c29bf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137028796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323add35bc6ea4f4a5a8b204ff25e99ac5ef6bf1e32cdf9e529402da0f3ec3ae`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3193435e4946ec028eeea6d9cd36c97de2d8aadad82e23c06d4d57a7b796eec1`  
		Last Modified: Tue, 29 Apr 2025 00:33:19 GMT  
		Size: 105.0 MB (104958305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87731d847ede151767ec041ca951a73ce8fc086290b136ca26ba4aeccee77c86`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38ed7e15cf5cceec258fb261134dfbd40ea6224996f9008056c03e560e0aa1d`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:ddf964f71b0c0952f1a6bc496153e9a3c48f62055a9e8dea374500f9ad45f5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf6c2ed8342dd48583fd61e8228f2f785985c3dc376f729a9a53d364f22396c`

```dockerfile
```

-	Layers:
	-	`sha256:59ac67029d18279dac18dd817629f21a4aebd2534e7767e7bbee3a31d72ae093`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 18.9 KB (18884 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; s390x

```console
$ docker pull varnish@sha256:72b074e2f19bc90c53b61eb1c7b69a251b13007f13c842859a439dd59897953b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112144101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b34dabe3364079afbafc0635d712c83c133e66658674f46f2d389f30930d6a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c0afa22588812a685d63f169267aaa819a5d4694e83b7ea954d3e1e0c4da38`  
		Last Modified: Mon, 28 Apr 2025 23:58:57 GMT  
		Size: 85.3 MB (85257186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094ff07e8df96906a4ab6e53b3dc03e09b65b05a7f6d90391ada09d1b2709215`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a7d67eca8d2ce4bc90cb000e30962e8413c6c17486bbfe92ec2942ce141ff1`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:76f330b0e7338efa15c393bfcd33f5e9b99aa7389ade0daea954617684f9c6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e6d6994a8e7c391a4537c6c49733b01d84d2d85ce856e4ff4523dee5470354`

```dockerfile
```

-	Layers:
	-	`sha256:d6425b061c170152fa4451d358ec00bc5665f23f503ac58305c082d6da433442`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.1-alpine`

```console
$ docker pull varnish@sha256:889cbd23197112e75773111a63ca342b15ff07c78101b3452df284c1914fcbe8
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

### `varnish:7.6.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:cea8646dcc243e71ed9e3d45055c8d4edbb244f62308d85985c76041d3e9a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73503835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7ca24fc498e3f92c1488fd4ff724d5fbdd51ba1572ff7a03c7850c5807b467`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f18e5ee15b30322b340b50363205554d0072c742abc97109ee109af901d70`  
		Last Modified: Thu, 20 Mar 2025 20:49:03 GMT  
		Size: 70.1 MB (70080908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984719446ab1208d5434dc302aaddb6a50728448133507f6571aecfb9bf2385`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093556cead941ed143ba4d8eae061178a833fcd6a012ccf6fb0587dc2b6df5a7`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:620589ef60655bd95a7224c102279a7e251fd7c93fb34ec70eb376b7849a0a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f7eac1ff2486705ed7ab3703f1975d838c850cd2354a34ebd991788379f4da`

```dockerfile
```

-	Layers:
	-	`sha256:7cf4aaaab0b9957870eeb0d720d0e0e4cfcc99f495e815950d36c3a45705b61f`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 18.8 KB (18804 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3a68f396e3a33a39d15e7ee577b4d3762d673eb6aee39d798af309d58bc9ba46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57701783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bdd592b48398e853a7e5def2226eea0b3e705e6e6268982d2d29c80359fdf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83fdeaed4a0f5fd1c7da49f735cc0ffc5f2ebe699edb3411c56d4a89dfc789ec`  
		Last Modified: Fri, 14 Feb 2025 12:02:28 GMT  
		Size: 2.9 MB (2928999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27416bff113d8f24380377ffb42ac39dfdd67b1137b2373b871d39fcd3c426fa`  
		Last Modified: Thu, 20 Mar 2025 20:55:52 GMT  
		Size: 54.8 MB (54770727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db75fcc41dd2a451d7daedc14c136e54985557e45451152b2ca6e63341a8f2b7`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fad2892c6952544d2917b6650809e2994fe1794a5781cf4a291cf48726624c4`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:23989a80ae452da348f6f36847ec90aeb87fa622e1185a542d0968172b962cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735ed7f1d4b3e6c76ab7c0799882d144ab04e77869eea01ceb8efe7560f10e16`

```dockerfile
```

-	Layers:
	-	`sha256:c52cf7abb4f6619880b530088a6f3f9254c8c698b9ef295210e206c791d918a0`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3e99b357cfebf29315f5c6c1757e97474ea415d3ecdf9351abc0b6b7bbf0a9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70224522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec791631402f7ae975774f4b6c2fe49a56a44577665ec8f469d911655947971`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314dbe51a23e5aa36e6f06cb8131fb67ce3336f95cce019738e2b56b21edf0b0`  
		Last Modified: Thu, 20 Mar 2025 20:54:54 GMT  
		Size: 66.9 MB (66861043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b9a16fdb9c48c3123dedd60c7e6ba7e0e0962e57068c081b20e444deb8dfcc`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7ffa8106b9714bcdcf65732cd12da3e815e160582e810d0848d4f99ca61ff4`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e9c5c8719e2984189db33d8d8e30ca9672fdc56c95f4b531da4be7212cf6a7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4b22bbdefa389173bb668631bdabf08de9af4bb0dda35baeefc83fc1d46926`

```dockerfile
```

-	Layers:
	-	`sha256:9f9604e2370f4626f35df6ac79eeffd6d362b00f0248799bd606ddd4c2705a3e`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:5c791d454d530cd33c23edb3a5138931390382951bb4f8860e8ae77dff0d4c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75520843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757b34fc17bec41eb78d0aa86510a54a70249f736c538898be6c926ff65c07b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105edcac606f410c0a0480d6aa3ba8c697e6849c4e9bacbdbf8edf276e85faa2`  
		Last Modified: Thu, 20 Mar 2025 20:49:13 GMT  
		Size: 72.3 MB (72263339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2146b0b689108a78ccc703c22bed6653e16a9083948bcce183a965e16e0042`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3639f317bd35f20772ffa4d992ca7f78a98979fadab9c48b99cbc1efe98a2165`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d2e530159f245e975e1997f8009298d7c9fe6a05eadca7d7619ae79af1f3d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4710a17a7af83aaf44a8b1ae0756a96a92990e79509ef4cef6ca3b613d0a2b4`

```dockerfile
```

-	Layers:
	-	`sha256:ebdb2b6983834e3a0de138515539bd40e0abe377996086267afca1e52f798936`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:cecd5ab036369bc9f93e96b751d336fb5c2e900cd9881569d77d833d2e81f300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71019634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635256b7fcb8cfdda9959ab995354551d8f4f43c7f52ffa3a3ef7cb34899e0de`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dbb81854e57495f319359a216625484e49eda40cc71bbedd331c77a691db03`  
		Last Modified: Thu, 20 Mar 2025 20:59:24 GMT  
		Size: 67.7 MB (67651439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db38eb2c902867cb53b936c6379d20d3a30f98fb468c109e5da24d7059ef0b8e`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687ef06ba3519de4b614d0a1d2680236223054ec3e9cfa088d0d0adccdb7049`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f71c8954ca22f4d38cbdc1c4e6036f80ca96efea432b5e0d90014a7a57dbb567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f4feeaf4c5a7ae7fcc344eff51f6490162ddd1435b36e6e87a06fe15488e59`

```dockerfile
```

-	Layers:
	-	`sha256:526b999ab1be5a288adff6be69eb0a6318ba6df88c93367acc253ca560f9dfd7`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:24660accdbdc53f4bb3603c08280b6f6384fb66a0445b39daa0dcb9e58a8cc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65405882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3a59e903c9d2a5a1f9e716fe06b237797002be14d5bbb3d0d080717021f17d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6ed6a11500b4dd92fd1b04a0eefcc30aeee6a545bd70b481dca6a8aa8c28f4`  
		Last Modified: Thu, 20 Mar 2025 20:56:26 GMT  
		Size: 62.1 MB (62149009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af226806eb4379bc9469a0210d5c4a8104803fe0fd7f52e2988b5ccc362dece8`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed42a627c6611b8e149439a43ed94fbdf3aecb62043b5896d7195734c49bd4a`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:85fca3d73c264caa655ec59dfdabbff7897081a02d21c3e588e2f3729fc40aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b547091505d268e8cd358ad6d34098c51ec84f2f08c8ce9e9519ea2ebc5d2aa`

```dockerfile
```

-	Layers:
	-	`sha256:7d07064a5d33392132cfab6a4f816bee701f6e3523f300c70f0b1cc832cb0b57`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:3677549b54558d31781d7bc5cf7eedb7dc529c8c2bdd658b5051bee38bddf716
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
$ docker pull varnish@sha256:5e582fe889ca8310d2438bbd359daab57ca51b822852380c213c6b757ce95d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134415217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d742f05731972fee8d565fd85b4063c391bd1a581ce6f5fac464be67f98619`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7b4e8561448447b5f17cdf10d16890983d981514d3e05b75afd403b4996105`  
		Last Modified: Mon, 28 Apr 2025 21:57:18 GMT  
		Size: 106.2 MB (106185535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb22ecd6cb33ac30f613868cf419ec33d9f59a3c8730f4ce33ffaf8c3bf64ee`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823c65497a18778874aa28bee2837df9e19da913bf21ba619d9a0e9cf2fc53b5`  
		Last Modified: Mon, 28 Apr 2025 21:57:17 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:b4d10289b86494a80849156633f8e20e092f09cc5390c4d270f0f94c0e574366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b937ebe837f9e47fd72b397157665e81c31d53a1341960b83dbf77c8b73ba8`

```dockerfile
```

-	Layers:
	-	`sha256:af5ca19bbc966bd6ae113c6fb062c2fc3ae349ae26d039823d1d2145154f260c`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c402e70ff618c750e4410ce74a6db1d84900b9e3c3b17f0ec158d091e93acc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104769290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9641fa2fee25c455ea22d4b8e218fcddab8fa85fefcd0e1a0f6a5a9deccde2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9364319ee06ae4bf793ccb5fc25bfd513c692eb71fafb6ac87776949ee3bc100`  
		Last Modified: Tue, 29 Apr 2025 03:30:45 GMT  
		Size: 80.8 MB (80829172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa721a1687c539d9c9a35850d4e20fddb509dbd6956a6cc445c000c70803012`  
		Last Modified: Tue, 29 Apr 2025 03:30:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4041ff56553fd96405a370eec490461068688511cb919ac9b7fac30ffba130d2`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:acdf0d138dd54916c74c1c1ea388a7030e5b4d097f444af960939582d45911fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ac5243e35371d10811891153007e8d691ea5583b0e6f7d76de7adfe58ffeea`

```dockerfile
```

-	Layers:
	-	`sha256:8674f207a0c369f9b69dd03060109a0130b0e8e16aa45c114de5512badf6bf19`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e14d12b67892d1a28aa7f4b76eb3c271aba73ad7815838bb0e64a98727c8fec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128717070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9d429f1d4a98fe900ea9c5dbaf87edab863c532203908094cfc71aa41a8b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f15d75e39de09fd0b81df4c7a488430e737e8b13bcc87349e672b54f6dfe0`  
		Last Modified: Tue, 29 Apr 2025 01:41:44 GMT  
		Size: 100.6 MB (100648406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2beda40612114f7b4e72b251f4e11ef46cfe9b526c8b8c8f91ab637b94e5e4e`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907bb59a11ef4a09e17a8bfd536e895f54a6aa41dfc6ab16e303bf5d85fb05d`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:7c4fbd9538c71f1e43a5917239e7a6a06e5ca22ec225138afd4be8cf287f3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfa568f8a6779d61b60d9de5199c559340fe5d6b4848e7e9760269c82229212`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c6f1e11c15ae9323f4854c423f6734d033a88917973b673de74478be0c8fc`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; 386

```console
$ docker pull varnish@sha256:12e085143d06fd1f852cc6e44ca2fcfc92a2c1c3ff25edb7b26bcb022e89f567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131508706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44bd4d23a67aa97268702362f0f8e033489d29f2b889668c4e6cfd6cac30b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b0acd2647e8753d66ff4f8e9283a0e95cbd8d1b4a074e3587232c2c84fe5`  
		Last Modified: Mon, 28 Apr 2025 21:55:26 GMT  
		Size: 102.3 MB (102295800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2693aef1f511398eb6ddf46822cf63cfbff6525e42d286ef7709c4eff63d9f45`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901bd6790d92b32002940e613c07c22254557b4a9986d92deda977a97eee74b`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:b5a68cfe963088ffd67f5e2047080feb3e01c5d362ed65d6a2af9a381cdb043a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f1f91bec453456dd78729905045a12be8b3e823090abd36546cc3bbdad60a4`

```dockerfile
```

-	Layers:
	-	`sha256:c6c6cd5add8cac6fe641c8ebd9e866072721b41e52effcfad7b52262602f33a1`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; ppc64le

```console
$ docker pull varnish@sha256:57413efcd46c2d2a269e5b6d7d281e75df5295d8822fdbd43a1403856eae3eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137197788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab9a7c1f01651ce6374b1794bfdedaeedd17365045cc956c7ed4c15ba1a127`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a9ff1699f2e910d7dc5b9eb4faec71a66c0dec32a6f666c86161ca4116c29`  
		Last Modified: Tue, 29 Apr 2025 00:27:59 GMT  
		Size: 105.1 MB (105127296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68d270a371be1ef6a95992cbe1367f2c489a0d60ac1d6cc43799b41a75b43f1`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22dc480c2d31d38f0f5126e1899429c2a2f57e076a48a30ae50fd54f5368`  
		Last Modified: Tue, 29 Apr 2025 00:27:56 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:798748a8668f2d191df9a0ddead23e04595d4d6b3d7e86384e3e1235fa9e9992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0d05f566163ef49c04c513870aa065a234685892985d1d2ab675fb29c1462a`

```dockerfile
```

-	Layers:
	-	`sha256:716b65325abd64c3e8d0d7d53a0ec58a4bb4a8a239e59e9108887a92624f9b3f`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; s390x

```console
$ docker pull varnish@sha256:00922e2886c9708ebd0398bec71a14a080323bd372e07086d071353267955acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112320868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474b3921d4cbde7bc1762576743522e68cd31f960e959a37f610d2ea2dd1abc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3117e4cac62b98179e474b41ecff263277909443424fde57be72cc3c4b458a49`  
		Last Modified: Mon, 28 Apr 2025 23:56:17 GMT  
		Size: 85.4 MB (85433954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad77db3e5534bad6736406965e8a8a9a47defa03a530c5185e0b8efedb7536c`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87d84786ca3a0a3b8613a9ab75e1f8a8f33d1a43c98523f30a3a0e1743783d`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:d19a0fd1b9dd1c1507c14b5a37daef2f02777fab5602c97d6b27147d5e38dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b385edcff1a6bfa467177b3c3b6d5b98f2fabf1cbbbdd697615b8da2e322de9f`

```dockerfile
```

-	Layers:
	-	`sha256:f3c18d363652d564de4601374b57093fbcdd554ed35713f5db6392f8dcb5bb47`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7-alpine`

```console
$ docker pull varnish@sha256:d62e5a73fe9928aae297c1cab31d3d602c6e71863dca69ff3daa03f6d9948dba
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
$ docker pull varnish@sha256:d7e148ec7d3a887e2ffc8aec14aaebc6eb169fc48995eabb29882fc6988c2fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73660932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bc8783b318613ff3297d2e84859d2839c1d064ef286021173e84302d003a94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6197199357be88819ed2d1d3f2a78e9f03de447def19ba8e7a1e4facfe53d0`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 70.2 MB (70238008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46db07dd06f45e7fa84d447b12fe6796e23178b4f018e6efa358e52d0f95f1e`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56637b510d4d3e86e2ecb77499b26ff8e2088f282c26dd242728eedc872a221a`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6aab6a99ed6c459097f0a53d453e3d9c667948f0e348eab3c02d3e2063a8e4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8277fb0c5e18c543a480c9980b8cdb815e7a103b1be70ac5dca920b665f2b`

```dockerfile
```

-	Layers:
	-	`sha256:2220ab8b577a4aef4d317e22d7fb49d2a57830d65f928b21891f9b913ef473c3`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 19.5 KB (19504 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5cdff5f8cdc86735cf3884098b25bb98d252d73dbee2fcbb8da0f192bcffba02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57868334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1a7af8983e9d8dedae368516ea89161e2c08ae5fcbe241d8c103c388bc5cec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83fdeaed4a0f5fd1c7da49f735cc0ffc5f2ebe699edb3411c56d4a89dfc789ec`  
		Last Modified: Fri, 14 Feb 2025 12:02:28 GMT  
		Size: 2.9 MB (2928999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b2fcb1e173a7c9c0f213b66e7007b5c1e6640f963db140b7641cb9c82d49d`  
		Last Modified: Thu, 20 Mar 2025 20:51:33 GMT  
		Size: 54.9 MB (54937275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927054ad65fa76f4687ff13459e96e9e2c431c80f35cbd75c8e2a6935801b26`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feee134b9efa4613b0c6af347a8ac2620e23353606389764b1846db5cdcae00e`  
		Last Modified: Thu, 20 Mar 2025 20:51:32 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4ead67a26abaf8fe0d1fb19622d8d14c546e14707461473039106e5208ae281c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7cae3e6c1ee2779eb84c3a428d8285db3addb6a09e7da5c31ac5129738f7f3`

```dockerfile
```

-	Layers:
	-	`sha256:4ddf3e6cd0fb731c535d6dc8b6d3a64b7c0c4dc2d511a6d54ccb1f363f2e9b0b`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 19.6 KB (19588 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ae93dd32a098b75e43257f1233d2da431329b067789195f24e455bbc7bcc9f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70380462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c55ab7ec3face2422bcc229b98c44b77778cf19c2d111eb139bc6c99de8e57c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e341e2e806c5beace803379ac980e67270f064187e8cc3eb2d3d497c640359b3`  
		Last Modified: Thu, 20 Mar 2025 20:50:57 GMT  
		Size: 67.0 MB (67016981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922bc3294fe218e430ef6821ad70f471a5d5623dca0110c170e38c0dc2b5e21e`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa3b8614225790b3a53a681d04efcf6afefbdbdffee3ef2df54fb955e651ddc`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9754f7a97aefd96a8a5083c616d6b696ae8a0a1bcacee125a7281a3ee6ea7d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2bcb3a16f36e11111d6c2196771af075f5cfa77ff4050c4d6d7251a49ec4fe`

```dockerfile
```

-	Layers:
	-	`sha256:a2f3555c80c3b024f6cb3eae0ecc06626ca24716b014f41e1f575a46e99c5b73`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 19.6 KB (19620 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:ed8a3d011fd526ed92bc7fc37bd43253026a1dcc9007f3704aa0d74092a1cfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75675277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce80b46b1d57f82c93ebb8fedc397df0c5e9d73c0f9f4bca30b953f173374ce`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceea9d04caf7123c428cc71b6e189a701c0df9dfb5c4636cdb932a182c5dc92b`  
		Last Modified: Thu, 20 Mar 2025 20:49:18 GMT  
		Size: 72.4 MB (72417773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbf628b09c56f1ed9a9bc0c6c80e30384c1e212514ac6d4320fad560f76154`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68e4e53b91e7a2a0bacd7195519477e580278fbd62ff1e165dc3d26182a5e40`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:095da0d2ed38cc0f3cdd97f259030778e2db708196bbd692ee530528d96fcba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054084cd1ffb8a0cb53a2ebbef0d5b644fb8d8f6af5bbcd46c0dcb8e3bd6a73b`

```dockerfile
```

-	Layers:
	-	`sha256:006e78a4fc563908ab782848ef484c1cd38954fe1d7db867bbd567741a5616d9`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:ed47ea7fca08b1d59646052271e39082656a30391b9d1065e5731d876e174e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71173698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfb1a9773960e2166100bdf78b0094372fe8f1f088fa1ae554461f53db2b632`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fd377eadab07129ae42057b3a16a87aca2e34cc454137b6ad3eebd6472d671`  
		Last Modified: Thu, 20 Mar 2025 20:53:21 GMT  
		Size: 67.8 MB (67805504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81a16e6a322ac046043d3947a2b952f562ed9e6b9a8dcb8d08aeef3ebf1473`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6081bae5b7b1caccd6289bf5cdad31d109060d1b56a9b6e68e48daee158f59`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3603283b01c0481efe5f71fbfdfc61da6c79565d645af850ec154e0b2af60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e9863851dd0104e6518306251bd45cd43ab025a102f8fef257b4017a68d7be`

```dockerfile
```

-	Layers:
	-	`sha256:56107729091864baa86fc11d1a3bd790a74d944f1f8c591da367f65ba5db438a`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:142b451bbc107898e7a43626694442f8d689e862bc76e6658c16a0e3e480c97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65564524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9c3fc8d83faf437103d088d06f0ab28c78071fbc721bfaa507344fb60f4e38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26ca67b2cc4f3c0d15180a19540e9b0a8077bec01f8213e27886b9cbb53750a`  
		Last Modified: Thu, 20 Mar 2025 20:52:03 GMT  
		Size: 62.3 MB (62307641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a98df498d36504153285d47ac06e34aa48bce7cd6649d7d8233f1ae913b56`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172ffc710311115ba888f35e74818e247cfc16ab6e82c0ea1256a68f0adec21`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6d2ff36f410fb69c0d1ab67ef1d8ef8c534c4e9d021da06dbb777f05f1d38670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef5c0271027e9dc11cf1442054efecab44ebdac61c2f31e161f0727b747116e`

```dockerfile
```

-	Layers:
	-	`sha256:6f29dbad55a89c5bf361b46d778edd1d920636239f023fd05dd37b9a502f3816`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.0`

```console
$ docker pull varnish@sha256:3677549b54558d31781d7bc5cf7eedb7dc529c8c2bdd658b5051bee38bddf716
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

### `varnish:7.7.0` - linux; amd64

```console
$ docker pull varnish@sha256:5e582fe889ca8310d2438bbd359daab57ca51b822852380c213c6b757ce95d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134415217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d742f05731972fee8d565fd85b4063c391bd1a581ce6f5fac464be67f98619`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7b4e8561448447b5f17cdf10d16890983d981514d3e05b75afd403b4996105`  
		Last Modified: Mon, 28 Apr 2025 21:57:18 GMT  
		Size: 106.2 MB (106185535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb22ecd6cb33ac30f613868cf419ec33d9f59a3c8730f4ce33ffaf8c3bf64ee`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823c65497a18778874aa28bee2837df9e19da913bf21ba619d9a0e9cf2fc53b5`  
		Last Modified: Mon, 28 Apr 2025 21:57:17 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0` - unknown; unknown

```console
$ docker pull varnish@sha256:b4d10289b86494a80849156633f8e20e092f09cc5390c4d270f0f94c0e574366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b937ebe837f9e47fd72b397157665e81c31d53a1341960b83dbf77c8b73ba8`

```dockerfile
```

-	Layers:
	-	`sha256:af5ca19bbc966bd6ae113c6fb062c2fc3ae349ae26d039823d1d2145154f260c`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c402e70ff618c750e4410ce74a6db1d84900b9e3c3b17f0ec158d091e93acc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104769290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9641fa2fee25c455ea22d4b8e218fcddab8fa85fefcd0e1a0f6a5a9deccde2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9364319ee06ae4bf793ccb5fc25bfd513c692eb71fafb6ac87776949ee3bc100`  
		Last Modified: Tue, 29 Apr 2025 03:30:45 GMT  
		Size: 80.8 MB (80829172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa721a1687c539d9c9a35850d4e20fddb509dbd6956a6cc445c000c70803012`  
		Last Modified: Tue, 29 Apr 2025 03:30:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4041ff56553fd96405a370eec490461068688511cb919ac9b7fac30ffba130d2`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0` - unknown; unknown

```console
$ docker pull varnish@sha256:acdf0d138dd54916c74c1c1ea388a7030e5b4d097f444af960939582d45911fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ac5243e35371d10811891153007e8d691ea5583b0e6f7d76de7adfe58ffeea`

```dockerfile
```

-	Layers:
	-	`sha256:8674f207a0c369f9b69dd03060109a0130b0e8e16aa45c114de5512badf6bf19`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e14d12b67892d1a28aa7f4b76eb3c271aba73ad7815838bb0e64a98727c8fec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128717070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9d429f1d4a98fe900ea9c5dbaf87edab863c532203908094cfc71aa41a8b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f15d75e39de09fd0b81df4c7a488430e737e8b13bcc87349e672b54f6dfe0`  
		Last Modified: Tue, 29 Apr 2025 01:41:44 GMT  
		Size: 100.6 MB (100648406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2beda40612114f7b4e72b251f4e11ef46cfe9b526c8b8c8f91ab637b94e5e4e`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907bb59a11ef4a09e17a8bfd536e895f54a6aa41dfc6ab16e303bf5d85fb05d`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0` - unknown; unknown

```console
$ docker pull varnish@sha256:7c4fbd9538c71f1e43a5917239e7a6a06e5ca22ec225138afd4be8cf287f3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfa568f8a6779d61b60d9de5199c559340fe5d6b4848e7e9760269c82229212`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c6f1e11c15ae9323f4854c423f6734d033a88917973b673de74478be0c8fc`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0` - linux; 386

```console
$ docker pull varnish@sha256:12e085143d06fd1f852cc6e44ca2fcfc92a2c1c3ff25edb7b26bcb022e89f567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131508706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44bd4d23a67aa97268702362f0f8e033489d29f2b889668c4e6cfd6cac30b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b0acd2647e8753d66ff4f8e9283a0e95cbd8d1b4a074e3587232c2c84fe5`  
		Last Modified: Mon, 28 Apr 2025 21:55:26 GMT  
		Size: 102.3 MB (102295800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2693aef1f511398eb6ddf46822cf63cfbff6525e42d286ef7709c4eff63d9f45`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901bd6790d92b32002940e613c07c22254557b4a9986d92deda977a97eee74b`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0` - unknown; unknown

```console
$ docker pull varnish@sha256:b5a68cfe963088ffd67f5e2047080feb3e01c5d362ed65d6a2af9a381cdb043a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f1f91bec453456dd78729905045a12be8b3e823090abd36546cc3bbdad60a4`

```dockerfile
```

-	Layers:
	-	`sha256:c6c6cd5add8cac6fe641c8ebd9e866072721b41e52effcfad7b52262602f33a1`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:57413efcd46c2d2a269e5b6d7d281e75df5295d8822fdbd43a1403856eae3eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137197788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab9a7c1f01651ce6374b1794bfdedaeedd17365045cc956c7ed4c15ba1a127`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a9ff1699f2e910d7dc5b9eb4faec71a66c0dec32a6f666c86161ca4116c29`  
		Last Modified: Tue, 29 Apr 2025 00:27:59 GMT  
		Size: 105.1 MB (105127296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68d270a371be1ef6a95992cbe1367f2c489a0d60ac1d6cc43799b41a75b43f1`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22dc480c2d31d38f0f5126e1899429c2a2f57e076a48a30ae50fd54f5368`  
		Last Modified: Tue, 29 Apr 2025 00:27:56 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0` - unknown; unknown

```console
$ docker pull varnish@sha256:798748a8668f2d191df9a0ddead23e04595d4d6b3d7e86384e3e1235fa9e9992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0d05f566163ef49c04c513870aa065a234685892985d1d2ab675fb29c1462a`

```dockerfile
```

-	Layers:
	-	`sha256:716b65325abd64c3e8d0d7d53a0ec58a4bb4a8a239e59e9108887a92624f9b3f`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0` - linux; s390x

```console
$ docker pull varnish@sha256:00922e2886c9708ebd0398bec71a14a080323bd372e07086d071353267955acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112320868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474b3921d4cbde7bc1762576743522e68cd31f960e959a37f610d2ea2dd1abc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3117e4cac62b98179e474b41ecff263277909443424fde57be72cc3c4b458a49`  
		Last Modified: Mon, 28 Apr 2025 23:56:17 GMT  
		Size: 85.4 MB (85433954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad77db3e5534bad6736406965e8a8a9a47defa03a530c5185e0b8efedb7536c`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87d84786ca3a0a3b8613a9ab75e1f8a8f33d1a43c98523f30a3a0e1743783d`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0` - unknown; unknown

```console
$ docker pull varnish@sha256:d19a0fd1b9dd1c1507c14b5a37daef2f02777fab5602c97d6b27147d5e38dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b385edcff1a6bfa467177b3c3b6d5b98f2fabf1cbbbdd697615b8da2e322de9f`

```dockerfile
```

-	Layers:
	-	`sha256:f3c18d363652d564de4601374b57093fbcdd554ed35713f5db6392f8dcb5bb47`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.0-alpine`

```console
$ docker pull varnish@sha256:d62e5a73fe9928aae297c1cab31d3d602c6e71863dca69ff3daa03f6d9948dba
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

### `varnish:7.7.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:d7e148ec7d3a887e2ffc8aec14aaebc6eb169fc48995eabb29882fc6988c2fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73660932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bc8783b318613ff3297d2e84859d2839c1d064ef286021173e84302d003a94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6197199357be88819ed2d1d3f2a78e9f03de447def19ba8e7a1e4facfe53d0`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 70.2 MB (70238008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46db07dd06f45e7fa84d447b12fe6796e23178b4f018e6efa358e52d0f95f1e`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56637b510d4d3e86e2ecb77499b26ff8e2088f282c26dd242728eedc872a221a`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6aab6a99ed6c459097f0a53d453e3d9c667948f0e348eab3c02d3e2063a8e4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8277fb0c5e18c543a480c9980b8cdb815e7a103b1be70ac5dca920b665f2b`

```dockerfile
```

-	Layers:
	-	`sha256:2220ab8b577a4aef4d317e22d7fb49d2a57830d65f928b21891f9b913ef473c3`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 19.5 KB (19504 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5cdff5f8cdc86735cf3884098b25bb98d252d73dbee2fcbb8da0f192bcffba02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57868334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1a7af8983e9d8dedae368516ea89161e2c08ae5fcbe241d8c103c388bc5cec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83fdeaed4a0f5fd1c7da49f735cc0ffc5f2ebe699edb3411c56d4a89dfc789ec`  
		Last Modified: Fri, 14 Feb 2025 12:02:28 GMT  
		Size: 2.9 MB (2928999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b2fcb1e173a7c9c0f213b66e7007b5c1e6640f963db140b7641cb9c82d49d`  
		Last Modified: Thu, 20 Mar 2025 20:51:33 GMT  
		Size: 54.9 MB (54937275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927054ad65fa76f4687ff13459e96e9e2c431c80f35cbd75c8e2a6935801b26`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feee134b9efa4613b0c6af347a8ac2620e23353606389764b1846db5cdcae00e`  
		Last Modified: Thu, 20 Mar 2025 20:51:32 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4ead67a26abaf8fe0d1fb19622d8d14c546e14707461473039106e5208ae281c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7cae3e6c1ee2779eb84c3a428d8285db3addb6a09e7da5c31ac5129738f7f3`

```dockerfile
```

-	Layers:
	-	`sha256:4ddf3e6cd0fb731c535d6dc8b6d3a64b7c0c4dc2d511a6d54ccb1f363f2e9b0b`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 19.6 KB (19588 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ae93dd32a098b75e43257f1233d2da431329b067789195f24e455bbc7bcc9f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70380462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c55ab7ec3face2422bcc229b98c44b77778cf19c2d111eb139bc6c99de8e57c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e341e2e806c5beace803379ac980e67270f064187e8cc3eb2d3d497c640359b3`  
		Last Modified: Thu, 20 Mar 2025 20:50:57 GMT  
		Size: 67.0 MB (67016981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922bc3294fe218e430ef6821ad70f471a5d5623dca0110c170e38c0dc2b5e21e`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa3b8614225790b3a53a681d04efcf6afefbdbdffee3ef2df54fb955e651ddc`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9754f7a97aefd96a8a5083c616d6b696ae8a0a1bcacee125a7281a3ee6ea7d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2bcb3a16f36e11111d6c2196771af075f5cfa77ff4050c4d6d7251a49ec4fe`

```dockerfile
```

-	Layers:
	-	`sha256:a2f3555c80c3b024f6cb3eae0ecc06626ca24716b014f41e1f575a46e99c5b73`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 19.6 KB (19620 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:ed8a3d011fd526ed92bc7fc37bd43253026a1dcc9007f3704aa0d74092a1cfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75675277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce80b46b1d57f82c93ebb8fedc397df0c5e9d73c0f9f4bca30b953f173374ce`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceea9d04caf7123c428cc71b6e189a701c0df9dfb5c4636cdb932a182c5dc92b`  
		Last Modified: Thu, 20 Mar 2025 20:49:18 GMT  
		Size: 72.4 MB (72417773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbf628b09c56f1ed9a9bc0c6c80e30384c1e212514ac6d4320fad560f76154`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68e4e53b91e7a2a0bacd7195519477e580278fbd62ff1e165dc3d26182a5e40`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:095da0d2ed38cc0f3cdd97f259030778e2db708196bbd692ee530528d96fcba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054084cd1ffb8a0cb53a2ebbef0d5b644fb8d8f6af5bbcd46c0dcb8e3bd6a73b`

```dockerfile
```

-	Layers:
	-	`sha256:006e78a4fc563908ab782848ef484c1cd38954fe1d7db867bbd567741a5616d9`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:ed47ea7fca08b1d59646052271e39082656a30391b9d1065e5731d876e174e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71173698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfb1a9773960e2166100bdf78b0094372fe8f1f088fa1ae554461f53db2b632`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fd377eadab07129ae42057b3a16a87aca2e34cc454137b6ad3eebd6472d671`  
		Last Modified: Thu, 20 Mar 2025 20:53:21 GMT  
		Size: 67.8 MB (67805504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81a16e6a322ac046043d3947a2b952f562ed9e6b9a8dcb8d08aeef3ebf1473`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6081bae5b7b1caccd6289bf5cdad31d109060d1b56a9b6e68e48daee158f59`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3603283b01c0481efe5f71fbfdfc61da6c79565d645af850ec154e0b2af60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e9863851dd0104e6518306251bd45cd43ab025a102f8fef257b4017a68d7be`

```dockerfile
```

-	Layers:
	-	`sha256:56107729091864baa86fc11d1a3bd790a74d944f1f8c591da367f65ba5db438a`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:142b451bbc107898e7a43626694442f8d689e862bc76e6658c16a0e3e480c97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65564524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9c3fc8d83faf437103d088d06f0ab28c78071fbc721bfaa507344fb60f4e38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26ca67b2cc4f3c0d15180a19540e9b0a8077bec01f8213e27886b9cbb53750a`  
		Last Modified: Thu, 20 Mar 2025 20:52:03 GMT  
		Size: 62.3 MB (62307641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a98df498d36504153285d47ac06e34aa48bce7cd6649d7d8233f1ae913b56`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172ffc710311115ba888f35e74818e247cfc16ab6e82c0ea1256a68f0adec21`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6d2ff36f410fb69c0d1ab67ef1d8ef8c534c4e9d021da06dbb777f05f1d38670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef5c0271027e9dc11cf1442054efecab44ebdac61c2f31e161f0727b747116e`

```dockerfile
```

-	Layers:
	-	`sha256:6f29dbad55a89c5bf361b46d778edd1d920636239f023fd05dd37b9a502f3816`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:d62e5a73fe9928aae297c1cab31d3d602c6e71863dca69ff3daa03f6d9948dba
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
$ docker pull varnish@sha256:d7e148ec7d3a887e2ffc8aec14aaebc6eb169fc48995eabb29882fc6988c2fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73660932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bc8783b318613ff3297d2e84859d2839c1d064ef286021173e84302d003a94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6197199357be88819ed2d1d3f2a78e9f03de447def19ba8e7a1e4facfe53d0`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 70.2 MB (70238008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46db07dd06f45e7fa84d447b12fe6796e23178b4f018e6efa358e52d0f95f1e`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56637b510d4d3e86e2ecb77499b26ff8e2088f282c26dd242728eedc872a221a`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6aab6a99ed6c459097f0a53d453e3d9c667948f0e348eab3c02d3e2063a8e4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8277fb0c5e18c543a480c9980b8cdb815e7a103b1be70ac5dca920b665f2b`

```dockerfile
```

-	Layers:
	-	`sha256:2220ab8b577a4aef4d317e22d7fb49d2a57830d65f928b21891f9b913ef473c3`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 19.5 KB (19504 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5cdff5f8cdc86735cf3884098b25bb98d252d73dbee2fcbb8da0f192bcffba02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57868334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1a7af8983e9d8dedae368516ea89161e2c08ae5fcbe241d8c103c388bc5cec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83fdeaed4a0f5fd1c7da49f735cc0ffc5f2ebe699edb3411c56d4a89dfc789ec`  
		Last Modified: Fri, 14 Feb 2025 12:02:28 GMT  
		Size: 2.9 MB (2928999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b2fcb1e173a7c9c0f213b66e7007b5c1e6640f963db140b7641cb9c82d49d`  
		Last Modified: Thu, 20 Mar 2025 20:51:33 GMT  
		Size: 54.9 MB (54937275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927054ad65fa76f4687ff13459e96e9e2c431c80f35cbd75c8e2a6935801b26`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feee134b9efa4613b0c6af347a8ac2620e23353606389764b1846db5cdcae00e`  
		Last Modified: Thu, 20 Mar 2025 20:51:32 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4ead67a26abaf8fe0d1fb19622d8d14c546e14707461473039106e5208ae281c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7cae3e6c1ee2779eb84c3a428d8285db3addb6a09e7da5c31ac5129738f7f3`

```dockerfile
```

-	Layers:
	-	`sha256:4ddf3e6cd0fb731c535d6dc8b6d3a64b7c0c4dc2d511a6d54ccb1f363f2e9b0b`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 19.6 KB (19588 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ae93dd32a098b75e43257f1233d2da431329b067789195f24e455bbc7bcc9f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70380462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c55ab7ec3face2422bcc229b98c44b77778cf19c2d111eb139bc6c99de8e57c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e341e2e806c5beace803379ac980e67270f064187e8cc3eb2d3d497c640359b3`  
		Last Modified: Thu, 20 Mar 2025 20:50:57 GMT  
		Size: 67.0 MB (67016981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922bc3294fe218e430ef6821ad70f471a5d5623dca0110c170e38c0dc2b5e21e`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa3b8614225790b3a53a681d04efcf6afefbdbdffee3ef2df54fb955e651ddc`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9754f7a97aefd96a8a5083c616d6b696ae8a0a1bcacee125a7281a3ee6ea7d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2bcb3a16f36e11111d6c2196771af075f5cfa77ff4050c4d6d7251a49ec4fe`

```dockerfile
```

-	Layers:
	-	`sha256:a2f3555c80c3b024f6cb3eae0ecc06626ca24716b014f41e1f575a46e99c5b73`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 19.6 KB (19620 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:ed8a3d011fd526ed92bc7fc37bd43253026a1dcc9007f3704aa0d74092a1cfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75675277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce80b46b1d57f82c93ebb8fedc397df0c5e9d73c0f9f4bca30b953f173374ce`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceea9d04caf7123c428cc71b6e189a701c0df9dfb5c4636cdb932a182c5dc92b`  
		Last Modified: Thu, 20 Mar 2025 20:49:18 GMT  
		Size: 72.4 MB (72417773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbf628b09c56f1ed9a9bc0c6c80e30384c1e212514ac6d4320fad560f76154`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68e4e53b91e7a2a0bacd7195519477e580278fbd62ff1e165dc3d26182a5e40`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:095da0d2ed38cc0f3cdd97f259030778e2db708196bbd692ee530528d96fcba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054084cd1ffb8a0cb53a2ebbef0d5b644fb8d8f6af5bbcd46c0dcb8e3bd6a73b`

```dockerfile
```

-	Layers:
	-	`sha256:006e78a4fc563908ab782848ef484c1cd38954fe1d7db867bbd567741a5616d9`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:ed47ea7fca08b1d59646052271e39082656a30391b9d1065e5731d876e174e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71173698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfb1a9773960e2166100bdf78b0094372fe8f1f088fa1ae554461f53db2b632`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fd377eadab07129ae42057b3a16a87aca2e34cc454137b6ad3eebd6472d671`  
		Last Modified: Thu, 20 Mar 2025 20:53:21 GMT  
		Size: 67.8 MB (67805504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81a16e6a322ac046043d3947a2b952f562ed9e6b9a8dcb8d08aeef3ebf1473`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6081bae5b7b1caccd6289bf5cdad31d109060d1b56a9b6e68e48daee158f59`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3603283b01c0481efe5f71fbfdfc61da6c79565d645af850ec154e0b2af60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e9863851dd0104e6518306251bd45cd43ab025a102f8fef257b4017a68d7be`

```dockerfile
```

-	Layers:
	-	`sha256:56107729091864baa86fc11d1a3bd790a74d944f1f8c591da367f65ba5db438a`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:142b451bbc107898e7a43626694442f8d689e862bc76e6658c16a0e3e480c97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65564524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9c3fc8d83faf437103d088d06f0ab28c78071fbc721bfaa507344fb60f4e38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26ca67b2cc4f3c0d15180a19540e9b0a8077bec01f8213e27886b9cbb53750a`  
		Last Modified: Thu, 20 Mar 2025 20:52:03 GMT  
		Size: 62.3 MB (62307641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a98df498d36504153285d47ac06e34aa48bce7cd6649d7d8233f1ae913b56`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172ffc710311115ba888f35e74818e247cfc16ab6e82c0ea1256a68f0adec21`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6d2ff36f410fb69c0d1ab67ef1d8ef8c534c4e9d021da06dbb777f05f1d38670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef5c0271027e9dc11cf1442054efecab44ebdac61c2f31e161f0727b747116e`

```dockerfile
```

-	Layers:
	-	`sha256:6f29dbad55a89c5bf361b46d778edd1d920636239f023fd05dd37b9a502f3816`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:3677549b54558d31781d7bc5cf7eedb7dc529c8c2bdd658b5051bee38bddf716
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
$ docker pull varnish@sha256:5e582fe889ca8310d2438bbd359daab57ca51b822852380c213c6b757ce95d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134415217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d742f05731972fee8d565fd85b4063c391bd1a581ce6f5fac464be67f98619`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7b4e8561448447b5f17cdf10d16890983d981514d3e05b75afd403b4996105`  
		Last Modified: Mon, 28 Apr 2025 21:57:18 GMT  
		Size: 106.2 MB (106185535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb22ecd6cb33ac30f613868cf419ec33d9f59a3c8730f4ce33ffaf8c3bf64ee`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823c65497a18778874aa28bee2837df9e19da913bf21ba619d9a0e9cf2fc53b5`  
		Last Modified: Mon, 28 Apr 2025 21:57:17 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:b4d10289b86494a80849156633f8e20e092f09cc5390c4d270f0f94c0e574366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b937ebe837f9e47fd72b397157665e81c31d53a1341960b83dbf77c8b73ba8`

```dockerfile
```

-	Layers:
	-	`sha256:af5ca19bbc966bd6ae113c6fb062c2fc3ae349ae26d039823d1d2145154f260c`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c402e70ff618c750e4410ce74a6db1d84900b9e3c3b17f0ec158d091e93acc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104769290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9641fa2fee25c455ea22d4b8e218fcddab8fa85fefcd0e1a0f6a5a9deccde2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9364319ee06ae4bf793ccb5fc25bfd513c692eb71fafb6ac87776949ee3bc100`  
		Last Modified: Tue, 29 Apr 2025 03:30:45 GMT  
		Size: 80.8 MB (80829172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa721a1687c539d9c9a35850d4e20fddb509dbd6956a6cc445c000c70803012`  
		Last Modified: Tue, 29 Apr 2025 03:30:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4041ff56553fd96405a370eec490461068688511cb919ac9b7fac30ffba130d2`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:acdf0d138dd54916c74c1c1ea388a7030e5b4d097f444af960939582d45911fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ac5243e35371d10811891153007e8d691ea5583b0e6f7d76de7adfe58ffeea`

```dockerfile
```

-	Layers:
	-	`sha256:8674f207a0c369f9b69dd03060109a0130b0e8e16aa45c114de5512badf6bf19`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e14d12b67892d1a28aa7f4b76eb3c271aba73ad7815838bb0e64a98727c8fec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128717070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9d429f1d4a98fe900ea9c5dbaf87edab863c532203908094cfc71aa41a8b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f15d75e39de09fd0b81df4c7a488430e737e8b13bcc87349e672b54f6dfe0`  
		Last Modified: Tue, 29 Apr 2025 01:41:44 GMT  
		Size: 100.6 MB (100648406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2beda40612114f7b4e72b251f4e11ef46cfe9b526c8b8c8f91ab637b94e5e4e`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907bb59a11ef4a09e17a8bfd536e895f54a6aa41dfc6ab16e303bf5d85fb05d`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:7c4fbd9538c71f1e43a5917239e7a6a06e5ca22ec225138afd4be8cf287f3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfa568f8a6779d61b60d9de5199c559340fe5d6b4848e7e9760269c82229212`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c6f1e11c15ae9323f4854c423f6734d033a88917973b673de74478be0c8fc`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:12e085143d06fd1f852cc6e44ca2fcfc92a2c1c3ff25edb7b26bcb022e89f567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131508706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44bd4d23a67aa97268702362f0f8e033489d29f2b889668c4e6cfd6cac30b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b0acd2647e8753d66ff4f8e9283a0e95cbd8d1b4a074e3587232c2c84fe5`  
		Last Modified: Mon, 28 Apr 2025 21:55:26 GMT  
		Size: 102.3 MB (102295800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2693aef1f511398eb6ddf46822cf63cfbff6525e42d286ef7709c4eff63d9f45`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901bd6790d92b32002940e613c07c22254557b4a9986d92deda977a97eee74b`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:b5a68cfe963088ffd67f5e2047080feb3e01c5d362ed65d6a2af9a381cdb043a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f1f91bec453456dd78729905045a12be8b3e823090abd36546cc3bbdad60a4`

```dockerfile
```

-	Layers:
	-	`sha256:c6c6cd5add8cac6fe641c8ebd9e866072721b41e52effcfad7b52262602f33a1`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:57413efcd46c2d2a269e5b6d7d281e75df5295d8822fdbd43a1403856eae3eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137197788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab9a7c1f01651ce6374b1794bfdedaeedd17365045cc956c7ed4c15ba1a127`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a9ff1699f2e910d7dc5b9eb4faec71a66c0dec32a6f666c86161ca4116c29`  
		Last Modified: Tue, 29 Apr 2025 00:27:59 GMT  
		Size: 105.1 MB (105127296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68d270a371be1ef6a95992cbe1367f2c489a0d60ac1d6cc43799b41a75b43f1`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22dc480c2d31d38f0f5126e1899429c2a2f57e076a48a30ae50fd54f5368`  
		Last Modified: Tue, 29 Apr 2025 00:27:56 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:798748a8668f2d191df9a0ddead23e04595d4d6b3d7e86384e3e1235fa9e9992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0d05f566163ef49c04c513870aa065a234685892985d1d2ab675fb29c1462a`

```dockerfile
```

-	Layers:
	-	`sha256:716b65325abd64c3e8d0d7d53a0ec58a4bb4a8a239e59e9108887a92624f9b3f`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:00922e2886c9708ebd0398bec71a14a080323bd372e07086d071353267955acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112320868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474b3921d4cbde7bc1762576743522e68cd31f960e959a37f610d2ea2dd1abc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3117e4cac62b98179e474b41ecff263277909443424fde57be72cc3c4b458a49`  
		Last Modified: Mon, 28 Apr 2025 23:56:17 GMT  
		Size: 85.4 MB (85433954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad77db3e5534bad6736406965e8a8a9a47defa03a530c5185e0b8efedb7536c`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87d84786ca3a0a3b8613a9ab75e1f8a8f33d1a43c98523f30a3a0e1743783d`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:d19a0fd1b9dd1c1507c14b5a37daef2f02777fab5602c97d6b27147d5e38dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b385edcff1a6bfa467177b3c3b6d5b98f2fabf1cbbbdd697615b8da2e322de9f`

```dockerfile
```

-	Layers:
	-	`sha256:f3c18d363652d564de4601374b57093fbcdd554ed35713f5db6392f8dcb5bb47`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:d62e5a73fe9928aae297c1cab31d3d602c6e71863dca69ff3daa03f6d9948dba
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
$ docker pull varnish@sha256:d7e148ec7d3a887e2ffc8aec14aaebc6eb169fc48995eabb29882fc6988c2fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73660932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bc8783b318613ff3297d2e84859d2839c1d064ef286021173e84302d003a94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6197199357be88819ed2d1d3f2a78e9f03de447def19ba8e7a1e4facfe53d0`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 70.2 MB (70238008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46db07dd06f45e7fa84d447b12fe6796e23178b4f018e6efa358e52d0f95f1e`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56637b510d4d3e86e2ecb77499b26ff8e2088f282c26dd242728eedc872a221a`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6aab6a99ed6c459097f0a53d453e3d9c667948f0e348eab3c02d3e2063a8e4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8277fb0c5e18c543a480c9980b8cdb815e7a103b1be70ac5dca920b665f2b`

```dockerfile
```

-	Layers:
	-	`sha256:2220ab8b577a4aef4d317e22d7fb49d2a57830d65f928b21891f9b913ef473c3`  
		Last Modified: Thu, 20 Mar 2025 20:49:12 GMT  
		Size: 19.5 KB (19504 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5cdff5f8cdc86735cf3884098b25bb98d252d73dbee2fcbb8da0f192bcffba02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57868334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1a7af8983e9d8dedae368516ea89161e2c08ae5fcbe241d8c103c388bc5cec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83fdeaed4a0f5fd1c7da49f735cc0ffc5f2ebe699edb3411c56d4a89dfc789ec`  
		Last Modified: Fri, 14 Feb 2025 12:02:28 GMT  
		Size: 2.9 MB (2928999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b2fcb1e173a7c9c0f213b66e7007b5c1e6640f963db140b7641cb9c82d49d`  
		Last Modified: Thu, 20 Mar 2025 20:51:33 GMT  
		Size: 54.9 MB (54937275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927054ad65fa76f4687ff13459e96e9e2c431c80f35cbd75c8e2a6935801b26`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feee134b9efa4613b0c6af347a8ac2620e23353606389764b1846db5cdcae00e`  
		Last Modified: Thu, 20 Mar 2025 20:51:32 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4ead67a26abaf8fe0d1fb19622d8d14c546e14707461473039106e5208ae281c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7cae3e6c1ee2779eb84c3a428d8285db3addb6a09e7da5c31ac5129738f7f3`

```dockerfile
```

-	Layers:
	-	`sha256:4ddf3e6cd0fb731c535d6dc8b6d3a64b7c0c4dc2d511a6d54ccb1f363f2e9b0b`  
		Last Modified: Thu, 20 Mar 2025 20:51:31 GMT  
		Size: 19.6 KB (19588 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ae93dd32a098b75e43257f1233d2da431329b067789195f24e455bbc7bcc9f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70380462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c55ab7ec3face2422bcc229b98c44b77778cf19c2d111eb139bc6c99de8e57c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e341e2e806c5beace803379ac980e67270f064187e8cc3eb2d3d497c640359b3`  
		Last Modified: Thu, 20 Mar 2025 20:50:57 GMT  
		Size: 67.0 MB (67016981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922bc3294fe218e430ef6821ad70f471a5d5623dca0110c170e38c0dc2b5e21e`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa3b8614225790b3a53a681d04efcf6afefbdbdffee3ef2df54fb955e651ddc`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:9754f7a97aefd96a8a5083c616d6b696ae8a0a1bcacee125a7281a3ee6ea7d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2bcb3a16f36e11111d6c2196771af075f5cfa77ff4050c4d6d7251a49ec4fe`

```dockerfile
```

-	Layers:
	-	`sha256:a2f3555c80c3b024f6cb3eae0ecc06626ca24716b014f41e1f575a46e99c5b73`  
		Last Modified: Thu, 20 Mar 2025 20:50:55 GMT  
		Size: 19.6 KB (19620 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:ed8a3d011fd526ed92bc7fc37bd43253026a1dcc9007f3704aa0d74092a1cfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75675277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce80b46b1d57f82c93ebb8fedc397df0c5e9d73c0f9f4bca30b953f173374ce`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceea9d04caf7123c428cc71b6e189a701c0df9dfb5c4636cdb932a182c5dc92b`  
		Last Modified: Thu, 20 Mar 2025 20:49:18 GMT  
		Size: 72.4 MB (72417773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbf628b09c56f1ed9a9bc0c6c80e30384c1e212514ac6d4320fad560f76154`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68e4e53b91e7a2a0bacd7195519477e580278fbd62ff1e165dc3d26182a5e40`  
		Last Modified: Thu, 20 Mar 2025 20:49:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:095da0d2ed38cc0f3cdd97f259030778e2db708196bbd692ee530528d96fcba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054084cd1ffb8a0cb53a2ebbef0d5b644fb8d8f6af5bbcd46c0dcb8e3bd6a73b`

```dockerfile
```

-	Layers:
	-	`sha256:006e78a4fc563908ab782848ef484c1cd38954fe1d7db867bbd567741a5616d9`  
		Last Modified: Thu, 20 Mar 2025 20:49:17 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:ed47ea7fca08b1d59646052271e39082656a30391b9d1065e5731d876e174e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71173698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfb1a9773960e2166100bdf78b0094372fe8f1f088fa1ae554461f53db2b632`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fd377eadab07129ae42057b3a16a87aca2e34cc454137b6ad3eebd6472d671`  
		Last Modified: Thu, 20 Mar 2025 20:53:21 GMT  
		Size: 67.8 MB (67805504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81a16e6a322ac046043d3947a2b952f562ed9e6b9a8dcb8d08aeef3ebf1473`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6081bae5b7b1caccd6289bf5cdad31d109060d1b56a9b6e68e48daee158f59`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3603283b01c0481efe5f71fbfdfc61da6c79565d645af850ec154e0b2af60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e9863851dd0104e6518306251bd45cd43ab025a102f8fef257b4017a68d7be`

```dockerfile
```

-	Layers:
	-	`sha256:56107729091864baa86fc11d1a3bd790a74d944f1f8c591da367f65ba5db438a`  
		Last Modified: Thu, 20 Mar 2025 20:53:18 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:142b451bbc107898e7a43626694442f8d689e862bc76e6658c16a0e3e480c97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65564524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9c3fc8d83faf437103d088d06f0ab28c78071fbc721bfaa507344fb60f4e38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26ca67b2cc4f3c0d15180a19540e9b0a8077bec01f8213e27886b9cbb53750a`  
		Last Modified: Thu, 20 Mar 2025 20:52:03 GMT  
		Size: 62.3 MB (62307641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a98df498d36504153285d47ac06e34aa48bce7cd6649d7d8233f1ae913b56`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172ffc710311115ba888f35e74818e247cfc16ab6e82c0ea1256a68f0adec21`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6d2ff36f410fb69c0d1ab67ef1d8ef8c534c4e9d021da06dbb777f05f1d38670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef5c0271027e9dc11cf1442054efecab44ebdac61c2f31e161f0727b747116e`

```dockerfile
```

-	Layers:
	-	`sha256:6f29dbad55a89c5bf361b46d778edd1d920636239f023fd05dd37b9a502f3816`  
		Last Modified: Thu, 20 Mar 2025 20:52:01 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:3677549b54558d31781d7bc5cf7eedb7dc529c8c2bdd658b5051bee38bddf716
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
$ docker pull varnish@sha256:5e582fe889ca8310d2438bbd359daab57ca51b822852380c213c6b757ce95d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134415217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d742f05731972fee8d565fd85b4063c391bd1a581ce6f5fac464be67f98619`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7b4e8561448447b5f17cdf10d16890983d981514d3e05b75afd403b4996105`  
		Last Modified: Mon, 28 Apr 2025 21:57:18 GMT  
		Size: 106.2 MB (106185535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb22ecd6cb33ac30f613868cf419ec33d9f59a3c8730f4ce33ffaf8c3bf64ee`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823c65497a18778874aa28bee2837df9e19da913bf21ba619d9a0e9cf2fc53b5`  
		Last Modified: Mon, 28 Apr 2025 21:57:17 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:b4d10289b86494a80849156633f8e20e092f09cc5390c4d270f0f94c0e574366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b937ebe837f9e47fd72b397157665e81c31d53a1341960b83dbf77c8b73ba8`

```dockerfile
```

-	Layers:
	-	`sha256:af5ca19bbc966bd6ae113c6fb062c2fc3ae349ae26d039823d1d2145154f260c`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c402e70ff618c750e4410ce74a6db1d84900b9e3c3b17f0ec158d091e93acc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104769290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9641fa2fee25c455ea22d4b8e218fcddab8fa85fefcd0e1a0f6a5a9deccde2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9364319ee06ae4bf793ccb5fc25bfd513c692eb71fafb6ac87776949ee3bc100`  
		Last Modified: Tue, 29 Apr 2025 03:30:45 GMT  
		Size: 80.8 MB (80829172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa721a1687c539d9c9a35850d4e20fddb509dbd6956a6cc445c000c70803012`  
		Last Modified: Tue, 29 Apr 2025 03:30:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4041ff56553fd96405a370eec490461068688511cb919ac9b7fac30ffba130d2`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:acdf0d138dd54916c74c1c1ea388a7030e5b4d097f444af960939582d45911fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ac5243e35371d10811891153007e8d691ea5583b0e6f7d76de7adfe58ffeea`

```dockerfile
```

-	Layers:
	-	`sha256:8674f207a0c369f9b69dd03060109a0130b0e8e16aa45c114de5512badf6bf19`  
		Last Modified: Tue, 29 Apr 2025 03:30:43 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e14d12b67892d1a28aa7f4b76eb3c271aba73ad7815838bb0e64a98727c8fec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128717070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9d429f1d4a98fe900ea9c5dbaf87edab863c532203908094cfc71aa41a8b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f15d75e39de09fd0b81df4c7a488430e737e8b13bcc87349e672b54f6dfe0`  
		Last Modified: Tue, 29 Apr 2025 01:41:44 GMT  
		Size: 100.6 MB (100648406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2beda40612114f7b4e72b251f4e11ef46cfe9b526c8b8c8f91ab637b94e5e4e`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907bb59a11ef4a09e17a8bfd536e895f54a6aa41dfc6ab16e303bf5d85fb05d`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:7c4fbd9538c71f1e43a5917239e7a6a06e5ca22ec225138afd4be8cf287f3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfa568f8a6779d61b60d9de5199c559340fe5d6b4848e7e9760269c82229212`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c6f1e11c15ae9323f4854c423f6734d033a88917973b673de74478be0c8fc`  
		Last Modified: Tue, 29 Apr 2025 01:41:40 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:12e085143d06fd1f852cc6e44ca2fcfc92a2c1c3ff25edb7b26bcb022e89f567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131508706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44bd4d23a67aa97268702362f0f8e033489d29f2b889668c4e6cfd6cac30b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b0acd2647e8753d66ff4f8e9283a0e95cbd8d1b4a074e3587232c2c84fe5`  
		Last Modified: Mon, 28 Apr 2025 21:55:26 GMT  
		Size: 102.3 MB (102295800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2693aef1f511398eb6ddf46822cf63cfbff6525e42d286ef7709c4eff63d9f45`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901bd6790d92b32002940e613c07c22254557b4a9986d92deda977a97eee74b`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:b5a68cfe963088ffd67f5e2047080feb3e01c5d362ed65d6a2af9a381cdb043a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f1f91bec453456dd78729905045a12be8b3e823090abd36546cc3bbdad60a4`

```dockerfile
```

-	Layers:
	-	`sha256:c6c6cd5add8cac6fe641c8ebd9e866072721b41e52effcfad7b52262602f33a1`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:57413efcd46c2d2a269e5b6d7d281e75df5295d8822fdbd43a1403856eae3eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137197788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab9a7c1f01651ce6374b1794bfdedaeedd17365045cc956c7ed4c15ba1a127`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a9ff1699f2e910d7dc5b9eb4faec71a66c0dec32a6f666c86161ca4116c29`  
		Last Modified: Tue, 29 Apr 2025 00:27:59 GMT  
		Size: 105.1 MB (105127296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68d270a371be1ef6a95992cbe1367f2c489a0d60ac1d6cc43799b41a75b43f1`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22dc480c2d31d38f0f5126e1899429c2a2f57e076a48a30ae50fd54f5368`  
		Last Modified: Tue, 29 Apr 2025 00:27:56 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:798748a8668f2d191df9a0ddead23e04595d4d6b3d7e86384e3e1235fa9e9992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0d05f566163ef49c04c513870aa065a234685892985d1d2ab675fb29c1462a`

```dockerfile
```

-	Layers:
	-	`sha256:716b65325abd64c3e8d0d7d53a0ec58a4bb4a8a239e59e9108887a92624f9b3f`  
		Last Modified: Tue, 29 Apr 2025 00:27:55 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:00922e2886c9708ebd0398bec71a14a080323bd372e07086d071353267955acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112320868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474b3921d4cbde7bc1762576743522e68cd31f960e959a37f610d2ea2dd1abc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3117e4cac62b98179e474b41ecff263277909443424fde57be72cc3c4b458a49`  
		Last Modified: Mon, 28 Apr 2025 23:56:17 GMT  
		Size: 85.4 MB (85433954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad77db3e5534bad6736406965e8a8a9a47defa03a530c5185e0b8efedb7536c`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87d84786ca3a0a3b8613a9ab75e1f8a8f33d1a43c98523f30a3a0e1743783d`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:d19a0fd1b9dd1c1507c14b5a37daef2f02777fab5602c97d6b27147d5e38dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b385edcff1a6bfa467177b3c3b6d5b98f2fabf1cbbbdd697615b8da2e322de9f`

```dockerfile
```

-	Layers:
	-	`sha256:f3c18d363652d564de4601374b57093fbcdd554ed35713f5db6392f8dcb5bb47`  
		Last Modified: Mon, 28 Apr 2025 23:56:16 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:392b7a345bbece3fff16412696879a2e2cd818a38094caaabc880a2999d17b25
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
$ docker pull varnish@sha256:2ff25c0539a93bfaab23560820679eaeead08a20b83d308b5963ca0f134c6440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134223431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7ae0c300b5434fac6efdb73a5f8e42076ff494fda57378adad16f328282b25`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd216553706e69a2f474de76f228faab86ce1125e5940e0609e1bcb1d05581d8`  
		Last Modified: Mon, 28 Apr 2025 21:57:26 GMT  
		Size: 106.0 MB (105993748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37a969703010e8a4205f70a0c873161a902d34c1cc7db02b619698754c21e1`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a02b7a4b892df9ebb3f70c42dd6af257abce9438b514accf626e6b4ba4a585`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:7ca43761a990badfd7465a643026e91bd0bb0c524733cbdfea5d002942c7fe68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d1398c922fc29fd9c65a8134e66bbf3a95d27023888cf7d4840739a12b304b`

```dockerfile
```

-	Layers:
	-	`sha256:f743c3c420c533c168e954a51a9b13cb0069ea8a3301b3dfc5c8e1e7abc3cc01`  
		Last Modified: Mon, 28 Apr 2025 21:57:23 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d10729abf1128e476456659b6430558d63948d73a98989f34a1634e6fe99323b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104605767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2cf92822d35a0b7991aa3e98197a3b57f162654b3bd256224ab9f27da4eb71`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26699162f33b93aaee327495a053e9e73ed91c7f9ef49957cdc41278ac3c0c4d`  
		Last Modified: Tue, 29 Apr 2025 03:33:56 GMT  
		Size: 80.7 MB (80665649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f598f5990a40210d6afe2d8b5ae214ff215d711ace58c837ab456ba1fdcbfdcb`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5564fa94668584067783e080ce6387d24fd607e70905167f6e52e3471ba1792c`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:824678cb3925eacab1c68f38bb8ce743c22782aa17d3f8856f33b801d7a187c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1817272c11a485f4fd3ffb9bc23195d8ad7fb9a19253d1ce02800622d9a6d1d4`

```dockerfile
```

-	Layers:
	-	`sha256:c0508effd86891effe9ba5956cbe4ac5f3bbc1d00518cf15a66313e4ea5d1b73`  
		Last Modified: Tue, 29 Apr 2025 03:33:53 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3d87d6e9107f05b3fdf4faa907da022c409e14e12a41938ed789f5c22d08360c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128546406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec921b50493106c35f93a6b65fce5826e9cf12aa1967010c2e64bf6b6caa56af`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9007928d56da5956c3adb5c9b09cd6052e96eea3d6b32188b18f1abdfafa146`  
		Last Modified: Tue, 29 Apr 2025 01:44:22 GMT  
		Size: 100.5 MB (100477739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec066d9f82de1a6eeab143dcd97003245d1c11b278233dff87c405b260a7d9`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec3524e4e7f30b267be1cfc7a6670001491801c87ba8f2e7c1b0fabe6ac016a`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:622a6360a17e934022c7d4fe24ebf4db904777f9cd490f35c7063b90c47f0117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc7c639574b829cf3f99b393c5c893bbd2196d4faf4e3d8dcd16b1cd384f861`

```dockerfile
```

-	Layers:
	-	`sha256:436db9522c40712324082095c6781b04835223afddf2c628e654f72d30cd7be9`  
		Last Modified: Tue, 29 Apr 2025 01:44:19 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:b316e37e5e0956ddee4d3aedc2dd2dd5364d7fca3587f7b5ab91129f10f7c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131346360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a327fca69bdd4a49b802a99ccb4ce9e7079e679b10498bf79696c9072e97e5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe369bcdf81670933ddffbfb1c2526dd850b10c9bfa6625a6a9ba80b99e6a553`  
		Last Modified: Mon, 28 Apr 2025 21:55:36 GMT  
		Size: 102.1 MB (102133453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07707c37a55d9f43914fbb068753ce52f76bfff997783b74c7de6f820aecf764`  
		Last Modified: Mon, 28 Apr 2025 21:55:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a075088a22133c4633cbe4644976b94ee415685dd6e84eabfa015b5bfc20566`  
		Last Modified: Mon, 28 Apr 2025 21:55:33 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:42dedbcf904216f149eb9f3b3a24cdfdc184259ce9ea3ed64bd1fcbbfede42ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8018d56b0c1e07eab3226f34b2f5195d543d2f954237f87412041940ce4d0b`

```dockerfile
```

-	Layers:
	-	`sha256:01be35c1c45bf9e604c6549165dd929cb56d66baa5bf06d3885791e09b7f5ef5`  
		Last Modified: Mon, 28 Apr 2025 21:55:32 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:c541fd0765cf5296adc92ae9857b103e883ab287effd245f2e2ecf639c29bf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137028796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323add35bc6ea4f4a5a8b204ff25e99ac5ef6bf1e32cdf9e529402da0f3ec3ae`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3193435e4946ec028eeea6d9cd36c97de2d8aadad82e23c06d4d57a7b796eec1`  
		Last Modified: Tue, 29 Apr 2025 00:33:19 GMT  
		Size: 105.0 MB (104958305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87731d847ede151767ec041ca951a73ce8fc086290b136ca26ba4aeccee77c86`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38ed7e15cf5cceec258fb261134dfbd40ea6224996f9008056c03e560e0aa1d`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:ddf964f71b0c0952f1a6bc496153e9a3c48f62055a9e8dea374500f9ad45f5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf6c2ed8342dd48583fd61e8228f2f785985c3dc376f729a9a53d364f22396c`

```dockerfile
```

-	Layers:
	-	`sha256:59ac67029d18279dac18dd817629f21a4aebd2534e7767e7bbee3a31d72ae093`  
		Last Modified: Tue, 29 Apr 2025 00:33:15 GMT  
		Size: 18.9 KB (18884 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:72b074e2f19bc90c53b61eb1c7b69a251b13007f13c842859a439dd59897953b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112144101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b34dabe3364079afbafc0635d712c83c133e66658674f46f2d389f30930d6a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c0afa22588812a685d63f169267aaa819a5d4694e83b7ea954d3e1e0c4da38`  
		Last Modified: Mon, 28 Apr 2025 23:58:57 GMT  
		Size: 85.3 MB (85257186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094ff07e8df96906a4ab6e53b3dc03e09b65b05a7f6d90391ada09d1b2709215`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a7d67eca8d2ce4bc90cb000e30962e8413c6c17486bbfe92ec2942ce141ff1`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:76f330b0e7338efa15c393bfcd33f5e9b99aa7389ade0daea954617684f9c6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e6d6994a8e7c391a4537c6c49733b01d84d2d85ce856e4ff4523dee5470354`

```dockerfile
```

-	Layers:
	-	`sha256:d6425b061c170152fa4451d358ec00bc5665f23f503ac58305c082d6da433442`  
		Last Modified: Mon, 28 Apr 2025 23:58:55 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:889cbd23197112e75773111a63ca342b15ff07c78101b3452df284c1914fcbe8
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
$ docker pull varnish@sha256:cea8646dcc243e71ed9e3d45055c8d4edbb244f62308d85985c76041d3e9a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73503835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7ca24fc498e3f92c1488fd4ff724d5fbdd51ba1572ff7a03c7850c5807b467`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f18e5ee15b30322b340b50363205554d0072c742abc97109ee109af901d70`  
		Last Modified: Thu, 20 Mar 2025 20:49:03 GMT  
		Size: 70.1 MB (70080908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0984719446ab1208d5434dc302aaddb6a50728448133507f6571aecfb9bf2385`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093556cead941ed143ba4d8eae061178a833fcd6a012ccf6fb0587dc2b6df5a7`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:620589ef60655bd95a7224c102279a7e251fd7c93fb34ec70eb376b7849a0a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f7eac1ff2486705ed7ab3703f1975d838c850cd2354a34ebd991788379f4da`

```dockerfile
```

-	Layers:
	-	`sha256:7cf4aaaab0b9957870eeb0d720d0e0e4cfcc99f495e815950d36c3a45705b61f`  
		Last Modified: Thu, 20 Mar 2025 20:49:01 GMT  
		Size: 18.8 KB (18804 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3a68f396e3a33a39d15e7ee577b4d3762d673eb6aee39d798af309d58bc9ba46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57701783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bdd592b48398e853a7e5def2226eea0b3e705e6e6268982d2d29c80359fdf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:83fdeaed4a0f5fd1c7da49f735cc0ffc5f2ebe699edb3411c56d4a89dfc789ec`  
		Last Modified: Fri, 14 Feb 2025 12:02:28 GMT  
		Size: 2.9 MB (2928999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27416bff113d8f24380377ffb42ac39dfdd67b1137b2373b871d39fcd3c426fa`  
		Last Modified: Thu, 20 Mar 2025 20:55:52 GMT  
		Size: 54.8 MB (54770727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db75fcc41dd2a451d7daedc14c136e54985557e45451152b2ca6e63341a8f2b7`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fad2892c6952544d2917b6650809e2994fe1794a5781cf4a291cf48726624c4`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:23989a80ae452da348f6f36847ec90aeb87fa622e1185a542d0968172b962cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735ed7f1d4b3e6c76ab7c0799882d144ab04e77869eea01ceb8efe7560f10e16`

```dockerfile
```

-	Layers:
	-	`sha256:c52cf7abb4f6619880b530088a6f3f9254c8c698b9ef295210e206c791d918a0`  
		Last Modified: Thu, 20 Mar 2025 20:55:50 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3e99b357cfebf29315f5c6c1757e97474ea415d3ecdf9351abc0b6b7bbf0a9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70224522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec791631402f7ae975774f4b6c2fe49a56a44577665ec8f469d911655947971`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314dbe51a23e5aa36e6f06cb8131fb67ce3336f95cce019738e2b56b21edf0b0`  
		Last Modified: Thu, 20 Mar 2025 20:54:54 GMT  
		Size: 66.9 MB (66861043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b9a16fdb9c48c3123dedd60c7e6ba7e0e0962e57068c081b20e444deb8dfcc`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7ffa8106b9714bcdcf65732cd12da3e815e160582e810d0848d4f99ca61ff4`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e9c5c8719e2984189db33d8d8e30ca9672fdc56c95f4b531da4be7212cf6a7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4b22bbdefa389173bb668631bdabf08de9af4bb0dda35baeefc83fc1d46926`

```dockerfile
```

-	Layers:
	-	`sha256:9f9604e2370f4626f35df6ac79eeffd6d362b00f0248799bd606ddd4c2705a3e`  
		Last Modified: Thu, 20 Mar 2025 20:54:52 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:5c791d454d530cd33c23edb3a5138931390382951bb4f8860e8ae77dff0d4c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75520843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757b34fc17bec41eb78d0aa86510a54a70249f736c538898be6c926ff65c07b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105edcac606f410c0a0480d6aa3ba8c697e6849c4e9bacbdbf8edf276e85faa2`  
		Last Modified: Thu, 20 Mar 2025 20:49:13 GMT  
		Size: 72.3 MB (72263339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2146b0b689108a78ccc703c22bed6653e16a9083948bcce183a965e16e0042`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3639f317bd35f20772ffa4d992ca7f78a98979fadab9c48b99cbc1efe98a2165`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d2e530159f245e975e1997f8009298d7c9fe6a05eadca7d7619ae79af1f3d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4710a17a7af83aaf44a8b1ae0756a96a92990e79509ef4cef6ca3b613d0a2b4`

```dockerfile
```

-	Layers:
	-	`sha256:ebdb2b6983834e3a0de138515539bd40e0abe377996086267afca1e52f798936`  
		Last Modified: Thu, 20 Mar 2025 20:49:11 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:cecd5ab036369bc9f93e96b751d336fb5c2e900cd9881569d77d833d2e81f300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71019634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635256b7fcb8cfdda9959ab995354551d8f4f43c7f52ffa3a3ef7cb34899e0de`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dbb81854e57495f319359a216625484e49eda40cc71bbedd331c77a691db03`  
		Last Modified: Thu, 20 Mar 2025 20:59:24 GMT  
		Size: 67.7 MB (67651439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db38eb2c902867cb53b936c6379d20d3a30f98fb468c109e5da24d7059ef0b8e`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687ef06ba3519de4b614d0a1d2680236223054ec3e9cfa088d0d0adccdb7049`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f71c8954ca22f4d38cbdc1c4e6036f80ca96efea432b5e0d90014a7a57dbb567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f4feeaf4c5a7ae7fcc344eff51f6490162ddd1435b36e6e87a06fe15488e59`

```dockerfile
```

-	Layers:
	-	`sha256:526b999ab1be5a288adff6be69eb0a6318ba6df88c93367acc253ca560f9dfd7`  
		Last Modified: Thu, 20 Mar 2025 20:59:21 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:24660accdbdc53f4bb3603c08280b6f6384fb66a0445b39daa0dcb9e58a8cc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65405882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3a59e903c9d2a5a1f9e716fe06b237797002be14d5bbb3d0d080717021f17d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.6.1
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6ed6a11500b4dd92fd1b04a0eefcc30aeee6a545bd70b481dca6a8aa8c28f4`  
		Last Modified: Thu, 20 Mar 2025 20:56:26 GMT  
		Size: 62.1 MB (62149009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af226806eb4379bc9469a0210d5c4a8104803fe0fd7f52e2988b5ccc362dece8`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed42a627c6611b8e149439a43ed94fbdf3aecb62043b5896d7195734c49bd4a`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:85fca3d73c264caa655ec59dfdabbff7897081a02d21c3e588e2f3729fc40aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b547091505d268e8cd358ad6d34098c51ec84f2f08c8ce9e9519ea2ebc5d2aa`

```dockerfile
```

-	Layers:
	-	`sha256:7d07064a5d33392132cfab6a4f816bee701f6e3523f300c70f0b1cc832cb0b57`  
		Last Modified: Thu, 20 Mar 2025 20:56:25 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:f1627a662a4bbb9fc4759202d15162c4a09394230001332dc7b07c5819564314
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
$ docker pull varnish@sha256:ab303565b5539b30566a7b1ad3ebbd005919e85cd486e2e91cb9e942b0906183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545aeccb6abdaf1c10e6010b2922282ac2ad02aa023e16a78a387a9992acd8e7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67648ea82312889df780c03818e66dbda6438f92c80dd7fc872a0edb2ad4e2b`  
		Last Modified: Mon, 28 Apr 2025 21:56:44 GMT  
		Size: 99.5 MB (99515839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dfb8e6b2be6e67c850dc82909d9bfd382718debc0f57a2bff5cb54db58ec9c`  
		Last Modified: Mon, 28 Apr 2025 21:56:40 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:9789645accfe58d663426ad28d1e7d3c81a361d751e869ec31c0d95409ca0b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a904c1a9fd65616e3c7d77ea138356595ba10f715ad084c4a7dce111410cf`

```dockerfile
```

-	Layers:
	-	`sha256:06d28f6084e4496b4f9afaa24aa6e86b3693e1b692552008bbed6912246ac1a0`  
		Last Modified: Mon, 28 Apr 2025 21:56:40 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e05a7d308f600d12c7ca20d67e5829b18b9dc288ec5145730a4242a01ac08f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98288920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5e25f6e59a37a4c69ad5ec874404bd339d6c974c930372b2bd6c61da597e03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afd1e156989368f6e666d38cbcbbddee98d6d589cfab5f656736802bd30d620`  
		Last Modified: Tue, 29 Apr 2025 03:36:23 GMT  
		Size: 74.4 MB (74350094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cc51571a88822dfed8e9892fc6d4a241ceb58cdbdbf185ca8c55f85a7ae48a`  
		Last Modified: Tue, 29 Apr 2025 03:36:21 GMT  
		Size: 720.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:4749c6b8b2d1452c7b84c704abe9f8a3da7f117f1c74607ee09a5b8693e044f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8028707394edfe4d3367ee99486252c3c8ba08c629a6ce3d5be37f859fc735`

```dockerfile
```

-	Layers:
	-	`sha256:30e1cdce869e12ed2dec7c2bab241172b95b06e79c31636ede419b0c9ce35c45`  
		Last Modified: Tue, 29 Apr 2025 03:36:21 GMT  
		Size: 12.7 KB (12732 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ea5690ea35f34ee6c52a90abacbe55ef701bb020e032cfe3a4a017ed4c24941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122359056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b15a3433566c27a95d2fb5d227db18611a58089e00f29cc2a20bf3607ec2e67`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f07bf5498cc53e332bcd52e9c936f3f8c2dacca688722ffc4975b72a0c8a39f`  
		Last Modified: Tue, 29 Apr 2025 01:46:18 GMT  
		Size: 94.3 MB (94291679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfade164f990e3d97229ec2e3b14ded6cd5a50463bb71dae262c06d022ee006`  
		Last Modified: Tue, 29 Apr 2025 01:46:15 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:fec29a8db8167835c3d33c13a53adb187be8ea1137e6437ae8cb7a02670e3d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0add89bfc80390c60bae6a10e97291fa9c4670e89dba05fca30a38e0b906263e`

```dockerfile
```

-	Layers:
	-	`sha256:709bb17f371f9cd6d69c1228e0c6c31cc07e4cf35023cac9a99f4c380ae40334`  
		Last Modified: Tue, 29 Apr 2025 01:46:15 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:baed0f4c518b3031447533c5124da57eef5fb94d48ff34121fbb13353a31a468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124905026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10a158cab887e28dc0310795e865268ef6fab3afa24c4736e534c5511c9bcc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c721a5f1a0287cb31914178d641a48fa6274d52b08210daa2d85721fb41fd546`  
		Last Modified: Mon, 28 Apr 2025 21:54:50 GMT  
		Size: 95.7 MB (95693406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9cb400d85d47cc31734b9480164e0fba4cd9204cdc79694d370b894edb293c`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:c14c4e1400c264fb990b93d9125c09324cb6644dfb9c36cef4e8db41f8227627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c14ae74490207909574666aff7d17fa462f1c628ecd4a652aa619ce851273b0`

```dockerfile
```

-	Layers:
	-	`sha256:6377d9af43befec53fe4750bbebf4a1b9af0a7dbc30b6c9fe8b5649be6a94ab3`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:2ab2742df42e389b2d99b9b98f5d0f204cd5b2815db1d6ca1650f4b455f0612e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130405865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62af1c76c0e8c751881da24bbc76d605b15bfd206b20210b19c7f53737347323`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f1df676d0d3abc4949bfa1dea6269425b20479a4c559d02450410f90cd7f49`  
		Last Modified: Tue, 29 Apr 2025 00:37:38 GMT  
		Size: 98.3 MB (98336669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ed85d7bbb179a43d80cde46090f4332590ab823c91852bd65014a4918c9a67`  
		Last Modified: Tue, 29 Apr 2025 00:37:35 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:fdf5528c67d68405073265decbd118edaf02082ced8c7eefdbc36d7fee9f306d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63c1819b6d2fd1c6160178365c3036888a57785713559bc742dd2fe94c9d8b6`

```dockerfile
```

-	Layers:
	-	`sha256:d34991ca2d68b135ab293a3bf02619ec2939d20786a7f44f725cd251b448561c`  
		Last Modified: Tue, 29 Apr 2025 00:37:35 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:7828527c1d0af8f5746ee8a3a008886eb1c022ac7740f333e730654c7dec6335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241cc916ed898550243ebba83f6e9b75ccafa64071888671514deccace37cc3d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 25 Dec 2024 01:40:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be33dfb4c49615e8253f2ebdbbedfbabd730fd663917126ea31c212a55796a0d`  
		Last Modified: Tue, 29 Apr 2025 00:00:47 GMT  
		Size: 78.7 MB (78743483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7559210d805dd5af9d8a51a6b402e5cca6457dbd86b11500e5e0bfb120ff7204`  
		Last Modified: Tue, 29 Apr 2025 00:00:46 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:56e40c2e20a892c4d5bb11fab3f28806328e2c40dc20a84193b7020992309cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395ef4d628ed77d9861592b9ebbf10acc9001c96b583f74f6da217bf41dc519a`

```dockerfile
```

-	Layers:
	-	`sha256:396878abb84adc7edba33dd84d36dd0cd0abcd7a097e67e6fa7f5353933fe50e`  
		Last Modified: Tue, 29 Apr 2025 00:00:46 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json
