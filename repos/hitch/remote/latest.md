## `hitch:latest`

```console
$ docker pull hitch@sha256:202b5632dfad15f793e5c970a1c4dbf09cb2be0e8b9c6d8e688dc4bf884ee050
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
$ docker pull hitch@sha256:61397d68be34a701ffddcdef9e94b459c026155fc394b0f445e6382d506b317e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32998507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccc8815e53920c63991b50b61d743b2859b5b79973757d04f929760cb4b4cc9`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7547589e6e7f8761f26e4c5d20305a1a79a63c4dcdd868d4cffd88437b58e8`  
		Last Modified: Tue, 13 Aug 2024 01:19:20 GMT  
		Size: 1.6 MB (1569775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8d028f1e9c8da20af797dff0ababb94343b26ca4dc74000d4d54672523414`  
		Last Modified: Tue, 13 Aug 2024 01:19:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:74f0dc0f7f01c07638309c1b70136c20a12f220ded2650f32ab917f2e895c7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6fe35172482e6c8a50169563472a0dd3557f88e3ade6d9eed87979e691dd94`

```dockerfile
```

-	Layers:
	-	`sha256:897a0e81a70f92f744b8a5db0421b5c6b8cf6966543c724505cec6420424d5f3`  
		Last Modified: Tue, 13 Aug 2024 01:19:20 GMT  
		Size: 2.7 MB (2680963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10d43083f71ec9c463ec304f64deface6b019f9cade8e94ee1715255196b4f4c`  
		Last Modified: Tue, 13 Aug 2024 01:19:20 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:981d450a3e81145a9b2130fe1c7dbe443a2eea38ab972e756aa3e3716b045355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28078165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144090bd5c4246795c40b8cc1e0997123d807d4c873a1d59fac30cdaa7de3049`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c2aa502d43acbcb5595150f593e1a0efb15cd856419d09c0f1be5d981dfff`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 1.5 MB (1488591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127634bebf3abf5444ea33fab4571e990ec450543485d0d886835048376ccdb`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:004b4069765b12a0d2adc95d51b9d45410849c9af6aa810484b4b78f0756e0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eba83e05d9e2558a232d07ae49fe26c9a5018af842a460f55c137cc669f470`

```dockerfile
```

-	Layers:
	-	`sha256:5e91e859c9b01c135d7d5cceda113f8caa92c170592ce436e56f4cbd8d2cf581`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 2.7 MB (2683194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c8f004fa7967294a167804dc0cac2fecfefa353171e717b765ae145610d0ec`  
		Last Modified: Tue, 23 Jul 2024 17:53:38 GMT  
		Size: 13.5 KB (13497 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:3a985ee2d35811197464beeb2a68a8cd9835876e5fd053cf14d73ff758447244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31624449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8604f44a8499a0718aa8190f8a465441ee35c5cb28d3ad58449a267fb63a324`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455070218babcfdd6e868c45c5efc29179126ffa6cebaa8dfab811e8b2bbb22e`  
		Last Modified: Tue, 13 Aug 2024 07:18:52 GMT  
		Size: 1.5 MB (1547918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16891a43dd999e10d4724ede06cad05a60e62f6e6fa9a2dd8e157ca8486d3375`  
		Last Modified: Tue, 13 Aug 2024 07:18:52 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:5f9f5db93985878f66ae7e9e86eb5f0d908e99e66575aeb61776dcd258dcf229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a09f66e27684b72fbe5d69f196686f3dd3f881b4ecec88d818a253a9976bef0`

```dockerfile
```

-	Layers:
	-	`sha256:272fab3727fb6173df4d9f4bf2b37f24780d00d4fdcdce269479c4b341afa47f`  
		Last Modified: Tue, 13 Aug 2024 07:18:52 GMT  
		Size: 2.7 MB (2681226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459fb8d3a814818de517017949d0839509ff44742f2239f74b9cfbea14f9ab01`  
		Last Modified: Tue, 13 Aug 2024 07:18:52 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:8d87414944014d426348c46e0ebe60a1c34425576255add15916f0702dbc6eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33987918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fee8b0e31c06740d3e74aa05e21274c53f583dd155d0813d9d5d8bf47f73cde`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
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
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28610147358fdc30a297f81f09fa40c8e0803a5810d124b82d1e4f9849d40f54`  
		Last Modified: Tue, 13 Aug 2024 01:19:41 GMT  
		Size: 1.6 MB (1573691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa75d8a06e5db66073d76843703fb1ff59b5a3810c6c00bb2ffca7f35bc0456`  
		Last Modified: Tue, 13 Aug 2024 01:19:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:1e786fbb6395552efe77171f936dc18f141e831b21cd18136dfe3312c226d7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8fa6120a178e46248a9716743ce8f181bd708f591a1bedd16be2b043d9f475`

```dockerfile
```

-	Layers:
	-	`sha256:059a8006ec6c7d5ac2b6f1ccc49b8fee007ea50641779cc70e1633925eefffb7`  
		Last Modified: Tue, 13 Aug 2024 01:19:41 GMT  
		Size: 2.7 MB (2678086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb033b635104d25b7f9803d0f47c92d1eb03094dd07bc59602fa17edce86851`  
		Last Modified: Tue, 13 Aug 2024 01:19:41 GMT  
		Size: 13.4 KB (13385 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:570852ed1ea2e1c86bd1dc65d9dbdd13f41308c1c108a8b418aead868361660e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36933969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e767f501a7ed21627da21eb882d62e29c66076fc34d16194a9259455e06b86cd`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
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
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d19dc72d4f14713c57c01983020a05abdc2a0d55997174b091a68988d3a6403`  
		Last Modified: Tue, 13 Aug 2024 06:44:01 GMT  
		Size: 1.6 MB (1628391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3515b8b53e2e952f5787afcbe703a2e5914d5e5d2813b848b63239d10ed4cd0e`  
		Last Modified: Tue, 13 Aug 2024 06:44:01 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:34c82578f52899d5d4d494ea52ee160566cd54951dacb907a6d4b63ed59e0917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bb50457371186a8d2904fa04fa5c885ce29ebe804f78172b3649fd3f69e8d8`

```dockerfile
```

-	Layers:
	-	`sha256:78e5dd7482c45f1929d6cb61f097cf39fe80523e1056e78656ed3846383793cb`  
		Last Modified: Tue, 13 Aug 2024 06:44:01 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b254ee1119c6269e2417613bbff8f5ffff04fee8edf56bbd376c8f9cedcd66f6`  
		Last Modified: Tue, 13 Aug 2024 06:44:01 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:836177b790ec2c6a2083f728f7a48b2698a47539bf20db95ebad0bc1097639c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31236359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2c58190a22589bad4f212fce9e4d4a9bff15db5498112f7bc54448fbd7444c`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
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
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9184947932277c891963dc85412f837f3994e307e43f2e09175be46e919751`  
		Last Modified: Tue, 13 Aug 2024 05:21:52 GMT  
		Size: 1.6 MB (1566951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881899f919fdbe1140666ee902f81ffbf1e6954e737aba8f3d2be2ec9403ae4b`  
		Last Modified: Tue, 13 Aug 2024 05:21:52 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:88b77eeb5f3fb3a6e27f2618fac2acb57aebf460b95332002191afb3e9c8942c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d56f0eee29dcac004a3c3a92ee789db6b38adc0bf22e95e8008c2c482db8232`

```dockerfile
```

-	Layers:
	-	`sha256:d3b96a4927a53622154f31cfaaa2749cebfaf5003b0ffb0be97b2ccf174e89ce`  
		Last Modified: Tue, 13 Aug 2024 05:21:52 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c2a20a0b26632e61fb0e3afe9c462b41affe34bbc66d17b4a57a2e38995795`  
		Last Modified: Tue, 13 Aug 2024 05:21:52 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json
