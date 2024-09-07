## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:39e12df3c235220c7800b88db9e3e7f759c0c7858f05b78ca600bbeab97ede6c
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
$ docker pull api-firewall@sha256:faec41a079fa227de63374169e78f0061661f82fdd3e406c1f0042ffa138bb9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13145052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4a3c0005d8f2c1399d78b027282b169d45650bb7652fce4141be0925975d17`
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
# Sat, 07 Sep 2024 01:57:21 GMT
ENV APIFIREWALL_VERSION=v0.8.0
# Sat, 07 Sep 2024 01:57:23 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='014461629090796aeb06739580f36cfbbce9b81ad9d38abca37574151dcc800c';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='94df745b7809cdba394e31fdf535525edc11d611651cd9fbc055cdb43c4bc509';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='f2dba11a265fd3aa7eccb73a2ae3379cd7915ae47ff84b5a93c597bad216e9a5';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 07 Sep 2024 01:57:24 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 07 Sep 2024 01:57:24 GMT
USER api-firewall
# Sat, 07 Sep 2024 01:57:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 01:57:24 GMT
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
	-	`sha256:f349c114c2a1607a94b89d4eb76860b014099d0dc329e406a168aafb6ceaf5e1`  
		Last Modified: Sat, 07 Sep 2024 01:57:33 GMT  
		Size: 9.7 MB (9674620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1da3039661b14dc96b482d9e1954d367b91b633577c84efdc8febb1d7e51423`  
		Last Modified: Sat, 07 Sep 2024 01:57:31 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
