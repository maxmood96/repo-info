<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.7.4`](#api-firewall074)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.7.4`

```console
$ docker pull api-firewall@sha256:a47bc900220012cc8e6a00451540fa3f5013afbe290631e7223c80583ffd0723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.7.4` - linux; amd64

```console
$ docker pull api-firewall@sha256:f12173c89fd0d79e4639e8c9688ab543240dec4b2c101ca9f021302b67b4b2ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14644893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164885ca2f842aeb00bcc632280236e9ce8b605980d438a210cf3aa7462e9215`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 18:19:30 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 12 Jul 2024 18:19:31 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 18:19:31 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 12 Jul 2024 18:19:31 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Fri, 12 Jul 2024 18:19:34 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 12 Jul 2024 18:19:34 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 12 Jul 2024 18:19:34 GMT
USER api-firewall
# Fri, 12 Jul 2024 18:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jul 2024 18:19:34 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d87dbfe46217158067587a65cde2c7b6b8aa41cc8ebdaa75a144ea29c306ee`  
		Last Modified: Fri, 12 Jul 2024 18:19:44 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11040d078ace94f003df18419efa7fabb30eb2e839293695b40743791dadc376`  
		Last Modified: Fri, 12 Jul 2024 18:19:45 GMT  
		Size: 11.0 MB (11019786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b40e476a957fc2a18034e7beead6988e59d91c3a525856b10ad98de6cfd141`  
		Last Modified: Fri, 12 Jul 2024 18:19:44 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.7.4` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:02b121ea61fc728d4027a84dfdcdfb29a133447418363ba6132339d6683a8f6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14430862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ade5ac3740069dfd306351c98e30ac51cd5deb8e15fa0116dedd8f6c510a838`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 18:40:48 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 12 Jul 2024 18:40:49 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 18:40:49 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 12 Jul 2024 18:40:49 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Fri, 12 Jul 2024 18:40:51 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 12 Jul 2024 18:40:52 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 12 Jul 2024 18:40:52 GMT
USER api-firewall
# Fri, 12 Jul 2024 18:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jul 2024 18:40:52 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc5b2e06412f2565fb493031051479b67cf55af7da844c2f8b1a4801f7ebb18`  
		Last Modified: Fri, 12 Jul 2024 18:41:00 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c2344c7e394ab5ddf90729d42d2264ccfbe2a4eff884afca1bc56bd60f433f`  
		Last Modified: Fri, 12 Jul 2024 18:41:01 GMT  
		Size: 10.3 MB (10340796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ac2d40b30e82a06c122f8d176aafd2f1b99675e53cbf9332b1ec97b24b2233`  
		Last Modified: Fri, 12 Jul 2024 18:40:59 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.7.4` - linux; 386

```console
$ docker pull api-firewall@sha256:d20c20fd418bbfcbdc30d21f7af2992ad6668c923a95646612f32b1846e3f5e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13096587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb388b92ecd302fc2c9bccae5e3c44049b838cc18dacc7c439897a671912281f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 18:38:14 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 12 Jul 2024 18:38:14 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 18:38:15 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 12 Jul 2024 18:38:15 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Fri, 12 Jul 2024 18:38:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 12 Jul 2024 18:38:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 12 Jul 2024 18:38:18 GMT
USER api-firewall
# Fri, 12 Jul 2024 18:38:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jul 2024 18:38:18 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f9757a387dfc29b82459ac4b98a5b04951b128fdae32a639c26a704b8da02`  
		Last Modified: Fri, 12 Jul 2024 18:38:27 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb084c1a532241d94ef310e9de9f60aa5532c652db91ae38f2d29c9f339ec7`  
		Last Modified: Fri, 12 Jul 2024 18:38:29 GMT  
		Size: 9.6 MB (9625850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe35beefbdfe5e877db79243b7a49f55ee8950f5fc5bc24843fed7eea884b94`  
		Last Modified: Fri, 12 Jul 2024 18:38:27 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:a47bc900220012cc8e6a00451540fa3f5013afbe290631e7223c80583ffd0723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:f12173c89fd0d79e4639e8c9688ab543240dec4b2c101ca9f021302b67b4b2ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14644893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164885ca2f842aeb00bcc632280236e9ce8b605980d438a210cf3aa7462e9215`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 18:19:30 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 12 Jul 2024 18:19:31 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 18:19:31 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 12 Jul 2024 18:19:31 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Fri, 12 Jul 2024 18:19:34 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 12 Jul 2024 18:19:34 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 12 Jul 2024 18:19:34 GMT
USER api-firewall
# Fri, 12 Jul 2024 18:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jul 2024 18:19:34 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d87dbfe46217158067587a65cde2c7b6b8aa41cc8ebdaa75a144ea29c306ee`  
		Last Modified: Fri, 12 Jul 2024 18:19:44 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11040d078ace94f003df18419efa7fabb30eb2e839293695b40743791dadc376`  
		Last Modified: Fri, 12 Jul 2024 18:19:45 GMT  
		Size: 11.0 MB (11019786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b40e476a957fc2a18034e7beead6988e59d91c3a525856b10ad98de6cfd141`  
		Last Modified: Fri, 12 Jul 2024 18:19:44 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:02b121ea61fc728d4027a84dfdcdfb29a133447418363ba6132339d6683a8f6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14430862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ade5ac3740069dfd306351c98e30ac51cd5deb8e15fa0116dedd8f6c510a838`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 18:40:48 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 12 Jul 2024 18:40:49 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 18:40:49 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 12 Jul 2024 18:40:49 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Fri, 12 Jul 2024 18:40:51 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 12 Jul 2024 18:40:52 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 12 Jul 2024 18:40:52 GMT
USER api-firewall
# Fri, 12 Jul 2024 18:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jul 2024 18:40:52 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc5b2e06412f2565fb493031051479b67cf55af7da844c2f8b1a4801f7ebb18`  
		Last Modified: Fri, 12 Jul 2024 18:41:00 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c2344c7e394ab5ddf90729d42d2264ccfbe2a4eff884afca1bc56bd60f433f`  
		Last Modified: Fri, 12 Jul 2024 18:41:01 GMT  
		Size: 10.3 MB (10340796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ac2d40b30e82a06c122f8d176aafd2f1b99675e53cbf9332b1ec97b24b2233`  
		Last Modified: Fri, 12 Jul 2024 18:40:59 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:d20c20fd418bbfcbdc30d21f7af2992ad6668c923a95646612f32b1846e3f5e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13096587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb388b92ecd302fc2c9bccae5e3c44049b838cc18dacc7c439897a671912281f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 18:38:14 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 12 Jul 2024 18:38:14 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 18:38:15 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 12 Jul 2024 18:38:15 GMT
ENV APIFIREWALL_VERSION=v0.7.4
# Fri, 12 Jul 2024 18:38:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='176bbcd6165de7dc03184fe64eb2018e129a130b41fd4f5908a81dd50fcabeb0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='24e67d30b5f32138a6b83dbaee886af2d4084c0b29e197b80378f4414b6079c9';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='75f92885364801f9af7c64cff91529745bad5d1f88ebe20053ab99311eab91e6';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 12 Jul 2024 18:38:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 12 Jul 2024 18:38:18 GMT
USER api-firewall
# Fri, 12 Jul 2024 18:38:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jul 2024 18:38:18 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f9757a387dfc29b82459ac4b98a5b04951b128fdae32a639c26a704b8da02`  
		Last Modified: Fri, 12 Jul 2024 18:38:27 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb084c1a532241d94ef310e9de9f60aa5532c652db91ae38f2d29c9f339ec7`  
		Last Modified: Fri, 12 Jul 2024 18:38:29 GMT  
		Size: 9.6 MB (9625850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe35beefbdfe5e877db79243b7a49f55ee8950f5fc5bc24843fed7eea884b94`  
		Last Modified: Fri, 12 Jul 2024 18:38:27 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
