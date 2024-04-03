<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.7.0`](#api-firewall070)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.7.0`

```console
$ docker pull api-firewall@sha256:8ab6c6f561fb21f29dcd4790dcd83b296a70cad370a62fa12e22d4bd55bfb275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.7.0` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:803cc0f4d4acafbe215148598dbf47805c8e8d5d16b45ab59c7fe6f1e3a4248d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13254556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a5a9b79750576074f2db254ef923c65de7e526f6e68b1ac19642ab4fdff48a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:53:04 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 16 Mar 2024 02:53:04 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 02:53:04 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 03 Apr 2024 19:06:06 GMT
ENV APIFIREWALL_VERSION=v0.7.0
# Wed, 03 Apr 2024 19:06:09 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='b4fcb15f6af4e6652b83264be595cb545abc97f569b23a2029d877c209e4a072';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b87620ca4fdb697f4e63db453e90d9da52825e8bad558988bff668f3be794fd1';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='82fac89ba99edbd9243a161ccfef147f8151b2f1b07532ac848329ed34abf391';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 03 Apr 2024 19:06:09 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 03 Apr 2024 19:06:09 GMT
USER api-firewall
# Wed, 03 Apr 2024 19:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 19:06:09 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aae77be32174ba91ba46eef23ccdaeed963df0e51624d178421140648cb98b`  
		Last Modified: Sat, 16 Mar 2024 02:53:16 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84cba5feb4d9ec23ad088dd076f30c51c0dbbdab9cbb49dff4f024b0819be13`  
		Last Modified: Wed, 03 Apr 2024 19:06:19 GMT  
		Size: 9.9 MB (9919631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d388573a64ee79c66b094b72a30a8a67f41d7f28522e9f4a6c302b24d2b2366`  
		Last Modified: Wed, 03 Apr 2024 19:06:18 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.7.0` - linux; 386

```console
$ docker pull api-firewall@sha256:3349d46dd1abc0a8aeee09209373a55891e79839a60eb468631342237a01db21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12572211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9505ebe97ecc4a8973b6da4fc1068fada2fa6806a8a453647df69df93cdaec16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:52:59 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 15 Mar 2024 23:52:59 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 23:52:59 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 03 Apr 2024 18:56:19 GMT
ENV APIFIREWALL_VERSION=v0.7.0
# Wed, 03 Apr 2024 18:56:22 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='b4fcb15f6af4e6652b83264be595cb545abc97f569b23a2029d877c209e4a072';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b87620ca4fdb697f4e63db453e90d9da52825e8bad558988bff668f3be794fd1';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='82fac89ba99edbd9243a161ccfef147f8151b2f1b07532ac848329ed34abf391';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 03 Apr 2024 18:56:22 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 03 Apr 2024 18:56:22 GMT
USER api-firewall
# Wed, 03 Apr 2024 18:56:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 18:56:23 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b16feb1c089d261f25d668bc94fb450ae9faaf09472431fb07eaa76ff9fb84`  
		Last Modified: Fri, 15 Mar 2024 23:53:10 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec5de873a70b7066dda3fa56cbf65a60ca45eec10218f8ba6da84d6cb7277ef`  
		Last Modified: Wed, 03 Apr 2024 18:56:33 GMT  
		Size: 9.3 MB (9331584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede4a68e765493da1c6082f79ca0cfaeb64933c5c74cd214deea0d6e3b04564a`  
		Last Modified: Wed, 03 Apr 2024 18:56:31 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:e27813eed102d719691cb0b8c9d71998797bac6bc291e19a66a3e8e8d02b7018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:ff324e6ce14d097b0a2126e4ecb476036a42eb6af310ab20935bc134b74e6cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13630560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0708b8331531b5f218c5a668e0d162a122d4a2239df6edfe22a2ffea8d222b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:58:15 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 16 Mar 2024 07:58:15 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 07:58:15 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 01 Apr 2024 17:52:43 GMT
ENV APIFIREWALL_VERSION=v0.6.17
# Mon, 01 Apr 2024 17:52:45 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c6542de42ccf214cc543f595995a0246b2667ccab9c39b509c88d21ec4071621';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='13c830b7a7c4b97f35a141ebe576f459449fd3d27c0b14188f6440693feb2e8c';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='7d03a6f37e60ac3ea1494d958481b8fc484bd02b204aa7497d7dd6e8802101ac';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 01 Apr 2024 17:52:45 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 01 Apr 2024 17:52:46 GMT
USER api-firewall
# Mon, 01 Apr 2024 17:52:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Apr 2024 17:52:46 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996bf125e6b3d4ba812c8d06e1edb5c9b93b9afcf0b23a4b46709f99f65a1ef0`  
		Last Modified: Sat, 16 Mar 2024 07:58:26 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89237bf4d78b4096819a522d3780055a62022dfe841e4e73197c5d72be8737e`  
		Last Modified: Mon, 01 Apr 2024 17:52:56 GMT  
		Size: 10.2 MB (10226461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a705c56175d5bbe4ec6db9d294d38abc508fcd21d32f1bdf25c8fc619de298f5`  
		Last Modified: Mon, 01 Apr 2024 17:52:54 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:803cc0f4d4acafbe215148598dbf47805c8e8d5d16b45ab59c7fe6f1e3a4248d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13254556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a5a9b79750576074f2db254ef923c65de7e526f6e68b1ac19642ab4fdff48a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:53:04 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 16 Mar 2024 02:53:04 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 02:53:04 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 03 Apr 2024 19:06:06 GMT
ENV APIFIREWALL_VERSION=v0.7.0
# Wed, 03 Apr 2024 19:06:09 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='b4fcb15f6af4e6652b83264be595cb545abc97f569b23a2029d877c209e4a072';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b87620ca4fdb697f4e63db453e90d9da52825e8bad558988bff668f3be794fd1';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='82fac89ba99edbd9243a161ccfef147f8151b2f1b07532ac848329ed34abf391';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 03 Apr 2024 19:06:09 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 03 Apr 2024 19:06:09 GMT
USER api-firewall
# Wed, 03 Apr 2024 19:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 19:06:09 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aae77be32174ba91ba46eef23ccdaeed963df0e51624d178421140648cb98b`  
		Last Modified: Sat, 16 Mar 2024 02:53:16 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84cba5feb4d9ec23ad088dd076f30c51c0dbbdab9cbb49dff4f024b0819be13`  
		Last Modified: Wed, 03 Apr 2024 19:06:19 GMT  
		Size: 9.9 MB (9919631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d388573a64ee79c66b094b72a30a8a67f41d7f28522e9f4a6c302b24d2b2366`  
		Last Modified: Wed, 03 Apr 2024 19:06:18 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:3349d46dd1abc0a8aeee09209373a55891e79839a60eb468631342237a01db21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12572211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9505ebe97ecc4a8973b6da4fc1068fada2fa6806a8a453647df69df93cdaec16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:52:59 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 15 Mar 2024 23:52:59 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 23:52:59 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 03 Apr 2024 18:56:19 GMT
ENV APIFIREWALL_VERSION=v0.7.0
# Wed, 03 Apr 2024 18:56:22 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='b4fcb15f6af4e6652b83264be595cb545abc97f569b23a2029d877c209e4a072';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='b87620ca4fdb697f4e63db453e90d9da52825e8bad558988bff668f3be794fd1';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='82fac89ba99edbd9243a161ccfef147f8151b2f1b07532ac848329ed34abf391';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 03 Apr 2024 18:56:22 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 03 Apr 2024 18:56:22 GMT
USER api-firewall
# Wed, 03 Apr 2024 18:56:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 18:56:23 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b16feb1c089d261f25d668bc94fb450ae9faaf09472431fb07eaa76ff9fb84`  
		Last Modified: Fri, 15 Mar 2024 23:53:10 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec5de873a70b7066dda3fa56cbf65a60ca45eec10218f8ba6da84d6cb7277ef`  
		Last Modified: Wed, 03 Apr 2024 18:56:33 GMT  
		Size: 9.3 MB (9331584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede4a68e765493da1c6082f79ca0cfaeb64933c5c74cd214deea0d6e3b04564a`  
		Last Modified: Wed, 03 Apr 2024 18:56:31 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
