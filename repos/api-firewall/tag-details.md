<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.8.0`](#api-firewall080)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.8.0`

```console
$ docker pull api-firewall@sha256:b3f45691f72d3b6a4044c2ce6e6b18ce73ed2d37965156064a145ff2890c69d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.8.0` - linux; amd64

```console
$ docker pull api-firewall@sha256:b5f875205cfcccbb31468e0fa85e5457da5d0244d5ad934edcee06e05095feca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14693591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3295d41216cb9802e46b8e817f46d4c0a76f0ff159c39f4cc67ebde38853f8e8`
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
# Fri, 06 Sep 2024 22:37:41 GMT
ENV APIFIREWALL_VERSION=v0.8.0
# Fri, 06 Sep 2024 22:37:43 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='014461629090796aeb06739580f36cfbbce9b81ad9d38abca37574151dcc800c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='94df745b7809cdba394e31fdf535525edc11d611651cd9fbc055cdb43c4bc509';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='f2dba11a265fd3aa7eccb73a2ae3379cd7915ae47ff84b5a93c597bad216e9a5';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 06 Sep 2024 22:37:44 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 06 Sep 2024 22:37:44 GMT
USER api-firewall
# Fri, 06 Sep 2024 22:37:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:37:44 GMT
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
	-	`sha256:b0e63a7de01bfc93541257d3a49db93f1f38eeb26e1b0e67fddccbd0ea70fef8`  
		Last Modified: Fri, 06 Sep 2024 22:37:53 GMT  
		Size: 11.1 MB (11068519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314f75fc60681bfd47545f986ee00c02710f1911b8b31aeffd8dc47357924193`  
		Last Modified: Fri, 06 Sep 2024 22:37:52 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.8.0` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:b130d2d002c861ecd53b44f51c51e29183a67bb3ebd2a861d2ce8f65ff29660f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14482465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422e78a3262e54aafee3efbb809475bffa1879a2983b7bf8beb86f087d0eb65`
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
# Fri, 06 Sep 2024 23:03:55 GMT
ENV APIFIREWALL_VERSION=v0.8.0
# Fri, 06 Sep 2024 23:03:58 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='014461629090796aeb06739580f36cfbbce9b81ad9d38abca37574151dcc800c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='94df745b7809cdba394e31fdf535525edc11d611651cd9fbc055cdb43c4bc509';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='f2dba11a265fd3aa7eccb73a2ae3379cd7915ae47ff84b5a93c597bad216e9a5';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 06 Sep 2024 23:03:58 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 06 Sep 2024 23:03:58 GMT
USER api-firewall
# Fri, 06 Sep 2024 23:03:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 23:03:58 GMT
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
	-	`sha256:f9799eeccef68a610fd17c3463f3e492457bca023261f5e70cf2399027542644`  
		Last Modified: Fri, 06 Sep 2024 23:04:06 GMT  
		Size: 10.4 MB (10393553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c165af2f3b12e85787855a3dcbb8d8851c772106bf1fa5c076639cc434c51e63`  
		Last Modified: Fri, 06 Sep 2024 23:04:04 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.8.0` - linux; 386

```console
$ docker pull api-firewall@sha256:7a510107597fb01fd15222f62461d7de9efe7f02e6f245df3648dec93c777a5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13143965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead520836ff522f6e0def56d8f0dccea9bd931eff063952f0a23c47546086d28`
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
# Tue, 20 Aug 2024 18:38:30 GMT
ENV APIFIREWALL_VERSION=v0.8.0
# Tue, 20 Aug 2024 18:38:33 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='014461629090796aeb06739580f36cfbbce9b81ad9d38abca37574151dcc800c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='94df745b7809cdba394e31fdf535525edc11d611651cd9fbc055cdb43c4bc509';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='f2dba11a265fd3aa7eccb73a2ae3379cd7915ae47ff84b5a93c597bad216e9a5';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 20 Aug 2024 18:38:33 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 20 Aug 2024 18:38:33 GMT
USER api-firewall
# Tue, 20 Aug 2024 18:38:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 18:38:33 GMT
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
	-	`sha256:09e9fafeb6abf4355b5cd312b42ab8d51c6d80db010e2511b6e892d08788e72f`  
		Last Modified: Tue, 20 Aug 2024 18:38:43 GMT  
		Size: 9.7 MB (9674630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decd6769656ddd05c2d15a220e5ecb99d23592d08edce491bc7d9b9559c4b6c9`  
		Last Modified: Tue, 20 Aug 2024 18:38:41 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:b3f45691f72d3b6a4044c2ce6e6b18ce73ed2d37965156064a145ff2890c69d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:b5f875205cfcccbb31468e0fa85e5457da5d0244d5ad934edcee06e05095feca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14693591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3295d41216cb9802e46b8e817f46d4c0a76f0ff159c39f4cc67ebde38853f8e8`
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
# Fri, 06 Sep 2024 22:37:41 GMT
ENV APIFIREWALL_VERSION=v0.8.0
# Fri, 06 Sep 2024 22:37:43 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='014461629090796aeb06739580f36cfbbce9b81ad9d38abca37574151dcc800c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='94df745b7809cdba394e31fdf535525edc11d611651cd9fbc055cdb43c4bc509';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='f2dba11a265fd3aa7eccb73a2ae3379cd7915ae47ff84b5a93c597bad216e9a5';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 06 Sep 2024 22:37:44 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 06 Sep 2024 22:37:44 GMT
USER api-firewall
# Fri, 06 Sep 2024 22:37:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 22:37:44 GMT
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
	-	`sha256:b0e63a7de01bfc93541257d3a49db93f1f38eeb26e1b0e67fddccbd0ea70fef8`  
		Last Modified: Fri, 06 Sep 2024 22:37:53 GMT  
		Size: 11.1 MB (11068519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314f75fc60681bfd47545f986ee00c02710f1911b8b31aeffd8dc47357924193`  
		Last Modified: Fri, 06 Sep 2024 22:37:52 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:b130d2d002c861ecd53b44f51c51e29183a67bb3ebd2a861d2ce8f65ff29660f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14482465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422e78a3262e54aafee3efbb809475bffa1879a2983b7bf8beb86f087d0eb65`
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
# Fri, 06 Sep 2024 23:03:55 GMT
ENV APIFIREWALL_VERSION=v0.8.0
# Fri, 06 Sep 2024 23:03:58 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='014461629090796aeb06739580f36cfbbce9b81ad9d38abca37574151dcc800c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='94df745b7809cdba394e31fdf535525edc11d611651cd9fbc055cdb43c4bc509';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='f2dba11a265fd3aa7eccb73a2ae3379cd7915ae47ff84b5a93c597bad216e9a5';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 06 Sep 2024 23:03:58 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 06 Sep 2024 23:03:58 GMT
USER api-firewall
# Fri, 06 Sep 2024 23:03:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 23:03:58 GMT
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
	-	`sha256:f9799eeccef68a610fd17c3463f3e492457bca023261f5e70cf2399027542644`  
		Last Modified: Fri, 06 Sep 2024 23:04:06 GMT  
		Size: 10.4 MB (10393553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c165af2f3b12e85787855a3dcbb8d8851c772106bf1fa5c076639cc434c51e63`  
		Last Modified: Fri, 06 Sep 2024 23:04:04 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:7a510107597fb01fd15222f62461d7de9efe7f02e6f245df3648dec93c777a5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13143965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead520836ff522f6e0def56d8f0dccea9bd931eff063952f0a23c47546086d28`
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
# Tue, 20 Aug 2024 18:38:30 GMT
ENV APIFIREWALL_VERSION=v0.8.0
# Tue, 20 Aug 2024 18:38:33 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='014461629090796aeb06739580f36cfbbce9b81ad9d38abca37574151dcc800c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='94df745b7809cdba394e31fdf535525edc11d611651cd9fbc055cdb43c4bc509';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='f2dba11a265fd3aa7eccb73a2ae3379cd7915ae47ff84b5a93c597bad216e9a5';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Tue, 20 Aug 2024 18:38:33 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Tue, 20 Aug 2024 18:38:33 GMT
USER api-firewall
# Tue, 20 Aug 2024 18:38:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 18:38:33 GMT
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
	-	`sha256:09e9fafeb6abf4355b5cd312b42ab8d51c6d80db010e2511b6e892d08788e72f`  
		Last Modified: Tue, 20 Aug 2024 18:38:43 GMT  
		Size: 9.7 MB (9674630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decd6769656ddd05c2d15a220e5ecb99d23592d08edce491bc7d9b9559c4b6c9`  
		Last Modified: Tue, 20 Aug 2024 18:38:41 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
