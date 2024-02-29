<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.16`](#api-firewall0616)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.16`

```console
$ docker pull api-firewall@sha256:9a370b21d8c3d1ab07de01578be036d69f40010600a2bf31ddef7a52dd6c32ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.16` - linux; amd64

```console
$ docker pull api-firewall@sha256:58a851e00743e33c7b8aed9e77351ea4a2afaf26844ad583ad6971d27ad52731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13788249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b398f9d2dda4f2ef8050a7bedbc36eb66df7da0af33c61e2c9a44a042afd76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:13 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 27 Jan 2024 03:33:14 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 03:33:14 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 29 Feb 2024 19:19:30 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Thu, 29 Feb 2024 19:19:33 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 29 Feb 2024 19:19:33 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 29 Feb 2024 19:19:33 GMT
USER api-firewall
# Thu, 29 Feb 2024 19:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 19:19:33 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7fa9cc7f694476223b4feef7158e98c072e4da14da5bd35abe6d8360cc68e5`  
		Last Modified: Sat, 27 Jan 2024 03:33:25 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aee6853eacec2e28f0dca040fb4cfbfbf161c73310df5665f5286d8c9e9b484`  
		Last Modified: Thu, 29 Feb 2024 19:19:43 GMT  
		Size: 10.4 MB (10384147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0a924464f4b7b618bbbbe800dae81fc502a96e599e26281c3a6bb0223f56a9`  
		Last Modified: Thu, 29 Feb 2024 19:19:41 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.16` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:c5fd851d139972a89a14325c3b9fbeed7227212e083022997cc2f76692441505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12875145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4a4735346a3d3b1d4e89682d9ac6594a6cd594530da98d38f9fd90ea4add4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:38:37 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 27 Jan 2024 00:38:37 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 00:38:38 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 29 Feb 2024 19:39:15 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Thu, 29 Feb 2024 19:39:17 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 29 Feb 2024 19:39:17 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 29 Feb 2024 19:39:17 GMT
USER api-firewall
# Thu, 29 Feb 2024 19:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 19:39:17 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5763baeada3eded7a53c0af9d034cf3838f5df6a0e0ea99bbc2712ca89fcbed`  
		Last Modified: Sat, 27 Jan 2024 00:38:49 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f1f384cb07529d6d21d9cb449d59a7b716025b3f202da9aaa9f5e611bae1a0`  
		Last Modified: Thu, 29 Feb 2024 19:39:28 GMT  
		Size: 9.5 MB (9540226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2ee72fbfadcee2b80beea46cbbe7ef95257894911154f53d85b9c6a2a07d8`  
		Last Modified: Thu, 29 Feb 2024 19:39:27 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.16` - linux; 386

```console
$ docker pull api-firewall@sha256:0c1f8a58d3b6e56aa2fe5601dd11b6617d66c483b6ebd0e1eea130f2a36c8ede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12285949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4784bbf98d4b6cd9d0a03cc33f87be861276c224a0e99f0ee9f0962b1ee2e04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:24:20 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 27 Jan 2024 04:24:20 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 04:24:20 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 29 Feb 2024 19:58:58 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Thu, 29 Feb 2024 19:59:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 29 Feb 2024 19:59:01 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 29 Feb 2024 19:59:01 GMT
USER api-firewall
# Thu, 29 Feb 2024 19:59:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 19:59:02 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc8a7e6d1cf0a2002010c76b334ccc3c00785e01d28d3b2f747aa41672a8b3d`  
		Last Modified: Sat, 27 Jan 2024 04:24:31 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22e522e982b405a5a2ce79ac72818a8deeef1fb7762a8862234e18a29ed8b6e`  
		Last Modified: Thu, 29 Feb 2024 19:59:12 GMT  
		Size: 9.0 MB (9045324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2023777f9b60cead2a9713cab7ca14101d2c7cbab003acd8d1888b0dc3ed85`  
		Last Modified: Thu, 29 Feb 2024 19:59:10 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:9a370b21d8c3d1ab07de01578be036d69f40010600a2bf31ddef7a52dd6c32ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:58a851e00743e33c7b8aed9e77351ea4a2afaf26844ad583ad6971d27ad52731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13788249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b398f9d2dda4f2ef8050a7bedbc36eb66df7da0af33c61e2c9a44a042afd76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:13 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 27 Jan 2024 03:33:14 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 03:33:14 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 29 Feb 2024 19:19:30 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Thu, 29 Feb 2024 19:19:33 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 29 Feb 2024 19:19:33 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 29 Feb 2024 19:19:33 GMT
USER api-firewall
# Thu, 29 Feb 2024 19:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 19:19:33 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7fa9cc7f694476223b4feef7158e98c072e4da14da5bd35abe6d8360cc68e5`  
		Last Modified: Sat, 27 Jan 2024 03:33:25 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aee6853eacec2e28f0dca040fb4cfbfbf161c73310df5665f5286d8c9e9b484`  
		Last Modified: Thu, 29 Feb 2024 19:19:43 GMT  
		Size: 10.4 MB (10384147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0a924464f4b7b618bbbbe800dae81fc502a96e599e26281c3a6bb0223f56a9`  
		Last Modified: Thu, 29 Feb 2024 19:19:41 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:c5fd851d139972a89a14325c3b9fbeed7227212e083022997cc2f76692441505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12875145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4a4735346a3d3b1d4e89682d9ac6594a6cd594530da98d38f9fd90ea4add4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:38:37 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 27 Jan 2024 00:38:37 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 00:38:38 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 29 Feb 2024 19:39:15 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Thu, 29 Feb 2024 19:39:17 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 29 Feb 2024 19:39:17 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 29 Feb 2024 19:39:17 GMT
USER api-firewall
# Thu, 29 Feb 2024 19:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 19:39:17 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5763baeada3eded7a53c0af9d034cf3838f5df6a0e0ea99bbc2712ca89fcbed`  
		Last Modified: Sat, 27 Jan 2024 00:38:49 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f1f384cb07529d6d21d9cb449d59a7b716025b3f202da9aaa9f5e611bae1a0`  
		Last Modified: Thu, 29 Feb 2024 19:39:28 GMT  
		Size: 9.5 MB (9540226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2ee72fbfadcee2b80beea46cbbe7ef95257894911154f53d85b9c6a2a07d8`  
		Last Modified: Thu, 29 Feb 2024 19:39:27 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:0c1f8a58d3b6e56aa2fe5601dd11b6617d66c483b6ebd0e1eea130f2a36c8ede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12285949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4784bbf98d4b6cd9d0a03cc33f87be861276c224a0e99f0ee9f0962b1ee2e04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:24:20 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 27 Jan 2024 04:24:20 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 04:24:20 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 29 Feb 2024 19:58:58 GMT
ENV APIFIREWALL_VERSION=v0.6.16
# Thu, 29 Feb 2024 19:59:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='2dacb18e7fc05cd4747d9f9da9f7ab7bac22f7f4f1e7d666bdd7ceb3bfc4ebef';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c38b8c5e19376161176e20326150d3ab21c0a73b109d5da29d8b109476a89b1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='e6963efd79929fb79abe0e27629062bad74859851ce9f8cd077cd3f249b196f0';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 29 Feb 2024 19:59:01 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 29 Feb 2024 19:59:01 GMT
USER api-firewall
# Thu, 29 Feb 2024 19:59:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 19:59:02 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc8a7e6d1cf0a2002010c76b334ccc3c00785e01d28d3b2f747aa41672a8b3d`  
		Last Modified: Sat, 27 Jan 2024 04:24:31 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22e522e982b405a5a2ce79ac72818a8deeef1fb7762a8862234e18a29ed8b6e`  
		Last Modified: Thu, 29 Feb 2024 19:59:12 GMT  
		Size: 9.0 MB (9045324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2023777f9b60cead2a9713cab7ca14101d2c7cbab003acd8d1888b0dc3ed85`  
		Last Modified: Thu, 29 Feb 2024 19:59:10 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
