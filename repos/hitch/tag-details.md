<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `hitch`

-	[`hitch:1`](#hitch1)
-	[`hitch:1.8`](#hitch18)
-	[`hitch:1.8.0`](#hitch180)
-	[`hitch:1.8.0-1`](#hitch180-1)
-	[`hitch:latest`](#hitchlatest)

## `hitch:1`

```console
$ docker pull hitch@sha256:45262bdb2098f681d0ba61d6c25eb0fbefd8771ece796a98c41139b3fb2270a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1` - linux; amd64

```console
$ docker pull hitch@sha256:a4623bcd5ef3177d57f154ee17523ccbc27e2d5056e6bac6240e09f38969ff63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32991061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ce93bc1072b63320a48feee715977fec01c775095693984b2110dacb4ff9f1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:54:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:56:05 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:56:05 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:56:05 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:56:05 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:56:05 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:56:05 GMT
CMD []
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ff41f52a3215e340ddec890974b3bd15f85680227a7e52cc3e5c8c907f1d8`  
		Last Modified: Thu, 01 Feb 2024 00:56:29 GMT  
		Size: 1.6 MB (1572818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fa56bbd5d8f0220116f7baadcf3a155f99b4a87b8a2d4e1203faff70ea41df`  
		Last Modified: Thu, 01 Feb 2024 00:56:28 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:a3b09aa6e8d1f5d670aac61719c935223192c82d204b0207f2d6febb839eb43a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28071094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2c73cbcc64daf8ef901d6bf7f3e1b0c109b7a76cefe5b1e2f30bcf5d8b8a64`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SRCVER=1.8.0
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGVER=1
# Wed, 31 Jan 2024 23:54:10 GMT
ARG DISTVER=bullseye
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Wed, 31 Jan 2024 23:55:52 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 31 Jan 2024 23:55:54 GMT
WORKDIR /etc/hitch
# Wed, 31 Jan 2024 23:55:54 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:55:54 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 31 Jan 2024 23:55:54 GMT
EXPOSE 443
# Wed, 31 Jan 2024 23:55:54 GMT
CMD []
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67854d7f42d59e5d755d5811d10d8540098bf5d884fce57ec205ff29834c06f6`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 1.5 MB (1491465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e264300dd141bbccd46bcd751eaf408e2c1527bcc8915805c310ac42f17479`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:f054c5ba6819a03d4b5227bd9f75393c97d33e331d8f3ea30373966aee78758b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31615212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefd9f7c4c3871fb1d1d1272f6c09f1312e6fb5de94e8a3f4e831d2457e84680`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 09:12:16 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 09:13:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 09:13:37 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 09:13:37 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 09:13:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 09:13:38 GMT
EXPOSE 443
# Thu, 11 Jan 2024 09:13:38 GMT
CMD []
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ad5ce62eddddd36c43710f168d19546c4133334975829025c2d32025b07a75`  
		Last Modified: Thu, 11 Jan 2024 09:14:00 GMT  
		Size: 1.6 MB (1550787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bad413c88755bba6b057915250364aded645e63782818a969dc3dea2d02cda`  
		Last Modified: Thu, 11 Jan 2024 09:13:59 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; 386

```console
$ docker pull hitch@sha256:b683cd7dcc4d6a92000484d8bd6b318f91ce50f2a06e5e3eca9a3855bfa9890a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33979519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5ef73b0fcadf8893aa36c7bc54d3e8fe6ce38faed6015765d2d913828a35e`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:39:01 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Thu, 11 Jan 2024 02:39:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:07:53 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 03:07:53 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 03:07:54 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 03:09:56 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 03:09:56 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 03:09:56 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:09:56 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 03:09:57 GMT
EXPOSE 443
# Thu, 11 Jan 2024 03:09:57 GMT
CMD []
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9b6efa1a1a7694bc9bf4b720a7a71fbf75fbbf313f78b84f64941593dbe74e`  
		Last Modified: Thu, 11 Jan 2024 03:10:09 GMT  
		Size: 1.6 MB (1576430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5471ffa497320202164cbf7178db88ed2cd46ebc4fc3aae6789e9bcbebed0d`  
		Last Modified: Thu, 11 Jan 2024 03:10:08 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; ppc64le

```console
$ docker pull hitch@sha256:abbd63d38943c48192134d90b79d99e62baf014089816950d90adfbcc0cee9c6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36926063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c526758776e31e1bfafccf9adb5f6b9699bac768f9777933963de2963833a4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:30:11 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 31 Jan 2024 22:30:14 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:42:49 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:42:49 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:42:50 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:42:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:42:51 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:47:30 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:47:32 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:47:32 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:47:33 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:47:34 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:47:34 GMT
CMD []
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d75a4cd9607ce7734cf2775908ece8521ca11f31b33ef97e25491189478db0e`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 1.6 MB (1632003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34ec8717fe70adf7f5c47cf7fac153f742e0a0b261d166fd6b879660f3e0d16`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; s390x

```console
$ docker pull hitch@sha256:87ef8651aef17d8af9810708e238965eb13f0e0612c0a50fcedf36812b18cf34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31227518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f5df1c474133a90c94a18c7d3c80a1957ba50298212733761c9b81be63bae5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 23:02:52 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Wed, 31 Jan 2024 23:02:55 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:08:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 01:08:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 01:08:29 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 01:09:54 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 01:09:55 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 01:09:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:09:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 01:09:55 GMT
EXPOSE 443
# Thu, 01 Feb 2024 01:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50938e7ab7d8fa550f407e76920f2b517a9a3d0533777fa6119389780b7c4194`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 1.6 MB (1569969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68c5f13fb276a8659f2a7c832dd647bcd1a0cb54d4c19b1be060d4297bcbb18`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.8`

```console
$ docker pull hitch@sha256:45262bdb2098f681d0ba61d6c25eb0fbefd8771ece796a98c41139b3fb2270a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.8` - linux; amd64

```console
$ docker pull hitch@sha256:a4623bcd5ef3177d57f154ee17523ccbc27e2d5056e6bac6240e09f38969ff63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32991061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ce93bc1072b63320a48feee715977fec01c775095693984b2110dacb4ff9f1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:54:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:56:05 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:56:05 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:56:05 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:56:05 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:56:05 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:56:05 GMT
CMD []
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ff41f52a3215e340ddec890974b3bd15f85680227a7e52cc3e5c8c907f1d8`  
		Last Modified: Thu, 01 Feb 2024 00:56:29 GMT  
		Size: 1.6 MB (1572818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fa56bbd5d8f0220116f7baadcf3a155f99b4a87b8a2d4e1203faff70ea41df`  
		Last Modified: Thu, 01 Feb 2024 00:56:28 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8` - linux; arm variant v7

```console
$ docker pull hitch@sha256:a3b09aa6e8d1f5d670aac61719c935223192c82d204b0207f2d6febb839eb43a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28071094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2c73cbcc64daf8ef901d6bf7f3e1b0c109b7a76cefe5b1e2f30bcf5d8b8a64`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SRCVER=1.8.0
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGVER=1
# Wed, 31 Jan 2024 23:54:10 GMT
ARG DISTVER=bullseye
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Wed, 31 Jan 2024 23:55:52 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 31 Jan 2024 23:55:54 GMT
WORKDIR /etc/hitch
# Wed, 31 Jan 2024 23:55:54 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:55:54 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 31 Jan 2024 23:55:54 GMT
EXPOSE 443
# Wed, 31 Jan 2024 23:55:54 GMT
CMD []
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67854d7f42d59e5d755d5811d10d8540098bf5d884fce57ec205ff29834c06f6`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 1.5 MB (1491465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e264300dd141bbccd46bcd751eaf408e2c1527bcc8915805c310ac42f17479`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:f054c5ba6819a03d4b5227bd9f75393c97d33e331d8f3ea30373966aee78758b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31615212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefd9f7c4c3871fb1d1d1272f6c09f1312e6fb5de94e8a3f4e831d2457e84680`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 09:12:16 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 09:13:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 09:13:37 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 09:13:37 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 09:13:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 09:13:38 GMT
EXPOSE 443
# Thu, 11 Jan 2024 09:13:38 GMT
CMD []
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ad5ce62eddddd36c43710f168d19546c4133334975829025c2d32025b07a75`  
		Last Modified: Thu, 11 Jan 2024 09:14:00 GMT  
		Size: 1.6 MB (1550787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bad413c88755bba6b057915250364aded645e63782818a969dc3dea2d02cda`  
		Last Modified: Thu, 11 Jan 2024 09:13:59 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8` - linux; 386

```console
$ docker pull hitch@sha256:b683cd7dcc4d6a92000484d8bd6b318f91ce50f2a06e5e3eca9a3855bfa9890a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33979519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5ef73b0fcadf8893aa36c7bc54d3e8fe6ce38faed6015765d2d913828a35e`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:39:01 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Thu, 11 Jan 2024 02:39:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:07:53 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 03:07:53 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 03:07:54 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 03:09:56 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 03:09:56 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 03:09:56 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:09:56 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 03:09:57 GMT
EXPOSE 443
# Thu, 11 Jan 2024 03:09:57 GMT
CMD []
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9b6efa1a1a7694bc9bf4b720a7a71fbf75fbbf313f78b84f64941593dbe74e`  
		Last Modified: Thu, 11 Jan 2024 03:10:09 GMT  
		Size: 1.6 MB (1576430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5471ffa497320202164cbf7178db88ed2cd46ebc4fc3aae6789e9bcbebed0d`  
		Last Modified: Thu, 11 Jan 2024 03:10:08 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8` - linux; ppc64le

```console
$ docker pull hitch@sha256:abbd63d38943c48192134d90b79d99e62baf014089816950d90adfbcc0cee9c6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36926063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c526758776e31e1bfafccf9adb5f6b9699bac768f9777933963de2963833a4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:30:11 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 31 Jan 2024 22:30:14 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:42:49 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:42:49 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:42:50 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:42:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:42:51 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:47:30 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:47:32 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:47:32 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:47:33 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:47:34 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:47:34 GMT
CMD []
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d75a4cd9607ce7734cf2775908ece8521ca11f31b33ef97e25491189478db0e`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 1.6 MB (1632003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34ec8717fe70adf7f5c47cf7fac153f742e0a0b261d166fd6b879660f3e0d16`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8` - linux; s390x

```console
$ docker pull hitch@sha256:87ef8651aef17d8af9810708e238965eb13f0e0612c0a50fcedf36812b18cf34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31227518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f5df1c474133a90c94a18c7d3c80a1957ba50298212733761c9b81be63bae5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 23:02:52 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Wed, 31 Jan 2024 23:02:55 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:08:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 01:08:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 01:08:29 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 01:09:54 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 01:09:55 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 01:09:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:09:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 01:09:55 GMT
EXPOSE 443
# Thu, 01 Feb 2024 01:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50938e7ab7d8fa550f407e76920f2b517a9a3d0533777fa6119389780b7c4194`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 1.6 MB (1569969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68c5f13fb276a8659f2a7c832dd647bcd1a0cb54d4c19b1be060d4297bcbb18`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.8.0`

```console
$ docker pull hitch@sha256:45262bdb2098f681d0ba61d6c25eb0fbefd8771ece796a98c41139b3fb2270a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.8.0` - linux; amd64

```console
$ docker pull hitch@sha256:a4623bcd5ef3177d57f154ee17523ccbc27e2d5056e6bac6240e09f38969ff63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32991061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ce93bc1072b63320a48feee715977fec01c775095693984b2110dacb4ff9f1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:54:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:56:05 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:56:05 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:56:05 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:56:05 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:56:05 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:56:05 GMT
CMD []
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ff41f52a3215e340ddec890974b3bd15f85680227a7e52cc3e5c8c907f1d8`  
		Last Modified: Thu, 01 Feb 2024 00:56:29 GMT  
		Size: 1.6 MB (1572818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fa56bbd5d8f0220116f7baadcf3a155f99b4a87b8a2d4e1203faff70ea41df`  
		Last Modified: Thu, 01 Feb 2024 00:56:28 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0` - linux; arm variant v7

```console
$ docker pull hitch@sha256:a3b09aa6e8d1f5d670aac61719c935223192c82d204b0207f2d6febb839eb43a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28071094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2c73cbcc64daf8ef901d6bf7f3e1b0c109b7a76cefe5b1e2f30bcf5d8b8a64`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SRCVER=1.8.0
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGVER=1
# Wed, 31 Jan 2024 23:54:10 GMT
ARG DISTVER=bullseye
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Wed, 31 Jan 2024 23:55:52 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 31 Jan 2024 23:55:54 GMT
WORKDIR /etc/hitch
# Wed, 31 Jan 2024 23:55:54 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:55:54 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 31 Jan 2024 23:55:54 GMT
EXPOSE 443
# Wed, 31 Jan 2024 23:55:54 GMT
CMD []
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67854d7f42d59e5d755d5811d10d8540098bf5d884fce57ec205ff29834c06f6`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 1.5 MB (1491465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e264300dd141bbccd46bcd751eaf408e2c1527bcc8915805c310ac42f17479`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:f054c5ba6819a03d4b5227bd9f75393c97d33e331d8f3ea30373966aee78758b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31615212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefd9f7c4c3871fb1d1d1272f6c09f1312e6fb5de94e8a3f4e831d2457e84680`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 09:12:16 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 09:13:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 09:13:37 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 09:13:37 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 09:13:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 09:13:38 GMT
EXPOSE 443
# Thu, 11 Jan 2024 09:13:38 GMT
CMD []
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ad5ce62eddddd36c43710f168d19546c4133334975829025c2d32025b07a75`  
		Last Modified: Thu, 11 Jan 2024 09:14:00 GMT  
		Size: 1.6 MB (1550787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bad413c88755bba6b057915250364aded645e63782818a969dc3dea2d02cda`  
		Last Modified: Thu, 11 Jan 2024 09:13:59 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0` - linux; 386

```console
$ docker pull hitch@sha256:b683cd7dcc4d6a92000484d8bd6b318f91ce50f2a06e5e3eca9a3855bfa9890a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33979519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5ef73b0fcadf8893aa36c7bc54d3e8fe6ce38faed6015765d2d913828a35e`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:39:01 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Thu, 11 Jan 2024 02:39:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:07:53 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 03:07:53 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 03:07:54 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 03:09:56 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 03:09:56 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 03:09:56 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:09:56 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 03:09:57 GMT
EXPOSE 443
# Thu, 11 Jan 2024 03:09:57 GMT
CMD []
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9b6efa1a1a7694bc9bf4b720a7a71fbf75fbbf313f78b84f64941593dbe74e`  
		Last Modified: Thu, 11 Jan 2024 03:10:09 GMT  
		Size: 1.6 MB (1576430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5471ffa497320202164cbf7178db88ed2cd46ebc4fc3aae6789e9bcbebed0d`  
		Last Modified: Thu, 11 Jan 2024 03:10:08 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0` - linux; ppc64le

```console
$ docker pull hitch@sha256:abbd63d38943c48192134d90b79d99e62baf014089816950d90adfbcc0cee9c6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36926063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c526758776e31e1bfafccf9adb5f6b9699bac768f9777933963de2963833a4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:30:11 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 31 Jan 2024 22:30:14 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:42:49 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:42:49 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:42:50 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:42:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:42:51 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:47:30 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:47:32 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:47:32 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:47:33 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:47:34 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:47:34 GMT
CMD []
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d75a4cd9607ce7734cf2775908ece8521ca11f31b33ef97e25491189478db0e`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 1.6 MB (1632003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34ec8717fe70adf7f5c47cf7fac153f742e0a0b261d166fd6b879660f3e0d16`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0` - linux; s390x

```console
$ docker pull hitch@sha256:87ef8651aef17d8af9810708e238965eb13f0e0612c0a50fcedf36812b18cf34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31227518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f5df1c474133a90c94a18c7d3c80a1957ba50298212733761c9b81be63bae5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 23:02:52 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Wed, 31 Jan 2024 23:02:55 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:08:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 01:08:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 01:08:29 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 01:09:54 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 01:09:55 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 01:09:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:09:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 01:09:55 GMT
EXPOSE 443
# Thu, 01 Feb 2024 01:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50938e7ab7d8fa550f407e76920f2b517a9a3d0533777fa6119389780b7c4194`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 1.6 MB (1569969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68c5f13fb276a8659f2a7c832dd647bcd1a0cb54d4c19b1be060d4297bcbb18`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.8.0-1`

```console
$ docker pull hitch@sha256:45262bdb2098f681d0ba61d6c25eb0fbefd8771ece796a98c41139b3fb2270a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.8.0-1` - linux; amd64

```console
$ docker pull hitch@sha256:a4623bcd5ef3177d57f154ee17523ccbc27e2d5056e6bac6240e09f38969ff63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32991061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ce93bc1072b63320a48feee715977fec01c775095693984b2110dacb4ff9f1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:54:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:56:05 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:56:05 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:56:05 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:56:05 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:56:05 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:56:05 GMT
CMD []
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ff41f52a3215e340ddec890974b3bd15f85680227a7e52cc3e5c8c907f1d8`  
		Last Modified: Thu, 01 Feb 2024 00:56:29 GMT  
		Size: 1.6 MB (1572818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fa56bbd5d8f0220116f7baadcf3a155f99b4a87b8a2d4e1203faff70ea41df`  
		Last Modified: Thu, 01 Feb 2024 00:56:28 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:a3b09aa6e8d1f5d670aac61719c935223192c82d204b0207f2d6febb839eb43a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28071094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2c73cbcc64daf8ef901d6bf7f3e1b0c109b7a76cefe5b1e2f30bcf5d8b8a64`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SRCVER=1.8.0
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGVER=1
# Wed, 31 Jan 2024 23:54:10 GMT
ARG DISTVER=bullseye
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Wed, 31 Jan 2024 23:55:52 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 31 Jan 2024 23:55:54 GMT
WORKDIR /etc/hitch
# Wed, 31 Jan 2024 23:55:54 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:55:54 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 31 Jan 2024 23:55:54 GMT
EXPOSE 443
# Wed, 31 Jan 2024 23:55:54 GMT
CMD []
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67854d7f42d59e5d755d5811d10d8540098bf5d884fce57ec205ff29834c06f6`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 1.5 MB (1491465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e264300dd141bbccd46bcd751eaf408e2c1527bcc8915805c310ac42f17479`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:f054c5ba6819a03d4b5227bd9f75393c97d33e331d8f3ea30373966aee78758b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31615212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefd9f7c4c3871fb1d1d1272f6c09f1312e6fb5de94e8a3f4e831d2457e84680`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 09:12:16 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 09:13:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 09:13:37 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 09:13:37 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 09:13:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 09:13:38 GMT
EXPOSE 443
# Thu, 11 Jan 2024 09:13:38 GMT
CMD []
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ad5ce62eddddd36c43710f168d19546c4133334975829025c2d32025b07a75`  
		Last Modified: Thu, 11 Jan 2024 09:14:00 GMT  
		Size: 1.6 MB (1550787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bad413c88755bba6b057915250364aded645e63782818a969dc3dea2d02cda`  
		Last Modified: Thu, 11 Jan 2024 09:13:59 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0-1` - linux; 386

```console
$ docker pull hitch@sha256:b683cd7dcc4d6a92000484d8bd6b318f91ce50f2a06e5e3eca9a3855bfa9890a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33979519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5ef73b0fcadf8893aa36c7bc54d3e8fe6ce38faed6015765d2d913828a35e`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:39:01 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Thu, 11 Jan 2024 02:39:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:07:53 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 03:07:53 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 03:07:54 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 03:09:56 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 03:09:56 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 03:09:56 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:09:56 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 03:09:57 GMT
EXPOSE 443
# Thu, 11 Jan 2024 03:09:57 GMT
CMD []
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9b6efa1a1a7694bc9bf4b720a7a71fbf75fbbf313f78b84f64941593dbe74e`  
		Last Modified: Thu, 11 Jan 2024 03:10:09 GMT  
		Size: 1.6 MB (1576430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5471ffa497320202164cbf7178db88ed2cd46ebc4fc3aae6789e9bcbebed0d`  
		Last Modified: Thu, 11 Jan 2024 03:10:08 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:abbd63d38943c48192134d90b79d99e62baf014089816950d90adfbcc0cee9c6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36926063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c526758776e31e1bfafccf9adb5f6b9699bac768f9777933963de2963833a4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:30:11 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 31 Jan 2024 22:30:14 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:42:49 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:42:49 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:42:50 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:42:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:42:51 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:47:30 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:47:32 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:47:32 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:47:33 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:47:34 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:47:34 GMT
CMD []
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d75a4cd9607ce7734cf2775908ece8521ca11f31b33ef97e25491189478db0e`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 1.6 MB (1632003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34ec8717fe70adf7f5c47cf7fac153f742e0a0b261d166fd6b879660f3e0d16`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.8.0-1` - linux; s390x

```console
$ docker pull hitch@sha256:87ef8651aef17d8af9810708e238965eb13f0e0612c0a50fcedf36812b18cf34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31227518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f5df1c474133a90c94a18c7d3c80a1957ba50298212733761c9b81be63bae5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 23:02:52 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Wed, 31 Jan 2024 23:02:55 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:08:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 01:08:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 01:08:29 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 01:09:54 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 01:09:55 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 01:09:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:09:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 01:09:55 GMT
EXPOSE 443
# Thu, 01 Feb 2024 01:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50938e7ab7d8fa550f407e76920f2b517a9a3d0533777fa6119389780b7c4194`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 1.6 MB (1569969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68c5f13fb276a8659f2a7c832dd647bcd1a0cb54d4c19b1be060d4297bcbb18`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:latest`

```console
$ docker pull hitch@sha256:45262bdb2098f681d0ba61d6c25eb0fbefd8771ece796a98c41139b3fb2270a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:latest` - linux; amd64

```console
$ docker pull hitch@sha256:a4623bcd5ef3177d57f154ee17523ccbc27e2d5056e6bac6240e09f38969ff63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32991061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ce93bc1072b63320a48feee715977fec01c775095693984b2110dacb4ff9f1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:54:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:54:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:54:28 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:56:05 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:56:05 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:56:05 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:56:05 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:56:05 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:56:05 GMT
CMD []
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ff41f52a3215e340ddec890974b3bd15f85680227a7e52cc3e5c8c907f1d8`  
		Last Modified: Thu, 01 Feb 2024 00:56:29 GMT  
		Size: 1.6 MB (1572818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fa56bbd5d8f0220116f7baadcf3a155f99b4a87b8a2d4e1203faff70ea41df`  
		Last Modified: Thu, 01 Feb 2024 00:56:28 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:a3b09aa6e8d1f5d670aac61719c935223192c82d204b0207f2d6febb839eb43a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28071094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2c73cbcc64daf8ef901d6bf7f3e1b0c109b7a76cefe5b1e2f30bcf5d8b8a64`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SRCVER=1.8.0
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGVER=1
# Wed, 31 Jan 2024 23:54:10 GMT
ARG DISTVER=bullseye
# Wed, 31 Jan 2024 23:54:10 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 31 Jan 2024 23:54:10 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Wed, 31 Jan 2024 23:55:52 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 31 Jan 2024 23:55:54 GMT
WORKDIR /etc/hitch
# Wed, 31 Jan 2024 23:55:54 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:55:54 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 31 Jan 2024 23:55:54 GMT
EXPOSE 443
# Wed, 31 Jan 2024 23:55:54 GMT
CMD []
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67854d7f42d59e5d755d5811d10d8540098bf5d884fce57ec205ff29834c06f6`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 1.5 MB (1491465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e264300dd141bbccd46bcd751eaf408e2c1527bcc8915805c310ac42f17479`  
		Last Modified: Wed, 31 Jan 2024 23:56:09 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:f054c5ba6819a03d4b5227bd9f75393c97d33e331d8f3ea30373966aee78758b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31615212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefd9f7c4c3871fb1d1d1272f6c09f1312e6fb5de94e8a3f4e831d2457e84680`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 09:12:16 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 09:12:16 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 09:12:16 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 09:13:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 09:13:37 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 09:13:37 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 09:13:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 09:13:38 GMT
EXPOSE 443
# Thu, 11 Jan 2024 09:13:38 GMT
CMD []
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ad5ce62eddddd36c43710f168d19546c4133334975829025c2d32025b07a75`  
		Last Modified: Thu, 11 Jan 2024 09:14:00 GMT  
		Size: 1.6 MB (1550787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bad413c88755bba6b057915250364aded645e63782818a969dc3dea2d02cda`  
		Last Modified: Thu, 11 Jan 2024 09:13:59 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:b683cd7dcc4d6a92000484d8bd6b318f91ce50f2a06e5e3eca9a3855bfa9890a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33979519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5ef73b0fcadf8893aa36c7bc54d3e8fe6ce38faed6015765d2d913828a35e`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 11 Jan 2024 02:39:01 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Thu, 11 Jan 2024 02:39:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:07:53 GMT
ARG SRCVER=1.8.0
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGVER=1
# Thu, 11 Jan 2024 03:07:53 GMT
ARG DISTVER=bullseye
# Thu, 11 Jan 2024 03:07:53 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 11 Jan 2024 03:07:54 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 11 Jan 2024 03:09:56 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 11 Jan 2024 03:09:56 GMT
WORKDIR /etc/hitch
# Thu, 11 Jan 2024 03:09:56 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:09:56 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 11 Jan 2024 03:09:57 GMT
EXPOSE 443
# Thu, 11 Jan 2024 03:09:57 GMT
CMD []
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9b6efa1a1a7694bc9bf4b720a7a71fbf75fbbf313f78b84f64941593dbe74e`  
		Last Modified: Thu, 11 Jan 2024 03:10:09 GMT  
		Size: 1.6 MB (1576430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5471ffa497320202164cbf7178db88ed2cd46ebc4fc3aae6789e9bcbebed0d`  
		Last Modified: Thu, 11 Jan 2024 03:10:08 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:abbd63d38943c48192134d90b79d99e62baf014089816950d90adfbcc0cee9c6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36926063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c526758776e31e1bfafccf9adb5f6b9699bac768f9777933963de2963833a4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:30:11 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 31 Jan 2024 22:30:14 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:42:49 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 00:42:49 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 00:42:50 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 00:42:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 00:42:51 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 00:47:30 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 00:47:32 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 00:47:32 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 00:47:33 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 00:47:34 GMT
EXPOSE 443
# Thu, 01 Feb 2024 00:47:34 GMT
CMD []
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d75a4cd9607ce7734cf2775908ece8521ca11f31b33ef97e25491189478db0e`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 1.6 MB (1632003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34ec8717fe70adf7f5c47cf7fac153f742e0a0b261d166fd6b879660f3e0d16`  
		Last Modified: Thu, 01 Feb 2024 00:47:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:87ef8651aef17d8af9810708e238965eb13f0e0612c0a50fcedf36812b18cf34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31227518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f5df1c474133a90c94a18c7d3c80a1957ba50298212733761c9b81be63bae5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 23:02:52 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Wed, 31 Jan 2024 23:02:55 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:08:28 GMT
ARG SRCVER=1.8.0
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGVER=1
# Thu, 01 Feb 2024 01:08:28 GMT
ARG DISTVER=bullseye
# Thu, 01 Feb 2024 01:08:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 01 Feb 2024 01:08:29 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Thu, 01 Feb 2024 01:09:54 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2 SRCVER=1.8.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 01 Feb 2024 01:09:55 GMT
WORKDIR /etc/hitch
# Thu, 01 Feb 2024 01:09:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:09:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 01 Feb 2024 01:09:55 GMT
EXPOSE 443
# Thu, 01 Feb 2024 01:09:55 GMT
CMD []
```

-	Layers:
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50938e7ab7d8fa550f407e76920f2b517a9a3d0533777fa6119389780b7c4194`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 1.6 MB (1569969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68c5f13fb276a8659f2a7c832dd647bcd1a0cb54d4c19b1be060d4297bcbb18`  
		Last Modified: Thu, 01 Feb 2024 01:11:11 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
