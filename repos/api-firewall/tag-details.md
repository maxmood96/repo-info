<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.15`](#api-firewall0615)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.15`

```console
$ docker pull api-firewall@sha256:a95fe4defb49deb6876dc570643fb46f13904cc89547b2bc6fe47bdf16468662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.15` - linux; amd64

```console
$ docker pull api-firewall@sha256:83d7c29e6a80e74a6219c1af1d81fa29fdbe130e1fbe41b0815b9875276bafe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13747431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf178967bc9124aeb8a1d13e9b97dab6ccb3e4bdc3bbfc429562a92f8ffb5f5a`
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
# Tue, 20 Feb 2024 20:51:12 GMT
ENV APIFIREWALL_VERSION=v0.6.15
# Tue, 20 Feb 2024 20:51:15 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='bcd672cef9c3de2f87c995fe948efd0310fb66fd441f98a0e1f685ff215d6daf';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f69c9b63c89db1e140a9e268f75dd2bace1dadff4550363408be6f4e0f00365b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='96ac79d6a6e6df6c357391d5e611f2204e48b951a443152ede6a19753c959c27';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 20 Feb 2024 20:51:15 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 20 Feb 2024 20:51:15 GMT
USER api-firewall
# Tue, 20 Feb 2024 20:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 20:51:15 GMT
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
	-	`sha256:11cd2452c5eab1121633aeaa09018cb41d4d3c5971280a781dbb182b6922c3e7`  
		Last Modified: Tue, 20 Feb 2024 20:51:25 GMT  
		Size: 10.3 MB (10343328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8925df2bea293cf7042b9b7fcb6d024da73ae4dedd77cd4fc454ff8897aba02`  
		Last Modified: Tue, 20 Feb 2024 20:51:24 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.15` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:c86357f403b9578eb4fc38eef278825d2d8aed1515c8608581c778693b862c28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12837884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41c6270eb4253078101a2200d65ab874f8c80d6a7134d3a6695c962b2a4ba16`
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
# Tue, 20 Feb 2024 19:39:16 GMT
ENV APIFIREWALL_VERSION=v0.6.15
# Tue, 20 Feb 2024 19:39:19 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='bcd672cef9c3de2f87c995fe948efd0310fb66fd441f98a0e1f685ff215d6daf';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f69c9b63c89db1e140a9e268f75dd2bace1dadff4550363408be6f4e0f00365b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='96ac79d6a6e6df6c357391d5e611f2204e48b951a443152ede6a19753c959c27';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 20 Feb 2024 19:39:19 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 20 Feb 2024 19:39:19 GMT
USER api-firewall
# Tue, 20 Feb 2024 19:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 19:39:19 GMT
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
	-	`sha256:df702d9a21e9544557137b702ec2a529d1822b987bad4c1ead9dff0610630dc0`  
		Last Modified: Tue, 20 Feb 2024 19:39:28 GMT  
		Size: 9.5 MB (9502965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc1aab8bd6979880414ea50c492df0ff9e409f17bc4c7c799bbdd84acff1ac`  
		Last Modified: Tue, 20 Feb 2024 19:39:27 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.15` - linux; 386

```console
$ docker pull api-firewall@sha256:d437033a8649e58e9732d8eea97b30903adc94e0d0d9568a56066aabb7ce263f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12246548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943e398ca103d60edbbd9c0a92a9453dc2a44b35a8cdd6a6156fd4ff7d0dbae1`
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
# Tue, 20 Feb 2024 19:58:06 GMT
ENV APIFIREWALL_VERSION=v0.6.15
# Tue, 20 Feb 2024 19:58:09 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='bcd672cef9c3de2f87c995fe948efd0310fb66fd441f98a0e1f685ff215d6daf';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f69c9b63c89db1e140a9e268f75dd2bace1dadff4550363408be6f4e0f00365b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='96ac79d6a6e6df6c357391d5e611f2204e48b951a443152ede6a19753c959c27';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 20 Feb 2024 19:58:09 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 20 Feb 2024 19:58:09 GMT
USER api-firewall
# Tue, 20 Feb 2024 19:58:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 19:58:10 GMT
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
	-	`sha256:065b2e1aafa664bb8511ec8235c28587157aaa88cb223abfb5a71b5b4b975cba`  
		Last Modified: Tue, 20 Feb 2024 19:58:21 GMT  
		Size: 9.0 MB (9005922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e376b33a18dc1f7fda508cc8adf3a12cb408a18c84fa4f177b80cb7197b71a8`  
		Last Modified: Tue, 20 Feb 2024 19:58:19 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:a95fe4defb49deb6876dc570643fb46f13904cc89547b2bc6fe47bdf16468662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:83d7c29e6a80e74a6219c1af1d81fa29fdbe130e1fbe41b0815b9875276bafe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13747431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf178967bc9124aeb8a1d13e9b97dab6ccb3e4bdc3bbfc429562a92f8ffb5f5a`
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
# Tue, 20 Feb 2024 20:51:12 GMT
ENV APIFIREWALL_VERSION=v0.6.15
# Tue, 20 Feb 2024 20:51:15 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='bcd672cef9c3de2f87c995fe948efd0310fb66fd441f98a0e1f685ff215d6daf';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f69c9b63c89db1e140a9e268f75dd2bace1dadff4550363408be6f4e0f00365b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='96ac79d6a6e6df6c357391d5e611f2204e48b951a443152ede6a19753c959c27';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 20 Feb 2024 20:51:15 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 20 Feb 2024 20:51:15 GMT
USER api-firewall
# Tue, 20 Feb 2024 20:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 20:51:15 GMT
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
	-	`sha256:11cd2452c5eab1121633aeaa09018cb41d4d3c5971280a781dbb182b6922c3e7`  
		Last Modified: Tue, 20 Feb 2024 20:51:25 GMT  
		Size: 10.3 MB (10343328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8925df2bea293cf7042b9b7fcb6d024da73ae4dedd77cd4fc454ff8897aba02`  
		Last Modified: Tue, 20 Feb 2024 20:51:24 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:c86357f403b9578eb4fc38eef278825d2d8aed1515c8608581c778693b862c28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12837884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41c6270eb4253078101a2200d65ab874f8c80d6a7134d3a6695c962b2a4ba16`
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
# Tue, 20 Feb 2024 19:39:16 GMT
ENV APIFIREWALL_VERSION=v0.6.15
# Tue, 20 Feb 2024 19:39:19 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='bcd672cef9c3de2f87c995fe948efd0310fb66fd441f98a0e1f685ff215d6daf';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f69c9b63c89db1e140a9e268f75dd2bace1dadff4550363408be6f4e0f00365b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='96ac79d6a6e6df6c357391d5e611f2204e48b951a443152ede6a19753c959c27';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 20 Feb 2024 19:39:19 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 20 Feb 2024 19:39:19 GMT
USER api-firewall
# Tue, 20 Feb 2024 19:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 19:39:19 GMT
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
	-	`sha256:df702d9a21e9544557137b702ec2a529d1822b987bad4c1ead9dff0610630dc0`  
		Last Modified: Tue, 20 Feb 2024 19:39:28 GMT  
		Size: 9.5 MB (9502965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc1aab8bd6979880414ea50c492df0ff9e409f17bc4c7c799bbdd84acff1ac`  
		Last Modified: Tue, 20 Feb 2024 19:39:27 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:d437033a8649e58e9732d8eea97b30903adc94e0d0d9568a56066aabb7ce263f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12246548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943e398ca103d60edbbd9c0a92a9453dc2a44b35a8cdd6a6156fd4ff7d0dbae1`
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
# Tue, 20 Feb 2024 19:58:06 GMT
ENV APIFIREWALL_VERSION=v0.6.15
# Tue, 20 Feb 2024 19:58:09 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='bcd672cef9c3de2f87c995fe948efd0310fb66fd441f98a0e1f685ff215d6daf';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='f69c9b63c89db1e140a9e268f75dd2bace1dadff4550363408be6f4e0f00365b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='96ac79d6a6e6df6c357391d5e611f2204e48b951a443152ede6a19753c959c27';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 20 Feb 2024 19:58:09 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 20 Feb 2024 19:58:09 GMT
USER api-firewall
# Tue, 20 Feb 2024 19:58:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 19:58:10 GMT
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
	-	`sha256:065b2e1aafa664bb8511ec8235c28587157aaa88cb223abfb5a71b5b4b975cba`  
		Last Modified: Tue, 20 Feb 2024 19:58:21 GMT  
		Size: 9.0 MB (9005922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e376b33a18dc1f7fda508cc8adf3a12cb408a18c84fa4f177b80cb7197b71a8`  
		Last Modified: Tue, 20 Feb 2024 19:58:19 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
