<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.17`](#api-firewall0617)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.17`

```console
$ docker pull api-firewall@sha256:6eaf218bfbdea82231c03ca73d52afdd9bbfd94fd7e23749fe80b65634c5aa85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `api-firewall:0.6.17` - linux; amd64

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

### `api-firewall:0.6.17` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:f03fb265fabe2b03532472be41dc6323033a04993566d26a52131fb1ee20c87e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12769806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c266e1231cd9e67dd6a7a34ec5c960ca8694698319d5f1646bb203e3ae7c2a`
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
# Mon, 01 Apr 2024 18:08:52 GMT
ENV APIFIREWALL_VERSION=v0.6.17
# Mon, 01 Apr 2024 18:08:54 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c6542de42ccf214cc543f595995a0246b2667ccab9c39b509c88d21ec4071621';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='13c830b7a7c4b97f35a141ebe576f459449fd3d27c0b14188f6440693feb2e8c';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='7d03a6f37e60ac3ea1494d958481b8fc484bd02b204aa7497d7dd6e8802101ac';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 01 Apr 2024 18:08:54 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 01 Apr 2024 18:08:54 GMT
USER api-firewall
# Mon, 01 Apr 2024 18:08:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Apr 2024 18:08:55 GMT
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
	-	`sha256:33f761aba14be0b5422b07b53bee0bf64e64e471d1b48f1bfcf5722c6180a015`  
		Last Modified: Mon, 01 Apr 2024 18:09:04 GMT  
		Size: 9.4 MB (9434887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d3037199e480f94b7ecf3830de94724058d8c76c2b8701dc557cb1549240e6`  
		Last Modified: Mon, 01 Apr 2024 18:09:02 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:b5576f797f5ccb461aeeecbc8324fb5d8ba298a7643bd5fb2903e4b83a60b202
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
$ docker pull api-firewall@sha256:f03fb265fabe2b03532472be41dc6323033a04993566d26a52131fb1ee20c87e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12769806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c266e1231cd9e67dd6a7a34ec5c960ca8694698319d5f1646bb203e3ae7c2a`
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
# Mon, 01 Apr 2024 18:08:52 GMT
ENV APIFIREWALL_VERSION=v0.6.17
# Mon, 01 Apr 2024 18:08:54 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c6542de42ccf214cc543f595995a0246b2667ccab9c39b509c88d21ec4071621';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='13c830b7a7c4b97f35a141ebe576f459449fd3d27c0b14188f6440693feb2e8c';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='7d03a6f37e60ac3ea1494d958481b8fc484bd02b204aa7497d7dd6e8802101ac';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 01 Apr 2024 18:08:54 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 01 Apr 2024 18:08:54 GMT
USER api-firewall
# Mon, 01 Apr 2024 18:08:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Apr 2024 18:08:55 GMT
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
	-	`sha256:33f761aba14be0b5422b07b53bee0bf64e64e471d1b48f1bfcf5722c6180a015`  
		Last Modified: Mon, 01 Apr 2024 18:09:04 GMT  
		Size: 9.4 MB (9434887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d3037199e480f94b7ecf3830de94724058d8c76c2b8701dc557cb1549240e6`  
		Last Modified: Mon, 01 Apr 2024 18:09:02 GMT  
		Size: 353.0 B  
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
