<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.10`](#varnish6010)
-	[`varnish:7.0`](#varnish70)
-	[`varnish:7.0-alpine`](#varnish70-alpine)
-	[`varnish:7.0.2`](#varnish702)
-	[`varnish:7.0.2-alpine`](#varnish702-alpine)
-	[`varnish:7.1`](#varnish71)
-	[`varnish:7.1-alpine`](#varnish71-alpine)
-	[`varnish:7.1.0`](#varnish710)
-	[`varnish:7.1.0-alpine`](#varnish710-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:f28e4d5218f748b4cc583d5479bd50ce28f686cb26b6a11394c2b11324ff0116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:8b44a4c2f06876e38f998ac52b1b5eeb5722217b1374ed6d1d2a86788063b841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100590037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0388102969cbf53831d827235b7c512314159ef8b62c62f62e56a42be8eec33f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:19:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 15:24:19 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 15:24:20 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 15:24:20 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 15:24:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 15:24:20 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 15:24:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1ca7fca2c8edea4f001c6fca0411697c9d5e56f8492bd1ba90f2a6096bda2e`  
		Last Modified: Wed, 20 Apr 2022 15:25:40 GMT  
		Size: 69.2 MB (69210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c25bb177ab25201b8d89d4a7ac60b0cd82e581b252db5ae6cec2d81e09f09fc`  
		Last Modified: Wed, 20 Apr 2022 15:25:30 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a2f0a9f702cf2b39ca80ffcb82961a60bbc68a8fc5d37a62da0a6212f3d29eb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77224693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f98b4a10b8edfdf6e66d2ac8f10b34ba94b3ef543e44fb25f6a2cefa40be1f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 14:05:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 14:12:34 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 14:12:36 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 14:12:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 21 Apr 2022 14:12:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 14:12:38 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 14:12:39 GMT
CMD []
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d7b88c6c49f137f382e6f87256bebefe35ee1bd250c2be3c5e92b4a4b41e1`  
		Last Modified: Thu, 21 Apr 2022 14:15:09 GMT  
		Size: 50.6 MB (50648234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddb1c28572171a2274f9094026118a450de3eebfa5127411281f12f60b0c000`  
		Last Modified: Thu, 21 Apr 2022 14:14:51 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d06ba1b2751ee17970be1dc7fef64bface39548af4c87d52890dcbbff810f0f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94712514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17558ce401d3d5978e7c221146ee2ea1938db7212681314b424199f9f6c69838`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:51:42 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:58:54 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:58:54 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:58:56 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:58:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:58:57 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:58:58 GMT
CMD []
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd8694684e136aa212a9714d153d127c234e4c7d0fe71e03e3a5d6ab9813ecc`  
		Last Modified: Wed, 30 Mar 2022 01:00:18 GMT  
		Size: 64.6 MB (64647503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b730ab0811c67684f9f78f611e358243f883c3320a1230f8d22e28a385cd44`  
		Last Modified: Wed, 30 Mar 2022 01:00:08 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:ff04e6a007e6477f911cd890847e670d56ab77a595548f59b111b44b98f41f08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102072699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192058a187a8c2923c5d6916640d33fa10d39b60240d19c2114bb6d2b005b374`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:23:01 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 17:27:47 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 17:27:48 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 17:27:49 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 17:27:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 17:27:50 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 17:27:51 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fcee3146dcc754b299a98036e48fa76f36f7c629a2890bf5436b42ea38d7e1`  
		Last Modified: Wed, 20 Apr 2022 17:29:40 GMT  
		Size: 69.7 MB (69682400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb9c6d70bc7f4ae0e7a597a5a18364592f3bb2c33ebebf45756093ee888959`  
		Last Modified: Wed, 20 Apr 2022 17:29:30 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:c7e3a8a346402ae2dd6a844b519b55d8d7663f9b80c6064e30033a9bc6b23a27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99793645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbc5db50ecdce77bbf9a3bd8d0dc77aeac9f3c827e5b34a2f6d1d562e3611d6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 07:26:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 08:04:12 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 08:04:17 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 08:04:18 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 21 Apr 2022 08:04:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 08:04:22 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 08:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0d43e60a69dfadc43a5b66afb309fb7f38786253c4803557286895cb860d01`  
		Last Modified: Thu, 21 Apr 2022 08:06:41 GMT  
		Size: 64.5 MB (64507698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527abc12e54faba92bbdaaba9677b139501ea022a7793c0e8dee979ed6f4822e`  
		Last Modified: Thu, 21 Apr 2022 08:06:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:cd6e1971c7ba432941c074af2f67998deaf2299a8bbcce272da8af78a9438076
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81008041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cb6823bbeb84e6a370bc9981d400a4c30acbc5d79ea21c30fac05dba331fb9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 19:58:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 20:02:44 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 20:02:47 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 20:02:47 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 20:02:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 20:02:47 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 20:02:48 GMT
CMD []
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dd8f2c1b1715ce878a36dc931f63e342a10035c85178754400d59ffcb7845a`  
		Last Modified: Wed, 20 Apr 2022 20:04:13 GMT  
		Size: 51.4 MB (51352538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38455ce12c1b61bfdfdf5b127f16bf342c77d82e2f0c101325a6837a5674db0`  
		Last Modified: Wed, 20 Apr 2022 20:04:06 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.10`

```console
$ docker pull varnish@sha256:f28e4d5218f748b4cc583d5479bd50ce28f686cb26b6a11394c2b11324ff0116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0.10` - linux; amd64

```console
$ docker pull varnish@sha256:8b44a4c2f06876e38f998ac52b1b5eeb5722217b1374ed6d1d2a86788063b841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100590037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0388102969cbf53831d827235b7c512314159ef8b62c62f62e56a42be8eec33f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:19:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 15:24:19 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 15:24:20 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 15:24:20 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 15:24:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 15:24:20 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 15:24:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1ca7fca2c8edea4f001c6fca0411697c9d5e56f8492bd1ba90f2a6096bda2e`  
		Last Modified: Wed, 20 Apr 2022 15:25:40 GMT  
		Size: 69.2 MB (69210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c25bb177ab25201b8d89d4a7ac60b0cd82e581b252db5ae6cec2d81e09f09fc`  
		Last Modified: Wed, 20 Apr 2022 15:25:30 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.10` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a2f0a9f702cf2b39ca80ffcb82961a60bbc68a8fc5d37a62da0a6212f3d29eb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77224693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f98b4a10b8edfdf6e66d2ac8f10b34ba94b3ef543e44fb25f6a2cefa40be1f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 14:05:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 14:12:34 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 14:12:36 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 14:12:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 21 Apr 2022 14:12:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 14:12:38 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 14:12:39 GMT
CMD []
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d7b88c6c49f137f382e6f87256bebefe35ee1bd250c2be3c5e92b4a4b41e1`  
		Last Modified: Thu, 21 Apr 2022 14:15:09 GMT  
		Size: 50.6 MB (50648234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddb1c28572171a2274f9094026118a450de3eebfa5127411281f12f60b0c000`  
		Last Modified: Thu, 21 Apr 2022 14:14:51 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.10` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d06ba1b2751ee17970be1dc7fef64bface39548af4c87d52890dcbbff810f0f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94712514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17558ce401d3d5978e7c221146ee2ea1938db7212681314b424199f9f6c69838`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:51:42 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:58:54 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:58:54 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:58:56 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:58:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:58:57 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:58:58 GMT
CMD []
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd8694684e136aa212a9714d153d127c234e4c7d0fe71e03e3a5d6ab9813ecc`  
		Last Modified: Wed, 30 Mar 2022 01:00:18 GMT  
		Size: 64.6 MB (64647503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b730ab0811c67684f9f78f611e358243f883c3320a1230f8d22e28a385cd44`  
		Last Modified: Wed, 30 Mar 2022 01:00:08 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.10` - linux; 386

```console
$ docker pull varnish@sha256:ff04e6a007e6477f911cd890847e670d56ab77a595548f59b111b44b98f41f08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102072699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192058a187a8c2923c5d6916640d33fa10d39b60240d19c2114bb6d2b005b374`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:23:01 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 17:27:47 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 17:27:48 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 17:27:49 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 17:27:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 17:27:50 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 17:27:51 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fcee3146dcc754b299a98036e48fa76f36f7c629a2890bf5436b42ea38d7e1`  
		Last Modified: Wed, 20 Apr 2022 17:29:40 GMT  
		Size: 69.7 MB (69682400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb9c6d70bc7f4ae0e7a597a5a18364592f3bb2c33ebebf45756093ee888959`  
		Last Modified: Wed, 20 Apr 2022 17:29:30 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.10` - linux; ppc64le

```console
$ docker pull varnish@sha256:c7e3a8a346402ae2dd6a844b519b55d8d7663f9b80c6064e30033a9bc6b23a27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99793645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbc5db50ecdce77bbf9a3bd8d0dc77aeac9f3c827e5b34a2f6d1d562e3611d6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 07:26:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 08:04:12 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 08:04:17 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 08:04:18 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 21 Apr 2022 08:04:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 08:04:22 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 08:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0d43e60a69dfadc43a5b66afb309fb7f38786253c4803557286895cb860d01`  
		Last Modified: Thu, 21 Apr 2022 08:06:41 GMT  
		Size: 64.5 MB (64507698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527abc12e54faba92bbdaaba9677b139501ea022a7793c0e8dee979ed6f4822e`  
		Last Modified: Thu, 21 Apr 2022 08:06:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.10` - linux; s390x

```console
$ docker pull varnish@sha256:cd6e1971c7ba432941c074af2f67998deaf2299a8bbcce272da8af78a9438076
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81008041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cb6823bbeb84e6a370bc9981d400a4c30acbc5d79ea21c30fac05dba331fb9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 19:58:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 20:02:44 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 20:02:47 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 20:02:47 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 20:02:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 20:02:47 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 20:02:48 GMT
CMD []
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dd8f2c1b1715ce878a36dc931f63e342a10035c85178754400d59ffcb7845a`  
		Last Modified: Wed, 20 Apr 2022 20:04:13 GMT  
		Size: 51.4 MB (51352538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38455ce12c1b61bfdfdf5b127f16bf342c77d82e2f0c101325a6837a5674db0`  
		Last Modified: Wed, 20 Apr 2022 20:04:06 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.0`

```console
$ docker pull varnish@sha256:0bab3835b20068d32e145d205665570fe25e4b9b36d2d9ecc532264fcb706fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.0` - linux; amd64

```console
$ docker pull varnish@sha256:cd8bbaedc6acc855d4dbde0ecbf144ffcec08ace28141a028c267a6108d5b0f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101201770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7492119e1c0f61a7ae796bfccb2774a6385a197b85402151a6b769604b65154b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:19:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 15:21:57 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 15:21:58 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 15:21:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 20 Apr 2022 15:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 15:21:58 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 15:21:58 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d4c26eb233b1f26ae0b9467fa72834229ed3d194ae98dec875b7e27670be4`  
		Last Modified: Wed, 20 Apr 2022 15:25:16 GMT  
		Size: 69.8 MB (69822317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113ca7b5e4d8bea5c4f3cfdbde42d78cedc9cc7a3f232dae8075ac49a7c6ef60`  
		Last Modified: Wed, 20 Apr 2022 15:25:06 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e4f991ee0fffceb5b576bf52af2f4187fa1c3545a35d9a27eaba2fc0f3816e20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77821225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fac8014668438566fd29bc6e67db06f71eed12ebc7deedfd06a14e3b9fc451`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 02:18:34 GMT
ADD file:e1835d1a0c70a0335757f211893e5d12ddf797e489e10434c0982bdf9b234f67 in / 
# Tue, 29 Mar 2022 02:18:36 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 04:58:07 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 05:03:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 05:03:41 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 05:03:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 05:03:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 05:03:42 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 05:03:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f98812e1a494a683a5b3dea593dd2ef305f5f732193044c147f22e44b00164bc`  
		Last Modified: Tue, 29 Mar 2022 02:34:13 GMT  
		Size: 26.6 MB (26575370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f7b6d4c7611e504f11c8135d715741175aae45a8b5c8f9fd2a514cf69022e5`  
		Last Modified: Wed, 30 Mar 2022 05:09:52 GMT  
		Size: 51.2 MB (51245383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761275f2ac473d69f8c0c3ec1b4b46d5d9572a82bac140e031cb00ee8ffbffb3`  
		Last Modified: Wed, 30 Mar 2022 05:09:24 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ea65c75635fd3e13c03da16c68995ed4f38ae3b63ffd798fd210a7470fe0be2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95311405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b7b74bf809ee04653fc225dc513a72a1bc98e4600df9d6ab8745e3df50fd09`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:51:42 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:54:27 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:54:28 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:54:29 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:54:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:54:30 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:54:31 GMT
CMD []
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b31818a80ab96d113ecc26bae4c921e8b1f15bd573c0567be45beb836048700`  
		Last Modified: Wed, 30 Mar 2022 00:59:33 GMT  
		Size: 65.2 MB (65246620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa175bc0d41052fdda42c92374ca4cf78d073d37324d6526efe02454a651cd`  
		Last Modified: Wed, 30 Mar 2022 00:59:24 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; 386

```console
$ docker pull varnish@sha256:259397fb199c0e9f739100dd0a93efb9a86e60827e66c65ed051b3e44ad83b93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102585485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01443ed33f01c5f1b4ed80c2b5351ad547ab887260ae9a4db797dc6623f747a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:23:01 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 17:25:18 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 17:25:19 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 17:25:20 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 20 Apr 2022 17:25:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 17:25:21 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 17:25:22 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47edc9eab3e86eb0355d68502318a630dc795c5d8d4d8779d7321b6b553cf98`  
		Last Modified: Wed, 20 Apr 2022 17:29:13 GMT  
		Size: 70.2 MB (70195418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aea8a62b1f5f50f6761a32239f5adc670e7af72f8b59664619186ddeae2fef`  
		Last Modified: Wed, 20 Apr 2022 17:29:04 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:9dfbab1f66da09461280e2006a8637a71cacc99345a3e005eb4cdd75f34e0057
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100376258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84ffd81229d9e36b2fe44a2d56797edb9d2f84a293a32b202b77177c2d0aa18`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 07:26:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 07:44:15 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 07:44:20 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 07:44:22 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 07:44:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 07:44:27 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 07:44:30 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddab9d225e329687fa4c9dbced15d44e0e90e64944867273cba0d7432395dfef`  
		Last Modified: Thu, 21 Apr 2022 08:06:05 GMT  
		Size: 65.1 MB (65090535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761715f8917a3a374aa705b10b377f1eb661cb0b7c33a6bc93d79f00ac0dede5`  
		Last Modified: Thu, 21 Apr 2022 08:05:52 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; s390x

```console
$ docker pull varnish@sha256:7b2d1d1fc79b00edd1129e176ec751b1c9e3372c2dff553327f9e66c3f00c57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81637417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af65f783a437fab01c28d0c2ade060a88aa9cded965a28602d723c9c41d8a18`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:51:57 GMT
ADD file:39c5e0d7a686abd19448ab3e6237d50955ae2187fc2b64289a08c2549352b8f1 in / 
# Tue, 29 Mar 2022 00:51:58 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:54:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:56:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:56:42 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:56:42 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:56:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:56:42 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:56:42 GMT
CMD []
```

-	Layers:
	-	`sha256:ffb22bcde95509bb75f6dd2d69f3fdb5c7471727e4d720b31d92cd297582865c`  
		Last Modified: Tue, 29 Mar 2022 01:04:43 GMT  
		Size: 29.7 MB (29655426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aabcd8580e9559702629fa9ee5e4029a5b1318fe425c2ae5725d6e84a8c2e0d`  
		Last Modified: Wed, 30 Mar 2022 01:00:29 GMT  
		Size: 52.0 MB (51981518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac10509f97438a4a52957c04e3ce7ad59423d6b7f865b29a3d1462ec09ea52e`  
		Last Modified: Wed, 30 Mar 2022 01:00:25 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.0-alpine`

```console
$ docker pull varnish@sha256:a96966b666c3eb795b5a5ffe4b7f1911e009156774d5551a355de6ba17dd6ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:1f798a786c909e75214591ae7bb11711b606d19904771e17cac071e3fc945f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58347562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f303a05efad59d4625679d65998e25ac6af2a5a1e8e761d6165038faf0af7a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:46:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 09:47:16 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 09:47:16 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 09:47:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 09:47:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 09:47:16 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 09:47:16 GMT
CMD []
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd49c5f702ffa093526e350e19af19adacee36ebd21a4d2b8215729aebd24701`  
		Last Modified: Tue, 05 Apr 2022 09:48:23 GMT  
		Size: 55.5 MB (55528711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b11f3cacc52df447f6e49ab5dcad0b25a3e95d3aa5ca786c8a00b94bcea4d97`  
		Last Modified: Tue, 05 Apr 2022 09:48:15 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d0ef8137631136de68aa9ca8b5a1c202753588e4823091fc74c7381800475e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44158672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b498faee8096b05f4ad1e1a034d79076f1405006bbb01cdc1b62443d19faf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 19:12:30 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 19:13:58 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 19:13:59 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 19:13:59 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 19:14:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 19:14:00 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 19:14:00 GMT
CMD []
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a122a3f3e3f4f262ecd7c937fb5b761d7c7025f6b85195b6f6e59efccc3e22`  
		Last Modified: Tue, 05 Apr 2022 19:17:11 GMT  
		Size: 41.7 MB (41730222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e23c5ffb616fb8979712f573ce76a21ff2948ffe3c222f25abeda1b044fb82`  
		Last Modified: Tue, 05 Apr 2022 19:16:49 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:287bbe458761ddf7b90152156bcfcf1680e8229b94e87c6be21fcdcff4105325
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51100328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb806b4ff6eae8a70eec669d64a63205e9fa899f74021c50544a8a3fe8492216`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:24:20 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 07:25:05 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 07:25:05 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 07:25:07 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 07:25:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 07:25:08 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 07:25:09 GMT
CMD []
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c097d0722cedf772b294574bd3df3ea7bc3fd2a7f0d584bdda75906ab4a4f76`  
		Last Modified: Tue, 05 Apr 2022 07:26:39 GMT  
		Size: 48.4 MB (48382460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda2d05467662609f11c35127449028bdba318e2920842c0c49a157d72fd14d4`  
		Last Modified: Tue, 05 Apr 2022 07:26:32 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:8d9a98e8ebe8c794faad1ca62b64b1d0f5d50b4bdc61593272165af938c90e58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58550969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b86a5912210274cdd2be334341ab5c8a5cc8b98b8cacbf00d0bc3b61391b34`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:38:32 GMT
ADD file:6508514d43b69774a3307679ef8f6dba0faf707e62ad6c6c1c8cf40d84e12d1d in / 
# Mon, 04 Apr 2022 23:38:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:44:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 06:45:29 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 06:45:29 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 06:45:31 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 06:45:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 06:45:32 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 06:45:33 GMT
CMD []
```

-	Layers:
	-	`sha256:c11e5e1035714514f6e237dffd1836a4d03b48af64e55a8e08f9bd9e998e24a9`  
		Last Modified: Mon, 04 Apr 2022 23:39:35 GMT  
		Size: 2.8 MB (2821213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781285b91779b0524f4a4b362a85bf7ad3c11049ec60271bc351d3ea22722f55`  
		Last Modified: Tue, 05 Apr 2022 06:47:18 GMT  
		Size: 55.7 MB (55729277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ede4c98a857e7e2e4374c87b05da88e9cfa36a1b9d2261f338a8e4cc091689`  
		Last Modified: Tue, 05 Apr 2022 06:47:09 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:99fc715aa51f45f415d42e16933cfd6640741633a9df875d1be9c41bb5eea1e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48200204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afb3e6b26fed2aaed2bdf33c3edb6718410d71cdda8521c1e6a42a745e020d3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:52:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 10:53:50 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 10:53:55 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 10:53:56 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:53:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 10:54:00 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 10:54:02 GMT
CMD []
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7876f582583c6ce1dd934300234645dd5b97252662a8c87fdfbf82c860328d90`  
		Last Modified: Tue, 05 Apr 2022 10:55:44 GMT  
		Size: 45.4 MB (45385557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bba04077c5c30296939df9ed09482547b8947d5decf08a738273fa064ca121a`  
		Last Modified: Tue, 05 Apr 2022 10:55:36 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d23bba4fca1b0dd78c6f32996dd386b94a4944ac5ea047d049913f9f2c51e200
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113021b450dcbd4035fcfba58dd928217e0d39bff640b6d895c83e8eb2592df4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:12:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 06:13:11 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 06:13:13 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 06:13:13 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 06:13:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 06:13:13 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 06:13:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df61fc68478458a071e8edf49185d9b224067a6e66831cdde802e5d2b66b097`  
		Last Modified: Tue, 05 Apr 2022 06:14:33 GMT  
		Size: 44.1 MB (44067532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829d58f668fddd7b5ed61e0d6c27f5b3abd19844eeb8ad111b395b944d064904`  
		Last Modified: Tue, 05 Apr 2022 06:14:27 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.0.2`

```console
$ docker pull varnish@sha256:0bab3835b20068d32e145d205665570fe25e4b9b36d2d9ecc532264fcb706fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.0.2` - linux; amd64

```console
$ docker pull varnish@sha256:cd8bbaedc6acc855d4dbde0ecbf144ffcec08ace28141a028c267a6108d5b0f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101201770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7492119e1c0f61a7ae796bfccb2774a6385a197b85402151a6b769604b65154b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:19:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 15:21:57 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 15:21:58 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 15:21:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 20 Apr 2022 15:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 15:21:58 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 15:21:58 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d4c26eb233b1f26ae0b9467fa72834229ed3d194ae98dec875b7e27670be4`  
		Last Modified: Wed, 20 Apr 2022 15:25:16 GMT  
		Size: 69.8 MB (69822317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113ca7b5e4d8bea5c4f3cfdbde42d78cedc9cc7a3f232dae8075ac49a7c6ef60`  
		Last Modified: Wed, 20 Apr 2022 15:25:06 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e4f991ee0fffceb5b576bf52af2f4187fa1c3545a35d9a27eaba2fc0f3816e20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77821225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fac8014668438566fd29bc6e67db06f71eed12ebc7deedfd06a14e3b9fc451`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 02:18:34 GMT
ADD file:e1835d1a0c70a0335757f211893e5d12ddf797e489e10434c0982bdf9b234f67 in / 
# Tue, 29 Mar 2022 02:18:36 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 04:58:07 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 05:03:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 05:03:41 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 05:03:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 05:03:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 05:03:42 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 05:03:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f98812e1a494a683a5b3dea593dd2ef305f5f732193044c147f22e44b00164bc`  
		Last Modified: Tue, 29 Mar 2022 02:34:13 GMT  
		Size: 26.6 MB (26575370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f7b6d4c7611e504f11c8135d715741175aae45a8b5c8f9fd2a514cf69022e5`  
		Last Modified: Wed, 30 Mar 2022 05:09:52 GMT  
		Size: 51.2 MB (51245383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761275f2ac473d69f8c0c3ec1b4b46d5d9572a82bac140e031cb00ee8ffbffb3`  
		Last Modified: Wed, 30 Mar 2022 05:09:24 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ea65c75635fd3e13c03da16c68995ed4f38ae3b63ffd798fd210a7470fe0be2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95311405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b7b74bf809ee04653fc225dc513a72a1bc98e4600df9d6ab8745e3df50fd09`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:51:42 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:54:27 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:54:28 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:54:29 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:54:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:54:30 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:54:31 GMT
CMD []
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b31818a80ab96d113ecc26bae4c921e8b1f15bd573c0567be45beb836048700`  
		Last Modified: Wed, 30 Mar 2022 00:59:33 GMT  
		Size: 65.2 MB (65246620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa175bc0d41052fdda42c92374ca4cf78d073d37324d6526efe02454a651cd`  
		Last Modified: Wed, 30 Mar 2022 00:59:24 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2` - linux; 386

```console
$ docker pull varnish@sha256:259397fb199c0e9f739100dd0a93efb9a86e60827e66c65ed051b3e44ad83b93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102585485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01443ed33f01c5f1b4ed80c2b5351ad547ab887260ae9a4db797dc6623f747a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:23:01 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 17:25:18 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 17:25:19 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 17:25:20 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 20 Apr 2022 17:25:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 17:25:21 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 17:25:22 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47edc9eab3e86eb0355d68502318a630dc795c5d8d4d8779d7321b6b553cf98`  
		Last Modified: Wed, 20 Apr 2022 17:29:13 GMT  
		Size: 70.2 MB (70195418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aea8a62b1f5f50f6761a32239f5adc670e7af72f8b59664619186ddeae2fef`  
		Last Modified: Wed, 20 Apr 2022 17:29:04 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2` - linux; ppc64le

```console
$ docker pull varnish@sha256:9dfbab1f66da09461280e2006a8637a71cacc99345a3e005eb4cdd75f34e0057
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100376258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84ffd81229d9e36b2fe44a2d56797edb9d2f84a293a32b202b77177c2d0aa18`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 07:26:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 07:44:15 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 07:44:20 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 07:44:22 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 07:44:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 07:44:27 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 07:44:30 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddab9d225e329687fa4c9dbced15d44e0e90e64944867273cba0d7432395dfef`  
		Last Modified: Thu, 21 Apr 2022 08:06:05 GMT  
		Size: 65.1 MB (65090535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761715f8917a3a374aa705b10b377f1eb661cb0b7c33a6bc93d79f00ac0dede5`  
		Last Modified: Thu, 21 Apr 2022 08:05:52 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2` - linux; s390x

```console
$ docker pull varnish@sha256:7b2d1d1fc79b00edd1129e176ec751b1c9e3372c2dff553327f9e66c3f00c57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81637417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af65f783a437fab01c28d0c2ade060a88aa9cded965a28602d723c9c41d8a18`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:51:57 GMT
ADD file:39c5e0d7a686abd19448ab3e6237d50955ae2187fc2b64289a08c2549352b8f1 in / 
# Tue, 29 Mar 2022 00:51:58 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:54:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:56:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:56:42 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:56:42 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:56:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:56:42 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:56:42 GMT
CMD []
```

-	Layers:
	-	`sha256:ffb22bcde95509bb75f6dd2d69f3fdb5c7471727e4d720b31d92cd297582865c`  
		Last Modified: Tue, 29 Mar 2022 01:04:43 GMT  
		Size: 29.7 MB (29655426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aabcd8580e9559702629fa9ee5e4029a5b1318fe425c2ae5725d6e84a8c2e0d`  
		Last Modified: Wed, 30 Mar 2022 01:00:29 GMT  
		Size: 52.0 MB (51981518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac10509f97438a4a52957c04e3ce7ad59423d6b7f865b29a3d1462ec09ea52e`  
		Last Modified: Wed, 30 Mar 2022 01:00:25 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.0.2-alpine`

```console
$ docker pull varnish@sha256:a96966b666c3eb795b5a5ffe4b7f1911e009156774d5551a355de6ba17dd6ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.0.2-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:1f798a786c909e75214591ae7bb11711b606d19904771e17cac071e3fc945f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58347562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f303a05efad59d4625679d65998e25ac6af2a5a1e8e761d6165038faf0af7a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:46:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 09:47:16 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 09:47:16 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 09:47:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 09:47:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 09:47:16 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 09:47:16 GMT
CMD []
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd49c5f702ffa093526e350e19af19adacee36ebd21a4d2b8215729aebd24701`  
		Last Modified: Tue, 05 Apr 2022 09:48:23 GMT  
		Size: 55.5 MB (55528711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b11f3cacc52df447f6e49ab5dcad0b25a3e95d3aa5ca786c8a00b94bcea4d97`  
		Last Modified: Tue, 05 Apr 2022 09:48:15 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d0ef8137631136de68aa9ca8b5a1c202753588e4823091fc74c7381800475e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44158672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b498faee8096b05f4ad1e1a034d79076f1405006bbb01cdc1b62443d19faf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 19:12:30 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 19:13:58 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 19:13:59 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 19:13:59 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 19:14:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 19:14:00 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 19:14:00 GMT
CMD []
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a122a3f3e3f4f262ecd7c937fb5b761d7c7025f6b85195b6f6e59efccc3e22`  
		Last Modified: Tue, 05 Apr 2022 19:17:11 GMT  
		Size: 41.7 MB (41730222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e23c5ffb616fb8979712f573ce76a21ff2948ffe3c222f25abeda1b044fb82`  
		Last Modified: Tue, 05 Apr 2022 19:16:49 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:287bbe458761ddf7b90152156bcfcf1680e8229b94e87c6be21fcdcff4105325
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51100328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb806b4ff6eae8a70eec669d64a63205e9fa899f74021c50544a8a3fe8492216`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:24:20 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 07:25:05 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 07:25:05 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 07:25:07 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 07:25:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 07:25:08 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 07:25:09 GMT
CMD []
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c097d0722cedf772b294574bd3df3ea7bc3fd2a7f0d584bdda75906ab4a4f76`  
		Last Modified: Tue, 05 Apr 2022 07:26:39 GMT  
		Size: 48.4 MB (48382460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda2d05467662609f11c35127449028bdba318e2920842c0c49a157d72fd14d4`  
		Last Modified: Tue, 05 Apr 2022 07:26:32 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2-alpine` - linux; 386

```console
$ docker pull varnish@sha256:8d9a98e8ebe8c794faad1ca62b64b1d0f5d50b4bdc61593272165af938c90e58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58550969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b86a5912210274cdd2be334341ab5c8a5cc8b98b8cacbf00d0bc3b61391b34`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:38:32 GMT
ADD file:6508514d43b69774a3307679ef8f6dba0faf707e62ad6c6c1c8cf40d84e12d1d in / 
# Mon, 04 Apr 2022 23:38:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:44:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 06:45:29 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 06:45:29 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 06:45:31 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 06:45:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 06:45:32 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 06:45:33 GMT
CMD []
```

-	Layers:
	-	`sha256:c11e5e1035714514f6e237dffd1836a4d03b48af64e55a8e08f9bd9e998e24a9`  
		Last Modified: Mon, 04 Apr 2022 23:39:35 GMT  
		Size: 2.8 MB (2821213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781285b91779b0524f4a4b362a85bf7ad3c11049ec60271bc351d3ea22722f55`  
		Last Modified: Tue, 05 Apr 2022 06:47:18 GMT  
		Size: 55.7 MB (55729277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ede4c98a857e7e2e4374c87b05da88e9cfa36a1b9d2261f338a8e4cc091689`  
		Last Modified: Tue, 05 Apr 2022 06:47:09 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:99fc715aa51f45f415d42e16933cfd6640741633a9df875d1be9c41bb5eea1e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48200204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afb3e6b26fed2aaed2bdf33c3edb6718410d71cdda8521c1e6a42a745e020d3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:52:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 10:53:50 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 10:53:55 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 10:53:56 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:53:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 10:54:00 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 10:54:02 GMT
CMD []
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7876f582583c6ce1dd934300234645dd5b97252662a8c87fdfbf82c860328d90`  
		Last Modified: Tue, 05 Apr 2022 10:55:44 GMT  
		Size: 45.4 MB (45385557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bba04077c5c30296939df9ed09482547b8947d5decf08a738273fa064ca121a`  
		Last Modified: Tue, 05 Apr 2022 10:55:36 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.2-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d23bba4fca1b0dd78c6f32996dd386b94a4944ac5ea047d049913f9f2c51e200
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113021b450dcbd4035fcfba58dd928217e0d39bff640b6d895c83e8eb2592df4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:12:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 06:13:11 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 06:13:13 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 06:13:13 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 06:13:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 06:13:13 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 06:13:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df61fc68478458a071e8edf49185d9b224067a6e66831cdde802e5d2b66b097`  
		Last Modified: Tue, 05 Apr 2022 06:14:33 GMT  
		Size: 44.1 MB (44067532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829d58f668fddd7b5ed61e0d6c27f5b3abd19844eeb8ad111b395b944d064904`  
		Last Modified: Tue, 05 Apr 2022 06:14:27 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.1`

```console
$ docker pull varnish@sha256:79d1bc5fd03b413ebc1404bcd2e4e25ba6b9697d453ebce5c8fb3e3d24d2be24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.1` - linux; amd64

```console
$ docker pull varnish@sha256:f3df28cda6d06334a65691c1de4bcc66820033985f1520125f36547b78b910d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105363177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e101db8ad94e05a3ef6573f0d73ae802e3392a7eedf795d88212d8b66135e4e0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:16:56 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 15:16:56 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 15:16:57 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 22:07:21 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 22:07:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 22:07:21 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 22:07:21 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 22:07:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 22:10:14 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 22:10:15 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 22:10:15 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 22:10:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 22:10:15 GMT
USER varnish
# Thu, 21 Apr 2022 22:10:15 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 22:10:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1884046f45237facbf7ee696de977ca8850f655c89a819747005fda9c5df99c`  
		Last Modified: Thu, 21 Apr 2022 22:12:38 GMT  
		Size: 74.0 MB (73983724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a292aef91ba2b5542e31a24f5d934bae41a4e7e81d914802a46d4d3a8d6bc13`  
		Last Modified: Thu, 21 Apr 2022 22:12:27 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3314c10d40367f434ac9c737cd42b16d9afed9f0369868bad7257410fc62d1db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81966286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0a4145e7da62efa2bf256ec57af8719f5fd17701fd3aed235c9c49bc12e46`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 13:58:43 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Thu, 21 Apr 2022 13:58:43 GMT
ARG VARNISH_VERSION=7.1.0
# Thu, 21 Apr 2022 13:58:44 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Thu, 21 Apr 2022 13:58:44 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Thu, 21 Apr 2022 13:58:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Thu, 21 Apr 2022 13:58:46 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 14:05:20 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         mkdir /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     cp /work/varnish/pkg-varnish-cache/include/vmb.h src/vmb.h;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 14:05:21 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 14:05:22 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 14:05:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 14:05:22 GMT
USER varnish
# Thu, 21 Apr 2022 14:05:23 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 14:05:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9173eb8d6ef4a29e0abc0f63c62bf8d6027745249347bf4259506b563f4ecae`  
		Last Modified: Thu, 21 Apr 2022 14:14:21 GMT  
		Size: 55.4 MB (55390054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba783aa75b78da6b7d8a81161ba9065b52275d66c270f11001bb5d4d84c3dc5`  
		Last Modified: Thu, 21 Apr 2022 14:14:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfff2d4cc940fc0049ae0ecd1c432c4bf7f5f59ee730e47cb7517a5b7465cf42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99469391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126ab99be3dd8df097ebb773d2462bb12abbcabb8be13f323dc5ff406e815b77`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:31:46 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 17:31:47 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 17:31:48 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 17:31:49 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 17:31:50 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 17:31:51 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:40:37 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:40:38 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:40:39 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:40:40 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:40:41 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:43:32 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:43:32 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:43:34 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:43:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:43:35 GMT
USER varnish
# Thu, 21 Apr 2022 20:43:36 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:43:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a2c9a025e49931c65c1621550b8ed759c2227123492745c2775cdb0a71ca6e`  
		Last Modified: Thu, 21 Apr 2022 20:46:59 GMT  
		Size: 69.4 MB (69403116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2e3174ebcdbd61d6438f4a495a322a98ffc9ba5312a95d77ced44379856af7`  
		Last Modified: Thu, 21 Apr 2022 20:46:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1` - linux; 386

```console
$ docker pull varnish@sha256:9e8e2bb1e2952b4bcaa32bc67336631f119cad69ba0c374763406fe34aefc95d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106725441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326aabe87cfcf2b7d546e5321566c42f3ab790e1e02adc7a711e05c5d8cdef67`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:19:29 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 17:19:29 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 17:19:30 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 17:19:31 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 17:19:32 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 17:19:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:38:55 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:38:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:38:57 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:38:58 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:38:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:41:47 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:41:47 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:41:49 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:41:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:41:50 GMT
USER varnish
# Thu, 21 Apr 2022 20:41:51 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:41:52 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46457da13e908eadea0a447ad74a77755fd841bf1abb47bc87c6d08be11873d`  
		Last Modified: Thu, 21 Apr 2022 20:44:50 GMT  
		Size: 74.3 MB (74335370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12719a93484f02b9f6424fcf767a4dc7916b4dec85f85bdf2acea301f56e994`  
		Last Modified: Thu, 21 Apr 2022 20:44:38 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:2927bfd221e8b6b1f6d199eae496dad91625eb62b56c2efab624e309347f3622
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104548169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3250f6d61c3ac7e27c621223ec9ba41a6bbf3be64f0806fe496fc74aa28defb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 06:59:19 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Thu, 21 Apr 2022 06:59:26 GMT
ARG VARNISH_VERSION=7.1.0
# Thu, 21 Apr 2022 06:59:34 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Thu, 21 Apr 2022 06:59:38 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Thu, 21 Apr 2022 06:59:46 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Thu, 21 Apr 2022 06:59:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 07:00:00 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Thu, 21 Apr 2022 07:00:02 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Thu, 21 Apr 2022 07:00:05 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 07:26:12 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         mkdir /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     cp /work/varnish/pkg-varnish-cache/include/vmb.h src/vmb.h;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 07:26:18 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 07:26:20 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 07:26:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 07:26:27 GMT
USER varnish
# Thu, 21 Apr 2022 07:26:30 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 07:26:31 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdf0e98fdec95c180ab215269b20a4afa69c295e5bb21a2617def1309012c49`  
		Last Modified: Thu, 21 Apr 2022 08:05:30 GMT  
		Size: 69.3 MB (69262445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef1599fc9172d28d818447793a85f375d4269c360738e534ebee2e53b689a25`  
		Last Modified: Thu, 21 Apr 2022 08:05:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1` - linux; s390x

```console
$ docker pull varnish@sha256:7e436b56075162028c9d1e15247d726f68bb0e723f8ecb5c82f132ef6724db35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85794352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43458476d36aa1b00f68f5a50ab03b613632b2fe0a25d680edc5e0ca47fddc2e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 19:51:37 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 19:51:38 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 19:51:38 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 19:51:39 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 19:51:39 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 19:51:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:41:47 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:41:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:41:48 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:41:48 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:41:48 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:44:32 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:44:34 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:44:34 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:44:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:44:34 GMT
USER varnish
# Thu, 21 Apr 2022 20:44:34 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:44:34 GMT
CMD []
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca2ed3d3c3db1d075048708d86e798d4f5533de95cb6150540d27f0221c76e2`  
		Last Modified: Thu, 21 Apr 2022 20:48:11 GMT  
		Size: 56.1 MB (56139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca96a2437ba4a34a30b1ce0d386fd7089f61e2b8f3cca90d9de74b30f45eeaa8`  
		Last Modified: Thu, 21 Apr 2022 20:48:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.1-alpine`

```console
$ docker pull varnish@sha256:839469849dfce592f136455079a46884d604b3f752722cee5f4aa164f0f196b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:81397424691b539bc850f20254af04c34cae93a5ec485c3d8339eb9b138dd2f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59100484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c410d76e4ae50504580f78c53148ba1e62fb8d27e1e4a1a2f98d3cde5a289e0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:44:24 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 09:44:24 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 22:10:26 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 22:10:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 22:10:26 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 22:10:26 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 22:10:26 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 22:11:41 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 22:11:41 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 22:11:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 22:11:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 22:11:41 GMT
USER varnish
# Thu, 21 Apr 2022 22:11:41 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 22:11:42 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab0de482a12061e292d208c300acfef4b7903ad36dc4fb177fc61b76f6d7e1a`  
		Last Modified: Thu, 21 Apr 2022 22:13:00 GMT  
		Size: 56.3 MB (56285443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fdb9a66b68029729002c46951f2c45aa31e27860321211a5aac411173bdc8f`  
		Last Modified: Thu, 21 Apr 2022 22:12:52 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:46dc04b33e0e7620276014ac79e7637727e63f4657c2609560d532fac60bef95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86036025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cacdbb671bfca990403a2e7feb33a61590cd0215111d4c110a2bb5a37e627ac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 19:09:14 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 19:09:15 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 19:09:15 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 19:09:15 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 19:09:16 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 19:09:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 05 Apr 2022 19:09:17 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 05 Apr 2022 19:09:17 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 05 Apr 2022 19:09:17 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 19:11:57 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;          mkdir -p /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     git clone https://github.com/varnishcache/varnish-cache.git;     cd varnish-cache;     git checkout d48636d23bb277ca8650a6174c872d74080f2859;     cp include/vmb.h ../src/vmb.h;     cd /work/vmod-dynamic;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 05 Apr 2022 19:11:58 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 19:11:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 19:11:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 19:11:59 GMT
USER varnish
# Tue, 05 Apr 2022 19:11:59 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 19:12:00 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4835da8a6a06c20b8df6cc2ddfd41f978b72fcea5b70942bebf8915714a18027`  
		Last Modified: Tue, 05 Apr 2022 19:16:25 GMT  
		Size: 83.6 MB (83611223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4cfdd1613e1129be77c6b90fd9e844cd4d15824bd4bf4f4112d73192ef9ea1`  
		Last Modified: Tue, 05 Apr 2022 19:15:48 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4baf57565dc415a17a031897b6ba12546044b510b9260fe92806a0ce17d22b57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51830728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca13aff345b38cd131a7f99e198b99d739d007f09d7977dabc789bdbc1f4480`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:22:16 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 07:22:17 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 07:22:18 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 07:22:19 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 07:22:20 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 07:22:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:43:49 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:43:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:43:51 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:43:52 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:43:53 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:45:14 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:45:14 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:45:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:45:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:45:17 GMT
USER varnish
# Thu, 21 Apr 2022 20:45:18 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:45:19 GMT
CMD []
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53648c9db1a4f4013c5d44e9fd4577e839980908f0dca7a76d3c8efad06d048`  
		Last Modified: Thu, 21 Apr 2022 20:47:24 GMT  
		Size: 49.1 MB (49113769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0a30b3f6f66f585ac84b9bf017f0e7975a34fd479b9701a245f950742ad5b`  
		Last Modified: Thu, 21 Apr 2022 20:47:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:de6628a1837145901ad6a52437bd103285f7830c8aa27203eea30f716f01dbe1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59292895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09ff39c7c861e7ca0f001f5e542ba94c66a520216bf35e15659ec0c23ba09b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:42:43 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 06:42:44 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 06:42:45 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 06:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 06:42:47 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 06:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:42:08 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:42:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:42:09 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:42:10 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:42:11 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:43:30 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:43:30 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:43:32 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:43:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:43:33 GMT
USER varnish
# Thu, 21 Apr 2022 20:43:34 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:43:35 GMT
CMD []
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34115bd677f7c2afb67705f651ff60b689e7a3a69b0cd15a60e3d836a0162e18`  
		Last Modified: Thu, 21 Apr 2022 20:45:21 GMT  
		Size: 56.5 MB (56473443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35e121fe38cf19136053915fbb7f2d88e8c3702004736c435aa530245164896`  
		Last Modified: Thu, 21 Apr 2022 20:45:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:e2b15844d7ef24c197ba5e2a1ef35d09957b9984bbdb80ab8072e9bd79f9153c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90095561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e485b139a84e89e60caf2503c044977eabffc55fd5d15a9c8f8cdfe9652f9899`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:48:31 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 10:48:33 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 10:48:35 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 10:48:37 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 10:48:40 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 10:48:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 05 Apr 2022 10:48:47 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 05 Apr 2022 10:48:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 05 Apr 2022 10:48:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 10:52:07 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;          mkdir -p /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     git clone https://github.com/varnishcache/varnish-cache.git;     cd varnish-cache;     git checkout d48636d23bb277ca8650a6174c872d74080f2859;     cp include/vmb.h ../src/vmb.h;     cd /work/vmod-dynamic;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 05 Apr 2022 10:52:15 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 10:52:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:52:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 10:52:19 GMT
USER varnish
# Tue, 05 Apr 2022 10:52:21 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 10:52:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e676e84e66a93a6a4f0cbe85ae6eaa99b571c1e0cd879f5e13314093e421de`  
		Last Modified: Tue, 05 Apr 2022 10:55:15 GMT  
		Size: 87.3 MB (87283898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d526fce93958e73887bd935d40fbbac9413c3826d8a8dc38711b2aa7501ef`  
		Last Modified: Tue, 05 Apr 2022 10:55:02 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:10414a54f8108d64836a2c9c6c865e5f9ebe6123647c3ee57867ced916313f4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47350962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac56919f84b42f704fd7cfaaffe0a712aff857fbe24d7a894d9d4156d8c8b6a6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:10:53 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 06:10:53 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:44:53 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:44:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:44:54 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:44:54 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:44:54 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:46:21 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:46:22 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:46:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:46:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:46:23 GMT
USER varnish
# Thu, 21 Apr 2022 20:46:23 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:46:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a48f1c01887a27a97e883fdd3fad9fb57c191e26cc389b076ad6ce3abe007`  
		Last Modified: Thu, 21 Apr 2022 20:48:28 GMT  
		Size: 44.8 MB (44750107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c99d1795f78de1f9b33331b3ee9178f8fa9622b60f90d85b5292655323e272`  
		Last Modified: Thu, 21 Apr 2022 20:48:23 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.1.0`

```console
$ docker pull varnish@sha256:79d1bc5fd03b413ebc1404bcd2e4e25ba6b9697d453ebce5c8fb3e3d24d2be24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.1.0` - linux; amd64

```console
$ docker pull varnish@sha256:f3df28cda6d06334a65691c1de4bcc66820033985f1520125f36547b78b910d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105363177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e101db8ad94e05a3ef6573f0d73ae802e3392a7eedf795d88212d8b66135e4e0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:16:56 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 15:16:56 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 15:16:57 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 22:07:21 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 22:07:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 22:07:21 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 22:07:21 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 22:07:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 22:10:14 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 22:10:15 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 22:10:15 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 22:10:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 22:10:15 GMT
USER varnish
# Thu, 21 Apr 2022 22:10:15 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 22:10:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1884046f45237facbf7ee696de977ca8850f655c89a819747005fda9c5df99c`  
		Last Modified: Thu, 21 Apr 2022 22:12:38 GMT  
		Size: 74.0 MB (73983724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a292aef91ba2b5542e31a24f5d934bae41a4e7e81d914802a46d4d3a8d6bc13`  
		Last Modified: Thu, 21 Apr 2022 22:12:27 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3314c10d40367f434ac9c737cd42b16d9afed9f0369868bad7257410fc62d1db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81966286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0a4145e7da62efa2bf256ec57af8719f5fd17701fd3aed235c9c49bc12e46`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 13:58:43 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Thu, 21 Apr 2022 13:58:43 GMT
ARG VARNISH_VERSION=7.1.0
# Thu, 21 Apr 2022 13:58:44 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Thu, 21 Apr 2022 13:58:44 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Thu, 21 Apr 2022 13:58:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Thu, 21 Apr 2022 13:58:46 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 14:05:20 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         mkdir /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     cp /work/varnish/pkg-varnish-cache/include/vmb.h src/vmb.h;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 14:05:21 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 14:05:22 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 14:05:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 14:05:22 GMT
USER varnish
# Thu, 21 Apr 2022 14:05:23 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 14:05:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9173eb8d6ef4a29e0abc0f63c62bf8d6027745249347bf4259506b563f4ecae`  
		Last Modified: Thu, 21 Apr 2022 14:14:21 GMT  
		Size: 55.4 MB (55390054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba783aa75b78da6b7d8a81161ba9065b52275d66c270f11001bb5d4d84c3dc5`  
		Last Modified: Thu, 21 Apr 2022 14:14:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfff2d4cc940fc0049ae0ecd1c432c4bf7f5f59ee730e47cb7517a5b7465cf42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99469391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126ab99be3dd8df097ebb773d2462bb12abbcabb8be13f323dc5ff406e815b77`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:31:46 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 17:31:47 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 17:31:48 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 17:31:49 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 17:31:50 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 17:31:51 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:40:37 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:40:38 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:40:39 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:40:40 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:40:41 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:43:32 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:43:32 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:43:34 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:43:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:43:35 GMT
USER varnish
# Thu, 21 Apr 2022 20:43:36 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:43:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a2c9a025e49931c65c1621550b8ed759c2227123492745c2775cdb0a71ca6e`  
		Last Modified: Thu, 21 Apr 2022 20:46:59 GMT  
		Size: 69.4 MB (69403116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2e3174ebcdbd61d6438f4a495a322a98ffc9ba5312a95d77ced44379856af7`  
		Last Modified: Thu, 21 Apr 2022 20:46:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0` - linux; 386

```console
$ docker pull varnish@sha256:9e8e2bb1e2952b4bcaa32bc67336631f119cad69ba0c374763406fe34aefc95d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106725441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326aabe87cfcf2b7d546e5321566c42f3ab790e1e02adc7a711e05c5d8cdef67`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:19:29 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 17:19:29 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 17:19:30 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 17:19:31 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 17:19:32 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 17:19:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:38:55 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:38:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:38:57 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:38:58 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:38:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:41:47 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:41:47 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:41:49 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:41:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:41:50 GMT
USER varnish
# Thu, 21 Apr 2022 20:41:51 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:41:52 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46457da13e908eadea0a447ad74a77755fd841bf1abb47bc87c6d08be11873d`  
		Last Modified: Thu, 21 Apr 2022 20:44:50 GMT  
		Size: 74.3 MB (74335370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12719a93484f02b9f6424fcf767a4dc7916b4dec85f85bdf2acea301f56e994`  
		Last Modified: Thu, 21 Apr 2022 20:44:38 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:2927bfd221e8b6b1f6d199eae496dad91625eb62b56c2efab624e309347f3622
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104548169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3250f6d61c3ac7e27c621223ec9ba41a6bbf3be64f0806fe496fc74aa28defb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 06:59:19 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Thu, 21 Apr 2022 06:59:26 GMT
ARG VARNISH_VERSION=7.1.0
# Thu, 21 Apr 2022 06:59:34 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Thu, 21 Apr 2022 06:59:38 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Thu, 21 Apr 2022 06:59:46 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Thu, 21 Apr 2022 06:59:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 07:00:00 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Thu, 21 Apr 2022 07:00:02 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Thu, 21 Apr 2022 07:00:05 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 07:26:12 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         mkdir /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     cp /work/varnish/pkg-varnish-cache/include/vmb.h src/vmb.h;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 07:26:18 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 07:26:20 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 07:26:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 07:26:27 GMT
USER varnish
# Thu, 21 Apr 2022 07:26:30 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 07:26:31 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdf0e98fdec95c180ab215269b20a4afa69c295e5bb21a2617def1309012c49`  
		Last Modified: Thu, 21 Apr 2022 08:05:30 GMT  
		Size: 69.3 MB (69262445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef1599fc9172d28d818447793a85f375d4269c360738e534ebee2e53b689a25`  
		Last Modified: Thu, 21 Apr 2022 08:05:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0` - linux; s390x

```console
$ docker pull varnish@sha256:7e436b56075162028c9d1e15247d726f68bb0e723f8ecb5c82f132ef6724db35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85794352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43458476d36aa1b00f68f5a50ab03b613632b2fe0a25d680edc5e0ca47fddc2e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 19:51:37 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 19:51:38 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 19:51:38 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 19:51:39 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 19:51:39 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 19:51:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:41:47 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:41:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:41:48 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:41:48 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:41:48 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:44:32 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:44:34 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:44:34 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:44:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:44:34 GMT
USER varnish
# Thu, 21 Apr 2022 20:44:34 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:44:34 GMT
CMD []
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca2ed3d3c3db1d075048708d86e798d4f5533de95cb6150540d27f0221c76e2`  
		Last Modified: Thu, 21 Apr 2022 20:48:11 GMT  
		Size: 56.1 MB (56139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca96a2437ba4a34a30b1ce0d386fd7089f61e2b8f3cca90d9de74b30f45eeaa8`  
		Last Modified: Thu, 21 Apr 2022 20:48:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.1.0-alpine`

```console
$ docker pull varnish@sha256:839469849dfce592f136455079a46884d604b3f752722cee5f4aa164f0f196b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.1.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:81397424691b539bc850f20254af04c34cae93a5ec485c3d8339eb9b138dd2f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59100484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c410d76e4ae50504580f78c53148ba1e62fb8d27e1e4a1a2f98d3cde5a289e0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:44:24 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 09:44:24 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 22:10:26 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 22:10:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 22:10:26 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 22:10:26 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 22:10:26 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 22:11:41 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 22:11:41 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 22:11:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 22:11:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 22:11:41 GMT
USER varnish
# Thu, 21 Apr 2022 22:11:41 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 22:11:42 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab0de482a12061e292d208c300acfef4b7903ad36dc4fb177fc61b76f6d7e1a`  
		Last Modified: Thu, 21 Apr 2022 22:13:00 GMT  
		Size: 56.3 MB (56285443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fdb9a66b68029729002c46951f2c45aa31e27860321211a5aac411173bdc8f`  
		Last Modified: Thu, 21 Apr 2022 22:12:52 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:46dc04b33e0e7620276014ac79e7637727e63f4657c2609560d532fac60bef95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86036025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cacdbb671bfca990403a2e7feb33a61590cd0215111d4c110a2bb5a37e627ac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 19:09:14 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 19:09:15 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 19:09:15 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 19:09:15 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 19:09:16 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 19:09:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 05 Apr 2022 19:09:17 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 05 Apr 2022 19:09:17 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 05 Apr 2022 19:09:17 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 19:11:57 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;          mkdir -p /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     git clone https://github.com/varnishcache/varnish-cache.git;     cd varnish-cache;     git checkout d48636d23bb277ca8650a6174c872d74080f2859;     cp include/vmb.h ../src/vmb.h;     cd /work/vmod-dynamic;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 05 Apr 2022 19:11:58 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 19:11:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 19:11:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 19:11:59 GMT
USER varnish
# Tue, 05 Apr 2022 19:11:59 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 19:12:00 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4835da8a6a06c20b8df6cc2ddfd41f978b72fcea5b70942bebf8915714a18027`  
		Last Modified: Tue, 05 Apr 2022 19:16:25 GMT  
		Size: 83.6 MB (83611223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4cfdd1613e1129be77c6b90fd9e844cd4d15824bd4bf4f4112d73192ef9ea1`  
		Last Modified: Tue, 05 Apr 2022 19:15:48 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4baf57565dc415a17a031897b6ba12546044b510b9260fe92806a0ce17d22b57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51830728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca13aff345b38cd131a7f99e198b99d739d007f09d7977dabc789bdbc1f4480`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:22:16 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 07:22:17 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 07:22:18 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 07:22:19 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 07:22:20 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 07:22:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:43:49 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:43:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:43:51 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:43:52 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:43:53 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:45:14 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:45:14 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:45:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:45:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:45:17 GMT
USER varnish
# Thu, 21 Apr 2022 20:45:18 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:45:19 GMT
CMD []
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53648c9db1a4f4013c5d44e9fd4577e839980908f0dca7a76d3c8efad06d048`  
		Last Modified: Thu, 21 Apr 2022 20:47:24 GMT  
		Size: 49.1 MB (49113769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0a30b3f6f66f585ac84b9bf017f0e7975a34fd479b9701a245f950742ad5b`  
		Last Modified: Thu, 21 Apr 2022 20:47:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:de6628a1837145901ad6a52437bd103285f7830c8aa27203eea30f716f01dbe1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59292895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09ff39c7c861e7ca0f001f5e542ba94c66a520216bf35e15659ec0c23ba09b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:42:43 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 06:42:44 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 06:42:45 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 06:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 06:42:47 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 06:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:42:08 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:42:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:42:09 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:42:10 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:42:11 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:43:30 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:43:30 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:43:32 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:43:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:43:33 GMT
USER varnish
# Thu, 21 Apr 2022 20:43:34 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:43:35 GMT
CMD []
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34115bd677f7c2afb67705f651ff60b689e7a3a69b0cd15a60e3d836a0162e18`  
		Last Modified: Thu, 21 Apr 2022 20:45:21 GMT  
		Size: 56.5 MB (56473443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35e121fe38cf19136053915fbb7f2d88e8c3702004736c435aa530245164896`  
		Last Modified: Thu, 21 Apr 2022 20:45:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:e2b15844d7ef24c197ba5e2a1ef35d09957b9984bbdb80ab8072e9bd79f9153c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90095561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e485b139a84e89e60caf2503c044977eabffc55fd5d15a9c8f8cdfe9652f9899`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:48:31 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 10:48:33 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 10:48:35 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 10:48:37 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 10:48:40 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 10:48:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 05 Apr 2022 10:48:47 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 05 Apr 2022 10:48:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 05 Apr 2022 10:48:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 10:52:07 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;          mkdir -p /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     git clone https://github.com/varnishcache/varnish-cache.git;     cd varnish-cache;     git checkout d48636d23bb277ca8650a6174c872d74080f2859;     cp include/vmb.h ../src/vmb.h;     cd /work/vmod-dynamic;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 05 Apr 2022 10:52:15 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 10:52:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:52:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 10:52:19 GMT
USER varnish
# Tue, 05 Apr 2022 10:52:21 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 10:52:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e676e84e66a93a6a4f0cbe85ae6eaa99b571c1e0cd879f5e13314093e421de`  
		Last Modified: Tue, 05 Apr 2022 10:55:15 GMT  
		Size: 87.3 MB (87283898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d526fce93958e73887bd935d40fbbac9413c3826d8a8dc38711b2aa7501ef`  
		Last Modified: Tue, 05 Apr 2022 10:55:02 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.1.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:10414a54f8108d64836a2c9c6c865e5f9ebe6123647c3ee57867ced916313f4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47350962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac56919f84b42f704fd7cfaaffe0a712aff857fbe24d7a894d9d4156d8c8b6a6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:10:53 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 06:10:53 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:44:53 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:44:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:44:54 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:44:54 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:44:54 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:46:21 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:46:22 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:46:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:46:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:46:23 GMT
USER varnish
# Thu, 21 Apr 2022 20:46:23 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:46:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a48f1c01887a27a97e883fdd3fad9fb57c191e26cc389b076ad6ce3abe007`  
		Last Modified: Thu, 21 Apr 2022 20:48:28 GMT  
		Size: 44.8 MB (44750107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c99d1795f78de1f9b33331b3ee9178f8fa9622b60f90d85b5292655323e272`  
		Last Modified: Thu, 21 Apr 2022 20:48:23 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:alpine`

```console
$ docker pull varnish@sha256:839469849dfce592f136455079a46884d604b3f752722cee5f4aa164f0f196b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:81397424691b539bc850f20254af04c34cae93a5ec485c3d8339eb9b138dd2f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59100484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c410d76e4ae50504580f78c53148ba1e62fb8d27e1e4a1a2f98d3cde5a289e0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:44:24 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 09:44:24 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 22:10:26 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 22:10:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 22:10:26 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 22:10:26 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 22:10:26 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 22:11:41 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 22:11:41 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 22:11:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 22:11:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 22:11:41 GMT
USER varnish
# Thu, 21 Apr 2022 22:11:41 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 22:11:42 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab0de482a12061e292d208c300acfef4b7903ad36dc4fb177fc61b76f6d7e1a`  
		Last Modified: Thu, 21 Apr 2022 22:13:00 GMT  
		Size: 56.3 MB (56285443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fdb9a66b68029729002c46951f2c45aa31e27860321211a5aac411173bdc8f`  
		Last Modified: Thu, 21 Apr 2022 22:12:52 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:46dc04b33e0e7620276014ac79e7637727e63f4657c2609560d532fac60bef95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86036025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cacdbb671bfca990403a2e7feb33a61590cd0215111d4c110a2bb5a37e627ac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 19:09:14 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 19:09:15 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 19:09:15 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 19:09:15 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 19:09:16 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 19:09:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 05 Apr 2022 19:09:17 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 05 Apr 2022 19:09:17 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 05 Apr 2022 19:09:17 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 19:11:57 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;          mkdir -p /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     git clone https://github.com/varnishcache/varnish-cache.git;     cd varnish-cache;     git checkout d48636d23bb277ca8650a6174c872d74080f2859;     cp include/vmb.h ../src/vmb.h;     cd /work/vmod-dynamic;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 05 Apr 2022 19:11:58 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 19:11:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 19:11:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 19:11:59 GMT
USER varnish
# Tue, 05 Apr 2022 19:11:59 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 19:12:00 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4835da8a6a06c20b8df6cc2ddfd41f978b72fcea5b70942bebf8915714a18027`  
		Last Modified: Tue, 05 Apr 2022 19:16:25 GMT  
		Size: 83.6 MB (83611223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4cfdd1613e1129be77c6b90fd9e844cd4d15824bd4bf4f4112d73192ef9ea1`  
		Last Modified: Tue, 05 Apr 2022 19:15:48 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4baf57565dc415a17a031897b6ba12546044b510b9260fe92806a0ce17d22b57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51830728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca13aff345b38cd131a7f99e198b99d739d007f09d7977dabc789bdbc1f4480`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:22:16 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 07:22:17 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 07:22:18 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 07:22:19 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 07:22:20 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 07:22:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:43:49 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:43:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:43:51 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:43:52 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:43:53 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:45:14 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:45:14 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:45:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:45:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:45:17 GMT
USER varnish
# Thu, 21 Apr 2022 20:45:18 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:45:19 GMT
CMD []
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53648c9db1a4f4013c5d44e9fd4577e839980908f0dca7a76d3c8efad06d048`  
		Last Modified: Thu, 21 Apr 2022 20:47:24 GMT  
		Size: 49.1 MB (49113769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0a30b3f6f66f585ac84b9bf017f0e7975a34fd479b9701a245f950742ad5b`  
		Last Modified: Thu, 21 Apr 2022 20:47:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:de6628a1837145901ad6a52437bd103285f7830c8aa27203eea30f716f01dbe1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59292895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09ff39c7c861e7ca0f001f5e542ba94c66a520216bf35e15659ec0c23ba09b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:42:43 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 06:42:44 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 06:42:45 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 06:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 06:42:47 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 06:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:42:08 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:42:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:42:09 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:42:10 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:42:11 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:43:30 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:43:30 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:43:32 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:43:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:43:33 GMT
USER varnish
# Thu, 21 Apr 2022 20:43:34 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:43:35 GMT
CMD []
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34115bd677f7c2afb67705f651ff60b689e7a3a69b0cd15a60e3d836a0162e18`  
		Last Modified: Thu, 21 Apr 2022 20:45:21 GMT  
		Size: 56.5 MB (56473443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35e121fe38cf19136053915fbb7f2d88e8c3702004736c435aa530245164896`  
		Last Modified: Thu, 21 Apr 2022 20:45:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:e2b15844d7ef24c197ba5e2a1ef35d09957b9984bbdb80ab8072e9bd79f9153c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90095561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e485b139a84e89e60caf2503c044977eabffc55fd5d15a9c8f8cdfe9652f9899`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:48:31 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 10:48:33 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 10:48:35 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 10:48:37 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 10:48:40 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 10:48:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 05 Apr 2022 10:48:47 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 05 Apr 2022 10:48:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 05 Apr 2022 10:48:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 10:52:07 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;          mkdir -p /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     git clone https://github.com/varnishcache/varnish-cache.git;     cd varnish-cache;     git checkout d48636d23bb277ca8650a6174c872d74080f2859;     cp include/vmb.h ../src/vmb.h;     cd /work/vmod-dynamic;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 05 Apr 2022 10:52:15 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 10:52:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:52:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 10:52:19 GMT
USER varnish
# Tue, 05 Apr 2022 10:52:21 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 10:52:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e676e84e66a93a6a4f0cbe85ae6eaa99b571c1e0cd879f5e13314093e421de`  
		Last Modified: Tue, 05 Apr 2022 10:55:15 GMT  
		Size: 87.3 MB (87283898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d526fce93958e73887bd935d40fbbac9413c3826d8a8dc38711b2aa7501ef`  
		Last Modified: Tue, 05 Apr 2022 10:55:02 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:10414a54f8108d64836a2c9c6c865e5f9ebe6123647c3ee57867ced916313f4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47350962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac56919f84b42f704fd7cfaaffe0a712aff857fbe24d7a894d9d4156d8c8b6a6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:10:53 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 06:10:53 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:44:53 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:44:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:44:54 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:44:54 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:44:54 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:46:21 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:46:22 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:46:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:46:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:46:23 GMT
USER varnish
# Thu, 21 Apr 2022 20:46:23 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:46:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a48f1c01887a27a97e883fdd3fad9fb57c191e26cc389b076ad6ce3abe007`  
		Last Modified: Thu, 21 Apr 2022 20:48:28 GMT  
		Size: 44.8 MB (44750107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c99d1795f78de1f9b33331b3ee9178f8fa9622b60f90d85b5292655323e272`  
		Last Modified: Thu, 21 Apr 2022 20:48:23 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:79d1bc5fd03b413ebc1404bcd2e4e25ba6b9697d453ebce5c8fb3e3d24d2be24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:f3df28cda6d06334a65691c1de4bcc66820033985f1520125f36547b78b910d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105363177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e101db8ad94e05a3ef6573f0d73ae802e3392a7eedf795d88212d8b66135e4e0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:16:56 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 15:16:56 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 15:16:57 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 22:07:21 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 22:07:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 22:07:21 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 22:07:21 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 22:07:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 22:10:14 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 22:10:15 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 22:10:15 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 22:10:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 22:10:15 GMT
USER varnish
# Thu, 21 Apr 2022 22:10:15 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 22:10:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1884046f45237facbf7ee696de977ca8850f655c89a819747005fda9c5df99c`  
		Last Modified: Thu, 21 Apr 2022 22:12:38 GMT  
		Size: 74.0 MB (73983724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a292aef91ba2b5542e31a24f5d934bae41a4e7e81d914802a46d4d3a8d6bc13`  
		Last Modified: Thu, 21 Apr 2022 22:12:27 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3314c10d40367f434ac9c737cd42b16d9afed9f0369868bad7257410fc62d1db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81966286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0a4145e7da62efa2bf256ec57af8719f5fd17701fd3aed235c9c49bc12e46`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 13:58:43 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Thu, 21 Apr 2022 13:58:43 GMT
ARG VARNISH_VERSION=7.1.0
# Thu, 21 Apr 2022 13:58:44 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Thu, 21 Apr 2022 13:58:44 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Thu, 21 Apr 2022 13:58:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Thu, 21 Apr 2022 13:58:46 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 14:05:20 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         mkdir /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     cp /work/varnish/pkg-varnish-cache/include/vmb.h src/vmb.h;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 14:05:21 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 14:05:22 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 14:05:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 14:05:22 GMT
USER varnish
# Thu, 21 Apr 2022 14:05:23 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 14:05:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9173eb8d6ef4a29e0abc0f63c62bf8d6027745249347bf4259506b563f4ecae`  
		Last Modified: Thu, 21 Apr 2022 14:14:21 GMT  
		Size: 55.4 MB (55390054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba783aa75b78da6b7d8a81161ba9065b52275d66c270f11001bb5d4d84c3dc5`  
		Last Modified: Thu, 21 Apr 2022 14:14:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfff2d4cc940fc0049ae0ecd1c432c4bf7f5f59ee730e47cb7517a5b7465cf42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99469391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126ab99be3dd8df097ebb773d2462bb12abbcabb8be13f323dc5ff406e815b77`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:31:46 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 17:31:47 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 17:31:48 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 17:31:49 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 17:31:50 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 17:31:51 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:40:37 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:40:38 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:40:39 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:40:40 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:40:41 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:43:32 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:43:32 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:43:34 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:43:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:43:35 GMT
USER varnish
# Thu, 21 Apr 2022 20:43:36 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:43:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a2c9a025e49931c65c1621550b8ed759c2227123492745c2775cdb0a71ca6e`  
		Last Modified: Thu, 21 Apr 2022 20:46:59 GMT  
		Size: 69.4 MB (69403116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2e3174ebcdbd61d6438f4a495a322a98ffc9ba5312a95d77ced44379856af7`  
		Last Modified: Thu, 21 Apr 2022 20:46:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:9e8e2bb1e2952b4bcaa32bc67336631f119cad69ba0c374763406fe34aefc95d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106725441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326aabe87cfcf2b7d546e5321566c42f3ab790e1e02adc7a711e05c5d8cdef67`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:19:29 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 17:19:29 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 17:19:30 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 17:19:31 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 17:19:32 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 17:19:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:38:55 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:38:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:38:57 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:38:58 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:38:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:41:47 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:41:47 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:41:49 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:41:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:41:50 GMT
USER varnish
# Thu, 21 Apr 2022 20:41:51 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:41:52 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46457da13e908eadea0a447ad74a77755fd841bf1abb47bc87c6d08be11873d`  
		Last Modified: Thu, 21 Apr 2022 20:44:50 GMT  
		Size: 74.3 MB (74335370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12719a93484f02b9f6424fcf767a4dc7916b4dec85f85bdf2acea301f56e994`  
		Last Modified: Thu, 21 Apr 2022 20:44:38 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:2927bfd221e8b6b1f6d199eae496dad91625eb62b56c2efab624e309347f3622
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104548169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3250f6d61c3ac7e27c621223ec9ba41a6bbf3be64f0806fe496fc74aa28defb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 06:59:19 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Thu, 21 Apr 2022 06:59:26 GMT
ARG VARNISH_VERSION=7.1.0
# Thu, 21 Apr 2022 06:59:34 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Thu, 21 Apr 2022 06:59:38 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Thu, 21 Apr 2022 06:59:46 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Thu, 21 Apr 2022 06:59:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 07:00:00 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Thu, 21 Apr 2022 07:00:02 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Thu, 21 Apr 2022 07:00:05 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 07:26:12 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         mkdir /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     cp /work/varnish/pkg-varnish-cache/include/vmb.h src/vmb.h;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 07:26:18 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 07:26:20 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 07:26:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 07:26:27 GMT
USER varnish
# Thu, 21 Apr 2022 07:26:30 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 07:26:31 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdf0e98fdec95c180ab215269b20a4afa69c295e5bb21a2617def1309012c49`  
		Last Modified: Thu, 21 Apr 2022 08:05:30 GMT  
		Size: 69.3 MB (69262445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef1599fc9172d28d818447793a85f375d4269c360738e534ebee2e53b689a25`  
		Last Modified: Thu, 21 Apr 2022 08:05:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:7e436b56075162028c9d1e15247d726f68bb0e723f8ecb5c82f132ef6724db35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85794352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43458476d36aa1b00f68f5a50ab03b613632b2fe0a25d680edc5e0ca47fddc2e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 19:51:37 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 19:51:38 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 19:51:38 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 19:51:39 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 19:51:39 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 19:51:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:41:47 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:41:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:41:48 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:41:48 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:41:48 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:44:32 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:44:34 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:44:34 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:44:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:44:34 GMT
USER varnish
# Thu, 21 Apr 2022 20:44:34 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:44:34 GMT
CMD []
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca2ed3d3c3db1d075048708d86e798d4f5533de95cb6150540d27f0221c76e2`  
		Last Modified: Thu, 21 Apr 2022 20:48:11 GMT  
		Size: 56.1 MB (56139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca96a2437ba4a34a30b1ce0d386fd7089f61e2b8f3cca90d9de74b30f45eeaa8`  
		Last Modified: Thu, 21 Apr 2022 20:48:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:839469849dfce592f136455079a46884d604b3f752722cee5f4aa164f0f196b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:81397424691b539bc850f20254af04c34cae93a5ec485c3d8339eb9b138dd2f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59100484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c410d76e4ae50504580f78c53148ba1e62fb8d27e1e4a1a2f98d3cde5a289e0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:44:24 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 09:44:24 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 09:44:24 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 22:10:26 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 22:10:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 22:10:26 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 22:10:26 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 22:10:26 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 22:11:41 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 22:11:41 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 22:11:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 22:11:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 22:11:41 GMT
USER varnish
# Thu, 21 Apr 2022 22:11:41 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 22:11:42 GMT
CMD []
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab0de482a12061e292d208c300acfef4b7903ad36dc4fb177fc61b76f6d7e1a`  
		Last Modified: Thu, 21 Apr 2022 22:13:00 GMT  
		Size: 56.3 MB (56285443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fdb9a66b68029729002c46951f2c45aa31e27860321211a5aac411173bdc8f`  
		Last Modified: Thu, 21 Apr 2022 22:12:52 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:46dc04b33e0e7620276014ac79e7637727e63f4657c2609560d532fac60bef95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86036025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cacdbb671bfca990403a2e7feb33a61590cd0215111d4c110a2bb5a37e627ac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 19:09:14 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 19:09:15 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 19:09:15 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 19:09:15 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 19:09:16 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 19:09:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 05 Apr 2022 19:09:17 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 05 Apr 2022 19:09:17 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 05 Apr 2022 19:09:17 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 19:11:57 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;          mkdir -p /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     git clone https://github.com/varnishcache/varnish-cache.git;     cd varnish-cache;     git checkout d48636d23bb277ca8650a6174c872d74080f2859;     cp include/vmb.h ../src/vmb.h;     cd /work/vmod-dynamic;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 05 Apr 2022 19:11:58 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 19:11:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 19:11:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 19:11:59 GMT
USER varnish
# Tue, 05 Apr 2022 19:11:59 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 19:12:00 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4835da8a6a06c20b8df6cc2ddfd41f978b72fcea5b70942bebf8915714a18027`  
		Last Modified: Tue, 05 Apr 2022 19:16:25 GMT  
		Size: 83.6 MB (83611223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4cfdd1613e1129be77c6b90fd9e844cd4d15824bd4bf4f4112d73192ef9ea1`  
		Last Modified: Tue, 05 Apr 2022 19:15:48 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4baf57565dc415a17a031897b6ba12546044b510b9260fe92806a0ce17d22b57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51830728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca13aff345b38cd131a7f99e198b99d739d007f09d7977dabc789bdbc1f4480`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:22:16 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 07:22:17 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 07:22:18 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 07:22:19 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 07:22:20 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 07:22:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:43:49 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:43:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:43:51 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:43:52 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:43:53 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:45:14 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:45:14 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:45:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:45:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:45:17 GMT
USER varnish
# Thu, 21 Apr 2022 20:45:18 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:45:19 GMT
CMD []
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53648c9db1a4f4013c5d44e9fd4577e839980908f0dca7a76d3c8efad06d048`  
		Last Modified: Thu, 21 Apr 2022 20:47:24 GMT  
		Size: 49.1 MB (49113769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0a30b3f6f66f585ac84b9bf017f0e7975a34fd479b9701a245f950742ad5b`  
		Last Modified: Thu, 21 Apr 2022 20:47:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:de6628a1837145901ad6a52437bd103285f7830c8aa27203eea30f716f01dbe1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59292895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09ff39c7c861e7ca0f001f5e542ba94c66a520216bf35e15659ec0c23ba09b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:42:43 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 06:42:44 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 06:42:45 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 06:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 06:42:47 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 06:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:42:08 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:42:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:42:09 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:42:10 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:42:11 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:43:30 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:43:30 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:43:32 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:43:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:43:33 GMT
USER varnish
# Thu, 21 Apr 2022 20:43:34 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:43:35 GMT
CMD []
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34115bd677f7c2afb67705f651ff60b689e7a3a69b0cd15a60e3d836a0162e18`  
		Last Modified: Thu, 21 Apr 2022 20:45:21 GMT  
		Size: 56.5 MB (56473443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35e121fe38cf19136053915fbb7f2d88e8c3702004736c435aa530245164896`  
		Last Modified: Thu, 21 Apr 2022 20:45:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:e2b15844d7ef24c197ba5e2a1ef35d09957b9984bbdb80ab8072e9bd79f9153c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90095561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e485b139a84e89e60caf2503c044977eabffc55fd5d15a9c8f8cdfe9652f9899`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:48:31 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 10:48:33 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 10:48:35 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 10:48:37 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 10:48:40 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 10:48:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 05 Apr 2022 10:48:47 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 05 Apr 2022 10:48:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 05 Apr 2022 10:48:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 10:52:07 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;          mkdir -p /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     git clone https://github.com/varnishcache/varnish-cache.git;     cd varnish-cache;     git checkout d48636d23bb277ca8650a6174c872d74080f2859;     cp include/vmb.h ../src/vmb.h;     cd /work/vmod-dynamic;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 05 Apr 2022 10:52:15 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 10:52:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:52:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 10:52:19 GMT
USER varnish
# Tue, 05 Apr 2022 10:52:21 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 10:52:22 GMT
CMD []
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e676e84e66a93a6a4f0cbe85ae6eaa99b571c1e0cd879f5e13314093e421de`  
		Last Modified: Tue, 05 Apr 2022 10:55:15 GMT  
		Size: 87.3 MB (87283898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d526fce93958e73887bd935d40fbbac9413c3826d8a8dc38711b2aa7501ef`  
		Last Modified: Tue, 05 Apr 2022 10:55:02 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:10414a54f8108d64836a2c9c6c865e5f9ebe6123647c3ee57867ced916313f4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47350962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac56919f84b42f704fd7cfaaffe0a712aff857fbe24d7a894d9d4156d8c8b6a6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:10:53 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_VERSION=7.1.0
# Tue, 05 Apr 2022 06:10:53 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 05 Apr 2022 06:10:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:44:53 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:44:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:44:54 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:44:54 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkgconfig py3-sphinx
# Thu, 21 Apr 2022 20:44:54 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:46:21 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:46:22 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:46:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:46:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:46:23 GMT
USER varnish
# Thu, 21 Apr 2022 20:46:23 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:46:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a48f1c01887a27a97e883fdd3fad9fb57c191e26cc389b076ad6ce3abe007`  
		Last Modified: Thu, 21 Apr 2022 20:48:28 GMT  
		Size: 44.8 MB (44750107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c99d1795f78de1f9b33331b3ee9178f8fa9622b60f90d85b5292655323e272`  
		Last Modified: Thu, 21 Apr 2022 20:48:23 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:79d1bc5fd03b413ebc1404bcd2e4e25ba6b9697d453ebce5c8fb3e3d24d2be24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:f3df28cda6d06334a65691c1de4bcc66820033985f1520125f36547b78b910d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105363177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e101db8ad94e05a3ef6573f0d73ae802e3392a7eedf795d88212d8b66135e4e0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:16:56 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 15:16:56 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 15:16:56 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 15:16:57 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 22:07:21 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 22:07:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 22:07:21 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 22:07:21 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 22:07:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 22:10:14 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 22:10:15 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 22:10:15 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 22:10:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 22:10:15 GMT
USER varnish
# Thu, 21 Apr 2022 22:10:15 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 22:10:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1884046f45237facbf7ee696de977ca8850f655c89a819747005fda9c5df99c`  
		Last Modified: Thu, 21 Apr 2022 22:12:38 GMT  
		Size: 74.0 MB (73983724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a292aef91ba2b5542e31a24f5d934bae41a4e7e81d914802a46d4d3a8d6bc13`  
		Last Modified: Thu, 21 Apr 2022 22:12:27 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3314c10d40367f434ac9c737cd42b16d9afed9f0369868bad7257410fc62d1db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81966286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0a4145e7da62efa2bf256ec57af8719f5fd17701fd3aed235c9c49bc12e46`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 13:58:43 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Thu, 21 Apr 2022 13:58:43 GMT
ARG VARNISH_VERSION=7.1.0
# Thu, 21 Apr 2022 13:58:44 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Thu, 21 Apr 2022 13:58:44 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 13:58:45 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Thu, 21 Apr 2022 13:58:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Thu, 21 Apr 2022 13:58:46 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 14:05:20 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         mkdir /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     cp /work/varnish/pkg-varnish-cache/include/vmb.h src/vmb.h;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 14:05:21 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 14:05:22 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 14:05:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 14:05:22 GMT
USER varnish
# Thu, 21 Apr 2022 14:05:23 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 14:05:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9173eb8d6ef4a29e0abc0f63c62bf8d6027745249347bf4259506b563f4ecae`  
		Last Modified: Thu, 21 Apr 2022 14:14:21 GMT  
		Size: 55.4 MB (55390054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba783aa75b78da6b7d8a81161ba9065b52275d66c270f11001bb5d4d84c3dc5`  
		Last Modified: Thu, 21 Apr 2022 14:14:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfff2d4cc940fc0049ae0ecd1c432c4bf7f5f59ee730e47cb7517a5b7465cf42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99469391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126ab99be3dd8df097ebb773d2462bb12abbcabb8be13f323dc5ff406e815b77`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:31:46 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 17:31:47 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 17:31:48 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 17:31:49 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 17:31:50 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 17:31:51 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:40:37 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:40:38 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:40:39 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:40:40 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:40:41 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:43:32 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:43:32 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:43:34 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:43:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:43:35 GMT
USER varnish
# Thu, 21 Apr 2022 20:43:36 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:43:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a2c9a025e49931c65c1621550b8ed759c2227123492745c2775cdb0a71ca6e`  
		Last Modified: Thu, 21 Apr 2022 20:46:59 GMT  
		Size: 69.4 MB (69403116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2e3174ebcdbd61d6438f4a495a322a98ffc9ba5312a95d77ced44379856af7`  
		Last Modified: Thu, 21 Apr 2022 20:46:50 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:9e8e2bb1e2952b4bcaa32bc67336631f119cad69ba0c374763406fe34aefc95d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106725441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326aabe87cfcf2b7d546e5321566c42f3ab790e1e02adc7a711e05c5d8cdef67`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:19:29 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 17:19:29 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 17:19:30 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 17:19:31 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 17:19:32 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 17:19:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:38:55 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:38:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:38:57 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:38:58 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:38:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:41:47 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:41:47 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:41:49 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:41:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:41:50 GMT
USER varnish
# Thu, 21 Apr 2022 20:41:51 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:41:52 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46457da13e908eadea0a447ad74a77755fd841bf1abb47bc87c6d08be11873d`  
		Last Modified: Thu, 21 Apr 2022 20:44:50 GMT  
		Size: 74.3 MB (74335370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12719a93484f02b9f6424fcf767a4dc7916b4dec85f85bdf2acea301f56e994`  
		Last Modified: Thu, 21 Apr 2022 20:44:38 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:2927bfd221e8b6b1f6d199eae496dad91625eb62b56c2efab624e309347f3622
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104548169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3250f6d61c3ac7e27c621223ec9ba41a6bbf3be64f0806fe496fc74aa28defb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 06:59:19 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Thu, 21 Apr 2022 06:59:26 GMT
ARG VARNISH_VERSION=7.1.0
# Thu, 21 Apr 2022 06:59:34 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Thu, 21 Apr 2022 06:59:38 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Thu, 21 Apr 2022 06:59:46 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Thu, 21 Apr 2022 06:59:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 07:00:00 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Thu, 21 Apr 2022 07:00:02 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Thu, 21 Apr 2022 07:00:05 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 07:26:12 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         mkdir /work/varnish-modules;     cd /work/varnish-modules;     curl -fLo src.tar.gz https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz;     echo "$VARNISH_MODULES_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;         mkdir /work/vmod-dynamic;     cd /work/vmod-dynamic;     curl -fLo src.tar.gz https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz;     echo "$VMOD_DYNAMIC_SHA512SUM  src.tar.gz" | sha512sum -c -;     tar xavf src.tar.gz --strip 1;     cp /work/varnish/pkg-varnish-cache/include/vmb.h src/vmb.h;     sed -i '14 a AC_CHECK_HEADERS([stdatomic.h])' configure.ac;     ./autogen.sh;     ./configure --libdir=/usr/lib;     make -j"$(nproc)" VERBOSE=1 install;     make -j"$(nproc)" VERBOSE=1 check;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 07:26:18 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 07:26:20 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 07:26:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 07:26:27 GMT
USER varnish
# Thu, 21 Apr 2022 07:26:30 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 07:26:31 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdf0e98fdec95c180ab215269b20a4afa69c295e5bb21a2617def1309012c49`  
		Last Modified: Thu, 21 Apr 2022 08:05:30 GMT  
		Size: 69.3 MB (69262445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef1599fc9172d28d818447793a85f375d4269c360738e534ebee2e53b689a25`  
		Last Modified: Thu, 21 Apr 2022 08:05:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:7e436b56075162028c9d1e15247d726f68bb0e723f8ecb5c82f132ef6724db35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85794352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43458476d36aa1b00f68f5a50ab03b613632b2fe0a25d680edc5e0ca47fddc2e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 19:51:37 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Wed, 20 Apr 2022 19:51:38 GMT
ARG VARNISH_VERSION=7.1.0
# Wed, 20 Apr 2022 19:51:38 GMT
ARG DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73
# Wed, 20 Apr 2022 19:51:39 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Wed, 20 Apr 2022 19:51:39 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Wed, 20 Apr 2022 19:51:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Thu, 21 Apr 2022 20:41:47 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Thu, 21 Apr 2022 20:41:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Thu, 21 Apr 2022 20:41:48 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 21 Apr 2022 20:41:48 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Thu, 21 Apr 2022 20:41:48 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 20:44:32 GMT
# ARGS: DIST_SHA512=ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.0 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.0.tgz -o $tmpdir/orig.tgz;     echo "ad9ce0cdc759976fcb7044914d28863edd197167f583fab2d1bc57f4e5b86c224b7c948faf1f7364a2a16bde9c415375d011462bdc43026c5f7a60e65bd21f73  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 21 Apr 2022 20:44:34 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 20:44:34 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 20:44:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 20:44:34 GMT
USER varnish
# Thu, 21 Apr 2022 20:44:34 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 20:44:34 GMT
CMD []
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca2ed3d3c3db1d075048708d86e798d4f5533de95cb6150540d27f0221c76e2`  
		Last Modified: Thu, 21 Apr 2022 20:48:11 GMT  
		Size: 56.1 MB (56139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca96a2437ba4a34a30b1ce0d386fd7089f61e2b8f3cca90d9de74b30f45eeaa8`  
		Last Modified: Thu, 21 Apr 2022 20:48:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old`

```console
$ docker pull varnish@sha256:0bab3835b20068d32e145d205665570fe25e4b9b36d2d9ecc532264fcb706fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:cd8bbaedc6acc855d4dbde0ecbf144ffcec08ace28141a028c267a6108d5b0f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101201770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7492119e1c0f61a7ae796bfccb2774a6385a197b85402151a6b769604b65154b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:19:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 15:21:57 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 15:21:58 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 15:21:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 20 Apr 2022 15:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 15:21:58 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 15:21:58 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d4c26eb233b1f26ae0b9467fa72834229ed3d194ae98dec875b7e27670be4`  
		Last Modified: Wed, 20 Apr 2022 15:25:16 GMT  
		Size: 69.8 MB (69822317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113ca7b5e4d8bea5c4f3cfdbde42d78cedc9cc7a3f232dae8075ac49a7c6ef60`  
		Last Modified: Wed, 20 Apr 2022 15:25:06 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e4f991ee0fffceb5b576bf52af2f4187fa1c3545a35d9a27eaba2fc0f3816e20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77821225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fac8014668438566fd29bc6e67db06f71eed12ebc7deedfd06a14e3b9fc451`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 02:18:34 GMT
ADD file:e1835d1a0c70a0335757f211893e5d12ddf797e489e10434c0982bdf9b234f67 in / 
# Tue, 29 Mar 2022 02:18:36 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 04:58:07 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 05:03:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 05:03:41 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 05:03:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 05:03:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 05:03:42 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 05:03:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f98812e1a494a683a5b3dea593dd2ef305f5f732193044c147f22e44b00164bc`  
		Last Modified: Tue, 29 Mar 2022 02:34:13 GMT  
		Size: 26.6 MB (26575370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f7b6d4c7611e504f11c8135d715741175aae45a8b5c8f9fd2a514cf69022e5`  
		Last Modified: Wed, 30 Mar 2022 05:09:52 GMT  
		Size: 51.2 MB (51245383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761275f2ac473d69f8c0c3ec1b4b46d5d9572a82bac140e031cb00ee8ffbffb3`  
		Last Modified: Wed, 30 Mar 2022 05:09:24 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ea65c75635fd3e13c03da16c68995ed4f38ae3b63ffd798fd210a7470fe0be2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95311405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b7b74bf809ee04653fc225dc513a72a1bc98e4600df9d6ab8745e3df50fd09`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:51:42 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:54:27 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:54:28 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:54:29 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:54:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:54:30 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:54:31 GMT
CMD []
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b31818a80ab96d113ecc26bae4c921e8b1f15bd573c0567be45beb836048700`  
		Last Modified: Wed, 30 Mar 2022 00:59:33 GMT  
		Size: 65.2 MB (65246620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa175bc0d41052fdda42c92374ca4cf78d073d37324d6526efe02454a651cd`  
		Last Modified: Wed, 30 Mar 2022 00:59:24 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:259397fb199c0e9f739100dd0a93efb9a86e60827e66c65ed051b3e44ad83b93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102585485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01443ed33f01c5f1b4ed80c2b5351ad547ab887260ae9a4db797dc6623f747a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:23:01 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 17:25:18 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 17:25:19 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 17:25:20 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 20 Apr 2022 17:25:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 17:25:21 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 17:25:22 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47edc9eab3e86eb0355d68502318a630dc795c5d8d4d8779d7321b6b553cf98`  
		Last Modified: Wed, 20 Apr 2022 17:29:13 GMT  
		Size: 70.2 MB (70195418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aea8a62b1f5f50f6761a32239f5adc670e7af72f8b59664619186ddeae2fef`  
		Last Modified: Wed, 20 Apr 2022 17:29:04 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:9dfbab1f66da09461280e2006a8637a71cacc99345a3e005eb4cdd75f34e0057
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100376258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84ffd81229d9e36b2fe44a2d56797edb9d2f84a293a32b202b77177c2d0aa18`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 07:26:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 07:44:15 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 07:44:20 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 07:44:22 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 21 Apr 2022 07:44:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 07:44:27 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 07:44:30 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddab9d225e329687fa4c9dbced15d44e0e90e64944867273cba0d7432395dfef`  
		Last Modified: Thu, 21 Apr 2022 08:06:05 GMT  
		Size: 65.1 MB (65090535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761715f8917a3a374aa705b10b377f1eb661cb0b7c33a6bc93d79f00ac0dede5`  
		Last Modified: Thu, 21 Apr 2022 08:05:52 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:7b2d1d1fc79b00edd1129e176ec751b1c9e3372c2dff553327f9e66c3f00c57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81637417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af65f783a437fab01c28d0c2ade060a88aa9cded965a28602d723c9c41d8a18`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:51:57 GMT
ADD file:39c5e0d7a686abd19448ab3e6237d50955ae2187fc2b64289a08c2549352b8f1 in / 
# Tue, 29 Mar 2022 00:51:58 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:54:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:56:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:56:42 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:56:42 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:56:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:56:42 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:56:42 GMT
CMD []
```

-	Layers:
	-	`sha256:ffb22bcde95509bb75f6dd2d69f3fdb5c7471727e4d720b31d92cd297582865c`  
		Last Modified: Tue, 29 Mar 2022 01:04:43 GMT  
		Size: 29.7 MB (29655426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aabcd8580e9559702629fa9ee5e4029a5b1318fe425c2ae5725d6e84a8c2e0d`  
		Last Modified: Wed, 30 Mar 2022 01:00:29 GMT  
		Size: 52.0 MB (51981518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac10509f97438a4a52957c04e3ce7ad59423d6b7f865b29a3d1462ec09ea52e`  
		Last Modified: Wed, 30 Mar 2022 01:00:25 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:a96966b666c3eb795b5a5ffe4b7f1911e009156774d5551a355de6ba17dd6ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:1f798a786c909e75214591ae7bb11711b606d19904771e17cac071e3fc945f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58347562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f303a05efad59d4625679d65998e25ac6af2a5a1e8e761d6165038faf0af7a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:46:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 09:47:16 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 09:47:16 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 09:47:16 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 09:47:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 09:47:16 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 09:47:16 GMT
CMD []
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd49c5f702ffa093526e350e19af19adacee36ebd21a4d2b8215729aebd24701`  
		Last Modified: Tue, 05 Apr 2022 09:48:23 GMT  
		Size: 55.5 MB (55528711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b11f3cacc52df447f6e49ab5dcad0b25a3e95d3aa5ca786c8a00b94bcea4d97`  
		Last Modified: Tue, 05 Apr 2022 09:48:15 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d0ef8137631136de68aa9ca8b5a1c202753588e4823091fc74c7381800475e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44158672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b498faee8096b05f4ad1e1a034d79076f1405006bbb01cdc1b62443d19faf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 19:12:30 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 19:13:58 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 19:13:59 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 19:13:59 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 19:14:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 19:14:00 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 19:14:00 GMT
CMD []
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a122a3f3e3f4f262ecd7c937fb5b761d7c7025f6b85195b6f6e59efccc3e22`  
		Last Modified: Tue, 05 Apr 2022 19:17:11 GMT  
		Size: 41.7 MB (41730222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e23c5ffb616fb8979712f573ce76a21ff2948ffe3c222f25abeda1b044fb82`  
		Last Modified: Tue, 05 Apr 2022 19:16:49 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:287bbe458761ddf7b90152156bcfcf1680e8229b94e87c6be21fcdcff4105325
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51100328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb806b4ff6eae8a70eec669d64a63205e9fa899f74021c50544a8a3fe8492216`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:24:20 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 07:25:05 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 07:25:05 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 07:25:07 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 07:25:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 07:25:08 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 07:25:09 GMT
CMD []
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c097d0722cedf772b294574bd3df3ea7bc3fd2a7f0d584bdda75906ab4a4f76`  
		Last Modified: Tue, 05 Apr 2022 07:26:39 GMT  
		Size: 48.4 MB (48382460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda2d05467662609f11c35127449028bdba318e2920842c0c49a157d72fd14d4`  
		Last Modified: Tue, 05 Apr 2022 07:26:32 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:8d9a98e8ebe8c794faad1ca62b64b1d0f5d50b4bdc61593272165af938c90e58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58550969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b86a5912210274cdd2be334341ab5c8a5cc8b98b8cacbf00d0bc3b61391b34`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:38:32 GMT
ADD file:6508514d43b69774a3307679ef8f6dba0faf707e62ad6c6c1c8cf40d84e12d1d in / 
# Mon, 04 Apr 2022 23:38:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:44:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 06:45:29 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 06:45:29 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 06:45:31 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 06:45:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 06:45:32 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 06:45:33 GMT
CMD []
```

-	Layers:
	-	`sha256:c11e5e1035714514f6e237dffd1836a4d03b48af64e55a8e08f9bd9e998e24a9`  
		Last Modified: Mon, 04 Apr 2022 23:39:35 GMT  
		Size: 2.8 MB (2821213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781285b91779b0524f4a4b362a85bf7ad3c11049ec60271bc351d3ea22722f55`  
		Last Modified: Tue, 05 Apr 2022 06:47:18 GMT  
		Size: 55.7 MB (55729277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ede4c98a857e7e2e4374c87b05da88e9cfa36a1b9d2261f338a8e4cc091689`  
		Last Modified: Tue, 05 Apr 2022 06:47:09 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:99fc715aa51f45f415d42e16933cfd6640741633a9df875d1be9c41bb5eea1e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48200204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afb3e6b26fed2aaed2bdf33c3edb6718410d71cdda8521c1e6a42a745e020d3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:52:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 10:53:50 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 10:53:55 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 10:53:56 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 10:53:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 10:54:00 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 10:54:02 GMT
CMD []
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7876f582583c6ce1dd934300234645dd5b97252662a8c87fdfbf82c860328d90`  
		Last Modified: Tue, 05 Apr 2022 10:55:44 GMT  
		Size: 45.4 MB (45385557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bba04077c5c30296939df9ed09482547b8947d5decf08a738273fa064ca121a`  
		Last Modified: Tue, 05 Apr 2022 10:55:36 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d23bba4fca1b0dd78c6f32996dd386b94a4944ac5ea047d049913f9f2c51e200
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113021b450dcbd4035fcfba58dd928217e0d39bff640b6d895c83e8eb2592df4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:12:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 05 Apr 2022 06:13:11 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.2/" 	-e 's@^source=.*@source="https://varnish-cache.org/downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Tue, 05 Apr 2022 06:13:13 GMT
WORKDIR /etc/varnish
# Tue, 05 Apr 2022 06:13:13 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 05 Apr 2022 06:13:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 05 Apr 2022 06:13:13 GMT
EXPOSE 80 8443
# Tue, 05 Apr 2022 06:13:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df61fc68478458a071e8edf49185d9b224067a6e66831cdde802e5d2b66b097`  
		Last Modified: Tue, 05 Apr 2022 06:14:33 GMT  
		Size: 44.1 MB (44067532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829d58f668fddd7b5ed61e0d6c27f5b3abd19844eeb8ad111b395b944d064904`  
		Last Modified: Tue, 05 Apr 2022 06:14:27 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:f28e4d5218f748b4cc583d5479bd50ce28f686cb26b6a11394c2b11324ff0116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:8b44a4c2f06876e38f998ac52b1b5eeb5722217b1374ed6d1d2a86788063b841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100590037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0388102969cbf53831d827235b7c512314159ef8b62c62f62e56a42be8eec33f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 15:19:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 15:24:19 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 15:24:20 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 15:24:20 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 15:24:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 15:24:20 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 15:24:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1ca7fca2c8edea4f001c6fca0411697c9d5e56f8492bd1ba90f2a6096bda2e`  
		Last Modified: Wed, 20 Apr 2022 15:25:40 GMT  
		Size: 69.2 MB (69210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c25bb177ab25201b8d89d4a7ac60b0cd82e581b252db5ae6cec2d81e09f09fc`  
		Last Modified: Wed, 20 Apr 2022 15:25:30 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a2f0a9f702cf2b39ca80ffcb82961a60bbc68a8fc5d37a62da0a6212f3d29eb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77224693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f98b4a10b8edfdf6e66d2ac8f10b34ba94b3ef543e44fb25f6a2cefa40be1f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 14:05:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 14:12:34 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 14:12:36 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 14:12:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 21 Apr 2022 14:12:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 14:12:38 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 14:12:39 GMT
CMD []
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d7b88c6c49f137f382e6f87256bebefe35ee1bd250c2be3c5e92b4a4b41e1`  
		Last Modified: Thu, 21 Apr 2022 14:15:09 GMT  
		Size: 50.6 MB (50648234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddb1c28572171a2274f9094026118a450de3eebfa5127411281f12f60b0c000`  
		Last Modified: Thu, 21 Apr 2022 14:14:51 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d06ba1b2751ee17970be1dc7fef64bface39548af4c87d52890dcbbff810f0f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94712514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17558ce401d3d5978e7c221146ee2ea1938db7212681314b424199f9f6c69838`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 00:51:42 GMT
ENV VARNISH_SIZE=100M
# Wed, 30 Mar 2022 00:58:54 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 30 Mar 2022 00:58:54 GMT
WORKDIR /etc/varnish
# Wed, 30 Mar 2022 00:58:56 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 30 Mar 2022 00:58:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 30 Mar 2022 00:58:57 GMT
EXPOSE 80 8443
# Wed, 30 Mar 2022 00:58:58 GMT
CMD []
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd8694684e136aa212a9714d153d127c234e4c7d0fe71e03e3a5d6ab9813ecc`  
		Last Modified: Wed, 30 Mar 2022 01:00:18 GMT  
		Size: 64.6 MB (64647503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b730ab0811c67684f9f78f611e358243f883c3320a1230f8d22e28a385cd44`  
		Last Modified: Wed, 30 Mar 2022 01:00:08 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:ff04e6a007e6477f911cd890847e670d56ab77a595548f59b111b44b98f41f08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102072699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192058a187a8c2923c5d6916640d33fa10d39b60240d19c2114bb6d2b005b374`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 07:37:35 GMT
ADD file:460761e2baaea91893a907ce122ff7d585ef5704f48c03454835986028a1d842 in / 
# Wed, 20 Apr 2022 07:37:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:23:01 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 17:27:47 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 17:27:48 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 17:27:49 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 17:27:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 17:27:50 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 17:27:51 GMT
CMD []
```

-	Layers:
	-	`sha256:6e5c4eb151e267d273883db6e9aee3ff01be07e098ca33f0d1d65bb0e0416921`  
		Last Modified: Wed, 20 Apr 2022 07:44:54 GMT  
		Size: 32.4 MB (32389597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fcee3146dcc754b299a98036e48fa76f36f7c629a2890bf5436b42ea38d7e1`  
		Last Modified: Wed, 20 Apr 2022 17:29:40 GMT  
		Size: 69.7 MB (69682400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb9c6d70bc7f4ae0e7a597a5a18364592f3bb2c33ebebf45756093ee888959`  
		Last Modified: Wed, 20 Apr 2022 17:29:30 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:c7e3a8a346402ae2dd6a844b519b55d8d7663f9b80c6064e30033a9bc6b23a27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99793645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbc5db50ecdce77bbf9a3bd8d0dc77aeac9f3c827e5b34a2f6d1d562e3611d6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 09:46:36 GMT
ADD file:8d406ebce4d9b0884d46ee25ec31fe7714726024b80aba9b408d81d39e2f6f8c in / 
# Wed, 20 Apr 2022 09:46:44 GMT
CMD ["bash"]
# Thu, 21 Apr 2022 07:26:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 21 Apr 2022 08:04:12 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 21 Apr 2022 08:04:17 GMT
WORKDIR /etc/varnish
# Thu, 21 Apr 2022 08:04:18 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 21 Apr 2022 08:04:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 21 Apr 2022 08:04:22 GMT
EXPOSE 80 8443
# Thu, 21 Apr 2022 08:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:5e0d035960b14409a1ddb839de80aa08677b71addd5e94264ff9ee89a2523e5b`  
		Last Modified: Wed, 20 Apr 2022 09:56:59 GMT  
		Size: 35.3 MB (35285249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0d43e60a69dfadc43a5b66afb309fb7f38786253c4803557286895cb860d01`  
		Last Modified: Thu, 21 Apr 2022 08:06:41 GMT  
		Size: 64.5 MB (64507698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527abc12e54faba92bbdaaba9677b139501ea022a7793c0e8dee979ed6f4822e`  
		Last Modified: Thu, 21 Apr 2022 08:06:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:cd6e1971c7ba432941c074af2f67998deaf2299a8bbcce272da8af78a9438076
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81008041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cb6823bbeb84e6a370bc9981d400a4c30acbc5d79ea21c30fac05dba331fb9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 20 Apr 2022 08:39:37 GMT
ADD file:c3381330644d6d9fc585301395580b564cdf7c880fb2dc2d8e48992673184f7d in / 
# Wed, 20 Apr 2022 08:39:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 19:58:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 20 Apr 2022 20:02:44 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.10.tgz -o $tmpdir/orig.tgz;     echo "b89ac4465aacde2fde963642727d20d7d33d04f89c0764c43d59fe13e70fe729079fef44da28cc0090fa153ec584a0fe9723fd2ce976e8e9021410a5f73eadd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.10|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 20 Apr 2022 20:02:47 GMT
WORKDIR /etc/varnish
# Wed, 20 Apr 2022 20:02:47 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 20 Apr 2022 20:02:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 20 Apr 2022 20:02:47 GMT
EXPOSE 80 8443
# Wed, 20 Apr 2022 20:02:48 GMT
CMD []
```

-	Layers:
	-	`sha256:3179e1eccb473ae22a70e8ac3e9ddb4660ebdfd977989d115bd4d322ecc12b89`  
		Last Modified: Wed, 20 Apr 2022 08:49:39 GMT  
		Size: 29.7 MB (29654805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dd8f2c1b1715ce878a36dc931f63e342a10035c85178754400d59ffcb7845a`  
		Last Modified: Wed, 20 Apr 2022 20:04:13 GMT  
		Size: 51.4 MB (51352538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38455ce12c1b61bfdfdf5b127f16bf342c77d82e2f0c101325a6837a5674db0`  
		Last Modified: Wed, 20 Apr 2022 20:04:06 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
