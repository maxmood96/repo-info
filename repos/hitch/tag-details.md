<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `hitch`

-	[`hitch:1`](#hitch1)
-	[`hitch:1.8`](#hitch18)
-	[`hitch:1.8.0`](#hitch180)
-	[`hitch:1.8.0-1`](#hitch180-1)
-	[`hitch:latest`](#hitchlatest)

## `hitch:1`

```console
$ docker pull hitch@sha256:8c070b2a392f25bfad6d5cf14b9e2fcd55db64fe05dc4c3632e98868fc338a08
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

### `hitch:1` - linux; amd64

```console
$ docker pull hitch@sha256:170cb108ee0dec44db046d4685551d5469862116ee2d222a3235f5056fa98be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31822904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f18deec619649e3999f0109a33d9f7d0514fa62f8bc7e629094a6949d57234`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d697a9ce5ab19b9e590473f743020081818fded42de57d42446e09c1ccf447`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 1.6 MB (1569795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f22c0f52ce30d1feec9ef6cce4c8f1d4525d5b1bfbb1cdb600ba5407c43500`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:4cd630e3f0e93e3770c8c0b91905f1acc2d8ab3fb30fc7586ce67d1f21aa0a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde0e57dd1c436cb292c7e1b46fe067d519a01d6e8945fe5de1aa54710d1eb5e`

```dockerfile
```

-	Layers:
	-	`sha256:8c60b76b391c7d7435d38b5faf2e51709cc59a516615649109d32ec23ac5eb01`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 2.7 MB (2690039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6696743f11f896220bc08bfcf29c7b43c206a6b2059322e12f2287bb2546cd07`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 13.6 KB (13625 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:0260faf6fc69190aab99b6880b7a09081762e31cd03c05107ec235702ea6f216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27022812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b028fa35fa3823ef019358a5d084fd842d83760f97b650db456472edfd7867a`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 20:45:43 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102431f6c85283678f018254635d8782d4ec57602cb0a684abc7458256406386`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 1.5 MB (1488408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4211154205e3c97642b3e68ba25d5f7f65623991c18b894059e8484a7dff232`  
		Last Modified: Tue, 14 Jan 2025 02:30:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:7915d6149d2416d1ed6107762d3846fd76c499a3fbcff58b014f768e558ea0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68804bf4bdca32a370bf9ed91a77827ea89991894fb20cadb793ee0f5da5cedb`

```dockerfile
```

-	Layers:
	-	`sha256:b1067f86bff6417689ee6fbb2f2768f18cd6c2ab7432bfcfd75a410913b05a09`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 2.7 MB (2692271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0b05802d226a9e24c8255c7d27a594f7919b3ceb99d495fc20b83731564014`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:b811507727ecec372a9842f21582ba11af1d744b74869e38e066475321f8af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30293284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4fdd24687e87d7d4a8271935e9094fd0af663f411966593e6c2e794bcf78cd`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a105e2bd89d8e97d81b5e9c50f97f1b0c2ea0fb95365baac64e7bb5d36bc55`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 1.5 MB (1547927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71c0f34fe225a75564e0979cc855423929ff86424670867390b9a1d4b956332`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:c924cf5c1b928970576752ecfa7b1b659ead3c3fb6b3de2af3aa8a23325ff905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2704044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c9bf8f77f312f835653c50230b722b2aac4f19e34ca7e860dfcf1de45c2e98`

```dockerfile
```

-	Layers:
	-	`sha256:954836a96a27e969580d7342dd1832250ad76b338250e21a692c37e1fe62085b`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 2.7 MB (2690303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1698a1fd8c7e744260f0fe3130388144c949ee8910c74509ec8733dcaa3701`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 13.7 KB (13741 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; 386

```console
$ docker pull hitch@sha256:5d65e9e0d32fbc7c5f1c139b9d2fa4b493d5bcf8bf356a76bf63925b75a507bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32753151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ad119c82ecf08dd836cf0d57766bbfd86ba5e7386e2a3b2c6647b22779f203`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885092d66c59fcbcff189c382da0c768de4449566489990f9343e351411a010c`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 1.6 MB (1573678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a4d221afd6c23791cee85d0d0f82248f11b7979931730a121f8e8a616663b`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:9c5fb417a207405ec17682e9b30de75091edf6468f017ac6502dbb497ef59e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6d52a1649d690009203b92d55de5d9c88b15aedc62281284e3dca9ec36f59`

```dockerfile
```

-	Layers:
	-	`sha256:a8f036d4b6818c352709fac107366aaa567c67d49303ad985115088660471b83`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 2.7 MB (2687163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f98003860bbbf9d8fb0465c220780c4f2f8835b5d94b5745d865fedaa64ad6`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 13.6 KB (13588 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; ppc64le

```console
$ docker pull hitch@sha256:1bdcd7bcd169b8de699dae282ed9132427b99bb8f3bfbac1cacbc2ce1d5b104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36928037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96c4164756efbaae82116b7b72bb2095a5138cae636ec7e0a585c93ee52057`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Tue, 07 Jan 2025 02:35:40 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96d996552b8211abcb134c637a2ff1f40f8948acc4fc03da156fc00d2cb2dd`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 1.6 MB (1628321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36644e74cb980ba714eec6ecf5729391a63781a34991264fc61069a239d5db`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:930b2a56783983d94990c5d8eb69841e1848a966f490e074c6f503c302919ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d1a71ab384aeac4980491883bcacb6682bb7ac79f99b75bdbef94246966341`

```dockerfile
```

-	Layers:
	-	`sha256:e83fceb4779f1817190640cf46aed07d46fd4b4cc148eb334f5dfafb1e675232`  
		Last Modified: Tue, 07 Jan 2025 01:35:16 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184e2f5c531bc52d63020dfb5cd44800780636aca7503a3adc510611f503d18c`  
		Last Modified: Wed, 08 Jan 2025 02:35:14 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; s390x

```console
$ docker pull hitch@sha256:d91204d37425e40a174c327556e101e756d3baae8af570d95d555175f76557b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31230843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae76908cceba307dde76e2e850f030d7571830f0b04f29b209232c4300010224`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e973ddf7be7a3ef6ce409e675b83570f4141ba68727c4e5c2f375f48cc2bc67b`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 1.6 MB (1566950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e660d42d0e4abfddbd5150c5fe8d04d19a455b3f0e9087d918b43b3324de5921`  
		Last Modified: Tue, 07 Jan 2025 22:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:03077a449c74e88e0f899654f6a39799feba8a345a61c14977d87473d71d3cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83d9dbc2df4829224947aa1ed659ad6749d36e63643e1abdfe15a0bf852fa77`

```dockerfile
```

-	Layers:
	-	`sha256:c77e4f53cec64a928050cca209f5b7c0d729347e768f45f7364466661e048246`  
		Last Modified: Mon, 06 Jan 2025 19:40:16 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be908d7cfac6586649e4fd45008a52ba458489d3ff11fa452c4ec31abe0fd571`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 13.4 KB (13416 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8`

```console
$ docker pull hitch@sha256:8c070b2a392f25bfad6d5cf14b9e2fcd55db64fe05dc4c3632e98868fc338a08
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

### `hitch:1.8` - linux; amd64

```console
$ docker pull hitch@sha256:170cb108ee0dec44db046d4685551d5469862116ee2d222a3235f5056fa98be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31822904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f18deec619649e3999f0109a33d9f7d0514fa62f8bc7e629094a6949d57234`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d697a9ce5ab19b9e590473f743020081818fded42de57d42446e09c1ccf447`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 1.6 MB (1569795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f22c0f52ce30d1feec9ef6cce4c8f1d4525d5b1bfbb1cdb600ba5407c43500`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:4cd630e3f0e93e3770c8c0b91905f1acc2d8ab3fb30fc7586ce67d1f21aa0a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde0e57dd1c436cb292c7e1b46fe067d519a01d6e8945fe5de1aa54710d1eb5e`

```dockerfile
```

-	Layers:
	-	`sha256:8c60b76b391c7d7435d38b5faf2e51709cc59a516615649109d32ec23ac5eb01`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 2.7 MB (2690039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6696743f11f896220bc08bfcf29c7b43c206a6b2059322e12f2287bb2546cd07`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 13.6 KB (13625 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; arm variant v7

```console
$ docker pull hitch@sha256:0260faf6fc69190aab99b6880b7a09081762e31cd03c05107ec235702ea6f216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27022812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b028fa35fa3823ef019358a5d084fd842d83760f97b650db456472edfd7867a`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 20:45:43 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102431f6c85283678f018254635d8782d4ec57602cb0a684abc7458256406386`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 1.5 MB (1488408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4211154205e3c97642b3e68ba25d5f7f65623991c18b894059e8484a7dff232`  
		Last Modified: Tue, 14 Jan 2025 02:30:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:7915d6149d2416d1ed6107762d3846fd76c499a3fbcff58b014f768e558ea0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68804bf4bdca32a370bf9ed91a77827ea89991894fb20cadb793ee0f5da5cedb`

```dockerfile
```

-	Layers:
	-	`sha256:b1067f86bff6417689ee6fbb2f2768f18cd6c2ab7432bfcfd75a410913b05a09`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 2.7 MB (2692271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0b05802d226a9e24c8255c7d27a594f7919b3ceb99d495fc20b83731564014`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:b811507727ecec372a9842f21582ba11af1d744b74869e38e066475321f8af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30293284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4fdd24687e87d7d4a8271935e9094fd0af663f411966593e6c2e794bcf78cd`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a105e2bd89d8e97d81b5e9c50f97f1b0c2ea0fb95365baac64e7bb5d36bc55`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 1.5 MB (1547927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71c0f34fe225a75564e0979cc855423929ff86424670867390b9a1d4b956332`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:c924cf5c1b928970576752ecfa7b1b659ead3c3fb6b3de2af3aa8a23325ff905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2704044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c9bf8f77f312f835653c50230b722b2aac4f19e34ca7e860dfcf1de45c2e98`

```dockerfile
```

-	Layers:
	-	`sha256:954836a96a27e969580d7342dd1832250ad76b338250e21a692c37e1fe62085b`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 2.7 MB (2690303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1698a1fd8c7e744260f0fe3130388144c949ee8910c74509ec8733dcaa3701`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 13.7 KB (13741 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; 386

```console
$ docker pull hitch@sha256:5d65e9e0d32fbc7c5f1c139b9d2fa4b493d5bcf8bf356a76bf63925b75a507bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32753151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ad119c82ecf08dd836cf0d57766bbfd86ba5e7386e2a3b2c6647b22779f203`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885092d66c59fcbcff189c382da0c768de4449566489990f9343e351411a010c`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 1.6 MB (1573678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a4d221afd6c23791cee85d0d0f82248f11b7979931730a121f8e8a616663b`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:9c5fb417a207405ec17682e9b30de75091edf6468f017ac6502dbb497ef59e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6d52a1649d690009203b92d55de5d9c88b15aedc62281284e3dca9ec36f59`

```dockerfile
```

-	Layers:
	-	`sha256:a8f036d4b6818c352709fac107366aaa567c67d49303ad985115088660471b83`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 2.7 MB (2687163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f98003860bbbf9d8fb0465c220780c4f2f8835b5d94b5745d865fedaa64ad6`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 13.6 KB (13588 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; ppc64le

```console
$ docker pull hitch@sha256:1bdcd7bcd169b8de699dae282ed9132427b99bb8f3bfbac1cacbc2ce1d5b104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36928037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96c4164756efbaae82116b7b72bb2095a5138cae636ec7e0a585c93ee52057`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Tue, 07 Jan 2025 02:35:40 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96d996552b8211abcb134c637a2ff1f40f8948acc4fc03da156fc00d2cb2dd`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 1.6 MB (1628321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36644e74cb980ba714eec6ecf5729391a63781a34991264fc61069a239d5db`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:930b2a56783983d94990c5d8eb69841e1848a966f490e074c6f503c302919ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d1a71ab384aeac4980491883bcacb6682bb7ac79f99b75bdbef94246966341`

```dockerfile
```

-	Layers:
	-	`sha256:e83fceb4779f1817190640cf46aed07d46fd4b4cc148eb334f5dfafb1e675232`  
		Last Modified: Tue, 07 Jan 2025 01:35:16 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184e2f5c531bc52d63020dfb5cd44800780636aca7503a3adc510611f503d18c`  
		Last Modified: Wed, 08 Jan 2025 02:35:14 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; s390x

```console
$ docker pull hitch@sha256:d91204d37425e40a174c327556e101e756d3baae8af570d95d555175f76557b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31230843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae76908cceba307dde76e2e850f030d7571830f0b04f29b209232c4300010224`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e973ddf7be7a3ef6ce409e675b83570f4141ba68727c4e5c2f375f48cc2bc67b`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 1.6 MB (1566950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e660d42d0e4abfddbd5150c5fe8d04d19a455b3f0e9087d918b43b3324de5921`  
		Last Modified: Tue, 07 Jan 2025 22:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:03077a449c74e88e0f899654f6a39799feba8a345a61c14977d87473d71d3cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83d9dbc2df4829224947aa1ed659ad6749d36e63643e1abdfe15a0bf852fa77`

```dockerfile
```

-	Layers:
	-	`sha256:c77e4f53cec64a928050cca209f5b7c0d729347e768f45f7364466661e048246`  
		Last Modified: Mon, 06 Jan 2025 19:40:16 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be908d7cfac6586649e4fd45008a52ba458489d3ff11fa452c4ec31abe0fd571`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 13.4 KB (13416 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8.0`

```console
$ docker pull hitch@sha256:8c070b2a392f25bfad6d5cf14b9e2fcd55db64fe05dc4c3632e98868fc338a08
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

### `hitch:1.8.0` - linux; amd64

```console
$ docker pull hitch@sha256:170cb108ee0dec44db046d4685551d5469862116ee2d222a3235f5056fa98be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31822904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f18deec619649e3999f0109a33d9f7d0514fa62f8bc7e629094a6949d57234`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d697a9ce5ab19b9e590473f743020081818fded42de57d42446e09c1ccf447`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 1.6 MB (1569795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f22c0f52ce30d1feec9ef6cce4c8f1d4525d5b1bfbb1cdb600ba5407c43500`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:4cd630e3f0e93e3770c8c0b91905f1acc2d8ab3fb30fc7586ce67d1f21aa0a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde0e57dd1c436cb292c7e1b46fe067d519a01d6e8945fe5de1aa54710d1eb5e`

```dockerfile
```

-	Layers:
	-	`sha256:8c60b76b391c7d7435d38b5faf2e51709cc59a516615649109d32ec23ac5eb01`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 2.7 MB (2690039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6696743f11f896220bc08bfcf29c7b43c206a6b2059322e12f2287bb2546cd07`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 13.6 KB (13625 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; arm variant v7

```console
$ docker pull hitch@sha256:0260faf6fc69190aab99b6880b7a09081762e31cd03c05107ec235702ea6f216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27022812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b028fa35fa3823ef019358a5d084fd842d83760f97b650db456472edfd7867a`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 20:45:43 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102431f6c85283678f018254635d8782d4ec57602cb0a684abc7458256406386`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 1.5 MB (1488408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4211154205e3c97642b3e68ba25d5f7f65623991c18b894059e8484a7dff232`  
		Last Modified: Tue, 14 Jan 2025 02:30:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:7915d6149d2416d1ed6107762d3846fd76c499a3fbcff58b014f768e558ea0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68804bf4bdca32a370bf9ed91a77827ea89991894fb20cadb793ee0f5da5cedb`

```dockerfile
```

-	Layers:
	-	`sha256:b1067f86bff6417689ee6fbb2f2768f18cd6c2ab7432bfcfd75a410913b05a09`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 2.7 MB (2692271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0b05802d226a9e24c8255c7d27a594f7919b3ceb99d495fc20b83731564014`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:b811507727ecec372a9842f21582ba11af1d744b74869e38e066475321f8af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30293284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4fdd24687e87d7d4a8271935e9094fd0af663f411966593e6c2e794bcf78cd`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a105e2bd89d8e97d81b5e9c50f97f1b0c2ea0fb95365baac64e7bb5d36bc55`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 1.5 MB (1547927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71c0f34fe225a75564e0979cc855423929ff86424670867390b9a1d4b956332`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:c924cf5c1b928970576752ecfa7b1b659ead3c3fb6b3de2af3aa8a23325ff905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2704044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c9bf8f77f312f835653c50230b722b2aac4f19e34ca7e860dfcf1de45c2e98`

```dockerfile
```

-	Layers:
	-	`sha256:954836a96a27e969580d7342dd1832250ad76b338250e21a692c37e1fe62085b`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 2.7 MB (2690303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1698a1fd8c7e744260f0fe3130388144c949ee8910c74509ec8733dcaa3701`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 13.7 KB (13741 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; 386

```console
$ docker pull hitch@sha256:5d65e9e0d32fbc7c5f1c139b9d2fa4b493d5bcf8bf356a76bf63925b75a507bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32753151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ad119c82ecf08dd836cf0d57766bbfd86ba5e7386e2a3b2c6647b22779f203`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885092d66c59fcbcff189c382da0c768de4449566489990f9343e351411a010c`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 1.6 MB (1573678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a4d221afd6c23791cee85d0d0f82248f11b7979931730a121f8e8a616663b`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:9c5fb417a207405ec17682e9b30de75091edf6468f017ac6502dbb497ef59e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6d52a1649d690009203b92d55de5d9c88b15aedc62281284e3dca9ec36f59`

```dockerfile
```

-	Layers:
	-	`sha256:a8f036d4b6818c352709fac107366aaa567c67d49303ad985115088660471b83`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 2.7 MB (2687163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f98003860bbbf9d8fb0465c220780c4f2f8835b5d94b5745d865fedaa64ad6`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 13.6 KB (13588 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; ppc64le

```console
$ docker pull hitch@sha256:1bdcd7bcd169b8de699dae282ed9132427b99bb8f3bfbac1cacbc2ce1d5b104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36928037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96c4164756efbaae82116b7b72bb2095a5138cae636ec7e0a585c93ee52057`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Tue, 07 Jan 2025 02:35:40 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96d996552b8211abcb134c637a2ff1f40f8948acc4fc03da156fc00d2cb2dd`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 1.6 MB (1628321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36644e74cb980ba714eec6ecf5729391a63781a34991264fc61069a239d5db`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:930b2a56783983d94990c5d8eb69841e1848a966f490e074c6f503c302919ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d1a71ab384aeac4980491883bcacb6682bb7ac79f99b75bdbef94246966341`

```dockerfile
```

-	Layers:
	-	`sha256:e83fceb4779f1817190640cf46aed07d46fd4b4cc148eb334f5dfafb1e675232`  
		Last Modified: Tue, 07 Jan 2025 01:35:16 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184e2f5c531bc52d63020dfb5cd44800780636aca7503a3adc510611f503d18c`  
		Last Modified: Wed, 08 Jan 2025 02:35:14 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; s390x

```console
$ docker pull hitch@sha256:d91204d37425e40a174c327556e101e756d3baae8af570d95d555175f76557b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31230843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae76908cceba307dde76e2e850f030d7571830f0b04f29b209232c4300010224`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e973ddf7be7a3ef6ce409e675b83570f4141ba68727c4e5c2f375f48cc2bc67b`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 1.6 MB (1566950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e660d42d0e4abfddbd5150c5fe8d04d19a455b3f0e9087d918b43b3324de5921`  
		Last Modified: Tue, 07 Jan 2025 22:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:03077a449c74e88e0f899654f6a39799feba8a345a61c14977d87473d71d3cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83d9dbc2df4829224947aa1ed659ad6749d36e63643e1abdfe15a0bf852fa77`

```dockerfile
```

-	Layers:
	-	`sha256:c77e4f53cec64a928050cca209f5b7c0d729347e768f45f7364466661e048246`  
		Last Modified: Mon, 06 Jan 2025 19:40:16 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be908d7cfac6586649e4fd45008a52ba458489d3ff11fa452c4ec31abe0fd571`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 13.4 KB (13416 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8.0-1`

```console
$ docker pull hitch@sha256:8c070b2a392f25bfad6d5cf14b9e2fcd55db64fe05dc4c3632e98868fc338a08
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

### `hitch:1.8.0-1` - linux; amd64

```console
$ docker pull hitch@sha256:170cb108ee0dec44db046d4685551d5469862116ee2d222a3235f5056fa98be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31822904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f18deec619649e3999f0109a33d9f7d0514fa62f8bc7e629094a6949d57234`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d697a9ce5ab19b9e590473f743020081818fded42de57d42446e09c1ccf447`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 1.6 MB (1569795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f22c0f52ce30d1feec9ef6cce4c8f1d4525d5b1bfbb1cdb600ba5407c43500`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:4cd630e3f0e93e3770c8c0b91905f1acc2d8ab3fb30fc7586ce67d1f21aa0a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde0e57dd1c436cb292c7e1b46fe067d519a01d6e8945fe5de1aa54710d1eb5e`

```dockerfile
```

-	Layers:
	-	`sha256:8c60b76b391c7d7435d38b5faf2e51709cc59a516615649109d32ec23ac5eb01`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 2.7 MB (2690039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6696743f11f896220bc08bfcf29c7b43c206a6b2059322e12f2287bb2546cd07`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 13.6 KB (13625 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:0260faf6fc69190aab99b6880b7a09081762e31cd03c05107ec235702ea6f216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27022812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b028fa35fa3823ef019358a5d084fd842d83760f97b650db456472edfd7867a`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 20:45:43 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102431f6c85283678f018254635d8782d4ec57602cb0a684abc7458256406386`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 1.5 MB (1488408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4211154205e3c97642b3e68ba25d5f7f65623991c18b894059e8484a7dff232`  
		Last Modified: Tue, 14 Jan 2025 02:30:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:7915d6149d2416d1ed6107762d3846fd76c499a3fbcff58b014f768e558ea0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68804bf4bdca32a370bf9ed91a77827ea89991894fb20cadb793ee0f5da5cedb`

```dockerfile
```

-	Layers:
	-	`sha256:b1067f86bff6417689ee6fbb2f2768f18cd6c2ab7432bfcfd75a410913b05a09`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 2.7 MB (2692271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0b05802d226a9e24c8255c7d27a594f7919b3ceb99d495fc20b83731564014`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:b811507727ecec372a9842f21582ba11af1d744b74869e38e066475321f8af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30293284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4fdd24687e87d7d4a8271935e9094fd0af663f411966593e6c2e794bcf78cd`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a105e2bd89d8e97d81b5e9c50f97f1b0c2ea0fb95365baac64e7bb5d36bc55`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 1.5 MB (1547927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71c0f34fe225a75564e0979cc855423929ff86424670867390b9a1d4b956332`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:c924cf5c1b928970576752ecfa7b1b659ead3c3fb6b3de2af3aa8a23325ff905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2704044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c9bf8f77f312f835653c50230b722b2aac4f19e34ca7e860dfcf1de45c2e98`

```dockerfile
```

-	Layers:
	-	`sha256:954836a96a27e969580d7342dd1832250ad76b338250e21a692c37e1fe62085b`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 2.7 MB (2690303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1698a1fd8c7e744260f0fe3130388144c949ee8910c74509ec8733dcaa3701`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 13.7 KB (13741 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; 386

```console
$ docker pull hitch@sha256:5d65e9e0d32fbc7c5f1c139b9d2fa4b493d5bcf8bf356a76bf63925b75a507bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32753151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ad119c82ecf08dd836cf0d57766bbfd86ba5e7386e2a3b2c6647b22779f203`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885092d66c59fcbcff189c382da0c768de4449566489990f9343e351411a010c`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 1.6 MB (1573678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a4d221afd6c23791cee85d0d0f82248f11b7979931730a121f8e8a616663b`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:9c5fb417a207405ec17682e9b30de75091edf6468f017ac6502dbb497ef59e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6d52a1649d690009203b92d55de5d9c88b15aedc62281284e3dca9ec36f59`

```dockerfile
```

-	Layers:
	-	`sha256:a8f036d4b6818c352709fac107366aaa567c67d49303ad985115088660471b83`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 2.7 MB (2687163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f98003860bbbf9d8fb0465c220780c4f2f8835b5d94b5745d865fedaa64ad6`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 13.6 KB (13588 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:1bdcd7bcd169b8de699dae282ed9132427b99bb8f3bfbac1cacbc2ce1d5b104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36928037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96c4164756efbaae82116b7b72bb2095a5138cae636ec7e0a585c93ee52057`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Tue, 07 Jan 2025 02:35:40 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96d996552b8211abcb134c637a2ff1f40f8948acc4fc03da156fc00d2cb2dd`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 1.6 MB (1628321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36644e74cb980ba714eec6ecf5729391a63781a34991264fc61069a239d5db`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:930b2a56783983d94990c5d8eb69841e1848a966f490e074c6f503c302919ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d1a71ab384aeac4980491883bcacb6682bb7ac79f99b75bdbef94246966341`

```dockerfile
```

-	Layers:
	-	`sha256:e83fceb4779f1817190640cf46aed07d46fd4b4cc148eb334f5dfafb1e675232`  
		Last Modified: Tue, 07 Jan 2025 01:35:16 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184e2f5c531bc52d63020dfb5cd44800780636aca7503a3adc510611f503d18c`  
		Last Modified: Wed, 08 Jan 2025 02:35:14 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; s390x

```console
$ docker pull hitch@sha256:d91204d37425e40a174c327556e101e756d3baae8af570d95d555175f76557b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31230843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae76908cceba307dde76e2e850f030d7571830f0b04f29b209232c4300010224`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e973ddf7be7a3ef6ce409e675b83570f4141ba68727c4e5c2f375f48cc2bc67b`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 1.6 MB (1566950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e660d42d0e4abfddbd5150c5fe8d04d19a455b3f0e9087d918b43b3324de5921`  
		Last Modified: Tue, 07 Jan 2025 22:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:03077a449c74e88e0f899654f6a39799feba8a345a61c14977d87473d71d3cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83d9dbc2df4829224947aa1ed659ad6749d36e63643e1abdfe15a0bf852fa77`

```dockerfile
```

-	Layers:
	-	`sha256:c77e4f53cec64a928050cca209f5b7c0d729347e768f45f7364466661e048246`  
		Last Modified: Mon, 06 Jan 2025 19:40:16 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be908d7cfac6586649e4fd45008a52ba458489d3ff11fa452c4ec31abe0fd571`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 13.4 KB (13416 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:latest`

```console
$ docker pull hitch@sha256:8c070b2a392f25bfad6d5cf14b9e2fcd55db64fe05dc4c3632e98868fc338a08
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

### `hitch:latest` - linux; amd64

```console
$ docker pull hitch@sha256:170cb108ee0dec44db046d4685551d5469862116ee2d222a3235f5056fa98be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31822904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f18deec619649e3999f0109a33d9f7d0514fa62f8bc7e629094a6949d57234`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d697a9ce5ab19b9e590473f743020081818fded42de57d42446e09c1ccf447`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 1.6 MB (1569795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f22c0f52ce30d1feec9ef6cce4c8f1d4525d5b1bfbb1cdb600ba5407c43500`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:4cd630e3f0e93e3770c8c0b91905f1acc2d8ab3fb30fc7586ce67d1f21aa0a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde0e57dd1c436cb292c7e1b46fe067d519a01d6e8945fe5de1aa54710d1eb5e`

```dockerfile
```

-	Layers:
	-	`sha256:8c60b76b391c7d7435d38b5faf2e51709cc59a516615649109d32ec23ac5eb01`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 2.7 MB (2690039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6696743f11f896220bc08bfcf29c7b43c206a6b2059322e12f2287bb2546cd07`  
		Last Modified: Tue, 14 Jan 2025 02:19:08 GMT  
		Size: 13.6 KB (13625 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:0260faf6fc69190aab99b6880b7a09081762e31cd03c05107ec235702ea6f216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27022812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b028fa35fa3823ef019358a5d084fd842d83760f97b650db456472edfd7867a`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 20:45:43 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102431f6c85283678f018254635d8782d4ec57602cb0a684abc7458256406386`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 1.5 MB (1488408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4211154205e3c97642b3e68ba25d5f7f65623991c18b894059e8484a7dff232`  
		Last Modified: Tue, 14 Jan 2025 02:30:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:7915d6149d2416d1ed6107762d3846fd76c499a3fbcff58b014f768e558ea0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68804bf4bdca32a370bf9ed91a77827ea89991894fb20cadb793ee0f5da5cedb`

```dockerfile
```

-	Layers:
	-	`sha256:b1067f86bff6417689ee6fbb2f2768f18cd6c2ab7432bfcfd75a410913b05a09`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 2.7 MB (2692271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0b05802d226a9e24c8255c7d27a594f7919b3ceb99d495fc20b83731564014`  
		Last Modified: Tue, 14 Jan 2025 02:30:50 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:b811507727ecec372a9842f21582ba11af1d744b74869e38e066475321f8af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30293284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4fdd24687e87d7d4a8271935e9094fd0af663f411966593e6c2e794bcf78cd`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a105e2bd89d8e97d81b5e9c50f97f1b0c2ea0fb95365baac64e7bb5d36bc55`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 1.5 MB (1547927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71c0f34fe225a75564e0979cc855423929ff86424670867390b9a1d4b956332`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:c924cf5c1b928970576752ecfa7b1b659ead3c3fb6b3de2af3aa8a23325ff905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2704044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c9bf8f77f312f835653c50230b722b2aac4f19e34ca7e860dfcf1de45c2e98`

```dockerfile
```

-	Layers:
	-	`sha256:954836a96a27e969580d7342dd1832250ad76b338250e21a692c37e1fe62085b`  
		Last Modified: Tue, 14 Jan 2025 02:57:35 GMT  
		Size: 2.7 MB (2690303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1698a1fd8c7e744260f0fe3130388144c949ee8910c74509ec8733dcaa3701`  
		Last Modified: Tue, 14 Jan 2025 02:57:34 GMT  
		Size: 13.7 KB (13741 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:5d65e9e0d32fbc7c5f1c139b9d2fa4b493d5bcf8bf356a76bf63925b75a507bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32753151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ad119c82ecf08dd836cf0d57766bbfd86ba5e7386e2a3b2c6647b22779f203`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885092d66c59fcbcff189c382da0c768de4449566489990f9343e351411a010c`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 1.6 MB (1573678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a4d221afd6c23791cee85d0d0f82248f11b7979931730a121f8e8a616663b`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:9c5fb417a207405ec17682e9b30de75091edf6468f017ac6502dbb497ef59e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6d52a1649d690009203b92d55de5d9c88b15aedc62281284e3dca9ec36f59`

```dockerfile
```

-	Layers:
	-	`sha256:a8f036d4b6818c352709fac107366aaa567c67d49303ad985115088660471b83`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 2.7 MB (2687163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f98003860bbbf9d8fb0465c220780c4f2f8835b5d94b5745d865fedaa64ad6`  
		Last Modified: Tue, 14 Jan 2025 02:17:19 GMT  
		Size: 13.6 KB (13588 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:1bdcd7bcd169b8de699dae282ed9132427b99bb8f3bfbac1cacbc2ce1d5b104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36928037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96c4164756efbaae82116b7b72bb2095a5138cae636ec7e0a585c93ee52057`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Tue, 07 Jan 2025 02:35:40 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96d996552b8211abcb134c637a2ff1f40f8948acc4fc03da156fc00d2cb2dd`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 1.6 MB (1628321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36644e74cb980ba714eec6ecf5729391a63781a34991264fc61069a239d5db`  
		Last Modified: Thu, 05 Sep 2024 00:26:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:930b2a56783983d94990c5d8eb69841e1848a966f490e074c6f503c302919ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d1a71ab384aeac4980491883bcacb6682bb7ac79f99b75bdbef94246966341`

```dockerfile
```

-	Layers:
	-	`sha256:e83fceb4779f1817190640cf46aed07d46fd4b4cc148eb334f5dfafb1e675232`  
		Last Modified: Tue, 07 Jan 2025 01:35:16 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184e2f5c531bc52d63020dfb5cd44800780636aca7503a3adc510611f503d18c`  
		Last Modified: Wed, 08 Jan 2025 02:35:14 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:d91204d37425e40a174c327556e101e756d3baae8af570d95d555175f76557b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31230843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae76908cceba307dde76e2e850f030d7571830f0b04f29b209232c4300010224`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e973ddf7be7a3ef6ce409e675b83570f4141ba68727c4e5c2f375f48cc2bc67b`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 1.6 MB (1566950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e660d42d0e4abfddbd5150c5fe8d04d19a455b3f0e9087d918b43b3324de5921`  
		Last Modified: Tue, 07 Jan 2025 22:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:03077a449c74e88e0f899654f6a39799feba8a345a61c14977d87473d71d3cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83d9dbc2df4829224947aa1ed659ad6749d36e63643e1abdfe15a0bf852fa77`

```dockerfile
```

-	Layers:
	-	`sha256:c77e4f53cec64a928050cca209f5b7c0d729347e768f45f7364466661e048246`  
		Last Modified: Mon, 06 Jan 2025 19:40:16 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be908d7cfac6586649e4fd45008a52ba458489d3ff11fa452c4ec31abe0fd571`  
		Last Modified: Thu, 05 Sep 2024 02:41:23 GMT  
		Size: 13.4 KB (13416 bytes)  
		MIME: application/vnd.in-toto+json
