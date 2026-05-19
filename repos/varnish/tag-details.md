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
$ docker pull varnish@sha256:ce48281fde11b2161655f901b3abd5bc09e54c08435a2ee8f1ac63d83a170163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:c258b30827c01e76bea09685cb6c2f260072c41f5df9b4957089aaaeed91bda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127671811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dcfcdb7feeb73aa04b58834be7c4b1bd7ea55d509ef3faf333011d7f66682f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:50:54 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:54 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:50:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:54 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:55 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac07b99ec939068af4c3948829183d21610a6b8b8fc7e42d6884c397d2135cdb`  
		Last Modified: Tue, 19 May 2026 16:51:09 GMT  
		Size: 99.4 MB (99434772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f943a779e749a62ba476b583d2a62f8ed559187a6583d1d002f2db3e70142`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6` - unknown; unknown

```console
$ docker pull varnish@sha256:82c2557c61d3eee26a34d3d2c93b31e0f3a8761c459c9ea65f196b8836098146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4da491fcc85938fea8ad2f88e45c7b5b38089eef50c3c9a57ac8cd363fb5b`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2bf9dd7478422558585888b17ca921358ba94a81a35ce5a04f75e5f85f0cb`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:820ea3a1cdacd690993318312d666bf27c5379e45c490a373e8d7e27212220e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122100906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ae80baf0549534b56f99f8a537a1943a1b1a9dc8ae9ce1ed3a21020267f7bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:51:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:09 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:51:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:09 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659a62075f19812c24999d3860ca0e8cfbcf98d81aa7cfab5de0dcd4fa864c7c`  
		Last Modified: Tue, 19 May 2026 16:51:24 GMT  
		Size: 94.0 MB (93983984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0700d0a66165a5b584e5ad61550d3f0b515836fca5cff47f97f3d6648d61e03c`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6` - unknown; unknown

```console
$ docker pull varnish@sha256:ea873ff0c885dacb99f4e714c712765a13f9312b8ac5a7ec1e04221a89eb53fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90489d6680c7b1745deb18e8fe5d6a93324c00e0a68b886fba9640ae0ecc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:643c0366a8db61b07f7c83c6ff8a137f0449bd2ebe78564a01b8c48a26b3166d`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0`

```console
$ docker pull varnish@sha256:ce48281fde11b2161655f901b3abd5bc09e54c08435a2ee8f1ac63d83a170163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:c258b30827c01e76bea09685cb6c2f260072c41f5df9b4957089aaaeed91bda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127671811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dcfcdb7feeb73aa04b58834be7c4b1bd7ea55d509ef3faf333011d7f66682f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:50:54 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:54 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:50:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:54 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:55 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac07b99ec939068af4c3948829183d21610a6b8b8fc7e42d6884c397d2135cdb`  
		Last Modified: Tue, 19 May 2026 16:51:09 GMT  
		Size: 99.4 MB (99434772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f943a779e749a62ba476b583d2a62f8ed559187a6583d1d002f2db3e70142`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:82c2557c61d3eee26a34d3d2c93b31e0f3a8761c459c9ea65f196b8836098146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4da491fcc85938fea8ad2f88e45c7b5b38089eef50c3c9a57ac8cd363fb5b`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2bf9dd7478422558585888b17ca921358ba94a81a35ce5a04f75e5f85f0cb`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:820ea3a1cdacd690993318312d666bf27c5379e45c490a373e8d7e27212220e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122100906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ae80baf0549534b56f99f8a537a1943a1b1a9dc8ae9ce1ed3a21020267f7bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:51:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:09 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:51:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:09 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659a62075f19812c24999d3860ca0e8cfbcf98d81aa7cfab5de0dcd4fa864c7c`  
		Last Modified: Tue, 19 May 2026 16:51:24 GMT  
		Size: 94.0 MB (93983984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0700d0a66165a5b584e5ad61550d3f0b515836fca5cff47f97f3d6648d61e03c`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:ea873ff0c885dacb99f4e714c712765a13f9312b8ac5a7ec1e04221a89eb53fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90489d6680c7b1745deb18e8fe5d6a93324c00e0a68b886fba9640ae0ecc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:643c0366a8db61b07f7c83c6ff8a137f0449bd2ebe78564a01b8c48a26b3166d`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.18`

```console
$ docker pull varnish@sha256:ce48281fde11b2161655f901b3abd5bc09e54c08435a2ee8f1ac63d83a170163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.18` - linux; amd64

```console
$ docker pull varnish@sha256:c258b30827c01e76bea09685cb6c2f260072c41f5df9b4957089aaaeed91bda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127671811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dcfcdb7feeb73aa04b58834be7c4b1bd7ea55d509ef3faf333011d7f66682f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:50:54 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:54 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:50:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:54 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:55 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac07b99ec939068af4c3948829183d21610a6b8b8fc7e42d6884c397d2135cdb`  
		Last Modified: Tue, 19 May 2026 16:51:09 GMT  
		Size: 99.4 MB (99434772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f943a779e749a62ba476b583d2a62f8ed559187a6583d1d002f2db3e70142`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.18` - unknown; unknown

```console
$ docker pull varnish@sha256:82c2557c61d3eee26a34d3d2c93b31e0f3a8761c459c9ea65f196b8836098146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4da491fcc85938fea8ad2f88e45c7b5b38089eef50c3c9a57ac8cd363fb5b`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2bf9dd7478422558585888b17ca921358ba94a81a35ce5a04f75e5f85f0cb`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.18` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:820ea3a1cdacd690993318312d666bf27c5379e45c490a373e8d7e27212220e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122100906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ae80baf0549534b56f99f8a537a1943a1b1a9dc8ae9ce1ed3a21020267f7bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:51:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:09 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:51:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:09 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659a62075f19812c24999d3860ca0e8cfbcf98d81aa7cfab5de0dcd4fa864c7c`  
		Last Modified: Tue, 19 May 2026 16:51:24 GMT  
		Size: 94.0 MB (93983984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0700d0a66165a5b584e5ad61550d3f0b515836fca5cff47f97f3d6648d61e03c`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.18` - unknown; unknown

```console
$ docker pull varnish@sha256:ea873ff0c885dacb99f4e714c712765a13f9312b8ac5a7ec1e04221a89eb53fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90489d6680c7b1745deb18e8fe5d6a93324c00e0a68b886fba9640ae0ecc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:643c0366a8db61b07f7c83c6ff8a137f0449bd2ebe78564a01b8c48a26b3166d`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.18-1`

```console
$ docker pull varnish@sha256:ce48281fde11b2161655f901b3abd5bc09e54c08435a2ee8f1ac63d83a170163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.18-1` - linux; amd64

```console
$ docker pull varnish@sha256:c258b30827c01e76bea09685cb6c2f260072c41f5df9b4957089aaaeed91bda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127671811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dcfcdb7feeb73aa04b58834be7c4b1bd7ea55d509ef3faf333011d7f66682f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:50:54 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:54 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:50:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:54 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:55 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac07b99ec939068af4c3948829183d21610a6b8b8fc7e42d6884c397d2135cdb`  
		Last Modified: Tue, 19 May 2026 16:51:09 GMT  
		Size: 99.4 MB (99434772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f943a779e749a62ba476b583d2a62f8ed559187a6583d1d002f2db3e70142`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.18-1` - unknown; unknown

```console
$ docker pull varnish@sha256:82c2557c61d3eee26a34d3d2c93b31e0f3a8761c459c9ea65f196b8836098146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4da491fcc85938fea8ad2f88e45c7b5b38089eef50c3c9a57ac8cd363fb5b`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2bf9dd7478422558585888b17ca921358ba94a81a35ce5a04f75e5f85f0cb`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.18-1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:820ea3a1cdacd690993318312d666bf27c5379e45c490a373e8d7e27212220e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122100906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ae80baf0549534b56f99f8a537a1943a1b1a9dc8ae9ce1ed3a21020267f7bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:51:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:09 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:51:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:09 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659a62075f19812c24999d3860ca0e8cfbcf98d81aa7cfab5de0dcd4fa864c7c`  
		Last Modified: Tue, 19 May 2026 16:51:24 GMT  
		Size: 94.0 MB (93983984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0700d0a66165a5b584e5ad61550d3f0b515836fca5cff47f97f3d6648d61e03c`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.18-1` - unknown; unknown

```console
$ docker pull varnish@sha256:ea873ff0c885dacb99f4e714c712765a13f9312b8ac5a7ec1e04221a89eb53fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90489d6680c7b1745deb18e8fe5d6a93324c00e0a68b886fba9640ae0ecc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:643c0366a8db61b07f7c83c6ff8a137f0449bd2ebe78564a01b8c48a26b3166d`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:aa9310b89f73419dace2304336deb6052b89e943bce787b5b38df87ce88ed920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:968ab1f174d9860b2a46e6efc7b8a1abb901127dd722c6e1cf81d440653b9400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129144552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da79eb0a6d4a953801bc94482a81bcd11c8c4befcbd55fd6b1daf899755fa7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:16 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:16 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:16 GMT
USER varnish
# Tue, 19 May 2026 16:51:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:16 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612df49696e4e9e8458780549dacf4870f02dba8677aa8258b9328ea6e52c680`  
		Last Modified: Tue, 19 May 2026 16:51:31 GMT  
		Size: 99.4 MB (99361215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205533a727eaee849c2f585a1b32c58d2735609c66ffa059cd0012cc2b86e9a6`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e2454d9c45432fd3e02f3bb384890904ebd724c013bf2f1bce311adecce333`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9587f4dfb40fa5abc9679be2e6f16742950a56f4d968f27c8fc8ec2fc2ad0710`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:e8dcd113f2ad51ed3a6842c5458ad3cafb79db960c5b06f867232d22e6cb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c4205061f4240b54a9152f04575f483983dde6b1dd6bbfe49cd57a7a77517d`

```dockerfile
```

-	Layers:
	-	`sha256:3b0210cff421aab0bd55c06f34b7a91455e1d8dbd73dbb71fa849f76b816ae73`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 20.9 KB (20868 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:15bb3c3c9325d159898c1d095b8a2ca4ff2be1417f06c19b5218a522bad54c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a94db5a53bf3a03fd4bae5afd73f381af0c594900bca47f430c252e9b28c6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:08 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:08 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:08 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:08 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:08 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:08 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:08 GMT
USER varnish
# Tue, 19 May 2026 16:51:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:08 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f9dba52e04c4321f076b9d04a0184e0dbd41c41a2ec7bd89a2299bd150cc2`  
		Last Modified: Tue, 19 May 2026 16:51:22 GMT  
		Size: 93.4 MB (93397299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aea9b7a8f6781940e903e375c896d13adeed792797e53dd234b29206d8f8f0`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de803ffcaac430d4c1b439a48bb9a8aad4204c3c0a66b6474436f7bc2cd67a1c`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a36b6d8ef3fe5bd0b89465e62e82794aa9117306a51741238282ce350e2214`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:49c716706ff0730dfeba693b41a8492ddb7cf159f032a06cf03334508fc42cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f62c23aabeb6ae6ed52931b53d73ad2db500c6d1362845242318ae1a5ecd0d`

```dockerfile
```

-	Layers:
	-	`sha256:4ea14e5ab2a277770f715332aa44ee0052cbca89b3f4b2114de5da514ae1fca3`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
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
$ docker pull varnish@sha256:aa9310b89f73419dace2304336deb6052b89e943bce787b5b38df87ce88ed920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:968ab1f174d9860b2a46e6efc7b8a1abb901127dd722c6e1cf81d440653b9400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129144552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da79eb0a6d4a953801bc94482a81bcd11c8c4befcbd55fd6b1daf899755fa7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:16 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:16 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:16 GMT
USER varnish
# Tue, 19 May 2026 16:51:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:16 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612df49696e4e9e8458780549dacf4870f02dba8677aa8258b9328ea6e52c680`  
		Last Modified: Tue, 19 May 2026 16:51:31 GMT  
		Size: 99.4 MB (99361215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205533a727eaee849c2f585a1b32c58d2735609c66ffa059cd0012cc2b86e9a6`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e2454d9c45432fd3e02f3bb384890904ebd724c013bf2f1bce311adecce333`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9587f4dfb40fa5abc9679be2e6f16742950a56f4d968f27c8fc8ec2fc2ad0710`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:e8dcd113f2ad51ed3a6842c5458ad3cafb79db960c5b06f867232d22e6cb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c4205061f4240b54a9152f04575f483983dde6b1dd6bbfe49cd57a7a77517d`

```dockerfile
```

-	Layers:
	-	`sha256:3b0210cff421aab0bd55c06f34b7a91455e1d8dbd73dbb71fa849f76b816ae73`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 20.9 KB (20868 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:15bb3c3c9325d159898c1d095b8a2ca4ff2be1417f06c19b5218a522bad54c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a94db5a53bf3a03fd4bae5afd73f381af0c594900bca47f430c252e9b28c6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:08 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:08 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:08 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:08 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:08 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:08 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:08 GMT
USER varnish
# Tue, 19 May 2026 16:51:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:08 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f9dba52e04c4321f076b9d04a0184e0dbd41c41a2ec7bd89a2299bd150cc2`  
		Last Modified: Tue, 19 May 2026 16:51:22 GMT  
		Size: 93.4 MB (93397299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aea9b7a8f6781940e903e375c896d13adeed792797e53dd234b29206d8f8f0`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de803ffcaac430d4c1b439a48bb9a8aad4204c3c0a66b6474436f7bc2cd67a1c`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a36b6d8ef3fe5bd0b89465e62e82794aa9117306a51741238282ce350e2214`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:49c716706ff0730dfeba693b41a8492ddb7cf159f032a06cf03334508fc42cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f62c23aabeb6ae6ed52931b53d73ad2db500c6d1362845242318ae1a5ecd0d`

```dockerfile
```

-	Layers:
	-	`sha256:4ea14e5ab2a277770f715332aa44ee0052cbca89b3f4b2114de5da514ae1fca3`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
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
$ docker pull varnish@sha256:aa9310b89f73419dace2304336deb6052b89e943bce787b5b38df87ce88ed920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.2` - linux; amd64

```console
$ docker pull varnish@sha256:968ab1f174d9860b2a46e6efc7b8a1abb901127dd722c6e1cf81d440653b9400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129144552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da79eb0a6d4a953801bc94482a81bcd11c8c4befcbd55fd6b1daf899755fa7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:16 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:16 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:16 GMT
USER varnish
# Tue, 19 May 2026 16:51:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:16 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612df49696e4e9e8458780549dacf4870f02dba8677aa8258b9328ea6e52c680`  
		Last Modified: Tue, 19 May 2026 16:51:31 GMT  
		Size: 99.4 MB (99361215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205533a727eaee849c2f585a1b32c58d2735609c66ffa059cd0012cc2b86e9a6`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e2454d9c45432fd3e02f3bb384890904ebd724c013bf2f1bce311adecce333`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9587f4dfb40fa5abc9679be2e6f16742950a56f4d968f27c8fc8ec2fc2ad0710`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2` - unknown; unknown

```console
$ docker pull varnish@sha256:e8dcd113f2ad51ed3a6842c5458ad3cafb79db960c5b06f867232d22e6cb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c4205061f4240b54a9152f04575f483983dde6b1dd6bbfe49cd57a7a77517d`

```dockerfile
```

-	Layers:
	-	`sha256:3b0210cff421aab0bd55c06f34b7a91455e1d8dbd73dbb71fa849f76b816ae73`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 20.9 KB (20868 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.2` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:15bb3c3c9325d159898c1d095b8a2ca4ff2be1417f06c19b5218a522bad54c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a94db5a53bf3a03fd4bae5afd73f381af0c594900bca47f430c252e9b28c6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:08 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:08 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:08 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:08 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:08 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:08 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:08 GMT
USER varnish
# Tue, 19 May 2026 16:51:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:08 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f9dba52e04c4321f076b9d04a0184e0dbd41c41a2ec7bd89a2299bd150cc2`  
		Last Modified: Tue, 19 May 2026 16:51:22 GMT  
		Size: 93.4 MB (93397299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aea9b7a8f6781940e903e375c896d13adeed792797e53dd234b29206d8f8f0`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de803ffcaac430d4c1b439a48bb9a8aad4204c3c0a66b6474436f7bc2cd67a1c`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a36b6d8ef3fe5bd0b89465e62e82794aa9117306a51741238282ce350e2214`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2` - unknown; unknown

```console
$ docker pull varnish@sha256:49c716706ff0730dfeba693b41a8492ddb7cf159f032a06cf03334508fc42cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f62c23aabeb6ae6ed52931b53d73ad2db500c6d1362845242318ae1a5ecd0d`

```dockerfile
```

-	Layers:
	-	`sha256:4ea14e5ab2a277770f715332aa44ee0052cbca89b3f4b2114de5da514ae1fca3`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.2-1`

```console
$ docker pull varnish@sha256:aa9310b89f73419dace2304336deb6052b89e943bce787b5b38df87ce88ed920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.2-1` - linux; amd64

```console
$ docker pull varnish@sha256:968ab1f174d9860b2a46e6efc7b8a1abb901127dd722c6e1cf81d440653b9400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129144552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da79eb0a6d4a953801bc94482a81bcd11c8c4befcbd55fd6b1daf899755fa7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:16 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:16 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:16 GMT
USER varnish
# Tue, 19 May 2026 16:51:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:16 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612df49696e4e9e8458780549dacf4870f02dba8677aa8258b9328ea6e52c680`  
		Last Modified: Tue, 19 May 2026 16:51:31 GMT  
		Size: 99.4 MB (99361215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205533a727eaee849c2f585a1b32c58d2735609c66ffa059cd0012cc2b86e9a6`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e2454d9c45432fd3e02f3bb384890904ebd724c013bf2f1bce311adecce333`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9587f4dfb40fa5abc9679be2e6f16742950a56f4d968f27c8fc8ec2fc2ad0710`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2-1` - unknown; unknown

```console
$ docker pull varnish@sha256:e8dcd113f2ad51ed3a6842c5458ad3cafb79db960c5b06f867232d22e6cb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c4205061f4240b54a9152f04575f483983dde6b1dd6bbfe49cd57a7a77517d`

```dockerfile
```

-	Layers:
	-	`sha256:3b0210cff421aab0bd55c06f34b7a91455e1d8dbd73dbb71fa849f76b816ae73`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 20.9 KB (20868 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.2-1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:15bb3c3c9325d159898c1d095b8a2ca4ff2be1417f06c19b5218a522bad54c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a94db5a53bf3a03fd4bae5afd73f381af0c594900bca47f430c252e9b28c6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:08 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:08 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:08 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:08 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:08 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:08 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:08 GMT
USER varnish
# Tue, 19 May 2026 16:51:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:08 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f9dba52e04c4321f076b9d04a0184e0dbd41c41a2ec7bd89a2299bd150cc2`  
		Last Modified: Tue, 19 May 2026 16:51:22 GMT  
		Size: 93.4 MB (93397299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aea9b7a8f6781940e903e375c896d13adeed792797e53dd234b29206d8f8f0`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de803ffcaac430d4c1b439a48bb9a8aad4204c3c0a66b6474436f7bc2cd67a1c`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a36b6d8ef3fe5bd0b89465e62e82794aa9117306a51741238282ce350e2214`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.2-1` - unknown; unknown

```console
$ docker pull varnish@sha256:49c716706ff0730dfeba693b41a8492ddb7cf159f032a06cf03334508fc42cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f62c23aabeb6ae6ed52931b53d73ad2db500c6d1362845242318ae1a5ecd0d`

```dockerfile
```

-	Layers:
	-	`sha256:4ea14e5ab2a277770f715332aa44ee0052cbca89b3f4b2114de5da514ae1fca3`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
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
$ docker pull varnish@sha256:63c4d6718480478d9698ebbb23e5ad82b2d4188776124d5a8c639150b483a72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9` - linux; amd64

```console
$ docker pull varnish@sha256:2c71b996dcd3da7fbbf8be0b6ee2d48296f571fb7e2dbc3516a537b414897f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131181792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2328c5d408f552eba16f95302e378b782e9ba73c615dc9672d22182a4f4c5f6f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:09 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:09 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:09 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:09 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:09 GMT
USER varnish
# Tue, 19 May 2026 16:50:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:09 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07730b1f10b9551728705b80db02b4bda492f1ffb8b419bce350fa386a0b19c6`  
		Last Modified: Tue, 19 May 2026 16:50:25 GMT  
		Size: 101.4 MB (101398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aba74e93b31c8282c1ee379a254b61ba7c906410b76b5c02784b5ad0552e48e`  
		Last Modified: Tue, 19 May 2026 16:50:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2fef983d7bd80d9985291135d79de0e4a069d15cef69401feba21e170bea9e`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6849c732280da8da18a2326133c27b6023384d11e61acc26fca0b91a9bc506`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:442a00268e323486eb8bd48c71b7b73803ee7be0a603f9757178dcb366c33603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6144c65fbf0e45a199767e451093eb505b7b86e4e9b4646ab55361028260a`

```dockerfile
```

-	Layers:
	-	`sha256:2afc292b0ac7588be9f9ae13bbf7b906eee0e423e8f265fe3c7961217ad313c6`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c5688af3bfeb30b3c2191b8da96576565dfc17c446a1a8ceb1be85ee6ff9db31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125593353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecdaafe694c9c92e76542f39c0b8a35509bad4b660c471a773e9147eb9af957`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:24 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:24 GMT
USER varnish
# Tue, 19 May 2026 16:50:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceafc9ca98aa86325cecb819b16c5aa3a018da676aaff721ea59101315c94809`  
		Last Modified: Tue, 19 May 2026 16:50:39 GMT  
		Size: 95.4 MB (95446822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122be5b32add808514c62a49e2e291412152fa3fe076727ef64b5618bbea76f`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa5871f1f9c9fcc658611b4db4fd046c4ee2070eaaaf13ad639d321d05f9d44`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fe534821efeff48d8808c4cc520920390865d9fa893598c8769803fb7afcf`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:bb95617620725164e44149349337fb9ed5a71d4187a9fb98ede7b77c4107e8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b676022739d5ab857c385f73ae7c896154be83c902a447b05cc1116633a5a6`

```dockerfile
```

-	Layers:
	-	`sha256:d9623b17246a5de0b31bb15576053e87a14ca842e6dd765bc7d9533f7ec6d9a8`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 20.2 KB (20152 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0`

```console
$ docker pull varnish@sha256:63c4d6718480478d9698ebbb23e5ad82b2d4188776124d5a8c639150b483a72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0` - linux; amd64

```console
$ docker pull varnish@sha256:2c71b996dcd3da7fbbf8be0b6ee2d48296f571fb7e2dbc3516a537b414897f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131181792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2328c5d408f552eba16f95302e378b782e9ba73c615dc9672d22182a4f4c5f6f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:09 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:09 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:09 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:09 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:09 GMT
USER varnish
# Tue, 19 May 2026 16:50:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:09 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07730b1f10b9551728705b80db02b4bda492f1ffb8b419bce350fa386a0b19c6`  
		Last Modified: Tue, 19 May 2026 16:50:25 GMT  
		Size: 101.4 MB (101398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aba74e93b31c8282c1ee379a254b61ba7c906410b76b5c02784b5ad0552e48e`  
		Last Modified: Tue, 19 May 2026 16:50:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2fef983d7bd80d9985291135d79de0e4a069d15cef69401feba21e170bea9e`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6849c732280da8da18a2326133c27b6023384d11e61acc26fca0b91a9bc506`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:442a00268e323486eb8bd48c71b7b73803ee7be0a603f9757178dcb366c33603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6144c65fbf0e45a199767e451093eb505b7b86e4e9b4646ab55361028260a`

```dockerfile
```

-	Layers:
	-	`sha256:2afc292b0ac7588be9f9ae13bbf7b906eee0e423e8f265fe3c7961217ad313c6`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c5688af3bfeb30b3c2191b8da96576565dfc17c446a1a8ceb1be85ee6ff9db31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125593353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecdaafe694c9c92e76542f39c0b8a35509bad4b660c471a773e9147eb9af957`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:24 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:24 GMT
USER varnish
# Tue, 19 May 2026 16:50:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceafc9ca98aa86325cecb819b16c5aa3a018da676aaff721ea59101315c94809`  
		Last Modified: Tue, 19 May 2026 16:50:39 GMT  
		Size: 95.4 MB (95446822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122be5b32add808514c62a49e2e291412152fa3fe076727ef64b5618bbea76f`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa5871f1f9c9fcc658611b4db4fd046c4ee2070eaaaf13ad639d321d05f9d44`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fe534821efeff48d8808c4cc520920390865d9fa893598c8769803fb7afcf`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:bb95617620725164e44149349337fb9ed5a71d4187a9fb98ede7b77c4107e8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b676022739d5ab857c385f73ae7c896154be83c902a447b05cc1116633a5a6`

```dockerfile
```

-	Layers:
	-	`sha256:d9623b17246a5de0b31bb15576053e87a14ca842e6dd765bc7d9533f7ec6d9a8`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 20.2 KB (20152 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0.3`

```console
$ docker pull varnish@sha256:63c4d6718480478d9698ebbb23e5ad82b2d4188776124d5a8c639150b483a72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0.3` - linux; amd64

```console
$ docker pull varnish@sha256:2c71b996dcd3da7fbbf8be0b6ee2d48296f571fb7e2dbc3516a537b414897f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131181792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2328c5d408f552eba16f95302e378b782e9ba73c615dc9672d22182a4f4c5f6f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:09 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:09 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:09 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:09 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:09 GMT
USER varnish
# Tue, 19 May 2026 16:50:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:09 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07730b1f10b9551728705b80db02b4bda492f1ffb8b419bce350fa386a0b19c6`  
		Last Modified: Tue, 19 May 2026 16:50:25 GMT  
		Size: 101.4 MB (101398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aba74e93b31c8282c1ee379a254b61ba7c906410b76b5c02784b5ad0552e48e`  
		Last Modified: Tue, 19 May 2026 16:50:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2fef983d7bd80d9985291135d79de0e4a069d15cef69401feba21e170bea9e`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6849c732280da8da18a2326133c27b6023384d11e61acc26fca0b91a9bc506`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.3` - unknown; unknown

```console
$ docker pull varnish@sha256:442a00268e323486eb8bd48c71b7b73803ee7be0a603f9757178dcb366c33603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6144c65fbf0e45a199767e451093eb505b7b86e4e9b4646ab55361028260a`

```dockerfile
```

-	Layers:
	-	`sha256:2afc292b0ac7588be9f9ae13bbf7b906eee0e423e8f265fe3c7961217ad313c6`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c5688af3bfeb30b3c2191b8da96576565dfc17c446a1a8ceb1be85ee6ff9db31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125593353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecdaafe694c9c92e76542f39c0b8a35509bad4b660c471a773e9147eb9af957`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:24 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:24 GMT
USER varnish
# Tue, 19 May 2026 16:50:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceafc9ca98aa86325cecb819b16c5aa3a018da676aaff721ea59101315c94809`  
		Last Modified: Tue, 19 May 2026 16:50:39 GMT  
		Size: 95.4 MB (95446822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122be5b32add808514c62a49e2e291412152fa3fe076727ef64b5618bbea76f`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa5871f1f9c9fcc658611b4db4fd046c4ee2070eaaaf13ad639d321d05f9d44`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fe534821efeff48d8808c4cc520920390865d9fa893598c8769803fb7afcf`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.3` - unknown; unknown

```console
$ docker pull varnish@sha256:bb95617620725164e44149349337fb9ed5a71d4187a9fb98ede7b77c4107e8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b676022739d5ab857c385f73ae7c896154be83c902a447b05cc1116633a5a6`

```dockerfile
```

-	Layers:
	-	`sha256:d9623b17246a5de0b31bb15576053e87a14ca842e6dd765bc7d9533f7ec6d9a8`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 20.2 KB (20152 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0.3-1`

```console
$ docker pull varnish@sha256:63c4d6718480478d9698ebbb23e5ad82b2d4188776124d5a8c639150b483a72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0.3-1` - linux; amd64

```console
$ docker pull varnish@sha256:2c71b996dcd3da7fbbf8be0b6ee2d48296f571fb7e2dbc3516a537b414897f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131181792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2328c5d408f552eba16f95302e378b782e9ba73c615dc9672d22182a4f4c5f6f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:09 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:09 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:09 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:09 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:09 GMT
USER varnish
# Tue, 19 May 2026 16:50:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:09 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07730b1f10b9551728705b80db02b4bda492f1ffb8b419bce350fa386a0b19c6`  
		Last Modified: Tue, 19 May 2026 16:50:25 GMT  
		Size: 101.4 MB (101398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aba74e93b31c8282c1ee379a254b61ba7c906410b76b5c02784b5ad0552e48e`  
		Last Modified: Tue, 19 May 2026 16:50:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2fef983d7bd80d9985291135d79de0e4a069d15cef69401feba21e170bea9e`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6849c732280da8da18a2326133c27b6023384d11e61acc26fca0b91a9bc506`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.3-1` - unknown; unknown

```console
$ docker pull varnish@sha256:442a00268e323486eb8bd48c71b7b73803ee7be0a603f9757178dcb366c33603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6144c65fbf0e45a199767e451093eb505b7b86e4e9b4646ab55361028260a`

```dockerfile
```

-	Layers:
	-	`sha256:2afc292b0ac7588be9f9ae13bbf7b906eee0e423e8f265fe3c7961217ad313c6`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0.3-1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c5688af3bfeb30b3c2191b8da96576565dfc17c446a1a8ceb1be85ee6ff9db31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125593353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecdaafe694c9c92e76542f39c0b8a35509bad4b660c471a773e9147eb9af957`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:24 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:24 GMT
USER varnish
# Tue, 19 May 2026 16:50:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceafc9ca98aa86325cecb819b16c5aa3a018da676aaff721ea59101315c94809`  
		Last Modified: Tue, 19 May 2026 16:50:39 GMT  
		Size: 95.4 MB (95446822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122be5b32add808514c62a49e2e291412152fa3fe076727ef64b5618bbea76f`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa5871f1f9c9fcc658611b4db4fd046c4ee2070eaaaf13ad639d321d05f9d44`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fe534821efeff48d8808c4cc520920390865d9fa893598c8769803fb7afcf`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.3-1` - unknown; unknown

```console
$ docker pull varnish@sha256:bb95617620725164e44149349337fb9ed5a71d4187a9fb98ede7b77c4107e8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b676022739d5ab857c385f73ae7c896154be83c902a447b05cc1116633a5a6`

```dockerfile
```

-	Layers:
	-	`sha256:d9623b17246a5de0b31bb15576053e87a14ca842e6dd765bc7d9533f7ec6d9a8`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 20.2 KB (20152 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:63c4d6718480478d9698ebbb23e5ad82b2d4188776124d5a8c639150b483a72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:2c71b996dcd3da7fbbf8be0b6ee2d48296f571fb7e2dbc3516a537b414897f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131181792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2328c5d408f552eba16f95302e378b782e9ba73c615dc9672d22182a4f4c5f6f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:09 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:09 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:09 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:09 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:09 GMT
USER varnish
# Tue, 19 May 2026 16:50:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:09 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07730b1f10b9551728705b80db02b4bda492f1ffb8b419bce350fa386a0b19c6`  
		Last Modified: Tue, 19 May 2026 16:50:25 GMT  
		Size: 101.4 MB (101398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aba74e93b31c8282c1ee379a254b61ba7c906410b76b5c02784b5ad0552e48e`  
		Last Modified: Tue, 19 May 2026 16:50:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2fef983d7bd80d9985291135d79de0e4a069d15cef69401feba21e170bea9e`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6849c732280da8da18a2326133c27b6023384d11e61acc26fca0b91a9bc506`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:442a00268e323486eb8bd48c71b7b73803ee7be0a603f9757178dcb366c33603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6144c65fbf0e45a199767e451093eb505b7b86e4e9b4646ab55361028260a`

```dockerfile
```

-	Layers:
	-	`sha256:2afc292b0ac7588be9f9ae13bbf7b906eee0e423e8f265fe3c7961217ad313c6`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c5688af3bfeb30b3c2191b8da96576565dfc17c446a1a8ceb1be85ee6ff9db31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125593353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecdaafe694c9c92e76542f39c0b8a35509bad4b660c471a773e9147eb9af957`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:24 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:24 GMT
USER varnish
# Tue, 19 May 2026 16:50:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceafc9ca98aa86325cecb819b16c5aa3a018da676aaff721ea59101315c94809`  
		Last Modified: Tue, 19 May 2026 16:50:39 GMT  
		Size: 95.4 MB (95446822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122be5b32add808514c62a49e2e291412152fa3fe076727ef64b5618bbea76f`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa5871f1f9c9fcc658611b4db4fd046c4ee2070eaaaf13ad639d321d05f9d44`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fe534821efeff48d8808c4cc520920390865d9fa893598c8769803fb7afcf`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:bb95617620725164e44149349337fb9ed5a71d4187a9fb98ede7b77c4107e8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b676022739d5ab857c385f73ae7c896154be83c902a447b05cc1116633a5a6`

```dockerfile
```

-	Layers:
	-	`sha256:d9623b17246a5de0b31bb15576053e87a14ca842e6dd765bc7d9533f7ec6d9a8`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 20.2 KB (20152 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:63c4d6718480478d9698ebbb23e5ad82b2d4188776124d5a8c639150b483a72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:2c71b996dcd3da7fbbf8be0b6ee2d48296f571fb7e2dbc3516a537b414897f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131181792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2328c5d408f552eba16f95302e378b782e9ba73c615dc9672d22182a4f4c5f6f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:09 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:09 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:09 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:09 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:09 GMT
USER varnish
# Tue, 19 May 2026 16:50:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:09 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07730b1f10b9551728705b80db02b4bda492f1ffb8b419bce350fa386a0b19c6`  
		Last Modified: Tue, 19 May 2026 16:50:25 GMT  
		Size: 101.4 MB (101398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aba74e93b31c8282c1ee379a254b61ba7c906410b76b5c02784b5ad0552e48e`  
		Last Modified: Tue, 19 May 2026 16:50:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2fef983d7bd80d9985291135d79de0e4a069d15cef69401feba21e170bea9e`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6849c732280da8da18a2326133c27b6023384d11e61acc26fca0b91a9bc506`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:442a00268e323486eb8bd48c71b7b73803ee7be0a603f9757178dcb366c33603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6144c65fbf0e45a199767e451093eb505b7b86e4e9b4646ab55361028260a`

```dockerfile
```

-	Layers:
	-	`sha256:2afc292b0ac7588be9f9ae13bbf7b906eee0e423e8f265fe3c7961217ad313c6`  
		Last Modified: Tue, 19 May 2026 16:50:21 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c5688af3bfeb30b3c2191b8da96576565dfc17c446a1a8ceb1be85ee6ff9db31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125593353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecdaafe694c9c92e76542f39c0b8a35509bad4b660c471a773e9147eb9af957`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:50:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:24 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 16:50:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:50:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:50:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:50:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 16:50:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:24 GMT
USER varnish
# Tue, 19 May 2026 16:50:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceafc9ca98aa86325cecb819b16c5aa3a018da676aaff721ea59101315c94809`  
		Last Modified: Tue, 19 May 2026 16:50:39 GMT  
		Size: 95.4 MB (95446822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122be5b32add808514c62a49e2e291412152fa3fe076727ef64b5618bbea76f`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa5871f1f9c9fcc658611b4db4fd046c4ee2070eaaaf13ad639d321d05f9d44`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fe534821efeff48d8808c4cc520920390865d9fa893598c8769803fb7afcf`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:bb95617620725164e44149349337fb9ed5a71d4187a9fb98ede7b77c4107e8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b676022739d5ab857c385f73ae7c896154be83c902a447b05cc1116633a5a6`

```dockerfile
```

-	Layers:
	-	`sha256:d9623b17246a5de0b31bb15576053e87a14ca842e6dd765bc7d9533f7ec6d9a8`  
		Last Modified: Tue, 19 May 2026 16:50:37 GMT  
		Size: 20.2 KB (20152 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:aa9310b89f73419dace2304336deb6052b89e943bce787b5b38df87ce88ed920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:968ab1f174d9860b2a46e6efc7b8a1abb901127dd722c6e1cf81d440653b9400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129144552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da79eb0a6d4a953801bc94482a81bcd11c8c4befcbd55fd6b1daf899755fa7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:16 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:16 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:16 GMT
USER varnish
# Tue, 19 May 2026 16:51:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:16 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612df49696e4e9e8458780549dacf4870f02dba8677aa8258b9328ea6e52c680`  
		Last Modified: Tue, 19 May 2026 16:51:31 GMT  
		Size: 99.4 MB (99361215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205533a727eaee849c2f585a1b32c58d2735609c66ffa059cd0012cc2b86e9a6`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e2454d9c45432fd3e02f3bb384890904ebd724c013bf2f1bce311adecce333`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9587f4dfb40fa5abc9679be2e6f16742950a56f4d968f27c8fc8ec2fc2ad0710`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e8dcd113f2ad51ed3a6842c5458ad3cafb79db960c5b06f867232d22e6cb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c4205061f4240b54a9152f04575f483983dde6b1dd6bbfe49cd57a7a77517d`

```dockerfile
```

-	Layers:
	-	`sha256:3b0210cff421aab0bd55c06f34b7a91455e1d8dbd73dbb71fa849f76b816ae73`  
		Last Modified: Tue, 19 May 2026 16:51:28 GMT  
		Size: 20.9 KB (20868 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:15bb3c3c9325d159898c1d095b8a2ca4ff2be1417f06c19b5218a522bad54c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123544061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a94db5a53bf3a03fd4bae5afd73f381af0c594900bca47f430c252e9b28c6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 16:51:08 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:08 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:08 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 16:51:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:08 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:08 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:08 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:08 GMT
USER varnish
# Tue, 19 May 2026 16:51:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:08 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f9dba52e04c4321f076b9d04a0184e0dbd41c41a2ec7bd89a2299bd150cc2`  
		Last Modified: Tue, 19 May 2026 16:51:22 GMT  
		Size: 93.4 MB (93397299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aea9b7a8f6781940e903e375c896d13adeed792797e53dd234b29206d8f8f0`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de803ffcaac430d4c1b439a48bb9a8aad4204c3c0a66b6474436f7bc2cd67a1c`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a36b6d8ef3fe5bd0b89465e62e82794aa9117306a51741238282ce350e2214`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:49c716706ff0730dfeba693b41a8492ddb7cf159f032a06cf03334508fc42cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f62c23aabeb6ae6ed52931b53d73ad2db500c6d1362845242318ae1a5ecd0d`

```dockerfile
```

-	Layers:
	-	`sha256:4ea14e5ab2a277770f715332aa44ee0052cbca89b3f4b2114de5da514ae1fca3`  
		Last Modified: Tue, 19 May 2026 16:51:20 GMT  
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
$ docker pull varnish@sha256:ce48281fde11b2161655f901b3abd5bc09e54c08435a2ee8f1ac63d83a170163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:c258b30827c01e76bea09685cb6c2f260072c41f5df9b4957089aaaeed91bda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127671811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dcfcdb7feeb73aa04b58834be7c4b1bd7ea55d509ef3faf333011d7f66682f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:50:54 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:50:54 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:50:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:50:54 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:50:55 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:50:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:50:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:50:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:50:55 GMT
CMD []
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac07b99ec939068af4c3948829183d21610a6b8b8fc7e42d6884c397d2135cdb`  
		Last Modified: Tue, 19 May 2026 16:51:09 GMT  
		Size: 99.4 MB (99434772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f943a779e749a62ba476b583d2a62f8ed559187a6583d1d002f2db3e70142`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:82c2557c61d3eee26a34d3d2c93b31e0f3a8761c459c9ea65f196b8836098146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4da491fcc85938fea8ad2f88e45c7b5b38089eef50c3c9a57ac8cd363fb5b`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2bf9dd7478422558585888b17ca921358ba94a81a35ce5a04f75e5f85f0cb`  
		Last Modified: Tue, 19 May 2026 16:51:06 GMT  
		Size: 13.3 KB (13263 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:820ea3a1cdacd690993318312d666bf27c5379e45c490a373e8d7e27212220e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122100906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ae80baf0549534b56f99f8a537a1943a1b1a9dc8ae9ce1ed3a21020267f7bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 19 May 2026 16:51:09 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 16:51:09 GMT
ARG VARNISH_VERSION_NUMBER=6.0.18-1
# Tue, 19 May 2026 16:51:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:09 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.18-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:09 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:09 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:09 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:09 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659a62075f19812c24999d3860ca0e8cfbcf98d81aa7cfab5de0dcd4fa864c7c`  
		Last Modified: Tue, 19 May 2026 16:51:24 GMT  
		Size: 94.0 MB (93983984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0700d0a66165a5b584e5ad61550d3f0b515836fca5cff47f97f3d6648d61e03c`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:ea873ff0c885dacb99f4e714c712765a13f9312b8ac5a7ec1e04221a89eb53fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90489d6680c7b1745deb18e8fe5d6a93324c00e0a68b886fba9640ae0ecc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:643c0366a8db61b07f7c83c6ff8a137f0449bd2ebe78564a01b8c48a26b3166d`  
		Last Modified: Tue, 19 May 2026 16:51:21 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json
