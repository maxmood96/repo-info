<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.18`](#varnish6018)
-	[`varnish:6.0.18-1`](#varnish6018-1)
-	[`varnish:8`](#varnish8)
-	[`varnish:8-alpine`](#varnish8-alpine)
-	[`varnish:8.0`](#varnish80)
-	[`varnish:8.0-alpine`](#varnish80-alpine)
-	[`varnish:8.0.2`](#varnish802)
-	[`varnish:8.0.2-1`](#varnish802-1)
-	[`varnish:8.0.2-alpine`](#varnish802-alpine)
-	[`varnish:9`](#varnish9)
-	[`varnish:9.0`](#varnish90)
-	[`varnish:9.0.3`](#varnish903)
-	[`varnish:9.0.3-1`](#varnish903-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:57d9f4ddc7d67bba82f6ac513bf8bd69ef07b15cfbbbb90110ff5c3782de2650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:9c0a40c3343f4f4634383a3a335390969b7390f5b4ad3b31917790fadc552dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121888240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64235d09f62f50a6d6a5708ed7e8067f8c45cd25c276996b0d63ae98d71402c5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:37:45 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:37:45 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:37:45 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:37:45 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:37:45 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:37:45 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:37:45 GMT
CMD []
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d4f18ac7aee82a961d1f287e6e04f8dc12803c4351dc53983d8dd054a1932`  
		Last Modified: Thu, 11 Jun 2026 00:37:59 GMT  
		Size: 93.6 MB (93649861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa8ae3048b527035b3e9af144792078211efdb13e49d3d5f9642746b48a246`  
		Last Modified: Thu, 11 Jun 2026 00:37:56 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6` - unknown; unknown

```console
$ docker pull varnish@sha256:da005506c27f72517aa4d1aa3246202087c1432ea2f13cfe5e185e9c8699fb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2899e2a48bc7022f51a1441fd4ebc715d4047c0c6c38d621b0bbec79e18b3eba`

```dockerfile
```

-	Layers:
	-	`sha256:2bbb355a7636f159c91fabcd337f6d16099fa7f11c1395f635f7ebdc02298a91`  
		Last Modified: Thu, 11 Jun 2026 00:37:57 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4cf407a0b4de0dda624608043e7d74ce81fbdd051acdf9de6b79ba593b26fd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116326149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ebcdb927a69fbf1853049a7fbe2e4301882d340b7c9d8bdc5fd1bb34aeb43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:39:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:13 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:39:13 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:14 GMT
CMD []
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4419eaa106fe57d8d5adbc7d7983edd918d32ff26041570322a7a931b3635c`  
		Last Modified: Thu, 11 Jun 2026 00:39:27 GMT  
		Size: 88.2 MB (88203088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68005bccf244228d37e3d43c9161ca4b9f29eb5db4c0f4f71b3b985fd841f9`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6` - unknown; unknown

```console
$ docker pull varnish@sha256:819d0d67cbdd131dfd47a2f183ea913eaabdd9407a3de29a9e527abf02b87d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3de7bac09419b6702d928102aeadb664112167022f4da1d8e1edfab6e421`

```dockerfile
```

-	Layers:
	-	`sha256:593bb87127d0183b172dc2d6c5cff0894f4e1afe314368c6c22a783275c8a91d`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0`

```console
$ docker pull varnish@sha256:57d9f4ddc7d67bba82f6ac513bf8bd69ef07b15cfbbbb90110ff5c3782de2650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:9c0a40c3343f4f4634383a3a335390969b7390f5b4ad3b31917790fadc552dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121888240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64235d09f62f50a6d6a5708ed7e8067f8c45cd25c276996b0d63ae98d71402c5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:37:45 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:37:45 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:37:45 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:37:45 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:37:45 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:37:45 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:37:45 GMT
CMD []
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d4f18ac7aee82a961d1f287e6e04f8dc12803c4351dc53983d8dd054a1932`  
		Last Modified: Thu, 11 Jun 2026 00:37:59 GMT  
		Size: 93.6 MB (93649861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa8ae3048b527035b3e9af144792078211efdb13e49d3d5f9642746b48a246`  
		Last Modified: Thu, 11 Jun 2026 00:37:56 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:da005506c27f72517aa4d1aa3246202087c1432ea2f13cfe5e185e9c8699fb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2899e2a48bc7022f51a1441fd4ebc715d4047c0c6c38d621b0bbec79e18b3eba`

```dockerfile
```

-	Layers:
	-	`sha256:2bbb355a7636f159c91fabcd337f6d16099fa7f11c1395f635f7ebdc02298a91`  
		Last Modified: Thu, 11 Jun 2026 00:37:57 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4cf407a0b4de0dda624608043e7d74ce81fbdd051acdf9de6b79ba593b26fd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116326149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ebcdb927a69fbf1853049a7fbe2e4301882d340b7c9d8bdc5fd1bb34aeb43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:39:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:13 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:39:13 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:14 GMT
CMD []
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4419eaa106fe57d8d5adbc7d7983edd918d32ff26041570322a7a931b3635c`  
		Last Modified: Thu, 11 Jun 2026 00:39:27 GMT  
		Size: 88.2 MB (88203088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68005bccf244228d37e3d43c9161ca4b9f29eb5db4c0f4f71b3b985fd841f9`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:819d0d67cbdd131dfd47a2f183ea913eaabdd9407a3de29a9e527abf02b87d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3de7bac09419b6702d928102aeadb664112167022f4da1d8e1edfab6e421`

```dockerfile
```

-	Layers:
	-	`sha256:593bb87127d0183b172dc2d6c5cff0894f4e1afe314368c6c22a783275c8a91d`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.18`

```console
$ docker pull varnish@sha256:57d9f4ddc7d67bba82f6ac513bf8bd69ef07b15cfbbbb90110ff5c3782de2650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.18` - linux; amd64

```console
$ docker pull varnish@sha256:9c0a40c3343f4f4634383a3a335390969b7390f5b4ad3b31917790fadc552dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121888240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64235d09f62f50a6d6a5708ed7e8067f8c45cd25c276996b0d63ae98d71402c5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:37:45 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:37:45 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:37:45 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:37:45 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:37:45 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:37:45 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:37:45 GMT
CMD []
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d4f18ac7aee82a961d1f287e6e04f8dc12803c4351dc53983d8dd054a1932`  
		Last Modified: Thu, 11 Jun 2026 00:37:59 GMT  
		Size: 93.6 MB (93649861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa8ae3048b527035b3e9af144792078211efdb13e49d3d5f9642746b48a246`  
		Last Modified: Thu, 11 Jun 2026 00:37:56 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.18` - unknown; unknown

```console
$ docker pull varnish@sha256:da005506c27f72517aa4d1aa3246202087c1432ea2f13cfe5e185e9c8699fb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2899e2a48bc7022f51a1441fd4ebc715d4047c0c6c38d621b0bbec79e18b3eba`

```dockerfile
```

-	Layers:
	-	`sha256:2bbb355a7636f159c91fabcd337f6d16099fa7f11c1395f635f7ebdc02298a91`  
		Last Modified: Thu, 11 Jun 2026 00:37:57 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.18` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4cf407a0b4de0dda624608043e7d74ce81fbdd051acdf9de6b79ba593b26fd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116326149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ebcdb927a69fbf1853049a7fbe2e4301882d340b7c9d8bdc5fd1bb34aeb43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:39:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:13 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:39:13 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:14 GMT
CMD []
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4419eaa106fe57d8d5adbc7d7983edd918d32ff26041570322a7a931b3635c`  
		Last Modified: Thu, 11 Jun 2026 00:39:27 GMT  
		Size: 88.2 MB (88203088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68005bccf244228d37e3d43c9161ca4b9f29eb5db4c0f4f71b3b985fd841f9`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.18` - unknown; unknown

```console
$ docker pull varnish@sha256:819d0d67cbdd131dfd47a2f183ea913eaabdd9407a3de29a9e527abf02b87d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3de7bac09419b6702d928102aeadb664112167022f4da1d8e1edfab6e421`

```dockerfile
```

-	Layers:
	-	`sha256:593bb87127d0183b172dc2d6c5cff0894f4e1afe314368c6c22a783275c8a91d`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.18-1`

```console
$ docker pull varnish@sha256:57d9f4ddc7d67bba82f6ac513bf8bd69ef07b15cfbbbb90110ff5c3782de2650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.18-1` - linux; amd64

```console
$ docker pull varnish@sha256:9c0a40c3343f4f4634383a3a335390969b7390f5b4ad3b31917790fadc552dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121888240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64235d09f62f50a6d6a5708ed7e8067f8c45cd25c276996b0d63ae98d71402c5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:37:45 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:37:45 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:37:45 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:37:45 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:37:45 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:37:45 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:37:45 GMT
CMD []
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d4f18ac7aee82a961d1f287e6e04f8dc12803c4351dc53983d8dd054a1932`  
		Last Modified: Thu, 11 Jun 2026 00:37:59 GMT  
		Size: 93.6 MB (93649861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa8ae3048b527035b3e9af144792078211efdb13e49d3d5f9642746b48a246`  
		Last Modified: Thu, 11 Jun 2026 00:37:56 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.18-1` - unknown; unknown

```console
$ docker pull varnish@sha256:da005506c27f72517aa4d1aa3246202087c1432ea2f13cfe5e185e9c8699fb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2899e2a48bc7022f51a1441fd4ebc715d4047c0c6c38d621b0bbec79e18b3eba`

```dockerfile
```

-	Layers:
	-	`sha256:2bbb355a7636f159c91fabcd337f6d16099fa7f11c1395f635f7ebdc02298a91`  
		Last Modified: Thu, 11 Jun 2026 00:37:57 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.18-1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4cf407a0b4de0dda624608043e7d74ce81fbdd051acdf9de6b79ba593b26fd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116326149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ebcdb927a69fbf1853049a7fbe2e4301882d340b7c9d8bdc5fd1bb34aeb43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:39:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:13 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:39:13 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:14 GMT
CMD []
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4419eaa106fe57d8d5adbc7d7983edd918d32ff26041570322a7a931b3635c`  
		Last Modified: Thu, 11 Jun 2026 00:39:27 GMT  
		Size: 88.2 MB (88203088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68005bccf244228d37e3d43c9161ca4b9f29eb5db4c0f4f71b3b985fd841f9`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.18-1` - unknown; unknown

```console
$ docker pull varnish@sha256:819d0d67cbdd131dfd47a2f183ea913eaabdd9407a3de29a9e527abf02b87d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3de7bac09419b6702d928102aeadb664112167022f4da1d8e1edfab6e421`

```dockerfile
```

-	Layers:
	-	`sha256:593bb87127d0183b172dc2d6c5cff0894f4e1afe314368c6c22a783275c8a91d`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:93ca8d2761bcd808aa149ede62ffb69fb9deee33702c3a985ed1bebf99fb9e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:b760a4d9e7deb6fb6928e857937ec45d7bd809462d9f3aafca2f47749808926d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120267305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a6f3777a38215bdd67ebc3ca379916aa07042af7550877a8311149e999868`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:38:14 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:14 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:14 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:14 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9a79c67eef4921db9588a7fa2053bd00d1fb99c4adffe16774b5b3d988ddd`  
		Last Modified: Thu, 11 Jun 2026 00:38:28 GMT  
		Size: 90.5 MB (90478782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c7abe729a644a60ebbfc9fd8234038e402b912ba71beae591d1aae0ed9ca1`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34403bab4b524d1a81bbacb80bc88c649c8a27df3d8fe7fd801f7b194b3eae7`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:38fc5afa7f13b3801c2c1a9c9cc04e739ac9e9fb1ed297af5fd882db38051c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb94d4bf7670d0bfa9278211d47183e5de9e07f03f2a351d1f8680856ccd774`

```dockerfile
```

-	Layers:
	-	`sha256:8ed30f1a836dbc9e4875ccf97fe3505d98ef18f3ecb1a6777910d23926af85ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 20.9 KB (20869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:37af1a0ef9eef90e018ea1ce3bdcc0bc765e28f07573b8f5f96b572864a449fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12b12aa1a8aeb7f0dc002335617be3daea6c39c30ec344bc9bd9fe01696d6f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:59 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:40:00 GMT
USER varnish
# Thu, 11 Jun 2026 00:40:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:40:00 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58db64060edffb977091268464a3f40da9f797a6da82caa2426803a4022e10b`  
		Last Modified: Thu, 11 Jun 2026 00:40:13 GMT  
		Size: 84.1 MB (84105671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf2133883e29ca2682f4c36d0a73cc7d4b4c746cb2bf320dadc331389c58d3`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61016503c5f7c6c73f7fb3dc32e7cb0c599639a95b9aa6701f82f269df06409`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6289e570503f41585a8a5cc6c38c730e1db5fe15f722f4075bf7554db5c19`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:ddc0f89310b2142564a864822b963ea1fb5ec76b670893c8a7958690672c32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d94cf5d59545de715ace5a02ac511a5ac631c66f7d6aa3ec176e758ea3cc25`

```dockerfile
```

-	Layers:
	-	`sha256:c62198045bd7091b79cad1277652d338bbad606f7baaefa91e4f429f3248f71a`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8-alpine`

```console
$ docker pull varnish@sha256:edd2efd296a8bdb021841e8498a7cb61ded8bd5f3cb22ab542001a61cc750083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:1e7ed3f804951e43ed90c300bfabb5715b26a4514d119fe6d8dd43f82394adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93035109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ea455493f4db66379e0f72bf70d9dded0fe1a84a6bc380c4a82f34325b7033`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:32 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:32 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:32 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:32 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:32 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:32 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:32 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:32 GMT
USER varnish
# Tue, 19 May 2026 16:51:32 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:32 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa485f15e897ed487ab343775f0ea4566f20ba9243dcf5e15d4be21c08e6631c`  
		Last Modified: Tue, 19 May 2026 16:51:46 GMT  
		Size: 89.2 MB (89167782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c9ee5c0f2ebc1aad93f89a4dfdf9d107fbae8bf00481a2decd2b78dbd1b2ad`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764fb603eb97ca18bc3b3c5ce407185d508a9671713605475c17d0d82a9323c`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e33232128fff25b6f01216c25ef9c69bc8ce41595b5ce57c613ef8321656a4`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:735b7f36f046328b55da201d60d548ee8362d91a4608b510b40c5c96c89bf4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d526de6586584e4a30351366b98a4360d074bc0f5f0c6642950aebfef0b761cd`

```dockerfile
```

-	Layers:
	-	`sha256:b40482caa22d698478f14b36e184f6f877cf75b72863e34c55b1075fcda74714`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 20.5 KB (20498 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:22dcaac69b93b44cc9f776b336847b241613aad120ada8630428acb97281e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84789676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f8b8675e0517fef28d057db82c312babdf17a2636bd43f2d2807a7f1c58945`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:24 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:24 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:24 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:24 GMT
USER varnish
# Tue, 19 May 2026 16:51:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866c4e9b6bce00e744f1b2a14cdce2e24376dd037eae4280770a37130134`  
		Last Modified: Tue, 19 May 2026 16:51:37 GMT  
		Size: 80.6 MB (80586666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49261e403353c66e660d668215eb89e5a5bd2c2667bb602a221c18eed513eb81`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b81b6ea6f91c21f310bd64d939b83e6a6afe6dfbbb6d2cb5675d5a8be1d2f8c`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981e2b7b44dd078d913c48139d9ba5e706b8ceae5d8c3810c4aa4a5c52fc88cd`  
		Last Modified: Tue, 19 May 2026 16:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4d820622217a8c5b08288f1e7f930bfd19cdd837a826628f419e111ac6f60971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2687331b117a35a869ac374c42ee5ffb2b98e39603c846eee668d7aa47f82ec`

```dockerfile
```

-	Layers:
	-	`sha256:cb5d188d7096c63fc9b8d2d3f404a5d4b2c1987915b922a2457e4945debb20bf`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 20.6 KB (20602 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0`

```console
$ docker pull varnish@sha256:93ca8d2761bcd808aa149ede62ffb69fb9deee33702c3a985ed1bebf99fb9e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:b760a4d9e7deb6fb6928e857937ec45d7bd809462d9f3aafca2f47749808926d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120267305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a6f3777a38215bdd67ebc3ca379916aa07042af7550877a8311149e999868`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:38:14 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:14 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:14 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:14 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9a79c67eef4921db9588a7fa2053bd00d1fb99c4adffe16774b5b3d988ddd`  
		Last Modified: Thu, 11 Jun 2026 00:38:28 GMT  
		Size: 90.5 MB (90478782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c7abe729a644a60ebbfc9fd8234038e402b912ba71beae591d1aae0ed9ca1`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34403bab4b524d1a81bbacb80bc88c649c8a27df3d8fe7fd801f7b194b3eae7`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:38fc5afa7f13b3801c2c1a9c9cc04e739ac9e9fb1ed297af5fd882db38051c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb94d4bf7670d0bfa9278211d47183e5de9e07f03f2a351d1f8680856ccd774`

```dockerfile
```

-	Layers:
	-	`sha256:8ed30f1a836dbc9e4875ccf97fe3505d98ef18f3ecb1a6777910d23926af85ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 20.9 KB (20869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:37af1a0ef9eef90e018ea1ce3bdcc0bc765e28f07573b8f5f96b572864a449fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12b12aa1a8aeb7f0dc002335617be3daea6c39c30ec344bc9bd9fe01696d6f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:59 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:40:00 GMT
USER varnish
# Thu, 11 Jun 2026 00:40:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:40:00 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58db64060edffb977091268464a3f40da9f797a6da82caa2426803a4022e10b`  
		Last Modified: Thu, 11 Jun 2026 00:40:13 GMT  
		Size: 84.1 MB (84105671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf2133883e29ca2682f4c36d0a73cc7d4b4c746cb2bf320dadc331389c58d3`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61016503c5f7c6c73f7fb3dc32e7cb0c599639a95b9aa6701f82f269df06409`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6289e570503f41585a8a5cc6c38c730e1db5fe15f722f4075bf7554db5c19`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:ddc0f89310b2142564a864822b963ea1fb5ec76b670893c8a7958690672c32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d94cf5d59545de715ace5a02ac511a5ac631c66f7d6aa3ec176e758ea3cc25`

```dockerfile
```

-	Layers:
	-	`sha256:c62198045bd7091b79cad1277652d338bbad606f7baaefa91e4f429f3248f71a`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0-alpine`

```console
$ docker pull varnish@sha256:edd2efd296a8bdb021841e8498a7cb61ded8bd5f3cb22ab542001a61cc750083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:1e7ed3f804951e43ed90c300bfabb5715b26a4514d119fe6d8dd43f82394adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93035109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ea455493f4db66379e0f72bf70d9dded0fe1a84a6bc380c4a82f34325b7033`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:32 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:32 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:32 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:32 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:32 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:32 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:32 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:32 GMT
USER varnish
# Tue, 19 May 2026 16:51:32 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:32 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa485f15e897ed487ab343775f0ea4566f20ba9243dcf5e15d4be21c08e6631c`  
		Last Modified: Tue, 19 May 2026 16:51:46 GMT  
		Size: 89.2 MB (89167782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c9ee5c0f2ebc1aad93f89a4dfdf9d107fbae8bf00481a2decd2b78dbd1b2ad`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764fb603eb97ca18bc3b3c5ce407185d508a9671713605475c17d0d82a9323c`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e33232128fff25b6f01216c25ef9c69bc8ce41595b5ce57c613ef8321656a4`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:735b7f36f046328b55da201d60d548ee8362d91a4608b510b40c5c96c89bf4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d526de6586584e4a30351366b98a4360d074bc0f5f0c6642950aebfef0b761cd`

```dockerfile
```

-	Layers:
	-	`sha256:b40482caa22d698478f14b36e184f6f877cf75b72863e34c55b1075fcda74714`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 20.5 KB (20498 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:22dcaac69b93b44cc9f776b336847b241613aad120ada8630428acb97281e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84789676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f8b8675e0517fef28d057db82c312babdf17a2636bd43f2d2807a7f1c58945`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:24 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:24 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:24 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:24 GMT
USER varnish
# Tue, 19 May 2026 16:51:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866c4e9b6bce00e744f1b2a14cdce2e24376dd037eae4280770a37130134`  
		Last Modified: Tue, 19 May 2026 16:51:37 GMT  
		Size: 80.6 MB (80586666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49261e403353c66e660d668215eb89e5a5bd2c2667bb602a221c18eed513eb81`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b81b6ea6f91c21f310bd64d939b83e6a6afe6dfbbb6d2cb5675d5a8be1d2f8c`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981e2b7b44dd078d913c48139d9ba5e706b8ceae5d8c3810c4aa4a5c52fc88cd`  
		Last Modified: Tue, 19 May 2026 16:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4d820622217a8c5b08288f1e7f930bfd19cdd837a826628f419e111ac6f60971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2687331b117a35a869ac374c42ee5ffb2b98e39603c846eee668d7aa47f82ec`

```dockerfile
```

-	Layers:
	-	`sha256:cb5d188d7096c63fc9b8d2d3f404a5d4b2c1987915b922a2457e4945debb20bf`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 20.6 KB (20602 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.2`

```console
$ docker pull varnish@sha256:93ca8d2761bcd808aa149ede62ffb69fb9deee33702c3a985ed1bebf99fb9e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.2` - linux; amd64

```console
$ docker pull varnish@sha256:b760a4d9e7deb6fb6928e857937ec45d7bd809462d9f3aafca2f47749808926d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120267305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a6f3777a38215bdd67ebc3ca379916aa07042af7550877a8311149e999868`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:38:14 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:14 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:14 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:14 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9a79c67eef4921db9588a7fa2053bd00d1fb99c4adffe16774b5b3d988ddd`  
		Last Modified: Thu, 11 Jun 2026 00:38:28 GMT  
		Size: 90.5 MB (90478782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c7abe729a644a60ebbfc9fd8234038e402b912ba71beae591d1aae0ed9ca1`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34403bab4b524d1a81bbacb80bc88c649c8a27df3d8fe7fd801f7b194b3eae7`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2` - unknown; unknown

```console
$ docker pull varnish@sha256:38fc5afa7f13b3801c2c1a9c9cc04e739ac9e9fb1ed297af5fd882db38051c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb94d4bf7670d0bfa9278211d47183e5de9e07f03f2a351d1f8680856ccd774`

```dockerfile
```

-	Layers:
	-	`sha256:8ed30f1a836dbc9e4875ccf97fe3505d98ef18f3ecb1a6777910d23926af85ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 20.9 KB (20869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.2` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:37af1a0ef9eef90e018ea1ce3bdcc0bc765e28f07573b8f5f96b572864a449fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12b12aa1a8aeb7f0dc002335617be3daea6c39c30ec344bc9bd9fe01696d6f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:59 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:40:00 GMT
USER varnish
# Thu, 11 Jun 2026 00:40:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:40:00 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58db64060edffb977091268464a3f40da9f797a6da82caa2426803a4022e10b`  
		Last Modified: Thu, 11 Jun 2026 00:40:13 GMT  
		Size: 84.1 MB (84105671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf2133883e29ca2682f4c36d0a73cc7d4b4c746cb2bf320dadc331389c58d3`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61016503c5f7c6c73f7fb3dc32e7cb0c599639a95b9aa6701f82f269df06409`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6289e570503f41585a8a5cc6c38c730e1db5fe15f722f4075bf7554db5c19`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2` - unknown; unknown

```console
$ docker pull varnish@sha256:ddc0f89310b2142564a864822b963ea1fb5ec76b670893c8a7958690672c32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d94cf5d59545de715ace5a02ac511a5ac631c66f7d6aa3ec176e758ea3cc25`

```dockerfile
```

-	Layers:
	-	`sha256:c62198045bd7091b79cad1277652d338bbad606f7baaefa91e4f429f3248f71a`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.2-1`

```console
$ docker pull varnish@sha256:93ca8d2761bcd808aa149ede62ffb69fb9deee33702c3a985ed1bebf99fb9e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.2-1` - linux; amd64

```console
$ docker pull varnish@sha256:b760a4d9e7deb6fb6928e857937ec45d7bd809462d9f3aafca2f47749808926d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120267305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a6f3777a38215bdd67ebc3ca379916aa07042af7550877a8311149e999868`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:38:14 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:14 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:14 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:14 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9a79c67eef4921db9588a7fa2053bd00d1fb99c4adffe16774b5b3d988ddd`  
		Last Modified: Thu, 11 Jun 2026 00:38:28 GMT  
		Size: 90.5 MB (90478782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c7abe729a644a60ebbfc9fd8234038e402b912ba71beae591d1aae0ed9ca1`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34403bab4b524d1a81bbacb80bc88c649c8a27df3d8fe7fd801f7b194b3eae7`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2-1` - unknown; unknown

```console
$ docker pull varnish@sha256:38fc5afa7f13b3801c2c1a9c9cc04e739ac9e9fb1ed297af5fd882db38051c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb94d4bf7670d0bfa9278211d47183e5de9e07f03f2a351d1f8680856ccd774`

```dockerfile
```

-	Layers:
	-	`sha256:8ed30f1a836dbc9e4875ccf97fe3505d98ef18f3ecb1a6777910d23926af85ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 20.9 KB (20869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.2-1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:37af1a0ef9eef90e018ea1ce3bdcc0bc765e28f07573b8f5f96b572864a449fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12b12aa1a8aeb7f0dc002335617be3daea6c39c30ec344bc9bd9fe01696d6f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:59 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:40:00 GMT
USER varnish
# Thu, 11 Jun 2026 00:40:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:40:00 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58db64060edffb977091268464a3f40da9f797a6da82caa2426803a4022e10b`  
		Last Modified: Thu, 11 Jun 2026 00:40:13 GMT  
		Size: 84.1 MB (84105671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf2133883e29ca2682f4c36d0a73cc7d4b4c746cb2bf320dadc331389c58d3`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61016503c5f7c6c73f7fb3dc32e7cb0c599639a95b9aa6701f82f269df06409`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6289e570503f41585a8a5cc6c38c730e1db5fe15f722f4075bf7554db5c19`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2-1` - unknown; unknown

```console
$ docker pull varnish@sha256:ddc0f89310b2142564a864822b963ea1fb5ec76b670893c8a7958690672c32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d94cf5d59545de715ace5a02ac511a5ac631c66f7d6aa3ec176e758ea3cc25`

```dockerfile
```

-	Layers:
	-	`sha256:c62198045bd7091b79cad1277652d338bbad606f7baaefa91e4f429f3248f71a`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.2-alpine`

```console
$ docker pull varnish@sha256:edd2efd296a8bdb021841e8498a7cb61ded8bd5f3cb22ab542001a61cc750083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.2-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:1e7ed3f804951e43ed90c300bfabb5715b26a4514d119fe6d8dd43f82394adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93035109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ea455493f4db66379e0f72bf70d9dded0fe1a84a6bc380c4a82f34325b7033`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:32 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:32 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:32 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:32 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:32 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:32 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:32 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:32 GMT
USER varnish
# Tue, 19 May 2026 16:51:32 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:32 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa485f15e897ed487ab343775f0ea4566f20ba9243dcf5e15d4be21c08e6631c`  
		Last Modified: Tue, 19 May 2026 16:51:46 GMT  
		Size: 89.2 MB (89167782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c9ee5c0f2ebc1aad93f89a4dfdf9d107fbae8bf00481a2decd2b78dbd1b2ad`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764fb603eb97ca18bc3b3c5ce407185d508a9671713605475c17d0d82a9323c`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e33232128fff25b6f01216c25ef9c69bc8ce41595b5ce57c613ef8321656a4`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:735b7f36f046328b55da201d60d548ee8362d91a4608b510b40c5c96c89bf4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d526de6586584e4a30351366b98a4360d074bc0f5f0c6642950aebfef0b761cd`

```dockerfile
```

-	Layers:
	-	`sha256:b40482caa22d698478f14b36e184f6f877cf75b72863e34c55b1075fcda74714`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 20.5 KB (20498 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.2-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:22dcaac69b93b44cc9f776b336847b241613aad120ada8630428acb97281e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84789676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f8b8675e0517fef28d057db82c312babdf17a2636bd43f2d2807a7f1c58945`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:24 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:24 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:24 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:24 GMT
USER varnish
# Tue, 19 May 2026 16:51:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866c4e9b6bce00e744f1b2a14cdce2e24376dd037eae4280770a37130134`  
		Last Modified: Tue, 19 May 2026 16:51:37 GMT  
		Size: 80.6 MB (80586666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49261e403353c66e660d668215eb89e5a5bd2c2667bb602a221c18eed513eb81`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b81b6ea6f91c21f310bd64d939b83e6a6afe6dfbbb6d2cb5675d5a8be1d2f8c`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981e2b7b44dd078d913c48139d9ba5e706b8ceae5d8c3810c4aa4a5c52fc88cd`  
		Last Modified: Tue, 19 May 2026 16:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4d820622217a8c5b08288f1e7f930bfd19cdd837a826628f419e111ac6f60971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2687331b117a35a869ac374c42ee5ffb2b98e39603c846eee668d7aa47f82ec`

```dockerfile
```

-	Layers:
	-	`sha256:cb5d188d7096c63fc9b8d2d3f404a5d4b2c1987915b922a2457e4945debb20bf`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 20.6 KB (20602 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9`

```console
$ docker pull varnish@sha256:47c2533928bb366d10c103e1c6c59ae124c5467414ec4ffae8187023c9f8754f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9` - linux; amd64

```console
$ docker pull varnish@sha256:7db93cafd7d610c3a646166bf8ff782da7e4fd0155a175d7beec28c796d469d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122306737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018c0a4b9b0d09bfa9771e58671cf257365e4587904e35a7f076486249358552`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:20 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:38:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:21 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:21 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a865d59f8841c5a1d9d80075950b45c272cf62e8f901ff4160921e78ab4f73`  
		Last Modified: Thu, 11 Jun 2026 00:38:36 GMT  
		Size: 92.5 MB (92518443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831fc33df1d56db312b1487a4bf796c3e148498c81b590a5f3be0d90ae7366e`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1204b04b99fa509d60e655bc8617895484a0d388a85b3c66e84404bb94b03c`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:d7f0c43c6f6bab3b3a4d409b9a47f51271642f8b761bac09dafe8b020fc41707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3becc62806b06786537e9335bd276af7cd2104a709e7143ab95a4437f19c426e`

```dockerfile
```

-	Layers:
	-	`sha256:2e92fe34525e7f52759828a22dcdd035f1492fd3256da2a3a2f40e212f745d7f`  
		Last Modified: Thu, 11 Jun 2026 00:38:32 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a589610d5b32e735322bbadd15c29cb9062b5110266118a3f39910f9a3b07da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116321702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef1052d0ed67549c400bea69f3686c8b049da8e44efc4fc77717e2091f64054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:36 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:36 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:39:36 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:36 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:36 GMT
USER varnish
# Thu, 11 Jun 2026 00:39:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:36 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e4b05bd500ff7afbaa40582df7064877cf9fe8af9f8c1f82744accaacdd532`  
		Last Modified: Thu, 11 Jun 2026 00:39:51 GMT  
		Size: 86.2 MB (86170285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f20a288279f4963897c3f96b9cb05daa5b41696c89c9b39419d0e70df77e19`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f37bf631c2e4c0a7c3b539f8ff93d917d4cd6068b93a1d942280d8226f196d`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17bb1eb5604db57d98c8def78eb4b865c244e6bea974b296085b3f6baa9db4`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:5b49eb1ea4373235ccba05f6c3a6835b9c6b826b86583d1e17fc26e37406d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107661f9909f101418dfe88d0ea2315f34fed13013cf53c2207a0a9547b47f5a`

```dockerfile
```

-	Layers:
	-	`sha256:6c0397fb9fc76dc791b8c73d8cbb8dc50dba697b8f2fd12b3b193c2f6fd8fa6f`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 20.1 KB (20150 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0`

```console
$ docker pull varnish@sha256:47c2533928bb366d10c103e1c6c59ae124c5467414ec4ffae8187023c9f8754f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0` - linux; amd64

```console
$ docker pull varnish@sha256:7db93cafd7d610c3a646166bf8ff782da7e4fd0155a175d7beec28c796d469d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122306737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018c0a4b9b0d09bfa9771e58671cf257365e4587904e35a7f076486249358552`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:20 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:38:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:21 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:21 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a865d59f8841c5a1d9d80075950b45c272cf62e8f901ff4160921e78ab4f73`  
		Last Modified: Thu, 11 Jun 2026 00:38:36 GMT  
		Size: 92.5 MB (92518443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831fc33df1d56db312b1487a4bf796c3e148498c81b590a5f3be0d90ae7366e`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1204b04b99fa509d60e655bc8617895484a0d388a85b3c66e84404bb94b03c`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:d7f0c43c6f6bab3b3a4d409b9a47f51271642f8b761bac09dafe8b020fc41707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3becc62806b06786537e9335bd276af7cd2104a709e7143ab95a4437f19c426e`

```dockerfile
```

-	Layers:
	-	`sha256:2e92fe34525e7f52759828a22dcdd035f1492fd3256da2a3a2f40e212f745d7f`  
		Last Modified: Thu, 11 Jun 2026 00:38:32 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a589610d5b32e735322bbadd15c29cb9062b5110266118a3f39910f9a3b07da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116321702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef1052d0ed67549c400bea69f3686c8b049da8e44efc4fc77717e2091f64054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:36 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:36 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:39:36 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:36 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:36 GMT
USER varnish
# Thu, 11 Jun 2026 00:39:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:36 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e4b05bd500ff7afbaa40582df7064877cf9fe8af9f8c1f82744accaacdd532`  
		Last Modified: Thu, 11 Jun 2026 00:39:51 GMT  
		Size: 86.2 MB (86170285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f20a288279f4963897c3f96b9cb05daa5b41696c89c9b39419d0e70df77e19`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f37bf631c2e4c0a7c3b539f8ff93d917d4cd6068b93a1d942280d8226f196d`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17bb1eb5604db57d98c8def78eb4b865c244e6bea974b296085b3f6baa9db4`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:5b49eb1ea4373235ccba05f6c3a6835b9c6b826b86583d1e17fc26e37406d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107661f9909f101418dfe88d0ea2315f34fed13013cf53c2207a0a9547b47f5a`

```dockerfile
```

-	Layers:
	-	`sha256:6c0397fb9fc76dc791b8c73d8cbb8dc50dba697b8f2fd12b3b193c2f6fd8fa6f`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 20.1 KB (20150 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0.3`

```console
$ docker pull varnish@sha256:47c2533928bb366d10c103e1c6c59ae124c5467414ec4ffae8187023c9f8754f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0.3` - linux; amd64

```console
$ docker pull varnish@sha256:7db93cafd7d610c3a646166bf8ff782da7e4fd0155a175d7beec28c796d469d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122306737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018c0a4b9b0d09bfa9771e58671cf257365e4587904e35a7f076486249358552`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:20 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:38:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:21 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:21 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a865d59f8841c5a1d9d80075950b45c272cf62e8f901ff4160921e78ab4f73`  
		Last Modified: Thu, 11 Jun 2026 00:38:36 GMT  
		Size: 92.5 MB (92518443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831fc33df1d56db312b1487a4bf796c3e148498c81b590a5f3be0d90ae7366e`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1204b04b99fa509d60e655bc8617895484a0d388a85b3c66e84404bb94b03c`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.3` - unknown; unknown

```console
$ docker pull varnish@sha256:d7f0c43c6f6bab3b3a4d409b9a47f51271642f8b761bac09dafe8b020fc41707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3becc62806b06786537e9335bd276af7cd2104a709e7143ab95a4437f19c426e`

```dockerfile
```

-	Layers:
	-	`sha256:2e92fe34525e7f52759828a22dcdd035f1492fd3256da2a3a2f40e212f745d7f`  
		Last Modified: Thu, 11 Jun 2026 00:38:32 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a589610d5b32e735322bbadd15c29cb9062b5110266118a3f39910f9a3b07da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116321702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef1052d0ed67549c400bea69f3686c8b049da8e44efc4fc77717e2091f64054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:36 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:36 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:39:36 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:36 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:36 GMT
USER varnish
# Thu, 11 Jun 2026 00:39:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:36 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e4b05bd500ff7afbaa40582df7064877cf9fe8af9f8c1f82744accaacdd532`  
		Last Modified: Thu, 11 Jun 2026 00:39:51 GMT  
		Size: 86.2 MB (86170285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f20a288279f4963897c3f96b9cb05daa5b41696c89c9b39419d0e70df77e19`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f37bf631c2e4c0a7c3b539f8ff93d917d4cd6068b93a1d942280d8226f196d`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17bb1eb5604db57d98c8def78eb4b865c244e6bea974b296085b3f6baa9db4`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.3` - unknown; unknown

```console
$ docker pull varnish@sha256:5b49eb1ea4373235ccba05f6c3a6835b9c6b826b86583d1e17fc26e37406d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107661f9909f101418dfe88d0ea2315f34fed13013cf53c2207a0a9547b47f5a`

```dockerfile
```

-	Layers:
	-	`sha256:6c0397fb9fc76dc791b8c73d8cbb8dc50dba697b8f2fd12b3b193c2f6fd8fa6f`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 20.1 KB (20150 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0.3-1`

```console
$ docker pull varnish@sha256:47c2533928bb366d10c103e1c6c59ae124c5467414ec4ffae8187023c9f8754f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0.3-1` - linux; amd64

```console
$ docker pull varnish@sha256:7db93cafd7d610c3a646166bf8ff782da7e4fd0155a175d7beec28c796d469d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122306737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018c0a4b9b0d09bfa9771e58671cf257365e4587904e35a7f076486249358552`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:20 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:38:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:21 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:21 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a865d59f8841c5a1d9d80075950b45c272cf62e8f901ff4160921e78ab4f73`  
		Last Modified: Thu, 11 Jun 2026 00:38:36 GMT  
		Size: 92.5 MB (92518443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831fc33df1d56db312b1487a4bf796c3e148498c81b590a5f3be0d90ae7366e`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1204b04b99fa509d60e655bc8617895484a0d388a85b3c66e84404bb94b03c`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.3-1` - unknown; unknown

```console
$ docker pull varnish@sha256:d7f0c43c6f6bab3b3a4d409b9a47f51271642f8b761bac09dafe8b020fc41707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3becc62806b06786537e9335bd276af7cd2104a709e7143ab95a4437f19c426e`

```dockerfile
```

-	Layers:
	-	`sha256:2e92fe34525e7f52759828a22dcdd035f1492fd3256da2a3a2f40e212f745d7f`  
		Last Modified: Thu, 11 Jun 2026 00:38:32 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0.3-1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a589610d5b32e735322bbadd15c29cb9062b5110266118a3f39910f9a3b07da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116321702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef1052d0ed67549c400bea69f3686c8b049da8e44efc4fc77717e2091f64054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:36 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:36 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:39:36 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:36 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:36 GMT
USER varnish
# Thu, 11 Jun 2026 00:39:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:36 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e4b05bd500ff7afbaa40582df7064877cf9fe8af9f8c1f82744accaacdd532`  
		Last Modified: Thu, 11 Jun 2026 00:39:51 GMT  
		Size: 86.2 MB (86170285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f20a288279f4963897c3f96b9cb05daa5b41696c89c9b39419d0e70df77e19`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f37bf631c2e4c0a7c3b539f8ff93d917d4cd6068b93a1d942280d8226f196d`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17bb1eb5604db57d98c8def78eb4b865c244e6bea974b296085b3f6baa9db4`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.3-1` - unknown; unknown

```console
$ docker pull varnish@sha256:5b49eb1ea4373235ccba05f6c3a6835b9c6b826b86583d1e17fc26e37406d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107661f9909f101418dfe88d0ea2315f34fed13013cf53c2207a0a9547b47f5a`

```dockerfile
```

-	Layers:
	-	`sha256:6c0397fb9fc76dc791b8c73d8cbb8dc50dba697b8f2fd12b3b193c2f6fd8fa6f`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 20.1 KB (20150 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:47c2533928bb366d10c103e1c6c59ae124c5467414ec4ffae8187023c9f8754f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:7db93cafd7d610c3a646166bf8ff782da7e4fd0155a175d7beec28c796d469d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122306737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018c0a4b9b0d09bfa9771e58671cf257365e4587904e35a7f076486249358552`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:20 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:38:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:21 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:21 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a865d59f8841c5a1d9d80075950b45c272cf62e8f901ff4160921e78ab4f73`  
		Last Modified: Thu, 11 Jun 2026 00:38:36 GMT  
		Size: 92.5 MB (92518443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831fc33df1d56db312b1487a4bf796c3e148498c81b590a5f3be0d90ae7366e`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1204b04b99fa509d60e655bc8617895484a0d388a85b3c66e84404bb94b03c`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:d7f0c43c6f6bab3b3a4d409b9a47f51271642f8b761bac09dafe8b020fc41707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3becc62806b06786537e9335bd276af7cd2104a709e7143ab95a4437f19c426e`

```dockerfile
```

-	Layers:
	-	`sha256:2e92fe34525e7f52759828a22dcdd035f1492fd3256da2a3a2f40e212f745d7f`  
		Last Modified: Thu, 11 Jun 2026 00:38:32 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a589610d5b32e735322bbadd15c29cb9062b5110266118a3f39910f9a3b07da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116321702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef1052d0ed67549c400bea69f3686c8b049da8e44efc4fc77717e2091f64054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:36 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:36 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:39:36 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:36 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:36 GMT
USER varnish
# Thu, 11 Jun 2026 00:39:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:36 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e4b05bd500ff7afbaa40582df7064877cf9fe8af9f8c1f82744accaacdd532`  
		Last Modified: Thu, 11 Jun 2026 00:39:51 GMT  
		Size: 86.2 MB (86170285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f20a288279f4963897c3f96b9cb05daa5b41696c89c9b39419d0e70df77e19`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f37bf631c2e4c0a7c3b539f8ff93d917d4cd6068b93a1d942280d8226f196d`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17bb1eb5604db57d98c8def78eb4b865c244e6bea974b296085b3f6baa9db4`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:5b49eb1ea4373235ccba05f6c3a6835b9c6b826b86583d1e17fc26e37406d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107661f9909f101418dfe88d0ea2315f34fed13013cf53c2207a0a9547b47f5a`

```dockerfile
```

-	Layers:
	-	`sha256:6c0397fb9fc76dc791b8c73d8cbb8dc50dba697b8f2fd12b3b193c2f6fd8fa6f`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 20.1 KB (20150 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:47c2533928bb366d10c103e1c6c59ae124c5467414ec4ffae8187023c9f8754f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:7db93cafd7d610c3a646166bf8ff782da7e4fd0155a175d7beec28c796d469d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122306737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018c0a4b9b0d09bfa9771e58671cf257365e4587904e35a7f076486249358552`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:20 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:38:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:20 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:38:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:21 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:21 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a865d59f8841c5a1d9d80075950b45c272cf62e8f901ff4160921e78ab4f73`  
		Last Modified: Thu, 11 Jun 2026 00:38:36 GMT  
		Size: 92.5 MB (92518443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831fc33df1d56db312b1487a4bf796c3e148498c81b590a5f3be0d90ae7366e`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1204b04b99fa509d60e655bc8617895484a0d388a85b3c66e84404bb94b03c`  
		Last Modified: Thu, 11 Jun 2026 00:38:33 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:d7f0c43c6f6bab3b3a4d409b9a47f51271642f8b761bac09dafe8b020fc41707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3becc62806b06786537e9335bd276af7cd2104a709e7143ab95a4437f19c426e`

```dockerfile
```

-	Layers:
	-	`sha256:2e92fe34525e7f52759828a22dcdd035f1492fd3256da2a3a2f40e212f745d7f`  
		Last Modified: Thu, 11 Jun 2026 00:38:32 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a589610d5b32e735322bbadd15c29cb9062b5110266118a3f39910f9a3b07da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116321702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef1052d0ed67549c400bea69f3686c8b049da8e44efc4fc77717e2091f64054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:36 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:36 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Thu, 11 Jun 2026 00:39:36 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:36 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:36 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
COPY index.html /var/www/html/ # buildkit
# Thu, 11 Jun 2026 00:39:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:36 GMT
USER varnish
# Thu, 11 Jun 2026 00:39:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:36 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e4b05bd500ff7afbaa40582df7064877cf9fe8af9f8c1f82744accaacdd532`  
		Last Modified: Thu, 11 Jun 2026 00:39:51 GMT  
		Size: 86.2 MB (86170285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f20a288279f4963897c3f96b9cb05daa5b41696c89c9b39419d0e70df77e19`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f37bf631c2e4c0a7c3b539f8ff93d917d4cd6068b93a1d942280d8226f196d`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17bb1eb5604db57d98c8def78eb4b865c244e6bea974b296085b3f6baa9db4`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:5b49eb1ea4373235ccba05f6c3a6835b9c6b826b86583d1e17fc26e37406d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107661f9909f101418dfe88d0ea2315f34fed13013cf53c2207a0a9547b47f5a`

```dockerfile
```

-	Layers:
	-	`sha256:6c0397fb9fc76dc791b8c73d8cbb8dc50dba697b8f2fd12b3b193c2f6fd8fa6f`  
		Last Modified: Thu, 11 Jun 2026 00:39:48 GMT  
		Size: 20.1 KB (20150 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:93ca8d2761bcd808aa149ede62ffb69fb9deee33702c3a985ed1bebf99fb9e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:b760a4d9e7deb6fb6928e857937ec45d7bd809462d9f3aafca2f47749808926d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120267305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a6f3777a38215bdd67ebc3ca379916aa07042af7550877a8311149e999868`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:38:14 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:14 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:14 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:14 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9a79c67eef4921db9588a7fa2053bd00d1fb99c4adffe16774b5b3d988ddd`  
		Last Modified: Thu, 11 Jun 2026 00:38:28 GMT  
		Size: 90.5 MB (90478782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c7abe729a644a60ebbfc9fd8234038e402b912ba71beae591d1aae0ed9ca1`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34403bab4b524d1a81bbacb80bc88c649c8a27df3d8fe7fd801f7b194b3eae7`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:38fc5afa7f13b3801c2c1a9c9cc04e739ac9e9fb1ed297af5fd882db38051c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb94d4bf7670d0bfa9278211d47183e5de9e07f03f2a351d1f8680856ccd774`

```dockerfile
```

-	Layers:
	-	`sha256:8ed30f1a836dbc9e4875ccf97fe3505d98ef18f3ecb1a6777910d23926af85ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 20.9 KB (20869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:37af1a0ef9eef90e018ea1ce3bdcc0bc765e28f07573b8f5f96b572864a449fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12b12aa1a8aeb7f0dc002335617be3daea6c39c30ec344bc9bd9fe01696d6f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:59 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:40:00 GMT
USER varnish
# Thu, 11 Jun 2026 00:40:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:40:00 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58db64060edffb977091268464a3f40da9f797a6da82caa2426803a4022e10b`  
		Last Modified: Thu, 11 Jun 2026 00:40:13 GMT  
		Size: 84.1 MB (84105671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf2133883e29ca2682f4c36d0a73cc7d4b4c746cb2bf320dadc331389c58d3`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61016503c5f7c6c73f7fb3dc32e7cb0c599639a95b9aa6701f82f269df06409`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6289e570503f41585a8a5cc6c38c730e1db5fe15f722f4075bf7554db5c19`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:ddc0f89310b2142564a864822b963ea1fb5ec76b670893c8a7958690672c32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d94cf5d59545de715ace5a02ac511a5ac631c66f7d6aa3ec176e758ea3cc25`

```dockerfile
```

-	Layers:
	-	`sha256:c62198045bd7091b79cad1277652d338bbad606f7baaefa91e4f429f3248f71a`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:edd2efd296a8bdb021841e8498a7cb61ded8bd5f3cb22ab542001a61cc750083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:1e7ed3f804951e43ed90c300bfabb5715b26a4514d119fe6d8dd43f82394adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93035109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ea455493f4db66379e0f72bf70d9dded0fe1a84a6bc380c4a82f34325b7033`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:32 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:32 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:32 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:32 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:32 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:32 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:32 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:32 GMT
USER varnish
# Tue, 19 May 2026 16:51:32 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:32 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa485f15e897ed487ab343775f0ea4566f20ba9243dcf5e15d4be21c08e6631c`  
		Last Modified: Tue, 19 May 2026 16:51:46 GMT  
		Size: 89.2 MB (89167782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c9ee5c0f2ebc1aad93f89a4dfdf9d107fbae8bf00481a2decd2b78dbd1b2ad`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764fb603eb97ca18bc3b3c5ce407185d508a9671713605475c17d0d82a9323c`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e33232128fff25b6f01216c25ef9c69bc8ce41595b5ce57c613ef8321656a4`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:735b7f36f046328b55da201d60d548ee8362d91a4608b510b40c5c96c89bf4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d526de6586584e4a30351366b98a4360d074bc0f5f0c6642950aebfef0b761cd`

```dockerfile
```

-	Layers:
	-	`sha256:b40482caa22d698478f14b36e184f6f877cf75b72863e34c55b1075fcda74714`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 20.5 KB (20498 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:22dcaac69b93b44cc9f776b336847b241613aad120ada8630428acb97281e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84789676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f8b8675e0517fef28d057db82c312babdf17a2636bd43f2d2807a7f1c58945`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:24 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:24 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:24 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:24 GMT
USER varnish
# Tue, 19 May 2026 16:51:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866c4e9b6bce00e744f1b2a14cdce2e24376dd037eae4280770a37130134`  
		Last Modified: Tue, 19 May 2026 16:51:37 GMT  
		Size: 80.6 MB (80586666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49261e403353c66e660d668215eb89e5a5bd2c2667bb602a221c18eed513eb81`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b81b6ea6f91c21f310bd64d939b83e6a6afe6dfbbb6d2cb5675d5a8be1d2f8c`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981e2b7b44dd078d913c48139d9ba5e706b8ceae5d8c3810c4aa4a5c52fc88cd`  
		Last Modified: Tue, 19 May 2026 16:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4d820622217a8c5b08288f1e7f930bfd19cdd837a826628f419e111ac6f60971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2687331b117a35a869ac374c42ee5ffb2b98e39603c846eee668d7aa47f82ec`

```dockerfile
```

-	Layers:
	-	`sha256:cb5d188d7096c63fc9b8d2d3f404a5d4b2c1987915b922a2457e4945debb20bf`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 20.6 KB (20602 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:57d9f4ddc7d67bba82f6ac513bf8bd69ef07b15cfbbbb90110ff5c3782de2650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:9c0a40c3343f4f4634383a3a335390969b7390f5b4ad3b31917790fadc552dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121888240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64235d09f62f50a6d6a5708ed7e8067f8c45cd25c276996b0d63ae98d71402c5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:37:45 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:37:45 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:37:45 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:37:45 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:37:45 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:37:45 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:37:45 GMT
CMD []
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d4f18ac7aee82a961d1f287e6e04f8dc12803c4351dc53983d8dd054a1932`  
		Last Modified: Thu, 11 Jun 2026 00:37:59 GMT  
		Size: 93.6 MB (93649861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa8ae3048b527035b3e9af144792078211efdb13e49d3d5f9642746b48a246`  
		Last Modified: Thu, 11 Jun 2026 00:37:56 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:da005506c27f72517aa4d1aa3246202087c1432ea2f13cfe5e185e9c8699fb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2899e2a48bc7022f51a1441fd4ebc715d4047c0c6c38d621b0bbec79e18b3eba`

```dockerfile
```

-	Layers:
	-	`sha256:2bbb355a7636f159c91fabcd337f6d16099fa7f11c1395f635f7ebdc02298a91`  
		Last Modified: Thu, 11 Jun 2026 00:37:57 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4cf407a0b4de0dda624608043e7d74ce81fbdd051acdf9de6b79ba593b26fd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116326149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ebcdb927a69fbf1853049a7fbe2e4301882d340b7c9d8bdc5fd1bb34aeb43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:39:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:13 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Thu, 11 Jun 2026 00:39:13 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:39:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:39:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:39:14 GMT
CMD []
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4419eaa106fe57d8d5adbc7d7983edd918d32ff26041570322a7a931b3635c`  
		Last Modified: Thu, 11 Jun 2026 00:39:27 GMT  
		Size: 88.2 MB (88203088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68005bccf244228d37e3d43c9161ca4b9f29eb5db4c0f4f71b3b985fd841f9`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:819d0d67cbdd131dfd47a2f183ea913eaabdd9407a3de29a9e527abf02b87d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3de7bac09419b6702d928102aeadb664112167022f4da1d8e1edfab6e421`

```dockerfile
```

-	Layers:
	-	`sha256:593bb87127d0183b172dc2d6c5cff0894f4e1afe314368c6c22a783275c8a91d`  
		Last Modified: Thu, 11 Jun 2026 00:39:24 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json
