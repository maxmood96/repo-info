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
