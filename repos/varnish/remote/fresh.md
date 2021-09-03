## `varnish:fresh`

```console
$ docker pull varnish@sha256:ae944e6e47550ec6b46d70f5ef78fb565278fe209db0a65bb11dfb77ec442050
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
$ docker pull varnish@sha256:bd055ff3af08e0289afc57083486e19b86ca6f303ac701f9569f82a49837af00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4fe6ea2a611a46a677fa808bcf79ffbc55d7203bb1ab07dbe90d41a2f9d53e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 03 Sep 2021 01:21:21 GMT
ADD file:19d7ba0fceddd7fc78b5fb96cf8110e5d10e0e5d2554030dfe640d161379cb79 in / 
# Fri, 03 Sep 2021 01:21:21 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 19:35:42 GMT
ENV VARNISH_SIZE=100M
# Fri, 03 Sep 2021 19:38:45 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 03 Sep 2021 19:38:46 GMT
WORKDIR /etc/varnish
# Fri, 03 Sep 2021 19:38:47 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 03 Sep 2021 19:38:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 03 Sep 2021 19:38:48 GMT
EXPOSE 80 8443
# Fri, 03 Sep 2021 19:38:48 GMT
CMD []
```

-	Layers:
	-	`sha256:f8416d8bac72cefc0ce17bd2dc0c03aa43e123d309db92ee23be9382192cf2ed`  
		Last Modified: Fri, 03 Sep 2021 01:27:25 GMT  
		Size: 31.4 MB (31368702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8721d22f3aeca3ec07ec26135e20cbaad7e5372fd92692b5fa624b2ba90c96e`  
		Last Modified: Fri, 03 Sep 2021 19:42:32 GMT  
		Size: 69.6 MB (69642862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753b74a29a3864439f0ff0428eb4b475c8af9109d3929ba30566062d5b40d9a7`  
		Last Modified: Fri, 03 Sep 2021 19:42:21 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:fee1c6951660dc650ddad24327e1db524a72cfe0a08e33669044b167c92550ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77638131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ada2287186a0a2a4e86a09ef7ab094c4942fd86ed0feb1fc9c6164e78d0434c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 03 Sep 2021 00:59:39 GMT
ADD file:94917ec8eb06f96483e43104557dd98e5160895900a9d49318eecbb3d5689d41 in / 
# Fri, 03 Sep 2021 00:59:39 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:30:03 GMT
ENV VARNISH_SIZE=100M
# Fri, 03 Sep 2021 02:35:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 03 Sep 2021 02:35:49 GMT
WORKDIR /etc/varnish
# Fri, 03 Sep 2021 02:35:50 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 03 Sep 2021 02:35:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 03 Sep 2021 02:35:51 GMT
EXPOSE 80 8443
# Fri, 03 Sep 2021 02:35:51 GMT
CMD []
```

-	Layers:
	-	`sha256:9bd46ffb253d51a8cc84bf034d289b4ca60344ca4446bf38633639b54c7c7ab9`  
		Last Modified: Fri, 03 Sep 2021 01:14:54 GMT  
		Size: 26.6 MB (26571627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8f7060d9d24d32c178df32f004297c9b7fad959e37cad0c38de2a5385ba7cc`  
		Last Modified: Fri, 03 Sep 2021 02:43:26 GMT  
		Size: 51.1 MB (51065803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92719d06be4c439a6f5144a0a11b3f34856d25310f5511b8a44c7aa2f9669ac3`  
		Last Modified: Fri, 03 Sep 2021 02:42:58 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5dbb5ddd694f5dc29b4abcc512f927729d9189758e06f18a246cec04f9a62750
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95117093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e787c5f44efd748754ad0e95b17e8bd91041925fad96da991c5dfd292f5d318c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 03 Sep 2021 00:40:33 GMT
ADD file:9600a4686ae105acffa54787a7c81f5252e90023cbcfbe37519150b954110c5c in / 
# Fri, 03 Sep 2021 00:40:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 11:22:56 GMT
ENV VARNISH_SIZE=100M
# Fri, 03 Sep 2021 11:25:14 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 03 Sep 2021 11:25:15 GMT
WORKDIR /etc/varnish
# Fri, 03 Sep 2021 11:25:15 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 03 Sep 2021 11:25:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 03 Sep 2021 11:25:15 GMT
EXPOSE 80 8443
# Fri, 03 Sep 2021 11:25:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1901ca797b5ea06f6a4facc81ad772177fdd833ed4329dc86ef126078633b949`  
		Last Modified: Fri, 03 Sep 2021 00:48:51 GMT  
		Size: 30.1 MB (30055483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6432947f57ce7924ff47d07b3d5a4f125ae19286ebf898776cf3234e3d1224`  
		Last Modified: Fri, 03 Sep 2021 11:26:28 GMT  
		Size: 65.1 MB (65060910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044a60437af21775c276529ec577a5455dea1e98f6f5e542464b1e094232bca3`  
		Last Modified: Fri, 03 Sep 2021 11:26:17 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:5f77e0a3551b7585cb383f98cb052830fb5d87e1ca2a2af66469819961eebe85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102413707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50671040d853f956c106a39bb03609044891ed0384f8f6710d769490e8ce58eb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 03 Sep 2021 00:39:52 GMT
ADD file:dcef0e50863a79295fdbbdad2086d337d6935a220550cb8adaedd7929bd7de63 in / 
# Fri, 03 Sep 2021 00:39:52 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 21:20:54 GMT
ENV VARNISH_SIZE=100M
# Fri, 03 Sep 2021 21:23:33 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 03 Sep 2021 21:23:33 GMT
WORKDIR /etc/varnish
# Fri, 03 Sep 2021 21:23:34 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 03 Sep 2021 21:23:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 03 Sep 2021 21:23:34 GMT
EXPOSE 80 8443
# Fri, 03 Sep 2021 21:23:34 GMT
CMD []
```

-	Layers:
	-	`sha256:e16e03ac165c3106d1f4265c32840999585f4c4f0e56bd13286caeef08c5be9a`  
		Last Modified: Fri, 03 Sep 2021 00:48:04 GMT  
		Size: 32.4 MB (32379875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf056f0b336dd527c551878ddbbd8241050ddc265e35761473d13a1f26c9bd4`  
		Last Modified: Fri, 03 Sep 2021 21:25:11 GMT  
		Size: 70.0 MB (70033134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eb9f25a63fcfae97518ab462e9ad375a8e4c9b5db0c5abe647e11b9a0d5d53`  
		Last Modified: Fri, 03 Sep 2021 21:24:56 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:15997be33ee30fefe5bc8111b1d099da71ceab49fbd114db65f297070666ea53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100193755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66143993eea77f62850d17f951f8d4ca8e18a457b2433378ca943c8c92fc674`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 03 Sep 2021 01:23:11 GMT
ADD file:71b4f3130e43c12907b826b33d9869308eec40607243a12d904fe47311431db9 in / 
# Fri, 03 Sep 2021 01:23:21 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 21:16:22 GMT
ENV VARNISH_SIZE=100M
# Fri, 03 Sep 2021 21:42:33 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 03 Sep 2021 21:42:41 GMT
WORKDIR /etc/varnish
# Fri, 03 Sep 2021 21:42:44 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 03 Sep 2021 21:42:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 03 Sep 2021 21:42:50 GMT
EXPOSE 80 8443
# Fri, 03 Sep 2021 21:42:54 GMT
CMD []
```

-	Layers:
	-	`sha256:be889fbf38c25cf263aa8d8c960d58470da7f841ab3f4949b8a1ac5c4514956c`  
		Last Modified: Fri, 03 Sep 2021 01:36:58 GMT  
		Size: 35.3 MB (35272405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f84733834dd5b01a28ba964d8937159e4b95d1a7117fc2cbeb11847067c58a`  
		Last Modified: Fri, 03 Sep 2021 21:44:55 GMT  
		Size: 64.9 MB (64920654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b886cf26239c19ebca2f9a273e962646f6d970202119262c75eba76f81a926`  
		Last Modified: Fri, 03 Sep 2021 21:44:43 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:76d6763a676433199ebd07ca5a3b1e14051d5ece7fff02e6d3a4734d23c4f7b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81437937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f921dcec6be90d3c8ab5cbaea5e92a6a8f44f60d8f40b2ac95a6732161364ad1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 03 Sep 2021 00:43:48 GMT
ADD file:9e72d98b2c920e433c6b776ed8eaf6a90cbf367d0ee37a8461d191499be72d39 in / 
# Fri, 03 Sep 2021 00:43:52 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 05:05:45 GMT
ENV VARNISH_SIZE=100M
# Fri, 03 Sep 2021 05:08:41 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 03 Sep 2021 05:08:44 GMT
WORKDIR /etc/varnish
# Fri, 03 Sep 2021 05:08:45 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 03 Sep 2021 05:08:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 03 Sep 2021 05:08:45 GMT
EXPOSE 80 8443
# Fri, 03 Sep 2021 05:08:46 GMT
CMD []
```

-	Layers:
	-	`sha256:33fe066e16e87fca4bcb280b7ec53d44c561299928e592068e985314cf93215b`  
		Last Modified: Fri, 03 Sep 2021 00:52:58 GMT  
		Size: 29.7 MB (29650625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223af47ec756e17feedc453b7f1d25969780cb02774c38c374b49602d87288ed`  
		Last Modified: Fri, 03 Sep 2021 05:10:24 GMT  
		Size: 51.8 MB (51786614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9bc11d1888eef75a1dea4a41b881b1960752e5c7dd91df8ca3b9e29a53e11e`  
		Last Modified: Fri, 03 Sep 2021 05:10:16 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
