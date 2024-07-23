<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.7.4`](#api-firewall074)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.7.4`

```console
$ docker pull api-firewall@sha256:0c97c5e2a2eee5f32c1d64724a2938fdcca73b25ec25ffe7246fc342c9952bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.7.4` - linux; amd64

```console
$ docker pull api-firewall@sha256:94a3ba048f6abb9e32e7c08f7481abca0e64801511906a44aee20a8f2eab3b05
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14643910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd98a392765c35c1ccae1df36f245a117e396619559ad1a56347d166f3c84b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:32:56 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 23 Jul 2024 00:32:56 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 00:32:57 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 23 Jul 2024 00:32:57 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Tue, 23 Jul 2024 00:33:00 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 23 Jul 2024 00:33:00 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 23 Jul 2024 00:33:00 GMT
USER api-firewall
# Tue, 23 Jul 2024 00:33:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:00 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad12bd0d35a37df686d0442f560c5d233b3a27d707e193ac288646a2b9583b`  
		Last Modified: Tue, 23 Jul 2024 00:33:09 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e2f70c9174f3a59400ecbc8d34b8e026b2a4b8a58dd48e4657def561e87fa4`  
		Last Modified: Tue, 23 Jul 2024 00:33:11 GMT  
		Size: 11.0 MB (11019754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d724668d4e23c86c0db5fcbdc64d344a8bb635a9491a661bf201b6952eae84af`  
		Last Modified: Tue, 23 Jul 2024 00:33:09 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.7.4` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:32730bac672c4a521c45519bd29feb6296fd30374b12d82a092f977f4c1859fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14428994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc9897fa38aea33afa11c4537b75ae5a6456bf1c1cee4b35a996cd65c9f07f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:08:54 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 22 Jul 2024 22:08:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jul 2024 22:08:55 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 22 Jul 2024 22:08:55 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Mon, 22 Jul 2024 22:08:57 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 22 Jul 2024 22:08:58 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 22 Jul 2024 22:08:58 GMT
USER api-firewall
# Mon, 22 Jul 2024 22:08:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:08:58 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4aab0e8cfa5cfe1b7c1c610501a4dd43cb8420d322b32b94ed50193964f4bc9`  
		Last Modified: Mon, 22 Jul 2024 22:09:05 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47972bb23652c6dff6e8aa27ebe3dca2d6bd3a86fb365b3cca1c667930ccef5e`  
		Last Modified: Mon, 22 Jul 2024 22:09:06 GMT  
		Size: 10.3 MB (10340795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b4bdc4bf0c8cc4b0a1f3bb85b93958659705abb8d41b9cd9e79c35ce970de0`  
		Last Modified: Mon, 22 Jul 2024 22:09:05 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.7.4` - linux; 386

```console
$ docker pull api-firewall@sha256:14c876577de14b7209ad16be2d40701912f60828bc4c38795a86410e3c3bdf0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13095197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e250ad7a8ed46283a12a6cc89eaef896cec845aee3db9cf3610ced53b8e2c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:26:37 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 23 Jul 2024 02:26:37 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 02:26:37 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 23 Jul 2024 02:26:38 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Tue, 23 Jul 2024 02:26:41 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 23 Jul 2024 02:26:41 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 23 Jul 2024 02:26:41 GMT
USER api-firewall
# Tue, 23 Jul 2024 02:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 02:26:41 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7376fd009633d50430a96172be8f59efcffb6dc902370e6a36e64e98deb0c2e`  
		Last Modified: Tue, 23 Jul 2024 02:26:50 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e4c32e87dc5501ad59a94ffa4d264ea00c76bfd904dd879ddd1a456883706e`  
		Last Modified: Tue, 23 Jul 2024 02:26:52 GMT  
		Size: 9.6 MB (9625860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203bf64b23fb5519daf0535c04a7e018fc05f20edfdd9fbf3cf063da1163ae45`  
		Last Modified: Tue, 23 Jul 2024 02:26:50 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:0c97c5e2a2eee5f32c1d64724a2938fdcca73b25ec25ffe7246fc342c9952bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:94a3ba048f6abb9e32e7c08f7481abca0e64801511906a44aee20a8f2eab3b05
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14643910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd98a392765c35c1ccae1df36f245a117e396619559ad1a56347d166f3c84b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:32:56 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 23 Jul 2024 00:32:56 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 00:32:57 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 23 Jul 2024 00:32:57 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Tue, 23 Jul 2024 00:33:00 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 23 Jul 2024 00:33:00 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 23 Jul 2024 00:33:00 GMT
USER api-firewall
# Tue, 23 Jul 2024 00:33:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:33:00 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad12bd0d35a37df686d0442f560c5d233b3a27d707e193ac288646a2b9583b`  
		Last Modified: Tue, 23 Jul 2024 00:33:09 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e2f70c9174f3a59400ecbc8d34b8e026b2a4b8a58dd48e4657def561e87fa4`  
		Last Modified: Tue, 23 Jul 2024 00:33:11 GMT  
		Size: 11.0 MB (11019754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d724668d4e23c86c0db5fcbdc64d344a8bb635a9491a661bf201b6952eae84af`  
		Last Modified: Tue, 23 Jul 2024 00:33:09 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:32730bac672c4a521c45519bd29feb6296fd30374b12d82a092f977f4c1859fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14428994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc9897fa38aea33afa11c4537b75ae5a6456bf1c1cee4b35a996cd65c9f07f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:08:54 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 22 Jul 2024 22:08:54 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jul 2024 22:08:55 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 22 Jul 2024 22:08:55 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Mon, 22 Jul 2024 22:08:57 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 22 Jul 2024 22:08:58 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 22 Jul 2024 22:08:58 GMT
USER api-firewall
# Mon, 22 Jul 2024 22:08:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:08:58 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4aab0e8cfa5cfe1b7c1c610501a4dd43cb8420d322b32b94ed50193964f4bc9`  
		Last Modified: Mon, 22 Jul 2024 22:09:05 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47972bb23652c6dff6e8aa27ebe3dca2d6bd3a86fb365b3cca1c667930ccef5e`  
		Last Modified: Mon, 22 Jul 2024 22:09:06 GMT  
		Size: 10.3 MB (10340795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b4bdc4bf0c8cc4b0a1f3bb85b93958659705abb8d41b9cd9e79c35ce970de0`  
		Last Modified: Mon, 22 Jul 2024 22:09:05 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:14c876577de14b7209ad16be2d40701912f60828bc4c38795a86410e3c3bdf0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13095197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e250ad7a8ed46283a12a6cc89eaef896cec845aee3db9cf3610ced53b8e2c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:26:37 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 23 Jul 2024 02:26:37 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 02:26:37 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Tue, 23 Jul 2024 02:26:38 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Tue, 23 Jul 2024 02:26:41 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 23 Jul 2024 02:26:41 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 23 Jul 2024 02:26:41 GMT
USER api-firewall
# Tue, 23 Jul 2024 02:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 02:26:41 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7376fd009633d50430a96172be8f59efcffb6dc902370e6a36e64e98deb0c2e`  
		Last Modified: Tue, 23 Jul 2024 02:26:50 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e4c32e87dc5501ad59a94ffa4d264ea00c76bfd904dd879ddd1a456883706e`  
		Last Modified: Tue, 23 Jul 2024 02:26:52 GMT  
		Size: 9.6 MB (9625860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203bf64b23fb5519daf0535c04a7e018fc05f20edfdd9fbf3cf063da1163ae45`  
		Last Modified: Tue, 23 Jul 2024 02:26:50 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
