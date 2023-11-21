## `varnish:stable`

```console
$ docker pull varnish@sha256:6df9a385d8a0eb59a3a577895c1abf990cc54c924cd3ab7a8fe5376708bc7037
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
$ docker pull varnish@sha256:b2da77a65fb800584255aedea8bac42b8f3a725e3c40518657b412a10a5bd991
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95851853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f213b3b4551b273a5786510ced4ac312d6200f13ec09c0a08753b840e985e1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 20:46:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 21 Nov 2023 20:48:08 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 21 Nov 2023 20:48:08 GMT
WORKDIR /etc/varnish
# Tue, 21 Nov 2023 20:48:08 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 21 Nov 2023 20:48:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 21 Nov 2023 20:48:09 GMT
EXPOSE 80 8443
# Tue, 21 Nov 2023 20:48:09 GMT
CMD []
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf4c4f08b5ec8f08c9cc92454f54024af547d2029c7cbed8c1fd909b8bc475c`  
		Last Modified: Tue, 21 Nov 2023 20:49:20 GMT  
		Size: 64.4 MB (64433328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43fcf1cf62dfe5afbcf811d328c927c843348719eb93f30b1d8735e342b1ebd`  
		Last Modified: Tue, 21 Nov 2023 20:49:11 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:b504e7fd4baade812a81d44303b2f7dfca41a12448ae67593bf9af9631a7e7c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72851076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dfa32b5692e0fea516a597abb6a7ba0d1e7f30b630e160dcd6ff5cb8473342`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 21 Nov 2023 03:58:04 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Tue, 21 Nov 2023 03:58:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 11:26:20 GMT
ENV VARNISH_SIZE=100M
# Tue, 21 Nov 2023 11:28:07 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 21 Nov 2023 11:28:07 GMT
WORKDIR /etc/varnish
# Tue, 21 Nov 2023 11:28:07 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 21 Nov 2023 11:28:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 21 Nov 2023 11:28:07 GMT
EXPOSE 80 8443
# Tue, 21 Nov 2023 11:28:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1891b0978b5dcef901a1aa5e099cf843811982c8e7df07f5211c0733759e3328`  
		Last Modified: Tue, 21 Nov 2023 11:29:20 GMT  
		Size: 46.3 MB (46271361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0411e198bc39e03f94610bb0d440d25ac806567cb5158091bdff8e116f27fde`  
		Last Modified: Tue, 21 Nov 2023 11:29:13 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:793f5005ad03613e1ce87635958b4a492bf0d7b99bc784865bded8071d58ffa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89947315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b54e0b0697ad0ac9e3086eaaf33b7c0d3388fc785ab115ec70bded84f7bfe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:58:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 Nov 2023 19:09:26 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 Nov 2023 19:09:27 GMT
WORKDIR /etc/varnish
# Tue, 14 Nov 2023 19:09:27 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 14 Nov 2023 19:09:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 Nov 2023 19:09:27 GMT
EXPOSE 80 8443
# Tue, 14 Nov 2023 19:09:27 GMT
CMD []
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e063fb3b15972ee782972ea002b0768df4e7573eaa6710d3216a89d6fef105`  
		Last Modified: Tue, 14 Nov 2023 19:11:12 GMT  
		Size: 59.9 MB (59882709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43236c977dcc592f56fa8e14b1ffc64156b6314bb51e5779e090fd2b529ea349`  
		Last Modified: Tue, 14 Nov 2023 19:11:05 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:b842943e7429125c62902f678680031c957134e780aa6a48987613a05c2cbaa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97117939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96d47bae6ce87e0790321c40cc2ab5911bae135d4660b8588780fb7702b9ef4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 21 Nov 2023 04:40:15 GMT
ADD file:7de881b584405a880c4d02778056aaa81bb5dd5d1af65b3086d66aed9ff0ad4b in / 
# Tue, 21 Nov 2023 04:40:16 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 15:18:48 GMT
ENV VARNISH_SIZE=100M
# Tue, 21 Nov 2023 15:20:59 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 21 Nov 2023 15:21:00 GMT
WORKDIR /etc/varnish
# Tue, 21 Nov 2023 15:21:00 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 21 Nov 2023 15:21:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 21 Nov 2023 15:21:01 GMT
EXPOSE 80 8443
# Tue, 21 Nov 2023 15:21:01 GMT
CMD []
```

-	Layers:
	-	`sha256:75c11612678b54e79a38118fe66e532c61b3d0798afb741007b4cd3209c0ec4e`  
		Last Modified: Tue, 21 Nov 2023 04:45:24 GMT  
		Size: 32.4 MB (32402632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92ff281c7632f3cc43de9266bd270b60c9947c71d8ecd4447a642432aa474a2`  
		Last Modified: Tue, 21 Nov 2023 15:22:37 GMT  
		Size: 64.7 MB (64714607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e11325b795fce4ed6da4516d07a680b0fed89bf469efa769f3bdd733bdd505`  
		Last Modified: Tue, 21 Nov 2023 15:22:24 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:eae28db647a78e9c81e7a12d56a54ddb38acc4196be62bd474fc6065f09c5260
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94635754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb31ef67ecd67eeae948cbf7035f3a62f9b306540d58cfdfb8cf6e6544f6a5e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:58:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 21 Nov 2023 13:01:18 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 21 Nov 2023 13:01:21 GMT
WORKDIR /etc/varnish
# Tue, 21 Nov 2023 13:01:21 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 21 Nov 2023 13:01:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 21 Nov 2023 13:01:21 GMT
EXPOSE 80 8443
# Tue, 21 Nov 2023 13:01:21 GMT
CMD []
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569c6d4e2d1dbb35d3b9ee83520833f8382e7eb87b7e6962c8d2e4c0be7806dd`  
		Last Modified: Tue, 21 Nov 2023 13:02:46 GMT  
		Size: 59.3 MB (59341325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448e034f0cac91c1eefcc5bec2f728aa50eb54a22d0abb010d4f5a8e3ad28047`  
		Last Modified: Tue, 21 Nov 2023 13:02:36 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:dde8be6d61dbfe04c80ef6d0d6682b48f56341286e20b120dfc09af19213f1b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76249420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d3d4e88e588930ceaf093f701e19d7e4576220bcdc6781ce47270faab78c62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 21 Nov 2023 05:05:18 GMT
ADD file:a545f27075704ce13e33e539170d3f47007424d2cc2bea5aecfd2608a5194151 in / 
# Tue, 21 Nov 2023 05:05:22 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:00:48 GMT
ENV VARNISH_SIZE=100M
# Tue, 21 Nov 2023 06:02:26 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 21 Nov 2023 06:02:31 GMT
WORKDIR /etc/varnish
# Tue, 21 Nov 2023 06:02:31 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 21 Nov 2023 06:02:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 21 Nov 2023 06:02:31 GMT
EXPOSE 80 8443
# Tue, 21 Nov 2023 06:02:31 GMT
CMD []
```

-	Layers:
	-	`sha256:b114072f1cab66b7376d690985b12816aebab2e4e41fc170e32f111df27951dc`  
		Last Modified: Tue, 21 Nov 2023 05:10:48 GMT  
		Size: 29.7 MB (29656938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f7bc93840abcf3ea916b48272ab2c1bca7b40c609c5d88dc691c12ef4a6db`  
		Last Modified: Tue, 21 Nov 2023 06:03:43 GMT  
		Size: 46.6 MB (46591782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c145c7d7422df63661fab6f076ca87bb1fdb71bc38c795a655e3b85010d35dd`  
		Last Modified: Tue, 21 Nov 2023 06:03:31 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
