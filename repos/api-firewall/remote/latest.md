## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:985a95ca09cc2b375a5fb8ed814f2ee3cd83caab3c4ffb7ac7af3ff7d793f05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:6fb0d8728da460f85f2cf91cbb62eae37759a67d7865321404379f5cade0a437
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14876711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ff6b5ecb039414eface7488167fd1022d03e02b782b276375210df258ba978`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:37:40 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 06 Sep 2024 22:37:40 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 22:37:41 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 16 Sep 2024 19:19:18 GMT
ENV APIFIREWALL_VERSION=v0.8.1
# Mon, 16 Sep 2024 19:19:20 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='cc81c8e0176d904471df3c3219fd92df6b317a211943c9c094c4c442aca1980c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='e668187589c8a6b74a57a66b061589c9bbae2441e6a1faa7c1560bb6d12c90f5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a1ed082eaf9bff778afef541f4b3651dc35032b5e0bfd559c04220a64edd20b9';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 16 Sep 2024 19:19:21 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 16 Sep 2024 19:19:21 GMT
USER api-firewall
# Mon, 16 Sep 2024 19:19:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 19:19:21 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf40d3d747019b351164402fd0d05781c2bfcac612fc6f83ea4684a63bd6885`  
		Last Modified: Fri, 06 Sep 2024 22:37:52 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f6b3ba48ac5ee00f9274fdb54a3ebda1315030a65cccb8ffeea87e8a8ae74d`  
		Last Modified: Mon, 16 Sep 2024 19:19:31 GMT  
		Size: 11.3 MB (11251637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e48aa65803502194b78c12a1cd7f46e405c6a1f04f6449e4ffe9f9985da6d9`  
		Last Modified: Mon, 16 Sep 2024 19:19:29 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:4391bb9660f853c9ca73a267d20b11fa012f944ea492e5064071b2ffbf76e6f4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14487059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6515131e7138c68463cd00f08483871fdcd75e24b3df095c99aca4633a7e7c69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:03:55 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 06 Sep 2024 23:03:55 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 23:03:55 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 16 Sep 2024 18:39:16 GMT
ENV APIFIREWALL_VERSION=v0.8.1
# Mon, 16 Sep 2024 18:39:19 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='cc81c8e0176d904471df3c3219fd92df6b317a211943c9c094c4c442aca1980c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='e668187589c8a6b74a57a66b061589c9bbae2441e6a1faa7c1560bb6d12c90f5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a1ed082eaf9bff778afef541f4b3651dc35032b5e0bfd559c04220a64edd20b9';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 16 Sep 2024 18:39:19 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 16 Sep 2024 18:39:19 GMT
USER api-firewall
# Mon, 16 Sep 2024 18:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 18:39:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65232210b9dc810dc66a876c2ed0208b0c13199f26228136e2fd2684553e72f3`  
		Last Modified: Fri, 06 Sep 2024 23:04:04 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bdf98248998b36f8d44307a6d20ee6a7fb40a1fb3f162b19ac656213e0d142`  
		Last Modified: Mon, 16 Sep 2024 18:39:28 GMT  
		Size: 10.4 MB (10398149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d13e481a005ceaeeb930ad9feb44246ba77a2f6d8fc8d07e97a408a5d448528`  
		Last Modified: Mon, 16 Sep 2024 18:39:26 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:5ed9d85e67ef95c024cc607cdd88fd4480c959e56e07e7d3e32aa6315fa6770b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13237437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a70856095ad67e9e1d092f51597f8f11ed1c226204a1f11a8681c8bf184b445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:20 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 07 Sep 2024 01:57:20 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Sep 2024 01:57:20 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 16 Sep 2024 18:38:13 GMT
ENV APIFIREWALL_VERSION=v0.8.1
# Mon, 16 Sep 2024 18:38:16 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='cc81c8e0176d904471df3c3219fd92df6b317a211943c9c094c4c442aca1980c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='e668187589c8a6b74a57a66b061589c9bbae2441e6a1faa7c1560bb6d12c90f5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a1ed082eaf9bff778afef541f4b3651dc35032b5e0bfd559c04220a64edd20b9';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 16 Sep 2024 18:38:16 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 16 Sep 2024 18:38:16 GMT
USER api-firewall
# Mon, 16 Sep 2024 18:38:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 18:38:16 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60e28bdd66504eebf65ca6892bddb641021505edb92d813701b39c212ef4cef`  
		Last Modified: Sat, 07 Sep 2024 01:57:30 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c5c29d126f7c0ef5346627aa98e5ec18408629fb4b2cb9d9aeedee1310aae1`  
		Last Modified: Mon, 16 Sep 2024 18:38:26 GMT  
		Size: 9.8 MB (9767008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3c14b33f62e98c5a8adf5b0390846d45276b3c9e048789e9cfdedc7d48934f`  
		Last Modified: Mon, 16 Sep 2024 18:38:24 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
