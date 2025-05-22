<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.14`](#varnish6014)
-	[`varnish:7`](#varnish7)
-	[`varnish:7-alpine`](#varnish7-alpine)
-	[`varnish:7.6`](#varnish76)
-	[`varnish:7.6-alpine`](#varnish76-alpine)
-	[`varnish:7.6.3`](#varnish763)
-	[`varnish:7.6.3-alpine`](#varnish763-alpine)
-	[`varnish:7.7`](#varnish77)
-	[`varnish:7.7-alpine`](#varnish77-alpine)
-	[`varnish:7.7.1`](#varnish771)
-	[`varnish:7.7.1-alpine`](#varnish771-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:e02631edbd9d11b0a469dc692fcc2c02df253e2ad2b462bfd2c673e1a26c56b7
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
$ docker pull varnish@sha256:f53b607d8fbeaf3b2965bb9a21f21ac15b5e019cf1adf36a78345258f242683c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f6da4b8adb77c3151c2bf7f5905b9636d09b2c4e1c1a962ad4217f98cc826c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238b18ac43560146d207c70490bece959b1bd7136aaa73401ce701ffb9bcc00`  
		Last Modified: Wed, 21 May 2025 23:22:00 GMT  
		Size: 99.5 MB (99518441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b473f68ca08352ea6bd1b9ec160db2cad3996f649dfbffafd7342553f3214e`  
		Last Modified: Wed, 21 May 2025 23:21:53 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:6972ed59c52893951900efe0d2a733ef7147a6da5b92242ffae5b5c36289a8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344aa08bd59f0208e0df8e7f1b4ca36dcc37aebf6e17777aaa4cf8d50a52b662`

```dockerfile
```

-	Layers:
	-	`sha256:a878b1e3d527f3802b44f7444bc605efe0ed647ababbac29be9db00f09677633`  
		Last Modified: Wed, 21 May 2025 23:21:53 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4d61dd84dea5fbc2c947c036bab3c341b2450b15e0c534c22984862dab2b73ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98274408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377625a439ab30859fa91034c1e9db518ab21b522a1ef66dfabfb71331ea02c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd34f616817a66c7206e8aec9dfe10604efb19a7a1452e939f4907689517b77`  
		Last Modified: Thu, 22 May 2025 02:27:18 GMT  
		Size: 74.3 MB (74340734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f263be4914f430a97cea2ca9bb05fee17a2b2d0a7f0cb3e435de87d04f7dd2c`  
		Last Modified: Thu, 22 May 2025 02:27:15 GMT  
		Size: 720.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:eae52885341d740b1cf17b763287aaa5f9dbddd81703f25b5344f0b2540e41e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b96b1060bb82b49993bf24fd8248e3004cd2053bd5cc5899d4f59fa437a00c`

```dockerfile
```

-	Layers:
	-	`sha256:f79f175fcfc04b47a05edf164e0fdd4e41519cff560ee36e160889e0cde6c68a`  
		Last Modified: Thu, 22 May 2025 02:27:15 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:23a968c01d282408a77e8198e94b2b44458d29d8f9aae33a80711bf7c7ee9377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122381016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8983e6c89348fdf4ff8cca4dac8200ff62b733d32a04672998cb633a37048c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10aeb6b7f48e4a7c5a5414b5dd6194ebb7f1f3efe2b98f602c29056608722dd`  
		Last Modified: Thu, 22 May 2025 02:46:51 GMT  
		Size: 94.3 MB (94314982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fba76c616734d324ddfe18e475795d32353cfbfd51fa3472f4d03c0ac58b47a`  
		Last Modified: Thu, 22 May 2025 02:46:48 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:2373fe0925df778658a1326d6ee59fad2bf302c7695720206d2b4ce52a6d7c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33be93909afdd4226908932632552ed2715be579068b72591b2a5e5e26e62db`

```dockerfile
```

-	Layers:
	-	`sha256:de85b8ca851879f11bdcf84c9575e0e885c36e2b7f819a76821be96619159c2c`  
		Last Modified: Thu, 22 May 2025 02:46:48 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:4d8954e4be622564882c2572d4be864845b05684bf66328c56c0c57c4d1dabec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124908579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61edd70e79541d3ea796b62ae52a3db383964009a9c0d8b5d3f29d750c6104b6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76b2de6c1cd22ab5564b1df01c1391f959c84b557d26d611f761b6e1925490`  
		Last Modified: Wed, 21 May 2025 23:20:55 GMT  
		Size: 95.7 MB (95700339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940c9819b00cb793425d8fc4a9fd18f97dacb286e88c676fa021e581add8b937`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:6ea5ed35179185a8fed81b68fd5b038009d80595951a10d2c7b76e6020c5432b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244cf4053f351a54ff8b2e2f6d0e27ec3f4cde67bfe1d3ef98eb75d328f8f61c`

```dockerfile
```

-	Layers:
	-	`sha256:9e12afc6d20c0f5d9893d474fe57bf0985dbaaba510709a544752083c2164afb`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:34447fca426a5d5fe08b9f8e9a1ecde2c4ec456200349bd81af272776473daf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130417116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a33d29837032baae03a73cdef6f3cdeebf2b023e209d1362ba70d2feb8ab45e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ddc7fd38cef02cc6c6fc6a5fc5c32d3b3b93dff5dd6e58a4ae35db96d93eb`  
		Last Modified: Wed, 14 May 2025 00:05:05 GMT  
		Size: 98.3 MB (98347918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31a65db2dd65a79300357dbea9a209652f91fdaeabd0861156cbb96fb53bd81`  
		Last Modified: Wed, 14 May 2025 00:05:02 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:b73ca8ea1d6d380fba641683fcc179d9ad1a94b69ba76e2051d50aeae0318bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fb8cec5bb9a7fa54d8fdb676a975e2740ccf004d4601bafb4bbf5bcb239a26`

```dockerfile
```

-	Layers:
	-	`sha256:c6bf3f06141a8df1e36083cb4dd00321da8372b285a3647953a8dfcfcf75fa78`  
		Last Modified: Wed, 14 May 2025 00:05:02 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:2a5e512d2ad441521129b845d46d80255b2ae0936909068062a476b04918c249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105623860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e03ee5fe6c9edb5086346089f27d6cdafebc57aa1dc6ed83ba60e61a01803`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce50e919b295f01d51d4e557f761ea2540b245fdbf5c80e8dd4f5efc4c3358e`  
		Last Modified: Thu, 22 May 2025 01:01:15 GMT  
		Size: 78.7 MB (78740299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec345b4d9f127d20b425df582f3136695d5deb850d7692520f52f62d0068a7`  
		Last Modified: Thu, 22 May 2025 01:01:13 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:8ecd2a0591197a879c4401602eb8812b6a07db8cfe143d13067dd65825440bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872cde2c29a3c2394016bd5fd1ac8f90a04bc2fd2c669487b16a9ab00e7d96d6`

```dockerfile
```

-	Layers:
	-	`sha256:57f9f532bed20d2dbff835d4b678d8968eb1512eafcf1d6fbc12ca96fa5904f3`  
		Last Modified: Thu, 22 May 2025 01:01:13 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.14`

```console
$ docker pull varnish@sha256:e02631edbd9d11b0a469dc692fcc2c02df253e2ad2b462bfd2c673e1a26c56b7
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

### `varnish:6.0.14` - linux; amd64

```console
$ docker pull varnish@sha256:f53b607d8fbeaf3b2965bb9a21f21ac15b5e019cf1adf36a78345258f242683c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f6da4b8adb77c3151c2bf7f5905b9636d09b2c4e1c1a962ad4217f98cc826c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238b18ac43560146d207c70490bece959b1bd7136aaa73401ce701ffb9bcc00`  
		Last Modified: Wed, 21 May 2025 23:22:00 GMT  
		Size: 99.5 MB (99518441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b473f68ca08352ea6bd1b9ec160db2cad3996f649dfbffafd7342553f3214e`  
		Last Modified: Wed, 21 May 2025 23:21:53 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:6972ed59c52893951900efe0d2a733ef7147a6da5b92242ffae5b5c36289a8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344aa08bd59f0208e0df8e7f1b4ca36dcc37aebf6e17777aaa4cf8d50a52b662`

```dockerfile
```

-	Layers:
	-	`sha256:a878b1e3d527f3802b44f7444bc605efe0ed647ababbac29be9db00f09677633`  
		Last Modified: Wed, 21 May 2025 23:21:53 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4d61dd84dea5fbc2c947c036bab3c341b2450b15e0c534c22984862dab2b73ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98274408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377625a439ab30859fa91034c1e9db518ab21b522a1ef66dfabfb71331ea02c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd34f616817a66c7206e8aec9dfe10604efb19a7a1452e939f4907689517b77`  
		Last Modified: Thu, 22 May 2025 02:27:18 GMT  
		Size: 74.3 MB (74340734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f263be4914f430a97cea2ca9bb05fee17a2b2d0a7f0cb3e435de87d04f7dd2c`  
		Last Modified: Thu, 22 May 2025 02:27:15 GMT  
		Size: 720.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:eae52885341d740b1cf17b763287aaa5f9dbddd81703f25b5344f0b2540e41e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b96b1060bb82b49993bf24fd8248e3004cd2053bd5cc5899d4f59fa437a00c`

```dockerfile
```

-	Layers:
	-	`sha256:f79f175fcfc04b47a05edf164e0fdd4e41519cff560ee36e160889e0cde6c68a`  
		Last Modified: Thu, 22 May 2025 02:27:15 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:23a968c01d282408a77e8198e94b2b44458d29d8f9aae33a80711bf7c7ee9377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122381016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8983e6c89348fdf4ff8cca4dac8200ff62b733d32a04672998cb633a37048c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10aeb6b7f48e4a7c5a5414b5dd6194ebb7f1f3efe2b98f602c29056608722dd`  
		Last Modified: Thu, 22 May 2025 02:46:51 GMT  
		Size: 94.3 MB (94314982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fba76c616734d324ddfe18e475795d32353cfbfd51fa3472f4d03c0ac58b47a`  
		Last Modified: Thu, 22 May 2025 02:46:48 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:2373fe0925df778658a1326d6ee59fad2bf302c7695720206d2b4ce52a6d7c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33be93909afdd4226908932632552ed2715be579068b72591b2a5e5e26e62db`

```dockerfile
```

-	Layers:
	-	`sha256:de85b8ca851879f11bdcf84c9575e0e885c36e2b7f819a76821be96619159c2c`  
		Last Modified: Thu, 22 May 2025 02:46:48 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; 386

```console
$ docker pull varnish@sha256:4d8954e4be622564882c2572d4be864845b05684bf66328c56c0c57c4d1dabec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124908579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61edd70e79541d3ea796b62ae52a3db383964009a9c0d8b5d3f29d750c6104b6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76b2de6c1cd22ab5564b1df01c1391f959c84b557d26d611f761b6e1925490`  
		Last Modified: Wed, 21 May 2025 23:20:55 GMT  
		Size: 95.7 MB (95700339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940c9819b00cb793425d8fc4a9fd18f97dacb286e88c676fa021e581add8b937`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:6ea5ed35179185a8fed81b68fd5b038009d80595951a10d2c7b76e6020c5432b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244cf4053f351a54ff8b2e2f6d0e27ec3f4cde67bfe1d3ef98eb75d328f8f61c`

```dockerfile
```

-	Layers:
	-	`sha256:9e12afc6d20c0f5d9893d474fe57bf0985dbaaba510709a544752083c2164afb`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; ppc64le

```console
$ docker pull varnish@sha256:34447fca426a5d5fe08b9f8e9a1ecde2c4ec456200349bd81af272776473daf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130417116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a33d29837032baae03a73cdef6f3cdeebf2b023e209d1362ba70d2feb8ab45e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ddc7fd38cef02cc6c6fc6a5fc5c32d3b3b93dff5dd6e58a4ae35db96d93eb`  
		Last Modified: Wed, 14 May 2025 00:05:05 GMT  
		Size: 98.3 MB (98347918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31a65db2dd65a79300357dbea9a209652f91fdaeabd0861156cbb96fb53bd81`  
		Last Modified: Wed, 14 May 2025 00:05:02 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:b73ca8ea1d6d380fba641683fcc179d9ad1a94b69ba76e2051d50aeae0318bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fb8cec5bb9a7fa54d8fdb676a975e2740ccf004d4601bafb4bbf5bcb239a26`

```dockerfile
```

-	Layers:
	-	`sha256:c6bf3f06141a8df1e36083cb4dd00321da8372b285a3647953a8dfcfcf75fa78`  
		Last Modified: Wed, 14 May 2025 00:05:02 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; s390x

```console
$ docker pull varnish@sha256:2a5e512d2ad441521129b845d46d80255b2ae0936909068062a476b04918c249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105623860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e03ee5fe6c9edb5086346089f27d6cdafebc57aa1dc6ed83ba60e61a01803`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce50e919b295f01d51d4e557f761ea2540b245fdbf5c80e8dd4f5efc4c3358e`  
		Last Modified: Thu, 22 May 2025 01:01:15 GMT  
		Size: 78.7 MB (78740299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec345b4d9f127d20b425df582f3136695d5deb850d7692520f52f62d0068a7`  
		Last Modified: Thu, 22 May 2025 01:01:13 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:8ecd2a0591197a879c4401602eb8812b6a07db8cfe143d13067dd65825440bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872cde2c29a3c2394016bd5fd1ac8f90a04bc2fd2c669487b16a9ab00e7d96d6`

```dockerfile
```

-	Layers:
	-	`sha256:57f9f532bed20d2dbff835d4b678d8968eb1512eafcf1d6fbc12ca96fa5904f3`  
		Last Modified: Thu, 22 May 2025 01:01:13 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7`

```console
$ docker pull varnish@sha256:86e8b8945266a860db142a641b60e919a34eda77f929a51be888b70d41bf6324
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
$ docker pull varnish@sha256:977ab78dc31ecbec4285eced93daf2391dc232d1ee452987a7c1740e902e9973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134432559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffb297b8223b1aae9fe862b8a03a6020f97a7fa4d8dae2134ba59518fcb7f84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ba1e050e4fcf7680bef6d92b2df063c4e527e294143a153dc00f28052a2176`  
		Last Modified: Wed, 21 May 2025 23:22:38 GMT  
		Size: 106.2 MB (106205179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da93242d1418a17c24960555b296029f7b8098770d10353a2e8c308970676138`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef390b256376ce19bd47ce3e975bf48d8d3f6bc71a7c31905c0fed7fc2059d13`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:1e0a03226641f48fdaba83cee24a1cb8e2a8f4827e2ca6f8902508550d83c03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414c6f46ac564e1a77e8f8ef21a1e32c4e2b3c32c7cbee7b00f9f25b8eb101b1`

```dockerfile
```

-	Layers:
	-	`sha256:3e2476437e1f9fe6c21db7b9d507881f836a784072f8c11c79dc9cd63d1f10fb`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 19.4 KB (19446 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c773ab683f23d2cd79e06d85d02996b2b01924bf328e3666f5f9b341cbfd0d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104785075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba66129a0dbe6f325051712cad928cbe8ad18e5800c4efdd574286e9d69f6fe0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac458455152571434f9a6c7df061f113f5a5c2068aef467ef345ac392b3897d6`  
		Last Modified: Thu, 22 May 2025 02:21:50 GMT  
		Size: 80.9 MB (80850108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb358afb88ae9a9c8149e8291ed8f719db1db6307b98ba3ba7e90000641a6b`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a7b99352f7ce860abc258d20d7bb084554b2ebe5306fad771ccb4aed6320fe`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:6c0d75b8f70c4a9a4025686d21d55ce66ae618432ae4923e0934e23a4c42b1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf627a5ab1f86c4df615ef35dcbe4227898c6ba005d21a0afe7bbac56015fa9`

```dockerfile
```

-	Layers:
	-	`sha256:480b751b13fe5c2f25340d8151c8ed61eb8722e2ab491566e35a7f7cdaf3f6f1`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1aad1b68dd84a97f68d7c89f793d30650db73f655ae9dd0f6f0268bcc13217b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128756188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade40f2aed6c3219ad502e0110acbf89f344b37f32f6ecd9bc36aff5244552f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b17e29ac9e54e576cb04765200626525f96dc401ab614bbc54eb2145157550`  
		Last Modified: Thu, 22 May 2025 02:42:08 GMT  
		Size: 100.7 MB (100688867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e3bb5152055b2725c6ebad6b01752877a4e804b3d8d3af8e16c7590878fe9a`  
		Last Modified: Thu, 22 May 2025 02:42:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a02a085b2688630644cda4682d17d517bc18e61f70125f6690207bb155419d`  
		Last Modified: Thu, 22 May 2025 02:42:04 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:757e93b0ee017bac182544700626a8ae26fcc93799faa6c610d43e5580cdc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ccce5ff2d796096453bef1cde02b0fc8a7fd864e105a6531e44d296d252583`

```dockerfile
```

-	Layers:
	-	`sha256:6afbcf3ccb160b6b79a88ff94546bbfde4ce05798cf2a0a00468afe4d224a23c`  
		Last Modified: Thu, 22 May 2025 02:42:05 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:459840cdaddcf109cc22f4a13e60eb13eec8078c2751263020b63e58ca3d3ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131537851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4345e460a9ec1a61a6167b276d59f12f88fa841eaef97898deefbeea756927`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0e1b7420750c7ad80b73bb0b5a38934c0b3d489b169108888796b0eb517e3`  
		Last Modified: Wed, 21 May 2025 23:22:23 GMT  
		Size: 102.3 MB (102328321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e36adf8a72f5214761c46f62dba51ea501386ecc7aee9df878eba645b927fe`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b2b528b3cc25073c565cb06deb12e3186235fb0a4c80de54b28ec663757f12`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:c1e8cd6066a3a7368c1f86e6f3a470eec4dbff018fcb14e2f84814a0f6c99c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b84d414ffbffca90b934a952a0da6bb34f54db530a1b904e79c493b59554354`

```dockerfile
```

-	Layers:
	-	`sha256:4cf8b13efc417a94e0f8d146bad31193adeadee7a679411e5e12d6207c259261`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:7d7d355b21c251e67d9b9e85a8f288363a9ad60560a971151378e43846668456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137233020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7b5b5e39554dc9f66a02e3c59fb3371f8678ecfa05941f93381870f6a36d2f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85372ffb9150cd3a320a4bc44ed4b2cdc019a9a1ecb70a111b384220d6116a1b`  
		Last Modified: Tue, 13 May 2025 23:51:11 GMT  
		Size: 105.2 MB (105162529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a8da1e97e0a49a6694eec4aa254842ac3589188d9ef503a15a2c2b9bd4c3be`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e61219f2f71de9614f1131b9292d43311eadd8e856d2a632f6fc28a3d50e`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:fc1ae7f7739a94a83065ee6d28e6def85a575001f37a0dbf579ee9c9091bbdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ff9e1f324990faa5d0bda41d3f97f8c3b02d2a61946c8e69aaba79da6e5566`

```dockerfile
```

-	Layers:
	-	`sha256:92ab709f19228dcc9118cedda83d251b2febd005f9493709cdc69e156b4fa576`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:2455f1bc08cbcce52d13fe8aafd3078ffe19fb13954051b395d676273e061f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112354777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694c9e09bf81a75334ff9be6cb3bdd4937b9c1791d01fc9ddce1e8b34326bda2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8299d63723e54463fad083282a50370c22bd894ca037870414a61da1b81a3daa`  
		Last Modified: Thu, 22 May 2025 00:56:32 GMT  
		Size: 85.5 MB (85469923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e21687c812f9934edcfcf1ce07fdbf0c291d184931706496aa49a657e7e794`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51af249f25615e77d6502237bcdee426a95a9e5649761460f178dc5b2fdfe188`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:573a4860c5f251faa947595939b5729f0b0d3fb703e20a598344ce017b44fa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7ec93bc1a67bbaaa5d04f82e69b77595dd5fd0e67ff7c8cb0bb321e30a2d26`

```dockerfile
```

-	Layers:
	-	`sha256:e10caa24f54ad7e91b672430ede572bba41c6b63b5a52bcd4da125bead791f83`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:edbb3bc7c0d80e0222c416c709b09a73ccd2df1cdae3866c7322a241eff4e180
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
$ docker pull varnish@sha256:259b86a44377185dba18240d733380c541601d25d666b2e9ba9acd577c4dcf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80309670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b284e6450b0b02b8aa6c5ced28b66e12656ba744baa00edecb76fe116c080556`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d09d2ebf1afc734637d3674346c53f56296aec75a61edd0c0344cf312eebb8a`  
		Last Modified: Tue, 13 May 2025 23:47:47 GMT  
		Size: 76.7 MB (76665367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020865b6f7518b5553fb3b5f5f87fe7d769c0bfd8862be571713f33c02335d57`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0716d6cccd5a8c846bee76362aae17be1826d27994c5806f1ce07585b70ff59`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ef0ab02e38b644a555096be9157be1cea81d90cc0f8de591ccb819b98940f00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b8aea16b52858945e38eec85b802ca5db8803f2036a627d258530547fe08c7`

```dockerfile
```

-	Layers:
	-	`sha256:bc90243747f045b359a650c8909062b2318c1499e7f48a798167cbfc7657f381`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8d292ee45a9dc2dfbfed35458b8fa0270f85040da8ee21207a334d4775d8380f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eaef00bc440210de5afb83262c54f02d0ec3c76d7ce72305a6cc82dc53aa03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20465a10cb0623d2638bae875b058ba3f793638be7cb92415040e000c1b76f8`  
		Last Modified: Tue, 13 May 2025 23:50:11 GMT  
		Size: 59.3 MB (59261224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083ea808ed9381df01328a2ef1653df216e9b4da36244e4dcadd17dcdf6e84a`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8794d458a0b8f646fc60add26e4459b4d4c9407b50280e428511293a11520f`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e91eaeeb5f0182b467108b50d78b5afa1b3a461e88852279d5862ea5cfa76cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179782e695fe7a93dca563aee6b50b5bd6c3c7e54edfc68e0641023f187d50f4`

```dockerfile
```

-	Layers:
	-	`sha256:23fdfa5b105ee18314872de802056b5f617360d56d3b086bdda360c3e7016ba2`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 19.6 KB (19597 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b61a409fdd32b44c75e05094b2f8c0a52caf048baee74cf2649889f8ab0c2230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbeb25ac1257f5e8d7c8b6cfd2aa0da22c8c31b371a8efcbf80b4431ba37a24`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218a17e7411247e7ec655ce4aaa9fe4b47d0895bd6e73851ed546667f0fe3e55`  
		Last Modified: Tue, 13 May 2025 23:49:41 GMT  
		Size: 73.3 MB (73320337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5196a02470ffb1dcbdfc7b2cbdb242760b0c07b10d6517ead18d891bb400f4c`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70010398e4917d413210539be9ac7a4403afbbcf085c8329fd7d92cd39012be1`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bb11082a4007faf836d047799e795f81b039d363ed2e41660ed5b9c64291e2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e4eb373937c062aa03046300871c364ec0cddbabb069f4c3727ccdfa2b0dd`

```dockerfile
```

-	Layers:
	-	`sha256:49e2f94d180b1c01ef09860292cee489ba53bf10fe0360ee401da18671f54bfb`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 19.6 KB (19628 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:092d4356881956db83c99181d24d22e18202524f068320f251560a070f0e421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82507424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f042b6c3a995ea20dd8f5d1fef7add00ff33db270e8df2ba861973326fd624`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ae4ff1dba2c4c9b0b650ad779e3fa82323317b6267e07b9e33df3854e9689c`  
		Last Modified: Tue, 13 May 2025 23:48:01 GMT  
		Size: 79.0 MB (79041745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0eb19cec68f9427b98d8d8da7cede7cfc1984fb199d85a714f9e6748446204`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb0373ef72019570b028f9ab8a1d5c7bfe013d9db28e8cb186a763a688a664a`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d91231a035890e7216b1fae2a3345dc0d803273bf8d669cfefcf4d55c73e2b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb327f2a61a25402a9d91889125075436aef52d049ba6290c71057db343a6a76`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b62d3004205f74b9851086a8e111bb2893118e7bcf7afaf4b7da2225ec91b`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f3f0d610397b274b22fb34b680e8ba7e33a72a604d4b1bbf48e4f529a4e12401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76432657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a00d6a6ef80ef24704f5d349a53f4ae3bd9aa4d09d004a67fbc7406b59d288`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8415d72717fd2f47320e78289223b64170d05f5f1c5ed853850b3ec622aca70`  
		Last Modified: Tue, 13 May 2025 23:53:20 GMT  
		Size: 72.9 MB (72856253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9f4c7b61730302b7702086f8672aff08ab5023af2e9cf71e290a1a9ef11d1c`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd285292c92d194571feccdd50b4da84ca96301d53122a96aa8043da2bf1b83`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7daef37645d9b686c2bc329d817a6c02ef1199122ef6728f491b3c255c28c85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cb6ff731d3d100c474d30fba1df224e326ef9c95f84e3076aad50497e3b1f3`

```dockerfile
```

-	Layers:
	-	`sha256:219a42b1eb87f194f15e45b78ecd52a13f1f31912d1d7f2335f307f6a2072e44`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7e05c6940177520cc8383444ba0a8572212bd77a0a49215191a322f8f5ce5e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71031247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff4aa0a5c80674732b38dfef9e8232d2b8e19898c99b389ba7661284018062`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6400ff82abe5ab3b99bdcac59bf46b6dc34bc7216ad735a629cc3bc9ce1375d`  
		Last Modified: Tue, 13 May 2025 23:51:36 GMT  
		Size: 67.6 MB (67561620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264077ca48f381269649e75852fcada29fbe169adccdb4a810c7934e48ddcc3`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b2fae274cd89bc147cb4f042b95d120b3e8db6d5b7281a70e2ff486dd3a2b7`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5fab5a82196b431e4b37a57ed657e8531ecc31f5e49e7fc7c5c191ca880741d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90fc38218c75cfc61c2c19fcbd8fe5f19a38759cefd5e48f936ca64fb508a2d`

```dockerfile
```

-	Layers:
	-	`sha256:c77b5005edf4457d5cc01076ea24907883bbcb850ad767ec13de864f45d7a43b`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6`

```console
$ docker pull varnish@sha256:6bf79e065f11a74652eb56f0423db163bae84cd3013f0f0954e414f553230a2d
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
$ docker pull varnish@sha256:57e478b79e0078859b9ad717500b7a1093ad75a5a7debb383efeb7969e775641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134226518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042814e438be6572f63bb9ee8f6240a87568cfbbf5e9c7df93b78f25ad9a1215`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7961ee463c9cd79cbd0c61a06fea21157f832e20108453ce05726a57fb3fc8d7`  
		Last Modified: Wed, 21 May 2025 23:22:45 GMT  
		Size: 106.0 MB (105999139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a805644002c267c15ec92a3e7147d38647f0b0132ab1420465e8ae17177b5`  
		Last Modified: Wed, 21 May 2025 23:22:43 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b72167e9fa216e8c59d59519f2b6105538d98051775dfa4183595460d6e5d`  
		Last Modified: Wed, 21 May 2025 23:22:44 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:e5b420e0900f7ef0c9b97431dd033d49c555f76fee34e06c29e122dde6398195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd809f96b0fb5ad1ef9df86653458b5b949a4d06ea67ca3c5630853689e210d`

```dockerfile
```

-	Layers:
	-	`sha256:75cbf9e831ada7abd87a666144f0b48d3f57152b02deaaadb524e439d795c29d`  
		Last Modified: Wed, 21 May 2025 23:22:43 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:2206778c8fc3cef6b8e2c531ac9061921334ab4257c9e573e26199f7be6e0463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104593411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c77cb0f82042e2bdf6c44034ae7ac355ad83257f93b662b32330861933cb35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0608e408adc671e0a0fed2d25e1dda0bf4b2a1c314aaae45b8d585b597c69fb`  
		Last Modified: Thu, 22 May 2025 02:24:56 GMT  
		Size: 80.7 MB (80658449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea3f89f757c6d373ee992295b1504bd3f0701fb19df6a3e1679f2f70a3c2bc0`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635597c7c7987dba75e13a51c0e182abdc184ded70871d70336cd8a449fbf1f4`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:63da5327089f8c608bfbd4f5b8f003384c0324e738c078c367166048c92978e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65844ee50d3f4752502b0349d6d66591e89a4a003af327a09058542eb2a963cc`

```dockerfile
```

-	Layers:
	-	`sha256:800aeaf1dfccf2f5546b6147bb3aefa8e91cf3d5696e1564ac0e9e1d6c39b29a`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:54c30202598e4aa53a4ae21a8b78e68ba6aae471987b57c810493a7e3abe1a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128550652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8e92e79663c4118b5dc879596aa2bfb575fb931e482df4bdeaf1fe94a22fc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e103af1b5ba34206099062e4e79bd5d0fbecc71c7e946b91806320efc8767fcc`  
		Last Modified: Thu, 22 May 2025 02:44:50 GMT  
		Size: 100.5 MB (100483330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f717e37f5ad5093f50dbcdcb0c6c62e656ab239b6e41552d5afde92f652d23`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04237c11137fd0a0b0b3a6aedb98001ed46399cac495e49a9d5e35ce91a17199`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:e0e92dcc17751fb899955fb174b1d9df59f585eaebb7dd39b21f4848086d625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3120c7d68d62a09723c238c1a7943b4f3bf59414c5f5f3709aa66b6d79f65cc`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b9939c443ccaf2f8aa4e2edd02a5d4aee982d4c0cd46044caf38b047ad821`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 18.9 KB (18938 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:c0be393634715d1e41b78c8f6efdf0a090fd8074f32566b2e3ca1761220ac6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131356310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c814ea02d5f19ac759f122f3dbeb7eecc2d86463a9b7875350a34e17dc26f0b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4133fcf0caeb66545bc6dee3845609e05c2ca87d6365bbb2b0a0d6683dfad3`  
		Last Modified: Wed, 21 May 2025 23:22:07 GMT  
		Size: 102.1 MB (102146780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8908cdb8d463a92001659b18fdf6ce92e634cf0078faef364eb35b50357130f`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7bbecf64db50ca5d123b5f31886503aa1eac602a2b0fd2b449ce75b31a927a`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:5d9fb3191e6d735de23a6f756fe912457d339dd87798a43442676df647d353e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497e9fba84fa0c8a083603c75981aa1e4e661cf494e256bc9d38022ecd928ea`

```dockerfile
```

-	Layers:
	-	`sha256:42684ebe804da166517493c0efc329b8f47ca9fca69f03af8c3d99ba788b0ebc`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:73387fdd9dc778ac5b60fc84343b1143dc1345701bd5b873da7905bc95cb622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137045074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08da53c1d76d7f208637512e08ac61614577751a04b9f1c917753d9990756d47`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd435ff69c5c6ed4704ae10b0945972fbf1a4e4dd8c82ff7d948ce03f1aa6624`  
		Last Modified: Tue, 13 May 2025 23:58:30 GMT  
		Size: 105.0 MB (104974584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fba4d4d00841714b3b1541e8423961b5551521b2a12a017f73c0cc0f5fd84a7`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733fde6a0fd126007558fc5d9cb027554c0f140929409dc4f258521cdfdd9ae9`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:90d910179a4bdc3bbca0c977f7ffcd69010efdba4137a846bb14b7eec5f98e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efde49921aa74cbc52b1c73024110e7dae588e2bd50b2d4753190b7b8d0c87a3`

```dockerfile
```

-	Layers:
	-	`sha256:4a0f8e185bc3440975a28df2a29c2a3ae3c3d6c64c95ecb0dd99ec7fffed24a5`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 18.9 KB (18885 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:5c96875ade9f46839762abfcb379e350768363e30a4c5e50be4818ca1a55b889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112142571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f916da155d02b53a7023cecfb0ce65928cfa562072a3929673329ebd3473f643`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105703520f036595bff09dffa3717a34106202f63d8a9d509302052079472976`  
		Last Modified: Thu, 22 May 2025 00:59:20 GMT  
		Size: 85.3 MB (85257721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d6faceb45eec5234f31017ce7e88172607eb02f383d2808e802450615e9e42`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61100beed27d3a5c5366963ea68abca2ef2e0556894a100a90ae1778f8589dfe`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:d86a501137d98d51cbc2638bbe416d68e64500738b77577be3f0a7eefc13196e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719bdbb94d7c4efcd614d6f02d3f94ac09d998533b39e6794e773f042aefd623`

```dockerfile
```

-	Layers:
	-	`sha256:9ce1b0b545bcedc8fb0638fec99b372740213c3707ccbcda32a88bba4d4d5d54`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:cb268b57c8a2cec3d39e8e4f74382646c8795718ff25aa57c0d0a5ee3eb1146f
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
$ docker pull varnish@sha256:832539f3c49155c868d6e605b23d11635697ee79308d4d67632bfd80a3592470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef6a698cd1a97012baa9bdd2db973a223ae7b7500b68afd5d7a2849cffaf42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dd875d896754e31f106b279b13f6496adc8421db2c4f87731e3e4723097d55`  
		Last Modified: Tue, 13 May 2025 23:47:56 GMT  
		Size: 76.5 MB (76480503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e6d4496a56a4cdc28e0728f444aca412abcdbf44de2a17517f260143d2445`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe2dce4d3db4cb8f19e79b85dd340da315f5a6503c0177d857e7d710bad2e19`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:745b542be3ade7260c951fd0df6eb7803b1d483c633be4bbe214419631ee5ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbc11303947e59091cf3071eab27aa971a25b9b73cfbb7832b60329497a50ab`

```dockerfile
```

-	Layers:
	-	`sha256:f89f56e4fa97bf3b52dbeb162f579e87f78751ccf4665eafdf273436ff4d5639`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c6f15a90cf4d116fb28f39ecb012995aefb0ecd49c02fa0bd9aeec4adf65cebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62177159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348b5a86113885af2ad1ae03b67a656675d858bac28550d8756c22fb352073a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b64d240de8405e58901ffaa351cf6d995f373610fee29e4806ebafbe8f51b4`  
		Last Modified: Tue, 13 May 2025 23:54:33 GMT  
		Size: 59.1 MB (59076980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f345bef6ca24ad7825007178523af189952fa489de9d8eb18ddad503404c52e`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb03c9836d2f802ac7a200af8b7b5a3d37f070eb40a1fca06426d08cf583d3`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:341536aa96b8653cdc7655ab75a700a74a413abb92fbd62c9736a51d288996b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ccd8901dac22a6fcb8114bc93626ea4a138d3c97c173fc51ce70e0fff5f590`

```dockerfile
```

-	Layers:
	-	`sha256:9df71e7bf646620391b06844710aa5d6a127203721dbbdce0a0b070fe4301319`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:03050dcb8e1b8c436dd6bb97d15cd02ce355fb92d5b0f4fd2a9d87236bacd7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa12c01235c01884aba1beb3ce7e3764811403422085d6361e69b7f7e89a142`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d0112c73e93ba409991084c46b91c454e8873ad85d1a0c704da073c738110`  
		Last Modified: Tue, 13 May 2025 23:53:47 GMT  
		Size: 73.1 MB (73139804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d5db8d46da3afc53cd359504e09f6a3822ceefd1859d19b3d76bcffdefa2e7`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15afac65ae6f31067843e3de68aa1266f07ddce142c1ae08692d23030bee350b`  
		Last Modified: Tue, 13 May 2025 23:53:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:79357498a90f86e478600efa6dccae02abc17f66981aec1940ea28ced6fd52f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d5e0e50d45a1f2ae76d217647b08bca1f59442495bc5c01e2f0ba8c9079ca`

```dockerfile
```

-	Layers:
	-	`sha256:56e88217b045f05b58b9caa245c23fded45cf4a2be1d1c230f34b1b574fb44e4`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:501e68fff243f1b20a14eb50b92274eb17d3668b18614971adbe63c11f567f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82330387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0ee568acabd5eb2489c8492d7ccfa16f09434e29b4969f6f9772f2e41aa022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b78442a5d78ba9003dcc9cdc85c9df4f9cfafb1ad42b203d6ac1ea49040aab4`  
		Last Modified: Tue, 13 May 2025 23:48:04 GMT  
		Size: 78.9 MB (78864705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b116832fccbcf9a985576f61c96fe8c6bd152de5d63b1d3584e815df6cc8030`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004edc5aa7acec0262bd1823f0da31ecb8e70efaf37858b2ea6ca28bf441780e`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09e44671e22716a149f4d002f38e34628f91c212ba0e3057686c99a07ab0e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e286f1515be59ef428b8da884b540ac598ed7f2a8b8e6f64ea9635f564882715`

```dockerfile
```

-	Layers:
	-	`sha256:725f13bcaad1fad6dc735aa5a28fbbe6d5b682b7282865560844161fc6878b0b`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f71a73be8317c4072b991ee98c4c3d8eadb24d188800178968beb834c5724d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76254322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae39867711695ca6650e67c074879731c99cebcdfc99080d153b82a437bbd0c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c9b258186a0fcc1c5c8c94beeb1d5bb81c0ab46f616ce67e7a00bf431cc4a3`  
		Last Modified: Wed, 14 May 2025 00:00:26 GMT  
		Size: 72.7 MB (72677915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e89d21db4cd9964b28450f72cf636a52889cfe69f1d4cb2f242a5a3d2ad350`  
		Last Modified: Wed, 14 May 2025 00:00:25 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b02ea0fef7a75f4975001831e3cc80c4fc8904726393c3c240acce25932a96`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b8bb1c1c7e7e8608aacbef7f0b606beb2db199da80c18d189ad22ba69cf00370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6951c078ba75ba3eb2418cecd3a1e5b91a4373905eabd1a4d5caee74b8d56e9`

```dockerfile
```

-	Layers:
	-	`sha256:cfc6a58d241c77836c04f39e0e1a7adfe81d3ee28a3f7889eec06d865211a268`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:01893f1c5743b8d2b36383618902945cba7b093649f09519ebe158ba9f5f8b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70859326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd196cc640f60dfe5eaa365485db2e8c6aac01a37f71995a8895ac495f0e5587`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb58c2794411aa50dc12dbb79cdf53b10c92442248361dbe2644b83e7d4d2ba`  
		Last Modified: Tue, 13 May 2025 23:56:19 GMT  
		Size: 67.4 MB (67389700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a824335bb1eb8cfc81d98eb1052441a94a5806fa9e3d060cb71f520520d0bf74`  
		Last Modified: Tue, 13 May 2025 23:56:17 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31dbfe4dde5d97940cea5e1c9a3d64dbc3d17c8aaba5d04926e5a54fe250069`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82c172006540f09f9dd5322d8d9f23fda47f1ad037a7196f60115a40f504927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c75b90bd5fa7d9fccf356e10d78df6ec4e00a7a88ad8dd24d0ec915d5e64412`

```dockerfile
```

-	Layers:
	-	`sha256:68c68e03488141b66b6f577ded0927247796d3cc30661286e556cf227077b16c`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.3`

```console
$ docker pull varnish@sha256:6bf79e065f11a74652eb56f0423db163bae84cd3013f0f0954e414f553230a2d
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

### `varnish:7.6.3` - linux; amd64

```console
$ docker pull varnish@sha256:57e478b79e0078859b9ad717500b7a1093ad75a5a7debb383efeb7969e775641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134226518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042814e438be6572f63bb9ee8f6240a87568cfbbf5e9c7df93b78f25ad9a1215`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7961ee463c9cd79cbd0c61a06fea21157f832e20108453ce05726a57fb3fc8d7`  
		Last Modified: Wed, 21 May 2025 23:22:45 GMT  
		Size: 106.0 MB (105999139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a805644002c267c15ec92a3e7147d38647f0b0132ab1420465e8ae17177b5`  
		Last Modified: Wed, 21 May 2025 23:22:43 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b72167e9fa216e8c59d59519f2b6105538d98051775dfa4183595460d6e5d`  
		Last Modified: Wed, 21 May 2025 23:22:44 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:e5b420e0900f7ef0c9b97431dd033d49c555f76fee34e06c29e122dde6398195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd809f96b0fb5ad1ef9df86653458b5b949a4d06ea67ca3c5630853689e210d`

```dockerfile
```

-	Layers:
	-	`sha256:75cbf9e831ada7abd87a666144f0b48d3f57152b02deaaadb524e439d795c29d`  
		Last Modified: Wed, 21 May 2025 23:22:43 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:2206778c8fc3cef6b8e2c531ac9061921334ab4257c9e573e26199f7be6e0463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104593411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c77cb0f82042e2bdf6c44034ae7ac355ad83257f93b662b32330861933cb35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0608e408adc671e0a0fed2d25e1dda0bf4b2a1c314aaae45b8d585b597c69fb`  
		Last Modified: Thu, 22 May 2025 02:24:56 GMT  
		Size: 80.7 MB (80658449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea3f89f757c6d373ee992295b1504bd3f0701fb19df6a3e1679f2f70a3c2bc0`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635597c7c7987dba75e13a51c0e182abdc184ded70871d70336cd8a449fbf1f4`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:63da5327089f8c608bfbd4f5b8f003384c0324e738c078c367166048c92978e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65844ee50d3f4752502b0349d6d66591e89a4a003af327a09058542eb2a963cc`

```dockerfile
```

-	Layers:
	-	`sha256:800aeaf1dfccf2f5546b6147bb3aefa8e91cf3d5696e1564ac0e9e1d6c39b29a`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:54c30202598e4aa53a4ae21a8b78e68ba6aae471987b57c810493a7e3abe1a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128550652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8e92e79663c4118b5dc879596aa2bfb575fb931e482df4bdeaf1fe94a22fc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e103af1b5ba34206099062e4e79bd5d0fbecc71c7e946b91806320efc8767fcc`  
		Last Modified: Thu, 22 May 2025 02:44:50 GMT  
		Size: 100.5 MB (100483330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f717e37f5ad5093f50dbcdcb0c6c62e656ab239b6e41552d5afde92f652d23`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04237c11137fd0a0b0b3a6aedb98001ed46399cac495e49a9d5e35ce91a17199`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:e0e92dcc17751fb899955fb174b1d9df59f585eaebb7dd39b21f4848086d625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3120c7d68d62a09723c238c1a7943b4f3bf59414c5f5f3709aa66b6d79f65cc`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b9939c443ccaf2f8aa4e2edd02a5d4aee982d4c0cd46044caf38b047ad821`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 18.9 KB (18938 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; 386

```console
$ docker pull varnish@sha256:c0be393634715d1e41b78c8f6efdf0a090fd8074f32566b2e3ca1761220ac6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131356310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c814ea02d5f19ac759f122f3dbeb7eecc2d86463a9b7875350a34e17dc26f0b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4133fcf0caeb66545bc6dee3845609e05c2ca87d6365bbb2b0a0d6683dfad3`  
		Last Modified: Wed, 21 May 2025 23:22:07 GMT  
		Size: 102.1 MB (102146780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8908cdb8d463a92001659b18fdf6ce92e634cf0078faef364eb35b50357130f`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7bbecf64db50ca5d123b5f31886503aa1eac602a2b0fd2b449ce75b31a927a`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:5d9fb3191e6d735de23a6f756fe912457d339dd87798a43442676df647d353e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497e9fba84fa0c8a083603c75981aa1e4e661cf494e256bc9d38022ecd928ea`

```dockerfile
```

-	Layers:
	-	`sha256:42684ebe804da166517493c0efc329b8f47ca9fca69f03af8c3d99ba788b0ebc`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:73387fdd9dc778ac5b60fc84343b1143dc1345701bd5b873da7905bc95cb622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137045074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08da53c1d76d7f208637512e08ac61614577751a04b9f1c917753d9990756d47`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd435ff69c5c6ed4704ae10b0945972fbf1a4e4dd8c82ff7d948ce03f1aa6624`  
		Last Modified: Tue, 13 May 2025 23:58:30 GMT  
		Size: 105.0 MB (104974584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fba4d4d00841714b3b1541e8423961b5551521b2a12a017f73c0cc0f5fd84a7`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733fde6a0fd126007558fc5d9cb027554c0f140929409dc4f258521cdfdd9ae9`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:90d910179a4bdc3bbca0c977f7ffcd69010efdba4137a846bb14b7eec5f98e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efde49921aa74cbc52b1c73024110e7dae588e2bd50b2d4753190b7b8d0c87a3`

```dockerfile
```

-	Layers:
	-	`sha256:4a0f8e185bc3440975a28df2a29c2a3ae3c3d6c64c95ecb0dd99ec7fffed24a5`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 18.9 KB (18885 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; s390x

```console
$ docker pull varnish@sha256:5c96875ade9f46839762abfcb379e350768363e30a4c5e50be4818ca1a55b889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112142571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f916da155d02b53a7023cecfb0ce65928cfa562072a3929673329ebd3473f643`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105703520f036595bff09dffa3717a34106202f63d8a9d509302052079472976`  
		Last Modified: Thu, 22 May 2025 00:59:20 GMT  
		Size: 85.3 MB (85257721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d6faceb45eec5234f31017ce7e88172607eb02f383d2808e802450615e9e42`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61100beed27d3a5c5366963ea68abca2ef2e0556894a100a90ae1778f8589dfe`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:d86a501137d98d51cbc2638bbe416d68e64500738b77577be3f0a7eefc13196e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719bdbb94d7c4efcd614d6f02d3f94ac09d998533b39e6794e773f042aefd623`

```dockerfile
```

-	Layers:
	-	`sha256:9ce1b0b545bcedc8fb0638fec99b372740213c3707ccbcda32a88bba4d4d5d54`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.3-alpine`

```console
$ docker pull varnish@sha256:cb268b57c8a2cec3d39e8e4f74382646c8795718ff25aa57c0d0a5ee3eb1146f
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

### `varnish:7.6.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:832539f3c49155c868d6e605b23d11635697ee79308d4d67632bfd80a3592470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef6a698cd1a97012baa9bdd2db973a223ae7b7500b68afd5d7a2849cffaf42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dd875d896754e31f106b279b13f6496adc8421db2c4f87731e3e4723097d55`  
		Last Modified: Tue, 13 May 2025 23:47:56 GMT  
		Size: 76.5 MB (76480503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e6d4496a56a4cdc28e0728f444aca412abcdbf44de2a17517f260143d2445`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe2dce4d3db4cb8f19e79b85dd340da315f5a6503c0177d857e7d710bad2e19`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:745b542be3ade7260c951fd0df6eb7803b1d483c633be4bbe214419631ee5ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbc11303947e59091cf3071eab27aa971a25b9b73cfbb7832b60329497a50ab`

```dockerfile
```

-	Layers:
	-	`sha256:f89f56e4fa97bf3b52dbeb162f579e87f78751ccf4665eafdf273436ff4d5639`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c6f15a90cf4d116fb28f39ecb012995aefb0ecd49c02fa0bd9aeec4adf65cebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62177159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348b5a86113885af2ad1ae03b67a656675d858bac28550d8756c22fb352073a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b64d240de8405e58901ffaa351cf6d995f373610fee29e4806ebafbe8f51b4`  
		Last Modified: Tue, 13 May 2025 23:54:33 GMT  
		Size: 59.1 MB (59076980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f345bef6ca24ad7825007178523af189952fa489de9d8eb18ddad503404c52e`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb03c9836d2f802ac7a200af8b7b5a3d37f070eb40a1fca06426d08cf583d3`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:341536aa96b8653cdc7655ab75a700a74a413abb92fbd62c9736a51d288996b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ccd8901dac22a6fcb8114bc93626ea4a138d3c97c173fc51ce70e0fff5f590`

```dockerfile
```

-	Layers:
	-	`sha256:9df71e7bf646620391b06844710aa5d6a127203721dbbdce0a0b070fe4301319`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:03050dcb8e1b8c436dd6bb97d15cd02ce355fb92d5b0f4fd2a9d87236bacd7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa12c01235c01884aba1beb3ce7e3764811403422085d6361e69b7f7e89a142`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d0112c73e93ba409991084c46b91c454e8873ad85d1a0c704da073c738110`  
		Last Modified: Tue, 13 May 2025 23:53:47 GMT  
		Size: 73.1 MB (73139804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d5db8d46da3afc53cd359504e09f6a3822ceefd1859d19b3d76bcffdefa2e7`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15afac65ae6f31067843e3de68aa1266f07ddce142c1ae08692d23030bee350b`  
		Last Modified: Tue, 13 May 2025 23:53:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:79357498a90f86e478600efa6dccae02abc17f66981aec1940ea28ced6fd52f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d5e0e50d45a1f2ae76d217647b08bca1f59442495bc5c01e2f0ba8c9079ca`

```dockerfile
```

-	Layers:
	-	`sha256:56e88217b045f05b58b9caa245c23fded45cf4a2be1d1c230f34b1b574fb44e4`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:501e68fff243f1b20a14eb50b92274eb17d3668b18614971adbe63c11f567f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82330387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0ee568acabd5eb2489c8492d7ccfa16f09434e29b4969f6f9772f2e41aa022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b78442a5d78ba9003dcc9cdc85c9df4f9cfafb1ad42b203d6ac1ea49040aab4`  
		Last Modified: Tue, 13 May 2025 23:48:04 GMT  
		Size: 78.9 MB (78864705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b116832fccbcf9a985576f61c96fe8c6bd152de5d63b1d3584e815df6cc8030`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004edc5aa7acec0262bd1823f0da31ecb8e70efaf37858b2ea6ca28bf441780e`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09e44671e22716a149f4d002f38e34628f91c212ba0e3057686c99a07ab0e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e286f1515be59ef428b8da884b540ac598ed7f2a8b8e6f64ea9635f564882715`

```dockerfile
```

-	Layers:
	-	`sha256:725f13bcaad1fad6dc735aa5a28fbbe6d5b682b7282865560844161fc6878b0b`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f71a73be8317c4072b991ee98c4c3d8eadb24d188800178968beb834c5724d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76254322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae39867711695ca6650e67c074879731c99cebcdfc99080d153b82a437bbd0c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c9b258186a0fcc1c5c8c94beeb1d5bb81c0ab46f616ce67e7a00bf431cc4a3`  
		Last Modified: Wed, 14 May 2025 00:00:26 GMT  
		Size: 72.7 MB (72677915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e89d21db4cd9964b28450f72cf636a52889cfe69f1d4cb2f242a5a3d2ad350`  
		Last Modified: Wed, 14 May 2025 00:00:25 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b02ea0fef7a75f4975001831e3cc80c4fc8904726393c3c240acce25932a96`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b8bb1c1c7e7e8608aacbef7f0b606beb2db199da80c18d189ad22ba69cf00370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6951c078ba75ba3eb2418cecd3a1e5b91a4373905eabd1a4d5caee74b8d56e9`

```dockerfile
```

-	Layers:
	-	`sha256:cfc6a58d241c77836c04f39e0e1a7adfe81d3ee28a3f7889eec06d865211a268`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:01893f1c5743b8d2b36383618902945cba7b093649f09519ebe158ba9f5f8b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70859326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd196cc640f60dfe5eaa365485db2e8c6aac01a37f71995a8895ac495f0e5587`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb58c2794411aa50dc12dbb79cdf53b10c92442248361dbe2644b83e7d4d2ba`  
		Last Modified: Tue, 13 May 2025 23:56:19 GMT  
		Size: 67.4 MB (67389700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a824335bb1eb8cfc81d98eb1052441a94a5806fa9e3d060cb71f520520d0bf74`  
		Last Modified: Tue, 13 May 2025 23:56:17 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31dbfe4dde5d97940cea5e1c9a3d64dbc3d17c8aaba5d04926e5a54fe250069`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82c172006540f09f9dd5322d8d9f23fda47f1ad037a7196f60115a40f504927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c75b90bd5fa7d9fccf356e10d78df6ec4e00a7a88ad8dd24d0ec915d5e64412`

```dockerfile
```

-	Layers:
	-	`sha256:68c68e03488141b66b6f577ded0927247796d3cc30661286e556cf227077b16c`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:86e8b8945266a860db142a641b60e919a34eda77f929a51be888b70d41bf6324
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
$ docker pull varnish@sha256:977ab78dc31ecbec4285eced93daf2391dc232d1ee452987a7c1740e902e9973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134432559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffb297b8223b1aae9fe862b8a03a6020f97a7fa4d8dae2134ba59518fcb7f84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ba1e050e4fcf7680bef6d92b2df063c4e527e294143a153dc00f28052a2176`  
		Last Modified: Wed, 21 May 2025 23:22:38 GMT  
		Size: 106.2 MB (106205179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da93242d1418a17c24960555b296029f7b8098770d10353a2e8c308970676138`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef390b256376ce19bd47ce3e975bf48d8d3f6bc71a7c31905c0fed7fc2059d13`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:1e0a03226641f48fdaba83cee24a1cb8e2a8f4827e2ca6f8902508550d83c03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414c6f46ac564e1a77e8f8ef21a1e32c4e2b3c32c7cbee7b00f9f25b8eb101b1`

```dockerfile
```

-	Layers:
	-	`sha256:3e2476437e1f9fe6c21db7b9d507881f836a784072f8c11c79dc9cd63d1f10fb`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 19.4 KB (19446 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c773ab683f23d2cd79e06d85d02996b2b01924bf328e3666f5f9b341cbfd0d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104785075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba66129a0dbe6f325051712cad928cbe8ad18e5800c4efdd574286e9d69f6fe0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac458455152571434f9a6c7df061f113f5a5c2068aef467ef345ac392b3897d6`  
		Last Modified: Thu, 22 May 2025 02:21:50 GMT  
		Size: 80.9 MB (80850108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb358afb88ae9a9c8149e8291ed8f719db1db6307b98ba3ba7e90000641a6b`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a7b99352f7ce860abc258d20d7bb084554b2ebe5306fad771ccb4aed6320fe`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:6c0d75b8f70c4a9a4025686d21d55ce66ae618432ae4923e0934e23a4c42b1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf627a5ab1f86c4df615ef35dcbe4227898c6ba005d21a0afe7bbac56015fa9`

```dockerfile
```

-	Layers:
	-	`sha256:480b751b13fe5c2f25340d8151c8ed61eb8722e2ab491566e35a7f7cdaf3f6f1`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1aad1b68dd84a97f68d7c89f793d30650db73f655ae9dd0f6f0268bcc13217b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128756188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade40f2aed6c3219ad502e0110acbf89f344b37f32f6ecd9bc36aff5244552f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b17e29ac9e54e576cb04765200626525f96dc401ab614bbc54eb2145157550`  
		Last Modified: Thu, 22 May 2025 02:42:08 GMT  
		Size: 100.7 MB (100688867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e3bb5152055b2725c6ebad6b01752877a4e804b3d8d3af8e16c7590878fe9a`  
		Last Modified: Thu, 22 May 2025 02:42:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a02a085b2688630644cda4682d17d517bc18e61f70125f6690207bb155419d`  
		Last Modified: Thu, 22 May 2025 02:42:04 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:757e93b0ee017bac182544700626a8ae26fcc93799faa6c610d43e5580cdc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ccce5ff2d796096453bef1cde02b0fc8a7fd864e105a6531e44d296d252583`

```dockerfile
```

-	Layers:
	-	`sha256:6afbcf3ccb160b6b79a88ff94546bbfde4ce05798cf2a0a00468afe4d224a23c`  
		Last Modified: Thu, 22 May 2025 02:42:05 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; 386

```console
$ docker pull varnish@sha256:459840cdaddcf109cc22f4a13e60eb13eec8078c2751263020b63e58ca3d3ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131537851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4345e460a9ec1a61a6167b276d59f12f88fa841eaef97898deefbeea756927`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0e1b7420750c7ad80b73bb0b5a38934c0b3d489b169108888796b0eb517e3`  
		Last Modified: Wed, 21 May 2025 23:22:23 GMT  
		Size: 102.3 MB (102328321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e36adf8a72f5214761c46f62dba51ea501386ecc7aee9df878eba645b927fe`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b2b528b3cc25073c565cb06deb12e3186235fb0a4c80de54b28ec663757f12`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:c1e8cd6066a3a7368c1f86e6f3a470eec4dbff018fcb14e2f84814a0f6c99c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b84d414ffbffca90b934a952a0da6bb34f54db530a1b904e79c493b59554354`

```dockerfile
```

-	Layers:
	-	`sha256:4cf8b13efc417a94e0f8d146bad31193adeadee7a679411e5e12d6207c259261`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; ppc64le

```console
$ docker pull varnish@sha256:7d7d355b21c251e67d9b9e85a8f288363a9ad60560a971151378e43846668456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137233020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7b5b5e39554dc9f66a02e3c59fb3371f8678ecfa05941f93381870f6a36d2f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85372ffb9150cd3a320a4bc44ed4b2cdc019a9a1ecb70a111b384220d6116a1b`  
		Last Modified: Tue, 13 May 2025 23:51:11 GMT  
		Size: 105.2 MB (105162529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a8da1e97e0a49a6694eec4aa254842ac3589188d9ef503a15a2c2b9bd4c3be`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e61219f2f71de9614f1131b9292d43311eadd8e856d2a632f6fc28a3d50e`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:fc1ae7f7739a94a83065ee6d28e6def85a575001f37a0dbf579ee9c9091bbdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ff9e1f324990faa5d0bda41d3f97f8c3b02d2a61946c8e69aaba79da6e5566`

```dockerfile
```

-	Layers:
	-	`sha256:92ab709f19228dcc9118cedda83d251b2febd005f9493709cdc69e156b4fa576`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; s390x

```console
$ docker pull varnish@sha256:2455f1bc08cbcce52d13fe8aafd3078ffe19fb13954051b395d676273e061f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112354777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694c9e09bf81a75334ff9be6cb3bdd4937b9c1791d01fc9ddce1e8b34326bda2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8299d63723e54463fad083282a50370c22bd894ca037870414a61da1b81a3daa`  
		Last Modified: Thu, 22 May 2025 00:56:32 GMT  
		Size: 85.5 MB (85469923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e21687c812f9934edcfcf1ce07fdbf0c291d184931706496aa49a657e7e794`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51af249f25615e77d6502237bcdee426a95a9e5649761460f178dc5b2fdfe188`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:573a4860c5f251faa947595939b5729f0b0d3fb703e20a598344ce017b44fa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7ec93bc1a67bbaaa5d04f82e69b77595dd5fd0e67ff7c8cb0bb321e30a2d26`

```dockerfile
```

-	Layers:
	-	`sha256:e10caa24f54ad7e91b672430ede572bba41c6b63b5a52bcd4da125bead791f83`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7-alpine`

```console
$ docker pull varnish@sha256:edbb3bc7c0d80e0222c416c709b09a73ccd2df1cdae3866c7322a241eff4e180
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
$ docker pull varnish@sha256:259b86a44377185dba18240d733380c541601d25d666b2e9ba9acd577c4dcf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80309670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b284e6450b0b02b8aa6c5ced28b66e12656ba744baa00edecb76fe116c080556`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d09d2ebf1afc734637d3674346c53f56296aec75a61edd0c0344cf312eebb8a`  
		Last Modified: Tue, 13 May 2025 23:47:47 GMT  
		Size: 76.7 MB (76665367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020865b6f7518b5553fb3b5f5f87fe7d769c0bfd8862be571713f33c02335d57`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0716d6cccd5a8c846bee76362aae17be1826d27994c5806f1ce07585b70ff59`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ef0ab02e38b644a555096be9157be1cea81d90cc0f8de591ccb819b98940f00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b8aea16b52858945e38eec85b802ca5db8803f2036a627d258530547fe08c7`

```dockerfile
```

-	Layers:
	-	`sha256:bc90243747f045b359a650c8909062b2318c1499e7f48a798167cbfc7657f381`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8d292ee45a9dc2dfbfed35458b8fa0270f85040da8ee21207a334d4775d8380f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eaef00bc440210de5afb83262c54f02d0ec3c76d7ce72305a6cc82dc53aa03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20465a10cb0623d2638bae875b058ba3f793638be7cb92415040e000c1b76f8`  
		Last Modified: Tue, 13 May 2025 23:50:11 GMT  
		Size: 59.3 MB (59261224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083ea808ed9381df01328a2ef1653df216e9b4da36244e4dcadd17dcdf6e84a`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8794d458a0b8f646fc60add26e4459b4d4c9407b50280e428511293a11520f`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e91eaeeb5f0182b467108b50d78b5afa1b3a461e88852279d5862ea5cfa76cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179782e695fe7a93dca563aee6b50b5bd6c3c7e54edfc68e0641023f187d50f4`

```dockerfile
```

-	Layers:
	-	`sha256:23fdfa5b105ee18314872de802056b5f617360d56d3b086bdda360c3e7016ba2`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 19.6 KB (19597 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b61a409fdd32b44c75e05094b2f8c0a52caf048baee74cf2649889f8ab0c2230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbeb25ac1257f5e8d7c8b6cfd2aa0da22c8c31b371a8efcbf80b4431ba37a24`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218a17e7411247e7ec655ce4aaa9fe4b47d0895bd6e73851ed546667f0fe3e55`  
		Last Modified: Tue, 13 May 2025 23:49:41 GMT  
		Size: 73.3 MB (73320337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5196a02470ffb1dcbdfc7b2cbdb242760b0c07b10d6517ead18d891bb400f4c`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70010398e4917d413210539be9ac7a4403afbbcf085c8329fd7d92cd39012be1`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bb11082a4007faf836d047799e795f81b039d363ed2e41660ed5b9c64291e2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e4eb373937c062aa03046300871c364ec0cddbabb069f4c3727ccdfa2b0dd`

```dockerfile
```

-	Layers:
	-	`sha256:49e2f94d180b1c01ef09860292cee489ba53bf10fe0360ee401da18671f54bfb`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 19.6 KB (19628 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:092d4356881956db83c99181d24d22e18202524f068320f251560a070f0e421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82507424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f042b6c3a995ea20dd8f5d1fef7add00ff33db270e8df2ba861973326fd624`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ae4ff1dba2c4c9b0b650ad779e3fa82323317b6267e07b9e33df3854e9689c`  
		Last Modified: Tue, 13 May 2025 23:48:01 GMT  
		Size: 79.0 MB (79041745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0eb19cec68f9427b98d8d8da7cede7cfc1984fb199d85a714f9e6748446204`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb0373ef72019570b028f9ab8a1d5c7bfe013d9db28e8cb186a763a688a664a`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d91231a035890e7216b1fae2a3345dc0d803273bf8d669cfefcf4d55c73e2b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb327f2a61a25402a9d91889125075436aef52d049ba6290c71057db343a6a76`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b62d3004205f74b9851086a8e111bb2893118e7bcf7afaf4b7da2225ec91b`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f3f0d610397b274b22fb34b680e8ba7e33a72a604d4b1bbf48e4f529a4e12401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76432657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a00d6a6ef80ef24704f5d349a53f4ae3bd9aa4d09d004a67fbc7406b59d288`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8415d72717fd2f47320e78289223b64170d05f5f1c5ed853850b3ec622aca70`  
		Last Modified: Tue, 13 May 2025 23:53:20 GMT  
		Size: 72.9 MB (72856253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9f4c7b61730302b7702086f8672aff08ab5023af2e9cf71e290a1a9ef11d1c`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd285292c92d194571feccdd50b4da84ca96301d53122a96aa8043da2bf1b83`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7daef37645d9b686c2bc329d817a6c02ef1199122ef6728f491b3c255c28c85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cb6ff731d3d100c474d30fba1df224e326ef9c95f84e3076aad50497e3b1f3`

```dockerfile
```

-	Layers:
	-	`sha256:219a42b1eb87f194f15e45b78ecd52a13f1f31912d1d7f2335f307f6a2072e44`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7e05c6940177520cc8383444ba0a8572212bd77a0a49215191a322f8f5ce5e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71031247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff4aa0a5c80674732b38dfef9e8232d2b8e19898c99b389ba7661284018062`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6400ff82abe5ab3b99bdcac59bf46b6dc34bc7216ad735a629cc3bc9ce1375d`  
		Last Modified: Tue, 13 May 2025 23:51:36 GMT  
		Size: 67.6 MB (67561620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264077ca48f381269649e75852fcada29fbe169adccdb4a810c7934e48ddcc3`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b2fae274cd89bc147cb4f042b95d120b3e8db6d5b7281a70e2ff486dd3a2b7`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5fab5a82196b431e4b37a57ed657e8531ecc31f5e49e7fc7c5c191ca880741d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90fc38218c75cfc61c2c19fcbd8fe5f19a38759cefd5e48f936ca64fb508a2d`

```dockerfile
```

-	Layers:
	-	`sha256:c77b5005edf4457d5cc01076ea24907883bbcb850ad767ec13de864f45d7a43b`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.1`

```console
$ docker pull varnish@sha256:86e8b8945266a860db142a641b60e919a34eda77f929a51be888b70d41bf6324
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

### `varnish:7.7.1` - linux; amd64

```console
$ docker pull varnish@sha256:977ab78dc31ecbec4285eced93daf2391dc232d1ee452987a7c1740e902e9973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134432559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffb297b8223b1aae9fe862b8a03a6020f97a7fa4d8dae2134ba59518fcb7f84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ba1e050e4fcf7680bef6d92b2df063c4e527e294143a153dc00f28052a2176`  
		Last Modified: Wed, 21 May 2025 23:22:38 GMT  
		Size: 106.2 MB (106205179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da93242d1418a17c24960555b296029f7b8098770d10353a2e8c308970676138`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef390b256376ce19bd47ce3e975bf48d8d3f6bc71a7c31905c0fed7fc2059d13`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1` - unknown; unknown

```console
$ docker pull varnish@sha256:1e0a03226641f48fdaba83cee24a1cb8e2a8f4827e2ca6f8902508550d83c03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414c6f46ac564e1a77e8f8ef21a1e32c4e2b3c32c7cbee7b00f9f25b8eb101b1`

```dockerfile
```

-	Layers:
	-	`sha256:3e2476437e1f9fe6c21db7b9d507881f836a784072f8c11c79dc9cd63d1f10fb`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 19.4 KB (19446 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c773ab683f23d2cd79e06d85d02996b2b01924bf328e3666f5f9b341cbfd0d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104785075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba66129a0dbe6f325051712cad928cbe8ad18e5800c4efdd574286e9d69f6fe0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac458455152571434f9a6c7df061f113f5a5c2068aef467ef345ac392b3897d6`  
		Last Modified: Thu, 22 May 2025 02:21:50 GMT  
		Size: 80.9 MB (80850108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb358afb88ae9a9c8149e8291ed8f719db1db6307b98ba3ba7e90000641a6b`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a7b99352f7ce860abc258d20d7bb084554b2ebe5306fad771ccb4aed6320fe`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1` - unknown; unknown

```console
$ docker pull varnish@sha256:6c0d75b8f70c4a9a4025686d21d55ce66ae618432ae4923e0934e23a4c42b1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf627a5ab1f86c4df615ef35dcbe4227898c6ba005d21a0afe7bbac56015fa9`

```dockerfile
```

-	Layers:
	-	`sha256:480b751b13fe5c2f25340d8151c8ed61eb8722e2ab491566e35a7f7cdaf3f6f1`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1aad1b68dd84a97f68d7c89f793d30650db73f655ae9dd0f6f0268bcc13217b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128756188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade40f2aed6c3219ad502e0110acbf89f344b37f32f6ecd9bc36aff5244552f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b17e29ac9e54e576cb04765200626525f96dc401ab614bbc54eb2145157550`  
		Last Modified: Thu, 22 May 2025 02:42:08 GMT  
		Size: 100.7 MB (100688867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e3bb5152055b2725c6ebad6b01752877a4e804b3d8d3af8e16c7590878fe9a`  
		Last Modified: Thu, 22 May 2025 02:42:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a02a085b2688630644cda4682d17d517bc18e61f70125f6690207bb155419d`  
		Last Modified: Thu, 22 May 2025 02:42:04 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1` - unknown; unknown

```console
$ docker pull varnish@sha256:757e93b0ee017bac182544700626a8ae26fcc93799faa6c610d43e5580cdc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ccce5ff2d796096453bef1cde02b0fc8a7fd864e105a6531e44d296d252583`

```dockerfile
```

-	Layers:
	-	`sha256:6afbcf3ccb160b6b79a88ff94546bbfde4ce05798cf2a0a00468afe4d224a23c`  
		Last Modified: Thu, 22 May 2025 02:42:05 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1` - linux; 386

```console
$ docker pull varnish@sha256:459840cdaddcf109cc22f4a13e60eb13eec8078c2751263020b63e58ca3d3ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131537851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4345e460a9ec1a61a6167b276d59f12f88fa841eaef97898deefbeea756927`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0e1b7420750c7ad80b73bb0b5a38934c0b3d489b169108888796b0eb517e3`  
		Last Modified: Wed, 21 May 2025 23:22:23 GMT  
		Size: 102.3 MB (102328321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e36adf8a72f5214761c46f62dba51ea501386ecc7aee9df878eba645b927fe`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b2b528b3cc25073c565cb06deb12e3186235fb0a4c80de54b28ec663757f12`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1` - unknown; unknown

```console
$ docker pull varnish@sha256:c1e8cd6066a3a7368c1f86e6f3a470eec4dbff018fcb14e2f84814a0f6c99c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b84d414ffbffca90b934a952a0da6bb34f54db530a1b904e79c493b59554354`

```dockerfile
```

-	Layers:
	-	`sha256:4cf8b13efc417a94e0f8d146bad31193adeadee7a679411e5e12d6207c259261`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:7d7d355b21c251e67d9b9e85a8f288363a9ad60560a971151378e43846668456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137233020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7b5b5e39554dc9f66a02e3c59fb3371f8678ecfa05941f93381870f6a36d2f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85372ffb9150cd3a320a4bc44ed4b2cdc019a9a1ecb70a111b384220d6116a1b`  
		Last Modified: Tue, 13 May 2025 23:51:11 GMT  
		Size: 105.2 MB (105162529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a8da1e97e0a49a6694eec4aa254842ac3589188d9ef503a15a2c2b9bd4c3be`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e61219f2f71de9614f1131b9292d43311eadd8e856d2a632f6fc28a3d50e`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1` - unknown; unknown

```console
$ docker pull varnish@sha256:fc1ae7f7739a94a83065ee6d28e6def85a575001f37a0dbf579ee9c9091bbdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ff9e1f324990faa5d0bda41d3f97f8c3b02d2a61946c8e69aaba79da6e5566`

```dockerfile
```

-	Layers:
	-	`sha256:92ab709f19228dcc9118cedda83d251b2febd005f9493709cdc69e156b4fa576`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1` - linux; s390x

```console
$ docker pull varnish@sha256:2455f1bc08cbcce52d13fe8aafd3078ffe19fb13954051b395d676273e061f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112354777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694c9e09bf81a75334ff9be6cb3bdd4937b9c1791d01fc9ddce1e8b34326bda2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8299d63723e54463fad083282a50370c22bd894ca037870414a61da1b81a3daa`  
		Last Modified: Thu, 22 May 2025 00:56:32 GMT  
		Size: 85.5 MB (85469923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e21687c812f9934edcfcf1ce07fdbf0c291d184931706496aa49a657e7e794`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51af249f25615e77d6502237bcdee426a95a9e5649761460f178dc5b2fdfe188`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1` - unknown; unknown

```console
$ docker pull varnish@sha256:573a4860c5f251faa947595939b5729f0b0d3fb703e20a598344ce017b44fa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7ec93bc1a67bbaaa5d04f82e69b77595dd5fd0e67ff7c8cb0bb321e30a2d26`

```dockerfile
```

-	Layers:
	-	`sha256:e10caa24f54ad7e91b672430ede572bba41c6b63b5a52bcd4da125bead791f83`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.1-alpine`

```console
$ docker pull varnish@sha256:edbb3bc7c0d80e0222c416c709b09a73ccd2df1cdae3866c7322a241eff4e180
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

### `varnish:7.7.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:259b86a44377185dba18240d733380c541601d25d666b2e9ba9acd577c4dcf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80309670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b284e6450b0b02b8aa6c5ced28b66e12656ba744baa00edecb76fe116c080556`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d09d2ebf1afc734637d3674346c53f56296aec75a61edd0c0344cf312eebb8a`  
		Last Modified: Tue, 13 May 2025 23:47:47 GMT  
		Size: 76.7 MB (76665367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020865b6f7518b5553fb3b5f5f87fe7d769c0bfd8862be571713f33c02335d57`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0716d6cccd5a8c846bee76362aae17be1826d27994c5806f1ce07585b70ff59`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ef0ab02e38b644a555096be9157be1cea81d90cc0f8de591ccb819b98940f00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b8aea16b52858945e38eec85b802ca5db8803f2036a627d258530547fe08c7`

```dockerfile
```

-	Layers:
	-	`sha256:bc90243747f045b359a650c8909062b2318c1499e7f48a798167cbfc7657f381`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8d292ee45a9dc2dfbfed35458b8fa0270f85040da8ee21207a334d4775d8380f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eaef00bc440210de5afb83262c54f02d0ec3c76d7ce72305a6cc82dc53aa03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20465a10cb0623d2638bae875b058ba3f793638be7cb92415040e000c1b76f8`  
		Last Modified: Tue, 13 May 2025 23:50:11 GMT  
		Size: 59.3 MB (59261224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083ea808ed9381df01328a2ef1653df216e9b4da36244e4dcadd17dcdf6e84a`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8794d458a0b8f646fc60add26e4459b4d4c9407b50280e428511293a11520f`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e91eaeeb5f0182b467108b50d78b5afa1b3a461e88852279d5862ea5cfa76cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179782e695fe7a93dca563aee6b50b5bd6c3c7e54edfc68e0641023f187d50f4`

```dockerfile
```

-	Layers:
	-	`sha256:23fdfa5b105ee18314872de802056b5f617360d56d3b086bdda360c3e7016ba2`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 19.6 KB (19597 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b61a409fdd32b44c75e05094b2f8c0a52caf048baee74cf2649889f8ab0c2230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbeb25ac1257f5e8d7c8b6cfd2aa0da22c8c31b371a8efcbf80b4431ba37a24`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218a17e7411247e7ec655ce4aaa9fe4b47d0895bd6e73851ed546667f0fe3e55`  
		Last Modified: Tue, 13 May 2025 23:49:41 GMT  
		Size: 73.3 MB (73320337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5196a02470ffb1dcbdfc7b2cbdb242760b0c07b10d6517ead18d891bb400f4c`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70010398e4917d413210539be9ac7a4403afbbcf085c8329fd7d92cd39012be1`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bb11082a4007faf836d047799e795f81b039d363ed2e41660ed5b9c64291e2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e4eb373937c062aa03046300871c364ec0cddbabb069f4c3727ccdfa2b0dd`

```dockerfile
```

-	Layers:
	-	`sha256:49e2f94d180b1c01ef09860292cee489ba53bf10fe0360ee401da18671f54bfb`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 19.6 KB (19628 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:092d4356881956db83c99181d24d22e18202524f068320f251560a070f0e421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82507424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f042b6c3a995ea20dd8f5d1fef7add00ff33db270e8df2ba861973326fd624`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ae4ff1dba2c4c9b0b650ad779e3fa82323317b6267e07b9e33df3854e9689c`  
		Last Modified: Tue, 13 May 2025 23:48:01 GMT  
		Size: 79.0 MB (79041745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0eb19cec68f9427b98d8d8da7cede7cfc1984fb199d85a714f9e6748446204`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb0373ef72019570b028f9ab8a1d5c7bfe013d9db28e8cb186a763a688a664a`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d91231a035890e7216b1fae2a3345dc0d803273bf8d669cfefcf4d55c73e2b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb327f2a61a25402a9d91889125075436aef52d049ba6290c71057db343a6a76`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b62d3004205f74b9851086a8e111bb2893118e7bcf7afaf4b7da2225ec91b`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f3f0d610397b274b22fb34b680e8ba7e33a72a604d4b1bbf48e4f529a4e12401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76432657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a00d6a6ef80ef24704f5d349a53f4ae3bd9aa4d09d004a67fbc7406b59d288`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8415d72717fd2f47320e78289223b64170d05f5f1c5ed853850b3ec622aca70`  
		Last Modified: Tue, 13 May 2025 23:53:20 GMT  
		Size: 72.9 MB (72856253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9f4c7b61730302b7702086f8672aff08ab5023af2e9cf71e290a1a9ef11d1c`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd285292c92d194571feccdd50b4da84ca96301d53122a96aa8043da2bf1b83`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7daef37645d9b686c2bc329d817a6c02ef1199122ef6728f491b3c255c28c85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cb6ff731d3d100c474d30fba1df224e326ef9c95f84e3076aad50497e3b1f3`

```dockerfile
```

-	Layers:
	-	`sha256:219a42b1eb87f194f15e45b78ecd52a13f1f31912d1d7f2335f307f6a2072e44`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7e05c6940177520cc8383444ba0a8572212bd77a0a49215191a322f8f5ce5e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71031247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff4aa0a5c80674732b38dfef9e8232d2b8e19898c99b389ba7661284018062`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6400ff82abe5ab3b99bdcac59bf46b6dc34bc7216ad735a629cc3bc9ce1375d`  
		Last Modified: Tue, 13 May 2025 23:51:36 GMT  
		Size: 67.6 MB (67561620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264077ca48f381269649e75852fcada29fbe169adccdb4a810c7934e48ddcc3`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b2fae274cd89bc147cb4f042b95d120b3e8db6d5b7281a70e2ff486dd3a2b7`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5fab5a82196b431e4b37a57ed657e8531ecc31f5e49e7fc7c5c191ca880741d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90fc38218c75cfc61c2c19fcbd8fe5f19a38759cefd5e48f936ca64fb508a2d`

```dockerfile
```

-	Layers:
	-	`sha256:c77b5005edf4457d5cc01076ea24907883bbcb850ad767ec13de864f45d7a43b`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:edbb3bc7c0d80e0222c416c709b09a73ccd2df1cdae3866c7322a241eff4e180
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
$ docker pull varnish@sha256:259b86a44377185dba18240d733380c541601d25d666b2e9ba9acd577c4dcf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80309670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b284e6450b0b02b8aa6c5ced28b66e12656ba744baa00edecb76fe116c080556`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d09d2ebf1afc734637d3674346c53f56296aec75a61edd0c0344cf312eebb8a`  
		Last Modified: Tue, 13 May 2025 23:47:47 GMT  
		Size: 76.7 MB (76665367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020865b6f7518b5553fb3b5f5f87fe7d769c0bfd8862be571713f33c02335d57`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0716d6cccd5a8c846bee76362aae17be1826d27994c5806f1ce07585b70ff59`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ef0ab02e38b644a555096be9157be1cea81d90cc0f8de591ccb819b98940f00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b8aea16b52858945e38eec85b802ca5db8803f2036a627d258530547fe08c7`

```dockerfile
```

-	Layers:
	-	`sha256:bc90243747f045b359a650c8909062b2318c1499e7f48a798167cbfc7657f381`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8d292ee45a9dc2dfbfed35458b8fa0270f85040da8ee21207a334d4775d8380f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eaef00bc440210de5afb83262c54f02d0ec3c76d7ce72305a6cc82dc53aa03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20465a10cb0623d2638bae875b058ba3f793638be7cb92415040e000c1b76f8`  
		Last Modified: Tue, 13 May 2025 23:50:11 GMT  
		Size: 59.3 MB (59261224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083ea808ed9381df01328a2ef1653df216e9b4da36244e4dcadd17dcdf6e84a`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8794d458a0b8f646fc60add26e4459b4d4c9407b50280e428511293a11520f`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e91eaeeb5f0182b467108b50d78b5afa1b3a461e88852279d5862ea5cfa76cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179782e695fe7a93dca563aee6b50b5bd6c3c7e54edfc68e0641023f187d50f4`

```dockerfile
```

-	Layers:
	-	`sha256:23fdfa5b105ee18314872de802056b5f617360d56d3b086bdda360c3e7016ba2`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 19.6 KB (19597 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b61a409fdd32b44c75e05094b2f8c0a52caf048baee74cf2649889f8ab0c2230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbeb25ac1257f5e8d7c8b6cfd2aa0da22c8c31b371a8efcbf80b4431ba37a24`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218a17e7411247e7ec655ce4aaa9fe4b47d0895bd6e73851ed546667f0fe3e55`  
		Last Modified: Tue, 13 May 2025 23:49:41 GMT  
		Size: 73.3 MB (73320337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5196a02470ffb1dcbdfc7b2cbdb242760b0c07b10d6517ead18d891bb400f4c`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70010398e4917d413210539be9ac7a4403afbbcf085c8329fd7d92cd39012be1`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bb11082a4007faf836d047799e795f81b039d363ed2e41660ed5b9c64291e2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e4eb373937c062aa03046300871c364ec0cddbabb069f4c3727ccdfa2b0dd`

```dockerfile
```

-	Layers:
	-	`sha256:49e2f94d180b1c01ef09860292cee489ba53bf10fe0360ee401da18671f54bfb`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 19.6 KB (19628 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:092d4356881956db83c99181d24d22e18202524f068320f251560a070f0e421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82507424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f042b6c3a995ea20dd8f5d1fef7add00ff33db270e8df2ba861973326fd624`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ae4ff1dba2c4c9b0b650ad779e3fa82323317b6267e07b9e33df3854e9689c`  
		Last Modified: Tue, 13 May 2025 23:48:01 GMT  
		Size: 79.0 MB (79041745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0eb19cec68f9427b98d8d8da7cede7cfc1984fb199d85a714f9e6748446204`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb0373ef72019570b028f9ab8a1d5c7bfe013d9db28e8cb186a763a688a664a`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d91231a035890e7216b1fae2a3345dc0d803273bf8d669cfefcf4d55c73e2b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb327f2a61a25402a9d91889125075436aef52d049ba6290c71057db343a6a76`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b62d3004205f74b9851086a8e111bb2893118e7bcf7afaf4b7da2225ec91b`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f3f0d610397b274b22fb34b680e8ba7e33a72a604d4b1bbf48e4f529a4e12401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76432657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a00d6a6ef80ef24704f5d349a53f4ae3bd9aa4d09d004a67fbc7406b59d288`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8415d72717fd2f47320e78289223b64170d05f5f1c5ed853850b3ec622aca70`  
		Last Modified: Tue, 13 May 2025 23:53:20 GMT  
		Size: 72.9 MB (72856253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9f4c7b61730302b7702086f8672aff08ab5023af2e9cf71e290a1a9ef11d1c`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd285292c92d194571feccdd50b4da84ca96301d53122a96aa8043da2bf1b83`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7daef37645d9b686c2bc329d817a6c02ef1199122ef6728f491b3c255c28c85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cb6ff731d3d100c474d30fba1df224e326ef9c95f84e3076aad50497e3b1f3`

```dockerfile
```

-	Layers:
	-	`sha256:219a42b1eb87f194f15e45b78ecd52a13f1f31912d1d7f2335f307f6a2072e44`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7e05c6940177520cc8383444ba0a8572212bd77a0a49215191a322f8f5ce5e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71031247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff4aa0a5c80674732b38dfef9e8232d2b8e19898c99b389ba7661284018062`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6400ff82abe5ab3b99bdcac59bf46b6dc34bc7216ad735a629cc3bc9ce1375d`  
		Last Modified: Tue, 13 May 2025 23:51:36 GMT  
		Size: 67.6 MB (67561620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264077ca48f381269649e75852fcada29fbe169adccdb4a810c7934e48ddcc3`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b2fae274cd89bc147cb4f042b95d120b3e8db6d5b7281a70e2ff486dd3a2b7`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5fab5a82196b431e4b37a57ed657e8531ecc31f5e49e7fc7c5c191ca880741d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90fc38218c75cfc61c2c19fcbd8fe5f19a38759cefd5e48f936ca64fb508a2d`

```dockerfile
```

-	Layers:
	-	`sha256:c77b5005edf4457d5cc01076ea24907883bbcb850ad767ec13de864f45d7a43b`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:86e8b8945266a860db142a641b60e919a34eda77f929a51be888b70d41bf6324
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
$ docker pull varnish@sha256:977ab78dc31ecbec4285eced93daf2391dc232d1ee452987a7c1740e902e9973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134432559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffb297b8223b1aae9fe862b8a03a6020f97a7fa4d8dae2134ba59518fcb7f84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ba1e050e4fcf7680bef6d92b2df063c4e527e294143a153dc00f28052a2176`  
		Last Modified: Wed, 21 May 2025 23:22:38 GMT  
		Size: 106.2 MB (106205179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da93242d1418a17c24960555b296029f7b8098770d10353a2e8c308970676138`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef390b256376ce19bd47ce3e975bf48d8d3f6bc71a7c31905c0fed7fc2059d13`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:1e0a03226641f48fdaba83cee24a1cb8e2a8f4827e2ca6f8902508550d83c03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414c6f46ac564e1a77e8f8ef21a1e32c4e2b3c32c7cbee7b00f9f25b8eb101b1`

```dockerfile
```

-	Layers:
	-	`sha256:3e2476437e1f9fe6c21db7b9d507881f836a784072f8c11c79dc9cd63d1f10fb`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 19.4 KB (19446 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c773ab683f23d2cd79e06d85d02996b2b01924bf328e3666f5f9b341cbfd0d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104785075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba66129a0dbe6f325051712cad928cbe8ad18e5800c4efdd574286e9d69f6fe0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac458455152571434f9a6c7df061f113f5a5c2068aef467ef345ac392b3897d6`  
		Last Modified: Thu, 22 May 2025 02:21:50 GMT  
		Size: 80.9 MB (80850108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb358afb88ae9a9c8149e8291ed8f719db1db6307b98ba3ba7e90000641a6b`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a7b99352f7ce860abc258d20d7bb084554b2ebe5306fad771ccb4aed6320fe`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:6c0d75b8f70c4a9a4025686d21d55ce66ae618432ae4923e0934e23a4c42b1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf627a5ab1f86c4df615ef35dcbe4227898c6ba005d21a0afe7bbac56015fa9`

```dockerfile
```

-	Layers:
	-	`sha256:480b751b13fe5c2f25340d8151c8ed61eb8722e2ab491566e35a7f7cdaf3f6f1`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1aad1b68dd84a97f68d7c89f793d30650db73f655ae9dd0f6f0268bcc13217b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128756188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade40f2aed6c3219ad502e0110acbf89f344b37f32f6ecd9bc36aff5244552f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b17e29ac9e54e576cb04765200626525f96dc401ab614bbc54eb2145157550`  
		Last Modified: Thu, 22 May 2025 02:42:08 GMT  
		Size: 100.7 MB (100688867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e3bb5152055b2725c6ebad6b01752877a4e804b3d8d3af8e16c7590878fe9a`  
		Last Modified: Thu, 22 May 2025 02:42:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a02a085b2688630644cda4682d17d517bc18e61f70125f6690207bb155419d`  
		Last Modified: Thu, 22 May 2025 02:42:04 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:757e93b0ee017bac182544700626a8ae26fcc93799faa6c610d43e5580cdc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ccce5ff2d796096453bef1cde02b0fc8a7fd864e105a6531e44d296d252583`

```dockerfile
```

-	Layers:
	-	`sha256:6afbcf3ccb160b6b79a88ff94546bbfde4ce05798cf2a0a00468afe4d224a23c`  
		Last Modified: Thu, 22 May 2025 02:42:05 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:459840cdaddcf109cc22f4a13e60eb13eec8078c2751263020b63e58ca3d3ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131537851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4345e460a9ec1a61a6167b276d59f12f88fa841eaef97898deefbeea756927`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0e1b7420750c7ad80b73bb0b5a38934c0b3d489b169108888796b0eb517e3`  
		Last Modified: Wed, 21 May 2025 23:22:23 GMT  
		Size: 102.3 MB (102328321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e36adf8a72f5214761c46f62dba51ea501386ecc7aee9df878eba645b927fe`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b2b528b3cc25073c565cb06deb12e3186235fb0a4c80de54b28ec663757f12`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:c1e8cd6066a3a7368c1f86e6f3a470eec4dbff018fcb14e2f84814a0f6c99c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b84d414ffbffca90b934a952a0da6bb34f54db530a1b904e79c493b59554354`

```dockerfile
```

-	Layers:
	-	`sha256:4cf8b13efc417a94e0f8d146bad31193adeadee7a679411e5e12d6207c259261`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:7d7d355b21c251e67d9b9e85a8f288363a9ad60560a971151378e43846668456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137233020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7b5b5e39554dc9f66a02e3c59fb3371f8678ecfa05941f93381870f6a36d2f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85372ffb9150cd3a320a4bc44ed4b2cdc019a9a1ecb70a111b384220d6116a1b`  
		Last Modified: Tue, 13 May 2025 23:51:11 GMT  
		Size: 105.2 MB (105162529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a8da1e97e0a49a6694eec4aa254842ac3589188d9ef503a15a2c2b9bd4c3be`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e61219f2f71de9614f1131b9292d43311eadd8e856d2a632f6fc28a3d50e`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:fc1ae7f7739a94a83065ee6d28e6def85a575001f37a0dbf579ee9c9091bbdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ff9e1f324990faa5d0bda41d3f97f8c3b02d2a61946c8e69aaba79da6e5566`

```dockerfile
```

-	Layers:
	-	`sha256:92ab709f19228dcc9118cedda83d251b2febd005f9493709cdc69e156b4fa576`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:2455f1bc08cbcce52d13fe8aafd3078ffe19fb13954051b395d676273e061f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112354777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694c9e09bf81a75334ff9be6cb3bdd4937b9c1791d01fc9ddce1e8b34326bda2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8299d63723e54463fad083282a50370c22bd894ca037870414a61da1b81a3daa`  
		Last Modified: Thu, 22 May 2025 00:56:32 GMT  
		Size: 85.5 MB (85469923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e21687c812f9934edcfcf1ce07fdbf0c291d184931706496aa49a657e7e794`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51af249f25615e77d6502237bcdee426a95a9e5649761460f178dc5b2fdfe188`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:573a4860c5f251faa947595939b5729f0b0d3fb703e20a598344ce017b44fa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7ec93bc1a67bbaaa5d04f82e69b77595dd5fd0e67ff7c8cb0bb321e30a2d26`

```dockerfile
```

-	Layers:
	-	`sha256:e10caa24f54ad7e91b672430ede572bba41c6b63b5a52bcd4da125bead791f83`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:edbb3bc7c0d80e0222c416c709b09a73ccd2df1cdae3866c7322a241eff4e180
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
$ docker pull varnish@sha256:259b86a44377185dba18240d733380c541601d25d666b2e9ba9acd577c4dcf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80309670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b284e6450b0b02b8aa6c5ced28b66e12656ba744baa00edecb76fe116c080556`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d09d2ebf1afc734637d3674346c53f56296aec75a61edd0c0344cf312eebb8a`  
		Last Modified: Tue, 13 May 2025 23:47:47 GMT  
		Size: 76.7 MB (76665367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020865b6f7518b5553fb3b5f5f87fe7d769c0bfd8862be571713f33c02335d57`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0716d6cccd5a8c846bee76362aae17be1826d27994c5806f1ce07585b70ff59`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ef0ab02e38b644a555096be9157be1cea81d90cc0f8de591ccb819b98940f00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b8aea16b52858945e38eec85b802ca5db8803f2036a627d258530547fe08c7`

```dockerfile
```

-	Layers:
	-	`sha256:bc90243747f045b359a650c8909062b2318c1499e7f48a798167cbfc7657f381`  
		Last Modified: Tue, 13 May 2025 23:47:46 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8d292ee45a9dc2dfbfed35458b8fa0270f85040da8ee21207a334d4775d8380f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eaef00bc440210de5afb83262c54f02d0ec3c76d7ce72305a6cc82dc53aa03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20465a10cb0623d2638bae875b058ba3f793638be7cb92415040e000c1b76f8`  
		Last Modified: Tue, 13 May 2025 23:50:11 GMT  
		Size: 59.3 MB (59261224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083ea808ed9381df01328a2ef1653df216e9b4da36244e4dcadd17dcdf6e84a`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8794d458a0b8f646fc60add26e4459b4d4c9407b50280e428511293a11520f`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e91eaeeb5f0182b467108b50d78b5afa1b3a461e88852279d5862ea5cfa76cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179782e695fe7a93dca563aee6b50b5bd6c3c7e54edfc68e0641023f187d50f4`

```dockerfile
```

-	Layers:
	-	`sha256:23fdfa5b105ee18314872de802056b5f617360d56d3b086bdda360c3e7016ba2`  
		Last Modified: Tue, 13 May 2025 23:50:09 GMT  
		Size: 19.6 KB (19597 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b61a409fdd32b44c75e05094b2f8c0a52caf048baee74cf2649889f8ab0c2230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77315419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbeb25ac1257f5e8d7c8b6cfd2aa0da22c8c31b371a8efcbf80b4431ba37a24`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218a17e7411247e7ec655ce4aaa9fe4b47d0895bd6e73851ed546667f0fe3e55`  
		Last Modified: Tue, 13 May 2025 23:49:41 GMT  
		Size: 73.3 MB (73320337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5196a02470ffb1dcbdfc7b2cbdb242760b0c07b10d6517ead18d891bb400f4c`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70010398e4917d413210539be9ac7a4403afbbcf085c8329fd7d92cd39012be1`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bb11082a4007faf836d047799e795f81b039d363ed2e41660ed5b9c64291e2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e4eb373937c062aa03046300871c364ec0cddbabb069f4c3727ccdfa2b0dd`

```dockerfile
```

-	Layers:
	-	`sha256:49e2f94d180b1c01ef09860292cee489ba53bf10fe0360ee401da18671f54bfb`  
		Last Modified: Tue, 13 May 2025 23:49:38 GMT  
		Size: 19.6 KB (19628 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:092d4356881956db83c99181d24d22e18202524f068320f251560a070f0e421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82507424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f042b6c3a995ea20dd8f5d1fef7add00ff33db270e8df2ba861973326fd624`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ae4ff1dba2c4c9b0b650ad779e3fa82323317b6267e07b9e33df3854e9689c`  
		Last Modified: Tue, 13 May 2025 23:48:01 GMT  
		Size: 79.0 MB (79041745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0eb19cec68f9427b98d8d8da7cede7cfc1984fb199d85a714f9e6748446204`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb0373ef72019570b028f9ab8a1d5c7bfe013d9db28e8cb186a763a688a664a`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d91231a035890e7216b1fae2a3345dc0d803273bf8d669cfefcf4d55c73e2b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb327f2a61a25402a9d91889125075436aef52d049ba6290c71057db343a6a76`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b62d3004205f74b9851086a8e111bb2893118e7bcf7afaf4b7da2225ec91b`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f3f0d610397b274b22fb34b680e8ba7e33a72a604d4b1bbf48e4f529a4e12401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76432657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a00d6a6ef80ef24704f5d349a53f4ae3bd9aa4d09d004a67fbc7406b59d288`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8415d72717fd2f47320e78289223b64170d05f5f1c5ed853850b3ec622aca70`  
		Last Modified: Tue, 13 May 2025 23:53:20 GMT  
		Size: 72.9 MB (72856253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9f4c7b61730302b7702086f8672aff08ab5023af2e9cf71e290a1a9ef11d1c`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd285292c92d194571feccdd50b4da84ca96301d53122a96aa8043da2bf1b83`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7daef37645d9b686c2bc329d817a6c02ef1199122ef6728f491b3c255c28c85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cb6ff731d3d100c474d30fba1df224e326ef9c95f84e3076aad50497e3b1f3`

```dockerfile
```

-	Layers:
	-	`sha256:219a42b1eb87f194f15e45b78ecd52a13f1f31912d1d7f2335f307f6a2072e44`  
		Last Modified: Tue, 13 May 2025 23:53:17 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7e05c6940177520cc8383444ba0a8572212bd77a0a49215191a322f8f5ce5e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71031247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff4aa0a5c80674732b38dfef9e8232d2b8e19898c99b389ba7661284018062`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6400ff82abe5ab3b99bdcac59bf46b6dc34bc7216ad735a629cc3bc9ce1375d`  
		Last Modified: Tue, 13 May 2025 23:51:36 GMT  
		Size: 67.6 MB (67561620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264077ca48f381269649e75852fcada29fbe169adccdb4a810c7934e48ddcc3`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b2fae274cd89bc147cb4f042b95d120b3e8db6d5b7281a70e2ff486dd3a2b7`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5fab5a82196b431e4b37a57ed657e8531ecc31f5e49e7fc7c5c191ca880741d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90fc38218c75cfc61c2c19fcbd8fe5f19a38759cefd5e48f936ca64fb508a2d`

```dockerfile
```

-	Layers:
	-	`sha256:c77b5005edf4457d5cc01076ea24907883bbcb850ad767ec13de864f45d7a43b`  
		Last Modified: Tue, 13 May 2025 23:51:34 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:86e8b8945266a860db142a641b60e919a34eda77f929a51be888b70d41bf6324
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
$ docker pull varnish@sha256:977ab78dc31ecbec4285eced93daf2391dc232d1ee452987a7c1740e902e9973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134432559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffb297b8223b1aae9fe862b8a03a6020f97a7fa4d8dae2134ba59518fcb7f84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ba1e050e4fcf7680bef6d92b2df063c4e527e294143a153dc00f28052a2176`  
		Last Modified: Wed, 21 May 2025 23:22:38 GMT  
		Size: 106.2 MB (106205179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da93242d1418a17c24960555b296029f7b8098770d10353a2e8c308970676138`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef390b256376ce19bd47ce3e975bf48d8d3f6bc71a7c31905c0fed7fc2059d13`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:1e0a03226641f48fdaba83cee24a1cb8e2a8f4827e2ca6f8902508550d83c03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414c6f46ac564e1a77e8f8ef21a1e32c4e2b3c32c7cbee7b00f9f25b8eb101b1`

```dockerfile
```

-	Layers:
	-	`sha256:3e2476437e1f9fe6c21db7b9d507881f836a784072f8c11c79dc9cd63d1f10fb`  
		Last Modified: Wed, 21 May 2025 23:22:36 GMT  
		Size: 19.4 KB (19446 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c773ab683f23d2cd79e06d85d02996b2b01924bf328e3666f5f9b341cbfd0d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104785075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba66129a0dbe6f325051712cad928cbe8ad18e5800c4efdd574286e9d69f6fe0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac458455152571434f9a6c7df061f113f5a5c2068aef467ef345ac392b3897d6`  
		Last Modified: Thu, 22 May 2025 02:21:50 GMT  
		Size: 80.9 MB (80850108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb358afb88ae9a9c8149e8291ed8f719db1db6307b98ba3ba7e90000641a6b`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a7b99352f7ce860abc258d20d7bb084554b2ebe5306fad771ccb4aed6320fe`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:6c0d75b8f70c4a9a4025686d21d55ce66ae618432ae4923e0934e23a4c42b1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf627a5ab1f86c4df615ef35dcbe4227898c6ba005d21a0afe7bbac56015fa9`

```dockerfile
```

-	Layers:
	-	`sha256:480b751b13fe5c2f25340d8151c8ed61eb8722e2ab491566e35a7f7cdaf3f6f1`  
		Last Modified: Thu, 22 May 2025 02:21:47 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1aad1b68dd84a97f68d7c89f793d30650db73f655ae9dd0f6f0268bcc13217b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128756188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade40f2aed6c3219ad502e0110acbf89f344b37f32f6ecd9bc36aff5244552f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b17e29ac9e54e576cb04765200626525f96dc401ab614bbc54eb2145157550`  
		Last Modified: Thu, 22 May 2025 02:42:08 GMT  
		Size: 100.7 MB (100688867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e3bb5152055b2725c6ebad6b01752877a4e804b3d8d3af8e16c7590878fe9a`  
		Last Modified: Thu, 22 May 2025 02:42:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a02a085b2688630644cda4682d17d517bc18e61f70125f6690207bb155419d`  
		Last Modified: Thu, 22 May 2025 02:42:04 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:757e93b0ee017bac182544700626a8ae26fcc93799faa6c610d43e5580cdc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ccce5ff2d796096453bef1cde02b0fc8a7fd864e105a6531e44d296d252583`

```dockerfile
```

-	Layers:
	-	`sha256:6afbcf3ccb160b6b79a88ff94546bbfde4ce05798cf2a0a00468afe4d224a23c`  
		Last Modified: Thu, 22 May 2025 02:42:05 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:459840cdaddcf109cc22f4a13e60eb13eec8078c2751263020b63e58ca3d3ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131537851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4345e460a9ec1a61a6167b276d59f12f88fa841eaef97898deefbeea756927`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0e1b7420750c7ad80b73bb0b5a38934c0b3d489b169108888796b0eb517e3`  
		Last Modified: Wed, 21 May 2025 23:22:23 GMT  
		Size: 102.3 MB (102328321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e36adf8a72f5214761c46f62dba51ea501386ecc7aee9df878eba645b927fe`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b2b528b3cc25073c565cb06deb12e3186235fb0a4c80de54b28ec663757f12`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:c1e8cd6066a3a7368c1f86e6f3a470eec4dbff018fcb14e2f84814a0f6c99c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b84d414ffbffca90b934a952a0da6bb34f54db530a1b904e79c493b59554354`

```dockerfile
```

-	Layers:
	-	`sha256:4cf8b13efc417a94e0f8d146bad31193adeadee7a679411e5e12d6207c259261`  
		Last Modified: Wed, 21 May 2025 23:22:20 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:7d7d355b21c251e67d9b9e85a8f288363a9ad60560a971151378e43846668456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137233020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7b5b5e39554dc9f66a02e3c59fb3371f8678ecfa05941f93381870f6a36d2f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85372ffb9150cd3a320a4bc44ed4b2cdc019a9a1ecb70a111b384220d6116a1b`  
		Last Modified: Tue, 13 May 2025 23:51:11 GMT  
		Size: 105.2 MB (105162529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a8da1e97e0a49a6694eec4aa254842ac3589188d9ef503a15a2c2b9bd4c3be`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e61219f2f71de9614f1131b9292d43311eadd8e856d2a632f6fc28a3d50e`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:fc1ae7f7739a94a83065ee6d28e6def85a575001f37a0dbf579ee9c9091bbdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ff9e1f324990faa5d0bda41d3f97f8c3b02d2a61946c8e69aaba79da6e5566`

```dockerfile
```

-	Layers:
	-	`sha256:92ab709f19228dcc9118cedda83d251b2febd005f9493709cdc69e156b4fa576`  
		Last Modified: Tue, 13 May 2025 23:51:08 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:2455f1bc08cbcce52d13fe8aafd3078ffe19fb13954051b395d676273e061f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112354777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694c9e09bf81a75334ff9be6cb3bdd4937b9c1791d01fc9ddce1e8b34326bda2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.7.1
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8299d63723e54463fad083282a50370c22bd894ca037870414a61da1b81a3daa`  
		Last Modified: Thu, 22 May 2025 00:56:32 GMT  
		Size: 85.5 MB (85469923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e21687c812f9934edcfcf1ce07fdbf0c291d184931706496aa49a657e7e794`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51af249f25615e77d6502237bcdee426a95a9e5649761460f178dc5b2fdfe188`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:573a4860c5f251faa947595939b5729f0b0d3fb703e20a598344ce017b44fa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7ec93bc1a67bbaaa5d04f82e69b77595dd5fd0e67ff7c8cb0bb321e30a2d26`

```dockerfile
```

-	Layers:
	-	`sha256:e10caa24f54ad7e91b672430ede572bba41c6b63b5a52bcd4da125bead791f83`  
		Last Modified: Thu, 22 May 2025 00:56:31 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:6bf79e065f11a74652eb56f0423db163bae84cd3013f0f0954e414f553230a2d
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
$ docker pull varnish@sha256:57e478b79e0078859b9ad717500b7a1093ad75a5a7debb383efeb7969e775641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134226518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042814e438be6572f63bb9ee8f6240a87568cfbbf5e9c7df93b78f25ad9a1215`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7961ee463c9cd79cbd0c61a06fea21157f832e20108453ce05726a57fb3fc8d7`  
		Last Modified: Wed, 21 May 2025 23:22:45 GMT  
		Size: 106.0 MB (105999139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a805644002c267c15ec92a3e7147d38647f0b0132ab1420465e8ae17177b5`  
		Last Modified: Wed, 21 May 2025 23:22:43 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b72167e9fa216e8c59d59519f2b6105538d98051775dfa4183595460d6e5d`  
		Last Modified: Wed, 21 May 2025 23:22:44 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e5b420e0900f7ef0c9b97431dd033d49c555f76fee34e06c29e122dde6398195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd809f96b0fb5ad1ef9df86653458b5b949a4d06ea67ca3c5630853689e210d`

```dockerfile
```

-	Layers:
	-	`sha256:75cbf9e831ada7abd87a666144f0b48d3f57152b02deaaadb524e439d795c29d`  
		Last Modified: Wed, 21 May 2025 23:22:43 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:2206778c8fc3cef6b8e2c531ac9061921334ab4257c9e573e26199f7be6e0463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104593411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c77cb0f82042e2bdf6c44034ae7ac355ad83257f93b662b32330861933cb35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0608e408adc671e0a0fed2d25e1dda0bf4b2a1c314aaae45b8d585b597c69fb`  
		Last Modified: Thu, 22 May 2025 02:24:56 GMT  
		Size: 80.7 MB (80658449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea3f89f757c6d373ee992295b1504bd3f0701fb19df6a3e1679f2f70a3c2bc0`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635597c7c7987dba75e13a51c0e182abdc184ded70871d70336cd8a449fbf1f4`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:63da5327089f8c608bfbd4f5b8f003384c0324e738c078c367166048c92978e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65844ee50d3f4752502b0349d6d66591e89a4a003af327a09058542eb2a963cc`

```dockerfile
```

-	Layers:
	-	`sha256:800aeaf1dfccf2f5546b6147bb3aefa8e91cf3d5696e1564ac0e9e1d6c39b29a`  
		Last Modified: Thu, 22 May 2025 02:24:53 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:54c30202598e4aa53a4ae21a8b78e68ba6aae471987b57c810493a7e3abe1a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128550652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8e92e79663c4118b5dc879596aa2bfb575fb931e482df4bdeaf1fe94a22fc6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e103af1b5ba34206099062e4e79bd5d0fbecc71c7e946b91806320efc8767fcc`  
		Last Modified: Thu, 22 May 2025 02:44:50 GMT  
		Size: 100.5 MB (100483330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f717e37f5ad5093f50dbcdcb0c6c62e656ab239b6e41552d5afde92f652d23`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04237c11137fd0a0b0b3a6aedb98001ed46399cac495e49a9d5e35ce91a17199`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e0e92dcc17751fb899955fb174b1d9df59f585eaebb7dd39b21f4848086d625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3120c7d68d62a09723c238c1a7943b4f3bf59414c5f5f3709aa66b6d79f65cc`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b9939c443ccaf2f8aa4e2edd02a5d4aee982d4c0cd46044caf38b047ad821`  
		Last Modified: Thu, 22 May 2025 02:44:46 GMT  
		Size: 18.9 KB (18938 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:c0be393634715d1e41b78c8f6efdf0a090fd8074f32566b2e3ca1761220ac6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131356310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c814ea02d5f19ac759f122f3dbeb7eecc2d86463a9b7875350a34e17dc26f0b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4133fcf0caeb66545bc6dee3845609e05c2ca87d6365bbb2b0a0d6683dfad3`  
		Last Modified: Wed, 21 May 2025 23:22:07 GMT  
		Size: 102.1 MB (102146780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8908cdb8d463a92001659b18fdf6ce92e634cf0078faef364eb35b50357130f`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7bbecf64db50ca5d123b5f31886503aa1eac602a2b0fd2b449ce75b31a927a`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:5d9fb3191e6d735de23a6f756fe912457d339dd87798a43442676df647d353e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497e9fba84fa0c8a083603c75981aa1e4e661cf494e256bc9d38022ecd928ea`

```dockerfile
```

-	Layers:
	-	`sha256:42684ebe804da166517493c0efc329b8f47ca9fca69f03af8c3d99ba788b0ebc`  
		Last Modified: Wed, 21 May 2025 23:22:04 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:73387fdd9dc778ac5b60fc84343b1143dc1345701bd5b873da7905bc95cb622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137045074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08da53c1d76d7f208637512e08ac61614577751a04b9f1c917753d9990756d47`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd435ff69c5c6ed4704ae10b0945972fbf1a4e4dd8c82ff7d948ce03f1aa6624`  
		Last Modified: Tue, 13 May 2025 23:58:30 GMT  
		Size: 105.0 MB (104974584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fba4d4d00841714b3b1541e8423961b5551521b2a12a017f73c0cc0f5fd84a7`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733fde6a0fd126007558fc5d9cb027554c0f140929409dc4f258521cdfdd9ae9`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:90d910179a4bdc3bbca0c977f7ffcd69010efdba4137a846bb14b7eec5f98e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efde49921aa74cbc52b1c73024110e7dae588e2bd50b2d4753190b7b8d0c87a3`

```dockerfile
```

-	Layers:
	-	`sha256:4a0f8e185bc3440975a28df2a29c2a3ae3c3d6c64c95ecb0dd99ec7fffed24a5`  
		Last Modified: Tue, 13 May 2025 23:58:26 GMT  
		Size: 18.9 KB (18885 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:5c96875ade9f46839762abfcb379e350768363e30a4c5e50be4818ca1a55b889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112142571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f916da155d02b53a7023cecfb0ce65928cfa562072a3929673329ebd3473f643`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105703520f036595bff09dffa3717a34106202f63d8a9d509302052079472976`  
		Last Modified: Thu, 22 May 2025 00:59:20 GMT  
		Size: 85.3 MB (85257721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d6faceb45eec5234f31017ce7e88172607eb02f383d2808e802450615e9e42`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61100beed27d3a5c5366963ea68abca2ef2e0556894a100a90ae1778f8589dfe`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:d86a501137d98d51cbc2638bbe416d68e64500738b77577be3f0a7eefc13196e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719bdbb94d7c4efcd614d6f02d3f94ac09d998533b39e6794e773f042aefd623`

```dockerfile
```

-	Layers:
	-	`sha256:9ce1b0b545bcedc8fb0638fec99b372740213c3707ccbcda32a88bba4d4d5d54`  
		Last Modified: Thu, 22 May 2025 00:59:18 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:cb268b57c8a2cec3d39e8e4f74382646c8795718ff25aa57c0d0a5ee3eb1146f
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
$ docker pull varnish@sha256:832539f3c49155c868d6e605b23d11635697ee79308d4d67632bfd80a3592470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef6a698cd1a97012baa9bdd2db973a223ae7b7500b68afd5d7a2849cffaf42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dd875d896754e31f106b279b13f6496adc8421db2c4f87731e3e4723097d55`  
		Last Modified: Tue, 13 May 2025 23:47:56 GMT  
		Size: 76.5 MB (76480503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e6d4496a56a4cdc28e0728f444aca412abcdbf44de2a17517f260143d2445`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe2dce4d3db4cb8f19e79b85dd340da315f5a6503c0177d857e7d710bad2e19`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:745b542be3ade7260c951fd0df6eb7803b1d483c633be4bbe214419631ee5ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbc11303947e59091cf3071eab27aa971a25b9b73cfbb7832b60329497a50ab`

```dockerfile
```

-	Layers:
	-	`sha256:f89f56e4fa97bf3b52dbeb162f579e87f78751ccf4665eafdf273436ff4d5639`  
		Last Modified: Tue, 13 May 2025 23:47:55 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c6f15a90cf4d116fb28f39ecb012995aefb0ecd49c02fa0bd9aeec4adf65cebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62177159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348b5a86113885af2ad1ae03b67a656675d858bac28550d8756c22fb352073a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b64d240de8405e58901ffaa351cf6d995f373610fee29e4806ebafbe8f51b4`  
		Last Modified: Tue, 13 May 2025 23:54:33 GMT  
		Size: 59.1 MB (59076980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f345bef6ca24ad7825007178523af189952fa489de9d8eb18ddad503404c52e`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb03c9836d2f802ac7a200af8b7b5a3d37f070eb40a1fca06426d08cf583d3`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:341536aa96b8653cdc7655ab75a700a74a413abb92fbd62c9736a51d288996b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ccd8901dac22a6fcb8114bc93626ea4a138d3c97c173fc51ce70e0fff5f590`

```dockerfile
```

-	Layers:
	-	`sha256:9df71e7bf646620391b06844710aa5d6a127203721dbbdce0a0b070fe4301319`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:03050dcb8e1b8c436dd6bb97d15cd02ce355fb92d5b0f4fd2a9d87236bacd7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa12c01235c01884aba1beb3ce7e3764811403422085d6361e69b7f7e89a142`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d0112c73e93ba409991084c46b91c454e8873ad85d1a0c704da073c738110`  
		Last Modified: Tue, 13 May 2025 23:53:47 GMT  
		Size: 73.1 MB (73139804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d5db8d46da3afc53cd359504e09f6a3822ceefd1859d19b3d76bcffdefa2e7`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15afac65ae6f31067843e3de68aa1266f07ddce142c1ae08692d23030bee350b`  
		Last Modified: Tue, 13 May 2025 23:53:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:79357498a90f86e478600efa6dccae02abc17f66981aec1940ea28ced6fd52f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d5e0e50d45a1f2ae76d217647b08bca1f59442495bc5c01e2f0ba8c9079ca`

```dockerfile
```

-	Layers:
	-	`sha256:56e88217b045f05b58b9caa245c23fded45cf4a2be1d1c230f34b1b574fb44e4`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:501e68fff243f1b20a14eb50b92274eb17d3668b18614971adbe63c11f567f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82330387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0ee568acabd5eb2489c8492d7ccfa16f09434e29b4969f6f9772f2e41aa022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b78442a5d78ba9003dcc9cdc85c9df4f9cfafb1ad42b203d6ac1ea49040aab4`  
		Last Modified: Tue, 13 May 2025 23:48:04 GMT  
		Size: 78.9 MB (78864705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b116832fccbcf9a985576f61c96fe8c6bd152de5d63b1d3584e815df6cc8030`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004edc5aa7acec0262bd1823f0da31ecb8e70efaf37858b2ea6ca28bf441780e`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09e44671e22716a149f4d002f38e34628f91c212ba0e3057686c99a07ab0e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e286f1515be59ef428b8da884b540ac598ed7f2a8b8e6f64ea9635f564882715`

```dockerfile
```

-	Layers:
	-	`sha256:725f13bcaad1fad6dc735aa5a28fbbe6d5b682b7282865560844161fc6878b0b`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f71a73be8317c4072b991ee98c4c3d8eadb24d188800178968beb834c5724d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76254322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae39867711695ca6650e67c074879731c99cebcdfc99080d153b82a437bbd0c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c9b258186a0fcc1c5c8c94beeb1d5bb81c0ab46f616ce67e7a00bf431cc4a3`  
		Last Modified: Wed, 14 May 2025 00:00:26 GMT  
		Size: 72.7 MB (72677915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e89d21db4cd9964b28450f72cf636a52889cfe69f1d4cb2f242a5a3d2ad350`  
		Last Modified: Wed, 14 May 2025 00:00:25 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b02ea0fef7a75f4975001831e3cc80c4fc8904726393c3c240acce25932a96`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b8bb1c1c7e7e8608aacbef7f0b606beb2db199da80c18d189ad22ba69cf00370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6951c078ba75ba3eb2418cecd3a1e5b91a4373905eabd1a4d5caee74b8d56e9`

```dockerfile
```

-	Layers:
	-	`sha256:cfc6a58d241c77836c04f39e0e1a7adfe81d3ee28a3f7889eec06d865211a268`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:01893f1c5743b8d2b36383618902945cba7b093649f09519ebe158ba9f5f8b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70859326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd196cc640f60dfe5eaa365485db2e8c6aac01a37f71995a8895ac495f0e5587`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb58c2794411aa50dc12dbb79cdf53b10c92442248361dbe2644b83e7d4d2ba`  
		Last Modified: Tue, 13 May 2025 23:56:19 GMT  
		Size: 67.4 MB (67389700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a824335bb1eb8cfc81d98eb1052441a94a5806fa9e3d060cb71f520520d0bf74`  
		Last Modified: Tue, 13 May 2025 23:56:17 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31dbfe4dde5d97940cea5e1c9a3d64dbc3d17c8aaba5d04926e5a54fe250069`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82c172006540f09f9dd5322d8d9f23fda47f1ad037a7196f60115a40f504927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c75b90bd5fa7d9fccf356e10d78df6ec4e00a7a88ad8dd24d0ec915d5e64412`

```dockerfile
```

-	Layers:
	-	`sha256:68c68e03488141b66b6f577ded0927247796d3cc30661286e556cf227077b16c`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:e02631edbd9d11b0a469dc692fcc2c02df253e2ad2b462bfd2c673e1a26c56b7
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
$ docker pull varnish@sha256:f53b607d8fbeaf3b2965bb9a21f21ac15b5e019cf1adf36a78345258f242683c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f6da4b8adb77c3151c2bf7f5905b9636d09b2c4e1c1a962ad4217f98cc826c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238b18ac43560146d207c70490bece959b1bd7136aaa73401ce701ffb9bcc00`  
		Last Modified: Wed, 21 May 2025 23:22:00 GMT  
		Size: 99.5 MB (99518441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b473f68ca08352ea6bd1b9ec160db2cad3996f649dfbffafd7342553f3214e`  
		Last Modified: Wed, 21 May 2025 23:21:53 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:6972ed59c52893951900efe0d2a733ef7147a6da5b92242ffae5b5c36289a8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344aa08bd59f0208e0df8e7f1b4ca36dcc37aebf6e17777aaa4cf8d50a52b662`

```dockerfile
```

-	Layers:
	-	`sha256:a878b1e3d527f3802b44f7444bc605efe0ed647ababbac29be9db00f09677633`  
		Last Modified: Wed, 21 May 2025 23:21:53 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4d61dd84dea5fbc2c947c036bab3c341b2450b15e0c534c22984862dab2b73ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98274408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377625a439ab30859fa91034c1e9db518ab21b522a1ef66dfabfb71331ea02c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd34f616817a66c7206e8aec9dfe10604efb19a7a1452e939f4907689517b77`  
		Last Modified: Thu, 22 May 2025 02:27:18 GMT  
		Size: 74.3 MB (74340734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f263be4914f430a97cea2ca9bb05fee17a2b2d0a7f0cb3e435de87d04f7dd2c`  
		Last Modified: Thu, 22 May 2025 02:27:15 GMT  
		Size: 720.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:eae52885341d740b1cf17b763287aaa5f9dbddd81703f25b5344f0b2540e41e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b96b1060bb82b49993bf24fd8248e3004cd2053bd5cc5899d4f59fa437a00c`

```dockerfile
```

-	Layers:
	-	`sha256:f79f175fcfc04b47a05edf164e0fdd4e41519cff560ee36e160889e0cde6c68a`  
		Last Modified: Thu, 22 May 2025 02:27:15 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:23a968c01d282408a77e8198e94b2b44458d29d8f9aae33a80711bf7c7ee9377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122381016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8983e6c89348fdf4ff8cca4dac8200ff62b733d32a04672998cb633a37048c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10aeb6b7f48e4a7c5a5414b5dd6194ebb7f1f3efe2b98f602c29056608722dd`  
		Last Modified: Thu, 22 May 2025 02:46:51 GMT  
		Size: 94.3 MB (94314982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fba76c616734d324ddfe18e475795d32353cfbfd51fa3472f4d03c0ac58b47a`  
		Last Modified: Thu, 22 May 2025 02:46:48 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:2373fe0925df778658a1326d6ee59fad2bf302c7695720206d2b4ce52a6d7c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33be93909afdd4226908932632552ed2715be579068b72591b2a5e5e26e62db`

```dockerfile
```

-	Layers:
	-	`sha256:de85b8ca851879f11bdcf84c9575e0e885c36e2b7f819a76821be96619159c2c`  
		Last Modified: Thu, 22 May 2025 02:46:48 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:4d8954e4be622564882c2572d4be864845b05684bf66328c56c0c57c4d1dabec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124908579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61edd70e79541d3ea796b62ae52a3db383964009a9c0d8b5d3f29d750c6104b6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76b2de6c1cd22ab5564b1df01c1391f959c84b557d26d611f761b6e1925490`  
		Last Modified: Wed, 21 May 2025 23:20:55 GMT  
		Size: 95.7 MB (95700339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940c9819b00cb793425d8fc4a9fd18f97dacb286e88c676fa021e581add8b937`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:6ea5ed35179185a8fed81b68fd5b038009d80595951a10d2c7b76e6020c5432b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244cf4053f351a54ff8b2e2f6d0e27ec3f4cde67bfe1d3ef98eb75d328f8f61c`

```dockerfile
```

-	Layers:
	-	`sha256:9e12afc6d20c0f5d9893d474fe57bf0985dbaaba510709a544752083c2164afb`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:34447fca426a5d5fe08b9f8e9a1ecde2c4ec456200349bd81af272776473daf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130417116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a33d29837032baae03a73cdef6f3cdeebf2b023e209d1362ba70d2feb8ab45e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ddc7fd38cef02cc6c6fc6a5fc5c32d3b3b93dff5dd6e58a4ae35db96d93eb`  
		Last Modified: Wed, 14 May 2025 00:05:05 GMT  
		Size: 98.3 MB (98347918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31a65db2dd65a79300357dbea9a209652f91fdaeabd0861156cbb96fb53bd81`  
		Last Modified: Wed, 14 May 2025 00:05:02 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:b73ca8ea1d6d380fba641683fcc179d9ad1a94b69ba76e2051d50aeae0318bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fb8cec5bb9a7fa54d8fdb676a975e2740ccf004d4601bafb4bbf5bcb239a26`

```dockerfile
```

-	Layers:
	-	`sha256:c6bf3f06141a8df1e36083cb4dd00321da8372b285a3647953a8dfcfcf75fa78`  
		Last Modified: Wed, 14 May 2025 00:05:02 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:2a5e512d2ad441521129b845d46d80255b2ae0936909068062a476b04918c249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105623860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e03ee5fe6c9edb5086346089f27d6cdafebc57aa1dc6ed83ba60e61a01803`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce50e919b295f01d51d4e557f761ea2540b245fdbf5c80e8dd4f5efc4c3358e`  
		Last Modified: Thu, 22 May 2025 01:01:15 GMT  
		Size: 78.7 MB (78740299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec345b4d9f127d20b425df582f3136695d5deb850d7692520f52f62d0068a7`  
		Last Modified: Thu, 22 May 2025 01:01:13 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:8ecd2a0591197a879c4401602eb8812b6a07db8cfe143d13067dd65825440bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872cde2c29a3c2394016bd5fd1ac8f90a04bc2fd2c669487b16a9ab00e7d96d6`

```dockerfile
```

-	Layers:
	-	`sha256:57f9f532bed20d2dbff835d4b678d8968eb1512eafcf1d6fbc12ca96fa5904f3`  
		Last Modified: Thu, 22 May 2025 01:01:13 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json
