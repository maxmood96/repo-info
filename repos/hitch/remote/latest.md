## `hitch:latest`

```console
$ docker pull hitch@sha256:2145db8fde41bee17f10423fdbcb6ce287fcf2fecedc73ab2bd15234cb0294fa
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
$ docker pull hitch@sha256:4641ebc78c6e2cfda600e630680d37567d7f0cd0d5b065c37ac344baf49807e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31827652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c8133af5cc4b28d2753ab34cc5b448edf2be1c64109db2e174c52b486938ee`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4021cd9418de8a73ab57feb7653a40d8be811392d0178436978388526ed9388a`  
		Last Modified: Tue, 10 Jun 2025 23:28:53 GMT  
		Size: 1.6 MB (1571142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01eefab8fcae8243e6528f68797133db069d3227e3a3f10d5ba7396cd22211b`  
		Last Modified: Tue, 10 Jun 2025 23:28:52 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:facca8f59133694c42effc52200b7a8b8075eb93338657711f31d8c32fcd2cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2826294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5db98bf9e111428174a84b14f7bd689a121bd87819e7c2605ddf2c05d36eab3`

```dockerfile
```

-	Layers:
	-	`sha256:25d5b8f045cd5f1ce3409b445c062855af940522e928ef5b087d286592404daa`  
		Last Modified: Wed, 11 Jun 2025 00:46:26 GMT  
		Size: 2.8 MB (2812669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64d2e27723887a662690c9c5dcfc7d4226d1e521429af689678c79a2aeab189`  
		Last Modified: Wed, 11 Jun 2025 00:46:27 GMT  
		Size: 13.6 KB (13625 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:efd8111147d5afd3e6b98cd7264effd043c07a4f92be71c6184c9a0b8addad35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27034730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862878eb560f2cec0cddbfb883c33ec3d0b68d205262983ec12d27931549a0c3`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
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
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41b7a36f7c966db559a14cf926028de1ff457012ce5595650cb4f60bf38666f`  
		Last Modified: Tue, 10 Jun 2025 23:45:29 GMT  
		Size: 1.5 MB (1490092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e856c5ff666840b230f0988422ac5a096ac1f8f4df589dd2792ff3fbe3ee721`  
		Last Modified: Tue, 10 Jun 2025 23:45:39 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:926269f078f243616ce706bb1288051fca1004d53fc4640bd95f2a31b7ef19cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2828610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c38d7a901976bac8731adbd23294b451c20d4a5eb3eed12e313b13a5fe659f`

```dockerfile
```

-	Layers:
	-	`sha256:746786ec31bce610bb1f997763b597f899d5c9a428560ffbd55fa710401f74a5`  
		Last Modified: Wed, 11 Jun 2025 00:46:32 GMT  
		Size: 2.8 MB (2814901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:266aa054c1a34f2a59721352747532261fb59a003f22d8908792eb3ba3476e78`  
		Last Modified: Wed, 11 Jun 2025 00:46:33 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:9b530a11c33eb2cb7ca188244b76a136302cbf8f83cc335d5eceaba8e73680b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30294094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff796184fb6370d4f20efe9924e6d9e98b513f70e42183f766931b9942f101b`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d946764ba3416c9f51bf5ad08ee743f181d8561833aaa4ef8f416df71b5afc9`  
		Last Modified: Wed, 11 Jun 2025 00:06:54 GMT  
		Size: 1.5 MB (1549466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b74f6c7062a675e3cf6a94ec08d4e40115bf3bd55304bd47726611a9e69a29`  
		Last Modified: Wed, 11 Jun 2025 00:06:55 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:8d66f0e36cb4e4014610763095371c0e34b4b6a153366747121391c228fe40da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2826674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9354e211c4a19c64d5a72d3a64b20344cfa5423c8e3aa4c6499ba445b63d7cb`

```dockerfile
```

-	Layers:
	-	`sha256:3d93096c24fa2defa9cb66fc535b18ddcf4aa51df505e31d3475d561ad54a99f`  
		Last Modified: Wed, 11 Jun 2025 03:46:28 GMT  
		Size: 2.8 MB (2812933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1491d08599e41a375f0d5f1ac74f5d155eccea2eeaa341d2a98cbb0153a8107`  
		Last Modified: Wed, 11 Jun 2025 03:46:28 GMT  
		Size: 13.7 KB (13741 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:f8e34c9bd6b02815a8018acd31550cc8dcb8fb9f906114c5a77e5b33f7cf0090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32765286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356d5939c5f40bcc2a01cad4c101f5365278bede71eaec5c0208fb3b810af6f8`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6d610e5d7a1fb6858e90b58a83df05456e34ecda2d0420d84e61401444b4f9`  
		Last Modified: Tue, 10 Jun 2025 23:59:14 GMT  
		Size: 1.6 MB (1575159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f91cd413a3b31f526008aa82a2778323bf0445ab8713c29ee47525617daa920`  
		Last Modified: Tue, 10 Jun 2025 23:59:29 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:5f87efcc4b1c1701e31c70d0693700c3e44302cb06ac8cdd7eec46e273548887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fd84952a477560b824dc64396830736c2bef411c1320bc5bd8a18794b78959`

```dockerfile
```

-	Layers:
	-	`sha256:fd9b5d93b78f181ee6424b0551fa63e331b2efed51faf200979e4ba200f9a329`  
		Last Modified: Wed, 11 Jun 2025 00:46:44 GMT  
		Size: 2.8 MB (2809841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0edc6eeab6d385f414b524240d9cee96d9fb52473603512dfead6950998e1f7`  
		Last Modified: Wed, 11 Jun 2025 00:46:44 GMT  
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
		Last Modified: Tue, 07 Jan 2025 20:35:45 GMT  
		Size: 1.6 MB (1628321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36644e74cb980ba714eec6ecf5729391a63781a34991264fc61069a239d5db`  
		Last Modified: Mon, 06 Jan 2025 17:36:34 GMT  
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
		Last Modified: Sun, 15 Dec 2024 19:17:08 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e973ddf7be7a3ef6ce409e675b83570f4141ba68727c4e5c2f375f48cc2bc67b`  
		Last Modified: Tue, 07 Jan 2025 05:35:08 GMT  
		Size: 1.6 MB (1566950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Tue, 07 Jan 2025 03:35:24 GMT  
		Size: 13.4 KB (13416 bytes)  
		MIME: application/vnd.in-toto+json
