<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.16`](#api-firewall0616)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.16`

```console
$ docker pull api-firewall@sha256:3b20b73dd0e90e1124426c7e695dce272045c7f611f351862aa20fb4ae01b0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.16` - linux; amd64

```console
$ docker pull api-firewall@sha256:ff5a25b648e99a9e13c3677930ad3735c362efc05067c2ee3d2af4923432cce4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13788252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa1fc14feb186655cba84cebf5878c225c1fe233d99e2cc6cc89f241c119a35`
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
# Sat, 16 Mar 2024 07:58:15 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Sat, 16 Mar 2024 07:58:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 16 Mar 2024 07:58:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 16 Mar 2024 07:58:18 GMT
USER api-firewall
# Sat, 16 Mar 2024 07:58:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:58:18 GMT
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
	-	`sha256:7043e0efbf2084a2d13df6ab5a6d65cb25957e9fc5e65c3e8efffb898239af76`  
		Last Modified: Sat, 16 Mar 2024 07:58:27 GMT  
		Size: 10.4 MB (10384148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7567a21ebf823e1b85b77f7ab2e7bc0022d7ce570dc52be07728247537abbd`  
		Last Modified: Sat, 16 Mar 2024 07:58:26 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.16` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:18a928c961425d4d0e19ccb4bae54cf7b8483bc3967ad1c60e79d47c5600b509
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12875144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97f84d3c2cc9f17ac522e704c01fcae9528bb84b7a0beefb1e22140796ce4c8`
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
# Sat, 16 Mar 2024 02:53:05 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Sat, 16 Mar 2024 02:53:09 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 16 Mar 2024 02:53:09 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 16 Mar 2024 02:53:09 GMT
USER api-firewall
# Sat, 16 Mar 2024 02:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:53:10 GMT
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
	-	`sha256:aec5da8b2dc5f1b6332942f210b78881525ada54ea300bc17c2b237fc610beff`  
		Last Modified: Sat, 16 Mar 2024 02:53:18 GMT  
		Size: 9.5 MB (9540222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f0fc2906c2a9f37ba18a177e83c248ad2184cc60c9c186518046ebd58eb223`  
		Last Modified: Sat, 16 Mar 2024 02:53:16 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.16` - linux; 386

```console
$ docker pull api-firewall@sha256:d6538706176b7c481355abb46dbeb25afcb272647e37dc2521e2a40db55a046c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12285957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d809de23c6a453bd5c3649e91d4e2398d5d8990dc9e6aca8b2774277f88697d5`
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
# Fri, 15 Mar 2024 23:53:00 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Fri, 15 Mar 2024 23:53:03 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 15 Mar 2024 23:53:03 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 15 Mar 2024 23:53:03 GMT
USER api-firewall
# Fri, 15 Mar 2024 23:53:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 23:53:03 GMT
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
	-	`sha256:c333a5bb3704498b98d9af5eca85b49fe0a4d7904232530ff97189cfe291d476`  
		Last Modified: Fri, 15 Mar 2024 23:53:13 GMT  
		Size: 9.0 MB (9045332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf3d4ab8bc13d52936bb95f0085ed7052151c120f84fde5254830fe9d96feb0`  
		Last Modified: Fri, 15 Mar 2024 23:53:10 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:3b20b73dd0e90e1124426c7e695dce272045c7f611f351862aa20fb4ae01b0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:ff5a25b648e99a9e13c3677930ad3735c362efc05067c2ee3d2af4923432cce4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13788252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa1fc14feb186655cba84cebf5878c225c1fe233d99e2cc6cc89f241c119a35`
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
# Sat, 16 Mar 2024 07:58:15 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Sat, 16 Mar 2024 07:58:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 16 Mar 2024 07:58:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 16 Mar 2024 07:58:18 GMT
USER api-firewall
# Sat, 16 Mar 2024 07:58:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:58:18 GMT
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
	-	`sha256:7043e0efbf2084a2d13df6ab5a6d65cb25957e9fc5e65c3e8efffb898239af76`  
		Last Modified: Sat, 16 Mar 2024 07:58:27 GMT  
		Size: 10.4 MB (10384148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7567a21ebf823e1b85b77f7ab2e7bc0022d7ce570dc52be07728247537abbd`  
		Last Modified: Sat, 16 Mar 2024 07:58:26 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:18a928c961425d4d0e19ccb4bae54cf7b8483bc3967ad1c60e79d47c5600b509
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12875144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97f84d3c2cc9f17ac522e704c01fcae9528bb84b7a0beefb1e22140796ce4c8`
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
# Sat, 16 Mar 2024 02:53:05 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Sat, 16 Mar 2024 02:53:09 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 16 Mar 2024 02:53:09 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 16 Mar 2024 02:53:09 GMT
USER api-firewall
# Sat, 16 Mar 2024 02:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:53:10 GMT
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
	-	`sha256:aec5da8b2dc5f1b6332942f210b78881525ada54ea300bc17c2b237fc610beff`  
		Last Modified: Sat, 16 Mar 2024 02:53:18 GMT  
		Size: 9.5 MB (9540222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f0fc2906c2a9f37ba18a177e83c248ad2184cc60c9c186518046ebd58eb223`  
		Last Modified: Sat, 16 Mar 2024 02:53:16 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:d6538706176b7c481355abb46dbeb25afcb272647e37dc2521e2a40db55a046c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12285957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d809de23c6a453bd5c3649e91d4e2398d5d8990dc9e6aca8b2774277f88697d5`
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
# Fri, 15 Mar 2024 23:53:00 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Fri, 15 Mar 2024 23:53:03 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 15 Mar 2024 23:53:03 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 15 Mar 2024 23:53:03 GMT
USER api-firewall
# Fri, 15 Mar 2024 23:53:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 23:53:03 GMT
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
	-	`sha256:c333a5bb3704498b98d9af5eca85b49fe0a4d7904232530ff97189cfe291d476`  
		Last Modified: Fri, 15 Mar 2024 23:53:13 GMT  
		Size: 9.0 MB (9045332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf3d4ab8bc13d52936bb95f0085ed7052151c120f84fde5254830fe9d96feb0`  
		Last Modified: Fri, 15 Mar 2024 23:53:10 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
